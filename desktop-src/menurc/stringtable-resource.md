---
title: STRINGTABLE-Ressource
description: Definiert eine oder mehrere Zeichen folgen Ressourcen für eine Anwendung. Zeichen folgen Ressourcen sind einfach mit NULL endende Unicode-oder ASCII-Zeichen folgen, die bei Bedarf aus der ausführbaren Datei mithilfe der LoadString-Funktion geladen werden können.
ms.assetid: 5868245d-3445-4792-86f5-253945310d36
keywords:
- STRINGTABLE-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- STRINGTABLE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 271abd022bdedd3b27e0434e7364542fa51c8987
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101627"
---
# <a name="stringtable-resource"></a><span data-ttu-id="7e385-105">STRINGTABLE-Ressource</span><span class="sxs-lookup"><span data-stu-id="7e385-105">STRINGTABLE resource</span></span>

<span data-ttu-id="7e385-106">Definiert eine oder mehrere Zeichen folgen Ressourcen für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="7e385-106">Defines one or more string resources for an application.</span></span> <span data-ttu-id="7e385-107">Zeichen folgen Ressourcen sind einfach mit NULL endende Unicode-oder ASCII-Zeichen folgen, die bei Bedarf aus der ausführbaren Datei mithilfe der [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) -Funktion geladen werden können.</span><span class="sxs-lookup"><span data-stu-id="7e385-107">String resources are simply null-terminated Unicode or ASCII strings that can be loaded when needed from the executable file, using the [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa) function.</span></span>

<span data-ttu-id="7e385-108">Es gibt zwei Möglichkeiten, eine **STRINGTABLE** -Anweisung zu formatieren:</span><span class="sxs-lookup"><span data-stu-id="7e385-108">There are two ways to format a **STRINGTABLE** statement:</span></span>

``` syntax
STRINGTABLE  [optional-statements] {stringID string  ...}
```

<span data-ttu-id="7e385-109">\- oder -</span><span class="sxs-lookup"><span data-stu-id="7e385-109">\- or -</span></span>

``` syntax
STRINGTABLE
  [optional-statements]
BEGIN
stringID string
. . .
END
```

## <a name="parameters"></a><span data-ttu-id="7e385-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e385-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e385-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="7e385-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="7e385-112">Dieser Parameter kann NULL oder mehr der folgenden-Anweisungen sein.</span><span class="sxs-lookup"><span data-stu-id="7e385-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="7e385-113">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="7e385-113">Statement</span></span>                                                        | <span data-ttu-id="7e385-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7e385-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e385-115">[**Merkmale**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7e385-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="7e385-116">Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="7e385-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="7e385-117">Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7e385-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="7e385-118">[**Sprach**](language-statement.md) *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="7e385-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="7e385-119">Gibt die Sprache für die Ressource an.</span><span class="sxs-lookup"><span data-stu-id="7e385-119">Specifies the language for the resource.</span></span> <span data-ttu-id="7e385-120">Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7e385-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                              |
| <span data-ttu-id="7e385-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="7e385-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="7e385-122">Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="7e385-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="7e385-123">Weitere Informationen finden Sie unter [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="7e385-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="7e385-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span><span class="sxs-lookup"><span data-stu-id="7e385-124"><span id="stringID"></span><span id="stringid"></span><span id="STRINGID"></span>*stringID*</span></span>
</dt> <dd>

<span data-ttu-id="7e385-125">16-Bit-Ganzzahl ohne Vorzeichen, die die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7e385-125">Unsigned 16-bit integer that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7e385-126"><span id="string"></span><span id="STRING"></span>*Schnür*</span><span class="sxs-lookup"><span data-stu-id="7e385-126"><span id="string"></span><span id="STRING"></span>*string*</span></span>
</dt> <dd>

<span data-ttu-id="7e385-127">Eine oder mehrere Zeichen folgen, die in Anführungszeichen eingeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="7e385-127">One or more strings, enclosed in quotation marks.</span></span> <span data-ttu-id="7e385-128">Die Zeichenfolge darf nicht länger als 4097 Zeichen sein und muss eine einzelne Zeile in der Quelldatei belegen.</span><span class="sxs-lookup"><span data-stu-id="7e385-128">The string must be no longer than 4097 characters and must occupy a single line in the source file.</span></span> <span data-ttu-id="7e385-129">Um der Zeichenfolge einen Wagen Rücklauf hinzuzufügen, verwenden Sie diese Zeichenfolge: \\ 012.</span><span class="sxs-lookup"><span data-stu-id="7e385-129">To add a carriage return to the string, use this character sequence: \\012.</span></span> <span data-ttu-id="7e385-130">Beispiel: "Line One \\ 012line Two" definiert eine Zeichenfolge, die wie folgt angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="7e385-130">For example, "Line one\\012Line two" defines a string that is displayed as follows:</span></span>

``` syntax
Line one
Line two
```

<span data-ttu-id="7e385-131">Um Anführungszeichen in die Zeichenfolge einzubetten, verwenden Sie die folgende Sequenz: "".</span><span class="sxs-lookup"><span data-stu-id="7e385-131">To embed quotes in the string, use the following sequence: "".</span></span> <span data-ttu-id="7e385-132">Beispielsweise wird in "" in Zeile drei "" "eine Zeichenfolge definiert, die wie folgt angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="7e385-132">For example, """Line three""" defines a string that is displayed as follows:</span></span>

``` syntax
"Line three"
```

<span data-ttu-id="7e385-133">Um Unicode-Zeichen zu codieren, verwenden Sie eine "L", gefolgt von den in Anführungszeichen eingeschlossenen Unicode-Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7e385-133">To encode Unicode characters, use an "L" followed by the Unicode characters enclosed by quotes.</span></span> <span data-ttu-id="7e385-134">Ein Beispiel finden Sie im Abschnitt "Beispiele".</span><span class="sxs-lookup"><span data-stu-id="7e385-134">See the Examples section for an example.</span></span>

<span data-ttu-id="7e385-135">Der Ressourcen Compiler unterstützt auch Zeilen Fortsetzungen in der *Zeichenfolge*.</span><span class="sxs-lookup"><span data-stu-id="7e385-135">The resource compiler also supports line continuations in *string*.</span></span> <span data-ttu-id="7e385-136">Ein Beispiel finden Sie im Abschnitt "Beispiele".</span><span class="sxs-lookup"><span data-stu-id="7e385-136">See the Examples section for an example.</span></span>

</dd> </dl>

<span data-ttu-id="7e385-137">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7e385-137">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="7e385-138">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="7e385-138">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7e385-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7e385-139">Remarks</span></span>

<span data-ttu-id="7e385-140">RC ordnet 16 Zeichen folgen pro Abschnitt zu und verwendet den Bezeichnerwert, um zu bestimmen, welcher Abschnitt die Zeichenfolge enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="7e385-140">RC allocates 16 strings per section and uses the identifier value to determine which section is to contain the string.</span></span> <span data-ttu-id="7e385-141">Zeichen folgen, deren Bezeichner sich nur in den unteren 4 Bits unterscheiden, werden im gleichen Abschnitt platziert.</span><span class="sxs-lookup"><span data-stu-id="7e385-141">Strings whose identifiers differ only in the bottom 4 bits are placed in the same section.</span></span> <span data-ttu-id="7e385-142">Weitere Informationen finden Sie unter [Q196774](https://support.microsoft.com/kb/196774).</span><span class="sxs-lookup"><span data-stu-id="7e385-142">For more information, see [Q196774](https://support.microsoft.com/kb/196774).</span></span>

## <a name="examples"></a><span data-ttu-id="7e385-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e385-143">Examples</span></span>

<span data-ttu-id="7e385-144">Das folgende Beispiel veranschaulicht die Verwendung der **STRINGTABLE** -Anweisung zum Anzeigen von ASCII-Zeichen folgen:</span><span class="sxs-lookup"><span data-stu-id="7e385-144">The following example demonstrates the use of the **STRINGTABLE** statement to display ASCII strings:</span></span>

``` syntax
#define IDS_HELLO    1
#define IDS_GOODBYE  2

STRINGTABLE
{
    IDS_HELLO,   "Hello"
    IDS_GOODBYE, "Goodbye"
} 
```

<span data-ttu-id="7e385-145">Im folgenden Beispiel wird gezeigt, wie Unicode-Zeichen codiert werden:</span><span class="sxs-lookup"><span data-stu-id="7e385-145">The following example shows how to encode Unicode characters:</span></span>

``` syntax
STRINGTABLE
BEGINIDS_CHINESESTRING L"\x5e2e\x52a9"
IDS_RUSSIANSTRING L"\x0421\x043f\x0440\x0430\x0432\x043a\x0430"
IDS_ARABICSTRING L"\x062a\x0639\x0644\x064a\x0645\x0627\x062a"
END
```

<span data-ttu-id="7e385-146">Das folgende Beispiel zeigt Zeichen folgen mit ASCII und Unicode.</span><span class="sxs-lookup"><span data-stu-id="7e385-146">The following example shows strings with both ASCII and Unicode.</span></span> <span data-ttu-id="7e385-147">Beachten Sie, dass Zeichen folgen ohne das ursprüngliche "L" das zweistellige escapeformat verwenden:</span><span class="sxs-lookup"><span data-stu-id="7e385-147">Note that strings without the initial "L" use the 2-digit escape format:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_1 L"5\x00BC-Inch Floppy Disk"
IDS_1a "5\xBC-Inch Floppy Disk"
IDS_2 L"Don't confuse \x2229 (intersection) with \x222A (union)"
IDS_3 "Copyright \xA92001"
IDS_3a L"Copyright \x00a92001"
END
```

<span data-ttu-id="7e385-148">Im folgenden Beispiel wird gezeigt, wie Zeilen Fortsetzungen verwendet werden können:</span><span class="sxs-lookup"><span data-stu-id="7e385-148">The following example shows how line continuations can be used:</span></span>

``` syntax
STRINGTABLE
BEGIN
IDS_VERYLONGSTRING "blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah \
blah blah blah blah blah blah"
END
```

## <a name="see-also"></a><span data-ttu-id="7e385-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7e385-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e385-150">**LoadString**</span><span class="sxs-lookup"><span data-stu-id="7e385-150">**LoadString**</span></span>](/windows/win32/api/winuser/nf-winuser-loadstringa)
</dt> <dt>

[<span data-ttu-id="7e385-151">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="7e385-151">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="7e385-152">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="7e385-152">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="7e385-153">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="7e385-153">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="7e385-154">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="7e385-154">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="7e385-155">**RCDATA**</span><span class="sxs-lookup"><span data-stu-id="7e385-155">**RCDATA**</span></span>](rcdata-resource.md)
</dt> <dt>

[<span data-ttu-id="7e385-156">**Version**</span><span class="sxs-lookup"><span data-stu-id="7e385-156">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 