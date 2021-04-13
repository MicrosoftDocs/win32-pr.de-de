---
description: Beendet den aktuellen Codierungs Durchlauf oder fragt ab, ob der aktuelle Codierungs Durchlauf der letzte ist.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Avenccommonpassend-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482515"
---
# <a name="avenccommonpassend-property"></a><span data-ttu-id="7bb42-103">Avenccommonpassend (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7bb42-103">AVEncCommonPassEnd property</span></span>

<span data-ttu-id="7bb42-104">Beendet den aktuellen Codierungs Durchlauf oder fragt ab, ob der aktuelle Codierungs Durchlauf der letzte ist.</span><span class="sxs-lookup"><span data-stu-id="7bb42-104">Stops the current encoding pass, or queries whether the current encoding pass is the last one.</span></span>

<span data-ttu-id="7bb42-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7bb42-105">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="7bb42-106">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7bb42-106">Data type</span></span>

<span data-ttu-id="7bb42-107">**Variant \_ bool** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="7bb42-107">**VARIANT\_BOOL** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="7bb42-108">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="7bb42-108">Property GUID</span></span>

<span data-ttu-id="7bb42-109">**Codecapi \_ avenccommonpassend**</span><span class="sxs-lookup"><span data-stu-id="7bb42-109">**CODECAPI\_AVEncCommonPassEnd**</span></span>

## <a name="remarks"></a><span data-ttu-id="7bb42-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7bb42-110">Remarks</span></span>

<span data-ttu-id="7bb42-111">Wenn diese Eigenschaft auf **Variant \_ true** festgelegt wird, wird der aktuelle Codierungs Durchlauf beendet.</span><span class="sxs-lookup"><span data-stu-id="7bb42-111">Setting this property to **VARIANT\_TRUE** ends the current encoding pass.</span></span> <span data-ttu-id="7bb42-112">Wenn Sie diese Eigenschaft auf **Variant \_ false** festlegen, wird die Multipass-Codierung beendet</span><span class="sxs-lookup"><span data-stu-id="7bb42-112">Setting this property to **VARIANT\_FALSE** terminates multipass encoding.</span></span>

<span data-ttu-id="7bb42-113">Beim Lesen dieser Eigenschaft wird abgefragt, ob der aktuelle Codierungs Durchlauf der letzte ist.</span><span class="sxs-lookup"><span data-stu-id="7bb42-113">Reading this property queries whether the current encoding pass is the last one.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bb42-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bb42-114">Requirements</span></span>



| <span data-ttu-id="7bb42-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7bb42-115">Requirement</span></span> | <span data-ttu-id="7bb42-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7bb42-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7bb42-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7bb42-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7bb42-118">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb42-118">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="7bb42-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7bb42-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7bb42-120">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="7bb42-120">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="7bb42-121">Header</span><span class="sxs-lookup"><span data-stu-id="7bb42-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bb42-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bb42-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7bb42-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bb42-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bb42-124">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="7bb42-124">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="7bb42-125">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="7bb42-125">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




