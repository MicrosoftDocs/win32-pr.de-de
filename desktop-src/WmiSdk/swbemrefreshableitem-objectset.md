---
description: Die Eigenschaft "Swap. ObjectSet" stellt das Objekt dar, das aktualisiert werden soll.
ms.assetid: f52101b1-bb6e-4798-b20f-d6efd31cf7c1
ms.tgt_platform: multiple
title: Swap. ObjectSet-Eigenschaft (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.ObjectSet
- ISWbemRefreshableItem.get_ObjectSet
- ISWbemRefreshableItem.put_ObjectSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0cbc611bb9e1a72f53e2178039b0ad76411e39a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351388"
---
# <a name="swbemrefreshableitemobjectset-property"></a><span data-ttu-id="7216f-103">Swap. ObjectSet-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7216f-103">SWbemRefreshableItem.ObjectSet property</span></span>

<span data-ttu-id="7216f-104">Die Eigenschaft " **Swap. ObjectSet** " stellt das Objekt dar, das aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="7216f-104">The **SWbemRefreshableItem.ObjectSet** property represents the object set to be refreshed.</span></span> <span data-ttu-id="7216f-105">Die **ObjectSet** -Eigenschaft ist entweder ein Enumerator oder ein Sammel Element, das in einem " [**Swap**](swbemrefresher.md) -Aktualisierungs"-Objekt enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7216f-105">The **ObjectSet** property is either an enumerator or a collection item that is contained in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span>

<span data-ttu-id="7216f-106">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="7216f-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="7216f-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7216f-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7216f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7216f-108">Syntax</span></span>


```VB
SWbemRefreshableItem.ObjectSet As Object
```



## <a name="property-value"></a><span data-ttu-id="7216f-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7216f-109">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="7216f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7216f-110">Remarks</span></span>

<span data-ttu-id="7216f-111">Diese Eigenschaft ist **null** , es sei denn, der Wert für " [**Swap. isset**](swbemrefreshableitem-isset.md) " ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="7216f-111">This property is **NULL** unless [**SWbemRefreshableItem.IsSet**](swbemrefreshableitem-isset.md) is **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7216f-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7216f-112">Requirements</span></span>



| <span data-ttu-id="7216f-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7216f-113">Requirement</span></span> | <span data-ttu-id="7216f-114">Wert</span><span class="sxs-lookup"><span data-stu-id="7216f-114">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7216f-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7216f-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7216f-116">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7216f-116">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7216f-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7216f-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7216f-118">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7216f-118">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7216f-119">Header</span><span class="sxs-lookup"><span data-stu-id="7216f-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7216f-120"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="7216f-120"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="7216f-121">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="7216f-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="7216f-122"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7216f-122"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7216f-123">DLL</span><span class="sxs-lookup"><span data-stu-id="7216f-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7216f-124"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7216f-124"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="7216f-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="7216f-125">CLSID</span></span><br/>                    | <span data-ttu-id="7216f-126">CLSID, \_ Swap-ableitem</span><span class="sxs-lookup"><span data-stu-id="7216f-126">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="7216f-127">IID</span><span class="sxs-lookup"><span data-stu-id="7216f-127">IID</span></span><br/>                      | <span data-ttu-id="7216f-128">IID \_ iswbemerfrischendes ableitem</span><span class="sxs-lookup"><span data-stu-id="7216f-128">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="7216f-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7216f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7216f-130">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="7216f-130">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="7216f-131">**Swap-aktuableitem**</span><span class="sxs-lookup"><span data-stu-id="7216f-131">**SWbemRefreshableItem**</span></span>](swbemrefresher.md)
</dt> </dl>

 

 




