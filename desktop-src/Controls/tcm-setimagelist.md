---
title: TCM_SETIMAGELIST Meldung (kommstrg. h)
description: Weist einem Registerkarten-Steuerelement eine Bildliste zu. Sie können diese Nachricht explizit oder mithilfe des tabstrg \_ SetImageList-Makros senden.
ms.assetid: b457c73c-4c38-4bc5-af5d-12bbd24504a6
keywords:
- Windows-Steuerelemente für TCM_SETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TCM_SETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 59172c677998e816b295939c14effe45ff8aa961
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040086"
---
# <a name="tcm_setimagelist-message"></a><span data-ttu-id="4253f-105">TCM \_ SetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="4253f-105">TCM\_SETIMAGELIST message</span></span>

<span data-ttu-id="4253f-106">Weist einem Registerkarten-Steuerelement eine Bildliste zu.</span><span class="sxs-lookup"><span data-stu-id="4253f-106">Assigns an image list to a tab control.</span></span> <span data-ttu-id="4253f-107">Sie können diese Nachricht explizit oder mithilfe des [**tabstrg \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="4253f-107">You can send this message explicitly or by using the [**TabCtrl\_SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_setimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="4253f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4253f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4253f-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4253f-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4253f-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4253f-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4253f-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4253f-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4253f-112">Handle für die Bildliste, die dem Registerkarten-Steuerelement zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4253f-112">Handle to the image list to assign to the tab control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4253f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4253f-113">Return value</span></span>

<span data-ttu-id="4253f-114">Gibt das Handle für die vorherige Bildliste zurück, oder **null** , wenn keine vorherige Bildliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="4253f-114">Returns the handle to the previous image list, or **NULL** if there is no previous image list.</span></span>

## <a name="requirements"></a><span data-ttu-id="4253f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4253f-115">Requirements</span></span>



| <span data-ttu-id="4253f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4253f-116">Requirement</span></span> | <span data-ttu-id="4253f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="4253f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4253f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4253f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4253f-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4253f-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4253f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4253f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4253f-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4253f-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4253f-122">Header</span><span class="sxs-lookup"><span data-stu-id="4253f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="4253f-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4253f-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





