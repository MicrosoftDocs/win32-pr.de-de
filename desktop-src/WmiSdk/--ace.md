---
description: Stellt einen Zugriffssteuerungseintrag (ACE) dar.
ms.assetid: 47daffd0-b9db-4367-b0b8-654a2da30fed
ms.tgt_platform: multiple
title: __ACE-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __ACE
- All
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
ms.openlocfilehash: ea2a765225145ce3d44e0aff89aeaca0a7563e0a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485755"
---
# <a name="__ace-class"></a>\_\_ACE-Klasse

Die **\_ \_ ACE** Abstract-System Klasse stellt einen Zugriffs Steuerungs Eintrag ([*ACE*](/windows/desktop/SecGloss/a-gly)) dar.

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class  __ACE : __SecurityRelatedClass
{
            AceFlags;
            AccessMask;
            AceType;
            GuidInheritedObjectType;
            GuidObjectType;
  uint64    TIME_CREATED;
  __Trustee Trustee;
};
```

## <a name="members"></a>Member

Die **\_ \_ ACE** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ \_ ACE** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessMask**
</dt> <dd> <dl> <dt>

Datentyp: 
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bitflags, die Rechte darstellen, die dem Vertrauens nehmer gewährt oder verweigert werden. Weitere Informationen und eine Beschreibung der Flags finden Sie unter **AccessMask** -Eigenschaft in der [**Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse "Ace".

</dd> <dt>

**AceFlags**
</dt> <dd> <dl> <dt>

Datentyp: 
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Bitflags, die die Vererbung des ACE angeben. Weitere Informationen und eine Beschreibung der Flags finden Sie unter **AceFlags** -Eigenschaft in der [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse.

</dd> <dt>

**AceType**
</dt> <dd> <dl> <dt>

Datentyp: 
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Typ des ACE-Eintrags, den diese Instanz darstellt.

</dd> <dt>

**Guidinheritedobjecttype**
</dt> <dd> <dl> <dt>

Datentyp: 
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die GUID des übergeordneten Elements des Objekts, auf das die Zugriffsrechte in der **AccessMask** -Eigenschaft angewendet werden.

</dd> <dt>

**Guidobjecttype**
</dt> <dd> <dl> <dt>

Datentyp: 
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Die GUID, die den Typ des Objekts angibt, auf das die Rechte in der **AccessMask** -Eigenschaft angewendet werden.

</dd> <dt>

**\_Erstellungszeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Zeit im CIM- [ \_ DateTime](cim-datetime.md) -Format, zu der die Sicherheits Beschreibung erstellt wurde.

</dd> <dt>

**Stiftungs**
</dt> <dd> <dl> <dt>

Datentyp: **[ **\_ \_ Treuhänder**](--trustee.md)**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> </dl>

Der Treuhänder des ACE-Eintrags, der durch diese Instanz der **\_ \_ ACE** -Klasse dargestellt wird.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse stellt die Eigenschaften bereit, die von der [**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) -Klasse geerbt werden, die ein Member der [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) -Klasse ist. Weitere Informationen finden Sie unter [WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md) und [Ändern der Zugriffssicherheit für Sicherungs fähige Objekte](changing-access-security-on-securable-objects.md). Weitere Informationen zu ACEs finden Sie unter [Access Control-Komponenten](/windows/desktop/SecAuthZ/access-control-components).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>       |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/> |
| Namespace<br/>                | Alle WMI-Namespaces<br/>  |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_\_Securityrelatedclass**](--securityrelatedclass.md)
</dt> <dt>

[WMI-System Klassen](wmi-system-classes.md)
</dt> <dt>

[**Win32- \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[Verwalten der WMI-Sicherheit](maintaining-wmi-security.md)
</dt> </dl>

 

