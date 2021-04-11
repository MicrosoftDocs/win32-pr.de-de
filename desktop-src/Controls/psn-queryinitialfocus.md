---
title: PSN_QUERYINITIALFOCUS Benachrichtigungs Code (prsht. h)
description: Wird von einem Eigenschaften Blatt gesendet, um der Seite eines Eigenschaften Blatts anzugeben, welches Dialogfeld-Steuerelement den Anfangs Fokus erhalten soll. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 29b5e598-75b2-4b6f-acdb-171b1f7a1850
keywords:
- Windows-Steuerelemente für PSN_QUERYINITIALFOCUS Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_QUERYINITIALFOCUS
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc542332440009f6564f384b415657e725edda00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102974"
---
# <a name="psn_queryinitialfocus-notification-code"></a><span data-ttu-id="16e97-105">PSN \_ queryinitialfocus-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="16e97-105">PSN\_QUERYINITIALFOCUS notification code</span></span>

<span data-ttu-id="16e97-106">Wird von einem Eigenschaften Blatt gesendet, um der Seite eines Eigenschaften Blatts anzugeben, welches Dialogfeld-Steuerelement den Anfangs Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="16e97-106">Sent by a property sheet to provide a property sheet page an opportunity to specify which dialog box control should receive the initial focus.</span></span> <span data-ttu-id="16e97-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="16e97-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_QUERYINITIALFOCUS

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="16e97-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="16e97-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16e97-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16e97-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16e97-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="16e97-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure.</span></span> <span data-ttu-id="16e97-111">Wandelt den **LPARAM** -Member dieser-Struktur in einen **HWND** -Typ um, um das Handle des Steuer Elements abzurufen, dem der Fokus standardmäßig zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="16e97-111">Cast the **lParam** member of this structure to an **HWND** type, to retrieve the handle of the control that will be given focus by default.</span></span> <span data-ttu-id="16e97-112">Die Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="16e97-112">The structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16e97-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16e97-113">Return value</span></span>

<span data-ttu-id="16e97-114">Um anzugeben, welches Steuerelement den Fokus erhalten soll, geben Sie das Handle des Steuer Elements zurück.</span><span class="sxs-lookup"><span data-stu-id="16e97-114">To specify which control should receive focus, return the control's handle.</span></span> <span data-ttu-id="16e97-115">Andernfalls wird NULL zurückgegeben, und der Fokus wird auf das Standard Steuerelement zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="16e97-115">Otherwise, return zero and focus will go to the default control.</span></span> <span data-ttu-id="16e97-116">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit einem **DWL- \_ msgresult** -Wert aufrufen und **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="16e97-116">To set the return value, the dialog box procedure must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with a **DWL\_MSGRESULT** value and return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="16e97-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16e97-117">Remarks</span></span>

<span data-ttu-id="16e97-118">Bei der Verarbeitung dieses Benachrichtigungs Codes darf eine Anwendung die [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) -Funktion nicht aufrufen.</span><span class="sxs-lookup"><span data-stu-id="16e97-118">An application must not call the [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) function while handling this notification code.</span></span> <span data-ttu-id="16e97-119">Gibt das Handle des Steuer Elements zurück, das den Fokus erhalten soll, und der Eigenschaften Blatt-Manager behandelt die Fokus Änderung.</span><span class="sxs-lookup"><span data-stu-id="16e97-119">Return the handle of the control that should receive focus, and the property sheet manager will handle the focus change.</span></span>

<span data-ttu-id="16e97-120">Der "PSN \_ queryinitialfocus"-Benachrichtigungs Code wird nicht gesendet, wenn der Eigenschaften Blatt-Manager feststellt, dass kein Steuerelement auf der Seite den Fokus erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="16e97-120">The PSN\_QUERYINITIALFOCUS notification code is not sent if the property sheet manager determines that no control on the page should receive focus.</span></span>

<span data-ttu-id="16e97-121">Dieses Code Fragment implementiert einen einfachen Handler für "PSN \_ queryinitialfocus".</span><span class="sxs-lookup"><span data-stu-id="16e97-121">This code fragment implements a simple handler for PSN\_QUERYINITIALFOCUS.</span></span> <span data-ttu-id="16e97-122">Sie fordert an, dass der anfängliche Fokus an die Location Control (**IDC- \_ Speicherort**) gegeben wird.</span><span class="sxs-lookup"><span data-stu-id="16e97-122">It requests that initial focus be given to the Location control (**IDC\_LOCATION**).</span></span>

``` syntax
case PSN_QUERYINITIALFOCUS :
    SetWindowLong(hDlg,DWL_MSGRESULT, (LPARAM)GetDlgItem(hDlg, IDC_LOCATION));
    return TRUE;
...
```

> [!Note]  
> <span data-ttu-id="16e97-123">Dieser Benachrichtigungs Code wird nicht unterstützt, wenn der Aero Wizard Style ([**PSH \_ aerowizard**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16e97-123">This notification code is not supported when using the Aero wizard style ([**PSH\_AEROWIZARD**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2)).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="16e97-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16e97-124">Requirements</span></span>



| <span data-ttu-id="16e97-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16e97-125">Requirement</span></span> | <span data-ttu-id="16e97-126">Wert</span><span class="sxs-lookup"><span data-stu-id="16e97-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="16e97-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16e97-127">Minimum supported client</span></span><br/> | <span data-ttu-id="16e97-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16e97-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="16e97-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16e97-129">Minimum supported server</span></span><br/> | <span data-ttu-id="16e97-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16e97-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="16e97-131">Header</span><span class="sxs-lookup"><span data-stu-id="16e97-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="16e97-132"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="16e97-132"><dt>Prsht.h</dt></span></span> </dl> |



 

