---
title: Sicherheitsbeschreibungen für Dateien und Registrierungsschlüssel
description: Active Directory-Dienstschnittstellen (ADSI) können verwendet werden, um Dateisysteme innerhalb einer Organisation zu verwalten und zu schützen, einschließlich der Möglichkeit, ACLs für Dateien oder Dateifreigaben festzulegen oder zu ändern, die von Benutzern erstellt wurden.
ms.assetid: 7233a82f-fc38-4718-b674-4e6a00666184
ms.tgt_platform: multiple
keywords:
- Sicherheitsbeschreibungen für Dateien und Registrierungsschlüssel ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae567e9550989153f0b85207be49a729bc0499c320f410c92fc993269d997da7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119333220"
---
# <a name="security-descriptors-on-files-and-registry-keys"></a>Sicherheitsbeschreibungen für Dateien und Registrierungsschlüssel

Active Directory-Dienstschnittstellen (ADSI) können verwendet werden, um Dateisysteme innerhalb einer Organisation zu verwalten und zu schützen, einschließlich der Möglichkeit, ACLs für Dateien oder Dateifreigaben festzulegen oder zu ändern, die von Benutzern erstellt wurden. Sicherheitsschnittstellen wie [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor) [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) legen ACLs für Active Directory-, Exchange-, Datei-, Dateifreigabe- oder Registrierungsschlüsselobjekte fest. Vor der Verwendung dieser Schnittstellen muss der Sicherheitsdeskriptor möglicherweise geändert werden, wenn er ein anderes Format als die Schnittstelle verwendet, oder wenn Sie nicht über Zugriffsrechte für die SACL des Sicherheitsdeskriptors verfügen, da Sie kein Mitglied der Sicherheitsadministratorgruppe sind.

Verwenden Sie die [**IADsSecurityUtility-Schnittstelle,**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) um den Sicherheitsdeskriptor abzurufen, festzulegen oder zu ändern. Mit dieser Schnittstelle können Sie einen Sicherheitsdeskriptor aus verschiedenen Ressourcen im ursprünglichen Format abrufen, z. B. das ADSI-Format [**IADsSecurityDescriptor,**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)einen unformatierten Sicherheitsdeskriptor oder eine hexadezimale Zeichenfolge, wie in Exchange 5.5 verwendet. Beim Abrufen können Sie es in ein anderes Format konvertieren, z. B. aus einem unformatierten Sicherheitsdeskriptor in **IADsSecurityDescriptor.** Anschließend können Sie das neue Format zurück in die Ressource schreiben.

Einige der [**IADsAccessControlEntry-Eigenschaftswerte,**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) z. B. [**AccessMask**](iadsaccesscontrolentry-property-methods.md) und **AceFlags,** unterscheiden sich für verschiedene Objekttypen. Beispielsweise verwendet ein Active Directory-Objekt den **\_ GENERISCHEN ADS RIGHT \_ \_ READ-Member** der [**ADS RIGHTS \_ \_ ENUM-Enumeration**](/windows/win32/api/iads/ne-iads-ads_rights_enum) für die **IADsAccessControlEntry.AccessMask-Eigenschaft,** aber das entsprechende Zugriffsrecht für ein Dateiobjekt ist **FILE GENERIC \_ \_ READ**. Es ist nicht sicher, davon auszugehen, dass alle Eigenschaftswerte für Active Directory-Objekte und Nicht-Active Directory-Objekte identisch sind. Die folgende Liste zeigt die **IADsAccessControlEntry-Eigenschaften,** die sich für Nicht-Active Directory-Objekte unterscheiden und wo die richtigen Werte abgerufen werden können.

<dl> <dt>

<span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**Accessmask**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen und eine Liste möglicher Werte für Datei- oder Dateifreigabeobjekte finden Sie unter [Dateisicherheit und Zugriffsrechte.](/windows/desktop/FileIO/file-security-and-access-rights)

Weitere Informationen und eine Liste der möglichen Werte für Registrierungsobjekte finden Sie unter Sicherheit und Zugriffsrechte für [Registrierungsschlüssel.](/windows/desktop/SysInfo/registry-key-security-and-access-rights)

</dd> <dt>

<span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter **AceType-Member** der [**ACE \_ HEADER-Struktur.**](/windows/desktop/api/winnt/ns-winnt-ace_header)

</dd> <dt>

<span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter **AceFlags-Member** der [**ACE \_ HEADER-Struktur.**](/windows/desktop/api/winnt/ns-winnt-ace_header)

</dd> <dt>

<span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flaggen**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Enthält 0 (null) oder eine Kombination aus mindestens einem der folgenden Werte aus WinNT.h.

<dl> <dt>

<span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ OBJEKTTYP \_ \_ VORHANDEN** (1)
</dt> <dd>

[**ObjectType**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.

</dd> <dt>

<span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ GEERBTER \_ \_ OBJEKTTYP \_ VORHANDEN** (2)
</dt> <dd>

[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.

</dd> </dl> </dd> <dt>

<span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**Objecttype**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter dem **ObjectType-Member** von [**ACCESS \_ DENIED \_ OBJECT \_ ACE,**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace) [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)und ähnlichen Strukturen. Diese Eigenschaft sollte nicht für Nicht-Active Directory-Objekte festgelegt oder geändert werden.

</dd> <dt>

<span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**Inheritedobjecttype**](iadsaccesscontrolentry-property-methods.md)
</dt> <dd>

Weitere Informationen finden Sie unter dem **InheritedObjectType-Member** von [**ACCESS \_ DENIED \_ OBJECT \_ ACE,**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace) [**ACCESS ALLOWED OBJECT \_ \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)und ähnlichen Strukturen. Diese Eigenschaft sollte nicht für Nicht-Active Directory-Objekte festgelegt oder geändert werden.

</dd> </dl>

Normalerweise ruft [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) alle Teile der Sicherheitsbeschreibung ab, z. B. Besitzer, Gruppe, SACL oder DACL. Auf ähnliche Weise überschreibt [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) standardmäßig alle Teile des Sicherheitsdeskriptors. Sie können die [**IADsSecurityUtility.SecurityMask-Eigenschaft**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) verwenden, um einzelne Teile der Sicherheitsbeschreibung anzugeben, die abgerufen oder festgelegt werden sollen. Beispielsweise können Sie **SecurityMask** auf [**ADS SECURITY INFO \_ \_ \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) festlegen, bevor **Sie GetSecurityDescriptor** aufrufen, um nur die DACL abzurufen, ohne die anderen Teile der Sicherheitsbeschreibung abzurufen.

Weitere Informationen und ein Codebeispiel, in dem die [**IADsSecurityUtility-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) zum Hinzufügen eines ACE zu einer Datei verwendet wird, finden Sie unter [Beispielcode zum Hinzufügen eines ACE zu einer Datei.](example-code-for-adding-an-ace-to-a-file.md)

Der folgende Beispielcode stellt die konstanten Bezeichner für Datei-, Dateifreigabe- und Registrierungsobjekte für die Eigenschaften [**AccessMask,**](iadsaccesscontrolentry-property-methods.md) **AceType,** **AceFlags** und **Flags** für die Verwendung mit Visual Basic und Microsoft Visual Basic Scripting Edition bereit.


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



 

 