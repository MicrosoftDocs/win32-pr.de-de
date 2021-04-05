---
title: Metadata Editor-Objekt
description: Metadata Editor-Objekt
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- Windows Media-Format-SDK, Metadaten-Editor-Objekte
- Advanced Systems Format (ASF), Metadaten-Editor-Objekte
- ASF (Advanced Systems Format), Metadaten-Editor-Objekte
- Objekte, Metadaten-Editor-Objekte
- Metadaten-Editor-Objekte, Informationen zu
- Metadaten, Editor-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724099"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="f3166-109">Metadata Editor-Objekt</span><span class="sxs-lookup"><span data-stu-id="f3166-109">Metadata Editor Object</span></span>

<span data-ttu-id="f3166-110">Das Metadateneditor-Objekt wird verwendet, um die im Header Abschnitt von ASF-Dateien gespeicherten Informationen zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="f3166-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="f3166-111">Die gebräuchlichsten Elemente, die von diesem Objekt bearbeitet werden, sind Metadatenattribute.</span><span class="sxs-lookup"><span data-stu-id="f3166-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="f3166-112">Darüber hinaus behandelt der Metadaten-Editor [*Marker*](wmformat-glossary.md) und Skript Befehle.</span><span class="sxs-lookup"><span data-stu-id="f3166-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="f3166-113">Sie müssen den Metadateneditor nur dann verwenden, wenn Sie den Header einer vorhandenen Datei bearbeiten möchten, ohne Sie zu spielen.</span><span class="sxs-lookup"><span data-stu-id="f3166-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="f3166-114">Das Metadateneditor-Objekt wird von der [**wmkreateeditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor)-Funktion erstellt, mit der ein Zeiger auf eine **IWMMetadataEditor** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="f3166-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="f3166-115">Die anderen Schnittstellen des Metadateneditor-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f3166-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="f3166-116">Die folgenden Schnittstellen werden vom Metadateneditor-Objekt unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3166-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="f3166-117">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f3166-117">Interface</span></span>                                        | <span data-ttu-id="f3166-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3166-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f3166-119">**Iwmdrmeditor**</span><span class="sxs-lookup"><span data-stu-id="f3166-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="f3166-120">Ermöglicht das Bearbeiten von Anwendungen, um die [*DRM*](wmformat-glossary.md) -Eigenschaften einer ASF-Datei zu untersuchen, ohne über Rechte zum Wiedergeben geschützter Inhalte zu verfügen.</span><span class="sxs-lookup"><span data-stu-id="f3166-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="f3166-121">**Iwmheaderinfo**</span><span class="sxs-lookup"><span data-stu-id="f3166-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="f3166-122">Bearbeitet Attribute, Marker und Skript Befehle in der Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="f3166-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="f3166-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="f3166-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="f3166-124">Ruft die Codec-Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="f3166-124">Retrieves codec information.</span></span> <span data-ttu-id="f3166-125">Erbt alle Methoden von **iwmheaderinfo**.</span><span class="sxs-lookup"><span data-stu-id="f3166-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="f3166-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="f3166-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="f3166-127">Bietet erweiterte Unterstützung für Attribute, einschließlich großer Attribute, mehrerer Sprachen und doppelter Attributnamen.</span><span class="sxs-lookup"><span data-stu-id="f3166-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="f3166-128">Erbt alle Methoden von **iwmheaderinfo** und **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="f3166-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="f3166-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="f3166-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="f3166-130">Öffnet, schließt und speichert Änderungen am Header einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f3166-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="f3166-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="f3166-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="f3166-132">Öffnet eine ASF-Datei für die Header Bearbeitung mit mehreren Optionen für Dateizugriff und Freigabe.</span><span class="sxs-lookup"><span data-stu-id="f3166-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="f3166-133">Erbt alle Methoden von **IWMMetadataEditor**.</span><span class="sxs-lookup"><span data-stu-id="f3166-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="f3166-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f3166-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3166-135">**Marker**</span><span class="sxs-lookup"><span data-stu-id="f3166-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="f3166-136">**Metadaten**</span><span class="sxs-lookup"><span data-stu-id="f3166-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="f3166-137">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="f3166-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="f3166-138">**Skriptbefehle**</span><span class="sxs-lookup"><span data-stu-id="f3166-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="f3166-139">**Arbeiten mit Metadaten**</span><span class="sxs-lookup"><span data-stu-id="f3166-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




