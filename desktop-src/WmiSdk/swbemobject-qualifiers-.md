---
description: Die \_ qualifizierereigenschaft des Objekts "errbewbject" gibt ein "errbemqualifierset"-Objekt zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: 5ecae751-0d83-4ad6-9840-ef47f76b1ff6
ms.tgt_platform: multiple
title: SWbemObject.Qualifiers_-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Qualifiers_
- ISWbemObject.Qualifiers_
- ISWbemObject.get_Qualifiers_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f9526596b7ae4a387cd0751ad95aff3b97dcc817
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348882"
---
# <a name="swbemobjectqualifiers_-property"></a><span data-ttu-id="92d2e-104">"Errbemubject. \_ qualifizierereigenschaft"</span><span class="sxs-lookup"><span data-stu-id="92d2e-104">SWbemObject.Qualifiers\_ property</span></span>

<span data-ttu-id="92d2e-105">Die **\_ qualifizierereigenschaft** des Objekts " [**errbewbject**](swbemobject.md) " gibt ein " [**errbemqualifierset**](swbemqualifierset.md) "-Objekt zurück, das eine Auflistung der Qualifizierer für die aktuelle Klasse oder Instanz ist.</span><span class="sxs-lookup"><span data-stu-id="92d2e-105">The **Qualifiers\_** property of the [**SWbemObject**](swbemobject.md) object returns an [**SWbemQualifierSet**](swbemqualifierset.md) object that is a collection of the qualifiers for the current class or instance.</span></span> <span data-ttu-id="92d2e-106">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="92d2e-106">This property is read-only.</span></span>

<span data-ttu-id="92d2e-107">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="92d2e-107">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="92d2e-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="92d2e-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92d2e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="92d2e-109">Syntax</span></span>


```VB
SWbemObject.Qualifiers_ As Object
```



## <a name="property-value"></a><span data-ttu-id="92d2e-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="92d2e-110">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="92d2e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92d2e-111">Examples</span></span>

<span data-ttu-id="92d2e-112">Die [Liste alle Qualifizierer für ein WMI-Klassen](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) -VBScript-Codebeispiel in der TechNet Gallery verwendet die \_ qualifizierereigenschaft, um die Klassen Qualifizierer für eine angegebene WMI-Klasse aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="92d2e-112">The [List All the Qualifiers for a WMI Class](https://Gallery.TechNet.Microsoft.Com/fe7a7ae2-d9d9-4c0f-bbf5-c9c112e90983) VBScript code sample on TechNet Gallery uses the Qualifier\_ property to list the class qualifiers for a specified WMI class.</span></span>

<span data-ttu-id="92d2e-113">Im Codebeispiel [List All Abstract classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript in der TechNet Gallery werden alle WMI-abstrakten Klassen aufgelistet, die im root \\ CIMV2-Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="92d2e-113">The [List All Abstract Classes in WMI](https://Gallery.TechNet.Microsoft.Com/2eb0a3ba-d825-432e-b011-7c6fe358707f) VBScript code sample on TechNet Gallery lists all WMI abstract classes defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="92d2e-114">Im Codebeispiel [List All Dynamic classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript wird die qualifizierereigenschaft verwendet \_ , um alle dynamischen WMI-Klassen (einschließlich Association-Klassen) aufzulisten, die im Stamm- \\ CIMV2-Namespace definiert sind.</span><span class="sxs-lookup"><span data-stu-id="92d2e-114">The [List All Dynamic Classes in WMI](https://Gallery.TechNet.Microsoft.Com/8352ca94-264c-43c7-9dda-258d65ac6c8c) VBScript code sample uses the Qualifier\_ property to list all WMI Dynamic classes (including Association classes) defined in the root\\cimv2 namespace.</span></span>

<span data-ttu-id="92d2e-115">Das [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell-Codebeispiel in der TechNet Gallery listet alle beschreibbaren Eigenschaften im angegebenen Namespace auf.</span><span class="sxs-lookup"><span data-stu-id="92d2e-115">The [Get-WritableWMIProperties.ps1](https://Gallery.TechNet.Microsoft.Com/816fb8b6-cdcf-4156-a9a3-a852ce1d2baa) PowerShell code sample on TechNet Gallery lists all writeable properties in the specified namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="92d2e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92d2e-116">Requirements</span></span>



| <span data-ttu-id="92d2e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92d2e-117">Requirement</span></span> | <span data-ttu-id="92d2e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="92d2e-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="92d2e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92d2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92d2e-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92d2e-120">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="92d2e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92d2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92d2e-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92d2e-122">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="92d2e-123">Header</span><span class="sxs-lookup"><span data-stu-id="92d2e-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="92d2e-124"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="92d2e-124"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="92d2e-125">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="92d2e-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="92d2e-126"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="92d2e-126"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="92d2e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="92d2e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92d2e-128"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92d2e-128"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="92d2e-129">CLSID</span><span class="sxs-lookup"><span data-stu-id="92d2e-129">CLSID</span></span><br/>                    | <span data-ttu-id="92d2e-130">CLSID- \_ Austausch Objekt</span><span class="sxs-lookup"><span data-stu-id="92d2e-130">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="92d2e-131">IID</span><span class="sxs-lookup"><span data-stu-id="92d2e-131">IID</span></span><br/>                      | <span data-ttu-id="92d2e-132">IID \_ iswbemujekt</span><span class="sxs-lookup"><span data-stu-id="92d2e-132">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




