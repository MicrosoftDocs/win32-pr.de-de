---
title: CDN_HELP Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld im Explorer-Stil geöffnet oder speichern unter gesendet, wenn der Benutzer auf die Schaltfläche Hilfe klickt.
ms.assetid: 18ee86b2-3446-4de4-a47a-2e44e677f4f7
keywords:
- Dialogfelder für CDN_HELP Benachrichtigungscode
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
ms.openlocfilehash: 0abd3519bdc877eca24304b1104a12d51b2dfe4f
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550065"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="686ea-104">CDN \_ HELP-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="686ea-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="686ea-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="686ea-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="686ea-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="686ea-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="686ea-107">Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.</span><span class="sxs-lookup"><span data-stu-id="686ea-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="686ea-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="686ea-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="686ea-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="686ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="686ea-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="686ea-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="686ea-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="686ea-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="686ea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="686ea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="686ea-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="686ea-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="686ea-114">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN \_ HELP-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="686ea-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="686ea-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="686ea-115">Return value</span></span>

<span data-ttu-id="686ea-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="686ea-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="686ea-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="686ea-117">Remarks</span></span>

<span data-ttu-id="686ea-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="686ea-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="686ea-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="686ea-119">Requirements</span></span>



| <span data-ttu-id="686ea-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="686ea-120">Requirement</span></span> | <span data-ttu-id="686ea-121">Wert</span><span class="sxs-lookup"><span data-stu-id="686ea-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="686ea-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="686ea-122">Minimum supported client</span></span><br/> | <span data-ttu-id="686ea-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="686ea-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="686ea-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="686ea-124">Minimum supported server</span></span><br/> | <span data-ttu-id="686ea-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="686ea-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="686ea-126">Header</span><span class="sxs-lookup"><span data-stu-id="686ea-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="686ea-127"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="686ea-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="686ea-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="686ea-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="686ea-129">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="686ea-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="686ea-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="686ea-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="686ea-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="686ea-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="686ea-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="686ea-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="686ea-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="686ea-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="686ea-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="686ea-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="686ea-135">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="686ea-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="686ea-136">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="686ea-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

