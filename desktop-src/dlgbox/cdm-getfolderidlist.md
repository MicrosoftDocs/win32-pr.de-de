---
title: CDM_GETFOLDERIDLIST Meldung (Commdlg.h)
description: Ruft die Adresse der Elementbezeichnerliste ab, die dem Ordner entspricht, in dem derzeit ein Dialogfeld im Explorer-Stil Geöffnet oder Speichern unter geöffnet ist.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- Dialogfelder für CDM_GETFOLDERIDLIST Meldung
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
ms.openlocfilehash: 24d16b53c90c3efc874b8aeabd1b97938a1b21ec
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590907"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="cae9c-104">CDM \_ GETFOLDERIDLIST-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cae9c-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="cae9c-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="cae9c-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="cae9c-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="cae9c-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="cae9c-107">Ruft die Adresse der Elementbezeichnerliste ab, die dem Ordner entspricht, in dem derzeit ein Dialogfeld im Explorer-Stil **Geöffnet** oder **Speichern unter** geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="cae9c-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="cae9c-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="cae9c-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="cae9c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cae9c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cae9c-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cae9c-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cae9c-111">Die Größe des *lParam-Puffers* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cae9c-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="cae9c-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cae9c-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cae9c-113">Ein Zeiger auf den Puffer, der die Liste der Elementbezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="cae9c-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cae9c-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cae9c-114">Return value</span></span>

<span data-ttu-id="cae9c-115">Wenn die Nachricht erfolgreich ist, entspricht der Rückgabewert der Größe der Liste der Elementbezeichner in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cae9c-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="cae9c-116">Dies ist entweder die Anzahl der in den Puffer kopierten Bytes oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="cae9c-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="cae9c-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="cae9c-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="cae9c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cae9c-118">Remarks</span></span>

<span data-ttu-id="cae9c-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cae9c-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="cae9c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cae9c-120">Requirements</span></span>



| <span data-ttu-id="cae9c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cae9c-121">Requirement</span></span> | <span data-ttu-id="cae9c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="cae9c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cae9c-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cae9c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="cae9c-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae9c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cae9c-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cae9c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="cae9c-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cae9c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cae9c-127">Header</span><span class="sxs-lookup"><span data-stu-id="cae9c-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="cae9c-128"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cae9c-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cae9c-129">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="cae9c-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="cae9c-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cae9c-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cae9c-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="cae9c-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="cae9c-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="cae9c-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="cae9c-133">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="cae9c-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="cae9c-134">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="cae9c-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cae9c-135">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="cae9c-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

