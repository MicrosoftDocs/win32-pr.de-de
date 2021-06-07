---
title: Präprozessordirektiven (HLSL)
description: Präprozessordirektiven wie \define und \ifdef werden in der Regel verwendet, um Quellprogramme einfach zu ändern und in verschiedenen Ausführungsumgebungen einfach zu kompilieren.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8efdd996ddeb58c09d1c8250f174c21bb939f082
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386829"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="dafb4-103">Präprozessordirektiven (HLSL)</span><span class="sxs-lookup"><span data-stu-id="dafb4-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="dafb4-104">Präprozessordirektiven wie [ \# define](dx-graphics-hlsl-appendix-pre-define.md) und [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md)werden in der Regel verwendet, um Quellprogramme einfach zu ändern und in verschiedenen Ausführungsumgebungen einfach zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="dafb4-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="dafb4-105">Anweisungen in der Quelldatei weisen den Präprozessor an, bestimmte Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="dafb4-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="dafb4-106">Beispielsweise kann der Präprozessor Token im Text ersetzen, den Inhalt von anderen Dateien in die Quelldatei einfügen oder die Kompilierung eines Teils der Datei unterdrücken, indem er Textabschnitte entfernt.</span><span class="sxs-lookup"><span data-stu-id="dafb4-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="dafb4-107">Präprozessorzeilen werden vor der Makroerweiterung erkannt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dafb4-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="dafb4-108">Wenn also die Erweiterung eines Makros aussieht wie ein Präprozessorbefehl, wird dieser Befehl nicht vom Präprozessor erkannt.</span><span class="sxs-lookup"><span data-stu-id="dafb4-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="dafb4-109">Präprozessoranweisungen verwenden den gleichen Zeichensatz wie Quelldateianweisungen, mit der Ausnahme, dass Escapesequenzen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dafb4-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="dafb4-110">Der Zeichensatz, der in Präprozessoranweisungen verwendet wird, ist mit dem Ausführungszeichensatz identisch.</span><span class="sxs-lookup"><span data-stu-id="dafb4-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="dafb4-111">Der Präprozessor erkennt auch negative Zeichenwerte.</span><span class="sxs-lookup"><span data-stu-id="dafb4-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="dafb4-112">Der HLSL-Präprozessor erkennt die folgenden Anweisungen:</span><span class="sxs-lookup"><span data-stu-id="dafb4-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="dafb4-113">\#Definieren</span><span class="sxs-lookup"><span data-stu-id="dafb4-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="dafb4-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="dafb4-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="dafb4-115">\#else</span><span class="sxs-lookup"><span data-stu-id="dafb4-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="dafb4-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="dafb4-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="dafb4-117">\#Fehler</span><span class="sxs-lookup"><span data-stu-id="dafb4-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="dafb4-118">\#Wenn</span><span class="sxs-lookup"><span data-stu-id="dafb4-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="dafb4-119">\#Ifdef</span><span class="sxs-lookup"><span data-stu-id="dafb4-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="dafb4-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="dafb4-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="dafb4-121">\#include</span><span class="sxs-lookup"><span data-stu-id="dafb4-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="dafb4-122">\#line</span><span class="sxs-lookup"><span data-stu-id="dafb4-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="dafb4-123">\#Pragma</span><span class="sxs-lookup"><span data-stu-id="dafb4-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="dafb4-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="dafb4-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="dafb4-125">Das Nummernzeichen ( ) muss das erste Nicht-Leerzeichen in der Zeile sein, die die -Direktive enthält. Leerzeichen können zwischen dem Nummernzeichen und dem ersten Buchstaben der -Direktive \# angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="dafb4-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="dafb4-126">Manche Anweisungen enthalten Argumente oder Werte.</span><span class="sxs-lookup"><span data-stu-id="dafb4-126">Some directives include arguments or values.</span></span> <span data-ttu-id="dafb4-127">Jedem Text, der auf eine -Anweisung folgt (mit Ausnahme eines Arguments oder Werts, das Teil der -Direktive ist), muss das einzeilenbasierte Kommentartrennzeichen (/) voranstehen oder in Kommentartrennzeichen (/ /) eingeschlossen \* \* werden.</span><span class="sxs-lookup"><span data-stu-id="dafb4-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="dafb4-128">Zeilen, die Präprozessordirektiven enthalten, können fortgesetzt werden, indem dem Zeilenendemarker unmittelbar ein zurücker schräger Schrägstrich ( ) vorangegangen \\ wird.</span><span class="sxs-lookup"><span data-stu-id="dafb4-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\\).</span></span>

<span data-ttu-id="dafb4-129">Präprozessoranweisungen können an beliebiger Stelle in einer Quelldatei auftreten, aber sie gelten nur für den Rest der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="dafb4-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dafb4-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dafb4-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dafb4-131">Anhang (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dafb4-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




