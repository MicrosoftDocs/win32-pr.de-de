---
title: CDM_GETFILEPATH Meldung (kommdlg. h)
description: Ruft den Pfad und den Dateinamen der ausgewählten Datei in einem Dialogfeld "Öffnen" oder "Speichern unter" im Explorer-Format ab.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Dialog Felder CDM_GETFILEPATH Meldung
topic_type:
- apiref
api_name:
- CDM_GETFILEPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b7cc278d1d5a2305b3d2a311ce9c82886f9b7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956944"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="a8d8d-104">CDM \_ GetFilePath-Meldung</span><span class="sxs-lookup"><span data-stu-id="a8d8d-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="a8d8d-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="a8d8d-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="a8d8d-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a8d8d-107">Ruft den Pfad und den Dateinamen der ausgewählten Datei in einem Dialogfeld " **Öffnen** " oder "Speichern unter" im Explorer-Format **ab** .</span><span class="sxs-lookup"><span data-stu-id="a8d8d-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="a8d8d-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="a8d8d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8d8d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8d8d-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8d8d-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d8d-111">Die Größe des *LPARAM* -Puffers in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="a8d8d-112">Bei der ANSI-Version ist dies die Anzahl der Bytes. bei der Unicode-Version ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="a8d8d-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8d8d-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8d8d-114">Ein Zeiger auf den Puffer, der den Dateinamen und den Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8d8d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8d8d-115">Return value</span></span>

<span data-ttu-id="a8d8d-116">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe (in Zeichen) des Datei namens und der Pfad Zeichenfolge, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="a8d8d-117">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="a8d8d-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="a8d8d-118">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a8d8d-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8d8d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8d8d-119">Remarks</span></span>

<span data-ttu-id="a8d8d-120">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="a8d8d-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="a8d8d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8d8d-121">Requirements</span></span>



| <span data-ttu-id="a8d8d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8d8d-122">Requirement</span></span> | <span data-ttu-id="a8d8d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a8d8d-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8d8d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8d8d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a8d8d-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8d8d-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8d8d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8d8d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a8d8d-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8d8d-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8d8d-128">Header</span><span class="sxs-lookup"><span data-stu-id="a8d8d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8d8d-129"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8d8d-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8d8d-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8d8d-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8d8d-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a8d8d-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8d8d-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a8d8d-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="a8d8d-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="a8d8d-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="a8d8d-134">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="a8d8d-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="a8d8d-135">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a8d8d-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8d8d-136">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8d8d-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

