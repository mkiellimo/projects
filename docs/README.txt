README
======

Il Backend è basato sull oggetto di tipo validation che usa le @assert impostate nelle entity per validare la chiamata che gli arriva dall'ecommerce.
Questo oggetto può rispondere o con un oggetto doctrine che poi mi servirà per salvare eeffettivamente i campi a db, oppure con un array che userò per la presentazione del dato sul frontend.
L'oggetto validation rinomina i capi qualora ci sia impostato un eventuale mapping e li valida.
Se il validatore trova delle differenze ripetto a come mi aspetto l'ogetto order della richiesta solleva un eccezione mandando un email e rispondendo con un json con un errore
HTTP_BAD_REQUEST.

http://philipp_plein.local/api/order_search :
Chiamata per inserire gli ordini a Db

la chiamata per vedere gli ordini che ho salavto a Db è la seguente:
http://philipp_plein.local/api/get_order
PARAMS : id_order
TYPE GET
Viene richiamata su ogni riga premendo il tasto "refresh"
Per la demo funzionarà solo per il primo ordine dato che ho mokkato la risposta dell e-commere nel controller.
