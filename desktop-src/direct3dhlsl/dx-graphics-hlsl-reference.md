---
title: Verweis für HLSL
description: In der HLSL-Referenz Dokumentation werden die Sprachmerkmale angegeben. Es ist in mehrere Abschnitte unterteilt.
ms.assetid: 1d0e12ff-8559-4e5c-9914-6ed313ea5464
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ce0bb59dd26bd8bb9723bcdff23bbc79ee810253
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037349"
---
# <a name="reference-for-hlsl"></a><span data-ttu-id="7db6d-104">Verweis für HLSL</span><span class="sxs-lookup"><span data-stu-id="7db6d-104">Reference for HLSL</span></span>

<span data-ttu-id="7db6d-105">In der HLSL-Referenz Dokumentation werden die Sprachmerkmale angegeben.</span><span class="sxs-lookup"><span data-stu-id="7db6d-105">The HLSL reference documentation specifies the language characteristics.</span></span> <span data-ttu-id="7db6d-106">Es ist in mehrere Abschnitte unterteilt.</span><span class="sxs-lookup"><span data-stu-id="7db6d-106">It is broken into several sections.</span></span>

-   <span data-ttu-id="7db6d-107">[Sprachsyntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) : das Programmieren von Shadern in HLSL erfordert, dass Sie die Sprachsyntax verstehen, d. h. wie Sie HLSL-Code schreiben.</span><span class="sxs-lookup"><span data-stu-id="7db6d-107">[Language Syntax (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md) - Programming shaders in HLSL requires that you understand the language syntax, that is, how you write HLSL code.</span></span> <span data-ttu-id="7db6d-108">Dies umfasst Code zum Deklarieren und Initialisieren von Variablen, Schreiben benutzerdefinierter Shaderfunktionen und Hinzufügen von flowsteuerungsanweisungen, damit ihre Funktionen leistungsfähiger werden.</span><span class="sxs-lookup"><span data-stu-id="7db6d-108">This includes code to declare and initialize variables, write user-defined shader functions, and add flow control statements to make your functions more powerful.</span></span>
-   <span data-ttu-id="7db6d-109">[Shader-Modelle vs shaderprofile](dx-graphics-hlsl-models.md) : der HLSL-Compiler implementiert Regeln und Einschränkungen basierend auf shadermodellen.</span><span class="sxs-lookup"><span data-stu-id="7db6d-109">[Shader Models vs Shader Profiles](dx-graphics-hlsl-models.md) - The HLSL compiler implements rules and restrictions based on shader models.</span></span> <span data-ttu-id="7db6d-110">Der Code in jedem Vertex-Shader, Geometry-Shader (bei Verwendung von Direct3D 10) und PixelShader werden anhand eines shadermodells überprüft, das Sie zum Zeitpunkt der Kompilierung angeben.</span><span class="sxs-lookup"><span data-stu-id="7db6d-110">The code in each vertex shader, geometry shader (if you are using Direct3D 10) and pixel shader are validated against a shader model, which you supply at compile time.</span></span>
-   <span data-ttu-id="7db6d-111">[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) : HLSL verfügt über viele intrinsische Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7db6d-111">[**Intrinsic Functions (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md) - HLSL has many intrinsic functions.</span></span> <span data-ttu-id="7db6d-112">Diese werden implementiert und getestet, damit Sie Sie verwenden können, um Sie zu überprüfen, dass Sie bereits gedeentschlallte und gut funktionieren.</span><span class="sxs-lookup"><span data-stu-id="7db6d-112">These are implemented and tested so that you can use them knowing that they are already debugged and they perform well.</span></span> <span data-ttu-id="7db6d-113">Wenn Sie eigene Funktionen schreiben möchten, lesen Sie den Abschnitt Sprachsyntax zum Schreiben von benutzerdefinierten Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7db6d-113">If you choose to write your own functions, see the language syntax section for writing user-defined functions.</span></span>
-   <span data-ttu-id="7db6d-114">[ASM-Shader](dx9-graphics-reference-asm.md) -verweisassemblyanweisungen, mit denen Sie Shader programmieren und Debuggen können.</span><span class="sxs-lookup"><span data-stu-id="7db6d-114">[Asm Shader Reference](dx9-graphics-reference-asm.md) - Assembly instructions that you can use to program and debug shaders.</span></span>
-   <span data-ttu-id="7db6d-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) : kompiliert eine Rohdaten-HLSL-Quelle.</span><span class="sxs-lookup"><span data-stu-id="7db6d-115">[D3DCompiler Reference](dx-graphics-d3dcompiler-reference.md) - Compiles raw HLSL source.</span></span>
-   <span data-ttu-id="7db6d-116">[Referenz zur Inline-Formatkonvertierung](inline-format-conversion-reference.md) : die D3DX \_ dxgiformatconvert. INL-Datei enthält Funktionen für Inline Formatkonvertierungen, die Sie im COMPUTE-Shader oder Pixel-Shader auf Direct3D 11-Hardware verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7db6d-116">[Inline Format Conversion Reference](inline-format-conversion-reference.md) - The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="7db6d-117">Sie können diese Funktionen in der Anwendung verwenden, um gleichzeitig Lese-und Schreibvorgänge für eine Textur auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7db6d-117">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="7db6d-118">Das heißt, Sie können eine direkte Bildbearbeitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="7db6d-118">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="7db6d-119">Um diese Funktionen für die Inline Formatkonvertierung zu verwenden, schließen \_ Sie die Datei D3DX dxgiformatconvert. INL in Ihre Anwendung ein.</span><span class="sxs-lookup"><span data-stu-id="7db6d-119">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>
-   <span data-ttu-id="7db6d-120">[Anhang (DirectX HLSL)](dx-graphics-hlsl-appendix.md) : der Anhang ist aus Gründen der Vollständigkeit enthalten.</span><span class="sxs-lookup"><span data-stu-id="7db6d-120">[Appendix (DirectX HLSL)](dx-graphics-hlsl-appendix.md) - The appendix is included for completeness.</span></span> <span data-ttu-id="7db6d-121">Sie enthält eine Liste der Schlüsselwörter und reservierten Wörter. Diese Wörter können nicht als Bezeichner in ihren Programmen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7db6d-121">It includes a listing of the keywords and reserved words; these words cannot be used as identifiers in your programs.</span></span> <span data-ttu-id="7db6d-122">Außerdem enthält Sie eine Auflistung der Sprachgrammatik für den Verweis.</span><span class="sxs-lookup"><span data-stu-id="7db6d-122">It also includes a listing of the language grammar for reference.</span></span>
-   <span data-ttu-id="7db6d-123">[**HLSL-Fehler und-Warnungen**](hlsl-errors-and-warnings.md) : gibt Fehler-und Warn Codes an, die ein Shader zurückgeben kann.</span><span class="sxs-lookup"><span data-stu-id="7db6d-123">[**HLSL errors and warnings**](hlsl-errors-and-warnings.md) - Provides error and warning codes that a shader can return.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7db6d-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7db6d-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7db6d-125">HLSL</span><span class="sxs-lookup"><span data-stu-id="7db6d-125">HLSL</span></span>](dx-graphics-hlsl.md)
</dt> <dt>

[<span data-ttu-id="7db6d-126">Programmieranleitung für HLSL</span><span class="sxs-lookup"><span data-stu-id="7db6d-126">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




