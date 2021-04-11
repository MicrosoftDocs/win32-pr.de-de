---
title: CDN_HELP Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer auf die Schaltfläche Hilfe klickt.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- Dialog Felder für CDN_HELP Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_HELP
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c73b690b1ac522a985ae121413804c4385e0f2cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105315"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="1f6ab-104">CDN- \_ Hilfe-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="1f6ab-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="1f6ab-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="1f6ab-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="1f6ab-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1f6ab-107">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="1f6ab-108">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="1f6ab-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f6ab-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1f6ab-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1f6ab-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f6ab-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1f6ab-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1f6ab-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1f6ab-113">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="1f6ab-114">Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN- \_ Hilfe** Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1f6ab-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f6ab-115">Return value</span></span>

<span data-ttu-id="1f6ab-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f6ab-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1f6ab-117">Remarks</span></span>

<span data-ttu-id="1f6ab-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1f6ab-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1f6ab-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1f6ab-119">Requirements</span></span>



| <span data-ttu-id="1f6ab-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1f6ab-120">Requirement</span></span> | <span data-ttu-id="1f6ab-121">Wert</span><span class="sxs-lookup"><span data-stu-id="1f6ab-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f6ab-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1f6ab-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1f6ab-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f6ab-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1f6ab-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1f6ab-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1f6ab-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1f6ab-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1f6ab-126">Header</span><span class="sxs-lookup"><span data-stu-id="1f6ab-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="1f6ab-127"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1f6ab-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1f6ab-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f6ab-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="1f6ab-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1f6ab-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1f6ab-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1f6ab-132">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="1f6ab-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1f6ab-133">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="1f6ab-134">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="1f6ab-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="1f6ab-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1f6ab-136">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1f6ab-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

