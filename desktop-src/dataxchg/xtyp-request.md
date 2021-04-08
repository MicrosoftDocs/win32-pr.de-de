---
title: XTYP_REQUEST Transaktion (Ddeml. h)
description: Ein Client verwendet die XYP- \_ Anforderungs Transaktion, um Daten von einem Server anzufordern. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion (DDE Callback) empfängt diese Transaktion, wenn ein Client eine \_ xType-Anforderung in der DDE clienttransaction-Funktion angibt.
ms.assetid: e776b995-6a64-4398-9e29-c151f3ef4c1d
keywords:
- XTYP_REQUEST Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_REQUEST
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e902c1525a8837f6ace6ef9bceb0607a608cda
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740328"
---
# <a name="xtyp_request-transaction"></a>XYP- \_ Anforderungs Transaktion

Ein Client verwendet die **XYP- \_ Anforderungs** Transaktion, um Daten von einem Server anzufordern. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*DDE Callback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client eine **xType- \_ Anforderung** in der [**DDE clienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.


```C++
#define     XCLASS_DATA              0x2000
#define     XTYP_REQUEST            (0x00B0 | XCLASS_DATA          )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Das Format, in dem der Serverdaten an den Client übermitteln soll.

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

Ein Handle für den Elementnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Nicht verwendet.

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

Der Server sollte die [**ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) -Funktion aufrufen, um ein Daten Handle zu erstellen, das die Daten identifiziert und dann das Handle zurückgibt. Der Server sollte **null** zurückgeben, wenn die Transaktion nicht abgeschlossen werden kann. Wenn der Server **null** zurückgibt, empfängt der Client ein DDE-Flag mit der Bezeichnung "DDE" \_ .

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn die Serveranwendung das Flag " **CBF \_ Fail \_ Requests** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.

Wenn die Reaktion auf diese Transaktion lange Verarbeitung erfordert, kann der Server den Rückgabecode des CBR-Blocks zurückgeben, \_ um zukünftige Transaktionen für die aktuelle Konversation anzuhalten und die Transaktion dann asynchron zu verarbeiten. Nachdem der Server beendet wurde und die Daten an den Client übergeben werden können, kann der Server die [**DDE enablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback) -Funktion zum Fortsetzen der Konversation aufruft.

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

[**Ddecreatedatahandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DDE enablecallback**](/windows/desktop/api/Ddeml/nf-ddeml-ddeenablecallback)
</dt> <dt>

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

