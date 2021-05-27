---
title: CDM_GETSPEC Nachricht (Commdlg.h)
description: Ruft den Dateinamen (ohne Den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld im Explorer-Stil open or Save As (Öffnen oder Speichern unter) ab.
ms.assetid: 22a67c92-bd24-4cba-bef8-291d241e6ec8
keywords:
- Dialogfelder für CDM_GETSPEC Meldung
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
ms.openlocfilehash: 27eff7e9a14f39554fa6c1a69846bbaca7c39990
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548875"
---
# <a name="cdm_getspec-message"></a><span data-ttu-id="98846-104">CDM \_ GETSPEC-Nachricht</span><span class="sxs-lookup"><span data-stu-id="98846-104">CDM\_GETSPEC message</span></span>

<span data-ttu-id="98846-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="98846-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="98846-106">Es wird empfohlen, die Dialogfeld-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="98846-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="98846-107">Ruft den Dateinamen (ohne den Pfad) der aktuell ausgewählten Datei in einem Dialogfeld im Explorer-Stil open or Save As **(Öffnen** oder **Speichern unter)** ab.</span><span class="sxs-lookup"><span data-stu-id="98846-107">Retrieves the file name (not including the path) of the currently selected file in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="98846-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="98846-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETSPEC             (CDM_FIRST + 0x0000)
```



## <a name="parameters"></a><span data-ttu-id="98846-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="98846-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98846-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98846-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98846-111">Die Größe des *lParam-Puffers* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="98846-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="98846-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98846-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98846-113">Ein Zeiger auf den Puffer, der den Dateinamen empfängt.</span><span class="sxs-lookup"><span data-stu-id="98846-113">A pointer to the buffer that receives the file name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98846-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98846-114">Return value</span></span>

<span data-ttu-id="98846-115">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe der Dateinamenzeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="98846-115">If the message succeeds, the return value is the size, in characters, of the file name string, including the terminating NULL character.</span></span> <span data-ttu-id="98846-116">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="98846-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="98846-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="98846-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="98846-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="98846-118">Remarks</span></span>

<span data-ttu-id="98846-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="98846-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetSpec(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="98846-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98846-120">Requirements</span></span>



| <span data-ttu-id="98846-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98846-121">Requirement</span></span> | <span data-ttu-id="98846-122">Wert</span><span class="sxs-lookup"><span data-stu-id="98846-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98846-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98846-123">Minimum supported client</span></span><br/> | <span data-ttu-id="98846-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98846-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98846-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98846-125">Minimum supported server</span></span><br/> | <span data-ttu-id="98846-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98846-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98846-127">Header</span><span class="sxs-lookup"><span data-stu-id="98846-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="98846-128"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="98846-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98846-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98846-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="98846-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="98846-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98846-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="98846-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="98846-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="98846-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="98846-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="98846-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="98846-134">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="98846-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98846-135">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="98846-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

