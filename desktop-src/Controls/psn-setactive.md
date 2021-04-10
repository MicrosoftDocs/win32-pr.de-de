---
title: PSN_SETACTIVE Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass Sie im Begriff ist, aktiviert zu werden. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 0cf918b7-9f0d-4dec-8df1-a1d2d8ac6463
keywords:
- Windows-Steuerelemente für PSN_SETACTIVE Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_SETACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f38db77c1c60ef60ce713d41a6112b42235b79a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956716"
---
# <a name="psn_setactive-notification-code"></a><span data-ttu-id="3d6f2-105">PSN- \_ SETACTIVE-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="3d6f2-105">PSN\_SETACTIVE notification code</span></span>

<span data-ttu-id="3d6f2-106">Benachrichtigt eine Seite, dass Sie im Begriff ist, aktiviert zu werden.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-106">Notifies a page that it is about to be activated.</span></span> <span data-ttu-id="3d6f2-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_SETACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="3d6f2-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d6f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d6f2-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3d6f2-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3d6f2-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="3d6f2-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="3d6f2-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d6f2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3d6f2-113">Return value</span></span>

<span data-ttu-id="3d6f2-114">Gibt NULL zurück, um die Aktivierung zu akzeptieren, oder-1 zum Aktivieren der nächsten oder der vorherigen Seite (abhängig davon, ob der Benutzer auf die Schaltfläche " **weiter** " oder " **zurück** " geklickt hat).</span><span class="sxs-lookup"><span data-stu-id="3d6f2-114">Returns zero to accept the activation, or -1 to activate the next or the previous page (depending on whether the user clicked the **Next** or **Back** button).</span></span> <span data-ttu-id="3d6f2-115">Um die Aktivierung auf eine bestimmte Seite festzulegen, geben Sie den Ressourcen Bezeichner der Seite zurück.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-115">To set the activation to a particular page, return the resource identifier of the page.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d6f2-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3d6f2-116">Remarks</span></span>

<span data-ttu-id="3d6f2-117">Der \_ Benachrichtigungs Code "PSN SETACTIVE" wird gesendet, bevor die Seite sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-117">The PSN\_SETACTIVE notification code is sent before the page is visible.</span></span> <span data-ttu-id="3d6f2-118">Eine Anwendung kann diesen Benachrichtigungs Code verwenden, um Daten auf der Seite zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-118">An application can use this notification code to initialize data in the page.</span></span>

> [!Note]  
> <span data-ttu-id="3d6f2-119">Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN SETACTIVE" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-119">The property sheet is in the process of manipulating the list of pages when the PSN\_SETACTIVE notification code is sent.</span></span> <span data-ttu-id="3d6f2-120">Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-120">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="3d6f2-121">Dies führt zu unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-121">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="3d6f2-122">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden, und die Dialogfeld Prozedur muss **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="3d6f2-122">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value, and the dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d6f2-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3d6f2-123">Requirements</span></span>



| <span data-ttu-id="3d6f2-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3d6f2-124">Requirement</span></span> | <span data-ttu-id="3d6f2-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3d6f2-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d6f2-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3d6f2-126">Minimum supported client</span></span><br/> | <span data-ttu-id="3d6f2-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6f2-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d6f2-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3d6f2-128">Minimum supported server</span></span><br/> | <span data-ttu-id="3d6f2-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3d6f2-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d6f2-130">Header</span><span class="sxs-lookup"><span data-stu-id="3d6f2-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d6f2-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d6f2-131"><dt>Prsht.h</dt></span></span> </dl> |



 

