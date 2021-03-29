---
description: Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-End-wait. Die folgende Syntax wird durch den MOF-Code vereinfacht.
ms.assetid: 89a357dd-c217-4b55-994a-4252fa3cae1c
title: ALPC_Unwait-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC_Unwait
- ALPC_Unwait.Status
api_type:
- NA
api_location: ''
ms.openlocfilehash: f0846eae1ebb88e8892f1fe9b8dd07fd1be9d146
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527056"
---
# <a name="alpc_unwait-class"></a>ALPC- \_ Klasse "Unwait"

Diese Klasse ist die Ereignistyp Klasse für Ereignisse von ALPC-End-wait.

Die folgende Syntax wird durch den MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType(37), EventTypeName("ALPC-Unwait")]
class ALPC_Unwait : ALPC
{
  uint32 Status;
};
```

## <a name="members"></a>Member

Die **ALPC- \_ Unwait** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ALPC- \_ Unwait** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Status**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Status des warte Vorgangs.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/> |



 

 




