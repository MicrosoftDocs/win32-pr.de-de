---
title: LBSELCHSTRING-Nachricht (Commdlg.h)
description: Ein Dialogfeld Öffnen oder Speichern unter sendet die registrierte LBSELCHSTRING-Nachricht an Ihre Hookprozedur, wenn sich die Auswahl in einem der Listenfelder oder Kombinationsfelder des Dialogfelds ändert.
ms.assetid: 3a8ebc63-b324-43ed-bb6f-34779f6043e7
keywords:
- LBSELCHSTRING-Meldungsdialogfelder
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
ms.openlocfilehash: 137429b8fa7eb29fb96ec579e0240c4c282d0766
ms.sourcegitcommit: 8e083a10b3a480dec8a8d74dbd5889f49dea15e4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2021
ms.locfileid: "107590767"
---
# <a name="lbselchstring-message"></a><span data-ttu-id="04417-104">LBSELCHSTRING-Meldung</span><span class="sxs-lookup"><span data-stu-id="04417-104">LBSELCHSTRING message</span></span>

<span data-ttu-id="04417-105">\[Ab Windows Vista wurden  **die** allgemeinen Dialogfelder Öffnen und Speichern unter durch den Allgemeinen [Elementdialog ersetzt.](/windows/win32/shell/common-file-dialog)</span><span class="sxs-lookup"><span data-stu-id="04417-105">\[Starting with Windows Vista, the **Open** and **Save As** common dialog boxes have been superseded by the [Common Item Dialog](/windows/win32/shell/common-file-dialog).</span></span> <span data-ttu-id="04417-106">Es wird empfohlen, anstelle dieser Dialogfelder aus der Common Dialog Box Library die API für den Allgemeinen Elementdialog zu verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="04417-106">We recommended that you use the Common Item Dialog API instead of these dialog boxes from the Common Dialog Box Library.\]</span></span>

<span data-ttu-id="04417-107">In einem  **Dialogfeld** Öffnen oder Speichern unter wird die bei **LBSELCHSTRING** registrierte Meldung an Ihre Hookprozedur gesendet, wenn sich die Auswahl in einem der Listenfelder oder Kombinationsfelder des Dialogfelds ändert.</span><span class="sxs-lookup"><span data-stu-id="04417-107">An **Open** or **Save As** dialog box sends the **LBSELCHSTRING** registered message to your hook procedure when the selection changes in any of the list boxes or combo boxes of the dialog box.</span></span>


```C++
#define LBSELCHSTRING TEXT("commdlg_LBSelChangedNotify")
```



## <a name="parameters"></a><span data-ttu-id="04417-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="04417-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04417-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="04417-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04417-110">Der Bezeichner des Listenfelds oder Kombinationsfelds, in dem die Auswahl geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="04417-110">The identifier of the list box or combo box in which the selection changed.</span></span>

</dd> <dt>

<span data-ttu-id="04417-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="04417-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="04417-112">Das Wort in niedriger Reihenfolge gibt die Elementnummer der ausgewählten Zeichenfolge im Listenfeld oder Kombinationsfeld an.</span><span class="sxs-lookup"><span data-stu-id="04417-112">The low-order word specifies the item number of the selected string in the list box or combo box.</span></span> <span data-ttu-id="04417-113">Das hochgeordnete Wort gibt den Typ der Auswahländerung an.</span><span class="sxs-lookup"><span data-stu-id="04417-113">The high-order word specifies the type of selection change.</span></span> <span data-ttu-id="04417-114">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="04417-114">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="04417-115">Wert</span><span class="sxs-lookup"><span data-stu-id="04417-115">Value</span></span>                                                                                                                                                                                                                       | <span data-ttu-id="04417-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="04417-116">Meaning</span></span>                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span id="CD_LBSELCHANGE"></span><span id="cd_lbselchange"></span><dl> <span data-ttu-id="04417-117"><dt>**CD \_ LBSELCHANGE**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="04417-117"><dt>**CD\_LBSELCHANGE**</dt> <dt>0</dt></span></span> </dl>     | <span data-ttu-id="04417-118">Das Element ist das einzige Element, das in einem Listenfeld mit nur einer Auswahl ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="04417-118">The item is the only item selected in a single-selection list box.</span></span><br/>      |
| <span id="CD_LBSELADD"></span><span id="cd_lbseladd"></span><dl> <span data-ttu-id="04417-119"><dt>**CD \_ LBSELADD**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="04417-119"><dt>**CD\_LBSELADD**</dt> <dt>2</dt></span></span> </dl>              | <span data-ttu-id="04417-120">Das Element ist eines der Elemente, die in einem Mehrfachauswahl-Listenfeld ausgewählt sind.</span><span class="sxs-lookup"><span data-stu-id="04417-120">The item is one of the items selected in a multiple-selection list box.</span></span><br/> |
| <span id="CD_LBSELSUB"></span><span id="cd_lbselsub"></span><dl> <span data-ttu-id="04417-121"><dt>**CD \_ LBSELSUB**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="04417-121"><dt>**CD\_LBSELSUB**</dt> <dt>1</dt></span></span> </dl>              | <span data-ttu-id="04417-122">Das Element wird nicht mehr in einem Mehrfachauswahl-Listenfeld ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="04417-122">The item is no longer selected in a multiple-selection list box.</span></span><br/>        |
| <span id="CD_LBSELNOITEMS"></span><span id="cd_lbselnoitems"></span><dl> <span data-ttu-id="04417-123"><dt>**CD \_ LBSELNOITEMS**</dt> <dt>-1</dt></span><span class="sxs-lookup"><span data-stu-id="04417-123"><dt>**CD\_LBSELNOITEMS**</dt> <dt>-1</dt></span></span> </dl> | <span data-ttu-id="04417-124">In einem Mehrfachauswahllistenfeld sind keine Elemente vorhanden.</span><span class="sxs-lookup"><span data-stu-id="04417-124">No items exist in a multiple-selection list box.</span></span><br/>                        |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04417-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="04417-125">Return value</span></span>

<span data-ttu-id="04417-126">Diese Meldung hat keinen Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="04417-126">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="04417-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="04417-127">Remarks</span></span>

<span data-ttu-id="04417-128">Die Hookprozedur muss die **LBSELCHSTRING-Konstante** in einem Aufruf der [**RegisterWindowMessage-Funktion**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) angeben, um den Bezeichner für die vom Dialogfeld gesendete Nachricht zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="04417-128">The hook procedure must specify the **LBSELCHSTRING** constant in a call to the [**RegisterWindowMessage**](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea) function to get the identifier for the message sent by the dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="04417-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="04417-129">Requirements</span></span>



| <span data-ttu-id="04417-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="04417-130">Requirement</span></span> | <span data-ttu-id="04417-131">Wert</span><span class="sxs-lookup"><span data-stu-id="04417-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="04417-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="04417-132">Minimum supported client</span></span><br/> | <span data-ttu-id="04417-133">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04417-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="04417-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="04417-134">Minimum supported server</span></span><br/> | <span data-ttu-id="04417-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="04417-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="04417-136">Header</span><span class="sxs-lookup"><span data-stu-id="04417-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="04417-137"><dt>Commdlg.h (windows.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="04417-137"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="04417-138">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="04417-138">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="04417-139">**LBSELCHSTRINGW** (Unicode) und **LBSELCHSTRINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="04417-139">**LBSELCHSTRINGW** (Unicode) and **LBSELCHSTRINGA** (ANSI)</span></span><br/>                                    |



## <a name="see-also"></a><span data-ttu-id="04417-140">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="04417-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="04417-141">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="04417-141">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="04417-142">**CDN \_ SELCHANGE**</span><span class="sxs-lookup"><span data-stu-id="04417-142">**CDN\_SELCHANGE**</span></span>](cdn-selchange.md)
</dt> <dt>

[<span data-ttu-id="04417-143">**CDN \_ TYPECHANGE**</span><span class="sxs-lookup"><span data-stu-id="04417-143">**CDN\_TYPECHANGE**</span></span>](cdn-typechange.md)
</dt> <dt>

[<span data-ttu-id="04417-144">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="04417-144">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

<span data-ttu-id="04417-145">**Konzeptionellen**</span><span class="sxs-lookup"><span data-stu-id="04417-145">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="04417-146">Allgemeine Dialogfeldbibliothek</span><span class="sxs-lookup"><span data-stu-id="04417-146">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

