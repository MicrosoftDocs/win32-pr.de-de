---
title: PSN_RESET Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass das Eigenschaften Blatt zerstört werden soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 75448852-8a5e-41a7-92b6-00692e771a06
keywords:
- Windows-Steuerelemente für PSN_RESET Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_RESET
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5642a5354d934b37ee58007a9fb260befe201edd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340314"
---
# <a name="psn_reset-notification-code"></a><span data-ttu-id="4bdce-105">\_Benachrichtigungs Code für PSN-zurück</span><span class="sxs-lookup"><span data-stu-id="4bdce-105">PSN\_RESET notification code</span></span>

<span data-ttu-id="4bdce-106">Benachrichtigt eine Seite, dass das Eigenschaften Blatt zerstört werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bdce-106">Notifies a page that the property sheet is about to be destroyed.</span></span> <span data-ttu-id="4bdce-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="4bdce-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_RESET 

    lppsn = (LPPSHNOTIFY) lParam;
```



## <a name="parameters"></a><span data-ttu-id="4bdce-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bdce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bdce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="4bdce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="4bdce-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="4bdce-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bdce-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bdce-111">Return value</span></span>

<span data-ttu-id="4bdce-112">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="4bdce-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bdce-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bdce-113">Remarks</span></span>

<span data-ttu-id="4bdce-114">Alle Änderungen, die seit dem letzten Benachrichtigungs Code für den [PSN \_](psn-apply.md) -Anwendungscode vorgenommen wurden, werden abgebrochen, außer im Fall von [**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), der diesen Benachrichtigungs Code nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4bdce-114">All changes made since the last [PSN\_APPLY](psn-apply.md) notification code are canceled, except in the case of [**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2), which does not support that notification code.</span></span>

<span data-ttu-id="4bdce-115">Der **LPARAM** -Member der [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, auf die von *LPARAM* verwiesen wird, wird auf " **true** " festgelegt, wenn der Benutzer auf die Schaltfläche " **X** " in der oberen rechten Ecke des Eigenschaften Blatts geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="4bdce-115">The **lParam** member of the [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure pointed to by *lParam* will be set to **TRUE** if the user clicked the **X** button in the upper-right corner of the property sheet.</span></span> <span data-ttu-id="4bdce-116">Der Wert ist **false** , wenn der Benutzer auf die Schaltfläche **Abbrechen** geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="4bdce-116">It will be **FALSE** if the user clicked the **Cancel** button.</span></span> <span data-ttu-id="4bdce-117">Die **pshnotify** -Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="4bdce-117">The **PSHNOTIFY** structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

<span data-ttu-id="4bdce-118">Eine Anwendung kann diesen Benachrichtigungs Code als Gelegenheit zum Ausführen von Bereinigungs Vorgängen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4bdce-118">An application can use this notification code as an opportunity to perform cleanup operations.</span></span>

> [!Note]  
> <span data-ttu-id="4bdce-119">Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code für die PSN-zurück Setzung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bdce-119">The property sheet is in the process of manipulating the list of pages when the PSN\_RESET notification code is sent.</span></span> <span data-ttu-id="4bdce-120">Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bdce-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="4bdce-121">Dies führt zu unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="4bdce-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="4bdce-122">Beim Verarbeiten dieses Benachrichtigungs Codes dürfen Sie die [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) -Funktion nicht aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="4bdce-122">Do not call the [**EndDialog**](/windows/desktop/api/winuser/nf-winuser-enddialog) function when processing this notification code.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bdce-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bdce-123">Requirements</span></span>



| <span data-ttu-id="4bdce-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bdce-124">Requirement</span></span> | <span data-ttu-id="4bdce-125">Wert</span><span class="sxs-lookup"><span data-stu-id="4bdce-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4bdce-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bdce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4bdce-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bdce-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="4bdce-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bdce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4bdce-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4bdce-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="4bdce-130">Header</span><span class="sxs-lookup"><span data-stu-id="4bdce-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="4bdce-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="4bdce-131"><dt>Prsht.h</dt></span></span> </dl> |



 

