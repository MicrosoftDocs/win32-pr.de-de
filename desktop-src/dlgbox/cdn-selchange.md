---
title: CDN_SELCHANGE Benachrichtigungscode (Commdlg.h)
description: Wird von einem Dialogfeld im Explorer-Stil geöffnet oder speichern unter gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.
ms.assetid: e622babf-7024-45c5-a8db-f80896f69140
keywords:
- Dialogfelder für CDN_SELCHANGE Benachrichtigungscode
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
ms.openlocfilehash: 8c21aa9dda117c74707b3c890ad96e017b45bcc0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549225"
---
# <a name="cdn_selchange-notification-code"></a><span data-ttu-id="63a2c-104">CDN \_ SELCHANGE-Benachrichtigungscode</span><span class="sxs-lookup"><span data-stu-id="63a2c-104">CDN\_SELCHANGE notification code</span></span>

<span data-ttu-id="63a2c-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="63a2c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="63a2c-106">Es wird empfohlen, die Dialogfeld-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="63a2c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="63a2c-107">Wird von einem Dialogfeld im Explorer-Stil **geöffnet** oder **speichern unter** gesendet, wenn sich die Auswahl im Listenfeld ändert, in dem der Inhalt des aktuell geöffneten Ordners oder Verzeichnisses angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="63a2c-107">Sent by an Explorer-style **Open** or **Save As** dialog box when the selection changes in the list box that displays the contents of the currently opened folder or directory.</span></span>

<span data-ttu-id="63a2c-108">Ihre [*OFNHookProc-Hookprozedur*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) empfängt diese Nachricht in Form einer [**WM \_ NOTIFY-Nachricht.**](../controls/wm-notify.md)</span><span class="sxs-lookup"><span data-stu-id="63a2c-108">Your [*OFNHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc) hook procedure receives this message in the form of a [**WM\_NOTIFY**](../controls/wm-notify.md) message.</span></span>


```C++
#define CDN_SELCHANGE           (CDN_FIRST - 0x0001)
#define CDN_FIRST               (0U-601U)
```



## <a name="parameters"></a><span data-ttu-id="63a2c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63a2c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63a2c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="63a2c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63a2c-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="63a2c-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="63a2c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="63a2c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="63a2c-113">Ein Zeiger auf eine [**OFNOTIFY-Struktur.**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)</span><span class="sxs-lookup"><span data-stu-id="63a2c-113">A pointer to an [**OFNOTIFY**](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya) structure.</span></span> <span data-ttu-id="63a2c-114">Die **OFNOTIFY-Struktur** enthält eine [**NMHDR-Struktur,**](/windows/win32/api/richedit/ns-richedit-nmhdr) deren **Codemember** die **CDN SELCHANGE-Benachrichtigungsmeldung \_** angibt.</span><span class="sxs-lookup"><span data-stu-id="63a2c-114">The **OFNOTIFY** structure contains an [**NMHDR**](/windows/win32/api/richedit/ns-richedit-nmhdr) structure whose **code** member indicates the **CDN\_SELCHANGE** notification message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63a2c-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63a2c-115">Return value</span></span>

<span data-ttu-id="63a2c-116">Der Rückgabewert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="63a2c-116">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="63a2c-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63a2c-117">Remarks</span></span>

<span data-ttu-id="63a2c-118">Das System sendet diese Benachrichtigung nur, wenn das Dialogfeld mit dem **\_ OFN-EXPLORER-Wert** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="63a2c-118">The system sends this notification only if the dialog box was created using the **OFN\_EXPLORER** value.</span></span>

<span data-ttu-id="63a2c-119">Um den Namen der neu ausgewählten Datei oder des ordners abzurufen, kann die Hookprozedur die [**CDM \_ GETFILEPATH-**](cdm-getfilepath.md) oder [**CDM \_ GETSPEC-Nachricht**](cdm-getspec.md) an das Dialogfeld senden.</span><span class="sxs-lookup"><span data-stu-id="63a2c-119">To get the name of the newly selected file or folder, the hook procedure can send the [**CDM\_GETFILEPATH**](cdm-getfilepath.md) or [**CDM\_GETSPEC**](cdm-getspec.md) message to the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="63a2c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63a2c-120">Requirements</span></span>



| <span data-ttu-id="63a2c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63a2c-121">Requirement</span></span> | <span data-ttu-id="63a2c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="63a2c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63a2c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="63a2c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="63a2c-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63a2c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="63a2c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="63a2c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="63a2c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="63a2c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="63a2c-127">Header</span><span class="sxs-lookup"><span data-stu-id="63a2c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="63a2c-128"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="63a2c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63a2c-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63a2c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="63a2c-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="63a2c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="63a2c-131">**CDM \_ GETFILEPATH**</span><span class="sxs-lookup"><span data-stu-id="63a2c-131">**CDM\_GETFILEPATH**</span></span>](cdm-getfilepath.md)
</dt> <dt>

[<span data-ttu-id="63a2c-132">**CDM \_ GETSPEC**</span><span class="sxs-lookup"><span data-stu-id="63a2c-132">**CDM\_GETSPEC**</span></span>](cdm-getspec.md)
</dt> <dt>

[<span data-ttu-id="63a2c-133">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="63a2c-133">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="63a2c-134">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="63a2c-134">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="63a2c-135">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="63a2c-135">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
</dt> <dt>

[<span data-ttu-id="63a2c-136">**OFNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="63a2c-136">**OFNOTIFY**</span></span>](/windows/desktop/api/Commdlg/ns-commdlg-ofnotifya)
</dt> <dt>

<span data-ttu-id="63a2c-137">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="63a2c-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="63a2c-138">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="63a2c-138">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

