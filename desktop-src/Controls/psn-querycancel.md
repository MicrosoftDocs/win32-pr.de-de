---
title: PSN_QUERYCANCEL Benachrichtigungs Code (prsht. h)
description: Gibt an, dass der Benutzer das Eigenschaften Blatt abgebrochen hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 4a789e08-065a-485c-87e3-f7958e2dc544
keywords:
- Windows-Steuerelemente für PSN_QUERYCANCEL Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_QUERYCANCEL
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27d39a7a02d80235db5f8fbe31809dcc913d51c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949769"
---
# <a name="psn_querycancel-notification-code"></a><span data-ttu-id="92f30-105">\_Benachrichtigungs Code für "PSN querycancel"</span><span class="sxs-lookup"><span data-stu-id="92f30-105">PSN\_QUERYCANCEL notification code</span></span>

<span data-ttu-id="92f30-106">Gibt an, dass der Benutzer das Eigenschaften Blatt abgebrochen hat.</span><span class="sxs-lookup"><span data-stu-id="92f30-106">Indicates that the user has canceled the property sheet.</span></span> <span data-ttu-id="92f30-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="92f30-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYCANCEL 

    lppsn = (LPPSHNOTIFY) lParam;  
```



## <a name="parameters"></a><span data-ttu-id="92f30-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="92f30-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92f30-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92f30-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92f30-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="92f30-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="92f30-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="92f30-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="92f30-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="92f30-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92f30-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92f30-113">Return value</span></span>

<span data-ttu-id="92f30-114">Gibt **true** zurück, um den Abbruch Vorgang zu verhindern, oder **false** , um dies zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="92f30-114">Returns **TRUE** to prevent the cancel operation, or **FALSE** to allow it.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f30-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92f30-115">Remarks</span></span>

<span data-ttu-id="92f30-116">Dieser Benachrichtigungs Code wird in der Regel gesendet, wenn ein Benutzer auf die Schaltfläche **Abbrechen** klickt.</span><span class="sxs-lookup"><span data-stu-id="92f30-116">This notification code is typically sent when a user clicks the **Cancel** button.</span></span> <span data-ttu-id="92f30-117">Sie wird auch gesendet, wenn ein Benutzer auf die Schaltfläche **X** in der rechten oberen Ecke des Eigenschaften Blatts klickt oder die Escapetaste drückt.</span><span class="sxs-lookup"><span data-stu-id="92f30-117">It is also sent when a user clicks the **X** button in the property sheet's upper right hand corner or presses the ESCAPE key.</span></span> <span data-ttu-id="92f30-118">Mit diesem Benachrichtigungs Code kann eine Eigenschaften Blattseite den Benutzer bitten, den Abbruch Vorgang zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="92f30-118">A property sheet page can handle this notification code to ask the user to verify the cancel operation.</span></span>

<span data-ttu-id="92f30-119">Um einen Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit DWL \_ msgresult aufrufen, die auf den Rückgabewert festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="92f30-119">To set a return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT set to the return value.</span></span> <span data-ttu-id="92f30-120">Die Dialogfeld Prozedur muss " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="92f30-120">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f30-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92f30-121">Requirements</span></span>



| <span data-ttu-id="92f30-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92f30-122">Requirement</span></span> | <span data-ttu-id="92f30-123">Wert</span><span class="sxs-lookup"><span data-stu-id="92f30-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92f30-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92f30-124">Minimum supported client</span></span><br/> | <span data-ttu-id="92f30-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92f30-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92f30-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92f30-126">Minimum supported server</span></span><br/> | <span data-ttu-id="92f30-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92f30-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92f30-128">Header</span><span class="sxs-lookup"><span data-stu-id="92f30-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="92f30-129"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="92f30-129"><dt>Prsht.h</dt></span></span> </dl> |



 

