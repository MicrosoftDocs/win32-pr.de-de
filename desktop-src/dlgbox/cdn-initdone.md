---
title: CDN_INITDONE Benachrichtigungs Code (kommdlg. h)
description: Wird von einem Explorer-Dialogfeld "Öffnen" oder "Speichern unter" gesendet, wenn das System das Anordnen der Steuerelemente im Dialogfeld abgeschlossen hat. Das System verschiebt die Standard Steuerelemente, um Platz für die Steuerelemente des untergeordneten Dialog Felds zu schaffen.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- Dialog Felder für CDN_INITDONE Benachrichtigungs Code
topic_type:
- apiref
api_name:
- CDN_INITDONE
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e6d51f1c34a0a399775e1786356aae4fc6526fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391907"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="0bc70-105">CDN- \_ initdone-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="0bc70-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="0bc70-106">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="0bc70-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="0bc70-107">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="0bc70-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="0bc70-108">Wird von einem Explorer-Dialogfeld " **Öffnen** " oder " **Speichern** unter" gesendet, wenn das System das Anordnen der Steuerelemente im Dialogfeld abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="0bc70-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="0bc70-109">Das System verschiebt die Standard Steuerelemente, um Platz für die Steuerelemente des untergeordneten Dialog Felds zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="0bc70-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="0bc70-110">Die [*ofnhuokproc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) -Hook-Prozedur empfängt diese Nachricht in Form einer [**WM- \_ Benachrichtigungs**](../controls/wm-notify.md) Meldung.</span><span class="sxs-lookup"><span data-stu-id="0bc70-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="0bc70-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bc70-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bc70-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0bc70-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc70-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="0bc70-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0bc70-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0bc70-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0bc70-115">Ein Zeiger auf eine [**ofnotify**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0bc70-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="0bc70-116">Die **ofnotify** -Struktur enthält eine [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) -Struktur, deren **Codemember** die CDN-Benachrichtigungs Meldung " **\_ initdone** " angibt.</span><span class="sxs-lookup"><span data-stu-id="0bc70-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bc70-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0bc70-117">Return value</span></span>

<span data-ttu-id="0bc70-118">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0bc70-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="0bc70-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0bc70-119">Remarks</span></span>

<span data-ttu-id="0bc70-120">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem Wert des **ofn- \_ Explorers** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0bc70-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bc70-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0bc70-121">Requirements</span></span>



| <span data-ttu-id="0bc70-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0bc70-122">Requirement</span></span> | <span data-ttu-id="0bc70-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0bc70-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0bc70-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0bc70-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0bc70-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bc70-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0bc70-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0bc70-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0bc70-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0bc70-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0bc70-128">Header</span><span class="sxs-lookup"><span data-stu-id="0bc70-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bc70-129"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0bc70-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bc70-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0bc70-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="0bc70-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="0bc70-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0bc70-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="0bc70-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="0bc70-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="0bc70-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="0bc70-134">*Ofnhuokproc*</span><span class="sxs-lookup"><span data-stu-id="0bc70-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="0bc70-135">**Ofnotify**</span><span class="sxs-lookup"><span data-stu-id="0bc70-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="0bc70-136">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="0bc70-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="0bc70-137">**Licher**</span><span class="sxs-lookup"><span data-stu-id="0bc70-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0bc70-138">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0bc70-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

