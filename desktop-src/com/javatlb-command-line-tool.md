---
title: JAVATLB-Command-Line Tool
description: JAVATLB-Command-Line Tool
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714429"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="06ecb-103">JAVATLB-Command-Line Tool</span><span class="sxs-lookup"><span data-stu-id="06ecb-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="06ecb-104">JAVATLB ist eine Komponente von Visual J++ 5,0.</span><span class="sxs-lookup"><span data-stu-id="06ecb-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="06ecb-105">JAVATLB ist eine Befehlszeilen Anwendung, die Klassendateien für ein COM-Objekt generiert.</span><span class="sxs-lookup"><span data-stu-id="06ecb-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="06ecb-106">Methoden, die Datentypen enthalten, die nicht präzise und sicher in Java dargestellt werden können, werden nicht konvertiert.</span><span class="sxs-lookup"><span data-stu-id="06ecb-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="06ecb-107">Im Gegensatz zum Assistenten für die [Java-Typbibliothek](java-type-library-wizard.md)generiert JAVATLB keine Zusammenfassungs Datei mit den Informationen der Java-Typbibliothek.</span><span class="sxs-lookup"><span data-stu-id="06ecb-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="06ecb-108">Zum Generieren von Java-Klassendateien für ein einzelnes COM-Objekt führen Sie in der Eingabeaufforderung Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="06ecb-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="06ecb-109">**JAVATLB** - *Dateiname*</span><span class="sxs-lookup"><span data-stu-id="06ecb-109">**javatlb** *filename*</span></span>

<span data-ttu-id="06ecb-110">wobei *filename* der Name der Datei ist, die die Typbibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="06ecb-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="06ecb-111">Diese Datei kann eine der folgenden Dateinamen Erweiterungen aufweisen: ". tlb", ". olb", ". ocx", ". dll" oder ". exe".</span><span class="sxs-lookup"><span data-stu-id="06ecb-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="06ecb-112">Um Java-Klassendateien für mehrere COM-Objekte zu generieren, führen Sie über die Eingabeaufforderung Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="06ecb-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="06ecb-113">\**JAVATLB @ \* \* \* Textdatei*</span><span class="sxs-lookup"><span data-stu-id="06ecb-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="06ecb-114">Dabei ist *Textfile* der Name einer Textdatei, die eine Liste der Dateien enthält, die die Typbibliotheken des COM-Objekts enthalten.</span><span class="sxs-lookup"><span data-stu-id="06ecb-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="06ecb-115">In Visual J++ 6,0 wird das Befehlszeilen Tool JAVATLB durch das [Tool JActiveX](jactivex-command-line-tool.md)ersetzt.</span><span class="sxs-lookup"><span data-stu-id="06ecb-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="06ecb-116">Weitere Informationen finden Sie in der Dokumentation zu Visual J++ 6,0.</span><span class="sxs-lookup"><span data-stu-id="06ecb-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="06ecb-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06ecb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06ecb-118">Übersetzen in Java</span><span class="sxs-lookup"><span data-stu-id="06ecb-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




