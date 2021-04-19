---
title: CDM_SETDEFEXT Nachricht (Commdlg.h)
description: Legt die Standarddateinamenerweiterung für ein Dialogfeld im Explorer-Stil "Öffnen" oder "Speichern unter" fest.
ms.assetid: bd4999f1-0a7e-4b7f-a0ba-a7c2a7f196c6
keywords:
- Dialogfelder für CDM_SETDEFEXT Meldung
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
ms.openlocfilehash: 1bd5706e0bccf0b61c0737ef54d6e227e5593bc9
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590857"
---
# <a name="cdm_setdefext-message"></a><span data-ttu-id="2f345-104">CDM \_ SETDEFEXT-Meldung</span><span class="sxs-lookup"><span data-stu-id="2f345-104">CDM\_SETDEFEXT message</span></span>

<span data-ttu-id="2f345-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](/windows/win32/shell/common-file-dialog)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="2f345-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="2f345-106">Es wird empfohlen, die DIALOGFELD-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="2f345-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="2f345-107">Legt die Standarddateinamenerweiterung für ein Dialogfeld im Explorer-Stil **"Öffnen"** oder **"Speichern** unter" fest.</span><span class="sxs-lookup"><span data-stu-id="2f345-107">Sets the default file name extension for an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="2f345-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="2f345-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_SETDEFEXT           (CDM_FIRST + 0x0006)
```



## <a name="parameters"></a><span data-ttu-id="2f345-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2f345-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f345-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2f345-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f345-111">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2f345-111">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2f345-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2f345-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2f345-113">Ein Zeiger auf die neue Dateinamenerweiterung.</span><span class="sxs-lookup"><span data-stu-id="2f345-113">A pointer to the new file name extension.</span></span> <span data-ttu-id="2f345-114">Darf den Punkt (.) nicht enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f345-114">Must not include the dot (.).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f345-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2f345-115">Return value</span></span>

<span data-ttu-id="2f345-116">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="2f345-116">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f345-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2f345-117">Remarks</span></span>

<span data-ttu-id="2f345-118">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2f345-118">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_SetDefExt(hwnd, lparam)
```

## <a name="requirements"></a><span data-ttu-id="2f345-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2f345-119">Requirements</span></span>



| <span data-ttu-id="2f345-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2f345-120">Requirement</span></span> | <span data-ttu-id="2f345-121">Wert</span><span class="sxs-lookup"><span data-stu-id="2f345-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f345-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2f345-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2f345-123">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f345-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2f345-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2f345-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2f345-125">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2f345-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2f345-126">Header</span><span class="sxs-lookup"><span data-stu-id="2f345-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f345-127"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="2f345-127"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f345-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="2f345-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="2f345-129">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2f345-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2f345-130">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="2f345-130">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="2f345-131">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="2f345-131">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="2f345-132">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="2f345-132">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="2f345-133">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="2f345-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2f345-134">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="2f345-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

