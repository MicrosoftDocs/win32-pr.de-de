---
title: HDM_DELETEITEM Meldung (kommstrg. h)
description: Löscht ein Element aus einem Header-Steuerelement. Sie können diese Nachricht explizit senden oder das-Header \_ DeleteItem-Makro verwenden.
ms.assetid: 1dd1f233-2812-41ae-8a36-c42b9ac70ffc
keywords:
- Windows-Steuerelemente für HDM_DELETEITEM Meldung
topic_type:
- apiref
api_name:
- HDM_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a3ec4b48c3dcc77579f70d26cd55b7127f5a6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040765"
---
# <a name="hdm_deleteitem-message"></a><span data-ttu-id="65c8a-105">HDM \_ DeleteItem-Meldung</span><span class="sxs-lookup"><span data-stu-id="65c8a-105">HDM\_DELETEITEM message</span></span>

<span data-ttu-id="65c8a-106">Löscht ein Element aus einem Header-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="65c8a-106">Deletes an item from a header control.</span></span> <span data-ttu-id="65c8a-107">Sie können diese Nachricht explizit senden oder das- [**Header \_ DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="65c8a-107">You can send this message explicitly or use the [**Header\_DeleteItem**](/windows/desktop/api/Commctrl/nf-commctrl-header_deleteitem) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="65c8a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="65c8a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65c8a-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="65c8a-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="65c8a-110">Ein Index des zu löschenden Elements.</span><span class="sxs-lookup"><span data-stu-id="65c8a-110">An index of the item to delete.</span></span>

</dd> <dt>

<span data-ttu-id="65c8a-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="65c8a-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="65c8a-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="65c8a-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65c8a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="65c8a-113">Return value</span></span>

<span data-ttu-id="65c8a-114">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="65c8a-114">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="65c8a-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="65c8a-115">Requirements</span></span>



| <span data-ttu-id="65c8a-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="65c8a-116">Requirement</span></span> | <span data-ttu-id="65c8a-117">Wert</span><span class="sxs-lookup"><span data-stu-id="65c8a-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="65c8a-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="65c8a-118">Minimum supported client</span></span><br/> | <span data-ttu-id="65c8a-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65c8a-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="65c8a-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="65c8a-120">Minimum supported server</span></span><br/> | <span data-ttu-id="65c8a-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="65c8a-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="65c8a-122">Header</span><span class="sxs-lookup"><span data-stu-id="65c8a-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="65c8a-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="65c8a-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





