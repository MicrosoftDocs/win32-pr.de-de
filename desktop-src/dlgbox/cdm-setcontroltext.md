---
title: CDM_SETCONTROLTEXT (Commdlg.h)
description: Legt den Text für das angegebene Steuerelement im Dialogfeld Öffnen oder Speichern unter im Explorer-Stil fest.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- CDM_SETCONTROLTEXT Meldungsdialogfelder
topic_type:
- apiref
api_name:
- CDM_SETCONTROLTEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89c82a9144717224871caecf44da352a4e01cac2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550125"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="7e786-104">CDM \_ SETCONTROLTEXT-Meldung</span><span class="sxs-lookup"><span data-stu-id="7e786-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="7e786-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="7e786-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="7e786-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="7e786-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="7e786-107">Legt den Text für das angegebene  Steuerelement im Dialogfeld Öffnen oder Speichern unter im **Explorer-Stil** fest.</span><span class="sxs-lookup"><span data-stu-id="7e786-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="7e786-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="7e786-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="7e786-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e786-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e786-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7e786-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e786-111">Der Bezeichner des Steuerelements, auf dessen Text festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e786-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="7e786-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7e786-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7e786-113">Der neue Text für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7e786-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e786-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7e786-114">Return value</span></span>

<span data-ttu-id="7e786-115">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7e786-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e786-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7e786-116">Remarks</span></span>

<span data-ttu-id="7e786-117">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7e786-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="7e786-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7e786-118">Requirements</span></span>



| <span data-ttu-id="7e786-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7e786-119">Requirement</span></span> | <span data-ttu-id="7e786-120">Wert</span><span class="sxs-lookup"><span data-stu-id="7e786-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e786-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7e786-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7e786-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e786-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7e786-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7e786-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7e786-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7e786-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7e786-125">Header</span><span class="sxs-lookup"><span data-stu-id="7e786-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e786-126"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7e786-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e786-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e786-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e786-128">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="7e786-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7e786-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="7e786-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="7e786-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="7e786-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="7e786-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="7e786-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="7e786-132">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="7e786-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7e786-133">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="7e786-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

