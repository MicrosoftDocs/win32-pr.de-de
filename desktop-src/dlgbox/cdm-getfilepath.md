---
title: CDM_GETFILEPATH Meldung (Commdlg.h)
description: Ruft den Pfad und den Dateinamen der ausgewählten Datei im Explorer-Stil im Dialogfeld Öffnen oder Speichern unter ab.
ms.assetid: fad8c5e2-9838-45a8-8c51-4326c989d939
keywords:
- Dialogfelder für CDM_GETFILEPATH Meldung
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
ms.openlocfilehash: 7d531999757d46e127b73584adf1b563e64ea25b
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548665"
---
# <a name="cdm_getfilepath-message"></a><span data-ttu-id="16a18-104">CDM \_ GETFILEPATH-Nachricht</span><span class="sxs-lookup"><span data-stu-id="16a18-104">CDM\_GETFILEPATH message</span></span>

<span data-ttu-id="16a18-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="16a18-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="16a18-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="16a18-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="16a18-107">Ruft den Pfad und den Dateinamen der ausgewählten Datei im Explorer-Stil im Dialogfeld **Öffnen** oder **Speichern unter** ab.</span><span class="sxs-lookup"><span data-stu-id="16a18-107">Retrieves the path and file name of the selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="16a18-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="16a18-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFILEPATH         (CDM_FIRST + 0x0001)
```



## <a name="parameters"></a><span data-ttu-id="16a18-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16a18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16a18-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="16a18-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16a18-111">Die Größe des *lParam-Puffers* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="16a18-111">The size, in characters, of the *lParam* buffer.</span></span> <span data-ttu-id="16a18-112">Für die ANSI-Version ist dies die Anzahl der Bytes. für die Unicode-Version ist dies die Anzahl der Zeichen.</span><span class="sxs-lookup"><span data-stu-id="16a18-112">For the ANSI version, this is the number of bytes; for the Unicode version, this is the number of characters.</span></span>

</dd> <dt>

<span data-ttu-id="16a18-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="16a18-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="16a18-114">Ein Zeiger auf den Puffer, der den Dateinamen und Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="16a18-114">A pointer to the buffer that receives the file name and path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16a18-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16a18-115">Return value</span></span>

<span data-ttu-id="16a18-116">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe des Dateinamens und der Pfadzeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="16a18-116">If the message succeeds, the return value is the size, in characters, of the file name and path string, including the terminating NULL character.</span></span> <span data-ttu-id="16a18-117">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="16a18-117">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="16a18-118">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="16a18-118">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="16a18-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="16a18-119">Remarks</span></span>

<span data-ttu-id="16a18-120">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="16a18-120">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFilePath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="16a18-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16a18-121">Requirements</span></span>



| <span data-ttu-id="16a18-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16a18-122">Requirement</span></span> | <span data-ttu-id="16a18-123">Wert</span><span class="sxs-lookup"><span data-stu-id="16a18-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16a18-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="16a18-124">Minimum supported client</span></span><br/> | <span data-ttu-id="16a18-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16a18-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="16a18-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="16a18-126">Minimum supported server</span></span><br/> | <span data-ttu-id="16a18-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="16a18-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="16a18-128">Header</span><span class="sxs-lookup"><span data-stu-id="16a18-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="16a18-129"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="16a18-129"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16a18-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a18-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="16a18-131">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="16a18-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="16a18-132">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="16a18-132">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="16a18-133">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="16a18-133">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="16a18-134">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="16a18-134">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="16a18-135">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="16a18-135">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="16a18-136">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="16a18-136">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

