---
title: CDM_GETFOLDERPATH Meldung (Commdlg.h)
description: Ruft den Pfad des derzeit geöffneten Ordners oder Verzeichnisses für das Dialogfeld Öffnen oder Speichern unter im Explorer-Stil ab.
ms.assetid: 7c3d4598-b45d-46c1-ad0d-cb0ecd20b3eb
keywords:
- Dialogfelder für CDM_GETFOLDERPATH Meldung
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
ms.openlocfilehash: fdd6a824892b1a3a31339e36e6a783bb00c08534
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590937"
---
# <a name="cdm_getfolderpath-message"></a><span data-ttu-id="416ae-104">CDM \_ GETFOLDERPATH-Nachricht</span><span class="sxs-lookup"><span data-stu-id="416ae-104">CDM\_GETFOLDERPATH message</span></span>

<span data-ttu-id="416ae-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="416ae-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="416ae-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="416ae-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="416ae-107">Ruft den Pfad des derzeit geöffneten Ordners oder Verzeichnisses für das Dialogfeld **Öffnen** oder **Speichern unter** im Explorer-Stil ab.</span><span class="sxs-lookup"><span data-stu-id="416ae-107">Retrieves the path of the currently open folder or directory for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="416ae-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="416ae-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERPATH       (CDM_FIRST + 0x0002)
```



## <a name="parameters"></a><span data-ttu-id="416ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="416ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="416ae-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="416ae-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="416ae-111">Die Größe des *lParam-Puffers* in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="416ae-111">The size, in characters, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="416ae-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="416ae-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="416ae-113">Ein Zeiger auf den Puffer, der den Pfad empfängt.</span><span class="sxs-lookup"><span data-stu-id="416ae-113">A pointer to the buffer that receives the path.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="416ae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="416ae-114">Return value</span></span>

<span data-ttu-id="416ae-115">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe der Pfadzeichenfolge in Zeichen, einschließlich des abschließenden NULL-Zeichens.</span><span class="sxs-lookup"><span data-stu-id="416ae-115">If the message succeeds, the return value is the size, in characters, of the path string, including the terminating null character.</span></span> <span data-ttu-id="416ae-116">Dies ist entweder die Anzahl von Bytes oder Zeichen, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="416ae-116">This is either the number of bytes or characters copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="416ae-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="416ae-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="416ae-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="416ae-118">Remarks</span></span>

<span data-ttu-id="416ae-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="416ae-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderPath(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="416ae-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="416ae-120">Requirements</span></span>



| <span data-ttu-id="416ae-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="416ae-121">Requirement</span></span> | <span data-ttu-id="416ae-122">Wert</span><span class="sxs-lookup"><span data-stu-id="416ae-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="416ae-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="416ae-123">Minimum supported client</span></span><br/> | <span data-ttu-id="416ae-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="416ae-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="416ae-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="416ae-125">Minimum supported server</span></span><br/> | <span data-ttu-id="416ae-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="416ae-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="416ae-127">Header</span><span class="sxs-lookup"><span data-stu-id="416ae-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="416ae-128"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="416ae-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="416ae-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="416ae-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="416ae-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="416ae-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="416ae-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="416ae-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="416ae-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="416ae-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="416ae-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="416ae-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="416ae-134">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="416ae-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="416ae-135">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="416ae-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

