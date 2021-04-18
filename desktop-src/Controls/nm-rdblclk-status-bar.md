---
title: NM_RDBLCLK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt die übergeordneten Fenster eines Status leisten-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 57d8c5a7-e179-4b65-a3aa-5566d5780c18
keywords:
- NM_RDBLCLK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18092b03a599c75a88deb56bb256d96728b96328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479419"
---
# <a name="nm_rdblclk-status-bar-notification-code"></a><span data-ttu-id="2d057-105">NM \_ rdblclk (Statusleiste) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="2d057-105">NM\_RDBLCLK (status bar) notification code</span></span>

<span data-ttu-id="2d057-106">Benachrichtigt die übergeordneten Fenster eines Status leisten-Steuer Elements, dass der Benutzer die Rechte Maustaste im Steuerelement doppelt geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="2d057-106">Notifies the parent windows of a status bar control that the user has double-clicked the right mouse button within the control.</span></span> <span data-ttu-id="2d057-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="2d057-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RDBLCLK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2d057-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="2d057-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2d057-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2d057-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2d057-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="2d057-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="2d057-111">Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="2d057-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2d057-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2d057-112">Return value</span></span>

<span data-ttu-id="2d057-113">Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System.</span><span class="sxs-lookup"><span data-stu-id="2d057-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="2d057-114">Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="2d057-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="2d057-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d057-115">Requirements</span></span>



| <span data-ttu-id="2d057-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d057-116">Requirement</span></span> | <span data-ttu-id="2d057-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2d057-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2d057-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2d057-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2d057-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d057-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2d057-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2d057-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2d057-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2d057-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2d057-122">Header</span><span class="sxs-lookup"><span data-stu-id="2d057-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2d057-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="2d057-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





