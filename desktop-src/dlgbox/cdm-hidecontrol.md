---
title: CDM_HIDECONTROL Meldung (Commdlg.h)
description: Blendet das angegebene Steuerelement im Explorer-Stil im Dialogfeld Öffnen oder Speichern unter aus.
ms.assetid: 5bf7f861-d38c-491a-89f0-5b3dfce8abfc
keywords:
- Dialogfelder für CDM_HIDECONTROL Meldung
topic_type:
- apiref
api_name:
- CDM_HIDECONTROL
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21f1a5a7a1830ceeb2c3671b0dfb538ad89e0a58
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110548655"
---
# <a name="cdm_hidecontrol-message"></a><span data-ttu-id="f74bb-104">CDM \_ HIDECONTROL-Nachricht</span><span class="sxs-lookup"><span data-stu-id="f74bb-104">CDM\_HIDECONTROL message</span></span>

<span data-ttu-id="f74bb-105">\[Ab Windows Vista wurden die Dialogfelder **Öffnen** und **Speichern unter** allgemein durch das [Dialogfeld "Allgemeines Element"](../shell/common-file-dialog.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="f74bb-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](../shell/common-file-dialog.md).</span></span> <span data-ttu-id="f74bb-106">Es wird empfohlen, die Dialogfeld-API für allgemeine Elemente anstelle dieser Dialogfelder aus der Common Dialog Box Library zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="f74bb-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="f74bb-107">Blendet das angegebene Steuerelement im Explorer-Stil im Dialogfeld **Öffnen** oder **Speichern unter** aus.</span><span class="sxs-lookup"><span data-stu-id="f74bb-107">Hides the specified control in an Explorer-style **Open** or **Save As** dialog box.</span></span> <span data-ttu-id="f74bb-108">Das Dialogfeld muss mit dem **\_ OFN-EXPLORER-Flag** erstellt worden sein. Andernfalls schlägt die Meldung fehl.</span><span class="sxs-lookup"><span data-stu-id="f74bb-108">The dialog box must have been created with the **OFN\_EXPLORER** flag; otherwise, the message fails.</span></span>


```C++
#define WM_USER                  0x0400
#define CDM_FIRST               (WM_USER + 100)
#define CDM_HIDECONTROL         (CDM_FIRST + 0x0005)
```



## <a name="parameters"></a><span data-ttu-id="f74bb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f74bb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f74bb-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f74bb-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f74bb-111">Der Bezeichner des steuerelements, das ausgeblendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f74bb-111">The identifier of the control to be hidden.</span></span>

</dd> <dt>

<span data-ttu-id="f74bb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f74bb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f74bb-113">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f74bb-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f74bb-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f74bb-114">Return value</span></span>

<span data-ttu-id="f74bb-115">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="f74bb-115">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f74bb-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f74bb-116">Remarks</span></span>

<span data-ttu-id="f74bb-117">Das entsprechende Makro lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f74bb-117">The corresponding macro is as follows:</span></span>

``` syntax
void CommDlg_OpenSave_HideControl(hwnd, wparam);
```

## <a name="requirements"></a><span data-ttu-id="f74bb-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f74bb-118">Requirements</span></span>



| <span data-ttu-id="f74bb-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f74bb-119">Requirement</span></span> | <span data-ttu-id="f74bb-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f74bb-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f74bb-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f74bb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f74bb-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f74bb-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f74bb-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f74bb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f74bb-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f74bb-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f74bb-125">Header</span><span class="sxs-lookup"><span data-stu-id="f74bb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f74bb-126"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="f74bb-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f74bb-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f74bb-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="f74bb-128">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="f74bb-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f74bb-129">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="f74bb-129">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
</dt> <dt>

[<span data-ttu-id="f74bb-130">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="f74bb-130">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
</dt> <dt>

[<span data-ttu-id="f74bb-131">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="f74bb-131">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
</dt> <dt>

<span data-ttu-id="f74bb-132">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="f74bb-132">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f74bb-133">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="f74bb-133">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

