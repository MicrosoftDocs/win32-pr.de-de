---
title: LVM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine Ziehbild Liste für das angegebene Element. Sie können diese Nachricht explizit oder mithilfe des ListView- \_ Makros "auflistungdragimage" senden.
ms.assetid: face4c8f-01ff-4f5a-a468-e306a50dae35
keywords:
- Windows-Steuerelemente für LVM_CREATEDRAGIMAGE Meldung
topic_type:
- apiref
api_name:
- LVM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ace975b178fee85e2794b518a78b40b375c65ae7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102906"
---
# <a name="lvm_createdragimage-message"></a><span data-ttu-id="76d0d-105">LVM-Nachricht für " \_ kreatedragimage"</span><span class="sxs-lookup"><span data-stu-id="76d0d-105">LVM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="76d0d-106">Erstellt eine Ziehbild Liste für das angegebene Element.</span><span class="sxs-lookup"><span data-stu-id="76d0d-106">Creates a drag image list for the specified item.</span></span> <span data-ttu-id="76d0d-107">Sie können diese Nachricht explizit oder mithilfe des ListView-Makros " [**auflistungdragimage \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) " senden.</span><span class="sxs-lookup"><span data-stu-id="76d0d-107">You can send this message explicitly or by using the [**ListView\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="76d0d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="76d0d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76d0d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="76d0d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d0d-110">Der Index des Elements.</span><span class="sxs-lookup"><span data-stu-id="76d0d-110">The index of the item.</span></span>

</dd> <dt>

<span data-ttu-id="76d0d-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="76d0d-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="76d0d-112">Ein Zeiger auf eine [**Punkt**](/previous-versions//dd162805(v=vs.85)) Struktur, die die ursprüngliche Position der oberen linken Ecke des Bilds in Ansichts Koordinaten empfängt.</span><span class="sxs-lookup"><span data-stu-id="76d0d-112">A pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that receives the initial location of the upper-left corner of the image, in view coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76d0d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76d0d-113">Return value</span></span>

<span data-ttu-id="76d0d-114">Gibt das Handle für die Drag-Bildliste zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="76d0d-114">Returns the handle to the drag image list if successful, or **NULL** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="76d0d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76d0d-115">Remarks</span></span>

<span data-ttu-id="76d0d-116">Die Anwendung ist dafür verantwortlich, die Bildliste zu zerstören, wenn Sie nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="76d0d-116">Your application is responsible for destroying the image list when it is no longer needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="76d0d-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76d0d-117">Requirements</span></span>



| <span data-ttu-id="76d0d-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76d0d-118">Requirement</span></span> | <span data-ttu-id="76d0d-119">Wert</span><span class="sxs-lookup"><span data-stu-id="76d0d-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76d0d-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76d0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="76d0d-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76d0d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="76d0d-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76d0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="76d0d-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76d0d-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="76d0d-124">Header</span><span class="sxs-lookup"><span data-stu-id="76d0d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="76d0d-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="76d0d-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

