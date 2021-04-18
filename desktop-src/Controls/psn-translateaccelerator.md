---
title: PSN_TRANSLATEACCELERATOR Benachrichtigungs Code (prsht. h)
description: Benachrichtigt ein Eigenschaften Blatt, dass eine Tastatur Meldung empfangen wurde. Die Seite bietet die Möglichkeit, eine private Tastatur Zugriffstaste zu übersetzen. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 04d67326-92f9-4b92-a27e-354815f3c1a8
keywords:
- Windows-Steuerelemente für PSN_TRANSLATEACCELERATOR Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_TRANSLATEACCELERATOR
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9dc86866be1154bbd0ef1cf76b3535b7b02496e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337492"
---
# <a name="psn_translateaccelerator-notification-code"></a><span data-ttu-id="a8f35-106">PSN \_ TranslateAccelerator-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="a8f35-106">PSN\_TRANSLATEACCELERATOR notification code</span></span>

<span data-ttu-id="a8f35-107">Benachrichtigt ein Eigenschaften Blatt, dass eine Tastatur Meldung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a8f35-107">Notifies a property sheet that a keyboard message has been received.</span></span> <span data-ttu-id="a8f35-108">Die Seite bietet die Möglichkeit, eine private Tastatur Zugriffstaste zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="a8f35-108">It provides the page an opportunity to do private keyboard accelerator translation.</span></span> <span data-ttu-id="a8f35-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="a8f35-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_TRANSLATEACCELERATOR 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="a8f35-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8f35-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f35-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8f35-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8f35-112">Ein Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="a8f35-112">A pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="a8f35-113">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member der **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="a8f35-113">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of the **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="a8f35-114">Der **LPARAM** -Member der **pshnotify** -Struktur ist ein Zeiger [**auf die Meldung**](/windows/win32/api/winuser/ns-winuser-msg)der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="a8f35-114">The **lParam** member of the **PSHNOTIFY** structure is a pointer to the message's [**MSG**](/windows/win32/api/winuser/ns-winuser-msg).</span></span> <span data-ttu-id="a8f35-115">Sie kann in einen **lpmsg** -Typ umgewandelt werden, um Zugriff auf die Parameter der zu über setzenden Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8f35-115">It can be cast to an **LPMSG** type, to get access to the parameters of the message to be translated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f35-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8f35-116">Return value</span></span>

<span data-ttu-id="a8f35-117">Gibt psnret \_ messagebehandelte zurück, um anzugeben, dass keine weitere Verarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a8f35-117">Returns PSNRET\_MESSAGEHANDLED to indicate that no further processing is necessary.</span></span> <span data-ttu-id="a8f35-118">Gibt psnret \_ noError zurück, um die normale Verarbeitung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="a8f35-118">Returns PSNRET\_NOERROR to request normal processing.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f35-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8f35-119">Remarks</span></span>

<span data-ttu-id="a8f35-120">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem DWL \_ msgresult-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="a8f35-120">To set the return value, the dialog box procedure for the page must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the DWL\_MSGRESULT value.</span></span> <span data-ttu-id="a8f35-121">Die Dialogfeld Prozedur muss " **true**" zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a8f35-121">The dialog box procedure must return **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8f35-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8f35-122">Requirements</span></span>



| <span data-ttu-id="a8f35-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8f35-123">Requirement</span></span> | <span data-ttu-id="a8f35-124">Wert</span><span class="sxs-lookup"><span data-stu-id="a8f35-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8f35-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8f35-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a8f35-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8f35-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8f35-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8f35-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a8f35-128">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8f35-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a8f35-129">Header</span><span class="sxs-lookup"><span data-stu-id="a8f35-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8f35-130"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8f35-130"><dt>Prsht.h</dt></span></span> </dl> |



 

