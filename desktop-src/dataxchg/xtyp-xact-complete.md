---
title: XTYP_XACT_COMPLETE Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Client Rückruffunktion (DDE Callback) empfängt die vollständige xD- \_ \_ Transaktion, wenn eine asynchrone Transaktion, die durch einen-Aufrufs der DDE clienttransaction-Funktion initiiert wurde, abgeschlossen wurde.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE Transaktionsdaten Austausch
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
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338717"
---
# <a name="xtyp_xact_complete-transaction"></a>\_Xttxact- \_ Transaktion abgeschlossen

Eine dynamischer Datenaustausch (DDE)-Client Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt die **\_ \_ vollständige xD** -Transaktion, wenn eine asynchrone Transaktion, die durch einen-Aufrufs der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion initiiert wurde, abgeschlossen wurde.


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

*UF* 
</dt> <dd>

Das Format der Daten, die der abgeschlossenen Transaktion (falls zutreffend) zugeordnet sind, oder **null** , wenn während der Transaktion keine Daten ausgetauscht wurden.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themen Namen, der an der abgeschlossenen Transaktion beteiligt ist.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen, der an der abgeschlossenen Transaktion beteiligt ist.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für die Daten, die an der abgeschlossenen Transaktion beteiligt sind, falls zutreffend. Wenn die Transaktion erfolgreich war, aber keine Daten umfasste, ist dieser Parameter **true**. Dieser Parameter ist **null** , wenn die Transaktion nicht erfolgreich war.

</dd> <dt>

*dwData1* 
</dt> <dd>

Der Transaktions Bezeichner der abgeschlossenen Transaktion.

</dd> <dt>

*dwData2* 
</dt> <dd>

Alle anwendbaren **DDE \_** -Statusflags im unteren Wort. Dieser Parameter bietet Unterstützung für Anwendungen, die von **DDE \_ appstatus** Bits abhängig sind. Es wird empfohlen, dass Anwendungen diese Bits nicht mehr verwenden, da Sie möglicherweise in zukünftigen Versionen der Ddeml nicht mehr unterstützt werden.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Eine Anwendung darf das Daten handle, das während dieser Transaktion abgerufen wurde, nicht freigeben. Eine Anwendung muss jedoch die Daten kopieren, die dem Daten Handle zugeordnet sind, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat. Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

