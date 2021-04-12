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
ms.openlocfilehash: 5f305387a29d1d1569addafd127f53c98246e1a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216322"
---
# <a name="__securitydescriptor-class"></a>\_\_SecurityDescriptor-Klasse

Die abstrakte System Klasse **\_ \_ securityDescriptor** stellt eine [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **\_ \_ securityDescriptor** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ securityDescriptor** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ControlFlags**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitflags, die Informationen über den Inhalt und das Format des Deskriptors bereitstellen. Eine Beschreibung der Flags finden Sie in der Eigenschaft " **ControlFlags** " in der Win32-Klasse " [**\_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) ".

</dd> <dt>

**DACL**
</dt> <dd> <dl> <dt>

Datentyp: **[**\_ \_ ACE**](--ace.md)** -Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Ein Array von [**\_ \_ ACE**](--ace.md) -Einträgen, die den Zugriff auf das-Objekt angeben.

</dd> <dt>

**Gruppieren**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

ACE, der den Vertrauens nehmer identifiziert, der die Gruppe des Objekts darstellt.

</dd> <dt>

**Besitzer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

ACE, der den Vertrauens nehmer identifiziert, der den Besitzer des Objekts darstellt.

</dd> <dt>

**SACL**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ ACE**](--ace.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Array von [**\_ \_ ACE**](--ace.md) -Einträgen, das Benutzer und Gruppen identifiziert, für die Überwachungsinformationen gesammelt werden.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Uhrzeit im [CIM- \_ DateTime](cim-datetime.md) -Format, als die Sicherheits Beschreibung erstellt wurde.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse stellt Eigenschaften bereit, die von [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)geerbt werden. Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md). Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**Win32- \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

