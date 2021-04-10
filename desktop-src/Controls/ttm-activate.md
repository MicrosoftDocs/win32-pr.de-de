---
title: TTM_ACTIVATE Meldung (kommstrg. h)
description: Aktiviert oder deaktiviert ein QuickInfo-Steuerelement.
ms.assetid: f37da001-748c-4c51-bb32-dc49031ff2fb
keywords:
- Windows-Steuerelemente für TTM_ACTIVATE Meldung
topic_type:
- apiref
api_name:
- TTM_ACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e200b769cd3d9e07cb63a5a540960bcc707f862d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040628"
---
# <a name="ttm_activate-message"></a><span data-ttu-id="2f8ef-104">TTM- \_ Aktivierungs Nachricht</span><span class="sxs-lookup"><span data-stu-id="2f8ef-104">TTM\_ACTIVATE message</span></span>

<span data-ttu-id="2f8ef-105">Aktiviert oder deaktiviert ein QuickInfo-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-105">Activates or deactivates a tooltip control.</span></span>

## <a name="parameters"></a><span data-ttu-id="2f8ef-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f8ef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f8ef-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f8ef-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f8ef-108">Aktivierungs Kennzeichen.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-108">Activation flag.</span></span> <span data-ttu-id="2f8ef-109">Wenn dieser Parameter **true** ist, wird das QuickInfo-Steuerelement aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-109">If this parameter is **TRUE**, the tooltip control is activated.</span></span> <span data-ttu-id="2f8ef-110">Wenn der Wert **false** ist, wird das QuickInfo-Steuerelement deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-110">If it is **FALSE**, the tooltip control is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="2f8ef-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f8ef-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="2f8ef-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f8ef-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f8ef-113">Return value</span></span>

<span data-ttu-id="2f8ef-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="2f8ef-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f8ef-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f8ef-115">Requirements</span></span>



| <span data-ttu-id="2f8ef-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f8ef-116">Requirement</span></span> | <span data-ttu-id="2f8ef-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2f8ef-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2f8ef-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f8ef-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2f8ef-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f8ef-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2f8ef-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f8ef-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2f8ef-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f8ef-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2f8ef-122">Header</span><span class="sxs-lookup"><span data-stu-id="2f8ef-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f8ef-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f8ef-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





