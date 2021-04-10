---
title: TBN_DROPDOWN Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Dropdown-Schaltfläche klickt Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 85360f74-4b43-4d0a-8c89-22b0741fe96a
keywords:
- Windows-Steuerelemente für TBN_DROPDOWN Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DROPDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad7adbb9e0e2ed3d77f8ca8bfb6b09dedd2265be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949693"
---
# <a name="tbn_dropdown-notification-code"></a><span data-ttu-id="b1db0-105">TBN- \_ Dropdown-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b1db0-105">TBN\_DROPDOWN notification code</span></span>

<span data-ttu-id="b1db0-106">Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Dropdown-Schaltfläche klickt</span><span class="sxs-lookup"><span data-stu-id="b1db0-106">Sent by a toolbar control when the user clicks a dropdown button.</span></span> <span data-ttu-id="b1db0-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="b1db0-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DROPDOWN

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="b1db0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1db0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1db0-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1db0-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1db0-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="b1db0-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="b1db0-111">Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig.</span><span class="sxs-lookup"><span data-stu-id="b1db0-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1db0-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1db0-112">Return value</span></span>

<span data-ttu-id="b1db0-113">Gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="b1db0-113">Returns one of the following values:</span></span>



| <span data-ttu-id="b1db0-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b1db0-114">Return code</span></span>                                                                                          | <span data-ttu-id="b1db0-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1db0-115">Description</span></span>                                                                       |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1db0-116"><dt>**tbddret ( \_ Standard)**</dt></span><span class="sxs-lookup"><span data-stu-id="b1db0-116"><dt>**TBDDRET\_DEFAULT**</dt></span></span> </dl>      | <span data-ttu-id="b1db0-117">Der Dropdown wurde behandelt.</span><span class="sxs-lookup"><span data-stu-id="b1db0-117">The drop-down was handled.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b1db0-118"><dt>**tbddret \_ NODEFAULT**</dt></span><span class="sxs-lookup"><span data-stu-id="b1db0-118"><dt>**TBDDRET\_NODEFAULT**</dt></span></span> </dl>    | <span data-ttu-id="b1db0-119">Die Dropdown-Dropdown-Anwendung wurde nicht behandelt.</span><span class="sxs-lookup"><span data-stu-id="b1db0-119">The drop-down was not handled.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b1db0-120"><dt>**tbddret- \_ behandelte**</dt></span><span class="sxs-lookup"><span data-stu-id="b1db0-120"><dt>**TBDDRET\_TREATPRESSED**</dt></span></span> </dl> | <span data-ttu-id="b1db0-121">Das Dropdown Feld wurde behandelt, aber die Schaltfläche wird wie eine reguläre Schaltfläche behandelt.</span><span class="sxs-lookup"><span data-stu-id="b1db0-121">The drop-down was handled, but treat the button like a regular button.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b1db0-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1db0-122">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b1db0-123">Dropdown Schaltflächen können Plain ([**btns- \_ Dropdown**](toolbar-control-and-button-styles.md) -Stil) sein, einen Pfeil neben dem Schaltflächen Bild anzeigen ([**btns- \_ volledropdown**](toolbar-control-and-button-styles.md) -Stil) oder einen Pfeil anzeigen, der vom Bild getrennt ist ([**tbstyle \_ Ex \_ drawddarrows**](toolbar-extended-styles.md) -Stil).</span><span class="sxs-lookup"><span data-stu-id="b1db0-123">Dropdown buttons can be plain ([**BTNS\_DROPDOWN**](toolbar-control-and-button-styles.md) style), display an arrow next to the button image ([**BTNS\_WHOLEDROPDOWN**](toolbar-control-and-button-styles.md) style), or display an arrow that is separated from the image ([**TBSTYLE\_EX\_DRAWDDARROWS**](toolbar-extended-styles.md) style).</span></span> <span data-ttu-id="b1db0-124">Wenn ein getrennter Pfeil verwendet wird, wird die TBN- \_ Dropdown Liste nur gesendet, wenn der Benutzer auf den Pfeil Bereich der Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="b1db0-124">If a separated arrow is used, TBN\_DROPDOWN is sent only if the user clicks the arrow portion of the button.</span></span> <span data-ttu-id="b1db0-125">Wenn der Benutzer auf den Hauptteil der Schaltfläche klickt, wird eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Meldung mit der ID des Schaltflächen wie bei einer Standard Schaltfläche gesendet.</span><span class="sxs-lookup"><span data-stu-id="b1db0-125">If the user clicks the main part of the button, a [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) message with button's ID is sent, just as with a standard button.</span></span> <span data-ttu-id="b1db0-126">Für die beiden anderen Stile der Dropdown Schaltfläche wird die TBN- \_ Dropdown Liste gesendet, wenn der Benutzer auf einen beliebigen Teil der Schaltfläche klickt.</span><span class="sxs-lookup"><span data-stu-id="b1db0-126">For the other two styles of dropdown button, TBN\_DROPDOWN is sent when the user clicks any part of the button.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="b1db0-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1db0-127">Requirements</span></span>



| <span data-ttu-id="b1db0-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1db0-128">Requirement</span></span> | <span data-ttu-id="b1db0-129">Wert</span><span class="sxs-lookup"><span data-stu-id="b1db0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b1db0-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1db0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b1db0-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1db0-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b1db0-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1db0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b1db0-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1db0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b1db0-134">Header</span><span class="sxs-lookup"><span data-stu-id="b1db0-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1db0-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1db0-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

