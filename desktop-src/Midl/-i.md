---
title: /I-Schalter
description: Der Schalter/I gibt Verzeichnisse an, die nach importierten IDL-Dateien, enthaltenen Header Dateien und ACF-Dateien durchsucht werden sollen.
ms.assetid: cdb0a1c2-ff99-4060-be72-a54dd20dbf93
keywords:
- /I-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /I
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ee48ad1e66caf5ed8facbf09ebf2c517c8c895
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038084"
---
# <a name="i-switch"></a><span data-ttu-id="69b5f-104">/I-Schalter</span><span class="sxs-lookup"><span data-stu-id="69b5f-104">/I switch</span></span>

<span data-ttu-id="69b5f-105">Der Schalter **/I** gibt Verzeichnisse an, die nach importierten IDL-Dateien, enthaltenen Header Dateien und ACF-Dateien durchsucht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="69b5f-105">The **/I** switch specifies directories to be searched for imported IDL files, included header files, and ACF files.</span></span>

``` syntax
midl /I include_path
```

## <a name="switch-options"></a><span data-ttu-id="69b5f-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="69b5f-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="69b5f-107">*\_Includepfad*</span><span class="sxs-lookup"><span data-stu-id="69b5f-107">*include\_path*</span></span> 
</dt> <dd>

<span data-ttu-id="69b5f-108">Gibt mindestens ein Verzeichnis an, das Import-, include-und ACF-Dateien enthält.</span><span class="sxs-lookup"><span data-stu-id="69b5f-108">Specifies one or more directories that contain import, include, and ACF files.</span></span> <span data-ttu-id="69b5f-109">Leerraum zwischen dem **/I** -Switch und dem *include- \_ Pfad* ist optional.</span><span class="sxs-lookup"><span data-stu-id="69b5f-109">White space between the **/I** switch and *include\_path* is optional.</span></span> <span data-ttu-id="69b5f-110">Trennen Sie mehrere Verzeichnisse durch ein Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="69b5f-110">Separate multiple directories with a semicolon character (;).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69b5f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="69b5f-111">Remarks</span></span>

<span data-ttu-id="69b5f-112">Mehrere Verzeichnisse können mit jedem **/I** -Schalter angezeigt werden, und es können mehr als ein **/I** -Schalter mit jedem mittleren Compileraufruf angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="69b5f-112">More than one directory can appear with each **/I** switch, and more than one **/I** switch can appear with each MIDL compiler invocation.</span></span> <span data-ttu-id="69b5f-113">Verzeichnisse werden in der Reihenfolge durchsucht, in der Sie angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="69b5f-113">Directories are searched in the order they are specified.</span></span>

<span data-ttu-id="69b5f-114">Die **/I** -switcheinstellung wird auch vom Mittelwert-Compiler an den c-Präprozessor des c-Compilers übermittelt.</span><span class="sxs-lookup"><span data-stu-id="69b5f-114">The **/I** switch setting is also passed by the MIDL compiler to the C compiler's C preprocessor.</span></span> <span data-ttu-id="69b5f-115">Wenn der [**/cpp \_ -cmd**](-cpp-cmd.md) -Schalter vorhanden und der [**/cpp- \_ opt**](-cpp-opt.md) -Switch nicht ist, verkettet der Mittell-Compiler die durch den **/cpp \_ cmd** -Schalter angegebene Zeichenfolge mit den Optionen **/I**, [**/D**](-d.md)und [**/U**](-u.md) und verwendet diese verketteten Zeichenfolge, um den C-Präprozessor für jede IDL-und ACF-Quelldatei aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="69b5f-115">When the [**/cpp\_cmd**](-cpp-cmd.md) switch is present and the [**/cpp\_opt**](-cpp-opt.md) switch is not, the MIDL compiler concatenates the string specified by the **/cpp\_cmd** switch with the **/I**, [**/D**](-d.md), and [**/U**](-u.md) options and uses this concatenated string to invoke the C preprocessor for each IDL and ACF source file.</span></span> <span data-ttu-id="69b5f-116">Der Mittell-Compilerschalter **/I** wird nicht an den Präprozessor übergeben, wenn der Mittelwert-Compilerschalter **/No \_ cpp** oder **/cpp \_ opt** angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="69b5f-116">The MIDL compiler switch **/I** is not passed to the preprocessor when the MIDL compiler switch **/no\_cpp** or **/cpp\_opt** is specified.</span></span>

<span data-ttu-id="69b5f-117">In Microsoft-Betriebssystemumgebungen (64-Bit-Windows, 32-Bit-Windows, 16-Bit-Windows und MS-DOS) werden Verzeichnisse in der folgenden Reihenfolge durchsucht:</span><span class="sxs-lookup"><span data-stu-id="69b5f-117">In Microsoft operating-system environments (64-bit Windows, 32-bit Windows, 16-bit Windows, and MS-DOS), directories are searched in the following sequence:</span></span>

1.  <span data-ttu-id="69b5f-118">Aktuelles Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="69b5f-118">Current directory</span></span>
2.  <span data-ttu-id="69b5f-119">Durch den **/I** -Schalter angegebene Verzeichnisse (in der Reihenfolge, in der Sie dem Switch folgen)</span><span class="sxs-lookup"><span data-stu-id="69b5f-119">Directories specified by the **/I** switch (in the order they follow the switch)</span></span>
3.  <span data-ttu-id="69b5f-120">Von der include-Umgebungsvariable angegebene Verzeichnisse</span><span class="sxs-lookup"><span data-stu-id="69b5f-120">Directories specified by the INCLUDE environment variable</span></span>

<span data-ttu-id="69b5f-121">Wenn Verzeichnisse mit dem Schalter **/I** angegeben werden, weist der [**/No \_ DEF \_ Idir**](-no-def-idir.md) -Schalter den Mittelwert Compiler an, das aktuelle Verzeichnis zu ignorieren, die von der INCLUDE-Umgebungsvariablen angegebenen Verzeichnisse zu ignorieren und nur die angegebenen Verzeichnisse zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="69b5f-121">When directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to ignore the current directory, ignore the directories specified by the INCLUDE environment variable, and search only the specified directories.</span></span>

<span data-ttu-id="69b5f-122">Wenn keine Verzeichnisse mit dem **/I** -Schalter angegeben werden, weist der [**/No \_ DEF \_ Idir**](-no-def-idir.md) -Schalter den Mittelwert Compiler an, nur das aktuelle Verzeichnis zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="69b5f-122">When no directories are specified with the **/I** switch, the [**/no\_def\_idir**](-no-def-idir.md) switch instructs the MIDL compiler to search only the current directory.</span></span>

## <a name="examples"></a><span data-ttu-id="69b5f-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="69b5f-123">Examples</span></span>

<span data-ttu-id="69b5f-124">**Mittel l/I c: \\ include; c: \\ include \\ h/I \\ include2 filename. idl**</span><span class="sxs-lookup"><span data-stu-id="69b5f-124">**midl /I c:\\include;c:\\include\\h /I\\include2 filename.idl**</span></span>

## <a name="see-also"></a><span data-ttu-id="69b5f-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69b5f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69b5f-126">Allgemeine Syntax der Mittell-Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="69b5f-126">General MIDL Command-line Syntax</span></span>](general-midl-command-line-syntax.md)
</dt> <dt>

[<span data-ttu-id="69b5f-127">**/acf**</span><span class="sxs-lookup"><span data-stu-id="69b5f-127">**/acf**</span></span>](-acf.md)
</dt> <dt>

[<span data-ttu-id="69b5f-128">**/cpp- \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="69b5f-128">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="69b5f-129">**/cpp \_ Opt**</span><span class="sxs-lookup"><span data-stu-id="69b5f-129">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="69b5f-130">**/No \_ DEF \_ Idir**</span><span class="sxs-lookup"><span data-stu-id="69b5f-130">**/no\_def\_idir**</span></span>](-no-def-idir.md)
</dt> </dl>

 

 




