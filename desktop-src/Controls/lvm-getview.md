---
title: LVM_GETVIEW Meldung (kommstrg. h)
description: Ruft die aktuelle Ansicht eines Listenansicht-Steuer Elements ab.
ms.assetid: dd63e726-3a7f-40e7-8d46-4680816c02a3
keywords:
- Windows-Steuerelemente für LVM_GETVIEW Meldung
topic_type:
- apiref
api_name:
- LVM_GETVIEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2da295fa5a5b335de60169ce06b777d9e355121
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105483"
---
# <a name="lvm_getview-message"></a><span data-ttu-id="4f2c0-104">LVM \_ GetView-Nachricht</span><span class="sxs-lookup"><span data-stu-id="4f2c0-104">LVM\_GETVIEW message</span></span>

<span data-ttu-id="4f2c0-105">Ruft die aktuelle Ansicht eines Listenansicht-Steuer Elements ab.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-105">Retrieves the current view of a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="4f2c0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f2c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f2c0-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="4f2c0-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="4f2c0-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="4f2c0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4f2c0-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="4f2c0-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f2c0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f2c0-111">Return value</span></span>

<span data-ttu-id="4f2c0-112">Gibt ein **DWORD** zurück, das die aktuelle Ansicht angibt.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-112">Returns a **DWORD** that specifies the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f2c0-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f2c0-113">Remarks</span></span>

<span data-ttu-id="4f2c0-114">Im folgenden werden die Werte für Sichten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-114">Following are the values for views.</span></span>

-   <span data-ttu-id="4f2c0-115">Details der LV- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="4f2c0-115">LV\_VIEW\_DETAILS</span></span>
-   <span data-ttu-id="4f2c0-116">Symbol für LV- \_ Ansicht \_</span><span class="sxs-lookup"><span data-stu-id="4f2c0-116">LV\_VIEW\_ICON</span></span>
-   <span data-ttu-id="4f2c0-117">LV- \_ Ansichts \_ Liste</span><span class="sxs-lookup"><span data-stu-id="4f2c0-117">LV\_VIEW\_LIST</span></span>
-   <span data-ttu-id="4f2c0-118">LV- \_ Ansicht \_ SmallIcon</span><span class="sxs-lookup"><span data-stu-id="4f2c0-118">LV\_VIEW\_SMALLICON</span></span>
-   <span data-ttu-id="4f2c0-119">LV- \_ Ansichts \_ Kachel</span><span class="sxs-lookup"><span data-stu-id="4f2c0-119">LV\_VIEW\_TILE</span></span>

> [!Note]  
> <span data-ttu-id="4f2c0-120">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="4f2c0-120">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="4f2c0-121">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4f2c0-121">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="4f2c0-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f2c0-122">Requirements</span></span>



| <span data-ttu-id="4f2c0-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f2c0-123">Requirement</span></span> | <span data-ttu-id="4f2c0-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4f2c0-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4f2c0-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4f2c0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="4f2c0-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f2c0-126">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="4f2c0-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4f2c0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="4f2c0-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4f2c0-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4f2c0-129">Header</span><span class="sxs-lookup"><span data-stu-id="4f2c0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="4f2c0-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="4f2c0-130"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





