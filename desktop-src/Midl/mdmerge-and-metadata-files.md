---
title: Mdmerge-und Metadatendateien
description: Verfasst mehrere Metadatendateien (. winmd) in einer Reihe von Ausgabe Metadatendateien, basierend auf dem Namespace.
ms.assetid: A3203627-82DF-4744-BBBC-53D13F30210E
keywords:
- metadata
- winmd-Datei
- Windows-Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2d91f8c7506dd80fd2477beb61c5b99a26b05b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947449"
---
# <a name="mdmerge-and-metadata-files"></a><span data-ttu-id="db37a-106">Mdmerge-und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="db37a-106">MDMERGE and metadata files</span></span>

<span data-ttu-id="db37a-107">Verfasst mehrere Metadatendateien (. winmd) in einer Reihe von Ausgabe Metadatendateien, basierend auf dem Namespace.</span><span class="sxs-lookup"><span data-stu-id="db37a-107">Composes multiple metadata (.winmd) files into a number of output metadata files, based on namespace.</span></span>

## <a name="usage"></a><span data-ttu-id="db37a-108">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="db37a-108">Usage</span></span>

<span data-ttu-id="db37a-109">Führen Sie mdmerge über die Befehlszeile mit dem folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="db37a-109">Run MDMERGE from the command line using the following command:</span></span>

<span data-ttu-id="db37a-110">**mdmerge** - *< ***Optionen***>*</span><span class="sxs-lookup"><span data-stu-id="db37a-110">**mdmerge** *<***options***>*</span></span>

<span data-ttu-id="db37a-111">Where- *< ***Optionen*** >* stellt die Befehlszeilenoptionen dar, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db37a-111">where *<***options***>* represents the command-line options you want to use.</span></span>

<span data-ttu-id="db37a-112">Generieren Sie Metadatendateien für die benutzerdefinierten Windows-Runtime Komponenten mithilfe des complrt-Compilers.</span><span class="sxs-lookup"><span data-stu-id="db37a-112">Generate metadata files for your custom Windows Runtime components by using the MIDLRT compiler.</span></span> <span data-ttu-id="db37a-113">Weitere Informationen finden Sie unter " [Mittel LRT-und Windows-Runtime Komponenten](midlrt-and-windows-runtime-components.md).</span><span class="sxs-lookup"><span data-stu-id="db37a-113">For more info, see [MIDLRT and Windows Runtime components](midlrt-and-windows-runtime-components.md).</span></span>

## <a name="command-line-switches"></a><span data-ttu-id="db37a-114">Befehlszeilenschalter</span><span class="sxs-lookup"><span data-stu-id="db37a-114">Command-line switches</span></span>

<span data-ttu-id="db37a-115">Die folgende Liste zeigt die Befehls Zeilenschalter, die von mdmerge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db37a-115">The following list shows the command-line switches that MDMERGE uses.</span></span>

<dl>

[<span data-ttu-id="db37a-116">**/i**</span><span class="sxs-lookup"><span data-stu-id="db37a-116">**/i**</span></span>](-mdmerge-i.md)  
[<span data-ttu-id="db37a-117">**/Metadata \_ dir**</span><span class="sxs-lookup"><span data-stu-id="db37a-117">**/metadata\_dir**</span></span>](-mdmerge-metadata-dir.md)  
[<span data-ttu-id="db37a-118">**/n**</span><span class="sxs-lookup"><span data-stu-id="db37a-118">**/n**</span></span>](-mdmerge-n.md)  
[<span data-ttu-id="db37a-119">**/o**</span><span class="sxs-lookup"><span data-stu-id="db37a-119">**/o**</span></span>](-mdmerge-o.md)  
[<span data-ttu-id="db37a-120">**/partial**</span><span class="sxs-lookup"><span data-stu-id="db37a-120">**/partial**</span></span>](-mdmerge-partial.md)  
[<span data-ttu-id="db37a-121">**/v**</span><span class="sxs-lookup"><span data-stu-id="db37a-121">**/v**</span></span>](-mdmerge-v.md)  
</dl>

<span data-ttu-id="db37a-122">Eine komplette Liste der mdmerge-Compilerschalter und-Optionen ist verfügbar, wenn Sie das **-h** und **/?**</span><span class="sxs-lookup"><span data-stu-id="db37a-122">A complete listing of MDMERGE compiler switches and options is available when you use the **-h** and **/?**</span></span> <span data-ttu-id="db37a-123">Mikro.</span><span class="sxs-lookup"><span data-stu-id="db37a-123">switches.</span></span>

## <a name="remarks"></a><span data-ttu-id="db37a-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db37a-124">Remarks</span></span>

<span data-ttu-id="db37a-125">Die metadatenkomposition ermöglicht, dass mehrere IDL-Dateien Definitionen für Windows-Runtime Komponenten im gleichen Namespace enthalten.</span><span class="sxs-lookup"><span data-stu-id="db37a-125">Metadata composition enables multiple IDL files to contain definitions for Windows Runtime components in the same namespace.</span></span> <span data-ttu-id="db37a-126">Dadurch werden alle Typen in einem Namespace innerhalb einer einzelnen IDL-Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="db37a-126">This frees you from defining all of the types in a namespace within a single IDL file.</span></span>

<span data-ttu-id="db37a-127">Wahrscheinlich verfügen Sie über zahlreiche Windows-Runtime Komponenten, die von ihren apps verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db37a-127">You're likely to have numerous Windows Runtime components that your apps use.</span></span> <span data-ttu-id="db37a-128">Wenn Sie den letzten Schritt ausführen, um bereitstell Bare Windows-Runtime Metadatenassemblys zu erstellen, können Sie mdmerge so konfigurieren, dass Komponenten aus mehreren metadatenverzeichnissen zusammengeführt werden, z. b. mit dem System (% Windows% \\ system32 \\ winmetadata), den Foundation-Typen und dem Buildverzeichnis Ihres aktuellen Projekts.</span><span class="sxs-lookup"><span data-stu-id="db37a-128">When you perform the final step to produce deployable Windows Runtime metadata assemblies, you can configure MDMERGE to merge components from multiple metadata directories, like those that are installed with the system (%WINDOWS%\\system32\\WinMetadata), your foundation types, and your current project’s build directory.</span></span> <span data-ttu-id="db37a-129">Alle erforderlichen Typen werden mit den richtigen, bereitstell baren Metadatenassemblys zusammengeführt, die Sie für den Windows Store verpacken können.</span><span class="sxs-lookup"><span data-stu-id="db37a-129">All necessary types are merged into the correct, deployable, metadata assemblies that you can package for the Windows Store.</span></span>

<span data-ttu-id="db37a-130">Mit der [**/n**](-mdmerge-n.md) -Option können Sie die unterstützte Namespace Tiefe für das Verfassen von Metadatenassemblys angeben.</span><span class="sxs-lookup"><span data-stu-id="db37a-130">You can use the [**/n**](-mdmerge-n.md) option to specify the supported namespace depth for composing metadata assemblies.</span></span> <span data-ttu-id="db37a-131">Dadurch wird die Konfiguration einer aktiven Teilung für Ihre Windows-Runtime Komponenten ermöglicht, sodass anstelle von vielen nur eine einzelne winmd-Datei gepackt wird.</span><span class="sxs-lookup"><span data-stu-id="db37a-131">This enables configuring a hot split for your Windows Runtime components, so that only a single .winmd file is packaged instead of many.</span></span> <span data-ttu-id="db37a-132">Dies reduziert die Ladezeiten und Datei-e/a, die von Ihren Windows Store-Apps benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="db37a-132">This reduces the load times and file I/O required by your Windows Store apps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db37a-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="db37a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db37a-134">Mittlere und Windows-Runtime Komponenten</span><span class="sxs-lookup"><span data-stu-id="db37a-134">MIDLRT and Windows Runtime components</span></span>](midlrt-and-windows-runtime-components.md)
</dt> </dl>

 

 




