---
title: CDM_GETFOLDERPATH (Commdlg.h)
description: Ruft den Pfad des derzeit geöffneten Ordners oder Verzeichnisses für das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil ab.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- CDM_GETFOLDERPATH meldungsdialogfelder
topic_type:
- apiref
api_name:
- CDM_GETFOLDERPATH
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d96b8d25714dc3f8bdcf016ac1fd69b2af2414f0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550005"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="5ff34-104">CDM \_ GETFOLDERPATH-Nachricht</span><span class="sxs-lookup"><span data-stu-id="5ff34-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="5ff34-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="5ff34-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="5ff34-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="5ff34-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="5ff34-107">Ruft den Pfad des derzeit geöffneten Ordners  oder Verzeichnisses für das Dialogfeld Öffnen oder Speichern unter im **Explorer-Stil** ab.</span><span class="sxs-lookup"><span data-stu-id="5ff34-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="5ff34-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="5ff34-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="5ff34-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ff34-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ff34-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ff34-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ff34-111">Die Größe des *lParam-Puffers* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="5ff34-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5ff34-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ff34-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ff34-113">Ein Zeiger auf den Puffer, der den Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="5ff34-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ff34-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ff34-114">Return value</span></span>

<span data-ttu-id="5ff34-115">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Größe der Pfadzeichenfolge in Zeichen, einschließlich des beendenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="5ff34-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="5ff34-116">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="5ff34-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="5ff34-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="5ff34-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ff34-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ff34-118">Remarks</span></span>

<span data-ttu-id="5ff34-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5ff34-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="5ff34-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ff34-120">Requirements</span></span>



| <span data-ttu-id="5ff34-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ff34-121">Requirement</span></span> | <span data-ttu-id="5ff34-122">Wert</span><span class="sxs-lookup"><span data-stu-id="5ff34-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ff34-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ff34-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ff34-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ff34-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ff34-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ff34-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ff34-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ff34-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ff34-127">Header</span><span class="sxs-lookup"><span data-stu-id="5ff34-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ff34-128"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ff34-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ff34-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ff34-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ff34-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="5ff34-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ff34-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="5ff34-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="5ff34-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="5ff34-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="5ff34-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="5ff34-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="5ff34-134">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="5ff34-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5ff34-135">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="5ff34-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

