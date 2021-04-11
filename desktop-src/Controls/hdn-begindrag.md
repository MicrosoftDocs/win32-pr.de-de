---
title: HDN_BEGINDRAG Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang für eines der Elemente begonnen hat. Dieser Benachrichtigungs Code wird nur von Header Steuerelementen gesendet, die auf den HDS DragDrop-Stil festgelegt sind \_ . Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3dfb7a7c-d783-48e0-ba92-8144104f163a
keywords:
- Windows-Steuerelemente für HDN_BEGINDRAG Benachrichtigungs
topic_type:
- apiref
api_name:
- HDN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed6b4af8e662a8a9891e9a81535de987337567f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040540"
---
# <a name="hdn_begindrag-notification-code"></a><span data-ttu-id="978fb-106">\_Benachrichtigungs Code für Hdn BeginDrag</span><span class="sxs-lookup"><span data-stu-id="978fb-106">HDN\_BEGINDRAG notification code</span></span>

<span data-ttu-id="978fb-107">Wird von einem Header-Steuerelement gesendet, wenn ein Zieh Vorgang für eines der Elemente begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="978fb-107">Sent by a header control when a drag operation has begun on one of its items.</span></span> <span data-ttu-id="978fb-108">Dieser Benachrichtigungs Code wird nur von Header Steuerelementen gesendet, die auf den [**HDS \_ DragDrop**](header-control-styles.md) -Stil festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="978fb-108">This notification code is sent only by header controls that are set to the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="978fb-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="978fb-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
HDN_BEGINDRAG

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a><span data-ttu-id="978fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="978fb-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978fb-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="978fb-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="978fb-112">Ein Zeiger auf eine [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) -Struktur, die Informationen über das Header Element enthält, das gezogen wird.</span><span class="sxs-lookup"><span data-stu-id="978fb-112">A pointer to an [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) structure containing information about the header item that is being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978fb-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="978fb-113">Return value</span></span>

<span data-ttu-id="978fb-114">Um dem Header Steuerelement das automatische Verwalten von Drag & Drop-Vorgängen zu ermöglichen, wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="978fb-114">To allow the header control to automatically manage drag-and-drop operations, return **FALSE**.</span></span> <span data-ttu-id="978fb-115">Wenn der Besitzer des Steuer Elements die Neuanordnung per Drag & Drop manuell ausführt, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="978fb-115">If the owner of the control is manually performing drag-and-drop reordering, return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="978fb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="978fb-116">Remarks</span></span>

<span data-ttu-id="978fb-117">Ein Header Steuerelement verwendet standardmäßig die automatische Verwaltung der Drag & Drop-Neuanordnung.</span><span class="sxs-lookup"><span data-stu-id="978fb-117">A header control defaults to automatically managing drag-and-drop reordering.</span></span> <span data-ttu-id="978fb-118">Wenn " **true** " zurückgegeben wird, um die externe (manuelle) Drag & Drop-Verwaltung anzugeben, kann der Besitzer des Steuer Elements benutzerdefinierte Dienste als Teil des Drag & Drop-Prozesses bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="978fb-118">Returning **TRUE** to indicate external (manual) drag-and-drop management allows the owner of the control to provide custom services as part of the drag-and-drop process.</span></span>

## <a name="requirements"></a><span data-ttu-id="978fb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="978fb-119">Requirements</span></span>



| <span data-ttu-id="978fb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="978fb-120">Requirement</span></span> | <span data-ttu-id="978fb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="978fb-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="978fb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="978fb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="978fb-123">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="978fb-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="978fb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="978fb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="978fb-125">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="978fb-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="978fb-126">Header</span><span class="sxs-lookup"><span data-stu-id="978fb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="978fb-127"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="978fb-127"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





