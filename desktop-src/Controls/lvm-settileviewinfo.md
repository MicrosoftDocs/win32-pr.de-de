---
title: LVM_SETTILEVIEWINFO Meldung (kommstrg. h)
description: Legt Informationen fest, die von einem Listenansicht-Steuerelement in der Kachel Ansicht verwendet werden.
ms.assetid: 1c4f2aff-1ce1-484a-9360-3efbe870b39b
keywords:
- Windows-Steuerelemente für LVM_SETTILEVIEWINFO Meldung
topic_type:
- apiref
api_name:
- LVM_SETTILEVIEWINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25d6c728d92bb931837eca440af679b5bcb98d1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103351"
---
# <a name="lvm_settileviewinfo-message"></a><span data-ttu-id="b0776-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="b0776-104">LVM\_SETTILEVIEWINFO message</span></span>

<span data-ttu-id="b0776-105">Legt Informationen fest, die von einem Listenansicht-Steuerelement in der Kachel Ansicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0776-105">Sets information that a list-view control uses in tile view.</span></span>

## <a name="parameters"></a><span data-ttu-id="b0776-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0776-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0776-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0776-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="b0776-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="b0776-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="b0776-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0776-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="b0776-110">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**lvtileviewinfo**</a> -Struktur, die die festzulegenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b0776-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileviewinfo">**LVTILEVIEWINFO**</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0776-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0776-111">Return value</span></span>

<span data-ttu-id="b0776-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="b0776-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0776-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0776-113">Remarks</span></span>

<span data-ttu-id="b0776-114">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="b0776-114">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="b0776-115">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b0776-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0776-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0776-116">Requirements</span></span>



| <span data-ttu-id="b0776-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b0776-117">Requirement</span></span> | <span data-ttu-id="b0776-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b0776-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b0776-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b0776-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0776-120">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0776-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b0776-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b0776-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0776-122">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b0776-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b0776-123">Header</span><span class="sxs-lookup"><span data-stu-id="b0776-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0776-124"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0776-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





