---
title: PGM_SETCHILD Meldung (kommstrg. h)
description: Legt das enthaltene Fenster für das Pager-Steuerelement fest.
ms.assetid: 717e6720-aa42-4ecd-9520-4618a04dc28d
keywords:
- Windows-Steuerelemente für PGM_SETCHILD Meldung
topic_type:
- apiref
api_name:
- PGM_SETCHILD
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c934c3c5688ac79b5c5ce67aef68e28ad3627ce
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103475"
---
# <a name="pgm_setchild-message"></a><span data-ttu-id="3c7b9-104">PGM- \_ setchild-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3c7b9-104">PGM\_SETCHILD message</span></span>

<span data-ttu-id="3c7b9-105">Legt das enthaltene Fenster für das Pager-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-105">Sets the contained window for the pager control.</span></span> <span data-ttu-id="3c7b9-106">Mit dieser Meldung wird das übergeordnete Element des enthaltenen Fensters nicht geändert. dem Pager-Steuerelement wird nur ein Fenster Handle für den Bildlauf zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-106">This message will not change the parent of the contained window; it only assigns a window handle to the pager control for scrolling.</span></span> <span data-ttu-id="3c7b9-107">In den meisten Fällen ist das enthaltene Fenster ein untergeordnetes Fenster.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-107">In most cases, the contained window will be a child window.</span></span> <span data-ttu-id="3c7b9-108">Wenn dies der Fall ist, sollte das enthaltene Fenster dem Pager-Steuerelement untergeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-108">If this is the case, the contained window should be a child of the pager control.</span></span> <span data-ttu-id="3c7b9-109">Sie können diese Nachricht explizit senden oder das [**Pager-Element \_ setchild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-109">You can send this message explicitly or use the [**Pager\_SetChild**](/windows/desktop/api/Commctrl/nf-commctrl-pager_setchild) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="3c7b9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c7b9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c7b9-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3c7b9-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3c7b9-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3c7b9-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3c7b9-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3c7b9-114">Handle für das Fenster, das enthalten sein soll.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-114">Handle to the window to be contained.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c7b9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3c7b9-115">Return value</span></span>

<span data-ttu-id="3c7b9-116">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c7b9-116">The return value is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c7b9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3c7b9-117">Requirements</span></span>



| <span data-ttu-id="3c7b9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3c7b9-118">Requirement</span></span> | <span data-ttu-id="3c7b9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="3c7b9-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c7b9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3c7b9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c7b9-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c7b9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3c7b9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3c7b9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c7b9-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3c7b9-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c7b9-124">Header</span><span class="sxs-lookup"><span data-stu-id="3c7b9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c7b9-125"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c7b9-125"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





