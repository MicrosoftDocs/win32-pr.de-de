---
title: TBN_DRAGOUT Benachrichtigungs Code (kommctrl. h)
description: Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt, und verschiebt den Cursor dann von der Schaltfläche. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 3566ad60-9744-494f-bb02-d30b41d06351
keywords:
- Windows-Steuerelemente für TBN_DRAGOUT Benachrichtigungs
topic_type:
- apiref
api_name:
- TBN_DRAGOUT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54fa61ef183b56b882c6ecdcb9d0d59edbf13e80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040355"
---
# <a name="tbn_dragout-notification-code"></a><span data-ttu-id="a9840-105">TBN- \_ dragout-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a9840-105">TBN\_DRAGOUT notification code</span></span>

<span data-ttu-id="a9840-106">Wird von einem ToolBar-Steuerelement gesendet, wenn der Benutzer auf eine Schaltfläche klickt, und verschiebt den Cursor dann von der Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a9840-106">Sent by a toolbar control when the user clicks a button and then moves the cursor off the button.</span></span> <span data-ttu-id="a9840-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9840-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_DRAGOUT

    lpnmtb = (LPNMTOOLBAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="a9840-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9840-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9840-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a9840-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a9840-110">Zeiger auf eine [**nmtoolbar**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) -Struktur, die Informationen zu diesem Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="a9840-110">Pointer to an [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) structure that contains information about this notification code.</span></span> <span data-ttu-id="a9840-111">Bei diesem Benachrichtigungs Code sind nur die **HDR** -und **iItem** -Member dieser Struktur gültig.</span><span class="sxs-lookup"><span data-stu-id="a9840-111">For this notification code, only the **hdr** and **iItem** members of this structure are valid.</span></span> <span data-ttu-id="a9840-112">Der **iItem** -Member dieser Struktur enthält den Befehls Bezeichner der gezogenen Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="a9840-112">The **iItem** member of this structure contains the command identifier of the button being dragged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9840-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9840-113">Return value</span></span>

<span data-ttu-id="a9840-114">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a9840-114">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9840-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9840-115">Remarks</span></span>

<span data-ttu-id="a9840-116">Mit diesem Benachrichtigungs Code kann eine Anwendung Drag & amp; Drop-Funktionen für Symbolleisten Schaltflächen implementieren.</span><span class="sxs-lookup"><span data-stu-id="a9840-116">This notification code allows an application to implement drag-and-drop functionality for toolbar buttons.</span></span> <span data-ttu-id="a9840-117">Bei der Verarbeitung dieses Benachrichtigungs Codes startet die Anwendung den Drag & Drop-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a9840-117">When processing this notification code, the application will begin the drag-and-drop operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9840-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9840-118">Requirements</span></span>



| <span data-ttu-id="a9840-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9840-119">Requirement</span></span> | <span data-ttu-id="a9840-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a9840-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a9840-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a9840-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a9840-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9840-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a9840-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a9840-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a9840-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a9840-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a9840-125">Header</span><span class="sxs-lookup"><span data-stu-id="a9840-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9840-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9840-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





