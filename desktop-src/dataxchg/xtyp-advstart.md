---
title: XTYP_ADVSTART Transaktion (Ddeml. h)
description: Ein Client verwendet die xtipp- \_ advstart-Transaktion, um eine Empfehlung-Schleife mit einem Server einzurichten.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_ADVSTART
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 852351ad902a0552ee012d6c1e5c4d61501e6e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741857"
---
# <a name="xtyp_advstart-transaction"></a>Xttyp- \_ advstart-Transaktion

Ein Client verwendet die **xtipp- \_ advstart** -Transaktion, um eine Empfehlung-Schleife mit einem Server einzurichten. Eine dynamischer Datenaustausch (DDE)-Server Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt diese Transaktion, wenn ein Client **xType \_ advstart** als *wType* -Parameter der [**ddeclienttransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) -Funktion angibt.


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYP_ADVSTART           (0x0030 | XCLASS_BOOL          )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*UF* 
</dt> <dd>

Das vom Client angeforderte Datenformat.

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

Eine Server Rückruffunktion sollte **true** zurückgeben, um eine Empfehlung-Schleife für den angegebenen Themen Namen und das Element namens paar zuzulassen, oder **false** , um die Empfehlung-Schleife abzulehnen. Wenn die Rückruffunktion **true** zurückgibt, bewirkt jeder nachfolgende Aufruf der [**ddepostadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) -Funktion durch den Server für denselben Themen Namen und dasselbe Elementnamen Paar, dass das System [**xD \_ advreq**](xtyp-advreq.md) -Transaktionen an den Server sendet.

## <a name="remarks"></a>Bemerkungen

Wenn ein Client eine Empfehlung-Schleife für einen Themen Namen, Elementnamen und ein Datenformat für eine bereits erstellte Empfehlung-Schleife anfordert, wird von der dynamischer Datenaustausch Management Library (Ddeml) keine doppelte Empfehlung-Schleife erstellt, sondern die Empfehlung-Schleifen-Flags (**xtypf \_ ackreq** und **xtypf \_ NODATA**) so geändert, dass Sie mit der aktuellen Anforderung übereinstimmen.

Diese Transaktion wird gefiltert, wenn von der Serveranwendung das Flag " **CBF \_ Fail \_** " in der Funktion " [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) " angegeben wurde.

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

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DDE postadvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

