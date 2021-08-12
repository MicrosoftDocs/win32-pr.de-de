---
title: XTYP_ADVSTART Transaktion (Ddeml.h)
description: Ein Client verwendet die XTYP \_ ADVSTART-Transaktion, um eine Advise-Schleife mit einem Server herzustellen.
ms.assetid: 8911e722-5656-4ca6-8b0a-6bdf8281611a
keywords:
- XTYP_ADVSTART Transaktion Data Exchange
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
ms.openlocfilehash: fb18bda3dce4db465045991e26cdc2d97ddd87ddc69c494ffaf103c566955da1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544759"
---
# <a name="xtyp_advstart-transaction"></a>XTYP \_ ADVSTART-Transaktion

Ein Client verwendet die **XTYP \_ ADVSTART-Transaktion,** um eine Advise-Schleife mit einem Server herzustellen. Eine dynamische Daten Exchange-Serverrückruffunktion [*(DdeCallback)*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, wenn ein Client **XTYP \_ ADVSTART** als *wType-Parameter* der [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) angibt.


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

*uFmt* 
</dt> <dd>

Das vom Client angeforderte Datenformat.

</dd> <dt>

*hconv* 
</dt> <dd>

Ein Handle für die Konversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Themennamen.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den Elementnamen.

</dd> <dt>

*hdata* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData1* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*dwData2* 
</dt> <dd>

Wird nicht verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Serverrückruffunktion sollte **TRUE** zurückgeben, um eine Advise-Schleife für das angegebene Themennamens- und Elementnamenpaar zu ermöglichen, oder **FALSE,** um die Advise-Schleife zu verweigern. Wenn die Rückruffunktion **TRUE** zurückgibt, bewirkt jeder nachfolgende Aufruf der [**DdePostAdvise-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) durch den Server im selben Themennamen- und Elementnamenpaar, dass das System [**XTYP \_ ADBENACHRICHTIGUNGQ-Transaktionen**](xtyp-advreq.md) an den Server sendet.

## <a name="remarks"></a>Hinweise

Wenn ein Client eine Advise-Schleife für einen Themennamen, Einen Elementnamen und ein Datenformat für eine bereits eingerichtete Advise-Schleife an fordert, erstellt die dynamische Daten Exchange Management Library (DDEML) keine doppelte Advise-Schleife, sondern ändert stattdessen die Advise-Schleifenflags (**XTYPF \_ ACKREQ** und **XTYPF \_ NODATA**) so, dass sie mit der neuesten Anforderung übereinstimmen.

Diese Transaktion wird gefiltert, wenn die Serveranwendung das **CBF \_ FAIL \_ ADVISES-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

**Referenz**
</dt> <dt>

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

