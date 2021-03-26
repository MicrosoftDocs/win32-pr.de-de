---
title: Präprozessordirektiven (HLSL)
description: Präprozessordirektiven, wie z. b. \ define und \ ifdef, werden normalerweise verwendet, um das ändern und Kompilieren von Quell Programmen in verschiedenen Ausführungs Umgebungen zu vereinfachen.
ms.assetid: b5164c0e-62ab-4da5-9c22-efb5e6319bd6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f2d9e51926d2a1b7bf374653becec4fe3de3daa
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739232"
---
# <a name="preprocessor-directives-hlsl"></a><span data-ttu-id="c0345-103">Präprozessordirektiven (HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0345-103">Preprocessor Directives (HLSL)</span></span>

<span data-ttu-id="c0345-104">Präprozessordirektiven, wie z. b. [ \# define](dx-graphics-hlsl-appendix-pre-define.md) und [ \# ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), werden normalerweise verwendet, um das ändern und Kompilieren von Quell Programmen in verschiedenen Ausführungs Umgebungen zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="c0345-104">Preprocessor directives, such as [\#define](dx-graphics-hlsl-appendix-pre-define.md) and [\#ifdef](dx-graphics-hlsl-appendix-pre-ifdef.md), are typically used to make source programs easy to change and easy to compile in different execution environments.</span></span> <span data-ttu-id="c0345-105">Anweisungen in der Quelldatei weisen den Präprozessor an, bestimmte Aktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c0345-105">Directives in the source file tell the preprocessor to perform specific actions.</span></span> <span data-ttu-id="c0345-106">Beispielsweise kann der Präprozessor Token im Text ersetzen, den Inhalt von anderen Dateien in die Quelldatei einfügen oder die Kompilierung eines Teils der Datei unterdrücken, indem er Textabschnitte entfernt.</span><span class="sxs-lookup"><span data-stu-id="c0345-106">For example, the preprocessor can replace tokens in the text, insert the contents of other files into the source file, or suppress compilation of part of the file by removing sections of text.</span></span> <span data-ttu-id="c0345-107">Präprozessorzeilen werden vor der Makroerweiterung erkannt und ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0345-107">Preprocessor lines are recognized and carried out before macro expansion.</span></span> <span data-ttu-id="c0345-108">Wenn also die Erweiterung eines Makros aussieht wie ein Präprozessorbefehl, wird dieser Befehl nicht vom Präprozessor erkannt.</span><span class="sxs-lookup"><span data-stu-id="c0345-108">Therefore, if a macro expands into something that looks like a preprocessor command, that command is not recognized by the preprocessor.</span></span>

<span data-ttu-id="c0345-109">Präprozessoranweisungen verwenden den gleichen Zeichensatz wie Quelldateianweisungen, mit der Ausnahme, dass Escapesequenzen nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="c0345-109">Preprocessor statements use the same character set as source file statements, with the exception that escape sequences are not supported.</span></span> <span data-ttu-id="c0345-110">Der Zeichensatz, der in Präprozessoranweisungen verwendet wird, ist mit dem Ausführungszeichensatz identisch.</span><span class="sxs-lookup"><span data-stu-id="c0345-110">The character set used in preprocessor statements is the same as the execution character set.</span></span> <span data-ttu-id="c0345-111">Der Präprozessor erkennt auch negative Zeichenwerte.</span><span class="sxs-lookup"><span data-stu-id="c0345-111">The preprocessor also recognizes negative character values.</span></span>

<span data-ttu-id="c0345-112">Der HLSL-Präprozessor erkennt die folgenden Direktiven:</span><span class="sxs-lookup"><span data-stu-id="c0345-112">The HLSL preprocessor recognizes the following directives:</span></span>

-   [<span data-ttu-id="c0345-113">\#define</span><span class="sxs-lookup"><span data-stu-id="c0345-113">\#define</span></span>](dx-graphics-hlsl-appendix-pre-define.md)
-   [<span data-ttu-id="c0345-114">\#elif</span><span class="sxs-lookup"><span data-stu-id="c0345-114">\#elif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="c0345-115">\#else</span><span class="sxs-lookup"><span data-stu-id="c0345-115">\#else</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="c0345-116">\#endif</span><span class="sxs-lookup"><span data-stu-id="c0345-116">\#endif</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="c0345-117">\#Zeit</span><span class="sxs-lookup"><span data-stu-id="c0345-117">\#error</span></span>](dx-graphics-hlsl-appendix-pre-error.md)
-   [<span data-ttu-id="c0345-118">\#if</span><span class="sxs-lookup"><span data-stu-id="c0345-118">\#if</span></span>](dx-graphics-hlsl-appendix-pre-if.md)
-   [<span data-ttu-id="c0345-119">\#ifdef</span><span class="sxs-lookup"><span data-stu-id="c0345-119">\#ifdef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="c0345-120">\#ifndef</span><span class="sxs-lookup"><span data-stu-id="c0345-120">\#ifndef</span></span>](dx-graphics-hlsl-appendix-pre-ifdef.md)
-   [<span data-ttu-id="c0345-121">\#darunter</span><span class="sxs-lookup"><span data-stu-id="c0345-121">\#include</span></span>](dx-graphics-hlsl-appendix-pre-include.md)
-   [<span data-ttu-id="c0345-122">\#Stimmen</span><span class="sxs-lookup"><span data-stu-id="c0345-122">\#line</span></span>](dx-graphics-hlsl-appendix-pre-line.md)
-   [<span data-ttu-id="c0345-123">\#pragma</span><span class="sxs-lookup"><span data-stu-id="c0345-123">\#pragma</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
-   [<span data-ttu-id="c0345-124">\#undef</span><span class="sxs-lookup"><span data-stu-id="c0345-124">\#undef</span></span>](dx-graphics-hlsl-appendix-pre-undef.md)

<span data-ttu-id="c0345-125">Das Nummern Zeichen ( \# ) muss das erste nicht-Leerzeichen in der Zeile sein, die die Direktive enthält. Leerzeichen können zwischen dem Nummern Zeichen und dem ersten Buchstaben der Direktive angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c0345-125">The number sign (\#) must be the first nonwhite-space character on the line containing the directive; white-space characters can appear between the number sign and the first letter of the directive.</span></span> <span data-ttu-id="c0345-126">Manche Anweisungen enthalten Argumente oder Werte.</span><span class="sxs-lookup"><span data-stu-id="c0345-126">Some directives include arguments or values.</span></span> <span data-ttu-id="c0345-127">Jedem Text, der auf eine Direktive folgt (außer einem Argument oder einem Wert, der Teil der Direktive ist), muss das einzeilige Kommentar Trennzeichen (//) vorangestellt sein, oder es muss in Kommentar Trennzeichen (/ \* \* /) eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="c0345-127">Any text that follows a directive (except an argument or value that is part of the directive) must be preceded by the single-line comment delimiter (//) or enclosed in comment delimiters (/\* \*/).</span></span> <span data-ttu-id="c0345-128">Zeilen, die Präprozessordirektiven enthalten, können fortgesetzt werden, indem unmittelbar vor dem Zeilenende Marker mit einem umgekehrten Schrägstrich ( \) .</span><span class="sxs-lookup"><span data-stu-id="c0345-128">Lines containing preprocessor directives can be continued by immediately preceding the end-of-line marker with a backslash (\).</span></span>

<span data-ttu-id="c0345-129">Präprozessoranweisungen können an beliebiger Stelle in einer Quelldatei auftreten, aber sie gelten nur für den Rest der Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="c0345-129">Preprocessor directives can appear anywhere in a source file, but they apply only to the remainder of the source file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0345-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0345-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0345-131">Anhang (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c0345-131">Appendix (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix.md)
</dt> </dl>

 

 




