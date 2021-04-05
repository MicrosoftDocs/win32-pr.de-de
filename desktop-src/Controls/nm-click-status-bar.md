---
title: NM_CLICK (Statusleiste) Benachrichtigungs Code (kommstrg. h)
description: Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 179ccbe9-f51f-4356-b91a-10d7e3607b09
keywords:
- NM_CLICK (Statusleiste) Windows-Steuerelemente für Benachrichtigungs Code
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6066f76a8cf0b6ca34b5298cfcdcba2b11e3fa5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859340"
---
# <a name="nm_click-status-bar-notification-code"></a><span data-ttu-id="6a476-105">NM \_ Klick (Statusleiste) Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="6a476-105">NM\_CLICK (status bar) notification code</span></span>

<span data-ttu-id="6a476-106">Benachrichtigt das übergeordnete Fenster eines StatusBar-Steuer Elements, dass der Benutzer auf die linke Maustaste im Steuerelement geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="6a476-106">Notifies the parent window of a status bar control that the user has clicked the left mouse button within the control.</span></span> <span data-ttu-id="6a476-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="6a476-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    lpnm = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="6a476-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a476-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a476-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6a476-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6a476-110">Zeiger auf eine [**nmmouse**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) -Struktur, die zusätzliche Informationen zu dieser Benachrichtigung enthält.</span><span class="sxs-lookup"><span data-stu-id="6a476-110">Pointer to an [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) structure that contains additional information about this notification.</span></span> <span data-ttu-id="6a476-111">Der **dwitemspec** -Member enthält den Index des Abschnitts, auf den geklickt wurde.</span><span class="sxs-lookup"><span data-stu-id="6a476-111">The **dwItemSpec** member contains the index of the section that was clicked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a476-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6a476-112">Return value</span></span>

<span data-ttu-id="6a476-113">Gibt **true** zurück, um anzugeben, dass der Maus Klick behandelt wurde, und unterdrückt die Standard Verarbeitung durch das System.</span><span class="sxs-lookup"><span data-stu-id="6a476-113">Return **TRUE** to indicate that the mouse click was handled and suppress default processing by the system.</span></span> <span data-ttu-id="6a476-114">Gibt **false** zurück, um die Standard Verarbeitung des Click zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="6a476-114">Return **FALSE** to allow default processing of the click.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a476-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6a476-115">Requirements</span></span>



| <span data-ttu-id="6a476-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6a476-116">Requirement</span></span> | <span data-ttu-id="6a476-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6a476-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6a476-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6a476-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6a476-119">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a476-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6a476-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6a476-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6a476-121">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6a476-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6a476-122">Header</span><span class="sxs-lookup"><span data-stu-id="6a476-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a476-123"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a476-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





