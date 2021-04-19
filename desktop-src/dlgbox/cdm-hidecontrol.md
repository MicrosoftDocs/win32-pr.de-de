---
title: CDM_HIDECONTROL Meldung (kommdlg. h)
description: Blendet das angegebene Steuerelement in einem Dialogfeld zum Öffnen oder speichern unter im Explorer-Format aus.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Dialog Felder CDM_HIDECONTROL Meldung
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff632b7d1e3c24c84f73498846db9e6bfa68fd74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346718"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="88eba-104">CDM- \_ hidecontrol-Meldung</span><span class="sxs-lookup"><span data-stu-id="88eba-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="88eba-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="88eba-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="88eba-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="88eba-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="88eba-107">Blendet das angegebene Steuerelement in einem Dialogfeld zum **Öffnen** oder **Speichern** unter im Explorer-Format aus.</span><span class="sxs-lookup"><span data-stu-id="88eba-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="88eba-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="88eba-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="88eba-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="88eba-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88eba-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="88eba-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88eba-111">Der Bezeichner des Steuer Elements, das ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88eba-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="88eba-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="88eba-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="88eba-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="88eba-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88eba-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="88eba-114">Return value</span></span>

<span data-ttu-id="88eba-115">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="88eba-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="88eba-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88eba-116">Remarks</span></span>

<span data-ttu-id="88eba-117">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="88eba-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="88eba-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88eba-118">Requirements</span></span>



| <span data-ttu-id="88eba-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88eba-119">Requirement</span></span> | <span data-ttu-id="88eba-120">Wert</span><span class="sxs-lookup"><span data-stu-id="88eba-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88eba-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="88eba-121">Minimum supported client</span></span><br/> | <span data-ttu-id="88eba-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88eba-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="88eba-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="88eba-123">Minimum supported server</span></span><br/> | <span data-ttu-id="88eba-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="88eba-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="88eba-125">Header</span><span class="sxs-lookup"><span data-stu-id="88eba-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="88eba-126"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="88eba-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88eba-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88eba-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="88eba-128">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="88eba-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="88eba-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="88eba-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="88eba-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="88eba-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="88eba-131">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="88eba-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="88eba-132">**Licher**</span><span class="sxs-lookup"><span data-stu-id="88eba-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="88eba-133">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="88eba-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

