---
description: Stellt eine Sicherheitsbeschreibung dar.
ms.assetid: 1ade1751-52a2-4ada-8255-323321111663
ms.tgt_platform: multiple
title: __SecurityDescriptor-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SecurityDescriptor
- All
- All
- All
- All
- All
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: c248a437651396811f71c04e72dd8b209c5d10823f49d03abbe7e9d9ee6b6867
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118110197"
---
# <a name="__securitydescriptor-class"></a>\_\_SecurityDescriptor-Klasse

Die abstrakte **\_ \_ SecurityDescriptor-Systemklasse** stellt einen [*Sicherheitsdeskriptor*](/windows/desktop/SecGloss/s-gly)dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
class __SecurityDescriptor
{
  uint32 ControlFlags;
  __ACE  DACL[];
  __ACE  Group;
  __ACE  Owner;
  __ACE  SACL;
  uint64 TIME_CREATED;
};
```

## <a name="members"></a>Member

Die **\_ \_ SecurityDescriptor-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ SecurityDescriptor-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Controlflags**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitflags, die Informationen zum Inhalt und Format des Deskriptors bereitstellen. Eine Beschreibung der Flags finden Sie in der **ControlFlags-Eigenschaft** in der [**Win32 \_ SecurityDescriptor-Klasse.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

</dd> <dt>

**Dacl**
</dt> <dd> <dl> <dt>

Datentyp: **[**\_ \_ ACE-Array**](--ace.md)**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array von [**\_ \_ ACE-Einträgen,**](--ace.md) die den Zugriff auf das Objekt angeben.

</dd> <dt>

**Gruppe**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

ACE, der den Vertrauensnehmer identifiziert, der die Gruppe des Objekts darstellt.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

ACE, der den Vertrauensnehmer identifiziert, der den Besitzer des Objekts darstellt.

</dd> <dt>

**Sacl**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von [**\_ \_ ACE-Einträgen,**](--ace.md) das Benutzer und Gruppen identifiziert, für die Überwachungsinformationen gesammelt werden.

</dd> <dt>

**TIME \_ CREATED**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Uhrzeit im [CIM \_ DATETIME-Format,](cim-datetime.md) zu der der Sicherheitsdeskriptor erstellt wurde.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Diese Klasse stellt Eigenschaften bereit, die von [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)geerbt werden. Weitere Informationen finden Sie unter [WMI-Sicherheitsbeschreibungsobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für sicherungsfähige Objekte.](changing-access-security-on-securable-objects.md) Weitere Informationen zu ACEs finden Sie unter [Access Control Components](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[WMI-Systemklassen](wmi-system-classes.md)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

