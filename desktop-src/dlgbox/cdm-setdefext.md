---
title: CDM_SETDEFEXT (Commdlg.h)
description: Legt die Standarddateinamenerweiterung für das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil fest.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- CDM_SETDEFEXT meldungsdialogfelder
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
ms.openlocfilehash: 0b0b1169a2777d5a5f82925366c6723af741706d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550115"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="375a3-104">CDM \_ SETDEFEXT-Nachricht</span><span class="sxs-lookup"><span data-stu-id="375a3-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="375a3-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="375a3-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="375a3-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="375a3-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="375a3-107">Legt die Standarddateinamenerweiterung für  das Dialogfeld Öffnen oder Speichern unter im **Explorer-Stil** fest.</span><span class="sxs-lookup"><span data-stu-id="375a3-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="375a3-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="375a3-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="375a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="375a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375a3-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="375a3-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375a3-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="375a3-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="375a3-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="375a3-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="375a3-113">Ein Zeiger auf die neue Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="375a3-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="375a3-114">Darf den Punkt (.) nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="375a3-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375a3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="375a3-115">Return value</span></span>

<span data-ttu-id="375a3-116">Diese Meldung hat keinen Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="375a3-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="375a3-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="375a3-117">Remarks</span></span>

<span data-ttu-id="375a3-118">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="375a3-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="375a3-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="375a3-119">Requirements</span></span>



| <span data-ttu-id="375a3-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="375a3-120">Requirement</span></span> | <span data-ttu-id="375a3-121">Wert</span><span class="sxs-lookup"><span data-stu-id="375a3-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375a3-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="375a3-122">Minimum supported client</span></span><br/> | <span data-ttu-id="375a3-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="375a3-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="375a3-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="375a3-124">Minimum supported server</span></span><br/> | <span data-ttu-id="375a3-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="375a3-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="375a3-126">Header</span><span class="sxs-lookup"><span data-stu-id="375a3-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="375a3-127"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="375a3-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375a3-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="375a3-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="375a3-129">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="375a3-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="375a3-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="375a3-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="375a3-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="375a3-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="375a3-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="375a3-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="375a3-133">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="375a3-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="375a3-134">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="375a3-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

