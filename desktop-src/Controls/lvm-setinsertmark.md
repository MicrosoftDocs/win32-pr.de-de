---
title: LVM_SETINSERTMARK Meldung (kommstrg. h)
description: Legt die Einfügemarke auf die definierte Position fest.
ms.assetid: 32cf5a11-918a-4dc4-bf10-88b3c26f26cc
keywords:
- Windows-Steuerelemente für LVM_SETINSERTMARK Meldung
topic_type:
- apiref
api_name:
- LVM_SETINSERTMARK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dab80b1b73b620ce94b75aecab90f6bdd69bf228
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102883"
---
# <a name="lvm_setinsertmark-message"></a><span data-ttu-id="8fbf6-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="8fbf6-104">LVM\_SETINSERTMARK message</span></span>

<span data-ttu-id="8fbf6-105">Legt die Einfügemarke auf die definierte Position fest.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-105">Sets the insertion point to the defined position.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fbf6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fbf6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fbf6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8fbf6-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="8fbf6-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="8fbf6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8fbf6-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="8fbf6-110">Ein Zeiger auf eine <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">lvinsertmark</a> -Struktur, die angibt, wo die Einfügemarke festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-110">Pointer to a <a href="/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark">LVINSERTMARK</a> structure that specifies where to set the insertion point.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fbf6-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8fbf6-111">Return value</span></span>

<span data-ttu-id="8fbf6-112">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8fbf6-112">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span> <span data-ttu-id="8fbf6-113">**False** wird zurückgegeben, wenn die Größe im **CBSIZE** -Member der [**lvinsertmark**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) -Struktur nicht der tatsächlichen Größe der Struktur entspricht oder wenn in der aktuellen Ansicht keine Einfügemarke angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-113">**FALSE** is returned if the size in the **cbSize** member of the [**LVINSERTMARK**](/windows/desktop/api/Commctrl/ns-commctrl-lvinsertmark) structure does not equal the actual size of the structure, or when an insertion point does not apply in the current view.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fbf6-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fbf6-114">Remarks</span></span>

<span data-ttu-id="8fbf6-115">Eine Einfügemarke kann nur angezeigt werden, wenn sich das Listenansicht-Steuerelement in der Symbol Ansicht, in der kleinen Symbol Ansicht oder in der Kachel Ansicht befindet und sich nicht im gruppenansichts Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-115">An insertion point can only appear if the list-view control is in icon view, small icon view, or tile view, and is not in group-view mode.</span></span>

> [!Note]  
> <span data-ttu-id="8fbf6-116">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="8fbf6-116">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="8fbf6-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8fbf6-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="8fbf6-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8fbf6-118">Requirements</span></span>



| <span data-ttu-id="8fbf6-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8fbf6-119">Requirement</span></span> | <span data-ttu-id="8fbf6-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8fbf6-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8fbf6-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8fbf6-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8fbf6-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fbf6-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8fbf6-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8fbf6-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8fbf6-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8fbf6-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8fbf6-125">Header</span><span class="sxs-lookup"><span data-stu-id="8fbf6-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8fbf6-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="8fbf6-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





