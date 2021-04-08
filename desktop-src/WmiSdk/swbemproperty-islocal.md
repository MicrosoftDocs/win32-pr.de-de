---
description: Die IsLocal-Eigenschaft des "Swap Property"-Objekts ist ein boolescher Wert, der verwendet werden kann, um zu bestimmen, ob diese Eigenschaft lokal ist. Der Wert false gibt an, dass diese Eigenschaft von einer anderen Klasse geerbt wurde. Diese Eigenschaft ist schreibgeschützt.
ms.assetid: eda1f962-03b5-4322-bb06-c27aedf94be1
ms.tgt_platform: multiple
title: Swap Property. IsLocal-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemProperty.IsLocal
- ISWbemProperty.IsLocal
- ISWbemProperty.get_IsLocal
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 187613a0111c7ad482c55e3d294d77fddb5b0941
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865656"
---
# <a name="swbempropertyislocal-property"></a><span data-ttu-id="63e92-105">Swap Property. IsLocal (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="63e92-105">SWbemProperty.IsLocal property</span></span>

<span data-ttu-id="63e92-106">Die **IsLocal** -Eigenschaft des " [**Swap Property**](swbemproperty.md) "-Objekts ist ein boolescher Wert, der verwendet werden kann, um zu bestimmen, ob diese Eigenschaft lokal ist.</span><span class="sxs-lookup"><span data-stu-id="63e92-106">The **IsLocal** property of the [**SWbemProperty**](swbemproperty.md) object is a Boolean value that can be used to determine if this property is local.</span></span> <span data-ttu-id="63e92-107">Der Wert **false** gibt an, dass diese Eigenschaft von einer anderen Klasse geerbt wurde.</span><span class="sxs-lookup"><span data-stu-id="63e92-107">A value of **FALSE** indicates that this property has been inherited from another class.</span></span> <span data-ttu-id="63e92-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="63e92-108">This property is read-only.</span></span>

<span data-ttu-id="63e92-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="63e92-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="63e92-110">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="63e92-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e92-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e92-111">Syntax</span></span>


```VB
SWbemProperty.IsLocal As Boolean
```



## <a name="property-value"></a><span data-ttu-id="63e92-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="63e92-112">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="63e92-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63e92-113">Requirements</span></span>



| <span data-ttu-id="63e92-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63e92-114">Requirement</span></span> | <span data-ttu-id="63e92-115">Wert</span><span class="sxs-lookup"><span data-stu-id="63e92-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63e92-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63e92-116">Minimum supported client</span></span><br/> | <span data-ttu-id="63e92-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="63e92-117">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="63e92-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63e92-118">Minimum supported server</span></span><br/> | <span data-ttu-id="63e92-119">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="63e92-119">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="63e92-120">Header</span><span class="sxs-lookup"><span data-stu-id="63e92-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="63e92-121"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e92-121"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="63e92-122">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="63e92-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="63e92-123"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="63e92-123"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="63e92-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63e92-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63e92-125"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63e92-125"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="63e92-126">CLSID</span><span class="sxs-lookup"><span data-stu-id="63e92-126">CLSID</span></span><br/>                    | <span data-ttu-id="63e92-127">CLSID- \_ Swap-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="63e92-127">CLSID\_SWbemProperty</span></span><br/>                                                         |
| <span data-ttu-id="63e92-128">IID</span><span class="sxs-lookup"><span data-stu-id="63e92-128">IID</span></span><br/>                      | <span data-ttu-id="63e92-129">IID \_ iswbemproperty</span><span class="sxs-lookup"><span data-stu-id="63e92-129">IID\_ISWbemProperty</span></span><br/>                                                          |



 

 




