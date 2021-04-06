---
title: TCM_GETIMAGELIST Meldung (kommstrg. h)
description: Ruft die einem Registerkarten-Steuerelement zugeordnete Bildliste ab. Sie können diese Nachricht explizit oder mit dem tabstrg \_ GetImageList-Makro senden.
ms.assetid: 86a0d8c7-ff3d-4e16-994e-4c72d1e62e9f
keywords:
- Windows-Steuerelemente für TCM_GETIMAGELIST Meldung
topic_type:
- apiref
api_name:
- TCM_GETIMAGELIST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c4d471ef4d072e4305507f4f5ebc4a8f2745ed9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859199"
---
# <a name="tcm_getimagelist-message"></a><span data-ttu-id="bad30-105">TCM \_ GetImageList-Meldung</span><span class="sxs-lookup"><span data-stu-id="bad30-105">TCM\_GETIMAGELIST message</span></span>

<span data-ttu-id="bad30-106">Ruft die einem Registerkarten-Steuerelement zugeordnete Bildliste ab.</span><span class="sxs-lookup"><span data-stu-id="bad30-106">Retrieves the image list associated with a tab control.</span></span> <span data-ttu-id="bad30-107">Sie können diese Nachricht explizit oder mit dem [**tabstrg \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) -Makro senden.</span><span class="sxs-lookup"><span data-stu-id="bad30-107">You can send this message explicitly or by using the [**TabCtrl\_GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getimagelist) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="bad30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bad30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bad30-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bad30-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="bad30-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bad30-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="bad30-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bad30-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="bad30-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="bad30-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bad30-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bad30-113">Return value</span></span>

<span data-ttu-id="bad30-114">Gibt das Handle für die Bildliste zurück, wenn erfolgreich, andernfalls **null** .</span><span class="sxs-lookup"><span data-stu-id="bad30-114">Returns the handle to the image list if successful, or **NULL** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad30-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bad30-115">Requirements</span></span>



| <span data-ttu-id="bad30-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bad30-116">Requirement</span></span> | <span data-ttu-id="bad30-117">Wert</span><span class="sxs-lookup"><span data-stu-id="bad30-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="bad30-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bad30-118">Minimum supported client</span></span><br/> | <span data-ttu-id="bad30-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bad30-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="bad30-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bad30-120">Minimum supported server</span></span><br/> | <span data-ttu-id="bad30-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bad30-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="bad30-122">Header</span><span class="sxs-lookup"><span data-stu-id="bad30-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="bad30-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="bad30-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





