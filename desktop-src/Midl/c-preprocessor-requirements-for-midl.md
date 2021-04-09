---
title: C-präprozessoranforderungen für die Mittel l
description: Diese Seite gilt nur für Entwickler, die bestimmte Gründe dafür haben, den Microsoft C/C++-Präprozessor als Präprozessor zu ersetzen, der von der Mittell verwendet wird, oder für Entwickler, die angepasste präprozessorswitches angeben müssen.
ms.assetid: 1dd5eef4-5ea4-4958-8f53-9a95c0ccbf3e
keywords:
- Mittlere compilermittell, C-präprozessoranforderungen
- C-präprozessormittell, Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b49c4e0c086a52eda2705d72cf2a2ff22c759290
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947943"
---
# <a name="c-preprocessor-requirements-for-midl"></a><span data-ttu-id="9192b-105">C-präprozessoranforderungen für die Mittel l</span><span class="sxs-lookup"><span data-stu-id="9192b-105">C-Preprocessor Requirements for MIDL</span></span>

<span data-ttu-id="9192b-106">Diese Seite gilt nur für Entwickler, die bestimmte Gründe dafür haben, den Microsoft C/C++-Präprozessor als Präprozessor zu ersetzen, der von der Mittell verwendet wird, oder für Entwickler, die angepasste präprozessorswitches angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="9192b-106">This page applies only to developers who have specific reasons to replace the Microsoft C/C++ preprocessor as the preprocessor used by MIDL, or to developers who must specify customized preprocessor switches.</span></span> <span data-ttu-id="9192b-107">Die mittleren Schalter [**/cpp \_ cmd**](-cpp-cmd.md), [**/cpp \_ opt**](-cpp-opt.md)und [**/No \_ cpp**](-no-cpp-nocpp.md) werden verwendet, um das Standardverhalten des Compilers zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="9192b-107">The MIDL switches [**/cpp\_cmd**](-cpp-cmd.md), [**/cpp\_opt**](-cpp-opt.md), and [**/no\_cpp**](-no-cpp-nocpp.md) are used to override the default behavior of the compiler.</span></span> <span data-ttu-id="9192b-108">Es gibt in der Regel keinen Grund, den Microsoft C/C++-Präprozessor zu ersetzen und keine angepassten präprozessorschalter anzugeben.</span><span class="sxs-lookup"><span data-stu-id="9192b-108">There is typically no reason to replace the Microsoft C/C++ preprocessor, nor to specify customized preprocessor switches.</span></span>

<span data-ttu-id="9192b-109">Der mittlerer l-Compiler verwendet bei der anfänglichen Verarbeitung der IDL-Datei einen C-Präprozessor.</span><span class="sxs-lookup"><span data-stu-id="9192b-109">The MIDL compiler uses a C preprocessor during initial processing of the IDL file.</span></span> <span data-ttu-id="9192b-110">Die Buildumgebung, die beim Kompilieren der IDL-Dateien verwendet wird, ist einem Standard-C/C++-Präprozessor zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="9192b-110">The build environment used when compiling the IDL files is associated with a default C/C++ preprocessor.</span></span> <span data-ttu-id="9192b-111">Wenn ein anderer Präprozessor verwendet werden soll, aktiviert der Mittell-Compilerschalter [**/cpp \_ cmd**](-cpp-cmd.md) eine außer Kraft setzung des standardmäßigen C/C++-präprozessornamens:</span><span class="sxs-lookup"><span data-stu-id="9192b-111">If a different preprocessor is to be used, the MIDL compiler switch [**/cpp\_cmd**](-cpp-cmd.md) enables an override of the default C/C++-preprocessor name:</span></span>

``` syntax
midl /cpp_cmd preprocessor_name filename
```

<dl> <dt>

<span data-ttu-id="9192b-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*\_präprozessorname*</span><span class="sxs-lookup"><span data-stu-id="9192b-112"><span id="preprocessor_name"></span><span id="PREPROCESSOR_NAME"></span>*preprocessor\_name*</span></span>
</dt> <dd>

<span data-ttu-id="9192b-113">Gibt den Namen des präprozessornamens an, der von der Mittell verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9192b-113">Specifies the name of the preprocessor to be used by MIDL.</span></span> <span data-ttu-id="9192b-114">Kann mit einem Pfad zur Binärdatei angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9192b-114">May be specified with a path to the binary.</span></span> <span data-ttu-id="9192b-115">Die Erweiterung ". exe" ist optional.</span><span class="sxs-lookup"><span data-stu-id="9192b-115">The .exe extension is optional.</span></span>

</dd> <dt>

<span data-ttu-id="9192b-116"><span id="filename"></span><span id="FILENAME"></span>*Einfügen*</span><span class="sxs-lookup"><span data-stu-id="9192b-116"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="9192b-117">Gibt den Namen der IDL-Datei an.</span><span class="sxs-lookup"><span data-stu-id="9192b-117">Specifies the name of the IDL file.</span></span>

</dd> </dl>

-   <span data-ttu-id="9192b-118">Der mittlerer l-Compiler erwartet, dass der Präprozessor die folgenden Konventionen beachtet:</span><span class="sxs-lookup"><span data-stu-id="9192b-118">The MIDL compiler expects any preprocessor to observe the following conventions:</span></span>
-   <span data-ttu-id="9192b-119">Die Eingabedatei wird als letztes Argument in der Befehlszeile angegeben.</span><span class="sxs-lookup"><span data-stu-id="9192b-119">The input file is specified as the last argument on the command line.</span></span>
-   <span data-ttu-id="9192b-120">Der Präprozessor muss die Ausgabe an das Standardausgabe Gerät (stdout) umleiten.</span><span class="sxs-lookup"><span data-stu-id="9192b-120">The preprocessor must redirect output to the standard output device, stdout.</span></span>
-   <span data-ttu-id="9192b-121">Im Ausgabestream des Präprozessors sind die **\# Zeilen** Anweisungen vorhanden, um bessere Diagnosemeldungen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9192b-121">In the output stream of the preprocessor, the **\#line** directives are present to enable better diagnostic messages.</span></span>
-   <span data-ttu-id="9192b-122">Die Zeilen Direktiven sind die einzigen Präprozessordirektiven im Ausgabestream.</span><span class="sxs-lookup"><span data-stu-id="9192b-122">The line directives are the only preprocessor directives in the output stream.</span></span>

<span data-ttu-id="9192b-123">In der Mitte wird davon ausgegangen, dass der erzeugte Präprozessor alle Präprozessordirektiven aus dem Eingabestream des Compilers entfernt hat, mit Ausnahme des Auftretens der Zeilen Direktive, die zum Ermitteln des Quell Speicher Orts in compilernachrichten erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9192b-123">MIDL assumes that the spawned preprocessor has removed all preprocessor directives from the input stream of the compiler, with the exception of the occurrences of the line directive necessary for pinpointing source location in compiler messages.</span></span> <span data-ttu-id="9192b-124">Wenn ein vom Microsoft C/C++-Präprozessor abweichender Präprozessor oder Präprozessoroptionen mit dem [**/cpp \_ opt**](-cpp-opt.md) -Schalter angegeben werden, ist die Angabe einer entsprechenden Präprozessoroption erforderlich, die die Zeilen Direktiven in den Eingabestream des Compilers einfügt.</span><span class="sxs-lookup"><span data-stu-id="9192b-124">When indicating a preprocessor different from the Microsoft C/C++ preprocessor, or when specifying preprocessor options with the [**/cpp\_opt**](-cpp-opt.md) switch, specifying an appropriate preprocessor option that puts the line directives in the input stream of the compiler is required.</span></span> <span data-ttu-id="9192b-125">Für den Microsoft C/C++-Präprozessor müsste z. b. die **/E** -Option verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="9192b-125">For example, for the Microsoft C/C++ preprocessor the **/E** option would have to be used:</span></span>

``` syntax
midl /cpp_cmd cl.exe /cpp_opt "/E" file.idl
```

<span data-ttu-id="9192b-126">Die **\# Line** -Direktive wird von der mittleren l in einer der folgenden Formen akzeptiert:</span><span class="sxs-lookup"><span data-stu-id="9192b-126">The **\#line** directive is accepted by MIDL in one of the following forms:</span></span>

``` syntax
#line digit-sequence "filename" new-line
 
# digit-sequence "filename" new-line
```

<span data-ttu-id="9192b-127">Eine umfassende Beschreibung der line-Direktive und anderer Präprozessordirektiven finden Sie in der Dokumentation für den verwendeten C-Compiler.</span><span class="sxs-lookup"><span data-stu-id="9192b-127">For a complete description of the line directive and other preprocessor directives, see the documentation for the C-compiler being used.</span></span>

<span data-ttu-id="9192b-128">In der-Klasse wird nur die Zeilen Präprozessordirektive akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="9192b-128">MIDL accepts only the line preprocessor directive.</span></span> <span data-ttu-id="9192b-129">Wenn der/No- [**\_ cpp**](-no-cpp-nocpp.md) -Schalter verwendet wird, darf die Eingabedatei nicht über andere Präprozessordirektiven verfügen, oder die Eingabedatei muss vor dem Aufrufen von "Mittel l" verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="9192b-129">Therefore, if the [**/no\_cpp**](-no-cpp-nocpp.md) switch is used, the input file must not have other preprocessor directives, or the input file must have been processed prior to invoking MIDL.</span></span>

<span data-ttu-id="9192b-130">Weitere Informationen finden Sie unter [Umgang mit \# Definitionen in IDL-Dateien](dealing-with-defines-in-idl-files-2.md).</span><span class="sxs-lookup"><span data-stu-id="9192b-130">For more information, see [Dealing with \#defines in IDL Files](dealing-with-defines-in-idl-files-2.md).</span></span>

 

 




