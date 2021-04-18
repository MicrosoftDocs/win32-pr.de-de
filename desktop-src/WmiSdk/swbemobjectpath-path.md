---
description: Die Path-Eigenschaft des "errbemubjectpath"-Objekts enthält den absoluten Pfad. Dies entspricht der \_ \_ Path-Eigenschaft in der com-API. Dies ist die Standard Eigenschaft dieses Objekts.
ms.assetid: cc0d2c56-bb69-4008-8688-0166714ea5fd
ms.tgt_platform: multiple
title: Errbemubjectpath. Path-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Path
- ISWbemObjectPath.Path
- ISWbemObjectPath.get_Path
- ISWbemObjectPath.put_Path
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02a3dfbf6dbc24434ad4d9807ab5e39dbc121043
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357837"
---
# <a name="swbemobjectpathpath-property"></a><span data-ttu-id="8a7ce-105">Errbemubjectpath. Path-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8a7ce-105">SWbemObjectPath.Path property</span></span>

<span data-ttu-id="8a7ce-106">Die **path** -Eigenschaft des " [**errbemubjectpath**](swbemobjectpath.md) "-Objekts enthält den absoluten Pfad.</span><span class="sxs-lookup"><span data-stu-id="8a7ce-106">The **Path** property of the [**SWbemObjectPath**](swbemobjectpath.md) object contains the absolute path.</span></span> <span data-ttu-id="8a7ce-107">Dies entspricht der [ \_ \_ path](wmi-system-properties.md) -Eigenschaft in der com-API.</span><span class="sxs-lookup"><span data-stu-id="8a7ce-107">This is the same as the [\_\_Path](wmi-system-properties.md) property in the COM API.</span></span> <span data-ttu-id="8a7ce-108">Dies ist die Standard Eigenschaft dieses Objekts.</span><span class="sxs-lookup"><span data-stu-id="8a7ce-108">This is the default property of this object.</span></span>

<span data-ttu-id="8a7ce-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8a7ce-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="8a7ce-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="8a7ce-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a7ce-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a7ce-111">Syntax</span></span>


```VB
SWbemObjectPath.Path As String
```



## <a name="property-value"></a><span data-ttu-id="8a7ce-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="8a7ce-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="8a7ce-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8a7ce-113">Requirements</span></span>



| <span data-ttu-id="8a7ce-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8a7ce-114">Requirement</span></span> | <span data-ttu-id="8a7ce-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8a7ce-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a7ce-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8a7ce-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8a7ce-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a7ce-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8a7ce-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8a7ce-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8a7ce-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a7ce-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8a7ce-120">Header</span><span class="sxs-lookup"><span data-stu-id="8a7ce-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a7ce-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8a7ce-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a7ce-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="8a7ce-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a7ce-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8a7ce-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8a7ce-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8a7ce-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a7ce-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a7ce-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a7ce-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="8a7ce-126">CLSID</span></span><br/>                    | <span data-ttu-id="8a7ce-127">CLSID- \_ Swap-Austausch Pfad</span><span class="sxs-lookup"><span data-stu-id="8a7ce-127">CLSID\_SWbemObjectPath</span></span><br/>                                                       |
| <span data-ttu-id="8a7ce-128">IID</span><span class="sxs-lookup"><span data-stu-id="8a7ce-128">IID</span></span><br/>                      | <span data-ttu-id="8a7ce-129">IID \_ iswbemubjectpath</span><span class="sxs-lookup"><span data-stu-id="8a7ce-129">IID\_ISWbemObjectPath</span></span><br/>                                                        |



 

 




