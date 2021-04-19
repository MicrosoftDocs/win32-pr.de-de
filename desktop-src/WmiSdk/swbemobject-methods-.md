---
description: Die Methods- \_ Eigenschaft des "errbemubject"-Objekts gibt ein "errbemmethodset"-Objekt zurück, das eine Auflistung der Methoden für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: ef9abced-5126-4698-b01e-f3e9c871162f
ms.tgt_platform: multiple
title: SWbemObject.Methods_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Methods_
- ISWbemObject.Methods_
- ISWbemObject.get_Methods_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6a702f0acf0736810de4d3176f8695fa8008d3ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362677"
---
# <a name="swbemobjectmethods_-property"></a><span data-ttu-id="6c5e0-104">' Errbemubject. Methods '- \_ Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="6c5e0-104">SWbemObject.Methods\_ property</span></span>

<span data-ttu-id="6c5e0-105">Die **Methods \_** -Eigenschaft des " [**errbemubject**](swbemobject.md) "-Objekts gibt ein " [**errbemmethodset**](swbemmethodset.md) "-Objekt zurück, das eine Auflistung der Methoden für die aktuelle Klasse oder Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="6c5e0-105">The **Methods\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemMethodSet**](swbemmethodset.md) object that is a collection of the methods for the current class or instance.</span></span> <span data-ttu-id="6c5e0-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6c5e0-106">This property is read-only.</span></span>

<span data-ttu-id="6c5e0-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6c5e0-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6c5e0-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6c5e0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5e0-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c5e0-109">Syntax</span></span>


```VB
SWbemObject.Methods_ As Object
```



## <a name="property-value"></a><span data-ttu-id="6c5e0-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6c5e0-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6c5e0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6c5e0-111">Examples</span></span>

<span data-ttu-id="6c5e0-112">Das folgende [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1)aus der TechNet Gallery beschreibt, wie alle Methoden einer Klasse aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="6c5e0-112">The following [code sample](https://Gallery.TechNet.Microsoft.Com/c15624ee-e335-4d58-a022-aed73ad330a1), taken from the TechNet Gallery, describes how to list all methods of a class.</span></span>


```VB
strComputer = "." 
strNameSpace = "root\cimv2" 
strClass = "Win32_Service" 
  
Set objClass = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & _  
    strComputer & "\" & strNameSpace & ":" & strClass) 
  
WScript.Echo strClass & " Class Methods" 
WScript.Echo "---------------------------" 
  
For Each objClassMethod In objClass.Methods_ 
    WScript.Echo objClassMethod.Name 
Next 
```



## <a name="requirements"></a><span data-ttu-id="6c5e0-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5e0-113">Requirements</span></span>



| <span data-ttu-id="6c5e0-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c5e0-114">Requirement</span></span> | <span data-ttu-id="6c5e0-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5e0-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5e0-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c5e0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5e0-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6c5e0-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6c5e0-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c5e0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5e0-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6c5e0-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6c5e0-120">Header</span><span class="sxs-lookup"><span data-stu-id="6c5e0-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5e0-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5e0-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c5e0-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6c5e0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="6c5e0-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6c5e0-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6c5e0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="6c5e0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c5e0-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5e0-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6c5e0-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="6c5e0-126">CLSID</span></span><br/>                    | <span data-ttu-id="6c5e0-127">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="6c5e0-127">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6c5e0-128">IID</span><span class="sxs-lookup"><span data-stu-id="6c5e0-128">IID</span></span><br/>                      | <span data-ttu-id="6c5e0-129">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="6c5e0-129">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




