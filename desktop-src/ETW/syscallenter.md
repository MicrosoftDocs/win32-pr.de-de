---
description: Diese Klasse ist die Ereignistypklasse für Enter-Ereignisse des Systemaufrufs. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 1ab32977-3f59-4816-b311-67142475dff2
title: SysCallEnter-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SysCallEnter
- SysCallEnter.SysCallAddress
api_type:
- NA
api_location: ''
ms.openlocfilehash: 53389fb4c5d78316020a145999ac13d2c8abfbf7474efaad802e29632d40beaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083190"
---
# <a name="syscallenter-class"></a>SysCallEnter-Klasse

Diese Klasse ist die Ereignistypklasse für Enter-Ereignisse des Systemaufrufs.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[EventType{51}, EventTypeName{"SysClEnter"}]
class SysCallEnter : PerfInfo
{
  uint32 SysCallAddress;
};
```

## <a name="members"></a>Member

Die **SysCallEnter-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **SysCallEnter-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**SysCallAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: WmiDataId(1), Zeiger
</dt> </dl>

Adresse des NT-Funktionsaufrufs, der eingegeben wird.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/> |



 

 




