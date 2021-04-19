---
description: Ordnet eine DLP-Aktion (Data Loss Prevention) eines Endpunkts einer Erzwingungsebene zu.
title: DLP_APP_OP_ENLIGHTENED_LEVEL-Struktur (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495789"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL-Struktur

Ordnet eine DLP-Aktion (Data Loss Prevention) eines Endpunkts einer Erzwingungsebene zu.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Members

<dl> <dt>

*Vorgang* \[ In\]
</dt> <dd>

Ein Wert aus der [DlpActionType-Enumeration,](endpointdlp-dlpactiontype.md) der den DLP-Endpunktaktionstyp angibt.

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[ In\]
</dt> <dd>

Ein Wert aus [DlpAppEnforceLevel,](endpointdlp-dlpappenforcelevel.md) der die Erzwingungsebene für den zugeordneten Endpunkt-DLP-Aktionstyp angibt.

</dd> </dl>





## <a name="remarks"></a>Bemerkungen

Übergeben Sie ein Array dieser Strukturen an [DlpInitializeEnforcementMode,](endpointdlp-dlpinitializeenforcementmode.md) um den Erzwingungsmodus für eine Reihe von Endpunkt-DLP-Vorgängen festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

