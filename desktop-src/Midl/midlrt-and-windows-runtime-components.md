---
title: Mittlere und Windows-Runtime Komponenten
description: Zeigt, wie Metadatendateien (. winmd) erstellt werden, die die API für benutzerdefinierte Windows-Runtime Komponenten darstellen.
ms.assetid: 7830A5DB-9696-4A93-948B-51DA46A5143C
keywords:
- Mittel l-compilermittell
- Mittel l-compilermittell, Mittel l und Windows-Runtime WinRT
- Windows-Runtime-Mittell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edf4d40b3fc5b0a5ed8eeb9b5fd47a3b87c4543
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104517216"
---
# <a name="midlrt-and-windows-runtime-components"></a><span data-ttu-id="cd3d6-106">Mittlere und Windows-Runtime Komponenten</span><span class="sxs-lookup"><span data-stu-id="cd3d6-106">MIDLRT and Windows Runtime components</span></span>

<span data-ttu-id="cd3d6-107">Zeigt, wie Metadatendateien (. winmd) erstellt werden, die die API für benutzerdefinierte Windows-Runtime Komponenten darstellen.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-107">Shows how to create metadata (.winmd) files that represent the API for custom Windows Runtime components.</span></span>


<span data-ttu-id="cd3d6-108">Verwenden Sie den-compilercompiler, um Metadatendateien (. winmd) für die benutzerdefinierten Windows-Runtime Komponenten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-108">Use the MIDLRT compiler to build metadata (.winmd) files for your custom Windows Runtime components.</span></span>

<span data-ttu-id="cd3d6-109">Wenn Ihre Metadatendateien generiert werden, können Sie Sie mithilfe des Hilfsprogramms "mdmerge" in ein effizienteres Paket zerlegen.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-109">When your metadata files are generated, you can compose them into a more efficient package by using the MDMERGE utility.</span></span> <span data-ttu-id="cd3d6-110">Weitere Informationen finden Sie unter [mdmerge-und Metadatendateien](mdmerge-and-metadata-files.md).</span><span class="sxs-lookup"><span data-stu-id="cd3d6-110">For more info, see [MDMERGE and metadata files](mdmerge-and-metadata-files.md).</span></span>


<span data-ttu-id="cd3d6-111">Die Verwendung von "Mittell" ähnelt der Verwendung des compl-Compilers.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-111">Using MIDLRT is similar to using the MIDL compiler.</span></span> <span data-ttu-id="cd3d6-112">Führen Sie in der Befehlszeile den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="cd3d6-112">Run MIDLRT from the command line using the following command:</span></span>

<span data-ttu-id="cd3d6-113">**mittlere**  *<* **Optionen** _>_ **Dateiname. idl**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-113">**midlrt** \*<\***options**_>_ **filename.idl**</span></span>

<span data-ttu-id="cd3d6-114">Where \* < *-\*\*Optionen*\* _>_ stellt die Befehlszeilenoptionen dar, die Sie verwenden möchten, und filename. idl ist der Name der zu kompilierenden IDL-Datei.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-114">where \*<\***options**_>_ represents the command-line options you want to use, and Filename.idl is the name of the IDL file to compile.</span></span>


<span data-ttu-id="cd3d6-115">In der folgenden Liste sind die Befehls Zeilenschalter aufgeführt, die von MIDLRT.EXE verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-115">The following list shows the command-line switches that MIDLRT.EXE uses.</span></span>

<dl>

[<span data-ttu-id="cd3d6-116">**/Enum- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-116">**/enum\_class**</span></span>](-enum-class.md)  
[<span data-ttu-id="cd3d6-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-117">**/metadata\_dir**</span></span>](-metadata-dir.md)  
[<span data-ttu-id="cd3d6-118">**/nomidl**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-118">**/nomidl**</span></span>](-nomidl.md)  
[<span data-ttu-id="cd3d6-119">**/nomd**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-119">**/nomd**</span></span>](-nomd.md)  
[<span data-ttu-id="cd3d6-120">**/NS- \_ Präfix**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-120">**/ns\_prefix**</span></span>](-ns-prefix.md)  
[<span data-ttu-id="cd3d6-121">**/winmd**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-121">**/winmd**</span></span>](-winmd.md)  
[<span data-ttu-id="cd3d6-122">**/WinRT**</span><span class="sxs-lookup"><span data-stu-id="cd3d6-122">**/winrt**</span></span>](-winrt.md)  
</dl>

<span data-ttu-id="cd3d6-123">Eine umfassende Liste mit den Compilerschaltern und-Optionen für den Mittelwert ist verfügbar, wenn Sie den-Compilerschalter [**/Help**](-help-.md) und/? verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-123">A complete listing of MIDLRT compiler switches and options is available when you use the MIDLRT compiler [**/help**](-help-.md) and /?</span></span> <span data-ttu-id="cd3d6-124">Mikro.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-124">switches.</span></span> <span data-ttu-id="cd3d6-125">Die Schalter sind nach Kategorien organisiert.</span><span class="sxs-lookup"><span data-stu-id="cd3d6-125">The switches are organized by categories.</span></span> <span data-ttu-id="cd3d6-126">Weitere Informationen finden Sie in der [Referenz zur Mittel l-Command-Line](midl-command-line-reference.md).</span><span class="sxs-lookup"><span data-stu-id="cd3d6-126">For more info, see the [MIDL Command-Line Reference](midl-command-line-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd3d6-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd3d6-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd3d6-128">Mdmerge-und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="cd3d6-128">MDMERGE and metadata files</span></span>](mdmerge-and-metadata-files.md)
</dt> </dl>

 

 




