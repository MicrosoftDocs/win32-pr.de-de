---
title: CDN_FILEOK Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche "OK" klickt.
ms.assetid: 7f3de96f-68d8-4f40-b74f-304835f9def2
keywords:
- Dialog Felder für CDN_FILEOK Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_FILEOK
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5aef63d531b603c94369936374bc10531639254
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106343472"
---
# <a name="cdn_fileok-notification-code"></a><span data-ttu-id="b1027-104">CDN- \_ FileOk-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="b1027-104">CDN\_FILEOK notification code</span></span>

<span data-ttu-id="b1027-105">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn der Benutzer einen Dateinamen angibt und auf die Schaltfläche " **OK** " klickt.</span><span class="sxs-lookup"><span data-stu-id="b1027-105">Sent by an Explorer-style **Open** or **Save As** dialog box when the user specifies a file name and clicks the **OK** button.</span></span>

<span data-ttu-id="b1027-106">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="b1027-106">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_FILEOK              (CDN_FIRST - 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="b1027-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1027-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1027-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b1027-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1027-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b1027-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b1027-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b1027-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b1027-111">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b1027-111">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span>

<span data-ttu-id="b1027-112">Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die **CDN \_ FileOk** -Benachrichtigungs Meldung angibt.</span><span class="sxs-lookup"><span data-stu-id="b1027-112">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_FILEOK** notification message.</span></span>

<span data-ttu-id="b1027-113">Die [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur enthält auch einen Zeiger auf eine [**OpenFileName**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) -Struktur, deren **LpstrFile** -Member die Adresse des ausgewählten Datei namens angibt.</span><span class="sxs-lookup"><span data-stu-id="b1027-113">The [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure also contains a pointer to an [**OPENFILENAME**](/windows/win32/api/commdlg/ns-commdlg-openfilenamea) structure whose **lpstrFile** member specifies the address of the selected file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1027-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1027-114">Return value</span></span>

<span data-ttu-id="b1027-115">Wenn die Hook-Prozedur NULL zurückgibt, akzeptiert das Dialogfeld den angegebenen Dateinamen und wird geschlossen.</span><span class="sxs-lookup"><span data-stu-id="b1027-115">If the hook procedure returns zero, the dialog box accepts the specified file name and closes.</span></span>

<span data-ttu-id="b1027-116">Wenn Sie den angegebenen Dateinamen ablehnen und erzwingen möchten, dass das Dialogfeld geöffnet bleibt, geben Sie einen Wert ungleich 0 (null) von der Hookprozedur zurück, und wenden Sie die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion an, um einen **DWL- \_ msgresult** -Wert von</span><span class="sxs-lookup"><span data-stu-id="b1027-116">To reject the specified file name and force the dialog box to remain open, return a nonzero value from the hook procedure and call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function to set a nonzero **DWL\_MSGRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1027-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1027-117">Remarks</span></span>

<span data-ttu-id="b1027-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b1027-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1027-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1027-119">Requirements</span></span>



| <span data-ttu-id="b1027-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1027-120">Requirement</span></span> | <span data-ttu-id="b1027-121">Wert</span><span class="sxs-lookup"><span data-stu-id="b1027-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1027-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1027-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b1027-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1027-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1027-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1027-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b1027-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1027-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b1027-126">Header</span><span class="sxs-lookup"><span data-stu-id="b1027-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1027-127"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b1027-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b1027-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1027-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="b1027-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="b1027-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b1027-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b1027-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="b1027-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="b1027-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="b1027-132">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="b1027-132">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="b1027-133">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="b1027-133">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="b1027-134">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="b1027-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

[<span data-ttu-id="b1027-135">**SetWindowLong**</span><span class="sxs-lookup"><span data-stu-id="b1027-135">**SetWindowLong**</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

<span data-ttu-id="b1027-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="b1027-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b1027-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b1027-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> <dt>

<span data-ttu-id="b1027-138">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="b1027-138">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b1027-139">**WM- \_ Benachrichtigung**</span><span class="sxs-lookup"><span data-stu-id="b1027-139">**WM\_NOTIFY**</span></span>](../controls/wm-notify.md)
</dt> </dl>

 

