---
title: XTYP_EXECUTE Transaktion (Ddeml. h)
description: Ein Client verwendet die xtyp- \_ Execute-Transaktion, um eine Befehls Zeichenfolge an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client xType \_ Execute in der DDE clienttransaction-Funktion angibt.
ms.assetid: 6001eb7d-59c0-49ec-97ce-26132891188c
keywords:
- XTYP_EXECUTE Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_EXECUTE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff08bfa60d07f3b8333f1de808359f77984cbba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040863"
---
# <a name="xtyp_execute-transaction"></a>XYP- \_ Ausführungs Transaktion

Ein Client verwendet die **xtyp- \_ Execute** -Transaktion, um eine Befehls Zeichenfolge an den Server zu senden. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ Execute** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_EXECUTE            (0x0050 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*has* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themen Namen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hdata* 
</dt> <dd>

Ein Handle für die Befehls Zeichenfolge.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Server Rückruffunktion sollte **DDE \_ fakk** zurückgeben, wenn Sie diese Transaktion verarbeitet, **DDE \_ fausgelastet** , wenn Sie zu stark ausgelastet ist, um diese Transaktion zu verarbeiten, oder **DDE \_ fnotverarbeitete** , wenn Sie diese Transaktion ablehnt.

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn die Serveranwendung das Flag für die **CBF- \_ \_ Ausführung** in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.

Eine Anwendung muss das Daten handle freigeben, das während dieser Transaktion abgerufen wurde. Eine Anwendung muss jedoch die dem Daten Handle zugeordnete Befehls Zeichenfolge kopieren, wenn die Anwendung die Zeichenfolge verarbeiten muss, nachdem die Rückruffunktion zurückgegeben hat. Eine Anwendung kann die [**DDE GetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) -Funktion verwenden, um die Daten zu kopieren.

Da die meisten Client Anwendungen erwarten, dass eine Serveranwendung eine **XYP- \_ Execute** -Transaktion synchron ausführt, sollte ein Server versuchen, die gesamte Verarbeitung der **Xder- \_ Execute** -Transaktion entweder aus der DDE-Rückruffunktion oder durch die Rückgabe des **CBR- \_ Block** Rückgabecodes auszuführen. Wenn der *hdata* -Parameter ein Befehl ist, der den Server anweist, zu beenden, sollte der Server dies nach der Verarbeitung der **xD- \_ Ausführungs** Transaktion tun.

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

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

