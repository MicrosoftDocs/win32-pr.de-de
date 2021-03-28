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
# <a name="library-description-schema"></a>Bibliotheks Beschreibungs Schema

Bibliotheks Beschreibungsdateien sind XML-Dateien, die Bibliotheken definieren. Bibliotheken aggregieren Elemente aus lokalen und Remote Speicherorten in einer einzelnen Ansicht in Windows-Explorer. Bibliotheks Beschreibungsdateien folgen dem Bibliotheks Beschreibungs Schema und werden als \* . Library-MS-Dateien gespeichert.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht über das Bibliotheks Beschreibungs Schema](#overview-of-the-library-description-schema)
-   [Namespace Versionierung](#namespace-versioning)
-   [Beispiel für eine Bibliotheks Beschreibungsdatei](#example-of-a-library-description-file)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Übersicht über das Bibliotheks Beschreibungs Schema

Bibliotheken enthalten Dateien, die an einem oder mehreren Speicherorten gespeichert sind. Diese Dateien werden von Bibliotheken nicht gespeichert. Stattdessen überwachen Sie die Ordner, die die Dateien enthalten, und ermöglichen Benutzern den Zugriff auf und die Anordnung von Dateien auf verschiedene Weise. Beispielsweise kann sich ein Benutzer Musikdateien in mehreren Ordnern auf einer lokalen Festplatte und auch auf einer externen Festplatte befinden. Mithilfe der **Musikbibliothek** kann der Benutzer gleichzeitig auf alle diese Dateien zugreifen und diese nach dem Namen des Künstlers oder dem Albumtitel als einzelne Gruppe sortieren.

Das Bibliotheks Beschreibungs Schema besteht aus drei Hauptkomponenten, die in der folgenden Tabelle beschrieben werden:



|                             |                                                                                                                                                            |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeine Bibliotheksinformationen | Informationen zur Bibliothek, z. b. Name, Besitzer, Version, Symbol, die Windows Explorer verwenden kann, wenn Sie die Bibliothek für einen Benutzer anzeigt.                   |
| Bibliotheks Eigenschaften          | Eine oder mehrere Eigenschaften, die die Bibliothek beschreiben. Diese benutzerdefinierten Eigenschaften sind spezifisch für die Bibliothek.                                                     |
| Bibliotheks Speicherorte           | Mindestens ein suchverbinder, der die in der Bibliothek einzuschließenden Speicherorte identifiziert. Jeder dieser Standorte kann auch über einen eindeutigen Satz von Eigenschaften verfügen. |



 

Bibliotheksdateien in Windows 7 werden im bekannten Ordner, folderid-Bibliotheken, gespeichert \_ . Standardmäßig befindet sich der Ordner folderid \_ Libraries unter% User Profile% \\ AppData \\ Roaming \\ Microsoft Windows \\ - \\ Bibliotheken.

## <a name="namespace-versioning"></a>Namespace Versionierung

Versionen des Bibliotheks Beschreibungsdatei Formats ( \* . Library-MS) werden nachverfolgt, indem der-Namespace geändert wird. Für Windows 7 weist das Dateiformat den folgenden Standard Namespace auf: https://schemas.microsoft.com/windows/2009/library .

Versionen der Bibliotheksinhalte werden jedoch mithilfe des- [<version>](schema-library-version.md) Elements in einer bestimmten Bibliotheks Beschreibungsdatei nachverfolgt.

## <a name="example-of-a-library-description-file"></a>Beispiel für eine Bibliotheks Beschreibungsdatei

Im folgenden finden Sie ein Beispiel für eine Bibliotheks Beschreibungsdatei, die eine Bibliothek für Dokument Dateien definiert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[foldertype-Element (Bibliotheks Schema)](schema-library-foldertype.md)
</dt> <dt>

[iconReference-Element (Bibliotheks Schema)](schema-library-iconreference.md)
</dt> <dt>

[islibrarypinned-Element (Bibliotheks Schema)](schema-library-islibrarypinned.md)
</dt> <dt>

[librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md)
</dt> <dt>

[Name-Element (Bibliotheks Schema)](schema-library-name.md)
</dt> <dt>

[Besitzer-SID-Element (Bibliotheks Schema)](schema-library-ownersid.md)
</dt> <dt>

[Property-Element (Bibliotheks Schema)](schema-library-property.md)
</dt> <dt>

[PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md)
</dt> <dt>

[searchconnectordescription-Element (Bibliotheks Schema)](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchconnectordescriptionlist-Element (Bibliotheks Schema)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateingefo-Element (Bibliotheks Schema)](schema-library-templateinfo.md)
</dt> <dt>

[Version-Element (Bibliotheks Schema)](schema-library-version.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
