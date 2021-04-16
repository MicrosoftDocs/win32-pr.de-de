---
title: Festlegen der Sicherheit bei der Namespace Erstellung
description: Die Managed Object Format (MOF)-Datei, die einen Namespace erstellt, kann auch die Sicherheits Deskriptoren für den Namespace definieren, indem der namespacesecuritysddl-Qualifizierer mit der Sicherheits Beschreibung im SDDL-Format (Security Deskriptor Definition Language) eingeschlossen wird.
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530137"
---
# <a name="setting-security-on-namespace-creation"></a><span data-ttu-id="40fb3-103">Festlegen der Sicherheit bei der Namespace Erstellung</span><span class="sxs-lookup"><span data-stu-id="40fb3-103">Setting security on namespace creation</span></span>

<span data-ttu-id="40fb3-104">Die Managed Object Format (MOF)-Datei, die einen Namespace erstellt, kann auch die [*Sicherheits Deskriptoren*](/windows/desktop/SecGloss/s-gly) für den Namespace definieren, indem der **namespacesecuritysddl** -Qualifizierer mit der Sicherheits Beschreibung im [SDDL-Format (Security Deskriptor Definition Language)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="40fb3-104">The Managed Object Format (MOF) file that creates a namespace can also define the [*security descriptors*](/windows/desktop/SecGloss/s-gly) for the namespace by including the **NamespaceSecuritySDDL** qualifier with the security descriptor in [security descriptor definition language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) format.</span></span>

<span data-ttu-id="40fb3-105">Sie können **namespacesecuritysddl** zum Sichern beliebiger Namespaces verwenden.</span><span class="sxs-lookup"><span data-stu-id="40fb3-105">You can use **NamespaceSecuritySDDL** to secure any namespace.</span></span> <span data-ttu-id="40fb3-106">Sie können diesen Qualifizierer auch in einer einfachen MOF-Datei verwenden, um die Sicherheits Beschreibung für einen vorhandenen Namespace zu ändern.</span><span class="sxs-lookup"><span data-stu-id="40fb3-106">You can also use this qualifier in a simple MOF file to alter the security descriptor on an existing namespace.</span></span> <span data-ttu-id="40fb3-107">Die SDDL-Zeichenfolge wird von WMI verarbeitet, um die Namespace Sicherheit festzulegen, wird jedoch nicht als Zeichenfolge gespeichert.</span><span class="sxs-lookup"><span data-stu-id="40fb3-107">The SDDL string is processed by WMI to establish the namespace security but is not stored as a string.</span></span> <span data-ttu-id="40fb3-108">Wenn kein Sicherheits Deskriptor angegeben wird, wird die Standard Sicherheit verwendet.</span><span class="sxs-lookup"><span data-stu-id="40fb3-108">If no security descriptor is specified, the default security is used.</span></span> <span data-ttu-id="40fb3-109">Weitere Informationen finden Sie unter [Festlegen von namepace-Sicherheits Deskriptoren](setting-namespace-security-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="40fb3-109">For more information, see [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).</span></span>

<span data-ttu-id="40fb3-110">Mit der folgenden Prozedur wird die Sicherheits Beschreibung für den Namespace " *\\ MyNamespace* " des Stamm Verzeichnisses festgelegt.</span><span class="sxs-lookup"><span data-stu-id="40fb3-110">The following procedure sets the security descriptor for the *root\\MyNamespace* namespace.</span></span> <span data-ttu-id="40fb3-111">Die SDDL-Zeichenfolge legt den Besitzer und die Gruppe auf authentifizierte Benutzer fest und gibt eine freigegebene [*Zugriffs Steuerungs Liste (DACL)*](/windows/desktop/SecGloss/d-gly) an, die von untergeordneten Namespaces geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="40fb3-111">The SDDL string sets the owner and group to authenticated users and specifies a [*discretionary access control list (DACL)*](/windows/desktop/SecGloss/d-gly) that is inherited by child namespaces.</span></span> <span data-ttu-id="40fb3-112">Die DACL ermöglicht dem Benutzer das Recht, Daten zu lesen, Methoden auszuführen, Daten in Anbieter Klassen zu schreiben und Remote Zugriff zu verwenden: **WBEM \_ enable**, **WBEM \_ method \_ Execute**, **WBEM \_ Write \_ Provider**, **WBEM \_ Remote \_ Access**.</span><span class="sxs-lookup"><span data-stu-id="40fb3-112">The DACL allows the user the right to read data, execute methods, write data to provider classes and use remote access: **WBEM\_ENABLE**, **WBEM\_METHOD\_EXECUTE**, **WBEM\_WRITE\_PROVIDER**, **WBEM\_REMOTE\_ACCESS**.</span></span> <span data-ttu-id="40fb3-113">Weitere Informationen finden Sie unter [zugreifen auf WMI-Namespaces](access-to-wmi-namespaces.md).</span><span class="sxs-lookup"><span data-stu-id="40fb3-113">For more information, see [Access to WMI Namespaces](access-to-wmi-namespaces.md).</span></span>

<span data-ttu-id="40fb3-114">**So legen Sie eine Namespace-DACL fest**</span><span class="sxs-lookup"><span data-stu-id="40fb3-114">**To set a namespace DACL**</span></span>

1.  <span data-ttu-id="40fb3-115">Erstellen Sie eine MOF-Datei (Managed Object Format), oder ändern Sie die vorhandene MOF-Datei, die den Namespace definiert, um den **namespacesecuritysddl** -Qualifizierer der SDDL-Zeichenfolge hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="40fb3-115">Create a Managed Object Format (MOF) file or modify your existing MOF file that defines the namespace to add the **NamespaceSecuritySDDL** qualifier with the SDDL string.</span></span>

    <span data-ttu-id="40fb3-116">Im folgenden Codebeispiel wird gezeigt, wie der Namespace, der geändert werden soll, der Stamm \\ MyNamespace und die Datei den Namen MyNamespace \_ Security. MOF hat.</span><span class="sxs-lookup"><span data-stu-id="40fb3-116">The following code example shows the namespace to be modified is root\\MyNamespace and the file is named MyNamespace\_security.mof.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  <span data-ttu-id="40fb3-117">Beachten Sie, dass bei der SDDL-Zeichenfolge die Groß-/Kleinschreibung beachtet wird: die Buchstaben müssen groß geschrieben werden</span><span class="sxs-lookup"><span data-stu-id="40fb3-117">Be aware that the SDDL string is case-sensitive: the letters must be capitalized.</span></span>

    <span data-ttu-id="40fb3-118">Das folgende Codebeispiel zeigt die Buchstaben "o" und "g" in der SDDL-Zeichenfolge in Kleinbuchstaben und bewirkt, dass Mofcomp.exe einen Fehler zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="40fb3-118">The following code example shows the letters "o" and "g" in the SDDL string as lowercase and will cause Mofcomp.exe to return an error.</span></span>

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  <span data-ttu-id="40fb3-119">Führen Sie [**Mofcomp.exe**](mofcomp.md) aus, um die MOF-Datei zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="40fb3-119">Run [**Mofcomp.exe**](mofcomp.md) to compile the MOF file.</span></span>

    <span data-ttu-id="40fb3-120">**c: " \\ mynamespace" " \_ Security. mof"**</span><span class="sxs-lookup"><span data-stu-id="40fb3-120">**c:\\mofcomp MyNamespace\_security.mof**</span></span>

    <span data-ttu-id="40fb3-121">Verwenden Sie in C++ die [**imuf Compiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="40fb3-121">In C++, use the [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) methods.</span></span>

4.  <span data-ttu-id="40fb3-122">Wenn Sie versuchen, die Namespace-DACL festzulegen, sollten Sie die folgenden Fehlermeldungen beachten:</span><span class="sxs-lookup"><span data-stu-id="40fb3-122">If your attempt to set the namespace DACL fails, consider the following error messages:</span></span>

    

    | <span data-ttu-id="40fb3-123">Fehler</span><span class="sxs-lookup"><span data-stu-id="40fb3-123">Error</span></span>                           | <span data-ttu-id="40fb3-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="40fb3-124">Description</span></span>                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="40fb3-125">**\_Ungültiger WBEM E- \_ \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="40fb3-125">**WBEM\_E\_INVALID\_PARAMETER**</span></span> | <span data-ttu-id="40fb3-126">Es ist keine geerbte DACL vorhanden.</span><span class="sxs-lookup"><span data-stu-id="40fb3-126">There is no inherited DACL.</span></span> <span data-ttu-id="40fb3-127">Alternativ hat der Aufrufer die DACL oder die SD im übergeordneten Namespace verletzt.</span><span class="sxs-lookup"><span data-stu-id="40fb3-127">Alternately, the caller has violated the DACL or the SD in the parent namespace.</span></span> |
    | <span data-ttu-id="40fb3-128">**WBEM \_ E- \_ Zugriff \_ verweigert**</span><span class="sxs-lookup"><span data-stu-id="40fb3-128">**WBEM\_E\_ACCESS\_DENIED**</span></span>     | <span data-ttu-id="40fb3-129">Der Aufrufer verfügt nicht über die Berechtigung zum Aktualisieren der SDDL in MOF.</span><span class="sxs-lookup"><span data-stu-id="40fb3-129">The caller does not have permission to update the SDDL in MOF.</span></span>                                               |

    

     

## <a name="related-topics"></a><span data-ttu-id="40fb3-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40fb3-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40fb3-131">Festlegen von Namespace-Sicherheits Deskriptoren</span><span class="sxs-lookup"><span data-stu-id="40fb3-131">Setting Namespace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="40fb3-132">**Namespace-Zugriffsrechte Konstanten**</span><span class="sxs-lookup"><span data-stu-id="40fb3-132">**Namespace Access Rights Constants**</span></span>](namespace-access-rights-constants.md)
</dt> <dt>

[<span data-ttu-id="40fb3-133">**Namespace-ACE-Flag-Konstanten**</span><span class="sxs-lookup"><span data-stu-id="40fb3-133">**Namespace ACE Flag Constants**</span></span>](namespace-ace-flag-constants.md)
</dt> <dt>

[<span data-ttu-id="40fb3-134">Ändern der Zugriffssicherheit für Sicherungs fähige Objekte</span><span class="sxs-lookup"><span data-stu-id="40fb3-134">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
