---
description: In MOF sind Zahlen Ziffern, die numerische Werte beschreiben. MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden. Außerdem können diese Zahlen in unterschiedlichen Formaten vorliegen. In der folgenden Tabelle werden die numerischen Werte aufgelistet, die von MOF unterstützt werden.
ms.assetid: 7a18ed36-9c12-42be-a4ee-0f6c0097b130
ms.tgt_platform: multiple
title: Zahlen (WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad348820e0294e76ba059a06b6daa6f1c916d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346890"
---
# <a name="numbers-wmi"></a><span data-ttu-id="7edf4-105">Zahlen (WMI)</span><span class="sxs-lookup"><span data-stu-id="7edf4-105">Numbers (WMI)</span></span>

<span data-ttu-id="7edf4-106">In MOF sind Zahlen Ziffern, die numerische Werte beschreiben.</span><span class="sxs-lookup"><span data-stu-id="7edf4-106">In MOF, numbers are digits that describe numerical values.</span></span> <span data-ttu-id="7edf4-107">MOF bietet eine Vielzahl von Datentypen, die in Automation übersetzt werden. Außerdem können diese Zahlen in unterschiedlichen Formaten vorliegen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-107">MOF provides a variety of data types that translate into Automation, and also allows those numbers to be in different formats.</span></span> <span data-ttu-id="7edf4-108">In der folgenden Tabelle werden die numerischen Werte aufgelistet, die von MOF unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7edf4-108">The following table lists the numeric values that MOF supports.</span></span>



| <span data-ttu-id="7edf4-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="7edf4-109">Data type</span></span>  | <span data-ttu-id="7edf4-110">Automatisierungstyp</span><span class="sxs-lookup"><span data-stu-id="7edf4-110">Automation type</span></span> | <span data-ttu-id="7edf4-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7edf4-111">Description</span></span>                                                                                                                                                             |
|------------|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7edf4-112">**sint8**</span><span class="sxs-lookup"><span data-stu-id="7edf4-112">**sint8**</span></span>  | <span data-ttu-id="7edf4-113">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="7edf4-113">**VT\_I2**</span></span>      | <span data-ttu-id="7edf4-114">8-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-114">Signed 8-bit integer.</span></span><br/>                                                                                                                                        |
| <span data-ttu-id="7edf4-115">**sint16**</span><span class="sxs-lookup"><span data-stu-id="7edf4-115">**sint16**</span></span> | <span data-ttu-id="7edf4-116">**VT \_ I2**</span><span class="sxs-lookup"><span data-stu-id="7edf4-116">**VT\_I2**</span></span>      | <span data-ttu-id="7edf4-117">Ganze 16-Bit-Zahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-117">Signed 16-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="7edf4-118">**sint32**</span><span class="sxs-lookup"><span data-stu-id="7edf4-118">**sint32**</span></span> | <span data-ttu-id="7edf4-119">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="7edf4-119">VT\_I4</span></span>          | <span data-ttu-id="7edf4-120">32-Bit-Ganzzahl mit Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-120">Signed 32-bit integer.</span></span><br/>                                                                                                                                       |
| <span data-ttu-id="7edf4-121">**sint64**</span><span class="sxs-lookup"><span data-stu-id="7edf4-121">**sint64**</span></span> | <span data-ttu-id="7edf4-122">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7edf4-122">**VT\_BSTR**</span></span>    | <span data-ttu-id="7edf4-123">64-Bit-Ganzzahl mit Vorzeichen in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7edf4-123">Signed 64-bit integer in string form.</span></span> <span data-ttu-id="7edf4-124">Dieser Typ folgt dem Hexadezimal-oder Dezimal Format gemäß den American National Standards Institute (ANSI) C-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7edf4-124">This type follows hexadecimal or decimal format according to the American National Standards Institute (ANSI) C rules.</span></span><br/> |
| <span data-ttu-id="7edf4-125">**real32**</span><span class="sxs-lookup"><span data-stu-id="7edf4-125">**real32**</span></span> | <span data-ttu-id="7edf4-126">**VT \_ R4**</span><span class="sxs-lookup"><span data-stu-id="7edf4-126">**VT\_R4**</span></span>      | <span data-ttu-id="7edf4-127">ein 4-Byte-Gleit Komma Wert, der dem Institute of Electrical and Electronics Engineers, Inc. (IEEE) Standard folgt.</span><span class="sxs-lookup"><span data-stu-id="7edf4-127">4-byte floating-point value that follows the Institute of Electrical and Electronics Engineers, Inc. (IEEE) standard.</span></span><br/>                                        |
| <span data-ttu-id="7edf4-128">**real64**</span><span class="sxs-lookup"><span data-stu-id="7edf4-128">**real64**</span></span> | <span data-ttu-id="7edf4-129">**VT \_ R8**</span><span class="sxs-lookup"><span data-stu-id="7edf4-129">**VT\_R8**</span></span>      | <span data-ttu-id="7edf4-130">8-Byte-Gleit Komma Wert, der auf den IEEE-Standard folgt.</span><span class="sxs-lookup"><span data-stu-id="7edf4-130">8-byte floating-point value that follows the IEEE standard.</span></span><br/>                                                                                                  |
| <span data-ttu-id="7edf4-131">**Uint8**</span><span class="sxs-lookup"><span data-stu-id="7edf4-131">**uint8**</span></span>  | <span data-ttu-id="7edf4-132">**VT \_ UI1**</span><span class="sxs-lookup"><span data-stu-id="7edf4-132">**VT\_UI1**</span></span>     | <span data-ttu-id="7edf4-133">8-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-133">Unsigned 8-bit integer.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="7edf4-134">**uint16**</span><span class="sxs-lookup"><span data-stu-id="7edf4-134">**uint16**</span></span> | <span data-ttu-id="7edf4-135">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="7edf4-135">**VT\_I4**</span></span>      | <span data-ttu-id="7edf4-136">16-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-136">Unsigned 16-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="7edf4-137">**uint32**</span><span class="sxs-lookup"><span data-stu-id="7edf4-137">**uint32**</span></span> | <span data-ttu-id="7edf4-138">**VT \_ I4**</span><span class="sxs-lookup"><span data-stu-id="7edf4-138">**VT\_I4**</span></span>      | <span data-ttu-id="7edf4-139">32-Bit-Ganzzahl ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-139">Unsigned 32-bit integer.</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="7edf4-140">**uint64**</span><span class="sxs-lookup"><span data-stu-id="7edf4-140">**uint64**</span></span> | <span data-ttu-id="7edf4-141">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="7edf4-141">**VT\_BSTR**</span></span>    | <span data-ttu-id="7edf4-142">64-Bit-Ganzzahl ohne Vorzeichen in Form einer Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="7edf4-142">Unsigned 64-bit integer in string form.</span></span> <span data-ttu-id="7edf4-143">Dieser Typ folgt dem Hexadezimal-oder Dezimal Format gemäß den ANSI C-Regeln.</span><span class="sxs-lookup"><span data-stu-id="7edf4-143">This type follows hexadecimal or decimal format according to ANSI C rules.</span></span><br/>                                           |



 

<span data-ttu-id="7edf4-144">Obwohl der MOF-Code flexibel ist, treten beim Umgang mit Automation einige Änderungen auf:</span><span class="sxs-lookup"><span data-stu-id="7edf4-144">Although flexible, MOF code does encounter some changes when dealing with Automation:</span></span>

-   <span data-ttu-id="7edf4-145">Sie müssen 64-Bit-Ganzzahlen als Zeichen folgen codieren.</span><span class="sxs-lookup"><span data-stu-id="7edf4-145">You must encode 64-bit integers as strings.</span></span>

    <span data-ttu-id="7edf4-146">Automation unterstützt keinen ganzzahligen 64-Bit-Typ.</span><span class="sxs-lookup"><span data-stu-id="7edf4-146">Automation does not support a 64-bit integral type.</span></span>

-   <span data-ttu-id="7edf4-147">Automatisierungs Typen entsprechen nicht immer den MOF-Datentypen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-147">Automation types do not always correspond in bit size to MOF data types.</span></span>

    <span data-ttu-id="7edf4-148">Automation verwendet beispielsweise VT \_ I4, um einen 16-Bit-Wert ohne Vorzeichen zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="7edf4-148">For example, Automation uses VT\_I4 to return an unsigned 16-bit value.</span></span> <span data-ttu-id="7edf4-149">Diese Abweichung ist aufgrund von Problemen mit der Signatur Erweiterung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7edf4-149">This discrepancy exists because of sign-extension problems.</span></span> <span data-ttu-id="7edf4-150">Wenn \_ die Automatisierung die Verwendung von VT I2 anstelle von VT I4 verwendet \_ hat, scheint 65.536 der Wert 1 zu sein, was zu Typen-und Bereichs Problemen führt.</span><span class="sxs-lookup"><span data-stu-id="7edf4-150">If Automation used VT\_I2 instead of VT\_I4, 65,536 would appear to be the value  1, causing type and range problems.</span></span> <span data-ttu-id="7edf4-151">Ebenso stellt Automation den **UInt32** -Typ als VT \_ I4 dar, da kein größerer ganzzahliger Typ vorhanden ist, der **UInt32** enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7edf4-151">Similarly, Automation represents the **uint32** type as VT\_I4 because there exists no larger integer type to contain **uint32**.</span></span>

-   <span data-ttu-id="7edf4-152">Sie müssen keine Darstellung für 8-Bit-Zahlen Typen ändern.</span><span class="sxs-lookup"><span data-stu-id="7edf4-152">You do not need to change any representation for 8-bit numeral types.</span></span>

    <span data-ttu-id="7edf4-153">Automation unterstützt VT \_ UI1, einen 8-Bit-Typ ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-153">Automation supports VT\_UI1, an unsigned 8-bit type.</span></span>

<span data-ttu-id="7edf4-154">MOF unterstützt lange Konstanten.</span><span class="sxs-lookup"><span data-stu-id="7edf4-154">MOF supports long constants.</span></span> <span data-ttu-id="7edf4-155">Sie deklarieren eine lange Konstante mit einer einfachen Reihe von Ziffern mit einem optionalen negativen Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-155">You declare a long constant using a simple series of digits with an optional negative sign.</span></span> <span data-ttu-id="7edf4-156">Eine lange Konstante darf nicht die Größe der Variablen überschreiten, die für die Speicherung deklariert ist.</span><span class="sxs-lookup"><span data-stu-id="7edf4-156">A long constant cannot exceed the size of the variable that is declared to hold it.</span></span> <span data-ttu-id="7edf4-157">Einige Beispiele für lange Konstanten sind 1000 und 12310.</span><span class="sxs-lookup"><span data-stu-id="7edf4-157">Some examples of long constants are 1000 and  12310.</span></span>

<span data-ttu-id="7edf4-158">MOF unterstützt auch alternative numerische Formate.</span><span class="sxs-lookup"><span data-stu-id="7edf4-158">MOF also supports alternate numerical formats.</span></span> <span data-ttu-id="7edf4-159">In der folgenden Tabelle werden die Sonderzeichen aufgelistet, die Sie zum Beschreiben von hexadezimalen, binären und oktalen Konstanten verwenden müssen.</span><span class="sxs-lookup"><span data-stu-id="7edf4-159">The following table lists the special characters you must use to describe hexadecimal, binary, and octal constants.</span></span>



| <span data-ttu-id="7edf4-160">Konstante</span><span class="sxs-lookup"><span data-stu-id="7edf4-160">Constant</span></span>               | <span data-ttu-id="7edf4-161">Sonderzeichen</span><span class="sxs-lookup"><span data-stu-id="7edf4-161">Special character</span></span>     | <span data-ttu-id="7edf4-162">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7edf4-162">Example</span></span>                   |
|------------------------|-----------------------|---------------------------|
| <span data-ttu-id="7edf4-163">Decimal</span><span class="sxs-lookup"><span data-stu-id="7edf4-163">Decimal</span></span><br/>     | <span data-ttu-id="7edf4-164">Keine</span><span class="sxs-lookup"><span data-stu-id="7edf4-164">None</span></span><br/>       | <span data-ttu-id="7edf4-165">Val = 65</span><span class="sxs-lookup"><span data-stu-id="7edf4-165">val = 65</span></span><br/>       |
| <span data-ttu-id="7edf4-166">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="7edf4-166">Hexadecimal</span></span><br/> | <span data-ttu-id="7edf4-167">0x-Präfix</span><span class="sxs-lookup"><span data-stu-id="7edf4-167">0x prefix</span></span><br/>  | <span data-ttu-id="7edf4-168">Val = 0x41</span><span class="sxs-lookup"><span data-stu-id="7edf4-168">val = 0x41</span></span><br/>     |
| <span data-ttu-id="7edf4-169">Oktal</span><span class="sxs-lookup"><span data-stu-id="7edf4-169">Octal</span></span><br/>       | <span data-ttu-id="7edf4-170">Führende 0</span><span class="sxs-lookup"><span data-stu-id="7edf4-170">Leading 0</span></span><br/>  | <span data-ttu-id="7edf4-171">Val = 0101</span><span class="sxs-lookup"><span data-stu-id="7edf4-171">val = 0101</span></span><br/>     |
| <span data-ttu-id="7edf4-172">Binary</span><span class="sxs-lookup"><span data-stu-id="7edf4-172">Binary</span></span><br/>      | <span data-ttu-id="7edf4-173">Nachfolgende B</span><span class="sxs-lookup"><span data-stu-id="7edf4-173">Trailing B</span></span><br/> | <span data-ttu-id="7edf4-174">Val = 1000001b</span><span class="sxs-lookup"><span data-stu-id="7edf4-174">val = 1000001B</span></span><br/> |



 

<span data-ttu-id="7edf4-175">Sie können eine Gleit Komma Konstante verwenden, um wissenschaftliche Schreibweise und Bruchteile darzustellen, wie im folgenden dargestellt:</span><span class="sxs-lookup"><span data-stu-id="7edf4-175">You can use a floating-point constant to represent scientific notation as well as fractions, as shown next:</span></span>

``` syntax
3.14
-3.14
-1.2778E+02
```

<span data-ttu-id="7edf4-176">WMI betrachtet Gleit Komma Konstanten als **VT \_ R8** -Typen für die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="7edf4-176">WMI considers floating-point constants as **VT\_R8** types for Automation.</span></span>

<span data-ttu-id="7edf4-177">Im folgenden Beispiel werden Klassen-und instanzdeklarationen beschrieben, die veranschaulichen, wie die einzelnen numerischen Datentypen verwendet werden, um Eigenschaften festzulegen:</span><span class="sxs-lookup"><span data-stu-id="7edf4-177">The following example describes class and instance declarations that illustrate how to use each of the numeric data types to set properties:</span></span>

``` syntax
Class NumericDataClass
 {
   [key] uint8 Duint8;
   SInt8       Dchar;
   UInt16      Dtword;
   Sint16      Dinst16;
   UInt32      Ddword;
   Sint32      Dinst1;
   Sint32      Dinst2;
   Sint32      Dinst3;
   Sint32      Dinst4;
   Sint32      Dinst5;
   Real32      Dfloat;
   Real64      Ddouble1;
   Real64      Ddouble2;
 };

instance of NumericDataClass
 {
   Duint8   =  122;
   Dchar    = -128;
   Dtword   =  30;
   Dinst16  = -1445;
   Ddword   =  6987777;
   Dinst1   = -455589;
   Dinst2   =  23;
   Dinst3   =  03;         // Base 8
   Dinst4   =  0xFe;       // Base 16
   Dinst5   =  11b;        // Base 2
   Dfloat   =  3.1478;
   Ddouble1 =  99987.3654;
   Ddouble2 =  2.3e-2;
 };
```

 

 




