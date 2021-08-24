---
title: XTYP_XACT_COMPLETE Transaktion (Ddeml.h)
description: Die Clientrückruffunktion DdeCallback (dynamische Daten Exchange Client Callback) empfängt die XTYP \_ XACT \_ COMPLETE-Transaktion, wenn eine asynchrone Transaktion, die durch einen Aufruf der DdeClientTransaction-Funktion initiiert wurde, abgeschlossen wurde.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE Exchange von Transaktionsdaten
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3833207371bbfab059f67ecb5bdb72b77334ef3ffc73618e013ce137835c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678010"
---
# <a name="xtyp_xact_complete-transaction"></a>XTYP \_ XACT \_ COMPLETE-Transaktion

Eine dynamische Daten Exchange (DDE)-Clientrückruffunktion, [*DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt die **XTYP \_ XACT \_ COMPLETE-Transaktion,** wenn eine asynchrone Transaktion, die durch einen Aufruf der [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) initiiert wurde, abgeschlossen wurde.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Das Format der Daten, die der abgeschlossenen Transaktion zugeordnet sind (falls zutreffend) oder **NULL,** wenn während der Transaktion keine Daten ausgetauscht wurden.

</dd> <dt>

*hconv* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themennamen, der an der abgeschlossenen Transaktion beteiligt ist.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen, der an der abgeschlossenen Transaktion beteiligt ist.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für die Daten, die an der abgeschlossenen Transaktion beteiligt sind, falls zutreffend. Wenn die Transaktion erfolgreich war, aber keine Daten umfasste, ist dieser Parameter **TRUE.** Dieser Parameter ist **NULL,** wenn die Transaktion nicht erfolgreich war.

</dd> <dt>

*dwData1* 
</dt> <dd>

Der Transaktionsbezeichner der abgeschlossenen Transaktion.

</dd> <dt>

*dwData2* 
</dt> <dd>

Alle anwendbaren **\_ DDE-Statusflags** im unteren Wort. Dieser Parameter bietet Unterstützung für Anwendungen, die von **DDE \_ APPSTATUS-Bits** abhängig sind. Es wird empfohlen, dass Anwendungen diese Bits nicht mehr verwenden, da sie in zukünftigen Versionen der DDEML möglicherweise nicht mehr unterstützt werden.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Eine Anwendung darf das datenhandle, das während dieser Transaktion abgerufen wurde, nicht freigeben. Eine Anwendung muss jedoch die dem Datenhandle zugeordneten Daten kopieren, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben wurde. Eine Anwendung kann die [**DdeGetData-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) verwenden, um die Daten zu kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange-Verwaltungsbibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

