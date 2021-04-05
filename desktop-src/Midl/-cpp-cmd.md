---
title: /cpp_cmd Schalter
description: Der/cpp- \_ cmd-Schalter gibt den Präprozessor an, den der Mittell-Compiler verwendet, um Eingabedateien vorzuverarbeiten.
ms.assetid: d6261fdd-155d-4327-b254-d0267f0dec69
keywords:
- /cpp_cmd-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /cpp_cmd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ad693f8dbf3ddc7acda6539b89930972ca81a87
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718696"
---
# <a name="cpp_cmd-switch"></a><span data-ttu-id="c9bc8-104">/cpp- \_ cmd-Schalter</span><span class="sxs-lookup"><span data-stu-id="c9bc8-104">/cpp\_cmd switch</span></span>

<span data-ttu-id="c9bc8-105">Der **/cpp- \_ cmd** -Schalter gibt den Präprozessor an, den der Mittell-Compiler verwendet, um Eingabedateien vorzuverarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-105">The **/cpp\_cmd** switch specifies the preprocessor that the MIDL compiler uses to preprocess input files.</span></span>

``` syntax
midl /cpp_cmd "C_preprocessor_binary"
```

## <a name="switch-options"></a><span data-ttu-id="c9bc8-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="c9bc8-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="c9bc8-107">*C- \_ \_ präprozessorbinär Datei*</span><span class="sxs-lookup"><span data-stu-id="c9bc8-107">*C\_preprocessor\_binary*</span></span> 
</dt> <dd>

<span data-ttu-id="c9bc8-108">Gibt den Befehl an, der den Präprozessor aufruft.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-108">Specifies the command that invokes the preprocessor.</span></span> <span data-ttu-id="c9bc8-109">Dieser Befehl ermöglicht es Entwicklern, den standardpräprozessor zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-109">This command allows developers to override the default preprocessor.</span></span> <span data-ttu-id="c9bc8-110">Standardmäßig ruft die Mittel l den Microsoft C/C++-Compiler aus der Buildumgebung des Buildcomputers auf.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-110">By default, MIDL invokes the Microsoft C/C++ compiler from the build machine's build environment.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9bc8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c9bc8-111">Remarks</span></span>

<span data-ttu-id="c9bc8-112">Das *\_ \_ binäre C-präprozessorargument* für den Switch kann den vollständigen Pfad angeben. das exe-Suffix und die Anführungszeichen sind optional.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-112">The *C\_preprocessor\_binary* argument to the switch may specify the full path; the exe suffix and quotes are optional.</span></span> <span data-ttu-id="c9bc8-113">In der Regel verwenden Entwickler den-Schalter, um eine bestimmte Version des Microsoft C/C++-präprozessorprozesses oder einer entsprechenden Version in der Buildumgebung auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-113">Typically, developers use the switch to choose a particular version of the Microsoft C/C++ preprocessor or equivalent in the build environment.</span></span> <span data-ttu-id="c9bc8-114">In diesem Fall ist es nicht erforderlich, den Schalter " [**/cpp \_ opt**](-cpp-opt.md) " mit **/cpp \_ cmd** zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-114">In this case, it is not necessary to use the [**/cpp\_opt**](-cpp-opt.md) switch with **/cpp\_cmd**.</span></span>

<span data-ttu-id="c9bc8-115">Wenn ein nicht-Microsoft-Präprozessor verwendet wird, insbesondere wenn der angegebene Präprozessor seine Ausgabe nicht an stdout weiterleitet, muss der C-Compilerschalter, der die Ausgabe an stdout umleitet, als Teil des Mittell-Compilers [**/cpp \_ opt**](-cpp-opt.md) -Schalter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-115">When using a non-Microsoft preprocessor, especially when the specified preprocessor does not direct its output to stdout, the C compiler switch that redirects output to stdout as part of the MIDL compiler [**/cpp\_opt**](-cpp-opt.md) switch must be specified.</span></span> <span data-ttu-id="c9bc8-116">Weitere Informationen finden Sie unter [C-präprozessoranforderungen für die mittlere](c-preprocessor-requirements-for-midl.md)</span><span class="sxs-lookup"><span data-stu-id="c9bc8-116">See [C-Preprocessor Requirements for MIDL](c-preprocessor-requirements-for-midl.md) for details</span></span>

<span data-ttu-id="c9bc8-117">Der Präprozessor wird durch eine Befehls Zeichenfolge aufgerufen, die aus den Informationen besteht, die von den **/cpp \_ cmd**-, [**/cpp \_ opt**](-cpp-opt.md)- [**,/D**](-d.md)-, [**/I**](-i.md)-und [**/U**](-u.md) -Switches an den Mittelwert des compl-Compilers</span><span class="sxs-lookup"><span data-stu-id="c9bc8-117">The preprocessor is invoked by a command string that is formed from the information provided to the MIDL compiler by **/cpp\_cmd**, [**/cpp\_opt**](-cpp-opt.md), [**/D**](-d.md), [**/I**](-i.md), and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="c9bc8-118">In der folgenden Tabelle wird zusammengefasst, wie die Befehls Zeichenfolge für jede Kombination aus **/cpp- \_ cmd** -und **/cpp- \_ opt** -Switches</span><span class="sxs-lookup"><span data-stu-id="c9bc8-118">The following table summarizes how the command string is constructed for each combination of **/cpp\_cmd** and **/cpp\_opt** switches.</span></span>

<span data-ttu-id="c9bc8-119">Wenn der **/cpp- \_ cmd** -Schalter nicht angegeben ist, ruft der kompil-Compiler den Microsoft C/C++-Compiler auf.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-119">When the **/cpp\_cmd** switch is not specified, the MIDL compiler invokes the Microsoft C/C++ compiler.</span></span> <span data-ttu-id="c9bc8-120">In der Buildumgebung wird von der mittleren l eine Cl.exe Binärdatei verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-120">MIDL uses a Cl.exe binary found in the build environment.</span></span>

<span data-ttu-id="c9bc8-121">Wenn der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " nicht vorhanden ist, verkettet der Mittell-Compiler die durch den **/cpp- \_ cmd** -Schalter angegebene Zeichenfolge mit den Informationen, die von den Optionen für die mittlere [**/I**](-i.md), [**/D**](-d.md) und [**/U**](-u.md) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-121">When the [**/cpp\_opt**](-cpp-opt.md) switch is not present, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the information specified by the MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) options.</span></span> <span data-ttu-id="c9bc8-122">Die Zeichenfolge/E wird auch mit der Aufruf Zeichenfolge für den c-Compiler verkettet, um anzugeben, dass der c/C++-Compiler nur die Vorverarbeitung durchführen soll.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-122">The string /E is also concatenated to the C-compiler invocation string to indicate that the C/C++ compiler should perform preprocessing only.</span></span> <span data-ttu-id="c9bc8-123">Der Schalter [**/nologo**](-nologo.md) wird hinzugefügt, um das C/C++-compilerbanner zu unterdrücken.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-123">The [**/nologo**](-nologo.md) switch is added to suppress the C/C++ compiler banner.</span></span> <span data-ttu-id="c9bc8-124">Der mittlerer l-Compiler verwendet die verketteten Zeichenfolge, um den C-Präprozessor für IDL auf oberster Ebene sowie importierte IDL-Dateien und auch für alle vorhandenen, entsprechenden ACF-Dateien aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-124">The MIDL compiler uses the concatenated string to invoke the C preprocessor for top-level IDL as well as imported IDL files, and also for any present, corresponding ACF files.</span></span>

<span data-ttu-id="c9bc8-125">Wenn der Schalter " [**/cpp \_ opt**](-cpp-opt.md) " vorhanden ist, was für die aktuellen 32-Bit-und 64-Bit-Plattformen in seltenen Fällen der Fall sein sollte, verkettet der Mittelwert Compiler die durch den Schalter " **/cpp \_ cmd** " angegebene Zeichenfolge mit der durch den **/cpp- \_ opt** -Schalter angegebenen Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-125">When the [**/cpp\_opt**](-cpp-opt.md) switch is present, which should be a rare case for the current 32-bit and 64-bit platforms, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the string specified by the **/cpp\_opt** switch.</span></span> <span data-ttu-id="c9bc8-126">Der mittlerer l-Compiler verwendet die verketteten Zeichenfolge, um die festgestellte präprozessorbinär Datei anstelle des standardpräprozessors aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-126">The MIDL compiler uses the concatenated string to invoke the indicated preprocessor binary in place of the default preprocessor.</span></span> <span data-ttu-id="c9bc8-127">Wenn der **Schalter/cpp \_ opt** vorhanden ist, werden weder die von den Switches [**/I**](-i.md), [**/D**](-d.md)und [**/U**](-u.md) angegebenen Mittelwert-Compileroptionen noch der C-Compilerschalter/E mit der Zeichenfolge verkettet.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-127">When the **/cpp\_opt** switch is present, neither the MIDL compiler options specified by the [**/I**](-i.md), [**/D**](-d.md), and [**/U**](-u.md) switches nor the C compiler switch /E is concatenated with the string.</span></span> <span data-ttu-id="c9bc8-128">Sie müssen die/E-Option oder eine entsprechende Option als Teil der Zeichenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-128">You must supply the /E option, or equivalent, as part of the string.</span></span>



| <span data-ttu-id="c9bc8-129">/cpp \_ cmd vorhanden?</span><span class="sxs-lookup"><span data-stu-id="c9bc8-129">/cpp\_cmd present?</span></span> | <span data-ttu-id="c9bc8-130">/cpp \_ opt vorhanden?</span><span class="sxs-lookup"><span data-stu-id="c9bc8-130">/cpp\_opt present?</span></span> | <span data-ttu-id="c9bc8-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c9bc8-131">Description</span></span>                                                                                                                                                                                                       |
|--------------------|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bc8-132">Nein (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9bc8-132">No (default)</span></span>       | <span data-ttu-id="c9bc8-133">Nein (Standard)</span><span class="sxs-lookup"><span data-stu-id="c9bc8-133">No (default)</span></span>       | <span data-ttu-id="c9bc8-134">Ruft den Microsoft C/C++-Standard Compiler mit Einstellungen auf, die von der Option "mittlere [**/I**](-i.md)", " [**/D**](-d.md) " und " [**/U**](-u.md) "</span><span class="sxs-lookup"><span data-stu-id="c9bc8-134">Invokes the default Microsoft C/C++ compiler with settings obtained from MIDL [**/I**](-i.md), [**/D**](-d.md) and [**/U**](-u.md) switches.</span></span> <span data-ttu-id="c9bc8-135">Fügt die präprozessorschalter/E und [**/nologo**](-nologo.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-135">Adds the preprocessor switches /E and [**/nologo**](-nologo.md).</span></span> |
| <span data-ttu-id="c9bc8-136">Ja</span><span class="sxs-lookup"><span data-stu-id="c9bc8-136">Yes</span></span>                | <span data-ttu-id="c9bc8-137">Nein</span><span class="sxs-lookup"><span data-stu-id="c9bc8-137">No</span></span>                 | <span data-ttu-id="c9bc8-138">Ruft die angegebene präprozessorbinär Datei mit denselben Switches wie oben auf.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-138">Invokes the indicated preprocessor binary with the same switches as above.</span></span>                                                                                                                                        |
| <span data-ttu-id="c9bc8-139">Nein</span><span class="sxs-lookup"><span data-stu-id="c9bc8-139">No</span></span>                 | <span data-ttu-id="c9bc8-140">Ja</span><span class="sxs-lookup"><span data-stu-id="c9bc8-140">Yes</span></span>                | <span data-ttu-id="c9bc8-141">Ruft den Microsoft C-Compiler mit den angegebenen Optionen auf.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-141">Invokes the Microsoft C compiler with specified options.</span></span> <span data-ttu-id="c9bc8-142">Verwendet keine Optionen für die Option " [**/I**](-i.md)", " [**/D**](-d.md)" und " [**/U**](-u.md) ".</span><span class="sxs-lookup"><span data-stu-id="c9bc8-142">Does not use MIDL [**/I**](-i.md), [**/D**](-d.md), [**/U**](-u.md) options.</span></span> <span data-ttu-id="c9bc8-143">Sie müssen/E als Teil von [**/cpp \_ opt**](-cpp-opt.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-143">You must supply /E as part of [**/cpp\_opt**](-cpp-opt.md).</span></span>             |
| <span data-ttu-id="c9bc8-144">Ja</span><span class="sxs-lookup"><span data-stu-id="c9bc8-144">Yes</span></span>                | <span data-ttu-id="c9bc8-145">Ja</span><span class="sxs-lookup"><span data-stu-id="c9bc8-145">Yes</span></span>                | <span data-ttu-id="c9bc8-146">Ruft die angegebene präprozessorbinär Datei mit den angegebenen Optionen auf.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-146">Invokes the specified preprocessor binary with specified options only.</span></span> <span data-ttu-id="c9bc8-147">Sie müssen Anführungszeichen verwenden.</span><span class="sxs-lookup"><span data-stu-id="c9bc8-147">You must use quotes.</span></span>                                                                                                                       |



 

## <a name="examples"></a><span data-ttu-id="c9bc8-148">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9bc8-148">Examples</span></span>

<span data-ttu-id="c9bc8-149">**Mittel l/cpp \_ cmd d: \\ NT \\ Tools \\ ia64 \\cl.exe/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-149">**midl /cpp\_cmd d:\\nt\\tools\\ia64\\cl.exe /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c9bc8-150">**Mittel l/cpp \_ cmd "mycpp"/DFLAG = true/IC: \\ Inc filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-150">**midl /cpp\_cmd "mycpp" /DFLAG=TRUE /Ic:\\inc filename.idl**</span></span>

<span data-ttu-id="c9bc8-151">**Mittel l/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-151">**midl /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

<span data-ttu-id="c9bc8-152">**Mittel l/cpp \_ cmd "CL"/cpp \_ Opt "/E/DFLAG = true/IC: \\ Inc" Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-152">**midl /cpp\_cmd "cl" /cpp\_opt "/E /DFLAG=TRUE /Ic:\\inc" filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c9bc8-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9bc8-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9bc8-154">**/savePP**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-154">**/savePP**</span></span>](-savepp.md)
</dt> <dt>

[<span data-ttu-id="c9bc8-155">**/cpp \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-155">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="c9bc8-156">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c9bc8-156">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c9bc8-157">**/No \_ cpp**</span><span class="sxs-lookup"><span data-stu-id="c9bc8-157">**/no\_cpp**</span></span>](-no-cpp-nocpp.md)
</dt> <dt>

[<span data-ttu-id="c9bc8-158">C-präprozessoranforderungen für die Mittel l</span><span class="sxs-lookup"><span data-stu-id="c9bc8-158">C-Preprocessor Requirements for MIDL</span></span>](c-preprocessor-requirements-for-midl.md)
</dt> </dl>

 

 




