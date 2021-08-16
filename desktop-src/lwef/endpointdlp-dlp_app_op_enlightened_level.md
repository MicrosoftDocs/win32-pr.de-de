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
ms.openlocfilehash: e47fa7705701701af2fc0832c5ea27cfdc7d1e67948ec095f3c24837a93de18b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610480"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL Struktur

Ordnet eine DLP-Aktion (Data Loss Prevention) eines Endpunkts einer Erzwingungsebene zu.

## <a name="syntax"></a>Syntax


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>Member

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





## <a name="remarks"></a>Hinweise

Übergeben Sie ein Array dieser Strukturen an [DlpInitializeEnforcementMode,](endpointdlp-dlpinitializeenforcementmode.md) um den Erzwingungsmodus für eine Reihe von Endpunkt-DLP-Vorgängen festzulegen.

## <a name="requirements"></a>Anforderungen



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

