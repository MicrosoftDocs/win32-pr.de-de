---
title: Colorokstring-Nachricht (kommdlg. h)
description: Ein Farb Dialogfeld sendet die registrierte colorokstring-Nachricht an die Hook-Prozedur cchookproc, wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche OK klickt.
ms.assetid: 18b28558-1262-4c88-becf-76ce799b7542
keywords:
- Colorokstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- COLOROKSTRING
- COLOROKSTRINGA
- COLOROKSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86229c71f1234efb4b561ac73bc8aa20f6258cdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103647"
---
# <a name="colorokstring-message"></a><span data-ttu-id="cea71-104">Colorokstring-Meldung</span><span class="sxs-lookup"><span data-stu-id="cea71-104">COLOROKSTRING message</span></span>

<span data-ttu-id="cea71-105">Ein **Farb** Dialogfeld sendet die registrierte **colorokstring** -Nachricht an die Hook-Prozedur [*cchookproc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), wenn der Benutzer eine Farbe auswählt und auf die Schaltfläche **OK** klickt.</span><span class="sxs-lookup"><span data-stu-id="cea71-105">A **Color** dialog box sends the **COLOROKSTRING** registered message to your hook procedure, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), when the user selects a color and clicks the **OK** button.</span></span> <span data-ttu-id="cea71-106">Die Hook-Prozedur kann die Farbe annehmen und zulassen, dass das Dialogfeld geschlossen wird, oder die Farbe ablehnen und erzwingen, dass das Dialogfeld geöffnet bleibt.</span><span class="sxs-lookup"><span data-stu-id="cea71-106">The hook procedure can accept the color and allow the dialog box to close, or reject the color and force the dialog box to remain open.</span></span>


```C++
#define COLOROKSTRING TEXT("commdlg_ColorOK")
```



## <a name="parameters"></a><span data-ttu-id="cea71-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cea71-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cea71-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cea71-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cea71-109">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cea71-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="cea71-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cea71-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cea71-111">Ein Zeiger auf eine [**chooon Color**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="cea71-111">A pointer to a [**CHOOSECOLOR**](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1) structure.</span></span> <span data-ttu-id="cea71-112">Der **rgbresult** -Member dieser Struktur enthält den RGB-Farbwert der ausgewählten Farbe.</span><span class="sxs-lookup"><span data-stu-id="cea71-112">The **rgbResult** member of this structure contains the RGB color value of the selected color.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cea71-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cea71-113">Return value</span></span>

<span data-ttu-id="cea71-114">Wenn die Hook-Prozedur 0 (null) zurückgibt, wird das Dialogfeld **Farbe** die ausgewählte Farbe annehmen und geschlossen.</span><span class="sxs-lookup"><span data-stu-id="cea71-114">If the hook procedure returns zero, the **Color** dialog box accepts the selected color and closes.</span></span>

<span data-ttu-id="cea71-115">Wenn die Hook-Prozedur einen Wert ungleich 0 (null) zurückgibt, lehnt das Dialogfeld **Farbe** die ausgewählte Farbe ab und bleibt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="cea71-115">If the hook procedure returns a nonzero value, the **Color** dialog box rejects the selected color and remains open.</span></span>

## <a name="remarks"></a><span data-ttu-id="cea71-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cea71-116">Remarks</span></span>

<span data-ttu-id="cea71-117">Die Hook-Prozedur muss die **colorokstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner der vom Dialogfeld gesendeten Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cea71-117">The hook procedure must specify the **COLOROKSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier of the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="cea71-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cea71-118">Requirements</span></span>



| <span data-ttu-id="cea71-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cea71-119">Requirement</span></span> | <span data-ttu-id="cea71-120">Wert</span><span class="sxs-lookup"><span data-stu-id="cea71-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cea71-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cea71-121">Minimum supported client</span></span><br/> | <span data-ttu-id="cea71-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea71-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cea71-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cea71-123">Minimum supported server</span></span><br/> | <span data-ttu-id="cea71-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cea71-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cea71-125">Header</span><span class="sxs-lookup"><span data-stu-id="cea71-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="cea71-126"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cea71-126"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="cea71-127">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="cea71-127">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="cea71-128">**Colorokstringw** (Unicode) und **colorokstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="cea71-128">**COLOROKSTRINGW** (Unicode) and **COLOROKSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="cea71-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cea71-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="cea71-130">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cea71-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cea71-131">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="cea71-131">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
</dt> <dt>

[<span data-ttu-id="cea71-132">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="cea71-132">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="cea71-133">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cea71-133">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cea71-134">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cea71-134">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

