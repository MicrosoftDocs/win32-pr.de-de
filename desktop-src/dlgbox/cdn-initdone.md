---
title: CDN_INITDONE Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld im Explorer-Stil geöffnet oder speichern unter gesendet, wenn das System die Anordnung der Steuerelemente im Dialogfeld abgeschlossen hat. Das System verschiebt die Standardsteuerelemente, um Platz für die Steuerelemente des untergeordneten Dialogfelds zu schaffen.
ms.assetid: 337fccac-5444-442d-92f0-862c5302fa21
keywords:
- Dialogfelder für CDN_INITDONE Benachrichtigungscode
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
ms.openlocfilehash: 5b07c25183eced86c3a430621091bed74c53f90d
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590797"
---
# <a name="cdn_initdone-notification-code"></a><span data-ttu-id="1a62c-105">CDN \_ INITDONE-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="1a62c-105">CDN\_INITDONE notification code</span></span>

<span data-ttu-id="1a62c-106">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1a62c-106">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="1a62c-107">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-107">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="1a62c-108">Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn das System die Anordnung der Steuerelemente im Dialogfeld abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="1a62c-108">Sent by an Explorer-style **Open** or **Save As** dialog box when the system has finished arranging the controls in the dialog box.</span></span> <span data-ttu-id="1a62c-109">Das System verschiebt die Standardsteuerelemente, um Platz für die Steuerelemente des untergeordneten Dialogfelds zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="1a62c-109">The system moves the standard controls to make room for the controls of the child dialog box.</span></span>

<span data-ttu-id="1a62c-110">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="1a62c-110">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_FIRST               (0U-601U)
#define CDN_INITDONE            (CDN_FIRST - 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="1a62c-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a62c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a62c-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a62c-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a62c-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1a62c-113">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a62c-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a62c-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a62c-115">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="1a62c-115">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="1a62c-116">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN \_ INITDONE-Benachrichtigungsmeldung** angibt.</span><span class="sxs-lookup"><span data-stu-id="1a62c-116">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_INITDONE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a62c-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a62c-117">Return value</span></span>

<span data-ttu-id="1a62c-118">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1a62c-118">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a62c-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a62c-119">Remarks</span></span>

<span data-ttu-id="1a62c-120">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1a62c-120">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a62c-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a62c-121">Requirements</span></span>



| <span data-ttu-id="1a62c-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a62c-122">Requirement</span></span> | <span data-ttu-id="1a62c-123">Wert</span><span class="sxs-lookup"><span data-stu-id="1a62c-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a62c-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1a62c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1a62c-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1a62c-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1a62c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1a62c-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1a62c-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a62c-128">Header</span><span class="sxs-lookup"><span data-stu-id="1a62c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a62c-129"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="1a62c-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a62c-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1a62c-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a62c-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="1a62c-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a62c-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="1a62c-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="1a62c-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="1a62c-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="1a62c-134">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="1a62c-134">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="1a62c-135">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="1a62c-135">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

[<span data-ttu-id="1a62c-136">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="1a62c-136">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="1a62c-137">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="1a62c-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a62c-138">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="1a62c-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

