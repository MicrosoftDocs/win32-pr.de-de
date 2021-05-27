---
title: CDM_GETFOLDERIDLIST (Commdlg.h)
description: Ruft die Adresse der Elementbezeichnerliste ab, die dem Ordner entspricht, der derzeit im Dialogfeld Öffnen oder Speichern im Explorer-Stil geöffnet ist.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- CDM_GETFOLDERIDLIST-Dialogfelder
topic_type:
- apiref
api_name:
- CDM_GETFOLDERIDLIST
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb3ffff4f80dc21ed685e589ed4780b43592c2d2
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549705"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="28f35-104">CDM \_ GETFOLDERIDLIST-Nachricht</span><span class="sxs-lookup"><span data-stu-id="28f35-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="28f35-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](../shell/common-file-dialog.md)</span><span class="sxs-lookup"><span data-stu-id="28f35-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="28f35-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="28f35-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="28f35-107">Ruft die Adresse der Elementbezeichnerliste ab, die  dem Ordner entspricht, der derzeit im Dialogfeld Öffnen oder Speichern **im** Explorer-Stil geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="28f35-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="28f35-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="28f35-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="28f35-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="28f35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28f35-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="28f35-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28f35-111">Die Größe des *lParam-Puffers* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="28f35-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="28f35-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="28f35-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="28f35-113">Ein Zeiger auf den Puffer, der die Liste der Elementbezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="28f35-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28f35-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28f35-114">Return value</span></span>

<span data-ttu-id="28f35-115">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe der Liste der Elementbezeichner in Bytes.</span><span class="sxs-lookup"><span data-stu-id="28f35-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="28f35-116">Dies ist entweder die Anzahl der in den Puffer kopierten Bytes oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="28f35-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="28f35-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="28f35-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="28f35-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="28f35-118">Remarks</span></span>

<span data-ttu-id="28f35-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="28f35-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="28f35-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28f35-120">Requirements</span></span>



| <span data-ttu-id="28f35-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28f35-121">Requirement</span></span> | <span data-ttu-id="28f35-122">Wert</span><span class="sxs-lookup"><span data-stu-id="28f35-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28f35-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28f35-123">Minimum supported client</span></span><br/> | <span data-ttu-id="28f35-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28f35-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="28f35-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28f35-125">Minimum supported server</span></span><br/> | <span data-ttu-id="28f35-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28f35-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="28f35-127">Header</span><span class="sxs-lookup"><span data-stu-id="28f35-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="28f35-128"><dt>Commdlg.h (einschließlich Windows.h)</dt></span><span class="sxs-lookup"><span data-stu-id="28f35-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="28f35-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28f35-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="28f35-130">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="28f35-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="28f35-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="28f35-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="28f35-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="28f35-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="28f35-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="28f35-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="28f35-134">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="28f35-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="28f35-135">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="28f35-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

