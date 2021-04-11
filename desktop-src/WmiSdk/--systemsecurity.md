---
description: Enthält Methoden, mit denen Sie auf die Sicherheitseinstellungen für einen Namespace zugreifen und diese ändern können.
ms.assetid: a54fdd85-feb8-4727-9f26-fe4f213cab6b
ms.tgt_platform: multiple
title: __SystemSecurity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 58de990b56518550705cda2f8360cd90a0381c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104132084"
---
# <a name="__systemsecurity-class"></a>\_\_SystemSecurity-Klasse

Die System **\_ \_ Security** -System Klasse enthält Methoden, mit denen Sie auf die Sicherheitseinstellungen für einen Namespace zugreifen und diese ändern können. Die **\_ \_ SystemSecurity** -Klasse ist eine Singleton-Klasse in jedem Namespace.

> [!Note]  
> Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
class __SystemSecurity
{
};
```

## <a name="members"></a>Member

Die **\_ \_ System Security** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **\_ \_ System Security** -Klasse verfügt über diese Methoden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Methode</th>
<th style="text-align: left;">BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-get9xuserlist.md"><strong>Get9XUserList</strong></a></td>
<td style="text-align: left;">Ruft eine Liste von Benutzern ab, denen der Remote Zugriff gestattet ist.<br/>
<blockquote>
[!Note]<br />
Diese Methode funktioniert nicht in unterstützten Versionen von Windows. Verwenden Sie stattdessen <a href="--systemsecurity-getsd.md"><strong>ge-d</strong></a> .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-getcalleraccessrights.md"><strong>Getcalleraccessrights</strong></a></td>
<td style="text-align: left;">Gibt eine Maske zurück, die jedem Bit entspricht, das einem Zugriffsrecht entspricht.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-getsd.md"><strong>GetSD</strong></a></td>
<td style="text-align: left;">Ruft den <a href="/windows/desktop/api/winnt/ns-winnt-security_descriptor"><strong>SECURITY_DESCRIPTOR</strong></a> für den Namespace ab, mit dem der Benutzer verbunden ist.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="getsecuritydescriptor-method-in-class---systemsecurity-.md"><strong>GetSecurityDescriptor</strong></a></td>
<td style="text-align: left;">Ruft die Sicherheits Beschreibung ab, die den Zugriff auf den WMI-Namespace steuert, der der- <strong>__SystemSecurity</strong>Instanz zugeordnet ist. Die Sicherheits Beschreibung wird als Instanz von<a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>zurückgegeben.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="--systemsecurity-set9xuserlist.md"><strong>Set9XUserList</strong></a></td>
<td style="text-align: left;">Legt eine Liste von Benutzern fest, denen der Remote Zugriff gestattet ist.<br/>
<blockquote>
[!Note]<br />
Diese Methode funktioniert nicht in unterstützten Versionen von Windows. Verwenden <a href="--systemsecurity-setsd.md"><strong>Sie</strong></a> stattdessen "".
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="--systemsecurity-setsd.md"><strong>SetSD</strong></a></td>
<td style="text-align: left;">Legt die Sicherheits Beschreibung für den Namespace fest, mit dem der Benutzer verbunden ist.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="setsecuritydescriptor-method-in-class---systemsecurity.md"><strong>SETSECURITYDESCRIPTOR</strong></a></td>
<td style="text-align: left;">Schreibt eine aktualisierte Version der Sicherheits Beschreibung, die den Zugriff auf den Drucker steuert. Die Sicherheits Beschreibung wird durch eine Instanz von <a href="--securitydescriptor.md"><strong>__SecurityDescriptor</strong></a>dargestellt.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Bemerkungen

Sie können festlegen, dass Client Skripts und-Anwendungen eine verschlüsselte Verbindung für die Authentifizierung verwenden, indem Sie der MOF-Datei, die den Namespace erstellt, den Wert "Requirements **sencryption** " hinzufügen. Sie können auch einen vorhandenen Namespace ändern, indem Sie dieses Attribut hinzufügen und die MOF-Datei erneut kompilieren. Weitere Informationen **zur Verwendung von**"Requirements" finden Sie unter [erfordern einer verschlüsselten Verbindung mit einem Namespace](requiring-an-encrypted-connection-to-a-namespace.md).

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

[WMI-Sicherheits Konstanten](wmi-security-constants.md)
</dt> <dt>

[WMI-sicherheitsdeskriptorobjekte](wmi-security-descriptor-objects.md)
</dt> <dt>

[Sichern von WMI-Namespaces](securing-wmi-namespaces.md)
</dt> <dt>

[Einrichten der Vererbung der Namespace Sicherheit](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[Access Control Listen (ACLs)](/windows/desktop/SecAuthZ/access-control-lists)
</dt> <dt>

[**Sicherheits \_ Beschreibung**](/windows/desktop/api/winnt/ns-winnt-security_descriptor)
</dt> </dl>

