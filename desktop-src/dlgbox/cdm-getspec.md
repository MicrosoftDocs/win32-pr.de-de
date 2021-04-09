---
title: CDM_GETSPEC Meldung (kommdlg. h)
description: Ruft den Dateinamen (ohne den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld "Öffnen" oder "Speichern unter" im Explorer-Format ab.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Dialog Felder CDM_GETSPEC Meldung
topic_type:
- apiref
api_name:
- CDM_GETSPEC
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2732bf2a8c581439a40538445853531b57cfc77a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102779"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="2b5e9-104">CDM- \_ getSpec-Nachricht</span><span class="sxs-lookup"><span data-stu-id="2b5e9-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="2b5e9-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="2b5e9-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="2b5e9-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2b5e9-107">Ruft den Dateinamen (ohne den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld " **Öffnen** " oder "Speichern unter" im Explorer-Format **ab** .</span><span class="sxs-lookup"><span data-stu-id="2b5e9-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="2b5e9-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="2b5e9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2b5e9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2b5e9-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2b5e9-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b5e9-111">Die Größe des *LPARAM* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="2b5e9-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2b5e9-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2b5e9-113">Ein Zeiger auf den Puffer, der den Dateinamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2b5e9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2b5e9-114">Return value</span></span>

<span data-ttu-id="2b5e9-115">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Größe (in Zeichen) der Dateiname-Zeichenfolge, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="2b5e9-116">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="2b5e9-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="2b5e9-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2b5e9-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b5e9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2b5e9-118">Remarks</span></span>

<span data-ttu-id="2b5e9-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2b5e9-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="2b5e9-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2b5e9-120">Requirements</span></span>



| <span data-ttu-id="2b5e9-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2b5e9-121">Requirement</span></span> | <span data-ttu-id="2b5e9-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2b5e9-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b5e9-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2b5e9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2b5e9-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b5e9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b5e9-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2b5e9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2b5e9-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2b5e9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b5e9-127">Header</span><span class="sxs-lookup"><span data-stu-id="2b5e9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b5e9-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b5e9-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b5e9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b5e9-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="2b5e9-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2b5e9-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2b5e9-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="2b5e9-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="2b5e9-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="2b5e9-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="2b5e9-133">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="2b5e9-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="2b5e9-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2b5e9-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2b5e9-135">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2b5e9-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

