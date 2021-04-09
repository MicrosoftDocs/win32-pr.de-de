---
description: Fungiert als übergeordnete Klasse für Anbieter definierte Fehlerklassen.
ms.assetid: fc2747f5-cfbc-4d61-894d-4585a03dda3f
ms.tgt_platform: multiple
title: __NotifyStatus-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __NotifyStatus
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: f19ef1f6088b5a058f4483f197877358177c81f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759439"
---
# <a name="__notifystatus-class"></a>\_\_Notifystatus-Klasse

Die abstrakte System Klasse **\_ \_ notifystatus** fungiert als übergeordnete Klasse für Anbieter definierte Fehlerklassen.

Die folgende Syntax wird von Managed Object Format Code (MF) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[abstract]
class __NotifyStatus
{
  uint32 StatusCode;
};
```

## <a name="members"></a>Member

Die **\_ \_ notifystatus** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ notifystatus** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Statuscode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Enthält einen Fehler-oder Informations Code für einen Vorgang. Dies kann ein beliebiger benutzerdefinierter Code sein, aber der Wert 0 (null) ist normalerweise reserviert, um den Erfolg anzugeben.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Obwohl die **\_ \_ notifystatus** -Klasse die übergeordnete Klasse für Anbieter definierte Fehlerklassen sein kann, wird empfohlen, dass Anbieter stattdessen Fehlerklassen von [**\_ \_ ExtendedStatus**](--extendedstatus.md) ableiten. Die Verwendung von **\_ \_ ExtendedStatus** ermöglicht eine stärkere Standardisierung von Fehlerklassen.

Anbieter sollten niemals Instanzen von **\_ \_ notifystatus** direkt erstellen, da diese Instanzen nicht mehr Informationen als einen einfachen Rückgabecode vermitteln.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> </dl>

 

 




