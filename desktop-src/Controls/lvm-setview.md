---
title: LVM_SETVIEW Meldung (kommstrg. h)
description: Legt die Ansicht eines Listenansicht-Steuer Elements fest.
ms.assetid: e6d3f16d-52ea-4863-a6c9-9a085d5f794a
keywords:
- Windows-Steuerelemente für LVM_SETVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_SETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a159710b3086bcba5298a5a88f9cab15f76e0d89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105464"
---
# <a name="lvm_setview-message"></a><span data-ttu-id="9d5a3-104">LVM- \_ Setview-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9d5a3-104">LVM\_SETVIEW message</span></span>

<span data-ttu-id="9d5a3-105">Legt die Ansicht eines Listenansicht-Steuer Elements fest.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-105">Sets the view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="9d5a3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d5a3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d5a3-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9d5a3-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9d5a3-108">**DWORD** , das die Ansicht angibt.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-108">**DWORD** that specifies the view.</span></span></dd> <dt>

<span data-ttu-id="9d5a3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d5a3-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9d5a3-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d5a3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9d5a3-111">Return value</span></span>

<span data-ttu-id="9d5a3-112">Gibt 1 zurück, wenn erfolgreich, andernfalls-1.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-112">Returns 1 if successful, or -1 otherwise.</span></span> <span data-ttu-id="9d5a3-113">Beispielsweise wird-1 zurückgegeben, wenn die Sicht ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-113">For example, -1 is returned if the view is invalid.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d5a3-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d5a3-114">Remarks</span></span>

<span data-ttu-id="9d5a3-115">Im folgenden werden die Werte für Sichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-115">Following are the values for views.</span></span>

-   <span data-ttu-id="9d5a3-116">Details der LV- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="9d5a3-116">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="9d5a3-117">Symbol für LV- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="9d5a3-117">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="9d5a3-118">LV- \_ Ansichts \_ Liste</span><span class="sxs-lookup"><span data-stu-id="9d5a3-118">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="9d5a3-119">LV- \_ Ansicht \_ SmallIcon</span><span class="sxs-lookup"><span data-stu-id="9d5a3-119">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="9d5a3-120">LV- \_ Ansichts \_ Kachel</span><span class="sxs-lookup"><span data-stu-id="9d5a3-120">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="9d5a3-121">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comctl32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="9d5a3-121">To use this message, you must provide a manifest specifying Comctl32.dll version 6.0.</span></span> <span data-ttu-id="9d5a3-122">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9d5a3-122">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="9d5a3-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d5a3-123">Requirements</span></span>



| <span data-ttu-id="9d5a3-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d5a3-124">Requirement</span></span> | <span data-ttu-id="9d5a3-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9d5a3-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d5a3-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d5a3-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9d5a3-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d5a3-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d5a3-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d5a3-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9d5a3-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d5a3-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d5a3-130">Header</span><span class="sxs-lookup"><span data-stu-id="9d5a3-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d5a3-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d5a3-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





