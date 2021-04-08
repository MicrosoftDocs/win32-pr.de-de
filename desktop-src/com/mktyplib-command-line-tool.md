---
title: MkTypLib-Command-Line Tool
description: MkTypLib ist eine Befehlszeilen Anwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu entwickeln. Sie kann auch verwendet werden, um eine C-oder C++-Header Datei zu generieren.
ms.assetid: 883d380d-1d73-439b-9f11-ee89fc62fdfd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc392351327124777c2d52d0bbe0653853dcb52
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730640"
---
# <a name="mktyplib-command-line-tool"></a><span data-ttu-id="1e89d-104">MkTypLib-Command-Line Tool</span><span class="sxs-lookup"><span data-stu-id="1e89d-104">MkTypLib Command-Line Tool</span></span>

<span data-ttu-id="1e89d-105">\[Das Mktyplib.exe Tool ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="1e89d-105">\[The Mktyplib.exe tool is obsolete.</span></span> <span data-ttu-id="1e89d-106">Verwenden Sie stattdessen den Mittel l-Compiler.</span><span class="sxs-lookup"><span data-stu-id="1e89d-106">Use the MIDL compiler instead.</span></span> <span data-ttu-id="1e89d-107">Wenn Sie Abwärtskompatibilität mit alten Automatisierungs Programmen benötigen, verwenden Sie den mittlerer l-Compiler mit der **/mktyplib203** -Option.\]</span><span class="sxs-lookup"><span data-stu-id="1e89d-107">If you need backward compatibility with old Automation programs, use the MIDL compiler with the **/mktyplib203** option.\]</span></span>

<span data-ttu-id="1e89d-108">MkTypLib ist eine Befehlszeilen Anwendung, die eine IDL-Datei verarbeitet, um eine Typbibliothek zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="1e89d-108">MkTypLib is a command-line application that processes an IDL file to produce a type library.</span></span> <span data-ttu-id="1e89d-109">Sie kann auch verwendet werden, um eine C-oder C++-Header Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1e89d-109">It can also be used to generate a C or C++ header file.</span></span>

<span data-ttu-id="1e89d-110">So generieren Sie eine Typbibliothek aus einer ODL-Datei:</span><span class="sxs-lookup"><span data-stu-id="1e89d-110">To generate a type library from a ODL file:</span></span>

-   <span data-ttu-id="1e89d-111">Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="1e89d-111">From the command prompt, run the following command:</span></span>

    <span data-ttu-id="1e89d-112">\**mktyplibs \* \* \* Dateiname*</span><span class="sxs-lookup"><span data-stu-id="1e89d-112">\**mktyplibÂ \*\*\*filename*</span></span>

    <span data-ttu-id="1e89d-113">wobei *filename* der Name der ODL-Datei ist.</span><span class="sxs-lookup"><span data-stu-id="1e89d-113">where *filename* is the name of the ODL file.</span></span>

<span data-ttu-id="1e89d-114">MkTypLib unterstützt auch mehrere optionale Parameter.</span><span class="sxs-lookup"><span data-stu-id="1e89d-114">MkTypLib also supports several optional parameters.</span></span> <span data-ttu-id="1e89d-115">Um eine komplette Liste zu erhalten, führen Sie die folgende Befehlszeile aus:</span><span class="sxs-lookup"><span data-stu-id="1e89d-115">For a complete list, run the following command line:</span></span>

<span data-ttu-id="1e89d-116">**MkTypLib/?**</span><span class="sxs-lookup"><span data-stu-id="1e89d-116">**mktyplib /?**</span></span>

<span data-ttu-id="1e89d-117">Da MkTypLib eine veraltete Anwendung ist, kann Sie keine IDL-Dateien oder-Dateien mit Schnittstellen analysieren, die außerhalb einer [**Library**](/windows/desktop/Midl/library) -Anweisung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1e89d-117">Because MkTypLib is an obsolete application, it cannot parse IDL files or files with interfaces defined outside of a [**library**](/windows/desktop/Midl/library) statement.</span></span> <span data-ttu-id="1e89d-118">Weitere Informationen finden Sie [unter Unterschiede zwischen mittlerer l und MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span><span class="sxs-lookup"><span data-stu-id="1e89d-118">For more information, see [Differences Between MIDL and MkTypLib](/windows/desktop/Midl/differences-between-midl-and-mktyplib).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e89d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e89d-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e89d-120">Übersetzen in C++</span><span class="sxs-lookup"><span data-stu-id="1e89d-120">Translating to C++</span></span>](translating-to-c--.md)
</dt> </dl>

 

 