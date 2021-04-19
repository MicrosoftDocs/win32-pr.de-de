---
description: Wenn Sie die Skript-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema als Teil eines Monikers an.
ms.assetid: 3c64047d-ce3a-4180-8f71-0e66c2e61627
ms.tgt_platform: multiple
title: Abrufen von geänderten Klassen mithilfe der Skript-API für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cef1971232eabdb984ad4321b5cadbdedd8b2be7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348889"
---
# <a name="retrieving-amended-classes-using-the-scripting-api-for-wmi"></a><span data-ttu-id="76f0a-103">Abrufen von geänderten Klassen mithilfe der Skript-API für WMI</span><span class="sxs-lookup"><span data-stu-id="76f0a-103">Retrieving Amended Classes Using the Scripting API for WMI</span></span>

<span data-ttu-id="76f0a-104">Wenn Sie die Skript-API für WMI verwenden, um lokalisierte Klassen Informationen abzurufen oder zu speichern, geben Sie das Gebiets Schema als Teil eines Monikers an.</span><span class="sxs-lookup"><span data-stu-id="76f0a-104">If you are using the Scripting API for WMI to retrieve or store localized class information, specify the locale as part of a moniker.</span></span> <span data-ttu-id="76f0a-105">Oder Sie können den Gebiets Schema Namen im "" "" "" " *" der Methode* "" von "" "" [**".**](swbemlocator-connectserver.md)</span><span class="sxs-lookup"><span data-stu-id="76f0a-105">Or, you can supply the locale name in the *strLocale* parameter to the [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md) method.</span></span> <span data-ttu-id="76f0a-106">Wenn Sie geänderte Klassen lesen oder schreiben möchten, geben Sie an, dass Sie lokalisierte Klassendefinitionen verwenden möchten, indem Sie [wbemflaguseamendedqualifizierer](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) als Flag für den *IFlags* -Parameter der aufzurufenden Methode angeben.</span><span class="sxs-lookup"><span data-stu-id="76f0a-106">When reading or writing amended classes, indicate that you want to use localized class definitions by specifying [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) as a flag for the *iFlags* parameter of the method you call.</span></span> <span data-ttu-id="76f0a-107">Für PowerShell können Sie den *-locale-* Parameter für [Get-WMIObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) verwenden, um das Gebiets Schema anzugeben.</span><span class="sxs-lookup"><span data-stu-id="76f0a-107">For PowerShell, you can use the *-locale* parameter on [Get-WmiObject](/powershell/module/microsoft.powershell.management/get-wmiobject?view=powershell-5.1&preserve-view=true) to specify the locale.</span></span>

<span data-ttu-id="76f0a-108">Im folgenden Codebeispiel wird gezeigt, wie eine lokalisierte Klasse mit einem WMI-skriptingmoniker oder dem-locale-Parameter abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="76f0a-108">The following code example shows how to retrieve a localized class by using a WMI scripting moniker or the -locale parameter.</span></span>


```VB
Set objwbemobject = GetObject("winmgmts:[locale=ms_409]!root/test:myclass")
```


```PowerShell

Get-WmiObject myclass -Namespace &quot;root\test&quot; -Locale &quot;ms_409&quot;
```





<span data-ttu-id="76f0a-109">Im folgenden Codebeispiel wird gezeigt, wie Sie den locale-Parameter festlegen und das [wbemflaguseamendedqualifizierungsflag](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) verwenden.</span><span class="sxs-lookup"><span data-stu-id="76f0a-109">The following code example shows how to set the locale parameter and use the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>


```VB
Set Locator = CreateObject("WbemScripting.SWbemLocator")
Set service = Locator.ConnectServer(,"root\test", , , "ms_409")
Set objwbemobject = service.Get("myclass", wbemFlagUseAmendedQualifiers)
```



> [!Note]  
> <span data-ttu-id="76f0a-110">Da der Rückruf für die Senke möglicherweise nicht auf derselben Authentifizierungs Ebene wie der Client zurückgegeben wird, wird empfohlen, semisynchrone anstelle der asynchronen Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="76f0a-110">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="76f0a-111">Weitere Informationen finden Sie unter [Aufrufen einer Methode](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="76f0a-111">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="76f0a-112">In der folgenden Tabelle werden die Methoden aufgelistet, die das [wbemflaguseamendedqualifizierungsflag](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="76f0a-112">The following table lists the methods that accept the [wbemFlagUseAmendedQualifiers](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemflagenum) flag.</span></span>



| <span data-ttu-id="76f0a-113">Synchrone Methode</span><span class="sxs-lookup"><span data-stu-id="76f0a-113">Synchronous Method</span></span>                                                 | <span data-ttu-id="76f0a-114">Asynchrone Methode</span><span class="sxs-lookup"><span data-stu-id="76f0a-114">Asynchronous Method</span></span>                                                          |
|--------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="76f0a-115">**Swap Services. SubclassesOf**</span><span class="sxs-lookup"><span data-stu-id="76f0a-115">**SWbemServices.SubclassesOf**</span></span>](swbemservices-subclassesof.md)   | [<span data-ttu-id="76f0a-116">**Austausch Services. subclassesofasync**</span><span class="sxs-lookup"><span data-stu-id="76f0a-116">**SWbemServices.SubclassesOfAsync**</span></span>](swbemservices-subclassesofasync.md)   |
| [<span data-ttu-id="76f0a-117">**Swap. subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-117">**SWbemObject.Subclasses\_**</span></span>](swbemobject-subclasses-.md)        | [<span data-ttu-id="76f0a-118">**Austauschen von "errbemubject. subclassesasync"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-118">**SWbemObject.SubclassesAsync\_**</span></span>](swbemobject-subclassesasync-.md)        |
| [<span data-ttu-id="76f0a-119">**Swap Services. InstancesOf**</span><span class="sxs-lookup"><span data-stu-id="76f0a-119">**SWbemServices.InstancesOf**</span></span>](swbemservices-instancesof.md)     | [<span data-ttu-id="76f0a-120">**Swap Services. instancesofasync**</span><span class="sxs-lookup"><span data-stu-id="76f0a-120">**SWbemServices.InstancesOfAsync**</span></span>](swbemservices-instancesofasync.md)     |
| [<span data-ttu-id="76f0a-121">**"Errbemubject. Instance"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-121">**SWbemObject.Instances\_**</span></span>](swbemobject-instances-.md)          | [<span data-ttu-id="76f0a-122">**Austauschen von "errbemubject. instancesasync"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-122">**SWbemObject.InstancesAsync\_**</span></span>](swbemobject-instancesasync-.md)          |
| [<span data-ttu-id="76f0a-123">**CquerySWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="76f0a-123">**SWbemServices.ExecQuery**</span></span>](swbemservices-execquery.md)         | [<span data-ttu-id="76f0a-124">**CqueryasyncSWbemServices.Exe**</span><span class="sxs-lookup"><span data-stu-id="76f0a-124">**SWbemServices.ExecQueryAsync**</span></span>](swbemservices-execqueryasync.md)         |
| [<span data-ttu-id="76f0a-125">**Austauschdienste. Get**</span><span class="sxs-lookup"><span data-stu-id="76f0a-125">**SWbemServices.Get**</span></span>](swbemservices-get.md)                     | [<span data-ttu-id="76f0a-126">**"Swap Services. getasync"**</span><span class="sxs-lookup"><span data-stu-id="76f0a-126">**SWbemServices.GetAsync**</span></span>](swbemservices-getasync.md)                     |
| [<span data-ttu-id="76f0a-127">**Swap-Datei\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-127">**SWbemObject.Put\_**</span></span>](swbemobject-put-.md)                      | [<span data-ttu-id="76f0a-128">**Austauschen von "errbemubject. putasync"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-128">**SWbemObject.PutAsync\_**</span></span>](swbemobject-putasync-.md)                      |
| [<span data-ttu-id="76f0a-129">**"Swap Services. referencesto"**</span><span class="sxs-lookup"><span data-stu-id="76f0a-129">**SWbemServices.ReferencesTo**</span></span>](swbemservices-referencesto.md)   | [<span data-ttu-id="76f0a-130">**"Swap Services. referencestoasync"**</span><span class="sxs-lookup"><span data-stu-id="76f0a-130">**SWbemServices.ReferencesToAsync**</span></span>](swbemservices-referencestoasync.md)   |
| [<span data-ttu-id="76f0a-131">**"Errbemubject. References"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-131">**SWbemObject.References\_**</span></span>](swbemobject-references-.md)        | [<span data-ttu-id="76f0a-132">**Austauschen von "errbemubject. referencesasync"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-132">**SWbemObject.ReferencesAsync\_**</span></span>](swbemobject-referencesasync-.md)        |
| [<span data-ttu-id="76f0a-133">**"Taubemservices. associatorsof"**</span><span class="sxs-lookup"><span data-stu-id="76f0a-133">**SWbemServices.AssociatorsOf**</span></span>](swbemservices-associatorsof.md) | [<span data-ttu-id="76f0a-134">**Swap Services. associatorsofasync**</span><span class="sxs-lookup"><span data-stu-id="76f0a-134">**SWbemServices.AssociatorsOfAsync**</span></span>](swbemservices-associatorsofasync.md) |
| [<span data-ttu-id="76f0a-135">**"Errbemujeject. ASSOCIATORS"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-135">**SWbemObject.Associators\_**</span></span>](swbemobject-associators-.md)      | [<span data-ttu-id="76f0a-136">**"Errbemubject. associatorsasync"\_**</span><span class="sxs-lookup"><span data-stu-id="76f0a-136">**SWbemObject.AssociatorsAsync\_**</span></span>](swbemobject-associatorsasync-.md)      |



 

 

 
