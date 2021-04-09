---
title: HDM_CREATEDRAGIMAGE Meldung (kommstrg. h)
description: Erstellt eine halbtransparente Version eines Element Bilds, das als Zieh Bild verwendet werden soll. Sie können diese Nachricht explizit senden oder das-Header-präffemage- \_ Makro verwenden.
ms.assetid: 1b9dc515-d327-4634-a424-cc15a32f0f7c
keywords:
- Windows-Steuerelemente für HDM_CREATEDRAGIMAGE Meldung
topic_type:
- apiref
api_name:
- HDM_CREATEDRAGIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9e801ad9771205b5f2e6df8e37bb0a0ad7f0bc6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040766"
---
# <a name="hdm_createdragimage-message"></a><span data-ttu-id="9986a-105">HDM- \_ Meldung "kreatedragimage"</span><span class="sxs-lookup"><span data-stu-id="9986a-105">HDM\_CREATEDRAGIMAGE message</span></span>

<span data-ttu-id="9986a-106">Erstellt eine halbtransparente Version eines Element Bilds, das als Zieh Bild verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9986a-106">Creates a semi-transparent version of an item's image for use as a dragging image.</span></span> <span data-ttu-id="9986a-107">Sie können diese Nachricht explizit senden oder das- [**Header \_**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) -präffemage-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="9986a-107">You can send this message explicitly or use the [**Header\_CreateDragImage**](/windows/desktop/api/Commctrl/nf-commctrl-header_createdragimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9986a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9986a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9986a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9986a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9986a-110">Der null basierte Index des Elements innerhalb des Header Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="9986a-110">The zero-based index of the item within the header control.</span></span> <span data-ttu-id="9986a-111">Das diesem Element zugewiesene Bild ist die Grundlage für das transparente Bild.</span><span class="sxs-lookup"><span data-stu-id="9986a-111">The image assigned to this item is the basis for the transparent image.</span></span>

</dd> <dt>

<span data-ttu-id="9986a-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9986a-112">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9986a-113">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9986a-113">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9986a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9986a-114">Return value</span></span>

<span data-ttu-id="9986a-115">Gibt ein Handle für eine Bildliste zurück, die das neue Bild als einziges Element enthält.</span><span class="sxs-lookup"><span data-stu-id="9986a-115">Returns a handle to an image list that contains the new image as its only element.</span></span>

## <a name="requirements"></a><span data-ttu-id="9986a-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9986a-116">Requirements</span></span>



| <span data-ttu-id="9986a-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9986a-117">Requirement</span></span> | <span data-ttu-id="9986a-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9986a-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9986a-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9986a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9986a-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9986a-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9986a-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9986a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9986a-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9986a-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9986a-123">Header</span><span class="sxs-lookup"><span data-stu-id="9986a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="9986a-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9986a-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





