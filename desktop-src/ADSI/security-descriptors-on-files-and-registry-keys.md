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
# <a name="security-descriptors-on-files-and-registry-keys"></a><span data-ttu-id="0f18d-104">Sicherheits Deskriptoren für Dateien und Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="0f18d-104">Security Descriptors on Files and Registry Keys</span></span>

<span data-ttu-id="0f18d-105">Mit Active Directory Service Interfaces (ADSI) können Dateisysteme innerhalb einer Organisation verwaltet und gesichert werden, einschließlich der Möglichkeit, ACLs auf Dateien oder Dateifreigaben festzulegen oder zu ändern, die von Benutzern erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0f18d-105">Active Directory Service Interfaces (ADSI) can be used to manage and secure file systems within an organization, including the ability to set or modify ACLs on files or file shares created by users.</span></span> <span data-ttu-id="0f18d-106">Sicherheits Schnittstellen, wie z. b. [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)und [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) , legen ACLs auf Active Directory-, Exchange-, Datei-, Dateifreigabe-oder Registrierungsschlüssel Objekten fest.</span><span class="sxs-lookup"><span data-stu-id="0f18d-106">Security interfaces, such as [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist), and [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) set ACLs on Active Directory, Exchange, file, file share, or registry key objects.</span></span> <span data-ttu-id="0f18d-107">Bevor Sie diese Schnittstellen verwenden, muss die Sicherheits Beschreibung möglicherweise geändert werden, wenn Sie ein anderes Format als die-Schnittstelle verwendet, oder wenn Sie nicht über Zugriffsrechte für die SACL der Sicherheits Beschreibung verfügen, da Sie kein Mitglied der Sicherheitsadministrator Gruppe sind.</span><span class="sxs-lookup"><span data-stu-id="0f18d-107">Before using these interfaces, the security descriptor may need to be modified if it uses a different format from the interface, or if you do not have access rights to the SACL of the security descriptor because you are not a member of the security administrator group.</span></span>

<span data-ttu-id="0f18d-108">Um die Sicherheits Beschreibung zu erhalten, festzulegen oder zu ändern, verwenden Sie die [**iadssecurityutility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0f18d-108">To get, set, or modify the security descriptor, use the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface.</span></span> <span data-ttu-id="0f18d-109">Mit dieser Schnittstelle können Sie eine Sicherheits Beschreibung aus verschiedenen Ressourcen im ursprünglichen Format abrufen, wie z. b. das ADSI-Format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), einen unformatierten Sicherheits Deskriptor oder als hexadezimale Zeichenfolge, wie in Exchange 5,5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="0f18d-109">This interface enables you to retrieve a security descriptor from various resources in its original format, such as the ADSI format [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor), a raw security descriptor, or as a hexadecimal string as used in Exchange 5.5.</span></span> <span data-ttu-id="0f18d-110">Wenn Sie abgerufen werden, können Sie Sie in ein anderes Format konvertieren, z. b. von einem unformatierten Sicherheits Deskriptor in **IADsSecurityDescriptor**.</span><span class="sxs-lookup"><span data-stu-id="0f18d-110">When retrieved, you can convert it to another format, for example, from a raw security descriptor to **IADsSecurityDescriptor**.</span></span> <span data-ttu-id="0f18d-111">Anschließend können Sie das neue Format wieder in die Ressource schreiben.</span><span class="sxs-lookup"><span data-stu-id="0f18d-111">You can then write the new format back to the resource.</span></span>

<span data-ttu-id="0f18d-112">Einige der [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) -Eigenschaftswerte (z. b. [**AccessMask**](iadsaccesscontrolentry-property-methods.md) und **AceFlags**) unterscheiden sich für unterschiedliche Objekttypen.</span><span class="sxs-lookup"><span data-stu-id="0f18d-112">Some of the [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) property values, such as [**AccessMask**](iadsaccesscontrolentry-property-methods.md) and **AceFlags**, will be different for different object types.</span></span> <span data-ttu-id="0f18d-113">Beispielsweise verwendet ein Active Directory Objekt den **\_ rechten \_ generischen \_ Lese** -Member der ADS- [**\_ Rechte \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum) Aufzählungs Enumeration für die **IADsAccessControlEntry. AccessMask** -Eigenschaft, aber das entsprechende Zugriffsrecht für ein Datei Objekt ist **Datei \_ generischer \_ Lese** Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0f18d-113">For example, an Active Directory object will use the **ADS\_RIGHT\_GENERIC\_READ** member of the [**ADS\_RIGHTS\_ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum) enumeration for the **IADsAccessControlEntry.AccessMask** property, but the equivalent access right for a file object is **FILE\_GENERIC\_READ**.</span></span> <span data-ttu-id="0f18d-114">Es ist nicht sicher anzunehmen, dass alle Eigenschaftswerte für Active Directory-Objekte und nicht-Active Directory-Objekte identisch sind.</span><span class="sxs-lookup"><span data-stu-id="0f18d-114">It is not safe to assume that all property values will be the same for Active Directory objects and non-Active Directory objects.</span></span> <span data-ttu-id="0f18d-115">In der folgenden Liste sind die **IADsAccessControlEntry** -Eigenschaften aufgeführt, die sich für nicht-Active Directory Objekte unterscheiden, und wo die richtigen Werte abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="0f18d-115">The following list shows the **IADsAccessControlEntry** properties that differ for non-Active Directory objects and where the proper values can be obtained.</span></span>

<dl> <dt>

<span data-ttu-id="0f18d-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-116"><span id="AccessMask"></span><span id="accessmask"></span><span id="ACCESSMASK"></span>[**AccessMask**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-117">Weitere Informationen und eine Liste möglicher Werte für Datei-oder Dateifreigabe Objekte finden Sie unter [Datei Sicherheit und Zugriffsrechte](/windows/desktop/FileIO/file-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="0f18d-117">For more information and a list of possible values for file or file share objects, see [File Security and Access Rights](/windows/desktop/FileIO/file-security-and-access-rights).</span></span>

<span data-ttu-id="0f18d-118">Weitere Informationen und eine Liste möglicher Werte für Registrierungs Objekte finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span><span class="sxs-lookup"><span data-stu-id="0f18d-118">For more information and a list of possible values for registry objects, see [Registry Key Security and Access Rights](/windows/desktop/SysInfo/registry-key-security-and-access-rights).</span></span>

</dd> <dt>

<span data-ttu-id="0f18d-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-119"><span id="AceType"></span><span id="acetype"></span><span id="ACETYPE"></span>[**AceType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-120">Weitere Informationen finden Sie unter dem Element " **AceType** " der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="0f18d-120">For more information, see the **AceType** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f18d-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-121"><span id="AceFlags"></span><span id="aceflags"></span><span id="ACEFLAGS"></span>[**AceFlags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-122">Weitere Informationen finden Sie unter dem **AceFlags** -Member der [**ACE- \_ Header**](/windows/desktop/api/winnt/ns-winnt-ace_header) Struktur.</span><span class="sxs-lookup"><span data-stu-id="0f18d-122">For more information, see the **AceFlags** member of the [**ACE\_HEADER**](/windows/desktop/api/winnt/ns-winnt-ace_header) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f18d-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Fahren**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-123"><span id="Flags"></span><span id="flags"></span><span id="FLAGS"></span>[**Flags**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-124">Enthält 0 (null) oder eine Kombination aus einem oder mehreren der folgenden Werte aus "Winnt. h".</span><span class="sxs-lookup"><span data-stu-id="0f18d-124">Contains zero or a combination of one or more of the following values from WinNT.h.</span></span>

<dl> <dt>

<span data-ttu-id="0f18d-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE \_ \_Objekttyp \_ vorhanden** (1)</span><span class="sxs-lookup"><span data-stu-id="0f18d-125"><span id="ACE_OBJECT_TYPE_PRESENT__1_"></span><span id="ace_object_type_present__1_"></span>**ACE\_OBJECT\_TYPE\_PRESENT** (1)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="0f18d-126">[**ObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> <dt>

<span data-ttu-id="0f18d-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE \_ Geerbter \_ \_ Objekttyp \_ vorhanden** (2)</span><span class="sxs-lookup"><span data-stu-id="0f18d-127"><span id="ACE_INHERITED_OBJECT_TYPE_PRESENT__2_"></span><span id="ace_inherited_object_type_present__2_"></span>**ACE\_INHERITED\_OBJECT\_TYPE\_PRESENT** (2)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-128">[**Ereritedobjecttype**](iadsaccesscontrolentry-property-methods.md) enthält einen gültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="0f18d-128">[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md) contains a valid value.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="0f18d-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-129"><span id="ObjectType"></span><span id="objecttype"></span><span id="OBJECTTYPE"></span>[**ObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-130">Weitere Informationen finden Sie unter **ObjectType** -Member des [**Zugriffs \_ verweigerten \_ Objekt- \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), Zugriff auf [**\_ zulässige Objekt- \_ \_ ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)und ähnliche Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0f18d-130">For more information, see the **ObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="0f18d-131">Diese Eigenschaft sollte für nicht Active Directory-Objekte nicht festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0f18d-131">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> <dt>

<span data-ttu-id="0f18d-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**Ereritedobjecttype**](iadsaccesscontrolentry-property-methods.md)</span><span class="sxs-lookup"><span data-stu-id="0f18d-132"><span id="InheritedObjectType"></span><span id="inheritedobjecttype"></span><span id="INHERITEDOBJECTTYPE"></span>[**InheritedObjectType**](iadsaccesscontrolentry-property-methods.md)</span></span>
</dt> <dd>

<span data-ttu-id="0f18d-133">Weitere Informationen finden Sie unter dem Element " **eritedobjecttype** " des [**Objekts "Zugriff \_ verweigert \_ \_**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace)", " [**Zugriff auf \_ zulässige \_ Objekte \_**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace)" und ähnlichen Strukturen.</span><span class="sxs-lookup"><span data-stu-id="0f18d-133">For more information, see the **InheritedObjectType** member of the [**ACCESS\_DENIED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_denied_object_ace), [**ACCESS\_ALLOWED\_OBJECT\_ACE**](/windows/desktop/api/winnt/ns-winnt-access_allowed_object_ace), and similar structures.</span></span> <span data-ttu-id="0f18d-134">Diese Eigenschaft sollte für nicht Active Directory-Objekte nicht festgelegt oder geändert werden.</span><span class="sxs-lookup"><span data-stu-id="0f18d-134">This property should not be set or modified for non-Active Directory objects.</span></span>

</dd> </dl>

<span data-ttu-id="0f18d-135">Normalerweise ruft [**iadssecurityutility. getsecuritydescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) alle Teile der Sicherheits Beschreibung ab, z. b. Besitzer, Gruppe, SACL oder DACL.</span><span class="sxs-lookup"><span data-stu-id="0f18d-135">Normally, [**IADsSecurityUtility.GetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-getsecuritydescriptor) will retrieve all parts of the security descriptor, such as owner, group, SACL, or DACL.</span></span> <span data-ttu-id="0f18d-136">Ebenso überschreibt [**iadssecurityutility. SETSECURITYDESCRIPTOR**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) alle Teile der Sicherheits Beschreibung standardmäßig.</span><span class="sxs-lookup"><span data-stu-id="0f18d-136">Similarly, [**IADsSecurityUtility.SetSecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-setsecuritydescriptor) will overwrite all parts of the security descriptor by default.</span></span> <span data-ttu-id="0f18d-137">Sie können die [**iadssecurityutility. securityymask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) -Eigenschaft verwenden, um einzelne Teile der Sicherheits Beschreibung anzugeben, die abgerufen oder festgelegt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0f18d-137">You can use the [**IADsSecurityUtility.SecurityMask**](/windows/desktop/api/Iads/nf-iads-iadssecurityutility-get_securitymask) property to specify individual parts of the security descriptor to retrieve or set.</span></span> <span data-ttu-id="0f18d-138">Beispielsweise können Sie **securitymask** auf [**ADS \_ Security \_ Info \_ DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) festlegen, bevor Sie **getsecuritydescriptor** aufrufen, um nur die DACL abzurufen, ohne die anderen Teile der Sicherheits Beschreibung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="0f18d-138">For example, you can set **SecurityMask** to [**ADS\_SECURITY\_INFO\_DACL**](/windows/win32/api/iads/ne-iads-ads_security_info_enum) before calling **GetSecurityDescriptor** to only retrieve the DACL without retrieving the other parts of the security descriptor.</span></span>

<span data-ttu-id="0f18d-139">Weitere Informationen und ein Codebeispiel, in dem die [**iadssecurityutility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) -Schnittstelle zum Hinzufügen eines ACE zu einer Datei verwendet wird, finden Sie unter [Beispielcode zum Hinzufügen eines ACE zu einer Datei](example-code-for-adding-an-ace-to-a-file.md).</span><span class="sxs-lookup"><span data-stu-id="0f18d-139">For more information and a code example that uses the [**IADsSecurityUtility**](/windows/desktop/api/Iads/nn-iads-iadssecurityutility) interface to add an ACE to a file, see [Example Code for Adding an ACE to a File](example-code-for-adding-an-ace-to-a-file.md).</span></span>

<span data-ttu-id="0f18d-140">Der folgende Beispielcode stellt die Konstanten Bezeichner für Datei-, Dateifreigabe-und Registrierungs Objekte für die Eigenschaften [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags** und **Flags** für die Verwendung mit Visual Basic und Microsoft Visual Basic Scripting Edition bereit.</span><span class="sxs-lookup"><span data-stu-id="0f18d-140">The following example code provides the constant identifiers for file, file share and registry objects for the [**AccessMask**](iadsaccesscontrolentry-property-methods.md), **AceType**, **AceFlags**, and **Flags** properties for use with Visual Basic and Microsoft Visual Basic Scripting Edition.</span></span>


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



 

 