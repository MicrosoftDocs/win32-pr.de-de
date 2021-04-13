---
title: Metadaten
description: Metadaten sind für dieses SDK Informationen, die eine ASF-Datei oder den Inhalt der Datei beschreiben.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- Windows Media-Format-SDK, Übersicht über Metadaten
- Advanced Systems Format (ASF), Übersicht über Metadaten
- ASF (Advanced Systems Format), Übersicht über Metadaten
- Metadaten, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311250"
---
# <a name="metadata"></a><span data-ttu-id="ee419-107">Metadaten</span><span class="sxs-lookup"><span data-stu-id="ee419-107">Metadata</span></span>

<span data-ttu-id="ee419-108">Metadaten sind für dieses SDK Informationen, die eine ASF-Datei oder den Inhalt der Datei beschreiben.</span><span class="sxs-lookup"><span data-stu-id="ee419-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="ee419-109">Der Header Abschnitt einer ASF-Datei enthält alle Metadaten, die mit dieser Datei verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="ee419-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="ee419-110">Einzelne Elemente von Metadaten in einer ASF-Datei werden als Attribute bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ee419-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="ee419-111">Jedes Attribut verfügt über einen Namen und einen Wert.</span><span class="sxs-lookup"><span data-stu-id="ee419-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="ee419-112">In dieser Dokumentation werden globale Konstanten verwendet, um Attribute zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ee419-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="ee419-113">Beispielsweise wird der Titel einer ASF-Datei im **g \_ wszwmtitle** -Attribut gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ee419-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="ee419-114">Eine Reihe von Attributen werden im Windows Media-Format-SDK definiert, um die gängigsten Metadatenanforderungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ee419-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="ee419-115">Außerdem können Sie eigene Attribute erstellen.</span><span class="sxs-lookup"><span data-stu-id="ee419-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="ee419-116">Wenn Sie benutzerdefinierte Attribute benennen, sollten Sie jedoch darauf achten, dass andere Anwendungsentwickler dieselben Namen verwenden können und Konflikte auftreten können.</span><span class="sxs-lookup"><span data-stu-id="ee419-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="ee419-117">Einige Attribute werden vom SDK festgelegt und können nicht manuell geändert werden.</span><span class="sxs-lookup"><span data-stu-id="ee419-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="ee419-118">Wenn Sie z. b. eine ASF-Datei indizieren, legt das SDK das **g \_ wszwmseekable** -Attribut fest, um anzuzeigen, dass die Datei jetzt von einem beliebigen angegebenen Punkt gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="ee419-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="ee419-119">Andere Attribute sind reine Informations Informationen und müssen manuell festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ee419-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="ee419-120">Wenn Sie z. b. den Autor einer Datei nachverfolgen möchten, sollten Sie **g \_ wszwmauthor** festlegen.</span><span class="sxs-lookup"><span data-stu-id="ee419-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="ee419-121">Das Windows Media-Format-SDK bietet Unterstützung für Attribute, die auf die gesamte Datei angewendet werden, sowie Attribute, die auf einzelne Streams angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee419-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="ee419-122">Sie können das SDK für den Windows Media-Format verwenden, um die Metadaten in MP3-Dateien zu bearbeiten. Sie sollten jedoch immer die in MP3-Dateien kompatiblen Attribute verwenden, um die Kompatibilität mit anderen MP3-Bearbeitungsprogrammen aufrechtzuerhalten.</span><span class="sxs-lookup"><span data-stu-id="ee419-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee419-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee419-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee419-124">**Konzepte**</span><span class="sxs-lookup"><span data-stu-id="ee419-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="ee419-125">**Metadata Editor-Objekt**</span><span class="sxs-lookup"><span data-stu-id="ee419-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="ee419-126">**Metadatenfeatures**</span><span class="sxs-lookup"><span data-stu-id="ee419-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="ee419-127">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="ee419-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




