---
description: Die übergeordnete Klasse, von der alle Systemereignis-Ablaufverfolgungsklassen abgeleitet werden. Die folgende Syntax wird durch einen MOF-Code vereinfacht.
ms.assetid: 27979d9c-eca7-426f-8f8e-99443e5a0188
title: MSNT_SystemTrace-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSNT_SystemTrace
- MSNT_SystemTrace.Flags
api_type:
- NA
api_location: ''
ms.openlocfilehash: c083f7a2336a374e8009af2ba8094d57d9826197e16b7577aaf3b00a4c035173
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829620"
---
# <a name="msnt_systemtrace-class"></a>MSNT \_ SystemTrace-Klasse

Die übergeordnete Klasse, von der alle Systemereignis-Ablaufverfolgungsklassen abgeleitet werden.

Die folgende Syntax wird durch einen MOF-Code vereinfacht.

## <a name="syntax"></a>Syntax

``` syntax
[Guid("{9e814aad-3204-11d2-9a82-006008a86939}")]
class MSNT_SystemTrace : EventTrace
{
  uint32 Flags;
};
```

## <a name="members"></a>Member

Die **MSNT \_ SystemTrace-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSNT \_ SystemTrace-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Flags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **DefineValues{"EVENT \_ TRACE \_ FLAG \_ PROCESS", "EVENT \_ TRACE FLAG \_ \_ THREAD", \_ \_ \_ "EVENT TRACE FLAG IMAGE \_ LOAD", "EVENT \_ TRACE FLAG PROCESS \_ \_ \_ COUNTERS", "EVENT \_ TRACE FLAG \_ \_ CSWITCH", "EVENT \_ TRACE FLAG \_ DPC", "EVENT TRACE FLAG \_ \_ \_ \_ INTERRUPT", "EVENT TRACE FLAG \_ \_ \_ SYSTEMCALL", "EVENT \_ TRACE FLAG DISK \_ \_ \_ IO", "EVENT \_ TRACE FLAG DISK FILE \_ \_ \_ \_ IO", "EVENT \_ TRACE FLAG DISK IO \_ \_ \_ \_ INIT", "EVENT \_ TRACE FLAG \_ \_ DISPATCHER", "EVENT TRACE FLAG MEMORY PAGE \_ \_ \_ \_ \_ FAULTS", "EVENT TRACE FLAG MEMORY HARD \_ \_ \_ \_ \_ FAULTS", "EVENT TRACE \_ FLAG VIRTUAL \_ \_ \_ ALLOC", "EVENT \_ TRACE FLAG NETWORK \_ \_ \_ TCPIP", "EVENT \_ TRACE FLAG \_ \_ REGISTRY", "EVENT \_ TRACE FLAG \_ \_ ALPC", " EVENT TRACE FLAG \_ \_ SPLIT \_ \_ IO", "EVENT \_ TRACE FLAG \_ \_ DRIVER", "EVENT \_ TRACE FLAG \_ \_ PROFILE", "EVENT \_ TRACE FLAG FILE \_ \_ \_ IO", "EVENT \_ TRACE FLAG FILE IO \_ \_ \_ \_ INIT"}**, **ValueMap{"0x00000001", "0x00000002", "0x00000004", "0x00000008", "0x00000010", "0x00000020", "0x00000040", "0x00000080", "0x00000100", "0x00000200", "0x00000400", "0x00000800", "0x00001000", "0x00002000", "0x00004000", "0x00010000", "0x00020000", "0x00100000", "0x00200000", "0x00800000", "0x01000000", "0x02000000", "0x04000000"}**
</dt> </dl>

Aktivieren Sie das Flag, das die aktivierten Kernelanbieter angibt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



 

 




