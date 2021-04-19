---
title: TCM_REMOVEIMAGE Meldung (kommstrg. h)
description: Entfernt ein Bild aus der Bildliste eines Registerkarten-Steuer Elements. Sie können diese Nachricht explizit oder mithilfe des tabctrl \_ removeimage-Makros senden.
ms.assetid: f2761338-0afa-47d8-9d9c-1d5a4a7f7bcf
keywords:
- Windows-Steuerelemente für TCM_REMOVEIMAGE Meldung
topic_type:
- apiref
api_name:
- TCM_REMOVEIMAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cbc51aa0efed847e39e735443c0d42e288bbaab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346335"
---
# <a name="tcm_removeimage-message"></a><span data-ttu-id="b7d7c-105">TCM \_ removeimage-Nachricht</span><span class="sxs-lookup"><span data-stu-id="b7d7c-105">TCM\_REMOVEIMAGE message</span></span>

<span data-ttu-id="b7d7c-106">Entfernt ein Bild aus der Bildliste eines Registerkarten-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-106">Removes an image from a tab control's image list.</span></span> <span data-ttu-id="b7d7c-107">Sie können diese Nachricht explizit oder mithilfe des [**tabctrl \_ removeimage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-107">You can send this message explicitly or by using the [**TabCtrl\_RemoveImage**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_removeimage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="b7d7c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b7d7c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7d7c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b7d7c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b7d7c-110">Der Index des zu entfernenden Bilds.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-110">Index of the image to remove.</span></span>

</dd> <dt>

<span data-ttu-id="b7d7c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b7d7c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b7d7c-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7d7c-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b7d7c-113">Return value</span></span>

<span data-ttu-id="b7d7c-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7d7c-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7d7c-115">Remarks</span></span>

<span data-ttu-id="b7d7c-116">Das Registerkarten-Steuerelement aktualisiert den Bildindex jeder Registerkarte, sodass jede Registerkarte dem gleichen Bild wie zuvor zugeordnet bleibt.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-116">The tab control updates each tab's image index, so each tab remains associated with the same image as before.</span></span> <span data-ttu-id="b7d7c-117">Wenn eine Registerkarte das zu entfernende Bild verwendet, wird die Registerkarte so festgelegt, dass Sie kein Bild hat.</span><span class="sxs-lookup"><span data-stu-id="b7d7c-117">If a tab is using the image being removed, the tab will be set to have no image.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d7c-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7d7c-118">Requirements</span></span>



| <span data-ttu-id="b7d7c-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d7c-119">Requirement</span></span> | <span data-ttu-id="b7d7c-120">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d7c-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d7c-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b7d7c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d7c-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d7c-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b7d7c-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b7d7c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d7c-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b7d7c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b7d7c-125">Header</span><span class="sxs-lookup"><span data-stu-id="b7d7c-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b7d7c-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b7d7c-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





