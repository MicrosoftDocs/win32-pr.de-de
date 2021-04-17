---
title: CDN_TYPECHANGE Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinations Feld "Dateitypen" auswählt.
ms.assetid: fb8324db-e435-4ef2-aac5-506a6b7adb2c
keywords:
- Dialog Felder für CDN_TYPECHANGE Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_TYPECHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64226c1ac15cb6b55c6c2e2de7264d726e6f3a7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476674"
---
# <a name="cdn_typechange-notification-code"></a><span data-ttu-id="8abea-104">CDN \_ typechange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="8abea-104">CDN\_TYPECHANGE notification code</span></span>

<span data-ttu-id="8abea-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="8abea-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="8abea-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="8abea-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="8abea-107">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer einen neuen Dateityp aus dem Kombinations Feld "Dateitypen" auswählt.</span><span class="sxs-lookup"><span data-stu-id="8abea-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the user selects a new file type from the file types combo box.</span></span>

<span data-ttu-id="8abea-108">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="8abea-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_TYPECHANGE          (CDN_FIRST - 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="8abea-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8abea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8abea-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="8abea-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8abea-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8abea-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="8abea-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="8abea-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="8abea-113">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8abea-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="8abea-114">Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN- \_ typechange** -Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="8abea-114">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_TYPECHANGE** notification message.</span></span>

<span data-ttu-id="8abea-115">Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält auch einen Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, deren **nfilterindex** -Member den 1-basierten Index des neu ausgewählten Dateityp Filters angibt.</span><span class="sxs-lookup"><span data-stu-id="8abea-115">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **nFilterIndex** member indicates the one-based index of the newly selected file type filter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8abea-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8abea-116">Return value</span></span>

<span data-ttu-id="8abea-117">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="8abea-117">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8abea-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8abea-118">Remarks</span></span>

<span data-ttu-id="8abea-119">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8abea-119">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="8abea-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8abea-120">Requirements</span></span>



| <span data-ttu-id="8abea-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8abea-121">Requirement</span></span> | <span data-ttu-id="8abea-122">Wert</span><span class="sxs-lookup"><span data-stu-id="8abea-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8abea-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8abea-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8abea-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8abea-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8abea-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8abea-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8abea-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8abea-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="8abea-127">Header</span><span class="sxs-lookup"><span data-stu-id="8abea-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8abea-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8abea-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8abea-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8abea-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="8abea-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8abea-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8abea-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8abea-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="8abea-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="8abea-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="8abea-133">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="8abea-133">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="8abea-134">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="8abea-134">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="8abea-135">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="8abea-135">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="8abea-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8abea-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8abea-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8abea-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

