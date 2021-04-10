---
title: RCDATA-Ressource
description: Definiert eine Rohdaten Ressource für eine Anwendung. Rohdaten Ressourcen ermöglichen die direkte Einbindung von Binärdaten in die ausführbare Datei.
ms.assetid: 7535cb06-858b-4726-aaa5-43519f84d0e4
keywords:
- RCDATA-Ressourcen Menüs und andere Ressourcen
topic_type:
- apiref
api_name:
- RCDATA
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44de0e71e3ba744f668535950224129b91bc3653
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948250"
---
# <a name="rcdata-resource"></a><span data-ttu-id="b5e85-105">RCDATA-Ressource</span><span class="sxs-lookup"><span data-stu-id="b5e85-105">RCDATA resource</span></span>

<span data-ttu-id="b5e85-106">Definiert eine Rohdaten Ressource für eine Anwendung.</span><span class="sxs-lookup"><span data-stu-id="b5e85-106">Defines a raw data resource for an application.</span></span> <span data-ttu-id="b5e85-107">Rohdaten Ressourcen ermöglichen die direkte Einbindung von Binärdaten in die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="b5e85-107">Raw data resources permit the inclusion of binary data directly in the executable file.</span></span>

``` syntax
nameID RCDATA  [optional-statements] {raw-data  ...}
```

## <a name="parameters"></a><span data-ttu-id="b5e85-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b5e85-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5e85-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*NameID*</span><span class="sxs-lookup"><span data-stu-id="b5e85-109"><span id="nameID"></span><span id="nameid"></span><span id="NAMEID"></span>*nameID*</span></span>
</dt> <dd>

<span data-ttu-id="b5e85-110">Eindeutiger Name oder ein 16-Bit-ganz Zahl Wert ohne Vorzeichen, der die Ressource identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b5e85-110">Unique name or a 16-bit unsigned integer value that identifies the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b5e85-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optionale-Anweisungen*</span><span class="sxs-lookup"><span data-stu-id="b5e85-111"><span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*optional-statements*</span></span>
</dt> <dd>

<span data-ttu-id="b5e85-112">Dieser Parameter kann NULL oder mehr der folgenden-Anweisungen sein.</span><span class="sxs-lookup"><span data-stu-id="b5e85-112">This parameter can be zero or more of the following statements.</span></span>



| <span data-ttu-id="b5e85-113">-Anweisung.</span><span class="sxs-lookup"><span data-stu-id="b5e85-113">Statement</span></span>                                                        | <span data-ttu-id="b5e85-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5e85-114">Description</span></span>                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5e85-115">[**Merkmale**](characteristics-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b5e85-115">[**CHARACTERISTICS**](characteristics-statement.md) *dword*</span></span>     | <span data-ttu-id="b5e85-116">Benutzerdefinierte Informationen zu einer Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="b5e85-116">User-defined information about a resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="b5e85-117">Weitere Informationen finden Sie unter [**Merkmale**](characteristics-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b5e85-117">For more information, see [**CHARACTERISTICS**](characteristics-statement.md).</span></span> |
| <span data-ttu-id="b5e85-118">[**Sprach**](language-statement.md) *Sprache*, *unter Sprache*</span><span class="sxs-lookup"><span data-stu-id="b5e85-118">[**LANGUAGE**](language-statement.md) *language*, *sublanguage*</span></span> | <span data-ttu-id="b5e85-119">Sprache für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="b5e85-119">Language for the resource.</span></span> <span data-ttu-id="b5e85-120">Weitere Informationen finden Sie unter [**Sprache**](language-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b5e85-120">For more information, see [**LANGUAGE**](language-statement.md).</span></span>                                                                                            |
| <span data-ttu-id="b5e85-121">[**Version**](version-statement.md) *DWORD*</span><span class="sxs-lookup"><span data-stu-id="b5e85-121">[**VERSION**](version-statement.md) *dword*</span></span>                     | <span data-ttu-id="b5e85-122">Eine benutzerdefinierte Versionsnummer für die Ressource, die von Tools verwendet werden kann, die Ressourcen Dateien lesen und schreiben.</span><span class="sxs-lookup"><span data-stu-id="b5e85-122">User-defined version number for the resource that can be used by tools that read and write resource files.</span></span> <span data-ttu-id="b5e85-123">Weitere Informationen finden Sie unter [**Version**](version-statement.md).</span><span class="sxs-lookup"><span data-stu-id="b5e85-123">For more information, see [**VERSION**](version-statement.md).</span></span>              |



 

</dd> <dt>

<span data-ttu-id="b5e85-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*Rohdaten*</span><span class="sxs-lookup"><span data-stu-id="b5e85-124"><span id="raw-data"></span><span id="RAW-DATA"></span>*raw-data*</span></span>
</dt> <dd>

<span data-ttu-id="b5e85-125">Rohdaten, die aus einer oder mehreren Ganzzahlen oder Zeichen folgen bestehen.</span><span class="sxs-lookup"><span data-stu-id="b5e85-125">Raw data consisting of one or more integers or strings of characters.</span></span> <span data-ttu-id="b5e85-126">Ganze Zahlen können im Dezimal-, Oktal-oder Hexadezimal Format angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b5e85-126">Integers can be specified in decimal, octal, or hexadecimal format.</span></span> <span data-ttu-id="b5e85-127">Um mit 16-Bit-Fenstern kompatibel zu sein, werden ganze Zahlen als **Word** -Werte gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b5e85-127">To be compatible with 16-bit Windows, integers are stored as **WORD** values.</span></span> <span data-ttu-id="b5e85-128">Sie können eine ganze Zahl als **DWORD** -Wert speichern, indem Sie die ganze Zahl mit dem Suffix "L" qualifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e85-128">You can store an integer as a **DWORD** value by qualifying the integer with the "L" suffix.</span></span>

<span data-ttu-id="b5e85-129">Zeichen folgen werden in Anführungszeichen eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b5e85-129">Strings are enclosed in quotation marks.</span></span> <span data-ttu-id="b5e85-130">RC fügt kein abschließendes NULL-Zeichen automatisch an eine Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="b5e85-130">RC does not automatically append a terminating null character to a string.</span></span> <span data-ttu-id="b5e85-131">Jede Zeichenfolge ist eine Sequenz der angegebenen ANSI-Zeichen, es sei denn, Sie qualifizieren Sie als breit Zeichen-Zeichenfolge mit dem L-Präfix.</span><span class="sxs-lookup"><span data-stu-id="b5e85-131">Each string is a sequence of the specified ANSI characters, unless you qualify it as a wide-character string with the L prefix.</span></span>

<span data-ttu-id="b5e85-132">Der Datenblock beginnt an einer **DWORD** -Grenze, und RC führt keine Auffüll-oder Ausrichtungs Daten im *RAW-Data-* Block aus.</span><span class="sxs-lookup"><span data-stu-id="b5e85-132">The block of data begins on a **DWORD** boundary and RC performs no padding or alignment of data within the *raw-data* block.</span></span> <span data-ttu-id="b5e85-133">Es liegt in ihrer Verantwortung, die richtige Ausrichtung der Daten innerhalb des Blocks sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="b5e85-133">It is your responsibility to ensure the proper alignment of data within the block.</span></span>

</dd> </dl>

<span data-ttu-id="b5e85-134">Bestimmte Attribute werden auch aus Gründen der Abwärtskompatibilität unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b5e85-134">Certain attributes are also supported for backward compatibility.</span></span> <span data-ttu-id="b5e85-135">Weitere Informationen finden Sie unter [allgemeine Ressourcen Attribute](common-resource-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="b5e85-135">For more information, see [Common Resource Attributes](common-resource-attributes.md).</span></span>

## <a name="examples"></a><span data-ttu-id="b5e85-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b5e85-136">Examples</span></span>

<span data-ttu-id="b5e85-137">Im folgenden Beispiel wird die Verwendung der **RCDATA** -Anweisung veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="b5e85-137">The following example demonstrates the use of the **RCDATA** statement:</span></span>

``` syntax
resname RCDATA
{
   "Here is an ANSI string\0",    // explicitly null-terminated 
   L"Here is a Unicode string\0", // explicitly null-terminated 
   1024,                          // integer, stored as WORD 
   7L,                            // integer, stored as DWORD 
   0x029a,                        // hex integer 
   0o733,                         // octal integer 
}
```

## <a name="see-also"></a><span data-ttu-id="b5e85-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5e85-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5e85-139">**Accelerators**</span><span class="sxs-lookup"><span data-stu-id="b5e85-139">**ACCELERATORS**</span></span>](accelerators-resource.md)
</dt> <dt>

[<span data-ttu-id="b5e85-140">**Charakteristik**</span><span class="sxs-lookup"><span data-stu-id="b5e85-140">**CHARACTERISTICS**</span></span>](characteristics-statement.md)
</dt> <dt>

[<span data-ttu-id="b5e85-141">**Kurse**</span><span class="sxs-lookup"><span data-stu-id="b5e85-141">**LANGUAGE**</span></span>](language-statement.md)
</dt> <dt>

[<span data-ttu-id="b5e85-142">**Stehen**</span><span class="sxs-lookup"><span data-stu-id="b5e85-142">**MENU**</span></span>](menu-resource.md)
</dt> <dt>

[<span data-ttu-id="b5e85-143">**STRINGTABLE**</span><span class="sxs-lookup"><span data-stu-id="b5e85-143">**STRINGTABLE**</span></span>](stringtable-resource.md)
</dt> <dt>

[<span data-ttu-id="b5e85-144">**Version**</span><span class="sxs-lookup"><span data-stu-id="b5e85-144">**VERSION**</span></span>](version-statement.md)
</dt> </dl>

 

 




