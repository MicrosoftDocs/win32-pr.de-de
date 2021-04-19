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
ms.openlocfilehash: c0221926700fc8960de5ef4d25c36136c3fc9737
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495581"
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


## <a name="members"></a>Members

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
