---
title: LVM_GETCOUNTPERPAGE Meldung (kommstrg. h)
description: Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansicht-Steuer Elements passen, wenn Sie in der Listen-oder Berichtsansicht enthalten sind. Nur vollständig sichtbare Elemente werden gezählt. Sie können diese Nachricht explizit oder mithilfe des ListView \_ getzähltperpage-Makros senden.
ms.assetid: 2ffd2bb1-cddf-4a4a-a4a8-087c9dc3fec0
keywords:
- Windows-Steuerelemente für LVM_GETCOUNTPERPAGE Meldung
topic_type:
- apiref
api_name:
- LVM_GETCOUNTPERPAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734d460754f9ae8a11c3a42d8eacebf31d0b6fc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040106"
---
# <a name="lvm_getcountperpage-message"></a><span data-ttu-id="30f55-106">LVM \_ getgräfin-Nachricht</span><span class="sxs-lookup"><span data-stu-id="30f55-106">LVM\_GETCOUNTPERPAGE message</span></span>

<span data-ttu-id="30f55-107">Berechnet die Anzahl der Elemente, die vertikal in den sichtbaren Bereich eines Listenansicht-Steuer Elements passen, wenn Sie in der Listen-oder Berichtsansicht enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="30f55-107">Calculates the number of items that can fit vertically in the visible area of a list-view control when in list or report view.</span></span> <span data-ttu-id="30f55-108">Nur vollständig sichtbare Elemente werden gezählt.</span><span class="sxs-lookup"><span data-stu-id="30f55-108">Only fully visible items are counted.</span></span> <span data-ttu-id="30f55-109">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_ getzähltperpage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) -Makros senden.</span><span class="sxs-lookup"><span data-stu-id="30f55-109">You can send this message explicitly or by using the [**ListView\_GetCountPerPage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcountperpage) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="30f55-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="30f55-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30f55-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="30f55-111">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="30f55-112">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="30f55-112">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="30f55-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="30f55-113">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="30f55-114">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="30f55-114">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30f55-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30f55-115">Return value</span></span>

<span data-ttu-id="30f55-116">Gibt die Anzahl der vollständig sichtbaren Elemente zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="30f55-116">Returns the number of fully visible items if successful.</span></span> <span data-ttu-id="30f55-117">Wenn die aktuelle Ansicht eine Symbol-oder kleine Symbol Ansicht ist, ist der Rückgabewert die Gesamtzahl der Elemente im Listenansicht-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="30f55-117">If the current view is icon or small icon view, the return value is the total number of items in the list-view control.</span></span>

## <a name="requirements"></a><span data-ttu-id="30f55-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30f55-118">Requirements</span></span>



| <span data-ttu-id="30f55-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30f55-119">Requirement</span></span> | <span data-ttu-id="30f55-120">Wert</span><span class="sxs-lookup"><span data-stu-id="30f55-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="30f55-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30f55-121">Minimum supported client</span></span><br/> | <span data-ttu-id="30f55-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30f55-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="30f55-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30f55-123">Minimum supported server</span></span><br/> | <span data-ttu-id="30f55-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="30f55-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="30f55-125">Header</span><span class="sxs-lookup"><span data-stu-id="30f55-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="30f55-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="30f55-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





