---
title: PSN_KILLACTIVE Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass Sie im Begriff ist, die Aktivierung zu verlieren, weil eine andere Seite aktiviert oder der Benutzer auf die Schaltfläche "OK" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 470cd6ff-73ad-451a-a861-4d3324a8a8db
keywords:
- Windows-Steuerelemente für PSN_KILLACTIVE Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_KILLACTIVE
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ae5f90670c79797ef8576c5e6e3911255ab5fe1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949771"
---
# <a name="psn_killactive-notification-code"></a><span data-ttu-id="db9fd-105">PSN- \_ killactive-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="db9fd-105">PSN\_KILLACTIVE notification code</span></span>

<span data-ttu-id="db9fd-106">Benachrichtigt eine Seite, dass Sie im Begriff ist, die Aktivierung zu verlieren, weil eine andere Seite aktiviert oder der Benutzer auf die Schaltfläche "OK" geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="db9fd-106">Notifies a page that it is about to lose activation either because another page is being activated or the user has clicked the OK button.</span></span> <span data-ttu-id="db9fd-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="db9fd-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_KILLACTIVE 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="db9fd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="db9fd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9fd-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="db9fd-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="db9fd-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="db9fd-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="db9fd-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="db9fd-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="db9fd-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="db9fd-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9fd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db9fd-113">Return value</span></span>

<span data-ttu-id="db9fd-114">Gibt **true** zurück, um zu verhindern, dass die Seite die Aktivierung verliert, oder **false** , um Sie zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="db9fd-114">Returns **TRUE** to prevent the page from losing the activation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="db9fd-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db9fd-115">Remarks</span></span>

<span data-ttu-id="db9fd-116">Eine Anwendung verarbeitet diesen Benachrichtigungs Code, um die vom Benutzer eingegebenen Informationen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="db9fd-116">An application handles this notification code to validate the information the user has entered.</span></span>

> [!Note]  
> <span data-ttu-id="db9fd-117">Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der \_ Benachrichtigungs Code "PSN killactive" gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="db9fd-117">The property sheet is in the process of manipulating the list of pages when the PSN\_KILLACTIVE notification code is sent.</span></span> <span data-ttu-id="db9fd-118">Versuchen Sie nicht, während der Verarbeitung dieses Benachrichtigungs Codes Seiten hinzuzufügen, zu entfernen oder einzufügen.</span><span class="sxs-lookup"><span data-stu-id="db9fd-118">Do not attempt to add, remove, or insert pages while handling this notification code.</span></span> <span data-ttu-id="db9fd-119">Dies führt zu unvorhersehbaren Ergebnissen.</span><span class="sxs-lookup"><span data-stu-id="db9fd-119">Doing so will have unpredictable results.</span></span>

 

<span data-ttu-id="db9fd-120">Um einen Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit einem DWL- \_ msgresult-Wert aufrufen, der auf den Rückgabewert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="db9fd-120">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a DWL\_MSGRESULT value set to the return value.</span></span> <span data-ttu-id="db9fd-121">Die Dialogfeld Prozedur muss " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="db9fd-121">The dialog box procedure must return **TRUE**.</span></span>

<span data-ttu-id="db9fd-122">Wenn in der Dialogfeld Prozedur DWL \_ msgresult auf **true** festgelegt wird, sollte ein Meldungs Feld angezeigt werden, um das Problem für den Benutzer zu erläutern.</span><span class="sxs-lookup"><span data-stu-id="db9fd-122">If the dialog box procedure sets DWL\_MSGRESULT to **TRUE**, it should display a message box to explain the problem to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="db9fd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db9fd-123">Requirements</span></span>



| <span data-ttu-id="db9fd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db9fd-124">Requirement</span></span> | <span data-ttu-id="db9fd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="db9fd-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="db9fd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db9fd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="db9fd-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db9fd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="db9fd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db9fd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="db9fd-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db9fd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="db9fd-130">Header</span><span class="sxs-lookup"><span data-stu-id="db9fd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="db9fd-131"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="db9fd-131"><dt>Prsht.h</dt></span></span> </dl> |



 

