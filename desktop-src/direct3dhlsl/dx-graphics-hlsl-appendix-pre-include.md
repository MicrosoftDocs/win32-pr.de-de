---
title: " include-Direktive"
description: Eine Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quell Programm einfügt, wenn die Anweisung angezeigt wird.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include-Direktive HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a844459234200ca99233eb3f64a2a1c30449cdcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993438"
---
# <a name="include-directive"></a><span data-ttu-id="df668-104">\#include-Direktive</span><span class="sxs-lookup"><span data-stu-id="df668-104">\#include Directive</span></span>

<span data-ttu-id="df668-105">Eine Präprozessordirektive, die den Inhalt der angegebenen Datei in das Quell Programm einfügt, wenn die Anweisung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="df668-105">Preprocessor directive that inserts the contents of the specified file into the source program at the point where the directive appears.</span></span>


| <span data-ttu-id="df668-106">\#"*Dateiname*" einschließen</span><span class="sxs-lookup"><span data-stu-id="df668-106">\#include "*filename*"</span></span>       |
|------------------------------|
| <span data-ttu-id="df668-107">\#<*Dateiname* einschließen></span><span class="sxs-lookup"><span data-stu-id="df668-107">\#include <*filename*></span></span> |

## <a name="parameters"></a><span data-ttu-id="df668-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="df668-108">Parameters</span></span>

| <span data-ttu-id="df668-109">Element</span><span class="sxs-lookup"><span data-stu-id="df668-109">Item</span></span> | <span data-ttu-id="df668-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df668-110">Description</span></span> |
|------|-------------|
| <span data-ttu-id="df668-111">*filename*</span><span class="sxs-lookup"><span data-stu-id="df668-111">*filename*</span></span> | <span data-ttu-id="df668-112">Der Dateiname der einzuschließenden Datei, dem optional eine Verzeichnis Spezifikation vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="df668-112">Filename of the file to include, optionally preceded by a directory specification.</span></span> <span data-ttu-id="df668-113">Der Dateiname muss eine vorhandene Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="df668-113">The filename must specify an existing file.</span></span> |

## <a name="remarks"></a><span data-ttu-id="df668-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df668-114">Remarks</span></span>

<span data-ttu-id="df668-115">Die \# include-Direktive bewirkt, dass die-Direktive durch den gesamten Inhalt der angegebenen Datei ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="df668-115">The \#include directive causes replacement of the directive by the entire contents of the specified file.</span></span> <span data-ttu-id="df668-116">Der Präprozessor beendet die Suche, sobald eine Datei mit dem angegebenen Namen gefunden wird. Wenn Sie eine eindeutige Pfadspezifikation für die Datei angeben, durchsucht der Präprozessor nur den angegebenen Pfad.</span><span class="sxs-lookup"><span data-stu-id="df668-116">The preprocessor stops searching as soon as it finds a file with the specified name; if you specify a complete, unambiguous path specification for the file, the preprocessor searches only the specified path.</span></span>

> [!NOTE]
> <span data-ttu-id="df668-117">Das [Effect-Compiler-Tool](/windows/desktop/direct3dtools/fxc) verfügt über einen integrierten include-Handler, der den/I-Schalter verwendet.</span><span class="sxs-lookup"><span data-stu-id="df668-117">The [Effect-Compiler Tool](/windows/desktop/direct3dtools/fxc) has a built-in include handler using the /I switch.</span></span> <span data-ttu-id="df668-118">Wenn Sie jedoch den Compiler über die API ausführen, können Sie einen benutzerdefinierten include-Handler bereitstellen, indem Sie die ID3DXInclude-Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="df668-118">However, when executing the compiler from the API, you can provide a customized include handler by implementing the ID3DXInclude interface.</span></span>

<span data-ttu-id="df668-119">Der Unterschied zwischen den beiden Syntax Formularen ist die Reihenfolge, in der der Präprozessor nach Header Dateien sucht, wenn der Pfad nicht vollständig angegeben ist, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="df668-119">The difference between the two syntax forms is the order in which the preprocessor searches for header files when the path is incompletely specified, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df668-120">Syntaxformat</span><span class="sxs-lookup"><span data-stu-id="df668-120">Syntax form</span></span></th>
<th><span data-ttu-id="df668-121">Präprozessorsuchmuster</span><span class="sxs-lookup"><span data-stu-id="df668-121">Preprocessor search pattern</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="df668-122">#<b>&quot;</b> <em>Dateiname</em> einschließen<b>&quot;</b></span><span class="sxs-lookup"><span data-stu-id="df668-122">#include <b>&quot;</b><em>filename</em><b>&quot;</b></span></span></td>
<td><span data-ttu-id="df668-123">Sucht nach der Includedatei:</span><span class="sxs-lookup"><span data-stu-id="df668-123">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="df668-124">im gleichen Verzeichnis wie die Datei, die die #include-Direktive enthält.</span><span class="sxs-lookup"><span data-stu-id="df668-124">in the same directory as the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="df668-125">in den Verzeichnissen von Dateien, die eine #include-Direktive für die Datei enthalten, die die #include-Direktive enthält.</span><span class="sxs-lookup"><span data-stu-id="df668-125">in the directories of any files that contain a #include directive for the file that contains the #include directive.</span></span></li>
<li><span data-ttu-id="df668-126">in der von der/I-Compileroption angegebenen Pfade in der Reihenfolge, in der Sie aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="df668-126">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="df668-127">in den Pfaden, die durch die include-Umgebungsvariable angegeben werden, in der Reihenfolge, in der Sie aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="df668-127">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="df668-128">Die include-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="df668-128">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="df668-129">Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation der Entwicklungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="df668-129">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="df668-130">#<b><</b> <em>Dateiname</em> einschließen<b>></b></span><span class="sxs-lookup"><span data-stu-id="df668-130">#include <b><</b><em>filename</em><b>></b></span></span></td>
<td><span data-ttu-id="df668-131">Sucht nach der Includedatei:</span><span class="sxs-lookup"><span data-stu-id="df668-131">Searches for the include file:</span></span>
<ol>
<li><span data-ttu-id="df668-132">in der von der/I-Compileroption angegebenen Pfade in der Reihenfolge, in der Sie aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="df668-132">in paths specified by the /I compiler option, in the order in which they are listed.</span></span></li>
<li><p><span data-ttu-id="df668-133">in den Pfaden, die durch die include-Umgebungsvariable angegeben werden, in der Reihenfolge, in der Sie aufgelistet sind.</span><span class="sxs-lookup"><span data-stu-id="df668-133">in paths specified by the INCLUDE environment variable, in the order in which they are listed.</span></span></p>
<blockquote>
[!NOTE]<br />
<span data-ttu-id="df668-134">Die include-Umgebungsvariable wird in einer Entwicklungsumgebung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="df668-134">The INCLUDE environment variable is ignored in an development environment.</span></span> <span data-ttu-id="df668-135">Informationen zum Festlegen der Includepfade für Ihr Projekt finden Sie in der Dokumentation der Entwicklungsumgebung.</span><span class="sxs-lookup"><span data-stu-id="df668-135">Refer to your development environment's documentation for information about how to set the include paths for your project.</span></span>
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a><span data-ttu-id="df668-136">Beispiele</span><span class="sxs-lookup"><span data-stu-id="df668-136">Examples</span></span>

<span data-ttu-id="df668-137">Das folgende Beispiel bewirkt, dass der Präprozessor die \# include-Direktive durch den Inhalt von "stdio. h" ersetzt.</span><span class="sxs-lookup"><span data-stu-id="df668-137">The following example causes the preprocessor to replace the \#include directive with the contents of stdio.h.</span></span> <span data-ttu-id="df668-138">Da im Beispiel das eckige Klammern-Format verwendet wird, sucht der Präprozessor nur in den Verzeichnissen, die von der/I-Compileroption und der INCLUDE-Umgebungsvariablen aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="df668-138">Because the example uses the angle bracket format, the preprocessor will search for the file only in the directories listed by the /I compiler option and the INCLUDE environment variable.</span></span>

```cpp
#include <stdio.h>
```

## <a name="see-also"></a><span data-ttu-id="df668-139">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="df668-139">See also</span></span>

- [<span data-ttu-id="df668-140">Präprozessordirektiven (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="df668-140">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)

- <span data-ttu-id="df668-141">[ID3D10Include-Schnittstelle](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="df668-141">[ID3D10Include Interface](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>

- [<span data-ttu-id="df668-142">Effekt-Compilertool</span><span class="sxs-lookup"><span data-stu-id="df668-142">Effect-Compiler Tool</span></span>](/windows/desktop/direct3dtools/fxc)