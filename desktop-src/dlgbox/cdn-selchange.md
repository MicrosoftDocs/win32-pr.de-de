---
title: CDN_SELCHANGE Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Dialog Felder für CDN_SELCHANGE Benachrichtigungs Code
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
ms.openlocfilehash: 6e2f0f5a7860c7d729340a84bd80bc4e5713c733
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476677"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="66239-104">CDN \_ selChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="66239-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="66239-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="66239-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="66239-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="66239-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="66239-107">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="66239-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="66239-108">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="66239-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="66239-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="66239-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66239-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="66239-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66239-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="66239-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="66239-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="66239-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="66239-113">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="66239-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="66239-114">Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die CDN-Benachrichtigungs Meldung " **\_ selChange** " angibt.</span><span class="sxs-lookup"><span data-stu-id="66239-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66239-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="66239-115">Return value</span></span>

<span data-ttu-id="66239-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="66239-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="66239-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="66239-117">Remarks</span></span>

<span data-ttu-id="66239-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="66239-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="66239-119">Um den Namen der neu ausgewählten Datei oder des ausgewählten Ordners zu erhalten, kann die Hook-Prozedur die [**CDM- \_ GetFilePath**](cdm-getfilepath.md) -oder die [**CDM \_ getSpec**](cdm-getspec.md) -Nachricht an das Dialogfeld senden.</span><span class="sxs-lookup"><span data-stu-id="66239-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="66239-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="66239-120">Requirements</span></span>



| <span data-ttu-id="66239-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="66239-121">Requirement</span></span> | <span data-ttu-id="66239-122">Wert</span><span class="sxs-lookup"><span data-stu-id="66239-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66239-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="66239-123">Minimum supported client</span></span><br/> | <span data-ttu-id="66239-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66239-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="66239-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="66239-125">Minimum supported server</span></span><br/> | <span data-ttu-id="66239-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="66239-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="66239-127">Header</span><span class="sxs-lookup"><span data-stu-id="66239-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="66239-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66239-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66239-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66239-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="66239-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="66239-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="66239-131">**CDM \_ GetFilePath**</span><span class="sxs-lookup"><span data-stu-id="66239-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="66239-132">**CDM \_ getSpec**</span><span class="sxs-lookup"><span data-stu-id="66239-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="66239-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="66239-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="66239-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="66239-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="66239-135">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="66239-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="66239-136">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="66239-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="66239-137">**Licher**</span><span class="sxs-lookup"><span data-stu-id="66239-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66239-138">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="66239-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

