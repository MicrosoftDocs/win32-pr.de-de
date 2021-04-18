---
title: Lbselchstring-Nachricht (kommdlg. h)
description: Ein Dialogfeld zum Öffnen oder speichern unter sendet die registrierte lbselchstring-Nachricht an die Hook-Prozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinations Felder des Dialog Felds ändert.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- Lbselchstring-Meldungs Dialogfelder
topic_type:
- apiref
api_name:
- LBSELCHSTRING
- LBSELCHSTRINGA
- LBSELCHSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14538c429bf943e4557974166bd7da747176bd93
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341008"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="a8109-104">Lbselchstring-Nachricht</span><span class="sxs-lookup"><span data-stu-id="a8109-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="a8109-105">\[Ab Windows Vista wurden die Dialogfelder " **Öffnen** " und " **Speichern** unter" im allgemeinen [Element](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85))ersetzt.</span><span class="sxs-lookup"><span data-stu-id="a8109-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/previous-versions/windows/desktop/legacy/bb776913(v=vs.85)).</span></span> <span data-ttu-id="a8109-106">Es wird empfohlen, dass Sie die allgemeine Element Dialogfeld-API anstelle dieser Dialogfelder aus der allgemeinen Dialogfeld Bibliothek verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="a8109-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="a8109-107">Ein Dialogfeld zum **Öffnen** oder **Speichern** unter sendet die registrierte **lbselchstring** -Nachricht an die Hook-Prozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinations Felder des Dialog Felds ändert.</span><span class="sxs-lookup"><span data-stu-id="a8109-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="a8109-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8109-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8109-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a8109-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8109-110">Der Bezeichner für das Listenfeld oder Kombinations Feld, in dem die Auswahl geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="a8109-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="a8109-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a8109-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a8109-112">Das nieder wertige Wort gibt die Element Nummer der ausgewählten Zeichenfolge im Listenfeld oder Kombinations Feld an.</span><span class="sxs-lookup"><span data-stu-id="a8109-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="a8109-113">Das höchst wertige Wort gibt den Typ der Auswahl Änderung an.</span><span class="sxs-lookup"><span data-stu-id="a8109-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="a8109-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="a8109-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="a8109-115">Wert</span><span class="sxs-lookup"><span data-stu-id="a8109-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="a8109-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a8109-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="a8109-117"><dt>**CD \_ Lbselchange**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a8109-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="a8109-118">Das Element ist das einzige Element, das in einem einfach Auswahl-Listenfeld ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="a8109-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="a8109-119"><dt>**CD \_ Lbseladd**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a8109-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="a8109-120">Das Element ist eines der Elemente, die in einem Listenfeld für Mehrfachauswahl ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="a8109-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="a8109-121"><dt>**CD \_ Lbselsub**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a8109-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="a8109-122">Das Element ist nicht mehr in einem Listenfeld Mehrfachauswahl ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a8109-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="a8109-123"><dt>**CD \_ Lbselnoitems**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="a8109-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="a8109-124">In einem Listenfeld mit Mehrfachauswahl sind keine Elemente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a8109-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8109-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8109-125">Return value</span></span>

<span data-ttu-id="a8109-126">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="a8109-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8109-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8109-127">Remarks</span></span>

<span data-ttu-id="a8109-128">Die Hook-Prozedur muss die **lbselchstring** -Konstante in einem Aufrufen der [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) -Funktion angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a8109-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8109-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8109-129">Requirements</span></span>



| <span data-ttu-id="a8109-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8109-130">Requirement</span></span> | <span data-ttu-id="a8109-131">Wert</span><span class="sxs-lookup"><span data-stu-id="a8109-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8109-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a8109-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a8109-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8109-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a8109-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a8109-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a8109-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a8109-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="a8109-136">Header</span><span class="sxs-lookup"><span data-stu-id="a8109-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8109-137"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a8109-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a8109-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="a8109-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a8109-139">**Lbselchstringw** (Unicode) und **lbselchstraninga** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a8109-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="a8109-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8109-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8109-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="a8109-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="a8109-142">**CDN \_ selChange**</span><span class="sxs-lookup"><span data-stu-id="a8109-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="a8109-143">**CDN- \_ Typänderung**</span><span class="sxs-lookup"><span data-stu-id="a8109-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="a8109-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="a8109-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="a8109-145">**Licher**</span><span class="sxs-lookup"><span data-stu-id="a8109-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8109-146">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a8109-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

