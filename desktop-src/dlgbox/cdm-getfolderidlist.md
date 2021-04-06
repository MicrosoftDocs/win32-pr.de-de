---
title: CDM_GETFOLDERIDLIST Meldung (kommdlg. h)
description: Ruft die Adresse der Element Bezeichner-Liste ab, die dem Ordner entspricht, der im Dialogfeld Explorer-Stil öffnen oder speichern unter geöffnet ist.
ms.assetid: 9d2d2c35-ff1d-43de-ab0b-c96e0f1e9e24
keywords:
- Dialog Felder CDM_GETFOLDERIDLIST Meldung
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
ms.openlocfilehash: 0b4ac82a628d6fcace6863abb30e5703af02a948
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743208"
---
# <a name="cdm_getfolderidlist-message"></a><span data-ttu-id="696bd-104">CDM \_ getfolderidlist-Meldung</span><span class="sxs-lookup"><span data-stu-id="696bd-104">CDM\_GETFOLDERIDLIST message</span></span>

<span data-ttu-id="696bd-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="696bd-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="696bd-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="696bd-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="696bd-107">Ruft die Adresse der Element Bezeichner-Liste ab, die dem Ordner entspricht, der im Dialogfeld Explorer-Stil **Öffnen** oder **Speichern** unter geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="696bd-107">Retrieves the address of the item identifier list corresponding to the folder that an Explorer-style **Open** or **Save As** dialog box currently has open.</span></span> <span data-ttu-id="696bd-108">Das Dialogfeld muss mit dem **ofn- \_ Explorer** -Flag erstellt worden sein. andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="696bd-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_GETFOLDERIDLIST     (CDM_FIRST + 0x0003)
```



## <a name="parameters"></a><span data-ttu-id="696bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="696bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="696bd-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="696bd-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="696bd-111">Die Größe des *LPARAM* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="696bd-111">The size, in bytes, of the *lParam* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="696bd-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="696bd-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="696bd-113">Ein Zeiger auf den Puffer, der die Liste der Element Bezeichner empfängt.</span><span class="sxs-lookup"><span data-stu-id="696bd-113">A pointer to the buffer that receives the list of item identifiers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="696bd-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="696bd-114">Return value</span></span>

<span data-ttu-id="696bd-115">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert die Größe (in Bytes) der Liste der Element Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="696bd-115">If the message succeeds, the return value is the size, in bytes, of the list of item identifiers.</span></span> <span data-ttu-id="696bd-116">Dies ist entweder die Anzahl der Bytes, die in den Puffer kopiert werden, oder die erforderliche Puffergröße, wenn der Puffer zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="696bd-116">This is either the number of bytes copied to the buffer, or the required buffer size if the buffer is too small.</span></span>

<span data-ttu-id="696bd-117">Wenn ein Fehler auftritt, ist der Rückgabewert kleiner als 0 (null).</span><span class="sxs-lookup"><span data-stu-id="696bd-117">If an error occurs, the return value is less than zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="696bd-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="696bd-118">Remarks</span></span>

<span data-ttu-id="696bd-119">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="696bd-119">The corresponding macro is as follows:</span></span>

``` syntax
int CommDlg_OpenSave_GetFolderIDList(hwnd, lparam, wparam); 
```

## <a name="requirements"></a><span data-ttu-id="696bd-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="696bd-120">Requirements</span></span>



| <span data-ttu-id="696bd-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="696bd-121">Requirement</span></span> | <span data-ttu-id="696bd-122">Wert</span><span class="sxs-lookup"><span data-stu-id="696bd-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="696bd-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="696bd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="696bd-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="696bd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="696bd-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="696bd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="696bd-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="696bd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="696bd-127">Header</span><span class="sxs-lookup"><span data-stu-id="696bd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="696bd-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="696bd-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="696bd-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="696bd-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="696bd-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="696bd-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="696bd-131">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="696bd-131">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="696bd-132">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="696bd-132">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="696bd-133">**OpenFileName**</span><span class="sxs-lookup"><span data-stu-id="696bd-133">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="696bd-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="696bd-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="696bd-135">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="696bd-135">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

