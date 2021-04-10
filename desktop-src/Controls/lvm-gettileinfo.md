---
title: LVM_GETTILEINFO Meldung (kommstrg. h)
description: Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.
ms.assetid: e89a3eae-0970-488c-ba95-1072aa85bbf4
keywords:
- Windows-Steuerelemente für LVM_GETTILEINFO Meldung
topic_type:
- apiref
api_name:
- LVM_GETTILEINFO
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db5bfd085cd5cbaced0bf90b17e8862a6c0e159b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040887"
---
# <a name="lvm_gettileinfo-message"></a><span data-ttu-id="5d01d-104">LVM \_ gettileinfo-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5d01d-104">LVM\_GETTILEINFO message</span></span>

<span data-ttu-id="5d01d-105">Ruft Informationen zu einer Kachel in einem Listenansicht-Steuerelement ab.</span><span class="sxs-lookup"><span data-stu-id="5d01d-105">Retrieves information about a tile in a list-view control.</span></span>

## <a name="parameters"></a><span data-ttu-id="5d01d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d01d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d01d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5d01d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5d01d-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="5d01d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5d01d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5d01d-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5d01d-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**lvtileinfo**</a> -Struktur, die die abgerufenen Informationen empfängt.</span><span class="sxs-lookup"><span data-stu-id="5d01d-110">Pointer to an <a href="/windows/win32/api/commctrl/ns-commctrl-lvtileinfo">**LVTILEINFO**</a> structure that receives the retrieved information.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d01d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5d01d-111">Return value</span></span>

<span data-ttu-id="5d01d-112">Der Rückgabewert wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="5d01d-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d01d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5d01d-113">Remarks</span></span>

<span data-ttu-id="5d01d-114">Die Kachel Ansicht ist eine neue Methode zum Anordnen und Anzeigen von Elementen in einem Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="5d01d-114">Tile view is a new way of arranging and displaying items in a list-view control.</span></span> <span data-ttu-id="5d01d-115">Die anderen Ansichten sind Icon, Small Icon, Details und List.</span><span class="sxs-lookup"><span data-stu-id="5d01d-115">The other views are icon, small icon, details, and list.</span></span>

> [!Note]  
> <span data-ttu-id="5d01d-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="5d01d-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="5d01d-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5d01d-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5d01d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5d01d-118">Requirements</span></span>



| <span data-ttu-id="5d01d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5d01d-119">Requirement</span></span> | <span data-ttu-id="5d01d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="5d01d-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5d01d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5d01d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="5d01d-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d01d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5d01d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5d01d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="5d01d-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5d01d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5d01d-125">Header</span><span class="sxs-lookup"><span data-stu-id="5d01d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="5d01d-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="5d01d-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





