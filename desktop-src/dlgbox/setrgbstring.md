---
title: Abmeldung von "sstrgbstring" (kommdlg. h)
description: Die Hook-Prozedur eines Farb Dialogfelds, cchookproc, kann die registrierte setrgbstring-Meldung an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.
ms.assetid: 02d36248-be75-4552-853f-6ac3ec034ebe
keywords:
- Dialog Felder "mestrgbstring"
topic_type:
- apiref
api_name:
- SETRGBSTRING
- SETRGBSTRINGA
- SETRGBSTRINGW
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dea5489aaa6fafcaa19a97a44d81fd85abb178d2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742585"
---
# <a name="setrgbstring-message"></a><span data-ttu-id="2dee1-104">"Abmeldung"</span><span class="sxs-lookup"><span data-stu-id="2dee1-104">SETRGBSTRING message</span></span>

<span data-ttu-id="2dee1-105">Die Hook-Prozedur eines **Farb** Dialogfelds, [*cchookproc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), kann die registrierte **setrgbstring** -Meldung an das Dialogfeld senden, um die aktuelle Farbauswahl festzulegen.</span><span class="sxs-lookup"><span data-stu-id="2dee1-105">The hook procedure of a **Color** dialog box, [*CCHookProc*](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc), can send the **SETRGBSTRING** registered message to the dialog box to set the current color selection.</span></span>


```C++
#define SETRGBSTRING TEXT("commdlg_SetRGBColor")
```



## <a name="parameters"></a><span data-ttu-id="2dee1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dee1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dee1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2dee1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dee1-108">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dee1-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="2dee1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2dee1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2dee1-110">Der RGB-Wert der Farbe, die im Dialogfeld **Farbe** ausgewählt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dee1-110">The RGB value of the color to select in the **Color** dialog box.</span></span> <span data-ttu-id="2dee1-111">Sie können das [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) -Makro verwenden, um die roten, grünen und blauen Intensitäten eines RGB-Farbwerts anzugeben.</span><span class="sxs-lookup"><span data-stu-id="2dee1-111">You can use the [**RGB**](/windows/desktop/api/wingdi/nf-wingdi-rgb) macro to specify the red, green, and blue intensities of an RGB color value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dee1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2dee1-112">Return value</span></span>

<span data-ttu-id="2dee1-113">Diese Nachricht weist keinen Rückgabewert auf.</span><span class="sxs-lookup"><span data-stu-id="2dee1-113">This message has no return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dee1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dee1-114">Remarks</span></span>

<span data-ttu-id="2dee1-115">Wenn *LPARAM* mit einer der Grundfarben oder einer der 16 benutzerdefinierten Farben übereinstimmt, wählt die Dialogfeld Prozedur diese Farbe aus.</span><span class="sxs-lookup"><span data-stu-id="2dee1-115">If *lParam* matches one of the basic colors or one of the 16 custom colors, the dialog box procedure selects that color.</span></span> <span data-ttu-id="2dee1-116">Die Dialogfeld Prozedur aktualisiert auch alle Steuerelemente in der benutzerdefinierten Farb Erweiterung des Dialog Felds **Farbe** , wenn Sie geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="2dee1-116">The dialog box procedure also updates all the controls in the custom color extension of the **Color** dialog box, if it is open.</span></span>

<span data-ttu-id="2dee1-117">Wenn *LPARAM* nicht mit einer einfachen oder benutzerdefinierten Farbe identisch ist, ändert die Dialogfeld Prozedur nicht die aktuelle Farbauswahl, sondern aktualisiert die benutzerdefinierten Farb Steuerelemente, wenn Sie sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="2dee1-117">If *lParam* does not match a basic or custom color, the dialog box procedure does not change the current color selection, but it does update the custom color controls, if they are visible.</span></span>

## <a name="examples"></a><span data-ttu-id="2dee1-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2dee1-118">Examples</span></span>

<span data-ttu-id="2dee1-119">Im folgenden Beispielcode wird der **setrgbstring** -Nachrichten Bezeichner abgerufen und anschließend die Farbauswahl auf Blau festgelegt.</span><span class="sxs-lookup"><span data-stu-id="2dee1-119">The following sample code gets the **SETRGBSTRING** message identifier and then sets the color selection to blue.</span></span>


```
UINT uiSetRGB;

uiSetRGB = RegisterWindowMessage(SETRGBSTRING);

SendMessage(hdlg, uiSetRGB, 0, (LPARAM) RGB(0, 0, 255)); 
```



## <a name="requirements"></a><span data-ttu-id="2dee1-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2dee1-120">Requirements</span></span>



| <span data-ttu-id="2dee1-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2dee1-121">Requirement</span></span> | <span data-ttu-id="2dee1-122">Wert</span><span class="sxs-lookup"><span data-stu-id="2dee1-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2dee1-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2dee1-123">Minimum supported client</span></span><br/> | <span data-ttu-id="2dee1-124">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dee1-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2dee1-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2dee1-125">Minimum supported server</span></span><br/> | <span data-ttu-id="2dee1-126">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2dee1-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2dee1-127">Header</span><span class="sxs-lookup"><span data-stu-id="2dee1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="2dee1-128"><dt>Kommdlg. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2dee1-128"><dt>Commdlg.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2dee1-129">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="2dee1-129">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="2dee1-130">" **Btrgbstringw** (Unicode) **" und "** ABl" (ANSI)</span><span class="sxs-lookup"><span data-stu-id="2dee1-130">**SETRGBSTRINGW** (Unicode) and **SETRGBSTRINGA** (ANSI)</span></span><br/>                                      |



## <a name="see-also"></a><span data-ttu-id="2dee1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dee1-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="2dee1-132">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="2dee1-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="2dee1-133">**RegisterWindowMessage**</span><span class="sxs-lookup"><span data-stu-id="2dee1-133">**RegisterWindowMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerwindowmessagea)
</dt> <dt>

[<span data-ttu-id="2dee1-134">**RGB**</span><span class="sxs-lookup"><span data-stu-id="2dee1-134">**RGB**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-rgb)
</dt> <dt>

[<span data-ttu-id="2dee1-135">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="2dee1-135">**SendMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

<span data-ttu-id="2dee1-136">**Licher**</span><span class="sxs-lookup"><span data-stu-id="2dee1-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2dee1-137">Allgemeine Dialog Feld Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2dee1-137">Common Dialog Box Library</span></span>](common-dialog-box-library.md)
</dt> </dl>

 

