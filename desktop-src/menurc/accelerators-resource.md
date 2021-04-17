---
title: Accelerators-Ressource
description: Definiert einen oder mehrere Acceleratoren für eine Anwendung. Eine Zugriffstaste ist eine von der Anwendung definierte Tastatureingabe, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Ressourcen Menüs und andere Ressourcen für Accelerators
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516751"
---
# <a name="accelerators-resource"></a><span data-ttu-id="bd93a-105">Accelerators-Ressource</span><span class="sxs-lookup"><span data-stu-id="bd93a-105">ACCELERATORS resource</span></span>

<span data-ttu-id="bd93a-106">Definiert einen oder mehrere Acceleratoren für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bd93a-106">Defines one or more accelerators for an application.</span></span> <span data-ttu-id="bd93a-107">Eine Zugriffstaste ist eine von der Anwendung definierte Tastatureingabe, um dem Benutzer eine schnelle Möglichkeit zum Ausführen einer Aufgabe zu geben.</span><span class="sxs-lookup"><span data-stu-id="bd93a-107">An accelerator is a keystroke defined by the application to give the user a quick way to perform a task.</span></span>

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a><span data-ttu-id="bd93a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd93a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd93a-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span><span class="sxs-lookup"><span data-stu-id="bd93a-109"><span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-110">Eindeutiger Name oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bd93a-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="bd93a-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="bd93a-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-112">NULL oder mehr der folgenden Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="bd93a-112">Zero or more of the following statements.</span></span>



| <span data-ttu-id="bd93a-113">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="bd93a-113">Statement</span></span>                                                        | <span data-ttu-id="bd93a-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd93a-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd93a-115">[**Merkmale**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="bd93a-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="bd93a-116">Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="bd93a-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="bd93a-117">Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="bd93a-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="bd93a-118">[**Sprach**](language-statement.md) *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="bd93a-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="bd93a-119">Gibt die Sprache für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="bd93a-119">Specifies the language for the resource.</span></span> <span data-ttu-id="bd93a-120">Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="bd93a-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="bd93a-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="bd93a-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="bd93a-122">Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="bd93a-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="bd93a-123">Weitere Informationen finden Sie unter [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="bd93a-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="bd93a-124"><span id="event"></span><span id="EVENT"></span>*Veranstalter*</span><span class="sxs-lookup"><span data-stu-id="bd93a-124"><span id="event"></span><span id="EVENT"></span>*event*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-125">Tastatureingabe, die als Zugriffstaste verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd93a-125">Keystroke to be used as an accelerator.</span></span> <span data-ttu-id="bd93a-126">Dabei kann es sich um einen der folgenden Zeichen Typen handeln:</span><span class="sxs-lookup"><span data-stu-id="bd93a-126">It can be any one of the following character types.</span></span>



| <span data-ttu-id="bd93a-127">type</span><span class="sxs-lookup"><span data-stu-id="bd93a-127">Type</span></span>                    | <span data-ttu-id="bd93a-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd93a-128">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd93a-129">"*char*"</span><span class="sxs-lookup"><span data-stu-id="bd93a-129">"*char*"</span></span>                | <span data-ttu-id="bd93a-130">Ein einzelnes Zeichen, das in doppelte Anführungszeichen (") eingeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bd93a-130">A single character enclosed in double quotation marks (").</span></span> <span data-ttu-id="bd93a-131">Dem Zeichen kann ein Caretzeichen (^) vorangestellt werden, was bedeutet, dass das Zeichen ein Steuerzeichen ist.</span><span class="sxs-lookup"><span data-stu-id="bd93a-131">The character can be preceded by a caret (^), meaning that the character is a control character.</span></span>                                                                                  |
| <span data-ttu-id="bd93a-132">*Zeichen*</span><span class="sxs-lookup"><span data-stu-id="bd93a-132">*Character*</span></span>             | <span data-ttu-id="bd93a-133">Ein ganzzahliger Wert, der ein Zeichen darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd93a-133">An integer value representing a character.</span></span> <span data-ttu-id="bd93a-134">Der *Typparameter* muss **ASCII** sein.</span><span class="sxs-lookup"><span data-stu-id="bd93a-134">The *type* parameter must be **ASCII**.</span></span>                                                                                                                                                           |
| <span data-ttu-id="bd93a-135">*virtuelles Schlüsselzeichen*</span><span class="sxs-lookup"><span data-stu-id="bd93a-135">*virtual-key character*</span></span> | <span data-ttu-id="bd93a-136">Ein ganzzahliger Wert, der einen virtuellen Schlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="bd93a-136">An integer value representing a virtual key.</span></span> <span data-ttu-id="bd93a-137">Der virtuelle Schlüssel für alphanumerische Schlüssel kann angegeben werden, indem der Großbuchstabe oder die Zahl in doppelte Anführungszeichen (z. b. "9" oder "C") platziert wird.</span><span class="sxs-lookup"><span data-stu-id="bd93a-137">The virtual key for alphanumeric keys can be specified by placing the uppercase letter or number in double quotation marks (for example, "9" or "C").</span></span> <span data-ttu-id="bd93a-138">Der *Typparameter* muss " **VIRTKEY**" lauten.</span><span class="sxs-lookup"><span data-stu-id="bd93a-138">The *type* parameter must be **VIRTKEY**.</span></span> |



 

</dd> <dt>

<span data-ttu-id="bd93a-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span><span class="sxs-lookup"><span data-stu-id="bd93a-139"><span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-140">ein 16-Bit-Ganzzahl-Wert ohne Vorzeichen, der die Zugriffstaste identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bd93a-140">a 16-bit unsigned integer value that identifies the accelerator.</span></span>

</dd> <dt>

<span data-ttu-id="bd93a-141"><span id="type"></span><span id="TYPE"></span>*Sorte*</span><span class="sxs-lookup"><span data-stu-id="bd93a-141"><span id="type"></span><span id="TYPE"></span>*type*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-142">Nur erforderlich, wenn der *Ereignis* Parameter ein *Zeichen* oder ein *Virtuelles Schlüsselzeichen* ist.</span><span class="sxs-lookup"><span data-stu-id="bd93a-142">Required only when the *event* parameter is a *character* or a *virtual-key character*.</span></span> <span data-ttu-id="bd93a-143">Der *Typparameter* gibt entweder **ASCII** oder **VIRTKEY** an. der ganzzahlige Wert des *Ereignisses* wird entsprechend interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bd93a-143">The *type* parameter specifies either **ASCII** or **VIRTKEY**; the integer value of *event* is interpreted accordingly.</span></span> <span data-ttu-id="bd93a-144">Wenn **VIRTKEY** angegeben wird und das *Ereignis* eine Zeichenfolge enthält, muss das *Ereignis* in Großbuchstaben angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bd93a-144">When **VIRTKEY** is specified and *event* contains a string, *event* must be uppercase.</span></span>

</dd> <dt>

<span data-ttu-id="bd93a-145"><span id="options"></span><span id="OPTIONS"></span>*Optionen*</span><span class="sxs-lookup"><span data-stu-id="bd93a-145"><span id="options"></span><span id="OPTIONS"></span>*options*</span></span>
</dt> <dd>

<span data-ttu-id="bd93a-146">Optionen, die die Zugriffstaste definieren.</span><span class="sxs-lookup"><span data-stu-id="bd93a-146">options that define the accelerator.</span></span> <span data-ttu-id="bd93a-147">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bd93a-147">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="bd93a-148">Option</span><span class="sxs-lookup"><span data-stu-id="bd93a-148">Option</span></span>                             | <span data-ttu-id="bd93a-149">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bd93a-149">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd93a-150">**Noinvert**</span><span class="sxs-lookup"><span data-stu-id="bd93a-150">**NOINVERT**</span></span>                       | <span data-ttu-id="bd93a-151">Gibt an, dass kein Menü Element der obersten Ebene hervorgehoben wird, wenn die Zugriffstaste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd93a-151">Specifies that no top-level menu item is highlighted when the accelerator is used.</span></span> <span data-ttu-id="bd93a-152">Dies ist hilfreich, wenn Sie schnell Infos für Aktionen definieren, z. b. durch Scrollen, die keinem Menü Element entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bd93a-152">This is useful when defining accelerators for actions such as scrolling that do not correspond to a menu item.</span></span> <span data-ttu-id="bd93a-153">Wenn **noinvert** weggelassen wird, wird ein Menü Element der obersten Ebene (sofern möglich) hervorgehoben, wenn die Zugriffstaste verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bd93a-153">If **NOINVERT** is omitted, a top-level menu item will be highlighted (if possible) when the accelerator is used.</span></span> <span data-ttu-id="bd93a-154">Dieses Attribut ist veraltet und wird nur aus Gründen der Abwärtskompatibilität mit Ressourcen Dateien, die für 16-Bit-Windows entwickelt wurden, beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bd93a-154">This attribute is obsolete and retained only for backward compatibility with resource files designed for 16-bit Windows.</span></span> |
| <span data-ttu-id="bd93a-155">**ALT**</span><span class="sxs-lookup"><span data-stu-id="bd93a-155">**ALT**</span></span>                            | <span data-ttu-id="bd93a-156">Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die Alt-Taste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="bd93a-156">Causes the accelerator to be activated only if the ALT key is down.</span></span> <span data-ttu-id="bd93a-157">Gilt nur für virtuelle Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="bd93a-157">Applies only to virtual keys.</span></span>                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="bd93a-158">**Schuss**</span><span class="sxs-lookup"><span data-stu-id="bd93a-158">**SHIFT**</span></span>                          | <span data-ttu-id="bd93a-159">Bewirkt, dass die Zugriffstaste nur aktiviert wird, wenn die UMSCHALTTASTE gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="bd93a-159">Causes the accelerator to be activated only if the SHIFT key is down.</span></span> <span data-ttu-id="bd93a-160">Gilt nur für virtuelle Schlüssel</span><span class="sxs-lookup"><span data-stu-id="bd93a-160">Applies only to virtual keys</span></span>                                                                                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="bd93a-161">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="bd93a-161">**CONTROL**</span></span>](control-control.md) | <span data-ttu-id="bd93a-162">Definiert das Zeichen als Steuerzeichen (die Zugriffstaste wird nur aktiviert, wenn die Steuertaste nicht aktiviert ist).</span><span class="sxs-lookup"><span data-stu-id="bd93a-162">Defines the character as a control character (the accelerator is only activated if the CONTROL key is down).</span></span> <span data-ttu-id="bd93a-163">Dies hat die gleiche Auswirkung wie die Verwendung eines Caretzeichen (^) vor dem Zugriffstasten Zeichen im *Ereignis* Parameter.</span><span class="sxs-lookup"><span data-stu-id="bd93a-163">This has the same effect as using a caret (^) before the accelerator character in the *event* parameter.</span></span> <span data-ttu-id="bd93a-164">Gilt nur für virtuelle Schlüssel</span><span class="sxs-lookup"><span data-stu-id="bd93a-164">Applies only to virtual keys</span></span>                                                                                                                                                                                           |



 

</dd> </dl>

<span data-ttu-id="bd93a-165">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bd93a-165">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="bd93a-166">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="bd93a-166">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd93a-167">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd93a-167">Remarks</span></span>

<span data-ttu-id="bd93a-168">Die [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) -Funktion wird verwendet, um Accelerators-Nachrichten aus der Anwendungs Warteschlange in [**WM- \_ Befehl**](./wm-command.md) -oder [**WM- \_ syscommand**](./wm-syscommand.md) -Meldungen</span><span class="sxs-lookup"><span data-stu-id="bd93a-168">The [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) function is used to translate accelerator messages from the application queue into [**WM\_COMMAND**](./wm-command.md) or [**WM\_SYSCOMMAND**](./wm-syscommand.md) messages.</span></span>

## <a name="examples"></a><span data-ttu-id="bd93a-169">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd93a-169">Examples</span></span>

<span data-ttu-id="bd93a-170">Das folgende Beispiel veranschaulicht die Verwendung von Zugriffstasten.</span><span class="sxs-lookup"><span data-stu-id="bd93a-170">The following example demonstrates the use of accelerator keys.</span></span>

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a><span data-ttu-id="bd93a-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd93a-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd93a-172">Verwenden von Tastatur Accelerators</span><span class="sxs-lookup"><span data-stu-id="bd93a-172">Using Keyboard Accelerators</span></span>](./using-keyboard-accelerators.md)
</dt> <dt>

[<span data-ttu-id="bd93a-173">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="bd93a-173">**TranslateAccelerator**</span></span>](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="bd93a-174">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="bd93a-174">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="bd93a-175">**Dialog**</span><span class="sxs-lookup"><span data-stu-id="bd93a-175">**DIALOG**</span></span>](dialog-resource.md)
</dt> <dt>

[<span data-ttu-id="bd93a-176">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="bd93a-176">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="bd93a-177">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="bd93a-177">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="bd93a-178">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="bd93a-178">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="bd93a-179">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="bd93a-179">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="bd93a-180">**Version**</span><span class="sxs-lookup"><span data-stu-id="bd93a-180">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 