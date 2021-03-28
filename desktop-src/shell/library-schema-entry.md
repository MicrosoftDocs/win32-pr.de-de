---
description: Bibliotheks Beschreibungsdateien sind XML-Dateien, die Bibliotheken definieren.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Bibliotheks Beschreibungs Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5bebbd7ed168cd977530ccfeb0b319c33142687
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "104981064"
---
# <a name="library-description-schema"></a><span data-ttu-id="613b1-103">Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="613b1-103">Library Description Schema</span></span>

<span data-ttu-id="613b1-104">Bibliotheks Beschreibungsdateien sind XML-Dateien, die Bibliotheken definieren.</span><span class="sxs-lookup"><span data-stu-id="613b1-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="613b1-105">Bibliotheken aggregieren Elemente aus lokalen und Remote Speicherorten in einer einzelnen Ansicht in Windows-Explorer.</span><span class="sxs-lookup"><span data-stu-id="613b1-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="613b1-106">Bibliotheks Beschreibungsdateien folgen dem Bibliotheks Beschreibungs Schema und werden als \* . Library-MS-Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="613b1-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="613b1-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="613b1-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="613b1-108">Übersicht über das Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="613b1-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="613b1-109">Namespace Versionierung</span><span class="sxs-lookup"><span data-stu-id="613b1-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="613b1-110">Beispiel für eine Bibliotheks Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="613b1-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="613b1-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="613b1-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="613b1-112">Übersicht über das Bibliotheks Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="613b1-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="613b1-113">Bibliotheken enthalten Dateien, die an einem oder mehreren Speicherorten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="613b1-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="613b1-114">Diese Dateien werden von Bibliotheken nicht gespeichert. Stattdessen überwachen Sie die Ordner, die die Dateien enthalten, und ermöglichen Benutzern den Zugriff auf und die Anordnung von Dateien auf verschiedene Weise.</span><span class="sxs-lookup"><span data-stu-id="613b1-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="613b1-115">Beispielsweise kann sich ein Benutzer Musikdateien in mehreren Ordnern auf einer lokalen Festplatte und auch auf einer externen Festplatte befinden.</span><span class="sxs-lookup"><span data-stu-id="613b1-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="613b1-116">Mithilfe der **Musikbibliothek** kann der Benutzer gleichzeitig auf alle diese Dateien zugreifen und diese nach dem Namen des Künstlers oder dem Albumtitel als einzelne Gruppe sortieren.</span><span class="sxs-lookup"><span data-stu-id="613b1-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="613b1-117">Das Bibliotheks Beschreibungs Schema besteht aus drei Hauptkomponenten, die in der folgenden Tabelle beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="613b1-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613b1-118">Allgemeine Bibliotheksinformationen</span><span class="sxs-lookup"><span data-stu-id="613b1-118">General library information</span></span> | <span data-ttu-id="613b1-119">Informationen zur Bibliothek, z. b. Name, Besitzer, Version, Symbol, die Windows Explorer verwenden kann, wenn Sie die Bibliothek für einen Benutzer anzeigt.</span><span class="sxs-lookup"><span data-stu-id="613b1-119">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="613b1-120">Bibliotheks Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="613b1-120">Library properties</span></span>          | <span data-ttu-id="613b1-121">Eine oder mehrere Eigenschaften, die die Bibliothek beschreiben.</span><span class="sxs-lookup"><span data-stu-id="613b1-121">One or more properties that describe the library.</span></span> <span data-ttu-id="613b1-122">Diese benutzerdefinierten Eigenschaften sind spezifisch für die Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="613b1-122">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="613b1-123">Bibliotheks Speicherorte</span><span class="sxs-lookup"><span data-stu-id="613b1-123">Library locations</span></span>           | <span data-ttu-id="613b1-124">Mindestens ein suchverbinder, der die in der Bibliothek einzuschließenden Speicherorte identifiziert.</span><span class="sxs-lookup"><span data-stu-id="613b1-124">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="613b1-125">Jeder dieser Standorte kann auch über einen eindeutigen Satz von Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="613b1-125">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="613b1-126">Bibliotheksdateien in Windows 7 werden im bekannten Ordner, folderid-Bibliotheken, gespeichert \_ .</span><span class="sxs-lookup"><span data-stu-id="613b1-126">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="613b1-127">Standardmäßig befindet sich der Ordner folderid \_ Libraries unter% User Profile% \\ AppData \\ Roaming \\ Microsoft Windows \\ - \\ Bibliotheken.</span><span class="sxs-lookup"><span data-stu-id="613b1-127">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="613b1-128">Namespace Versionierung</span><span class="sxs-lookup"><span data-stu-id="613b1-128">Namespace Versioning</span></span>

<span data-ttu-id="613b1-129">Versionen des Bibliotheks Beschreibungsdatei Formats ( \* . Library-MS) werden nachverfolgt, indem der-Namespace geändert wird.</span><span class="sxs-lookup"><span data-stu-id="613b1-129">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="613b1-130">Für Windows 7 weist das Dateiformat den folgenden Standard Namespace auf: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="613b1-130">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="613b1-131">Versionen der Bibliotheksinhalte werden jedoch mithilfe des- [<version>](schema-library-version.md) Elements in einer bestimmten Bibliotheks Beschreibungsdatei nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="613b1-131">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="613b1-132">Beispiel für eine Bibliotheks Beschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="613b1-132">Example of a Library Description File</span></span>

<span data-ttu-id="613b1-133">Im folgenden finden Sie ein Beispiel für eine Bibliotheks Beschreibungsdatei, die eine Bibliothek für Dokument Dateien definiert.</span><span class="sxs-lookup"><span data-stu-id="613b1-133">The following is an example of a Library Description file that defines a library for document files.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
    <name>@shell32.dll,-34575</name>
    <ownerSID>S-1-5-21-379071477-2495173225-776587366-1000</ownerSID>
    <version>1</version>
    <isLibraryPinned>true</isLibraryPinned>
    <iconReference>imageres.dll,-1002</iconReference>
    <templateInfo>
        <folderType>{7d49d726-3c21-4f05-99aa-fdc2c9474656}</folderType>
    </templateInfo>
    <searchConnectorDescriptionList>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34577</description>
            <isDefaultSaveLocation>true</isDefaultSaveLocation>
            <simpleLocation>
                <url>knownfolder:{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</url>
                <serialized>MBAAAEAFCAAA...MFNVAAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
        <searchConnectorDescription publisher="Microsoft" product="Windows">
            <description>@shell32.dll,-34579</description>
            <isDefaultNonOwnerSaveLocation>true</isDefaultNonOwnerSaveLocation>
            <simpleLocation>
                <url>knownfolder:{ED4824AF-DCE4-45A8-81E2-FC7965083634}</url>
                <serialized>MBAAAEAFCAAA...HJIfK9AAAAAA</serialized>
            </simpleLocation>
        </searchConnectorDescription>
    </searchConnectorDescriptionList>
</libraryDescription>
```



## <a name="related-topics"></a><span data-ttu-id="613b1-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="613b1-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="613b1-135">foldertype-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-135">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="613b1-136">iconReference-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-136">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="613b1-137">islibrarypinned-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-137">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="613b1-138">librarydescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-138">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="613b1-139">Name-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-139">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="613b1-140">Besitzer-SID-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-140">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="613b1-141">Property-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-141">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="613b1-142">PropertyStore-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-142">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="613b1-143">searchconnectordescription-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-143">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="613b1-144">searchconnectordescriptionlist-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-144">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="613b1-145">templateingefo-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-145">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="613b1-146">Version-Element (Bibliotheks Schema)</span><span class="sxs-lookup"><span data-stu-id="613b1-146">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="613b1-147">Suchdienst-Beschreibungs Schema</span><span class="sxs-lookup"><span data-stu-id="613b1-147">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
