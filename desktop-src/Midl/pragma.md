---
title: pragma-Attribut
description: Die Anweisung \ Pragma Mittel l \_ Echo weist die angegebene Zeichenfolge ohne Anführungszeichen in der generierten Header Datei an.
ms.assetid: b8a175d2-ea07-4103-ab45-0de7e477d27a
keywords:
- pragma-Attribut-Mittel l
topic_type:
- apiref
api_name:
- pragma
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72f5e1c00c089bc8915adc2d9f3363305c677a96
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948125"
---
# <a name="pragma-attribute"></a><span data-ttu-id="a223b-104">pragma-Attribut</span><span class="sxs-lookup"><span data-stu-id="a223b-104">pragma attribute</span></span>

<span data-ttu-id="a223b-105">Mit der Pragma-Anweisung "-Echo" wird die \# angegebene Zeichenfolge (ohne Anführungszeichen) in der generierten Header Datei durch die-Anweisung des- **pragma \_** -Attributs ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="a223b-105">The \#**pragma midl\_echo** directive instructs MIDL to emit the specified string, without the quotation characters, into the generated header file.</span></span>

``` syntax
#pragma midl_echo("string")
#pragma token-sequence
#pragma pack (n)
#pragma pack ( [push] [, id] [, n} )
#pragma pack ( [pop] [, id] [, n} )
```

## <a name="parameters"></a><span data-ttu-id="a223b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a223b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a223b-107">*string*</span><span class="sxs-lookup"><span data-stu-id="a223b-107">*string*</span></span> 
</dt> <dd>

<span data-ttu-id="a223b-108">Gibt eine Zeichenfolge an, die in die generierte Header Datei eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="a223b-108">Specifies a string that is inserted into the generated header file.</span></span> <span data-ttu-id="a223b-109">Die Anführungszeichen werden während des Einfügevorgangs entfernt.</span><span class="sxs-lookup"><span data-stu-id="a223b-109">The quotation marks are removed during the insertion process.</span></span>

</dd> <dt>

<span data-ttu-id="a223b-110">*tokensequenz*</span><span class="sxs-lookup"><span data-stu-id="a223b-110">*token-sequence*</span></span> 
</dt> <dd>

<span data-ttu-id="a223b-111">Gibt eine Sequenz von Token an, die in die generierte Header Datei als Teil einer **\# pragma** -Direktive eingefügt werden, ohne dass vom Mittelwert Compiler verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="a223b-111">Specifies a sequence of tokens that are inserted into the generated header file as part of a **\#pragma** directive without processing by the MIDL compiler.</span></span>

</dd> <dt>

<span data-ttu-id="a223b-112">*n*</span><span class="sxs-lookup"><span data-stu-id="a223b-112">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="a223b-113">Gibt die aktuelle Paketgröße an.</span><span class="sxs-lookup"><span data-stu-id="a223b-113">Specifies the current pack size.</span></span> <span data-ttu-id="a223b-114">Gültige Werte sind 1, 2, 4, 8 und 16.</span><span class="sxs-lookup"><span data-stu-id="a223b-114">Valid values are 1, 2, 4, 8, and 16.</span></span>

</dd> <dt>

<span data-ttu-id="a223b-115">*id*</span><span class="sxs-lookup"><span data-stu-id="a223b-115">*id*</span></span> 
</dt> <dd>

<span data-ttu-id="a223b-116">Gibt die Benutzer-ID an.</span><span class="sxs-lookup"><span data-stu-id="a223b-116">Specifies the user identifier.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a223b-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a223b-117">Remarks</span></span>

<span data-ttu-id="a223b-118">In der IDL-Datei angezeigte Vorverarbeitung-Direktiven der c-Sprache werden vom Präprozessor des C-Compilers verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a223b-118">C-language preprocessing directives that appear in the IDL file are processed by the C compiler's preprocessor.</span></span> <span data-ttu-id="a223b-119">Die **\# define** -Direktiven in der IDL-Datei sind während der Kompilierungs Kompilierung verfügbar, aber nicht für den C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="a223b-119">The **\#define** directives in the IDL file are available during MIDL compilation, although not to the C compiler.</span></span>

<span data-ttu-id="a223b-120">Wenn der Präprozessor z. b. auf die Direktive " \# Windows 4 definieren" stößt, ersetzt der Präprozessor alle Vorkommen von "Windows" in der IDL-Datei durch "4".</span><span class="sxs-lookup"><span data-stu-id="a223b-120">For example, when the preprocessor encounters the directive "\#define WINDOWS 4", the preprocessor replaces all occurrences of "WINDOWS" in the IDL file with "4".</span></span> <span data-ttu-id="a223b-121">Das Symbol "Windows" ist zum Zeitpunkt der C-Kompilierung nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a223b-121">The symbol "WINDOWS" is not available at C-compile time.</span></span>

<span data-ttu-id="a223b-122">Um zuzulassen, dass die c-präprozessormakrodefinitionen den Mittel l-Compiler an den c-Compiler übergeben, verwenden Sie die- **\# pragma \_** -Anweisung "-Echo" oder " [**cpp- \_ Anführungs**](cpp-quote.md) Zeichen".</span><span class="sxs-lookup"><span data-stu-id="a223b-122">To allow the C-preprocessor macro definitions to pass through the MIDL compiler to the C compiler, use the **\#pragma midl\_echo** or [**cpp\_quote**](cpp-quote.md) directive.</span></span> <span data-ttu-id="a223b-123">Diese Direktiven weisen den Mittelwert Compiler an, eine Header Datei zu generieren, die die Parameter Zeichenfolge enthält, wobei die Anführungszeichen entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="a223b-123">These directives instruct the MIDL compiler to generate a header file that contains the parameter string with the quotation marks removed.</span></span> <span data-ttu-id="a223b-124">Die Anweisungs-und **cpp- \_** Anweisungs Direktiven von **\# pragma \_** sind gleichwertig.</span><span class="sxs-lookup"><span data-stu-id="a223b-124">The **\#pragma midl\_echo** and **cpp\_quote** directives are equivalent.</span></span>

<span data-ttu-id="a223b-125">Die **\# pragma pack** -Direktive wird vom Mittelwert Compiler zum Steuern der Verpackung von Strukturen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a223b-125">The **\#pragma pack** directive is used by the MIDL compiler to control the packing of structures.</span></span> <span data-ttu-id="a223b-126">Er überschreibt den [**/ZP**](-zp.md) -Befehls Zeilenschalter.</span><span class="sxs-lookup"><span data-stu-id="a223b-126">It overrides the [**/Zp**](-zp.md) command-line switch.</span></span> <span data-ttu-id="a223b-127">Die Option Pack (*n*) legt die aktuelle Paketgröße auf einen bestimmten Wert fest: 1, 2, 4, 8 oder 16.</span><span class="sxs-lookup"><span data-stu-id="a223b-127">The pack (*n*) option sets the current pack size to a specific value: 1, 2, 4, 8, or 16.</span></span> <span data-ttu-id="a223b-128">Die Optionen Pack (Push) und Pack (Pop) weisen die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="a223b-128">The pack (push) and pack (pop) options have the following characteristics:</span></span>

-   <span data-ttu-id="a223b-129">Der Compiler behält einen Verpackungs Stapel bei.</span><span class="sxs-lookup"><span data-stu-id="a223b-129">The compiler maintains a packing stack.</span></span> <span data-ttu-id="a223b-130">Die Elemente des Verpackungs Stapels enthalten eine Paketgröße und eine optionale *ID*. Der Stapel wird nur durch den verfügbaren Arbeitsspeicher mit der aktuellen Paketgröße am oberen Rand des Stapels beschränkt.</span><span class="sxs-lookup"><span data-stu-id="a223b-130">The elements of the packing stack include a pack size and an optional *id*. The stack is limited only by available memory with the current pack size at the top of the stack.</span></span>
-   <span data-ttu-id="a223b-131">Pack (Push) führt dazu, dass die aktuelle Paketgröße auf den Verpackungs Stapel verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="a223b-131">Pack (push) results in the current pack size pushed onto the packing stack.</span></span> <span data-ttu-id="a223b-132">Der Stapel ist durch den verfügbaren Arbeitsspeicher begrenzt.</span><span class="sxs-lookup"><span data-stu-id="a223b-132">The stack is limited by available memory.</span></span>
-   <span data-ttu-id="a223b-133">Pack (Push,*n*) ist das gleiche wie Pack (Push), gefolgt von Pack (*n*).</span><span class="sxs-lookup"><span data-stu-id="a223b-133">Pack (push,*n*) is the same as pack (push) followed by pack (*n*).</span></span>
-   <span data-ttu-id="a223b-134">Pack (Push, *ID*) überträgt ebenfalls die *ID* zusammen mit der Paketgröße auf den Verpackungs Stapel.</span><span class="sxs-lookup"><span data-stu-id="a223b-134">Pack (push, *id*) also pushes *id* onto the packing stack along with the pack size.</span></span>
-   <span data-ttu-id="a223b-135">Pack (Push, *ID*, *n*) ist das gleiche wie Pack (Push, *ID*), gefolgt von Paket (*n*).</span><span class="sxs-lookup"><span data-stu-id="a223b-135">Pack (push, *id*, *n*) is the same as pack (push, *id*) followed by pack (*n*).</span></span>
-   <span data-ttu-id="a223b-136">Pack (Pop) führt zu einem Pop in den Verpackungs Stapel.</span><span class="sxs-lookup"><span data-stu-id="a223b-136">Pack (pop) results in popping the packing stack.</span></span> <span data-ttu-id="a223b-137">Unausgeglichene POPs verursachen Warnungen und legen die aktuelle Paketgröße auf den Befehlszeilen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="a223b-137">Unbalanced pops cause warnings and set the current pack size to the command-line value.</span></span>
-   <span data-ttu-id="a223b-138">Wenn Pack (Pop, *ID*, *n*) angegeben wird, wird *n* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a223b-138">If pack (pop, *id*, *n*) is specified, then *n* is ignored.</span></span>

<span data-ttu-id="a223b-139">Der-compilercompiler fügt die in den [**\\ cpp- \_ Anführungs**](cpp-quote.md) Zeichen und- **pragma** -Direktiven angegebenen Zeichen folgen in der-Header Datei in der Reihenfolge ein, in der Sie in der IDL-Datei und relativ zu anderen Schnittstellen Komponenten in der IDL-Datei angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="a223b-139">The MIDL compiler places the strings specified in the [**\\cpp\_quote**](cpp-quote.md) and **pragma** directives in the header file in the sequence in which they are specified in the IDL file and relative to other interface components in the IDL file.</span></span> <span data-ttu-id="a223b-140">Die Zeichen folgen sollten in der Regel im Schnittstellen Textabschnitt der IDL-Datei nach allen [**Import**](import.md) Vorgängen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a223b-140">The strings should usually appear in the interface-body section of the IDL file after all [**import**](import.md) operations.</span></span>

<span data-ttu-id="a223b-141">Der mittlerer l-Compiler versucht nicht, **\# pragma** -Direktiven zu verarbeiten, die nicht mit dem Präfix "Mittel l \_ " beginnen.</span><span class="sxs-lookup"><span data-stu-id="a223b-141">The MIDL compiler does not attempt to process **\#pragma** directives that do not start with the prefix "midl\_."</span></span> <span data-ttu-id="a223b-142">Andere **\# pragma** -Direktiven in der IDL-Datei werden ohne Änderungen an die generierte Header Datei übermittelt.</span><span class="sxs-lookup"><span data-stu-id="a223b-142">Other **\#pragma** directives in the IDL file are passed into the generated header file without changes.</span></span>

## <a name="examples"></a><span data-ttu-id="a223b-143">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a223b-143">Examples</span></span>

``` syntax
/* IDL file */ 
#pragma midl_echo("#define UNICODE") 
cpp_quote("#define __DELAYED_PREPROCESSING__ 1") 
#pragma hdrstop 
#pragma check_pointer(on) 
 
/* generated header file */ 
#define UNICODE 
#define __DELAYED_PREPROCESSING__ 1 
#pragma hdrstop 
#pragma check_pointer(on)
```

## <a name="see-also"></a><span data-ttu-id="a223b-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="a223b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a223b-145">**cpp- \_ Angebot**</span><span class="sxs-lookup"><span data-stu-id="a223b-145">**cpp\_quote**</span></span>](cpp-quote.md)
</dt> <dt>

[<span data-ttu-id="a223b-146">Schnittstellen Definitionsdatei (IDL)</span><span class="sxs-lookup"><span data-stu-id="a223b-146">Interface Definition (IDL) File</span></span>](interface-definition-idl-file.md)
</dt> <dt>

[<span data-ttu-id="a223b-147">**Importieren**</span><span class="sxs-lookup"><span data-stu-id="a223b-147">**import**</span></span>](import.md)
</dt> <dt>

[<span data-ttu-id="a223b-148">**/ZP**</span><span class="sxs-lookup"><span data-stu-id="a223b-148">**/Zp**</span></span>](-zp.md)
</dt> </dl>

 

 




