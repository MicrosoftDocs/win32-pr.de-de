---
title: Bindungs Zeichenfolge
description: Aufgrund der Anzahl von Objekten, auf die von einem Verzeichnisdienst aus zugegriffen werden kann, können Namenskollisionen auftreten.
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- Bindungs Zeichenfolge ADSI
- ADsPath ADSI, Beschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103949106"
---
# <a name="binding-string"></a><span data-ttu-id="d5a9b-105">Bindungs Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d5a9b-105">Binding String</span></span>

<span data-ttu-id="d5a9b-106">Aufgrund der Anzahl von Objekten, auf die von einem Verzeichnisdienst aus zugegriffen werden kann, können Namenskollisionen auftreten.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-106">Due to the number of objects accessible from a directory service, naming collisions can occur.</span></span> <span data-ttu-id="d5a9b-107">Die Bindungs Zeichenfolge, die im Allgemeinen als ADsPath bezeichnet wird, ermöglicht es Ihnen, ein bestimmtes Objekt anzugeben, ohne einen namens Konflikt zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-107">The binding string, which is commonly referred to as the ADsPath, enables you to specify a particular object without causing a naming collision.</span></span> <span data-ttu-id="d5a9b-108">Dies kann für einen einzelnen Verzeichnis Dienstanbieter oder für mehrere Verzeichnis Dienstanbieter angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-108">This can be applied for a single directory service provider or across multiple directory service providers.</span></span>

<span data-ttu-id="d5a9b-109">Ein ADsPath ist eine Zeichenfolge, die ein ADSI-Objekt in einem Verzeichnisdienst eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-109">An ADsPath is a string that uniquely identifies an ADSI object on a directory service.</span></span> <span data-ttu-id="d5a9b-110">Da ADSI-Objekte innerhalb des Kontexts des Namespace des zugrunde liegenden Verzeichnis Dienstanbieters vorhanden sind, ist ein Teil der Syntax eines ADsPath-namens Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-110">Because ADSI objects exist within the context of the namespace of the underlying directory service, part of the syntax of an ADsPath name is provider-specific.</span></span>

<span data-ttu-id="d5a9b-111">In der folgenden Tabelle sind die standardmäßig bereitgestellten ADSI-Anbieter aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-111">The following table lists the ADSI providers provided by default.</span></span>



| <span data-ttu-id="d5a9b-112">Anbieter</span><span class="sxs-lookup"><span data-stu-id="d5a9b-112">Provider</span></span>         | <span data-ttu-id="d5a9b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5a9b-113">Description</span></span>                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a9b-114">WinNT</span><span class="sxs-lookup"><span data-stu-id="d5a9b-114">WinNT</span></span><br/> | <span data-ttu-id="d5a9b-115">Wird zur Kommunikation mit Windows-Domänen Controllern verwendet.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-115">Used to communicate with Windows domain controllers.</span></span> <span data-ttu-id="d5a9b-116">Weitere Informationen zu WinNT ADsPath finden Sie unter [Winnt ADsPath](winnt-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-116">For more information about the WinNT ADsPath, see [WinNT ADsPath](winnt-adspath.md).</span></span><br/>           |
| <span data-ttu-id="d5a9b-117">LDAP</span><span class="sxs-lookup"><span data-stu-id="d5a9b-117">LDAP</span></span><br/>  | <span data-ttu-id="d5a9b-118">Wird für die Kommunikation mit LDAP-Servern verwendet, z. b. Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-118">Used to communicate with LDAP servers, such as Active Directory.</span></span> <span data-ttu-id="d5a9b-119">Weitere Informationen zum LDAP-ADsPath finden Sie unter [LDAP ADsPath](ldap-adspath.md).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-119">For more information about the LDAP ADsPath, see [LDAP ADsPath](ldap-adspath.md).</span></span><br/>  |
| <span data-ttu-id="d5a9b-120">Teams</span><span class="sxs-lookup"><span data-stu-id="d5a9b-120">ADs</span></span><br/>   | <span data-ttu-id="d5a9b-121">Stellt eine [**iadsnamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) -Implementierung bereit, die zum Auflisten aller auf dem Client installierten ADSI-Anbieter verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-121">Provides an [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) implementation that can be used to enumerate all of the ADSI providers installed on the client.</span></span><br/> |



 

<span data-ttu-id="d5a9b-122">Verwenden Sie diese Anbieter Namen, um auf den Standard Namespace des Anbieters zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-122">Use these provider names to access the default provider namespace.</span></span> <span data-ttu-id="d5a9b-123">Wenn Sie z. b. eine Bindung an LDAP herstellen, bindet ADSI an einen Container, der das derzeit angemeldete Domänen Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-123">For example, if you bind to LDAP, ADSI binds to a container that contains the domain object currently logged on.</span></span> <span data-ttu-id="d5a9b-124">Wenn Sie eine Bindung an WinNT herstellen, bindet ADSI eine Bindung an einen Container mit Objekten, die mit allen Domänen im Netzwerk korrelieren.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-124">If you bind to WinNT, ADSI binds to a container that holds objects that correlate to all domains on the network.</span></span>

<span data-ttu-id="d5a9b-125">Die ursprünglichen Elemente der ADsPath-Zeichenfolge sind der Programm Bezeichner (ProgID) des ADSI-Anbieters, gefolgt von "://", gefolgt von der Syntax, die vom Anbieter Namespace vorgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-125">The initial elements of the ADsPath string are the programmatic identifier (progID) of the ADSI provider, followed by "://", followed by syntax dictated by the provider namespace.</span></span> <span data-ttu-id="d5a9b-126">Die ProgID-Zeichenfolge kann je nach Anbieter die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-126">The progID string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="d5a9b-127">Die ProgID-Zeichen folgen für die oben aufgeführten Anbieter unterliegen der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-127">The progID strings for the providers listed above are case-sensitive.</span></span>

<span data-ttu-id="d5a9b-128">Die Pfad Zeichenfolge kann je nach Anbieter die Groß-/Kleinschreibung beachten.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-128">The path string may or may not be case-sensitive, depending on the provider.</span></span> <span data-ttu-id="d5a9b-129">Die Pfad Zeichenfolgen für die oben aufgeführten Anbieter unterliegen nicht der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-129">The path strings for the providers listed above are not case-sensitive.</span></span>

<span data-ttu-id="d5a9b-130">Im folgenden finden Sie Beispiele für adspaths.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-130">The following are examples of ADsPaths.</span></span>

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

<span data-ttu-id="d5a9b-131">Wenn Sie alle auf dem Computer installierten Anbieter suchen möchten, binden Sie ihn an den ADS-Anbieter, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-131">To find all providers installed on your computer, bind to the ADs provider as shown in the following code example.</span></span>


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



<span data-ttu-id="d5a9b-132">Mithilfe des LDAP-Anbieters können Sie den ADsPath entweder in einem DN-Formular (X. 500 Distinguished Name) angeben, beginnend mit dem CN-Tag, oder Sie können die hierarchische Umkehrung angeben, beginnend mit dem O-Tag.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-132">Using the LDAP provider, you can specify the ADsPath either in an X.500 distinguished name (DN) form, starting with the CN tag, or you can specify its hierarchical inverse, starting with the O tag.</span></span> <span data-ttu-id="d5a9b-133">Das Formular, das Sie in der anfänglichen ADsPath-Anwendung verwenden, bestimmt die Reihenfolge der Tags.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-133">The form you use in the initial ADsPath determines the order of the tags.</span></span>

<span data-ttu-id="d5a9b-134">In der folgenden Tabelle werden ADsPath-Sonderzeichen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-134">The following table lists ADsPath special characters.</span></span>



| <span data-ttu-id="d5a9b-135">Name</span><span class="sxs-lookup"><span data-stu-id="d5a9b-135">Name</span></span>                      | <span data-ttu-id="d5a9b-136">Zeichen</span><span class="sxs-lookup"><span data-stu-id="d5a9b-136">Character</span></span>           | <span data-ttu-id="d5a9b-137">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d5a9b-137">Description</span></span>                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5a9b-138">Doppeltes Anführungszeichen</span><span class="sxs-lookup"><span data-stu-id="d5a9b-138">Double quote</span></span><br/>   | <span data-ttu-id="d5a9b-139">"</span><span class="sxs-lookup"><span data-stu-id="d5a9b-139">"</span></span><br/>        | <span data-ttu-id="d5a9b-140">Wird verwendet, um einen Teil des ADsPath anzugeben, der möglicherweise ein Sonderzeichen enthält, sodass die Zeichenfolge buchstäblich interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-140">Used to quote any part of the ADsPath that may contain a special character so that the string is interpreted literally.</span></span> <span data-ttu-id="d5a9b-141">Beispiel: "CN = Name/prefix".</span><span class="sxs-lookup"><span data-stu-id="d5a9b-141">For example, "CN=Name/Prefix".</span></span><br/>                                     |
| <span data-ttu-id="d5a9b-142">Umgekehrter Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="d5a9b-142">Backslash</span></span><br/>      | \\<br/>       | <span data-ttu-id="d5a9b-143">Wird für Sonderzeichen verwendet, um anzugeben, dass Sie als Literale verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-143">Used to precede special characters to signify they should be used as literals.</span></span> <span data-ttu-id="d5a9b-144">Weitere Informationen und eine Liste von Sonderzeichen finden Sie unter [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-144">For more information and a list of special characters, see [Distinguished Names](/previous-versions/windows/desktop/ldap/distinguished-names).</span></span><br/> |
| <span data-ttu-id="d5a9b-145">ßen</span><span class="sxs-lookup"><span data-stu-id="d5a9b-145">Slash</span></span><br/>          | /<br/>        | <span data-ttu-id="d5a9b-146">Komponenten Trennzeichen.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-146">Component separator.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="d5a9b-147">Geschweifte Klammern</span><span class="sxs-lookup"><span data-stu-id="d5a9b-147">Angle brackets</span></span><br/> | <><br/> | <span data-ttu-id="d5a9b-148">Begrenzen Sie einen ADsPath innerhalb einer anderen Benennungs Konvention.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-148">Delimit an ADsPath within another naming convention.</span></span><br/>                                                                                                                                       |



 

<span data-ttu-id="d5a9b-149">Wenn Sie einen ADsPath in einer Such Spezifikation oder als Teil einer URL begrenzen möchten, verwenden Sie die linke und die Rechte Spitze Klammer (< >).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-149">To delimit an ADsPath in a search specification or as part of a URL, use the left and right angle bracket (< >).</span></span> <span data-ttu-id="d5a9b-150">Beispiel: " &lt; Winnt://mydomain/Useraccount &gt; ".</span><span class="sxs-lookup"><span data-stu-id="d5a9b-150">For example, "&lt;WinNT://MyDomain/UserAccount&gt;".</span></span>

<span data-ttu-id="d5a9b-151">Einige ADSI-Anbieter haben aufgrund von Namespace Anforderungen möglicherweise Syntax Einschränkungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d5a9b-151">Some ADSI providers may have added syntax restrictions due to namespace requirements.</span></span>

## <a name="active-directory-binding-options"></a><span data-ttu-id="d5a9b-152">Bindungs Optionen Active Directory</span><span class="sxs-lookup"><span data-stu-id="d5a9b-152">Active Directory Binding Options</span></span>

<span data-ttu-id="d5a9b-153">Active Directory bietet die Möglichkeit, an ein Objekt zu binden, indem es verschiedene andere Typen von Bindungs Zeichenfolgen verwendet, z. b. eine com-Globally Unique Identifier (GUID) oder eine Sicherheits-ID (SID).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-153">Active Directory provides the ability to bind to an object using several other types of binding strings, such as a COM globally unique identifier (GUID) or a security identifier (SID).</span></span> <span data-ttu-id="d5a9b-154">Weitere Informationen finden Sie unter [binden an Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span><span class="sxs-lookup"><span data-stu-id="d5a9b-154">For more information, see [Binding to Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services).</span></span>

 

