---
description: Die RelPath-Eigenschaft des errbemubjectpath-Objekts enthält den relativen Pfad vom gesamten Pfad.
ms.assetid: 9a4363ae-b6b3-4e8c-a7ca-a9e48c28e19b
ms.tgt_platform: multiple
title: Errbemubjectpath. RelPath-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Relpath
- ISWbemObjectPath.Relpath
- ISWbemObjectPath.get_Relpath
- ISWbemObjectPath.put_Relpath
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8330d1cdc65e818acd4fda63b223303b779b5472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366127"
---
# <a name="swbemobjectpathrelpath-property"></a><span data-ttu-id="6eaf9-103">Errbemubjectpath. RelPath (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6eaf9-103">SWbemObjectPath.Relpath property</span></span>

<span data-ttu-id="6eaf9-104">Die **RelPath** -Eigenschaft des [**errbemubjectpath**](swbemobjectpath.md) -Objekts enthält den relativen Pfad vom gesamten Pfad.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-104">The **Relpath** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the relative path from the complete path.</span></span>

<span data-ttu-id="6eaf9-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6eaf9-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="6eaf9-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="6eaf9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6eaf9-107">Syntax</span></span>


```VB
SWbemObjectPath.Relpath As String
```



## <a name="property-value"></a><span data-ttu-id="6eaf9-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6eaf9-108">Property value</span></span>

## <a name="examples"></a><span data-ttu-id="6eaf9-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6eaf9-109">Examples</span></span>

<span data-ttu-id="6eaf9-110">Das folgende VBScript-Codebeispiel zeigt den Unterschied zwischen den Daten, die von " [**errbemubject. Path \_**](swbemobject-path-.md) " und " **errbemubjectpath. RelPath**" abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6eaf9-110">The following VBScript code example shows the difference between the data obtained from [**SWbemObject.Path\_**](swbemobject-path-.md) and **SWbemObjectPath.Relpath**.</span></span>


```VB
set objWMIService = GetObject ("winmgmts:root/cimv2")

set Processes = objWMIService.ExecQuery( _
    "Select * from win32_process")

For Each Process in Processes
 WScript.Echo Process.Path_ 
 WScript.Echo Process.Path_.Relpath
Next
```



## <a name="requirements"></a><span data-ttu-id="6eaf9-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6eaf9-111">Requirements</span></span>



| <span data-ttu-id="6eaf9-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6eaf9-112">Requirement</span></span> | <span data-ttu-id="6eaf9-113">Wert</span><span class="sxs-lookup"><span data-stu-id="6eaf9-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eaf9-114">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6eaf9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6eaf9-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6eaf9-115">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6eaf9-116">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6eaf9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6eaf9-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6eaf9-117">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6eaf9-118">Header</span><span class="sxs-lookup"><span data-stu-id="6eaf9-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="6eaf9-119"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6eaf9-119"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6eaf9-120">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="6eaf9-120">Type library</span></span><br/>             | <dl> <span data-ttu-id="6eaf9-121"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6eaf9-121"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6eaf9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="6eaf9-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eaf9-123"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eaf9-123"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6eaf9-124">CLSID</span><span class="sxs-lookup"><span data-stu-id="6eaf9-124">CLSID</span></span><br/>                    | <span data-ttu-id="6eaf9-125">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="6eaf9-125">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="6eaf9-126">IID</span><span class="sxs-lookup"><span data-stu-id="6eaf9-126">IID</span></span><br/>                      | <span data-ttu-id="6eaf9-127">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="6eaf9-127">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




