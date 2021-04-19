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
ms.openlocfilehash: 5c03fae474f6622e1ccec0c5b52b0dfb473ba438
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590847"
---
# <a name="cdn_help-notification-code"></a><span data-ttu-id="387c1-104">CDN \_ HELP-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="387c1-104">CDN\_HELP notification code</span></span>

<span data-ttu-id="387c1-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="387c1-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="387c1-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="387c1-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="387c1-107">Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn der Benutzer auf die Schaltfläche **Hilfe** klickt.</span><span class="sxs-lookup"><span data-stu-id="387c1-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user clicks the **Help** button.</span></span>

<span data-ttu-id="387c1-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="387c1-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_HELP                (CDN_FIRST - 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="387c1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="387c1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="387c1-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="387c1-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="387c1-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="387c1-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="387c1-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="387c1-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="387c1-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="387c1-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="387c1-114">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN \_ HELP-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="387c1-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_HELP** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="387c1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="387c1-115">Return value</span></span>

<span data-ttu-id="387c1-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="387c1-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="387c1-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="387c1-117">Remarks</span></span>

<span data-ttu-id="387c1-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="387c1-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="387c1-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="387c1-119">Requirements</span></span>



| <span data-ttu-id="387c1-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="387c1-120">Requirement</span></span> | <span data-ttu-id="387c1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="387c1-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="387c1-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="387c1-122">Minimum supported client</span></span><br/> | <span data-ttu-id="387c1-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="387c1-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="387c1-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="387c1-124">Minimum supported server</span></span><br/> | <span data-ttu-id="387c1-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="387c1-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="387c1-126">Header</span><span class="sxs-lookup"><span data-stu-id="387c1-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="387c1-127"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="387c1-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="387c1-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="387c1-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="387c1-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="387c1-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="387c1-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="387c1-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="387c1-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="387c1-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="387c1-132">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="387c1-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="387c1-133">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="387c1-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="387c1-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="387c1-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="387c1-135">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="387c1-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="387c1-136">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="387c1-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

