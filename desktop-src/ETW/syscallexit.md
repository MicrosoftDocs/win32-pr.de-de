---
description: Diese Klasse ist die Ereignistypklasse für Beendigungsereignisse von Systemaufrufen. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: bb9a2770-f37b-4055-8811-59ba117adf82
title: SysCallExit-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallExit
- SysCallExit.SysCallNtStatus
api_type:
- NA
api_location: ''
ms.openlocfilehash: aa297ced8f6c0d17c0c01da9ce11705d30fe7448c8bc2f2ae6358ddc85f653be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102060"
---
# <a name="syscallexit-class"></a>SysCallExit-Klasse

Diese Klasse ist die Ereignistypklasse für Beendigungsereignisse von Systemaufrufen.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{52}, EventTypeName{"SysClExit"}]
class SysCallExit : PerfInfo
{
  uint32 SysCallNtStatus;
};
```

## <a name="members"></a>Member

Die **SysCallExit-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SysCallExit-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SysCallNtStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Format("x")
</dt> </dl>

Statuscode, der vom NT-Systemaufruf zurückgegeben wird.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




