---
title: LVM_INSERTMARKHITTEST Meldung (kommstrg. h)
description: Ruft die Einfügemarke ab, die einem angegebenen Punkt am nächsten ist.
ms.assetid: 901bb770-a36d-4d9f-a53b-d497b4df39e5
keywords:
- Windows-Steuerelemente für LVM_INSERTMARKHITTEST Meldung
topic_type:
- apiref
api_name:
- LVM_INSERTMARKHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bdb82e924b4a5d74d152917f52c4039e0aca81b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105477"
---
# <a name="lvm_insertmarkhittest-message"></a><span data-ttu-id="43632-104">LVM \_ insertmarkhittest-Meldung</span><span class="sxs-lookup"><span data-stu-id="43632-104">LVM\_INSERTMARKHITTEST message</span></span>

<span data-ttu-id="43632-105">Ruft die Einfügemarke ab, die einem angegebenen Punkt am nächsten ist.</span><span class="sxs-lookup"><span data-stu-id="43632-105">Retrieves the insertion point closest to a specified point.</span></span>

## <a name="parameters"></a><span data-ttu-id="43632-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="43632-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43632-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="43632-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="43632-108">Zeiger auf eine **Punkt** Struktur, die die Treffer Test Koordinaten enthält.</span><span class="sxs-lookup"><span data-stu-id="43632-108">Pointer to a **POINT** structure that contains the hit test coordinates.</span></span></dd> <dt>

<span data-ttu-id="43632-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="43632-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="43632-110">Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die die Einfügemarke angibt, die den durch den *wParam* -Parameter definierten Koordinaten am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="43632-110">Pointer to an <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies the insertion point closest to the coordinates defined by the *wParam* parameter.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43632-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="43632-111">Return value</span></span>

<span data-ttu-id="43632-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="43632-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="43632-113">**False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht oder wenn in der aktuellen Ansicht keine Einfügemarke angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="43632-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="43632-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43632-114">Remarks</span></span>

<span data-ttu-id="43632-115">Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbol Ansicht, in der kleinen Symbol Ansicht oder in der Kachel Ansicht befindet und sich nicht im gruppenansichts Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="43632-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view and is not in group-view mode.</span></span>

<span data-ttu-id="43632-116">Wenn für die Ansicht keine Einfügepunkte gelten, enthält die [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur im **iItem** -Member den Eintrag-1.</span><span class="sxs-lookup"><span data-stu-id="43632-116">If insertion points do not apply for the view, the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure contains a -1 in the **iItem** member.</span></span>

> [!Note]  
> <span data-ttu-id="43632-117">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="43632-117">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="43632-118">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="43632-118">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="43632-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43632-119">Requirements</span></span>



| <span data-ttu-id="43632-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43632-120">Requirement</span></span> | <span data-ttu-id="43632-121">Wert</span><span class="sxs-lookup"><span data-stu-id="43632-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="43632-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43632-122">Minimum supported client</span></span><br/> | <span data-ttu-id="43632-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43632-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="43632-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43632-124">Minimum supported server</span></span><br/> | <span data-ttu-id="43632-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43632-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="43632-126">Header</span><span class="sxs-lookup"><span data-stu-id="43632-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="43632-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="43632-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





