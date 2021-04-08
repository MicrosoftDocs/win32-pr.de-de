---
title: CDN_FOLDERCHANGE Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn ein neuer Ordner geöffnet wird.
ms.assetid: 864ab80d-cd99-4dd6-8aff-49beed246e53
keywords:
- Dialog Felder für CDN_FOLDERCHANGE Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_FOLDERCHANGE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c93bd37afa44e7fc5ca81d928974f56bf80d1b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103946"
---
# <a name="cdn_folderchange-notification-code"></a><span data-ttu-id="670b4-104">CDN- \_ FolderChange-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="670b4-104">CDN\_FOLDERCHANGE notification code</span></span>

<span data-ttu-id="670b4-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="670b4-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="670b4-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="670b4-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="670b4-107">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn ein neuer Ordner geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="670b4-107">Sent by an Explorer-style **Open** or **Save As** dialog box when a new folder is opened.</span></span>

<span data-ttu-id="670b4-108">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="670b4-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FOLDERCHANGE        (CDN_FIRST - 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="670b4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="670b4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="670b4-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="670b4-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="670b4-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="670b4-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="670b4-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="670b4-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="670b4-113">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="670b4-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="670b4-114">Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN- \_ FolderChange** -Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="670b4-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FOLDERCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="670b4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="670b4-115">Return value</span></span>

<span data-ttu-id="670b4-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="670b4-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="670b4-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="670b4-117">Remarks</span></span>

<span data-ttu-id="670b4-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="670b4-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="670b4-119">Um den Pfad des neu geöffneten Ordners zu erhalten, kann die Hook-Prozedur die [**CDM- \_ GetFolderPath**](cdm-getfolderpath.md) -Nachricht an das Dialogfeld senden.</span><span class="sxs-lookup"><span data-stu-id="670b4-119">To get the path of the newly opened folder, the hook procedure can send the [**CDM\_GETFOLDERPATH**](cdm-getfolderpath.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="670b4-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="670b4-120">Requirements</span></span>



| <span data-ttu-id="670b4-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="670b4-121">Requirement</span></span> | <span data-ttu-id="670b4-122">Wert</span><span class="sxs-lookup"><span data-stu-id="670b4-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="670b4-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="670b4-123">Minimum supported client</span></span><br/> | <span data-ttu-id="670b4-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="670b4-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="670b4-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="670b4-125">Minimum supported server</span></span><br/> | <span data-ttu-id="670b4-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="670b4-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="670b4-127">Header</span><span class="sxs-lookup"><span data-stu-id="670b4-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="670b4-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="670b4-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="670b4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="670b4-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="670b4-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="670b4-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="670b4-131">**CDM \_ GetFolderPath**</span><span class="sxs-lookup"><span data-stu-id="670b4-131">**CDM\_GETFOLDERPATH**</span></span>](cdm-getfolderpath.md)
</dt> <dt>

[<span data-ttu-id="670b4-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="670b4-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="670b4-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="670b4-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="670b4-134">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="670b4-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="670b4-135">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="670b4-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="670b4-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="670b4-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="670b4-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="670b4-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

