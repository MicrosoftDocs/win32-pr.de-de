---
description: Die TSPI LINE \_ SENDDIALOGINSTANCEDATA-Nachricht bewirkt, dass TAPI in der \_ UI-DLL, die htDlgInst zugeordnet ist, die FUNKTION MODISPI-AnbieterGenericDialogData aufruft und dabei den Parameterblock übergibt, auf den lpParams mit der Länge dwSize zeigt.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: LINE_SENDDIALOGINSTANCEDATA Meldung (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b955d890c385894467fa0f8f3f93ec50856c746c72f0957ecbe33af203917bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140133"
---
# <a name="line_senddialoginstancedata-message"></a>LINE \_ SENDDIALOGINSTANCEDATA-Nachricht

Die TSPI **LINE \_ SENDDIALOGINSTANCEDATA-Nachricht** bewirkt, dass TAPI in der UI-DLL, die *htDlgInst* zugeordnet ist, die [**FUNKTION MODISPI-AnbieterGenericDialogData \_**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) aufruft. Dabei wird der Parameterblock übergeben, auf den *lpParams* zeigt, der Länge *dwSize*.


```C++
            
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*htDlgInst* 
</dt> <dd>

Die HTAPIDIALOGINSTANCE, die an den Dienstanbieter zurückgegeben wurde, als die Dialogfeldinstanz mit [**LINE \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)erstellt wurde.

</dd> <dt>

*lpParams* 
</dt> <dd>

Zeiger auf einen anbieterspezifischen Parameterblock, der an die [**UI-DLL-DLL-FUNKTION DLLsPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) übermittelt wird, deren Größe von *dwSize* angegeben wird. Wenn dieser Parameter auf **NULL** festgelegt ist, ist dies eine Anforderung zum sofortigen Schließen des Dialogfelds und zum Bereinigen (die UI-DLL sollte während dieser Bereinigung [**NICHT DEN AUFRUF VON QUOTSPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) ausführen).

</dd> <dt>

*dwSize* 
</dt> <dd>

Die Größe des Parameterblocks in Bytes, der an die UI-DLL übermittelt werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|-----------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 2.0 oder höher<br/>                                             |
| Header<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**WIESSPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**\_PROVIDERSSPI-AnbieterGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**LINE \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md)
</dt> </dl>

 

