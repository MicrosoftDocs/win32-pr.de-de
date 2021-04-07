---
title: /char-Schalter
description: Mithilfe des/Char-Schalters können Sie sicherstellen, dass der Mittelwert Compiler und der C-Compiler ordnungsgemäß für alle char-und Small-Typen funktionieren.
ms.assetid: 83f204cf-9cd0-42f3-bce7-b8f582e50e67
keywords:
- /char-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /char
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2254db9d0f4efcd003362e4126c5c295ca532b2f
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718702"
---
# <a name="char-switch"></a><span data-ttu-id="c7178-104">/char-Schalter</span><span class="sxs-lookup"><span data-stu-id="c7178-104">/char switch</span></span>

<span data-ttu-id="c7178-105">Mithilfe des **/char** -Schalters können Sie sicherstellen, dass der Mittelwert Compiler und der C-Compiler ordnungsgemäß für alle [**char**](char-idl.md) -und [**Small**](small.md) -Typen funktionieren.</span><span class="sxs-lookup"><span data-stu-id="c7178-105">The **/char** switch helps to ensure that the MIDL compiler and C compiler operate together correctly for all [**char**](char-idl.md) and [**small**](small.md) types.</span></span>

``` syntax
midl /char { signed | unsigned | ascii7 }
```

## <a name="switch-options"></a><span data-ttu-id="c7178-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="c7178-106">Switch Options</span></span>

<dl> <dt>

 
</dt> <dd>

<dt>

<span id="signed"></span><span id="SIGNED"></span>

<span data-ttu-id="c7178-107"><span id="signed"></span><span id="SIGNED"></span>signiert \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c7178-107"><span id="signed"></span><span id="SIGNED"></span>\*\*\*\*signed\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c7178-108">Gibt an, dass der C-Compiler-Standard Typ für [**char**](char-idl.md) signiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7178-108">Specifies that the default C-compiler type for [**char**](char-idl.md) is signed.</span></span> <span data-ttu-id="c7178-109">Alle Vorkommen von **char** , die nicht von einer Vorzeichen Spezifikation begleitet werden, werden als unsigniertes char generiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-109">All occurrences of **char** not accompanied by a sign specification are generated as unsigned char.</span></span>

</dd> <dt>

<span id="unsigned"></span><span id="UNSIGNED"></span>

<span data-ttu-id="c7178-110"><span id="unsigned"></span><span id="UNSIGNED"></span>nicht signiert \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c7178-110"><span id="unsigned"></span><span id="UNSIGNED"></span>\*\*\*\*unsigned\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c7178-111">Gibt an, dass der Standard-C-Compilertyp für [**char**](char-idl.md) nicht signiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7178-111">Specifies that the default C-compiler type for [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="c7178-112">Alle Verwendungszwecke von [**Small**](small.md) , die nicht von einer Signierungs Spezifikation begleitet werden, werden als klein signiert generiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-112">All uses of [**small**](small.md) not accompanied by a sign specification are generated as signed small.</span></span>

</dd> <dt>

<span id="ascii7"></span><span id="ASCII7"></span>

<span data-ttu-id="c7178-113"><span id="ascii7"></span><span id="ASCII7"></span>ASCII7 \* \* \* \*</span><span class="sxs-lookup"><span data-stu-id="c7178-113"><span id="ascii7"></span><span id="ASCII7"></span>\*\*\*\*ascii7\*\*\*\*</span></span>


</dt> <dd>

<span data-ttu-id="c7178-114">Gibt an, dass alle [**char**](char-idl.md) -Werte ohne bestimmtes Signierungs Schlüsselwort an die generierten Dateien übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c7178-114">Specifies that all [**char**](char-idl.md) values are to be passed into the generated files without a specific sign keyword.</span></span> <span data-ttu-id="c7178-115">Alle Verwendungszwecke von " [**Small**](small.md) ", die nicht von einer Vorzeichen Spezifikation begleitet werden, werden als **klein** generiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-115">All uses of [**small**](small.md) not accompanied by a sign specification are generated as **small**.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c7178-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c7178-116">Remarks</span></span>

<span data-ttu-id="c7178-117">Definitions [**gemäß ist "**](char-idl.md) Mittelwert Zeichen" nicht signiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-117">By definition, MIDL [**char**](char-idl.md) is unsigned.</span></span> <span data-ttu-id="c7178-118">"Small" ist im Hinblick auf **char** ( \# define Small Char) und in der Mitte [**Small**](small.md) signiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-118">"Small" is defined in terms of **char** (\#define small char), and MIDL [**small**](small.md) is signed.</span></span>

<span data-ttu-id="c7178-119">Der **/char** -Schalter weist den Mittelwert Compiler an, explizite [**signierte**](signed.md) oder [**unsignierte**](unsigned.md) Deklarationen in den generierten Dateien anzugeben, wenn die C-compilersignier Deklaration mit dem Standardwert für diesen Typ in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="c7178-119">The **/char** switch directs the MIDL compiler to specify explicit [**signed**](signed.md) or [**unsigned**](unsigned.md) declarations in the generated files when the C-compiler sign declaration conflicts with the MIDL default for that type.</span></span>

<span data-ttu-id="c7178-120">Beachten Sie, dass der mittlerer l-Compiler die Stub als C-Quellcode generiert, den Sie als Teil der Client-und Serverprogramme kompilieren müssen.</span><span class="sxs-lookup"><span data-stu-id="c7178-120">Remember that the MIDL compiler generates the stubs as C source code, which you must compile as part of your client and server programs.</span></span> <span data-ttu-id="c7178-121">Einige Compiler verwenden eine **signierte char** Everywhere [**-**](char-idl.md) Daten, die im Quellcode angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c7178-121">Some compilers use a **signed char** everywhere [**char**](char-idl.md) data is specified in the source code.</span></span> <span data-ttu-id="c7178-122">Der stubquellcode, den der Mittell-Compiler generiert, behandelt alle **char** -Daten als **unsigniertes char**.</span><span class="sxs-lookup"><span data-stu-id="c7178-122">The stub source code that the MIDL compiler generates treats all **char** data as **unsigned char**.</span></span> <span data-ttu-id="c7178-123">Wenn der Mittell-Compiler einfach alle **char** -Daten in der IDL-Datei als **char** -Daten in den Stubs generiert hat, verursachen Compiler, die ein **signiertes char** für **char** -Daten verwenden, einen Konflikt im stubquellcode.</span><span class="sxs-lookup"><span data-stu-id="c7178-123">If the MIDL compiler simply generated all **char** data in the IDL file as **char** data in the stubs, compilers that use a **signed char** for **char** data would cause a conflict in the stub source code.</span></span>

<span data-ttu-id="c7178-124">Der Zweck des Befehls Zeilenschalters **/char** besteht darin, diese potenziellen Konflikte zu beheben.</span><span class="sxs-lookup"><span data-stu-id="c7178-124">The purpose of the **/char** command line switch is to resolve these potential conflicts.</span></span> <span data-ttu-id="c7178-125">Alle Daten, die als " [**char**](char-idl.md) " in der IDL-Datei angegeben sind, werden im stubquellcode als **Ganzzahl ohne Vorzeichen char** -Zeichen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c7178-125">It preserves all data specified as [**char**](char-idl.md) in the IDL file as **unsigned char** in the stub source code.</span></span> <span data-ttu-id="c7178-126">Außerdem werden [**kleine**](small.md) Daten als signiert verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c7178-126">It also maintains [**small**](small.md) data as signed.</span></span>

<span data-ttu-id="c7178-127">In der folgenden Tabelle werden die generierten Typen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="c7178-127">The following table summarizes the generated types.</span></span>



| <span data-ttu-id="c7178-128">Mittel l/char (Option)</span><span class="sxs-lookup"><span data-stu-id="c7178-128">midl /char option</span></span>       | <span data-ttu-id="c7178-129">Generierter char-Typ</span><span class="sxs-lookup"><span data-stu-id="c7178-129">Generated char type</span></span> | <span data-ttu-id="c7178-130">Generierter kleiner Typ</span><span class="sxs-lookup"><span data-stu-id="c7178-130">Generated small type</span></span> |
|-------------------------|---------------------|----------------------|
| <span data-ttu-id="c7178-131">**Mittel l/char signiert**</span><span class="sxs-lookup"><span data-stu-id="c7178-131">**midl /char signed**</span></span>   | <span data-ttu-id="c7178-132">**unsigned char**</span><span class="sxs-lookup"><span data-stu-id="c7178-132">**unsigned char**</span></span>   | <span data-ttu-id="c7178-133">**small**</span><span class="sxs-lookup"><span data-stu-id="c7178-133">**small**</span></span>            |
| <span data-ttu-id="c7178-134">**Mittel l/char unsigniert**</span><span class="sxs-lookup"><span data-stu-id="c7178-134">**midl /char unsigned**</span></span> | <span data-ttu-id="c7178-135">**char**</span><span class="sxs-lookup"><span data-stu-id="c7178-135">**char**</span></span>            | <span data-ttu-id="c7178-136">**klein signiert**</span><span class="sxs-lookup"><span data-stu-id="c7178-136">**signed small**</span></span>     |
| <span data-ttu-id="c7178-137">**Mittel l/char ASCII7**</span><span class="sxs-lookup"><span data-stu-id="c7178-137">**midl /char ascii7**</span></span>   | <span data-ttu-id="c7178-138">**char**</span><span class="sxs-lookup"><span data-stu-id="c7178-138">**char**</span></span>            | <span data-ttu-id="c7178-139">**small**</span><span class="sxs-lookup"><span data-stu-id="c7178-139">**small**</span></span>            |



 

<span data-ttu-id="c7178-140">Die Option **/char** signed gibt an, dass der C-Compiler char und Small Typen signiert sind.</span><span class="sxs-lookup"><span data-stu-id="c7178-140">The **/char** signed option indicates that the C-compiler char and small types are signed.</span></span> <span data-ttu-id="c7178-141">Damit die mittlere Standardeinstellung für **char** gefunden werden kann, muss der-compilercompiler alle Verwendungszwecke von **char** konvertieren, die nicht von einer **Signierungs** Spezifikation in ein Zeichen ohne Vorzeichen begleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c7178-141">To match the MIDL default for **char**, the MIDL compiler must convert all uses of **char** not accompanied by a sign specification to **unsigned char**.</span></span> <span data-ttu-id="c7178-142">Der [**kleine**](small.md) Typ wird nicht geändert, da dieser C-Compiler-Standard für **Small** mit dem mittleren Standardwert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="c7178-142">The [**small**](small.md) type is not modified because this C-compiler default matches the MIDL default for **small**.</span></span>

<span data-ttu-id="c7178-143">Die Option **/char** Ganzzahl ohne Vorzeichen gibt an, dass der C-Compiler- [**char**](char-idl.md) -Typ nicht signiert ist.</span><span class="sxs-lookup"><span data-stu-id="c7178-143">The **/char** unsigned option indicates that the C-compiler [**char**](char-idl.md) type is unsigned.</span></span> <span data-ttu-id="c7178-144">Der-compilercompiler konvertiert alle Verwendungszwecke von [**Small**](small.md) , nicht von einer Vorzeichen Spezifikation in eine **klein** **signierte** .</span><span class="sxs-lookup"><span data-stu-id="c7178-144">The MIDL compiler converts all uses of [**small**](small.md) not accompanied by a sign specification to **signed** **small**.</span></span>

<span data-ttu-id="c7178-145">Die ASCII7-Option gibt an, dass [**char**](char-idl.md) -Typen keine explizite Signierungs Spezifikation hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="c7178-145">The ascii7 option indicates that no explicit sign specification is added to [**char**](char-idl.md) types.</span></span> <span data-ttu-id="c7178-146">Der Typ [**Small**](small.md) wird als **kleiner** generiert.</span><span class="sxs-lookup"><span data-stu-id="c7178-146">The type [**small**](small.md) is generated as **small**.</span></span>

<span data-ttu-id="c7178-147">Um Verwirrung zu vermeiden, sollten Sie nach Möglichkeit explizite Vorzeichen Spezifikationen für [**char**](char-idl.md) und Small types in der IDL-Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="c7178-147">To avoid confusion, you should use explicit sign specifications for [**char**](char-idl.md) and small types whenever possible in the IDL file.</span></span> <span data-ttu-id="c7178-148">Beachten Sie, dass die Verwendung explizit signierter **char** -Typen in ihrer IDL-Datei von DCE IDL nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="c7178-148">Note that the use of explicitly signed **char** types in your IDL file is not supported by DCE IDL.</span></span> <span data-ttu-id="c7178-149">Diese Funktion ist daher nicht verfügbar, wenn Sie mit dem [**/OSF**](-osf.md) -Schalter für mittlere Kompilierung kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c7178-149">Therefore, this feature is not available when you compile with the MIDL [**/osf**](-osf.md) switch.</span></span>

<span data-ttu-id="c7178-150">Weitere Informationen zu **/char** finden Sie unter [**Small**](small.md).</span><span class="sxs-lookup"><span data-stu-id="c7178-150">For more information related to **/char**, see [**small**](small.md).</span></span>

## <a name="examples"></a><span data-ttu-id="c7178-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7178-151">Examples</span></span>

<span data-ttu-id="c7178-152">**Mittel l/char signierte Datei Name. idl**</span><span class="sxs-lookup"><span data-stu-id="c7178-152">**midl /char signed filename.idl**</span></span>

<span data-ttu-id="c7178-153">**Mittel l/char Dateiname. idl ohne Vorzeichen**</span><span class="sxs-lookup"><span data-stu-id="c7178-153">**midl /char unsigned filename.idl**</span></span>

<span data-ttu-id="c7178-154">**Mittel l/char ASCII7 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="c7178-154">**midl /char ascii7 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="c7178-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c7178-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7178-156">**Char**</span><span class="sxs-lookup"><span data-stu-id="c7178-156">**char**</span></span>](char-idl.md)
</dt> <dt>

[<span data-ttu-id="c7178-157">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="c7178-157">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="c7178-158">**/osf**</span><span class="sxs-lookup"><span data-stu-id="c7178-158">**/osf**</span></span>](-osf.md)
</dt> <dt>

[<span data-ttu-id="c7178-159">**zuletzt**</span><span class="sxs-lookup"><span data-stu-id="c7178-159">**small**</span></span>](small.md)
</dt> </dl>

 

 




