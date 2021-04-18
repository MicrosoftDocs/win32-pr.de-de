---
title: CDM_SETCONTROLTEXT Meldung (kommdlg. h)
description: Legt den Text für das angegebene Steuerelement in einem Dialogfeld "Öffnen" oder "Speichern unter" im Explorer-Format fest.
ms.assetid: ff0e50b7-a14d-40d1-8576-f93a612f3aa3
keywords:
- Dialog Felder CDM_SETCONTROLTEXT Meldung
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
ms.openlocfilehash: 87490ba20b5785da4fb9660d97b1b9232d047671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391484"
---
# <a name="cdm_setcontroltext-message"></a><span data-ttu-id="ff05e-104">CDM- \_ setcontroltext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="ff05e-104">CDM\_SETCONTROLTEXT message</span></span>

<span data-ttu-id="ff05e-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="ff05e-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="ff05e-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="ff05e-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="ff05e-107">Legt den Text für das angegebene Steuerelement in einem Dialogfeld " **Öffnen** " oder " **Speichern** unter" im Explorer-Format fest.</span><span class="sxs-lookup"><span data-stu-id="ff05e-107">Sets the text for the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="ff05e-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="ff05e-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETCONTROLTEXT      (CDM_FIRST + 0x0004)
```



## <a name="parameters"></a><span data-ttu-id="ff05e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff05e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff05e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ff05e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff05e-111">Der Bezeichner des Steuer Elements, dessen Text festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ff05e-111">The identifier of the control to whose text is to be set.</span></span>

</dd> <dt>

<span data-ttu-id="ff05e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ff05e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ff05e-113">Der neue Text für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="ff05e-113">The new text for the control.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff05e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff05e-114">Return value</span></span>

<span data-ttu-id="ff05e-115">Diese Meldung gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ff05e-115">This message does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff05e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff05e-116">Remarks</span></span>

<span data-ttu-id="ff05e-117">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="ff05e-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetControlText(hwnd, wparam, lparam)
```

## <a name="requirements"></a><span data-ttu-id="ff05e-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff05e-118">Requirements</span></span>



| <span data-ttu-id="ff05e-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff05e-119">Requirement</span></span> | <span data-ttu-id="ff05e-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ff05e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff05e-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ff05e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ff05e-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff05e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="ff05e-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ff05e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ff05e-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ff05e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ff05e-125">Header</span><span class="sxs-lookup"><span data-stu-id="ff05e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff05e-126"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff05e-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff05e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff05e-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff05e-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ff05e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ff05e-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ff05e-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="ff05e-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="ff05e-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="ff05e-131">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="ff05e-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="ff05e-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="ff05e-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ff05e-133">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff05e-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

