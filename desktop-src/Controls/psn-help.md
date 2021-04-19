---
title: PSN_HELP Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche "Hilfe" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4ad2c608-8caa-44c6-845d-4c0c1bd80763
keywords:
- Windows-Steuerelemente für PSN_HELP Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_HELP
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa60e039211e4c8e63a831ae547c3db116ede3f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342455"
---
# <a name="psn_help-notification-code"></a><span data-ttu-id="e216d-105">\_Benachrichtigungs Code für PSN-Hilfe</span><span class="sxs-lookup"><span data-stu-id="e216d-105">PSN\_HELP notification code</span></span>

<span data-ttu-id="e216d-106">Benachrichtigt eine Seite, dass der Benutzer auf die Schaltfläche "Hilfe" geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="e216d-106">Notifies a page that the user has clicked the Help button.</span></span> <span data-ttu-id="e216d-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="e216d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_HELP 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="e216d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e216d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e216d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e216d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e216d-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="e216d-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="e216d-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="e216d-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="e216d-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="e216d-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e216d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e216d-113">Return value</span></span>

<span data-ttu-id="e216d-114">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="e216d-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e216d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e216d-115">Remarks</span></span>

<span data-ttu-id="e216d-116">In einer Anwendung sollten Hilfe Informationen für die Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e216d-116">An application should display Help information for the page.</span></span>

> [!Note]  
> <span data-ttu-id="e216d-117">Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e216d-117">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e216d-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e216d-118">Requirements</span></span>



| <span data-ttu-id="e216d-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e216d-119">Requirement</span></span> | <span data-ttu-id="e216d-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e216d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e216d-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e216d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e216d-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e216d-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e216d-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e216d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e216d-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e216d-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e216d-125">Header</span><span class="sxs-lookup"><span data-stu-id="e216d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e216d-126"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="e216d-126"><dt>Prsht.h</dt></span></span> </dl> |



 

 





