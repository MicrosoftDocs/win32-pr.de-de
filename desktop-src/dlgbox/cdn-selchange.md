---
title: CDN_SELCHANGE Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld Im Explorer-Stil öffnen oder speichern unter gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- CDN_SELCHANGE Benachrichtigungscode (Dialogfelder)
topic_type:
- apiref
api_name:
- CDN_SELCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5a5c7aed47d02fb7c7fcf2232b144e7a99e7c46
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590753"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="6b9a9-104">CDN \_ SELCHANGE-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="6b9a9-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="6b9a9-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="6b9a9-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="6b9a9-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="6b9a9-107">Wird von einem  Dialogfeld Im Explorer-Stil öffnen oder speichern **unter** gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="6b9a9-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="6b9a9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b9a9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b9a9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b9a9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9a9-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b9a9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b9a9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b9a9-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="6b9a9-114">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Code** member die **CDN \_ SELCHANGE-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b9a9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b9a9-115">Return value</span></span>

<span data-ttu-id="6b9a9-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b9a9-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b9a9-117">Remarks</span></span>

<span data-ttu-id="6b9a9-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mithilfe des **\_ OFN-EXPLORER-Werts erstellt** wurde.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="6b9a9-119">Um den Namen der neu ausgewählten Datei oder des neu ausgewählten Ordners zu erhalten, kann die Hookprozedur die [**CDM \_ GETFILEPATH-**](cdm-getfilepath.md) oder [**CDM \_ GETSPEC-Nachricht**](cdm-getspec.md) an das Dialogfeld senden.</span><span class="sxs-lookup"><span data-stu-id="6b9a9-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b9a9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b9a9-120">Requirements</span></span>



| <span data-ttu-id="6b9a9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b9a9-121">Requirement</span></span> | <span data-ttu-id="6b9a9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="6b9a9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b9a9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6b9a9-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b9a9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6b9a9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b9a9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6b9a9-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b9a9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b9a9-127">Header</span><span class="sxs-lookup"><span data-stu-id="6b9a9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b9a9-128"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b9a9-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b9a9-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6b9a9-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b9a9-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6b9a9-131">**CDM \_ GETFILEPATH**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="6b9a9-132">**CDM \_ GETSPEC**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="6b9a9-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="6b9a9-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="6b9a9-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="6b9a9-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="6b9a9-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="6b9a9-137">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="6b9a9-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b9a9-138">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="6b9a9-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

