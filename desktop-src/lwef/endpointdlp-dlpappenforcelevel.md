---
description: Gibt die Erzwingungsebene eines Endpunkt-DLP-Vorgangs (Data Loss Prevention, Verhinderung von Datenverlust) an.
title: DlpAppEnforceLevel-Enumeration (endpointdlp.h)
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 99bd06a41c88ff0b5a02b9b329877c015aea7dfb3fdbc58fea3c2e305829faf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349350"
---
# <a name="dlpappenforcelevel-enumeration"></a>DlpAppEnforceLevel-Enumeration

Gibt die Erzwingungsebene eines Endpunkt-DLP-Vorgangs (Data Loss Prevention, Verhinderung von Datenverlust) an.

## <a name="syntax"></a>Syntax


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>Konstanten

<dl> <dt>

*DlpAppEnforceLevelNone* \[ In\]
</dt> <dd>

Keine Erzwingung durch die App. Das DLP-System erzwingt den Vorgang.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[ In\]
</dt> <dd>

Die Tne-App verwendet die DLP-APIs, um das DLP-System über den Vorgang zu benachrichtigen. Das DLP-System erzwingt den Vorgang.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[ In\]
</dt> <dd>

Wird in der aktuellen Version nicht unterstützt.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[ In\]
</dt> <dd>

Wird in der aktuellen Version nicht unterstützt.

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[ In\]
</dt> <dd>

Der Höchstwert der Enumeration.

</dd> </dl>



## <a name="remarks"></a>Hinweise

Werte aus dieser Enumeration werden von der [DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md) verwendet.


## <a name="requirements"></a>Anforderungen



| Anforderung          |    Wert                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1809 (10.0; Build 17763)           |

