---
description: Bibliotheksbeschreibungsdateien sind XML-Dateien, die Bibliotheken definieren.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Schema der Bibliotheksbeschreibung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a6da99820e81c55e5d705c72d4d0509ea271a4a
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581738"
---
# <a name="library-description-schema"></a><span data-ttu-id="c4fc7-103">Schema der Bibliotheksbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c4fc7-103">Library Description Schema</span></span>

<span data-ttu-id="c4fc7-104">Bibliotheksbeschreibungsdateien sind XML-Dateien, die Bibliotheken definieren.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-104">Library description files are XML files that define libraries.</span></span> <span data-ttu-id="c4fc7-105">Bibliotheken aggregieren Elemente von lokalen und Remotespeicherorten in einer einzelnen Ansicht im Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-105">Libraries aggregate items from local and remote storage locations into a single view in Windows Explorer.</span></span> <span data-ttu-id="c4fc7-106">Bibliotheksbeschreibungsdateien folgen dem Schema der Bibliotheksbeschreibung und werden als \* .library-ms-Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-106">Library description files follow the Library Description schema and are saved as \*.library-ms files.</span></span>

<span data-ttu-id="c4fc7-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="c4fc7-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="c4fc7-108">Übersicht über das Schema der Bibliotheksbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c4fc7-108">Overview of the Library Description Schema</span></span>](#overview-of-the-library-description-schema)
-   [<span data-ttu-id="c4fc7-109">Namespaceversionsierung</span><span class="sxs-lookup"><span data-stu-id="c4fc7-109">Namespace Versioning</span></span>](#namespace-versioning)
-   [<span data-ttu-id="c4fc7-110">Beispiel für eine Bibliotheksbeschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4fc7-110">Example of a Library Description File</span></span>](#example-of-a-library-description-file)
-   [<span data-ttu-id="c4fc7-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4fc7-111">Related topics</span></span>](#related-topics)

## <a name="overview-of-the-library-description-schema"></a><span data-ttu-id="c4fc7-112">Übersicht über das Schema der Bibliotheksbeschreibung</span><span class="sxs-lookup"><span data-stu-id="c4fc7-112">Overview of the Library Description Schema</span></span>

<span data-ttu-id="c4fc7-113">Bibliotheken enthalten Dateien, die an einem oder mehreren Speicherorten gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-113">Libraries contain files that are stored in one or more storage locations.</span></span> <span data-ttu-id="c4fc7-114">Bibliotheken speichern diese Dateien nicht tatsächlich. Stattdessen überwachen sie die Ordner, die die Dateien enthalten, und ermöglichen Es Benutzern, auf die Dateien auf unterschiedliche Weise zu zugreifen und sie zu anordnen.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-114">Libraries do not actually store these files; instead, they monitor the folders that contain the files, and let users access and arrange the files in different ways.</span></span> <span data-ttu-id="c4fc7-115">Beispielsweise kann ein Benutzer Musikdateien in mehreren Ordnern auf einer lokalen Festplatte und auch auf einer externen Festplatte haben.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-115">For example, a user can have music files in multiple folders on a local hard disk and also on an external hard disk.</span></span> <span data-ttu-id="c4fc7-116">Mithilfe **Musik Bibliothek** kann der Benutzer gleichzeitig auf alle diese Dateien zugreifen und sie alle nach Interpretenname oder Albumtitel als einzelne Gruppe sortieren.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-116">Using the **Music Library**, the user can access all of those files at the same time and sort them all by artist name or album title as a single group.</span></span>

<span data-ttu-id="c4fc7-117">Das Schema der Bibliotheksbeschreibung besteht aus drei Hauptteilen, die in der folgenden Tabelle beschrieben sind:</span><span class="sxs-lookup"><span data-stu-id="c4fc7-117">The Library Description schema consists of three major parts, described in the following table:</span></span>



| <span data-ttu-id="c4fc7-118">Teil</span><span class="sxs-lookup"><span data-stu-id="c4fc7-118">Part</span></span>                        | <span data-ttu-id="c4fc7-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c4fc7-119">Description</span></span>                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4fc7-120">Allgemeine Bibliotheksinformationen</span><span class="sxs-lookup"><span data-stu-id="c4fc7-120">General library information</span></span> | <span data-ttu-id="c4fc7-121">Informationen zur Bibliothek, z. B. Name, Besitzer, Version, Symbol, die der Windows-Explorer verwenden kann, wenn die Bibliothek einem Benutzer angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-121">Information about the library, such as name, owner, version, icon, that Windows Explorer can use when it displays the library to a user.</span></span>                   |
| <span data-ttu-id="c4fc7-122">Bibliothekseigenschaften</span><span class="sxs-lookup"><span data-stu-id="c4fc7-122">Library properties</span></span>          | <span data-ttu-id="c4fc7-123">Mindestens eine Eigenschaft, die die Bibliothek beschreibt.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-123">One or more properties that describe the library.</span></span> <span data-ttu-id="c4fc7-124">Diese benutzerdefinierten Eigenschaften sind bibliotheksspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-124">These custom properties are specific to the library.</span></span>                                                     |
| <span data-ttu-id="c4fc7-125">Bibliotheksstandorte</span><span class="sxs-lookup"><span data-stu-id="c4fc7-125">Library locations</span></span>           | <span data-ttu-id="c4fc7-126">Mindestens ein Suchconnectors, der Speicherorte identifiziert, die in die Bibliothek enthalten sein sollten.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-126">One or more search connectors that identify storage locations to include in the library.</span></span> <span data-ttu-id="c4fc7-127">Jeder dieser Speicherorte kann auch über einen eindeutigen Satz von Eigenschaften verfügen.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-127">Each of these locations can also have a unique set of properties.</span></span> |



 

<span data-ttu-id="c4fc7-128">Bibliotheksdateien in Windows 7 werden im bekannten Ordner \_ FOLDERID-Bibliotheken gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-128">Library files in Windows 7 are stored in the known folder, FOLDERID\_Libraries.</span></span> <span data-ttu-id="c4fc7-129">Standardmäßig befindet sich der Ordner FOLDERID Libraries unter \_ %USERPROFILE% \\ AppData \\ Roaming Microsoft \\ Windows \\ \\ Libraries.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-129">By default, the FOLDERID\_Libraries folder is located at %USERPROFILE%\\AppData\\Roaming\\Microsoft\\Windows\\Libraries.</span></span>

## <a name="namespace-versioning"></a><span data-ttu-id="c4fc7-130">Namespaceversionsierung</span><span class="sxs-lookup"><span data-stu-id="c4fc7-130">Namespace Versioning</span></span>

<span data-ttu-id="c4fc7-131">Versionen des Dateiformats bibliotheksbeschreibung ( \* .library-ms) werden durch Ändern des Namespace nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-131">Versions of the Library Description file format (\*.library-ms) are tracked by changing the namespace.</span></span> <span data-ttu-id="c4fc7-132">Für Windows 7 hat das Dateiformat den folgenden Standardnamespace: https://schemas.microsoft.com/windows/2009/library .</span><span class="sxs-lookup"><span data-stu-id="c4fc7-132">For Windows 7, the file format has the following default namespace: https://schemas.microsoft.com/windows/2009/library.</span></span>

<span data-ttu-id="c4fc7-133">Versionen des Bibliotheksinhalts werden jedoch mithilfe des -Elements [<version>](schema-library-version.md) in einer bestimmten Bibliotheksbeschreibungsdatei nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-133">Versions of the library contents, however, are tracked by using the [<version>](schema-library-version.md) element in a specific Library Description file.</span></span>

## <a name="example-of-a-library-description-file"></a><span data-ttu-id="c4fc7-134">Beispiel für eine Bibliotheksbeschreibungsdatei</span><span class="sxs-lookup"><span data-stu-id="c4fc7-134">Example of a Library Description File</span></span>

<span data-ttu-id="c4fc7-135">Im Folgenden finden Sie ein Beispiel für eine Bibliotheksbeschreibungsdatei, die eine Bibliothek für Dokumentdateien definiert.</span><span class="sxs-lookup"><span data-stu-id="c4fc7-135">The following is an example of a Library Description file that defines a library for document files.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="c4fc7-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c4fc7-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c4fc7-137">folderType-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-137">folderType Element (Library Schema)</span></span>](schema-library-foldertype.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-138">iconReference-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-138">iconReference Element (Library Schema)</span></span>](schema-library-iconreference.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-139">isLibraryPinned-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-139">isLibraryPinned Element (Library Schema)</span></span>](schema-library-islibrarypinned.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-140">libraryDescription-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-140">libraryDescription Element (Library Schema)</span></span>](schema-librarydescription.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-141">name-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-141">name Element (Library Schema)</span></span>](schema-library-name.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-142">ownerSID-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-142">ownerSID Element (Library Schema)</span></span>](schema-library-ownersid.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-143">property-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-143">property Element (Library Schema)</span></span>](schema-library-property.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-144">propertyStore-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-144">propertyStore Element (Library Schema)</span></span>](schema-library-propertystore.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-145">searchConnectorDescription-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-145">searchConnectorDescription Element (Library Schema)</span></span>](schema-library-searchconnectordescription.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-146">searchConnectorDescriptionList-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-146">searchConnectorDescriptionList Element (Library Schema)</span></span>](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-147">templateInfo-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-147">templateInfo Element (Library Schema)</span></span>](schema-library-templateinfo.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-148">version-Element (Bibliotheksschema)</span><span class="sxs-lookup"><span data-stu-id="c4fc7-148">version Element (Library Schema)</span></span>](schema-library-version.md)
</dt> <dt>

[<span data-ttu-id="c4fc7-149">Suchconnectorbeschreibungsschema</span><span class="sxs-lookup"><span data-stu-id="c4fc7-149">Search Connector Description Schema</span></span>](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
