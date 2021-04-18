---
description: Die TSPI-Zeile \_ senddialoginstancedata bewirkt, dass TAPI die Funktion "tuispi \_ providergenericdialogdata" in der Benutzeroberflächen-DLL aufruft, die mit "htdlginst" verknüpft ist, und übergibt dabei den Parameter Block, auf den lpparser zeigt, mit der Länge "dwSize".
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: LINE_SENDDIALOGINSTANCEDATA Meldung (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0af7ae5bfc942d4408ac5ce2438cd9a88c1f1f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371327"
---
# <a name="line_senddialoginstancedata-message"></a>Zeile \_ senddialoginstancedata

Die TSPI **-Zeile \_ senddialoginstancedata** bewirkt, dass TAPI die Funktion " [**tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) " in der Benutzeroberflächen-DLL aufruft, die mit " *htdlginst*" verknüpft ist, und übergibt dabei den Parameter Block, auf den *lpparser* zeigt, mit der Länge " *dwSize*".


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*"htdlginst"* 
</dt> <dd>

Die htapidialoginstance, die an den Dienstanbieter zurückgegeben wurde, als die Dialogfeld Instanz mithilfe der Zeile ' ' erstellt wurde. [**\_**](line-createdialoginstance.md)

</dd> <dt>

*lpparser* 
</dt> <dd>

Ein Zeiger auf einen anbieterspezifischen Parameter Block, der der Benutzeroberflächen-DLL-Funktion " [**tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) " übermittelt wird, deren Größe von *dwSize* angegeben wird. Wenn dieser Parameter auf **null** festgelegt ist, ist dies eine Anforderung zum sofortigen Schließen des Dialog Felds und zum Bereinigen (die Benutzeroberflächen-DLL sollte während dieser Bereinigung nicht " [**tuispidllcallback**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) " aufrufen).

</dd> <dt>

*dwSize* 
</dt> <dd>

Die Größe des Parameter Blocks in Bytes, der an die Benutzeroberflächen-DLL übermittelt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2,0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Tuispidllcallback**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**Tuispi \_ providergenericdialogdata**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**Zeile " \_ kreatedialoginstance"**](line-createdialoginstance.md)
</dt> </dl>

 

