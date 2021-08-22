---
title: XTYP_ADVSTOP Transaktion (Ddeml.h)
description: Ein Client verwendet die XTYP \_ ADVSTOP-Transaktion, um eine Advise-Schleife mit einem Server zu beenden. Eine dynamische Daten Exchange (DDE)-Serverrückruffunktion, DdeCallback, empfängt diese Transaktion, wenn ein Client XTYP \_ ADVSTOP in der DdeClientTransaction-Funktion angibt.
ms.assetid: 67dfa463-6a44-43a5-93be-a39c19c87c1c
keywords:
- XTYP_ADVSTOP Exchange von Transaktionsdaten
topic_type:
- apiref
api_name:
- XTYP_ADVSTOP
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37e81f1fe407186410e604a259f6e8039c074da039fc23b2f8a090c34ff58154
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544769"
---
# <a name="xtyp_advstop-transaction"></a>XTYP \_ ADVSTOP-Transaktion

Ein Client verwendet die **XTYP \_ ADVSTOP-Transaktion,** um eine Advise-Schleife mit einem Server zu beenden. Eine dynamische Daten Exchange (DDE)-Serverrückruffunktion, [*DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, wenn ein Client **XTYP \_ ADVSTOP** in der [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) angibt.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_ADVSTOP            (0x0040 | XCLASS_NOTIFICATION)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Das Datenformat, das der beendeten Advise-Schleife zugeordnet ist.

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

## <a name="remarks"></a>Hinweise

Diese Transaktion wird gefiltert, wenn die Serveranwendung das **CBF \_ FAIL \_ FILTERS-Flag** in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) angegeben hat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>Ddeml.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

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

[dynamische Daten Exchange-Verwaltungsbibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

