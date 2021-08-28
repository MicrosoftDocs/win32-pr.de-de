---
description: Bibliotheksbeschreibungsdateien sind XML-Dateien, die Bibliotheken definieren.
ms.assetid: 12F6E6AE-2776-408c-B9AC-E885BE93C27F
title: Bibliotheksbeschreibungsschema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bfbaa8401468a6bab79cf4bccc5d7d4cd0ff7bb
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879646"
---
# <a name="library-description-schema"></a>Bibliotheksbeschreibungsschema

Bibliotheksbeschreibungsdateien sind XML-Dateien, die Bibliotheken definieren. Bibliotheken aggregieren Elemente von lokalen und Remotespeicherorten in einer einzigen Ansicht in Windows Explorer. Bibliotheksbeschreibungsdateien folgen dem Schema der Bibliotheksbeschreibung und werden als \* LIBRARY-MS-Dateien gespeichert.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht über das Bibliotheksbeschreibungsschema](#overview-of-the-library-description-schema)
-   [Namespaceversionsierung](#namespace-versioning)
-   [Beispiel für eine Bibliotheksbeschreibungsdatei](#example-of-a-library-description-file)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Übersicht über das Bibliotheksbeschreibungsschema

Bibliotheken enthalten Dateien, die an einem oder mehreren Speicherorten gespeichert sind. Bibliotheken speichern diese Dateien nicht. Stattdessen überwachen sie die Ordner, die die Dateien enthalten, und ermöglichen Benutzern den Zugriff auf und die Anordnung der Dateien auf unterschiedliche Weise. Beispielsweise kann ein Benutzer Musikdateien in mehreren Ordnern auf einer lokalen Festplatte und auch auf einer externen Festplatte speichern. Mithilfe der **Musik-Bibliothek** kann der Benutzer gleichzeitig auf alle diese Dateien zugreifen und sie alle nach Interpretenname oder Albumtitel als einzelne Gruppe sortieren.

Das Schema "Bibliotheksbeschreibung" besteht aus drei Hauptteilen, die in der folgenden Tabelle beschrieben werden:



| Teil                        | Beschreibung                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeine Bibliotheksinformationen | Informationen zur Bibliothek, z. B. Name, Besitzer, Version, Symbol, die Windows Explorer verwenden kann, wenn die Bibliothek einem Benutzer angezeigt wird.                   |
| Bibliothekseigenschaften          | Eine oder mehrere Eigenschaften, die die Bibliothek beschreiben. Diese benutzerdefinierten Eigenschaften sind spezifisch für die Bibliothek.                                                     |
| Bibliotheksspeicherorte           | Ein oder mehrere Suchconnectors, die Speicherorte identifizieren, die in die Bibliothek eingeschlossen werden sollen. Jeder dieser Speicherorte kann auch über einen eindeutigen Satz von Eigenschaften verfügen. |



 

Bibliotheksdateien in Windows 7 werden im bekannten Ordner FOLDERID \_ Libraries gespeichert. Standardmäßig befindet sich der Ordner FOLDERID \_ Libraries unter %USERPROFILE% \\ AppData \\ Roaming Microsoft \\ Windows \\ \\ Libraries.

## <a name="namespace-versioning"></a>Namespaceversionsierung

Versionen des Dateiformats "Bibliotheksbeschreibung" \* (.library-ms) werden durch Ändern des Namespace nachverfolgt. Für Windows 7 weist das Dateiformat den folgenden Standardnamespace auf: https://schemas.microsoft.com/windows/2009/library .

Versionen des Bibliotheksinhalts werden jedoch mithilfe des [ &lt; &gt; Versionselements](schema-library-version.md) in einer bestimmten Bibliotheksbeschreibungsdatei nachverfolgt.

## <a name="example-of-a-library-description-file"></a>Beispiel für eine Bibliotheksbeschreibungsdatei

Im Folgenden sehen Sie ein Beispiel für eine Bibliotheksbeschreibungsdatei, die eine Bibliothek für Dokumentdateien definiert.


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

[folderType-Element (Bibliotheksschema)](schema-library-foldertype.md)
</dt> <dt>

[iconReference-Element (Bibliotheksschema)](schema-library-iconreference.md)
</dt> <dt>

[isLibraryPinned-Element (Bibliotheksschema)](schema-library-islibrarypinned.md)
</dt> <dt>

[libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md)
</dt> <dt>

[name-Element (Bibliotheksschema)](schema-library-name.md)
</dt> <dt>

[ownerSID-Element (Bibliotheksschema)](schema-library-ownersid.md)
</dt> <dt>

[property-Element (Bibliotheksschema)](schema-library-property.md)
</dt> <dt>

[propertyStore-Element (Bibliotheksschema)](schema-library-propertystore.md)
</dt> <dt>

[searchConnectorDescription-Element (Bibliotheksschema)](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchConnectorDescriptionList-Element (Bibliotheksschema)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateInfo-Element (Bibliotheksschema)](schema-library-templateinfo.md)
</dt> <dt>

[version-Element (Bibliotheksschema)](schema-library-version.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
