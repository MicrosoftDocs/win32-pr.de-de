---
description: Gibt Statusinformationen zu einem Endpunkt-DLP-Vorgang an.
title: DLP_POSTOP_STATUS-Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_POSTOP_STATUS
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 6b8922bee5fb93ee4412833418a63c19dd311c8809cf64132a0f28fbe91d11bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610230"
---
# <a name="dlp_postop_status-structure"></a>DLP_POSTOP_STATUS-Struktur

Gibt Statusinformationen zu einem Endpunkt-DLP-Vorgang an.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_POSTOP_STATUS {
    
    DWORD Version;    
    BOOL OperationSuccess;  

} DLP_POSTOP_STATUS, *PDLP_POSTOP_STATUS; 
```


## <a name="members"></a>Member

<dl> <dt>

*Version* \[ In\]
</dt> <dd>

Ein DWORD, das die API-Version angibt. Dieser Wert sollte immer **DLP_POSTOP_STATUS_V_LATEST** sein. Diese Konstante wird in der Beispielheaderdatei endpointdlp.h im Artikel Verhindern von [Endpunktdatenverlust](endpointdlp-endpoint-data-loss-prevention.md) definiert.

</dd> </dl>

<dl> <dt>

*OperationSuccess* \[ In\]
</dt> <dd>

Eine BOOL, die angibt, ob der Öffnungsvorgang erfolgreich war.

</dd> </dl>





## <a name="remarks"></a>Bemerkungen


## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |
