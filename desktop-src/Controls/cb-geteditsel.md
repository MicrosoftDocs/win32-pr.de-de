---
title: CB_GETEDITSEL Meldung (Winuser. h)
description: Ruft die Position des Anfangs-und des Endzeichens der aktuellen Auswahl im Bearbeitungs Steuerelement eines Kombinations Felds ab.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- Windows-Steuerelemente für CB_GETEDITSEL Meldung
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 319ce4a3c7a5a61903d4fc3bf04eed223e749787
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040605"
---
# <a name="cb_geteditsel-message"></a><span data-ttu-id="6e09a-104">CB \_ geteditsel-Meldung</span><span class="sxs-lookup"><span data-stu-id="6e09a-104">CB\_GETEDITSEL message</span></span>

<span data-ttu-id="6e09a-105">Ruft die Position des Anfangs-und des Endzeichens der aktuellen Auswahl im Bearbeitungs Steuerelement eines Kombinations Felds ab.</span><span class="sxs-lookup"><span data-stu-id="6e09a-105">Gets the starting and ending character positions of the current selection in the edit control of a combo box.</span></span>

## <a name="parameters"></a><span data-ttu-id="6e09a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e09a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e09a-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6e09a-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e09a-108">Ein Zeiger auf einen **DWORD** -Wert, der die Anfangsposition der Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="6e09a-108">A pointer to a **DWORD** value that receives the starting position of the selection.</span></span> <span data-ttu-id="6e09a-109">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="6e09a-109">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6e09a-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6e09a-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6e09a-111">Ein Zeiger auf einen **DWORD** -Wert, der die Endposition der Auswahl empfängt.</span><span class="sxs-lookup"><span data-stu-id="6e09a-111">A pointer to a **DWORD** value that receives the ending position of the selection.</span></span> <span data-ttu-id="6e09a-112">Dieser Parameter kann **NULL** sein.</span><span class="sxs-lookup"><span data-stu-id="6e09a-112">This parameter can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e09a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e09a-113">Return value</span></span>

<span data-ttu-id="6e09a-114">Der Rückgabewert ist ein NULL basierter **DWORD** -Wert mit der Anfangsposition der Auswahl im [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) und mit der Endposition des ersten Zeichens nach dem letzten ausgewählten Zeichen im [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="6e09a-114">The return value is a zero-based **DWORD** value with the starting position of the selection in the [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) and with the ending position of the first character after the last selected character in the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).</span></span>

## <a name="examples"></a><span data-ttu-id="6e09a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6e09a-115">Examples</span></span>

<span data-ttu-id="6e09a-116">Das folgende Codebeispiel zeigt zwei Möglichkeiten, den aktuellen Auswahlbereich abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e09a-116">The following code example shows two ways of retrieving the current selection range.</span></span>


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a><span data-ttu-id="6e09a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e09a-117">Requirements</span></span>



| <span data-ttu-id="6e09a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e09a-118">Requirement</span></span> | <span data-ttu-id="6e09a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="6e09a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e09a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6e09a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6e09a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e09a-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="6e09a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6e09a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6e09a-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6e09a-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6e09a-124">Header</span><span class="sxs-lookup"><span data-stu-id="6e09a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e09a-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="6e09a-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e09a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e09a-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6e09a-127">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="6e09a-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6e09a-128">**CB- \_ Sekunden**</span><span class="sxs-lookup"><span data-stu-id="6e09a-128">**CB\_SETEDITSEL**</span></span>](cb-seteditsel.md)
</dt> <dt>

<span data-ttu-id="6e09a-129">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="6e09a-129">**Other Resources**</span></span>
</dt> <dt>

<span data-ttu-id="6e09a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e09a-130">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6e09a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6e09a-131">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> </dl>

 

