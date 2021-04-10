---
title: TBM_GETTOOLTIPS Meldung (kommstrg. h)
description: Ruft das Handle für das QuickInfo-Steuerelement ab, das der TrackBar zugewiesen ist, sofern vorhanden.
ms.assetid: 30efef12-1aec-4635-94a7-1843db404c4f
keywords:
- Windows-Steuerelemente für TBM_GETTOOLTIPS Meldung
topic_type:
- apiref
api_name:
- TBM_GETTOOLTIPS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02b0b757b1aabfef2c9df2e80ca9f96542ba4a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858908"
---
# <a name="tbm_gettooltips-message"></a><span data-ttu-id="eab01-104">TBM \_ gettooltips-Meldung</span><span class="sxs-lookup"><span data-stu-id="eab01-104">TBM\_GETTOOLTIPS message</span></span>

<span data-ttu-id="eab01-105">Ruft das Handle für das QuickInfo-Steuerelement ab, das der TrackBar zugewiesen ist, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="eab01-105">Retrieves the handle to the tooltip control assigned to the trackbar, if any.</span></span>

## <a name="parameters"></a><span data-ttu-id="eab01-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="eab01-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eab01-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="eab01-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="eab01-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="eab01-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="eab01-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="eab01-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="eab01-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="eab01-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eab01-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eab01-111">Return value</span></span>

<span data-ttu-id="eab01-112">Gibt das Handle für das QuickInfo-Steuerelement zurück, das der TrackBar zugewiesen ist, oder **null** , wenn Quick Infos nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eab01-112">Returns the handle to the tooltip control assigned to the trackbar, or **NULL** if tooltips are not in use.</span></span> <span data-ttu-id="eab01-113">Wenn das TrackBar-Steuerelement den [**TSB- \_ Tooltips**](trackbar-control-styles.md) -Stil nicht verwendet, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="eab01-113">If the trackbar control does not use the [**TBS\_TOOLTIPS**](trackbar-control-styles.md) style, the return value is **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="eab01-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eab01-114">Requirements</span></span>



| <span data-ttu-id="eab01-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eab01-115">Requirement</span></span> | <span data-ttu-id="eab01-116">Wert</span><span class="sxs-lookup"><span data-stu-id="eab01-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eab01-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eab01-117">Minimum supported client</span></span><br/> | <span data-ttu-id="eab01-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eab01-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="eab01-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eab01-119">Minimum supported server</span></span><br/> | <span data-ttu-id="eab01-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eab01-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="eab01-121">Header</span><span class="sxs-lookup"><span data-stu-id="eab01-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="eab01-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="eab01-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





