---
title: TVN_SINGLEEXPAND Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Strukturansicht-Steuerelement mit dem singleexpand-Stil des TVs gesendet, \_ Wenn der Benutzer ein Strukturelement mit einem einzigen Mausklick öffnet oder schließt. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: ae738237-172a-400b-b9fe-33832224e299
keywords:
- Windows-Steuerelemente für TVN_SINGLEEXPAND Benachrichtigungs
topic_type:
- apiref
api_name:
- TVN_SINGLEEXPAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 976c0e8acfee1f024e4ee7f88d9f745e4029ec82
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475744"
---
# <a name="tvn_singleexpand-notification-code"></a><span data-ttu-id="de150-105">TVN \_ singleexpand-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="de150-105">TVN\_SINGLEEXPAND notification code</span></span>

<span data-ttu-id="de150-106">Wird von einem Strukturansicht-Steuerelement mit [**dem \_ singleexpand**](tree-view-control-window-styles.md) -Stil des TVs gesendet, wenn der Benutzer ein Strukturelement mit einem einzigen Mausklick öffnet oder schließt.</span><span class="sxs-lookup"><span data-stu-id="de150-106">Sent by a tree-view control with the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style when the user opens or closes a tree item using a single click of the mouse.</span></span> <span data-ttu-id="de150-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="de150-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_SINGLEEXPAND

    lpnmtv = (LPNMTREEVIEW)lParam;
```



## <a name="parameters"></a><span data-ttu-id="de150-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de150-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de150-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="de150-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="de150-110">Zeiger auf eine [**nmtreeview**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="de150-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure that contains information about this notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de150-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de150-111">Return value</span></span>

<span data-ttu-id="de150-112">Rückgabe von tvnret \_ Default, damit das Standardverhalten auftritt.</span><span class="sxs-lookup"><span data-stu-id="de150-112">Return TVNRET\_DEFAULT to allow the default behavior to occur.</span></span> <span data-ttu-id="de150-113">Um das Standardverhalten zu ändern, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="de150-113">To modify the default behavior, return:</span></span>



| <span data-ttu-id="de150-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="de150-114">Return code</span></span>                                                                                    | <span data-ttu-id="de150-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de150-115">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="de150-116"><dt>**tvnret \_ skipold**</dt></span><span class="sxs-lookup"><span data-stu-id="de150-116"><dt>**TVNRET\_SKIPOLD**</dt></span></span> </dl> | <span data-ttu-id="de150-117">Überspringen Sie die Standard Verarbeitung des Elements, dessen Auswahl aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="de150-117">Skip default processing of the item being unselected.</span></span><br/> |
| <dl> <span data-ttu-id="de150-118"><dt>**tvnret \_ skipnew**</dt></span><span class="sxs-lookup"><span data-stu-id="de150-118"><dt>**TVNRET\_SKIPNEW**</dt></span></span> </dl> | <span data-ttu-id="de150-119">Überspringen Sie die Standard Verarbeitung des ausgewählten Elements.</span><span class="sxs-lookup"><span data-stu-id="de150-119">Skip default processing of the item being selected.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="de150-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de150-120">Remarks</span></span>

<span data-ttu-id="de150-121">Um die Standard Verarbeitung ausgewählter und nicht ausgewählter Elemente zu überspringen, geben Sie sowohl tvnret \_ skipold als auch tvnret \_ skipnew zurück, indem Sie Sie mit einem logischen OR kombinieren.</span><span class="sxs-lookup"><span data-stu-id="de150-121">To skip default processing of selected and unselected items, return both TVNRET\_SKIPOLD and TVNRET\_SKIPNEW by combining them with a logical OR.</span></span>

<span data-ttu-id="de150-122">Dieser Benachrichtigungs Code wird nur von Strukturansicht-Steuerelementen gesendet, die den [**\_ singleexpand**](tree-view-control-window-styles.md) -Stil "TVs" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="de150-122">This notification code is only sent by tree-view controls that have the [**TVS\_SINGLEEXPAND**](tree-view-control-window-styles.md) style.</span></span>

## <a name="requirements"></a><span data-ttu-id="de150-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de150-123">Requirements</span></span>



| <span data-ttu-id="de150-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de150-124">Requirement</span></span> | <span data-ttu-id="de150-125">Wert</span><span class="sxs-lookup"><span data-stu-id="de150-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="de150-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="de150-126">Minimum supported client</span></span><br/> | <span data-ttu-id="de150-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de150-127">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="de150-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="de150-128">Minimum supported server</span></span><br/> | <span data-ttu-id="de150-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="de150-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="de150-130">Header</span><span class="sxs-lookup"><span data-stu-id="de150-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="de150-131"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="de150-131"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





