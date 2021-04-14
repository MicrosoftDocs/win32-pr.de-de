---
title: XTYP_REGISTER Transaktion (Ddeml. h)
description: Eine dynamischer Datenaustausch (DDE)-Rückruffunktion (ddecallback) empfängt den xtyp- \_ Register Transaktionstyp, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion "DDENameService" zum Registrieren eines Dienst namens verwendet, oder wenn eine nicht-Ddeml-Anwendung gestartet wird, die das System Thema unterstützt.
ms.assetid: 465e9c10-1526-4e2a-8a46-5984043f5a93
keywords:
- XTYP_REGISTER Transaktionsdaten Austausch
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
ms.openlocfilehash: cd56bf4f5ac2b4eb0f714e5348174942f685c2ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476179"
---
# <a name="xtyp_register-transaction"></a>XYP- \_ Register Transaktion

Eine dynamischer Datenaustausch (DDE)-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) empfängt den **xtyp- \_ Register** Transaktionstyp, wenn eine Ddeml-Serveranwendung (dynamischer Datenaustausch Management Library) die Funktion " [**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) " zum Registrieren eines Dienst namens verwendet, oder wenn eine nicht-Ddeml-Anwendung gestartet wird, die das System Thema unterstützt.


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

*UF* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*has* 
</dt> <dd>

Nicht verwendet.

</dd> <dt>

*hsz1* 
</dt> <dd>

Ein Handle für den Basis Dienstnamen, der registriert wird.

</dd> <dt>

*hsz2* 
</dt> <dd>

Ein Handle für den instanzspezifischen Dienstnamen, der registriert wird.

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

## <a name="remarks"></a>Bemerkungen

Diese Transaktion wird gefiltert, wenn die Anwendung das Flag " **CBF \_ Skip \_ Registrierungen** " in der [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion angegeben hat.

Eine-Anwendung kann diesen Transaktionstyp nicht blockieren; der Rückgabecode des **CBR- \_ Blocks** wird ignoriert.

Eine Anwendung sollte den *hsz1* -Parameter verwenden, um den Dienstnamen zur Liste der Server hinzuzufügen, die dem Benutzer zur Verfügung stehen. Eine Anwendung sollte den *hsz2* -Parameter verwenden, um die gestartete Anwendungs Instanz zu identifizieren.

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

[**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DDENameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice)
</dt> <dt>

**Licher**
</dt> <dt>

[dynamischer Datenaustausch-Verwaltungs Bibliothek](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

