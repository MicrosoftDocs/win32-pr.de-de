---
title: XTYP_POKE Transaktion (Ddeml.h)
description: Ein Client verwendet die \_ XTYP-TRANSAKTION, um nicht angeforderte Daten an den Server zu senden. Eine dynamische Daten Exchange (DDE)-Serverrückruffunktion, DdeCallback, empfängt diese Transaktion, wenn ein Client XTYP \_ CSVE in der DdeClientTransaction-Funktion angibt.
ms.assetid: 63c6115e-24f8-4f35-8397-8be63110b21f
keywords:
- XTYP_POKE transaktion Exchange
topic_type:
- apiref
api_name:
- XTYP_POKE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a179f4130ae06c4548b52586d6086201c2d832a158cef877d9aaf524160f4b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117914750"
---
# <a name="xtyp_poke-transaction"></a>\_XTYP-TRANSACTIONE-Transaktion

Ein Client verwendet die **\_ XTYP-TRANSAKTION,** um nicht angeforderte Daten an den Server zu senden. Eine dynamische Daten Exchange (DDE)-Serverrückruffunktion, [*DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, wenn ein Client **XTYP \_ CABE** in der [**DdeClientTransaction-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) angibt.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_POKE               (0x0090 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Das Format der vom Server gesendeten Daten.

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

Ein Handle für die Daten, die der Client an den Server sendet.

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

Eine Serverrückruffunktion sollte das **\_ DDE-FACK-Flag** zurückgeben, wenn diese Transaktion verarbeitet wird, das **\_ DDE-FBUSY-Flag,** wenn es zu ausgelastet ist, um diese Transaktion zu verarbeiten, oder das **DDE \_ FNOTPROCESSED-Flag,** wenn diese Transaktion abgelehnt wird.

## <a name="remarks"></a>Hinweise

Diese Transaktion wird gefiltert, wenn die Serveranwendung in der [**DdeInitialize-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) das **CBF \_ FAIL FAIL \_ FAILES-Flag** angegeben hat.

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

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange-Verwaltungsbibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

