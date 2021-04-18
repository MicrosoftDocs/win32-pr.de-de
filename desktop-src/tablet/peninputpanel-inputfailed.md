---
description: Veraltet. Der "tzinputpanel" wurde durch den Text Eingabe Panel (Tip) ersetzt. Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt "pinputpanel" Benutzereingaben in das angefügte Steuerelement einfügen konnte.
ms.assetid: a5928f78-29d6-40e8-8f87-17c188e51ba9
title: Das Ereignis "pinputpanel. InputFailed" (msink AUT. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 198c2b466dc03357d9851d7c8a6b7f44c6bf6884
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352775"
---
# <a name="peninputpanelinputfailed-event"></a><span data-ttu-id="3e2af-104">"Pinputpanel. InputFailed"-Ereignis</span><span class="sxs-lookup"><span data-stu-id="3e2af-104">PenInputPanel.InputFailed event</span></span>

<span data-ttu-id="3e2af-105">Veraltet.</span><span class="sxs-lookup"><span data-stu-id="3e2af-105">Deprecated.</span></span> <span data-ttu-id="3e2af-106">Der " [**tzinputpanel**](peninputpanel-class.md) " wurde durch den [Text Eingabe Panel (Tip)](text-input-panel-reference.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="3e2af-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="3e2af-107">Tritt auf, wenn sich der Eingabefokus ändert, bevor das Objekt " [**pinputpanel**](peninputpanel-class.md) " Benutzereingaben in das angefügte Steuerelement einfügen konnte.</span><span class="sxs-lookup"><span data-stu-id="3e2af-107">Occurs when input focus changes before the [**PenInputPanel**](peninputpanel-class.md) object was able to insert user input into the attached control.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e2af-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e2af-108">Syntax</span></span>


```C++
HRESULT InputFailed(
  [in] long  hWnd,
  [in] long  Key,
  [in] BSTR  Text,
  [in] short ShiftKey
);
```



## <a name="parameters"></a><span data-ttu-id="3e2af-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e2af-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3e2af-110">*HWND* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e2af-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2af-111">Das Fenster Handle des Steuer Elements [**, das das Objekt "**](peninputpanel-class.md) " mit dem Objekt "-Objekt" aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="3e2af-111">The window handle of the control that invoked the [**PenInputPanel**](peninputpanel-class.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="3e2af-112">*Schlüssel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e2af-112">*Key* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2af-113">Der virtuelle Schlüssel, der dem gedrückten Schlüssel entspricht.</span><span class="sxs-lookup"><span data-stu-id="3e2af-113">The virtual key corresponding to the key pressed.</span></span>

</dd> <dt>

<span data-ttu-id="3e2af-114">*Text* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e2af-114">*Text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2af-115">Die Zeichenfolge, die in das Steuerelement eingefügt werden soll, das durch den *HWND* -Parameter dargestellt wird, als das **InputFailed** -Ereignis ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="3e2af-115">The string that was to be inserted into the control represented by the *hWnd* parameter when the **InputFailed** event was raised.</span></span>

<span data-ttu-id="3e2af-116">Weitere Informationen zum BSTR-Datentyp finden Sie unter [Verwenden der com-Bibliothek](using-the-com-library.md).</span><span class="sxs-lookup"><span data-stu-id="3e2af-116">For more information about the BSTR data type, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> <dt>

<span data-ttu-id="3e2af-117">*ShiftKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3e2af-117">*ShiftKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3e2af-118">Der Zustand der Tastatur modifiziererer, einschließlich Shift, Caps, STRG und alt.</span><span class="sxs-lookup"><span data-stu-id="3e2af-118">The state of the keyboard modifiers, including SHIFT, CAPS, CTRL, and ALT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3e2af-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3e2af-119">Return value</span></span>

<span data-ttu-id="3e2af-120">Wenn dieses Ereignis erfolgreich ist, gibt es " **S \_ OK**" zurück.</span><span class="sxs-lookup"><span data-stu-id="3e2af-120">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3e2af-121">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e2af-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e2af-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e2af-122">Remarks</span></span>

<span data-ttu-id="3e2af-123">Das **InputFailed** -Ereignis tritt auf, wenn sich der Eingabefokus ändert, bevor Benutzereingaben in das angefügte Steuerelement eingefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="3e2af-123">The **InputFailed** event occurs when input focus changes before user input was inserted into the attached control.</span></span> <span data-ttu-id="3e2af-124">Wenn der Benutzer z. b. Freihand in den Schreib-Pad eingibt und dann auf ein anderes Bearbeitungs Steuerelement tippt, bevor die Erkennung abgeschlossen werden konnte, wird dieses Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="3e2af-124">For example, if the user enters ink into the writing pad, then taps on another edit control before the recognizer has had a chance to finish, this event fires.</span></span>

<span data-ttu-id="3e2af-125">Wenn Sie das Fenster Handle verwenden, das an dieses Ereignis übermittelt wurde, können Sie den Text selbst einfügen, wenn dieses Ereignis auftritt.</span><span class="sxs-lookup"><span data-stu-id="3e2af-125">Using the window handle passed into this event, you can choose to insert the text yourself when this event occurs.</span></span>

> [!Note]  
> <span data-ttu-id="3e2af-126">Ab Microsoft Windows XP Tablet PC Edition 2005 gilt das Ereignis " **InputFailed** " nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="3e2af-126">Starting with Microsoft Windows XP Tablet PC Edition 2005, the **InputFailed** event no longer applies.</span></span> <span data-ttu-id="3e2af-127">Text wird immer eingefügt, bevor der Fokus geändert wird.</span><span class="sxs-lookup"><span data-stu-id="3e2af-127">Text is always inserted before focus changes.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e2af-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3e2af-128">Requirements</span></span>



| <span data-ttu-id="3e2af-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3e2af-129">Requirement</span></span> | <span data-ttu-id="3e2af-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3e2af-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e2af-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3e2af-131">Minimum supported client</span></span><br/> | <span data-ttu-id="3e2af-132">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3e2af-132">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="3e2af-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3e2af-133">Minimum supported server</span></span><br/> | <span data-ttu-id="3e2af-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3e2af-134">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="3e2af-135">Header</span><span class="sxs-lookup"><span data-stu-id="3e2af-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e2af-136"><dt>Msink AUT. h (erfordert auch msink AUT \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="3e2af-136"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="3e2af-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3e2af-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="3e2af-138"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3e2af-138"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="3e2af-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e2af-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e2af-140">**"Pendel Panel"**</span><span class="sxs-lookup"><span data-stu-id="3e2af-140">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




