---
title: CDM_SETDEFEXT Meldung (kommdlg. h)
description: Legt die standardmäßige Dateinamenerweiterung für ein Dialogfeld "Öffnen" oder "Speichern unter" im Explorer-Format fest.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Dialog Felder CDM_SETDEFEXT Meldung
topic_type:
- apiref
api_name:
- CDM_SETDEFEXT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd722a5ae172e06879ae9aaafadc5180ee77867e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040861"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="353bb-104">CDM- \_ setdefext-Nachricht</span><span class="sxs-lookup"><span data-stu-id="353bb-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="353bb-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="353bb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="353bb-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="353bb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="353bb-107">Legt die standardmäßige Dateinamenerweiterung für ein Dialogfeld " **Öffnen** " oder " **Speichern** unter" im Explorer-Format fest.</span><span class="sxs-lookup"><span data-stu-id="353bb-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="353bb-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="353bb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="353bb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="353bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="353bb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="353bb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="353bb-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="353bb-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="353bb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="353bb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="353bb-113">Ein Zeiger auf die neue Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="353bb-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="353bb-114">Der Punkt (.) darf nicht enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="353bb-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="353bb-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="353bb-115">Return value</span></span>

<span data-ttu-id="353bb-116">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="353bb-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="353bb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="353bb-117">Remarks</span></span>

<span data-ttu-id="353bb-118">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="353bb-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="353bb-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="353bb-119">Requirements</span></span>



| <span data-ttu-id="353bb-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="353bb-120">Requirement</span></span> | <span data-ttu-id="353bb-121">Wert</span><span class="sxs-lookup"><span data-stu-id="353bb-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="353bb-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="353bb-122">Minimum supported client</span></span><br/> | <span data-ttu-id="353bb-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="353bb-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="353bb-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="353bb-124">Minimum supported server</span></span><br/> | <span data-ttu-id="353bb-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="353bb-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="353bb-126">Header</span><span class="sxs-lookup"><span data-stu-id="353bb-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="353bb-127"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="353bb-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="353bb-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="353bb-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="353bb-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="353bb-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="353bb-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="353bb-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="353bb-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="353bb-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="353bb-132">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="353bb-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="353bb-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="353bb-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="353bb-134">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="353bb-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

