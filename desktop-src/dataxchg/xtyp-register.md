---
title: XTYP_REGISTER Transaktion (Ddeml.h)
description: Eine dynamische Daten Exchange-Rückruffunktion (DDE), DdeCallback, empfängt den XTYP REGISTER-Transaktionstyp, wenn eine DDEML-Serveranwendung (dynamische Daten Exchange Management Library) die DdeNameService-Funktion zum Registrieren eines Dienstnamens verwendet oder wenn eine Nicht-DDEML-Anwendung gestartet wird, die das \_ Thema System unterstützt.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER Transaktion Data Exchange
topic_type:
- apiref
api_name:
- XTYP_REGISTER
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79c4ffdb48b7a69109659e65d816b4ab146a1f38bde976e7f8330746f564bc64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544749"
---
# <a name="xtyp_register-transaction"></a>XTYP \_ REGISTER-Transaktion

Eine dynamische Daten Exchange-Rückruffunktion [*(DDE), DdeCallback,*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)empfängt den **XTYP REGISTER-Transaktionstyp, \_** wenn eine DDEML-Serveranwendung (dynamische Daten Exchange Management Library) die [**DdeNameService-Funktion**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) verwendet, um einen Dienstnamen zu registrieren, oder wenn eine Nicht-DDEML-Anwendung gestartet wird, die das Thema System unterstützt.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_REGISTER           (0x00A0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uType* 
</dt> <dd>

Der Transaktionstyp:

</dd> <dt>

*uFmt* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hconv* 
</dt> <dd>

Wird nicht verwendet.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Basisdienstnamen, der registriert wird.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den instanzspezifischen Dienstnamen, der registriert wird.

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

Diese Transaktion wird gefiltert, wenn die Anwendung das **CBF \_ SKIP \_ REGISTRATIONS-Flag** in der [**DdeInitialize-Funktion angegeben**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) hat.

Eine Anwendung kann diesen Transaktionstyp nicht blockieren. Der **CBR \_ BLOCK-Rückgabecode** wird ignoriert.

Eine Anwendung sollte den *Parameter hsz1* verwenden, um den Dienstnamen der Liste der Server hinzuzufügen, die für den Benutzer verfügbar sind. Eine Anwendung sollte den *hsz2-Parameter* verwenden, um zu identifizieren, welche Anwendungsinstanz gestartet wurde.

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

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[dynamische Daten Exchange Management Library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

