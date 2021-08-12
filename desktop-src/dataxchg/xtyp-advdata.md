---
title: XTYP_ADVDATA Transaktion (Ddeml.h)
description: Informiert den Client darüber, dass sich der Wert des Datenelements geändert hat. Die dynamische Daten Exchange -Clientrückruffunktion (DDE), DdeCallback, empfängt diese Transaktion, nachdem eine Advise-Schleife mit einem Server hergestellt wurde.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA Transaktion Data Exchange
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9bf3f3b94f4454547d987ab6536929d1fe2998e7dc0394564143536f1da28d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544865"
---
# <a name="xtyp_advdata-transaction"></a>XTYP \_ ADVDATA-Transaktion

Informiert den Client darüber, dass sich der Wert des Datenelements geändert hat. Die dynamische Daten Exchange -Clientrückruffunktion [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt diese Transaktion, nachdem eine Advise-Schleife mit einem Server hergestellt wurde.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Das Formatatom der vom Server gesendeten Daten.

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

Ein Handle für die Daten, die dem Themennamen- und Elementnamenpaar zugeordnet sind. Dieser Parameter ist **NULL,** wenn der Client das **XTYPF \_ NODATA-Flag** angegeben hat, als er die Advise-Schleife angefordert hat.

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

Eine DDE-Rückruffunktion sollte **DDE \_ FACK** zurückgeben, wenn sie diese Transaktion verarbeitet, **DDE \_ FBUSY,** wenn sie zu ausgelastet ist, um diese Transaktion zu verarbeiten, oder **DDE \_ FNOTPROCESSED,** wenn diese Transaktion abgelehnt wird.

## <a name="remarks"></a>Hinweise

Eine Anwendung darf das während dieser Transaktion erhaltene Datenhand handle nicht frei geben. Eine Anwendung muss jedoch die daten kopieren, die dem Datenhand handle zugeordnet sind, wenn die Anwendung die Daten verarbeiten muss, nachdem die Rückruffunktion zurückgegeben wurde. Eine Anwendung kann die [**DdeGetData-Funktion verwenden,**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) um die Daten zu kopieren.

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

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

