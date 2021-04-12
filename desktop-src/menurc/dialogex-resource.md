---
title: DIALOGEX-Ressource
description: Definiert ein Dialogfeld. | DIALOGEX-Ressource
ms.assetid: 3ff28b68-e8b4-444d-8e26-5119ed30e44e
keywords:
- DIALOGEX-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- DIALOGEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbd55bfb06b678742aa5e356c9e62b14229aa8d3
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219310"
---
# <a name="dialogex-resource"></a><span data-ttu-id="30629-105">DIALOGEX-Ressource</span><span class="sxs-lookup"><span data-stu-id="30629-105">DIALOGEX resource</span></span>

<span data-ttu-id="30629-106">Definiert ein Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30629-106">Defines a dialog box.</span></span> <span data-ttu-id="30629-107">Die-Anweisung definiert die Position und die Dimensionen des Dialog Felds auf dem Bildschirm sowie den Dialogfeld Stil.</span><span class="sxs-lookup"><span data-stu-id="30629-107">The statement defines the position and dimensions of the dialog box on the screen as well as the dialog box style.</span></span> <span data-ttu-id="30629-108">Außerdem wird Folgendes definiert:</span><span class="sxs-lookup"><span data-stu-id="30629-108">It also defines the following:</span></span>

-   <span data-ttu-id="30629-109">Hilfe-IDs im Dialogfeld selbst sowie für Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30629-109">Help IDs on the dialog itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="30629-110">Verwendung der [**ExStyle**](exstyle-statement.md) -Anweisung für das Dialogfeld selbst und für Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30629-110">Use of the [**EXSTYLE**](exstyle-statement.md) statement for the dialog box itself as well as on controls within the dialog box.</span></span>
-   <span data-ttu-id="30629-111">Schrift Breite und kursiv Einstellungen für die Schriftart, die im Dialogfeld verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30629-111">Font weight and italic settings for the font to be used in the dialog box.</span></span>
-   <span data-ttu-id="30629-112">Steuerelement spezifische Daten für Steuerelemente im Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30629-112">Control-specific data for controls within the dialog box.</span></span>
-   <span data-ttu-id="30629-113">Verwendung der vordefinierten System Klassennamen " **BEDIT**", " **Iedit**" und " **HEdit** ".</span><span class="sxs-lookup"><span data-stu-id="30629-113">Use of the **BEDIT**, **IEDIT**, and **HEDIT** predefined system class names.</span></span>

``` syntax
nameID DIALOGEX x, y, width, height [ , helpID] [optional-statements]  {control-statements}
```

## <a name="parameters"></a><span data-ttu-id="30629-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="30629-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30629-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="30629-115"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="30629-116">Eindeutiger Name oder ein eindeutiger ganzzahliger 16-Bit-Wert ohne Vorzeichen, der das Dialogfeld identifiziert.</span><span class="sxs-lookup"><span data-stu-id="30629-116">Unique name or a unique 16-bit unsigned integer value that identifies the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="30629-117"><span id="x"></span><span id="X"></span>*Stuben*</span><span class="sxs-lookup"><span data-stu-id="30629-117"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="30629-118">Speicherort auf dem Bildschirm der linken Seite des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="30629-118">Location on the screen of the left side of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="30629-119"><span id="y"></span><span id="Y"></span>*Teenie*</span><span class="sxs-lookup"><span data-stu-id="30629-119"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="30629-120">Speicherort auf dem Bildschirm des oberen Rands des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="30629-120">Location on the screen of the top of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="30629-121"><span id="width"></span><span id="WIDTH"></span>*Breite*</span><span class="sxs-lookup"><span data-stu-id="30629-121"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="30629-122">Breite des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="30629-122">Width of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="30629-123"><span id="height"></span><span id="HEIGHT"></span>*Flugh*</span><span class="sxs-lookup"><span data-stu-id="30629-123"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="30629-124">Höhe des Dialog Felds in Dialogfeld Einheiten.</span><span class="sxs-lookup"><span data-stu-id="30629-124">Height of the dialog box, in dialog units.</span></span>

</dd> <dt>

<span data-ttu-id="30629-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*HelpID*</span><span class="sxs-lookup"><span data-stu-id="30629-125"><span id="helpID"></span><span id="helpid"></span><span id="HELPID"></span>*helpID*</span></span>
</dt> <dd>

<span data-ttu-id="30629-126">Numerischer Ausdruck, der die ID angibt, mit der das Dialogfeld während der [**WM- \_ Hilfe**](../shell/wm-help.md) Verarbeitung identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="30629-126">Numeric expression indicating the ID used to identify the dialog box during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="30629-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="30629-127"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="30629-128">Optionen für das Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="30629-128">Options for the dialog box.</span></span> <span data-ttu-id="30629-129">Dies kann NULL oder mehr der folgenden-Anweisungen sein.</span><span class="sxs-lookup"><span data-stu-id="30629-129">This can be zero or more of the following statements.</span></span>



| <span data-ttu-id="30629-130">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="30629-130">Statement</span></span>                                                         | <span data-ttu-id="30629-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30629-131">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30629-132">**Beschriftung** "*Text*"</span><span class="sxs-lookup"><span data-stu-id="30629-132">**CAPTION** "*text*"</span></span>                                              | <span data-ttu-id="30629-133">Beschriftung des Dialog Felds, wenn es über eine Titelleiste verfügt.</span><span class="sxs-lookup"><span data-stu-id="30629-133">Caption of the dialog box if it has a title bar.</span></span> <span data-ttu-id="30629-134">Weitere Informationen finden Sie unter [**Caption-Anweisung**](caption-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-134">For more information, see [**CAPTION Statement**](caption-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="30629-135">**Merkmale** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="30629-135">**CHARACTERISTICS** *dword*</span></span>                                       | <span data-ttu-id="30629-136">Benutzerdefinierter **DWORD** -Wert, der von Ressourcen Tools verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="30629-136">User-defined **DWORD** value for use by resource tools.</span></span> <span data-ttu-id="30629-137">Dieser Wert wird vom System nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="30629-137">This value is not used by the system.</span></span> <span data-ttu-id="30629-138">Weitere Informationen finden Sie unter [**Characteristics-Anweisung**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-138">For more information, see [**CHARACTERISTICS Statement**](characteristics-statement.md).</span></span>                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="30629-139">**Class**-_Klasse_</span><span class="sxs-lookup"><span data-stu-id="30629-139">**CLASS**_class_</span></span>                                                  | <span data-ttu-id="30629-140">Eine 16-Bit-Ganzzahl ohne Vorzeichen oder eine Zeichenfolge, die in doppelten Anführungszeichen (") eingeschlossen ist, die die Klasse des Dialog Felds angibt.</span><span class="sxs-lookup"><span data-stu-id="30629-140">A 16-bit unsigned integer or a string, enclosed in double quotation marks ("), that identifies the class of the dialog box.</span></span> <span data-ttu-id="30629-141">Weitere Informationen finden Sie unter [**Class-Anweisung**](class-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-141">For more information, see [**CLASS Statement**](class-statement.md).</span></span>                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="30629-142">**ExStyle** =  *Erweiterte Stile*</span><span class="sxs-lookup"><span data-stu-id="30629-142">**EXSTYLE**= *extended-styles*</span></span>                                    | <span data-ttu-id="30629-143">Erweiterte Fenster Stil des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="30629-143">Extended window style of the dialog box.</span></span> <span data-ttu-id="30629-144">Weitere Informationen finden Sie unter [**ExStyle-Anweisung**](exstyle-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-144">For more information, see [**EXSTYLE Statement**](exstyle-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="30629-145">**Schriftart** *pointsize*, Schriftart, *Weight*, *kursiv*, *CharSet*</span><span class="sxs-lookup"><span data-stu-id="30629-145">**FONT** *pointsize*, "*typeface*", *weight*, *italic*, *charset*</span></span> | <span data-ttu-id="30629-146">Die Punktgröße und Schriftart für die Schriftart.</span><span class="sxs-lookup"><span data-stu-id="30629-146">Point size and typeface for the font.</span></span> <span data-ttu-id="30629-147">Verwenden Sie für *Weight* die in WinGDI. h definierten \**FW \_ \** _-Werte.</span><span class="sxs-lookup"><span data-stu-id="30629-147">For *weight*, use the \**FW\_\** _ values defined in WinGDI.h.</span></span> <span data-ttu-id="30629-148">Geben Sie für _italic \* true an, um eine kursiv Schrift zu verwenden, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="30629-148">For _italic\*, specify TRUE to use an italic font, FALSE otherwise.</span></span> <span data-ttu-id="30629-149">Verwenden Sie für *CharSet* den Wert, der im **lfCharSet** -Member der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur definiert ist.</span><span class="sxs-lookup"><span data-stu-id="30629-149">For *charset*, use the value defined in the **lfCharSet** member of the [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure.</span></span> <span data-ttu-id="30629-150">Um die definitive Schriftart für ein Dialogfeld zu erhalten, sollte eine Anwendung *CharSet* zusammen mit anderen Schriftart Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="30629-150">To get the definitive font for a dialog box, an application should specify *charset* along with other font properties.</span></span> <span data-ttu-id="30629-151">Weitere Informationen finden Sie unter [**Font-Anweisung**](font-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-151">For more information, see [**FONT Statement**](font-statement.md).</span></span> |
| <span data-ttu-id="30629-152">**Sprach** *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="30629-152">**LANGUAGE** *language*, *sublanguage*</span></span>                            | <span data-ttu-id="30629-153">Sprache des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="30629-153">Language of the dialog box.</span></span> <span data-ttu-id="30629-154">Weitere Informationen finden Sie unter [**Language Statement**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-154">For more information, see [**LANGUAGE Statement**](language-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="30629-155"> *MENUNAME darf* -Menü</span><span class="sxs-lookup"><span data-stu-id="30629-155">**MENU** *menuname*</span></span>                                               | <span data-ttu-id="30629-156">Das zu verwendende Menü.</span><span class="sxs-lookup"><span data-stu-id="30629-156">Menu to be used.</span></span> <span data-ttu-id="30629-157">Dieser Wert ist entweder der Name des Menüs oder der ganzzahlige Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="30629-157">This value is either the name of the menu or its integer identifier.</span></span> <span data-ttu-id="30629-158">Weitere Informationen finden Sie unter [**Menu-Anweisung**](menu-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-158">For more information, see [**MENU Statement**](menu-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="30629-159">**Stil** *Stile*</span><span class="sxs-lookup"><span data-stu-id="30629-159">**STYLE** *styles*</span></span>                                                | <span data-ttu-id="30629-160">Stile des Dialog Felds.</span><span class="sxs-lookup"><span data-stu-id="30629-160">Styles of the dialog box.</span></span> <span data-ttu-id="30629-161">Weitere Informationen finden Sie unter [**Style-Anweisung**](style-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-161">For more information, see [**STYLE Statement**](style-statement.md).</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="30629-162">**Version** *DWORD*</span><span class="sxs-lookup"><span data-stu-id="30629-162">**VERSION** *dword*</span></span>                                               | <span data-ttu-id="30629-163">Benutzerdefinierter **DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="30629-163">User-defined **DWORD** value.</span></span> <span data-ttu-id="30629-164">Diese Anweisung ist für die Verwendung durch zusätzliche Ressourcen Tools vorgesehen und wird nicht vom System verwendet.</span><span class="sxs-lookup"><span data-stu-id="30629-164">This statement is intended for use by additional resource tools and is not used by the system.</span></span> <span data-ttu-id="30629-165">Weitere Informationen finden Sie unter [**Versions Anweisung**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="30629-165">For more information, see [**VERSION Statement**](version-statement.md).</span></span>                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

<span data-ttu-id="30629-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*Control-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="30629-166"><span id="control-statements"></span><span id="CONTROL-STATEMENTS"></span>*control-statements*</span></span>
</dt> <dd>

<span data-ttu-id="30629-167">Der Text der **DIALOGEX** -Ressource besteht aus einer beliebigen Anzahl von Steuerungs Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="30629-167">Body of the **DIALOGEX** resource is made up of any number of control statements.</span></span> <span data-ttu-id="30629-168">Es gibt vier Familien von Steuerungs Anweisungen: generisch, statisch, Schaltfläche und bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="30629-168">There are four families of control statements: generic, static, button, and edit.</span></span> <span data-ttu-id="30629-169">Weitere Informationen finden Sie in den Hinweisen.</span><span class="sxs-lookup"><span data-stu-id="30629-169">For more information, see Remarks.</span></span>

</dd> </dl>

<span data-ttu-id="30629-170">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30629-170">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="30629-171">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="30629-171">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="30629-172">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30629-172">Remarks</span></span>

<span data-ttu-id="30629-173">Die gültigen Vorgänge, die in einem der numerischen Ausdrücke in den Anweisungen von **DIALOGEX** enthalten sein können, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="30629-173">The valid operations that may be contained in any of the numeric expressions in the statements of **DIALOGEX** are as follows:</span></span>

-   <span data-ttu-id="30629-174">Hinzufügen ("+")</span><span class="sxs-lookup"><span data-stu-id="30629-174">Add ('+')</span></span>
-   <span data-ttu-id="30629-175">Subtraktion ("-")</span><span class="sxs-lookup"><span data-stu-id="30629-175">Subtract ('-')</span></span>
-   <span data-ttu-id="30629-176">Unäres Minuszeichen ("-")</span><span class="sxs-lookup"><span data-stu-id="30629-176">Unary minus ('-')</span></span>
-   <span data-ttu-id="30629-177">Unärer Not (' ~ ')</span><span class="sxs-lookup"><span data-stu-id="30629-177">Unary NOT ('~')</span></span>
-   <span data-ttu-id="30629-178">Und (' & ')</span><span class="sxs-lookup"><span data-stu-id="30629-178">AND ('&')</span></span>
-   <span data-ttu-id="30629-179">Oder (' \| ')</span><span class="sxs-lookup"><span data-stu-id="30629-179">OR ('\|')</span></span>

<span data-ttu-id="30629-180">Der Hauptteil der Ressource besteht aus generischen, statischen, Schaltflächen-und Bearbeitungs Steuerungs Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="30629-180">The body of the resource is made up of generic, static, button, and edit control statements.</span></span> <span data-ttu-id="30629-181">Obwohl jede dieser Aufstellungen eine andere Syntax zum Definieren spezifischer Features Ihrer Steuerelemente verwendet, haben Sie alle eine gemeinsame Syntax zum Definieren von Position, Größe, erweiterten Stilen, Hilfe Identifikationsnummer und Steuerungs spezifischen Daten.</span><span class="sxs-lookup"><span data-stu-id="30629-181">While each of these families of statements uses a different syntax for defining specific features of its controls, they all share a common syntax for defining the position, size, extended styles, help identification number, and control-specific data.</span></span> <span data-ttu-id="30629-182">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-182">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

### <a name="generic-control-statements"></a><span data-ttu-id="30629-183">Generische Steuerungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="30629-183">Generic Control Statements</span></span>

``` syntax
CONTROL controlText, id, className, style
```

<dl> <dt>

<span data-ttu-id="30629-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*</span><span class="sxs-lookup"><span data-stu-id="30629-184"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="30629-185">Fenster Text für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="30629-185">Window text for the control.</span></span> <span data-ttu-id="30629-186">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-186">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="30629-187"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="30629-187"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="30629-188">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="30629-188">Control identifier.</span></span> <span data-ttu-id="30629-189">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-189">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="30629-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*ClassName*</span><span class="sxs-lookup"><span data-stu-id="30629-190"><span id="className"></span><span id="classname"></span><span id="CLASSNAME"></span>*className*</span></span>
</dt> <dd>

<span data-ttu-id="30629-191">Name der Klasse.</span><span class="sxs-lookup"><span data-stu-id="30629-191">Name of the class.</span></span> <span data-ttu-id="30629-192">Dabei kann es sich um eine Zeichenfolge handeln, die in doppelten Anführungszeichen (") oder einer der folgenden vordefinierten System Klassen eingeschlossen ist: **Schaltfläche**, **statisch**, **Bearbeiten**, **ListBox**, **Scrollleiste** oder **ComboBox**.</span><span class="sxs-lookup"><span data-stu-id="30629-192">This may be either a string enclosed in double quotation marks (") or one of the following predefined system classes: **BUTTON**, **STATIC**, **EDIT**, **LISTBOX**, **SCROLLBAR**, or **COMBOBOX**.</span></span>

</dd> <dt>

<span data-ttu-id="30629-193"><span id="style"></span><span id="STYLE"></span>*Vorbild*</span><span class="sxs-lookup"><span data-stu-id="30629-193"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="30629-194">Fenster Stile (explizite, in winuser. H definierte Werte von **WS \_ \* *_, _* BS \_ \* *_, _* SS \_ \* *_, _* es \_ \* *_, _* lbs \_ \* *_, _* SBS \_ \* *_ und _* CBS \_ \*** können verwendet werden, indem der RC-Datei eine include-Datei hinzugefügt `#include "winuser.h"` wird:</span><span class="sxs-lookup"><span data-stu-id="30629-194">Window styles (explicit **WS\_\**_, _\* BS\_\**_, _\* SS\_\*\*_, _\* ES\_\*\*_, _\* LBS\_\*\*_, _\* SBS\_\*\*_, and _\* CBS\_\*\*\* style values defined in Winuser.H can be used by adding an include to the .rc file: `#include "winuser.h"`).</span></span> <span data-ttu-id="30629-195">Weitere Informationen finden Sie unter [Fenster Stile](/windows/desktop/winmsg/window-styles).</span><span class="sxs-lookup"><span data-stu-id="30629-195">For more information, see [Window Styles](/windows/desktop/winmsg/window-styles).</span></span>

</dd> </dl>

### <a name="static-control-statements"></a><span data-ttu-id="30629-196">Statische Steuerelement Anweisungen</span><span class="sxs-lookup"><span data-stu-id="30629-196">Static Control Statements</span></span>

``` syntax
staticClass controlText, id
```

<dl> <dt>

<span data-ttu-id="30629-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticclass*</span><span class="sxs-lookup"><span data-stu-id="30629-197"><span id="staticClass"></span><span id="staticclass"></span><span id="STATICCLASS"></span>*staticClass*</span></span>
</dt> <dd>

<span data-ttu-id="30629-198">**LTEXT**, **rtext** oder **CTEXT**.</span><span class="sxs-lookup"><span data-stu-id="30629-198">**LTEXT**, **RTEXT**, or **CTEXT**.</span></span>

</dd> <dt>

<span data-ttu-id="30629-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*</span><span class="sxs-lookup"><span data-stu-id="30629-199"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="30629-200">Fenster Text für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="30629-200">Window text for the control.</span></span> <span data-ttu-id="30629-201">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-201">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="30629-202"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="30629-202"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="30629-203">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="30629-203">Control identifier.</span></span> <span data-ttu-id="30629-204">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-204">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="button-control-statements"></a><span data-ttu-id="30629-205">Button-Steuerelement Anweisungen</span><span class="sxs-lookup"><span data-stu-id="30629-205">Button Control Statements</span></span>

``` syntax
buttonClass controlText, id
```

<dl> <dt>

<span data-ttu-id="30629-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*ButtonClass*</span><span class="sxs-lookup"><span data-stu-id="30629-206"><span id="buttonClass"></span><span id="buttonclass"></span><span id="BUTTONCLASS"></span>*buttonClass*</span></span>
</dt> <dd>

<span data-ttu-id="30629-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CheckBox**, **PUSHBOX**, **PUSHBUTTON**, **RadioButton**, **STATE3** oder **userButton**.</span><span class="sxs-lookup"><span data-stu-id="30629-207">**AUTO3STATE**, **AUTOCHECKBOX**, **AUTORADIOBUTTON**, **CHECKBOX**, **PUSHBOX**, **PUSHBUTTON**, **RADIOBUTTON**, **STATE3**, or **USERBUTTON**.</span></span>

</dd> <dt>

<span data-ttu-id="30629-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*ControlText*</span><span class="sxs-lookup"><span data-stu-id="30629-208"><span id="controlText"></span><span id="controltext"></span><span id="CONTROLTEXT"></span>*controlText*</span></span>
</dt> <dd>

<span data-ttu-id="30629-209">Fenster Text für das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="30629-209">Window text for the control.</span></span> <span data-ttu-id="30629-210">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-210">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> <dt>

<span data-ttu-id="30629-211"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="30629-211"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="30629-212">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="30629-212">Control identifier.</span></span> <span data-ttu-id="30629-213">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-213">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

### <a name="edit-control-statements"></a><span data-ttu-id="30629-214">Edit Control-Anweisungen</span><span class="sxs-lookup"><span data-stu-id="30629-214">Edit Control Statements</span></span>

``` syntax
editClass id
```

<dl> <dt>

<span data-ttu-id="30629-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*EditClass*</span><span class="sxs-lookup"><span data-stu-id="30629-215"><span id="editClass"></span><span id="editclass"></span><span id="EDITCLASS"></span>*editClass*</span></span>
</dt> <dd>

<span data-ttu-id="30629-216">**EDITTEXT**, **BEDIT**, **HEdit** oder **Iedit**.</span><span class="sxs-lookup"><span data-stu-id="30629-216">**EDITTEXT**, **BEDIT**, **HEDIT**, or **IEDIT**.</span></span>

</dd> <dt>

<span data-ttu-id="30629-217"><span id="id"></span><span id="ID"></span>*Name*</span><span class="sxs-lookup"><span data-stu-id="30629-217"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="30629-218">Steuerelement</span><span class="sxs-lookup"><span data-stu-id="30629-218">Control identifier.</span></span> <span data-ttu-id="30629-219">Weitere Informationen finden Sie unter [allgemeine Steuerelement Parameter](common-control-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="30629-219">For more information, see [Common Control Parameters](common-control-parameters.md).</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="30629-220">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30629-220">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30629-221">Verwenden von Dialog Feldern</span><span class="sxs-lookup"><span data-stu-id="30629-221">Using Dialog Boxes</span></span>](../dlgbox/using-dialog-boxes.md)
</dt> <dt>

[<span data-ttu-id="30629-222">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="30629-222">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="30629-223">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="30629-223">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="30629-224">**Steuerelement**</span><span class="sxs-lookup"><span data-stu-id="30629-224">**CONTROL**</span></span>](control-control.md)
</dt> <dt>

[<span data-ttu-id="30629-225">**"Kreatedialog"**</span><span class="sxs-lookup"><span data-stu-id="30629-225">**CreateDialog**</span></span>](/windows/win32/api/winuser/nf-winuser-createdialoga)
</dt> <dt>

[<span data-ttu-id="30629-226">**CreateWindow**</span><span class="sxs-lookup"><span data-stu-id="30629-226">**CreateWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[<span data-ttu-id="30629-227">**Dialogbox**</span><span class="sxs-lookup"><span data-stu-id="30629-227">**DialogBox**</span></span>](/windows/win32/api/winuser/nf-winuser-dialogboxa)
</dt> <dt>

[<span data-ttu-id="30629-228">**GetDialogBaseUnits**</span><span class="sxs-lookup"><span data-stu-id="30629-228">**GetDialogBaseUnits**</span></span>](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[<span data-ttu-id="30629-229">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="30629-229">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="30629-230">**"LogFont"**</span><span class="sxs-lookup"><span data-stu-id="30629-230">**LOGFONT**</span></span>](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[<span data-ttu-id="30629-231">Stehen</span><span class="sxs-lookup"><span data-stu-id="30629-231">MENU</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="30629-232">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="30629-232">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="30629-233">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="30629-233">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="30629-234">**Version**</span><span class="sxs-lookup"><span data-stu-id="30629-234">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 
