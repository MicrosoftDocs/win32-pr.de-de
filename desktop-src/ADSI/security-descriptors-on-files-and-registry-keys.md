---
title: Sicherheits Deskriptoren für Dateien und Registrierungsschlüssel
description: Mit Active Directory Service Interfaces (ADSI) können Dateisysteme innerhalb einer Organisation verwaltet und gesichert werden, einschließlich der Möglichkeit, ACLs auf Dateien oder Dateifreigaben festzulegen oder zu ändern, die von Benutzern erstellt wurden.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Sicherheits Deskriptoren für Dateien und Registrierungsschlüssel ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11600a495b9a70513b9bd401777e9cdd61449ede
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474244"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Sicherheits Deskriptoren für Dateien und Registrierungsschlüssel

Mit Active Directory Service Interfaces (ADSI) können Dateisysteme innerhalb einer Organisation verwaltet und gesichert werden, einschließlich der Möglichkeit, ACLs auf Dateien oder Dateifreigaben festzulegen oder zu ändern, die von Benutzern erstellt wurden. Sicherheits Schnittstellen, wie z. b. [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , legen ACLs auf Active Directory-, Exchange-, Datei-, Dateifreigabe-oder Registrierungsschlüssel Objekten fest. Bevor Sie diese Schnittstellen verwenden, muss die Sicherheits Beschreibung möglicherweise geändert werden, wenn Sie ein anderes Format als die-Schnittstelle verwendet, oder wenn Sie nicht über Zugriffsrechte für die SACL der Sicherheits Beschreibung verfügen, da Sie kein Mitglied der Sicherheitsadministrator Gruppe sind.

Um die Sicherheits Beschreibung zu erhalten, festzulegen oder zu ändern, verwenden Sie die [**iadssecurityutility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) -Schnittstelle. Mit dieser Schnittstelle können Sie eine Sicherheits Beschreibung aus verschiedenen Ressourcen im ursprünglichen Format abrufen, wie z. b. das ADSI-Format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), einen unformatierten Sicherheits Deskriptor oder als hexadezimale Zeichenfolge, wie in Exchange 5,5 verwendet. Wenn Sie abgerufen werden, können Sie Sie in ein anderes Format konvertieren, z. b. von einem unformatierten Sicherheits Deskriptor in **IADsSecurityDescriptor**. Anschließend können Sie das neue Format wieder in die Ressource schreiben.

Einige der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Eigenschaftswerte (z. b. [**AccessMask**](iadsaccesscontrolentry-property-methods.md) und **AceFlags**) unterscheiden sich für unterschiedliche Objekttypen. Beispielsweise verwendet ein Active Directory Objekt den **\_ rechten \_ generischen \_ Lese** -Member der ADS- [**\_ Rechte \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Aufzählungs Enumeration für die **IADsAccessControlEntry. AccessMask** -Eigenschaft, aber das entsprechende Zugriffsrecht für ein Datei Objekt ist **Datei \_ generischer \_ Lese** Vorgang. Es ist nicht sicher anzunehmen, dass alle Eigenschaftswerte für Active Directory-Objekte und nicht-Active Directory-Objekte identisch sind. In der folgenden Liste sind die **IADsAccessControlEntry** -Eigenschaften aufgeführt, die sich für nicht-Active Directory Objekte unterscheiden, und wo die richtigen Werte abgerufen werden können.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen und eine Liste möglicher Werte für Datei-oder Dateifreigabe Objekte finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights).

Weitere Informationen und eine Liste möglicher Werte für Registrierungs Objekte finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights).

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter dem Element " **AceType** " der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter dem **AceFlags** -Member der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Fahren**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Enthält 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte aus "Winnt. h".

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ \_Objekttyp \_ vorhanden** (1)
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Geerbter \_ \_ Objekttyp \_ vorhanden** (2)
</dt> <dd>

[**Ereritedobjecttype**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter **ObjectType** -Member des [**Zugriffs \_ verweigerten \_ Objekt- \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), Zugriff auf [**\_ zulässige Objekt- \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)und ähnliche Strukturen. Diese Eigenschaft sollte für nicht Active Directory-Objekte nicht festgelegt oder geändert werden.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**Ereritedobjecttype**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter dem Element " **eritedobjecttype** " des [**Objekts "Zugriff \_ verweigert \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)", " [**Zugriff auf \_ zulässige \_ Objekte \_**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)" und ähnlichen Strukturen. Diese Eigenschaft sollte für nicht Active Directory-Objekte nicht festgelegt oder geändert werden.

</dd> </dl>

Normalerweise ruft [**iadssecurityutility. getsecuritydescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) alle Teile der Sicherheits Beschreibung ab, z. b. Besitzer, Gruppe, SACL oder DACL. Ebenso überschreibt [**iadssecurityutility. SETSECURITYDESCRIPTOR**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) alle Teile der Sicherheits Beschreibung standardmäßig. Sie können die [**iadssecurityutility. securityymask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) -Eigenschaft verwenden, um einzelne Teile der Sicherheits Beschreibung anzugeben, die abgerufen oder festgelegt werden sollen. Beispielsweise können Sie **securitymask** auf [**ADS \_ Security \_ Info \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) festlegen, bevor Sie **getsecuritydescriptor** aufrufen, um nur die DACL abzurufen, ohne die anderen Teile der Sicherheits Beschreibung abzurufen.

Weitere Informationen und ein Codebeispiel, in dem die [**iadssecurityutility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) -Schnittstelle zum Hinzufügen eines ACE zu einer Datei verwendet wird, finden Sie unter [Beispielcode zum Hinzufügen eines ACE zu einer Datei](example-code-for-adding-an-ace-to-a-file.md).

Der folgende Beispielcode stellt die Konstanten Bezeichner für Datei-, Dateifreigabe-und Registrierungs Objekte für die Eigenschaften [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** und **Flags** für die Verwendung mit Visual Basic und Microsoft Visual Basic Scripting Edition bereit.


```VB
' Identifiers for the IADsAccessControlEntry.AccessMask property for file,
' file share, and registry objects.
Const DELETE = &H10000
Const READ_CONTROL = &H20000
Const WRITE_DAC = &H40000
Const WRITE_OWNER = &H80000
Const SYNCHRONIZE = &H100000

Const STANDARD_RIGHTS_REQUIRED = &HF0000

Const STANDARD_RIGHTS_READ = &H20000
Const STANDARD_RIGHTS_WRITE = &H20000
Const STANDARD_RIGHTS_EXECUTE = &H20000

Const STANDARD_RIGHTS_ALL = &H1F0000

Const SPECIFIC_RIGHTS_ALL = &HFFFF

' Identifiers for the IADsAccessControlEntry.AccessMask property for file and
' file share objects.
Const FILE_READ_DATA = &H1                  '  file & pipe
Const FILE_LIST_DIRECTORY = &H1             '  directory

Const FILE_WRITE_DATA = &H2                 '  file & pipe
Const FILE_ADD_FILE = &H2                   '  directory

Const FILE_APPEND_DATA = &H4                '  file
Const FILE_ADD_SUBDIRECTORY = &H4           '  directory
Const FILE_CREATE_PIPE_INSTANCE = &H4       '  named pipe

Const FILE_READ_EA = &H8                    '  file & directory

Const FILE_WRITE_EA = &H10                  '  file & directory

Const FILE_EXECUTE = &H20                   '  file
Const FILE_TRAVERSE = &H20                  '  directory

Const FILE_DELETE_CHILD = &H40              '  directory

Const FILE_READ_ATTRIBUTES = &H80           '  all

Const FILE_WRITE_ATTRIBUTES = &H100         '  all

Const FILE_ALL_ACCESS = STANDARD_RIGHTS_REQUIRED Or SYNCHRONIZE Or &H1FF

Const FILE_GENERIC_READ = STANDARD_RIGHTS_READ Or FILE_READ_DATA Or FILE_READ_ATTRIBUTES Or _
                          FILE_READ_EA Or SYNCHRONIZE

Const FILE_GENERIC_WRITE = STANDARD_RIGHTS_WRITE Or FILE_WRITE_DATA Or FILE_WRITE_ATTRIBUTES Or _
                           FILE_WRITE_EA Or FILE_APPEND_DATA Or SYNCHRONIZE

Const FILE_GENERIC_EXECUTE = STANDARD_RIGHTS_EXECUTE Or FILE_READ_ATTRIBUTES Or FILE_EXECUTE Or SYNCHRONIZE


' Identifiers for the IADsAccessControlEntry.AccessMask property for registry
' objects.
Const KEY_QUERY_VALUE = &H1
Const KEY_SET_VALUE = &H2
Const KEY_CREATE_SUB_KEY = &H4
Const KEY_ENUMERATE_SUB_KEYS = &H8
Const KEY_NOTIFY = &H10
Const KEY_CREATE_LINK = &H20
Const KEY_WOW64_32KEY = &H200
Const KEY_WOW64_64KEY = &H100
Const KEY_WOW64_RES = &H300

Const KEY_READ = ((STANDARD_RIGHTS_READ Or KEY_QUERY_VALUE Or KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY) And _
                  (Not SYNCHRONIZE))

Const KEY_WRITE = ((STANDARD_RIGHTS_WRITE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY) And (Not SYNCHRONIZE))

Const KEY_EXECUTE = ((KEY_READ) And (Not SYNCHRONIZE))

Const KEY_ALL_ACCESS = ((STANDARD_RIGHTS_ALL Or KEY_QUERY_VALUE Or KEY_SET_VALUE Or KEY_CREATE_SUB_KEY Or _
                         KEY_ENUMERATE_SUB_KEYS Or KEY_NOTIFY Or KEY_CREATE_LINK) And (Not SYNCHRONIZE))
    

' Identifiers for the IADsAccessControlEntry.AceFlags property for file and
' file share objects.
Const OBJECT_INHERIT_ACE = &H1
Const CONTAINER_INHERIT_ACE = &H2
Const NO_PROPAGATE_INHERIT_ACE = &H4
Const INHERIT_ONLY_ACE = &H8
Const INHERITED_ACE = &H10
    

' Identifiers for the IADsAccessControlEntry.Flags property.
Const ACE_OBJECT_TYPE_PRESENT = 1
Const ACE_INHERITED_OBJECT_TYPE_PRESENT = 2
```



 

 