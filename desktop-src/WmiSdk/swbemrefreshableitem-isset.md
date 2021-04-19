---
description: Die Eigenschaft "chanbemerfrischendes ableitem. isset" ist ein boolescher Wert, der angibt, ob das Objekt "Swap-ableitem" ein einzelnes Objekt oder einen Objekt Satz darstellt. Das ' Swap '-Objekt ' ' ist ein einzelnes Objekt oder ein Objekt Satz.
ms.assetid: 4be5d27c-9020-4150-84ce-f9efc55be947
ms.tgt_platform: multiple
title: Swap. isset-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.IsSet
- ISWbemRefreshableItem.get_IsSet
- ISWbemRefreshableItem.put_IsSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 71fb5f84ec7ad35f1d9beab32cb74db5b7591057
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106367273"
---
# <a name="swbemrefreshableitemisset-property"></a><span data-ttu-id="b5310-103">Swap. isset-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b5310-103">SWbemRefreshableItem.IsSet property</span></span>

<span data-ttu-id="b5310-104">Die Eigenschaft " **chanbemerfrischendes ableitem. isset** " ist ein boolescher Wert, der angibt, ob das Objekt " [**Swap-ableitem**](swbemrefreshableitem.md) " ein einzelnes Objekt oder einen Objekt Satz darstellt.</span><span class="sxs-lookup"><span data-stu-id="b5310-104">The **SWbemRefreshableItem.IsSet** property is a Boolean value that indicates whether the [**SWbemRefreshableItem**](swbemrefreshableitem.md) object represents a single object or an object set.</span></span>

<span data-ttu-id="b5310-105">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="b5310-105">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="b5310-106">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b5310-106">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5310-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b5310-107">Syntax</span></span>


```VB
SWbemRefreshableItem.IsSet As Boolean
```



## <a name="property-value"></a><span data-ttu-id="b5310-108">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b5310-108">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="b5310-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b5310-109">Remarks</span></span>

<span data-ttu-id="b5310-110">Wenn die Datei " **errbemaktuableitem. isset** " den Wert " **true**" hat, stellt das Element ein " [**errbewbjectset**](swbemobjectset.md) "-Objekt dar, und die [**Objekt**](swbemrefreshableitem-object.md) Eigenschaft ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b5310-110">If **SWbemRefreshableItem.IsSet** is **TRUE**, then the item represents an [**SWbemObjectSet**](swbemobjectset.md) object and the [**Object**](swbemrefreshableitem-object.md) property will be **NULL**.</span></span> <span data-ttu-id="b5310-111">Wenn der Wert **false** ist, stellt [**das Element ein-Objekt dar**](swbemobject.md) , und die- **Objekt** Eigenschaft ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b5310-111">If **FALSE**, the item represents an [**SWbemObject**](swbemobject.md) object and the **Object** property is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5310-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b5310-112">Requirements</span></span>



| <span data-ttu-id="b5310-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b5310-113">Requirement</span></span> | <span data-ttu-id="b5310-114">Wert</span><span class="sxs-lookup"><span data-stu-id="b5310-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b5310-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b5310-115">Minimum supported client</span></span><br/> | <span data-ttu-id="b5310-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b5310-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b5310-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b5310-117">Minimum supported server</span></span><br/> | <span data-ttu-id="b5310-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b5310-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b5310-119">Header</span><span class="sxs-lookup"><span data-stu-id="b5310-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="b5310-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="b5310-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="b5310-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="b5310-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="b5310-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b5310-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b5310-123">DLL</span><span class="sxs-lookup"><span data-stu-id="b5310-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b5310-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b5310-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="b5310-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="b5310-125">CLSID</span></span><br/>                    | <span data-ttu-id="b5310-126">CLSID, \_ Swap-ableitem</span><span class="sxs-lookup"><span data-stu-id="b5310-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="b5310-127">IID</span><span class="sxs-lookup"><span data-stu-id="b5310-127">IID</span></span><br/>                      | <span data-ttu-id="b5310-128">IID \_ iswbemerfrischendes ableitem</span><span class="sxs-lookup"><span data-stu-id="b5310-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="b5310-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5310-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5310-130">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="b5310-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="b5310-131">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="b5310-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




