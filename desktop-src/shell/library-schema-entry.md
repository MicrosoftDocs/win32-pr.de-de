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
# <a name="library-description-schema"></a>Schema der Bibliotheksbeschreibung

Bibliotheksbeschreibungsdateien sind XML-Dateien, die Bibliotheken definieren. Bibliotheken aggregieren Elemente von lokalen und Remotespeicherorten in einer einzelnen Ansicht im Windows Explorer. Bibliotheksbeschreibungsdateien folgen dem Schema der Bibliotheksbeschreibung und werden als \* .library-ms-Dateien gespeichert.

Dieses Thema enthält folgende Abschnitte:

-   [Übersicht über das Schema der Bibliotheksbeschreibung](#overview-of-the-library-description-schema)
-   [Namespaceversionsierung](#namespace-versioning)
-   [Beispiel für eine Bibliotheksbeschreibungsdatei](#example-of-a-library-description-file)
-   [Zugehörige Themen](#related-topics)

## <a name="overview-of-the-library-description-schema"></a>Übersicht über das Schema der Bibliotheksbeschreibung

Bibliotheken enthalten Dateien, die an einem oder mehreren Speicherorten gespeichert sind. Bibliotheken speichern diese Dateien nicht tatsächlich. Stattdessen überwachen sie die Ordner, die die Dateien enthalten, und ermöglichen Es Benutzern, auf die Dateien auf unterschiedliche Weise zu zugreifen und sie zu anordnen. Beispielsweise kann ein Benutzer Musikdateien in mehreren Ordnern auf einer lokalen Festplatte und auch auf einer externen Festplatte haben. Mithilfe **Musik Bibliothek** kann der Benutzer gleichzeitig auf alle diese Dateien zugreifen und sie alle nach Interpretenname oder Albumtitel als einzelne Gruppe sortieren.

Das Schema der Bibliotheksbeschreibung besteht aus drei Hauptteilen, die in der folgenden Tabelle beschrieben sind:



| Teil                        | BESCHREIBUNG                                                                                                                                                |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Allgemeine Bibliotheksinformationen | Informationen zur Bibliothek, z. B. Name, Besitzer, Version, Symbol, die der Windows-Explorer verwenden kann, wenn die Bibliothek einem Benutzer angezeigt wird.                   |
| Bibliothekseigenschaften          | Mindestens eine Eigenschaft, die die Bibliothek beschreibt. Diese benutzerdefinierten Eigenschaften sind bibliotheksspezifisch.                                                     |
| Bibliotheksstandorte           | Mindestens ein Suchconnectors, der Speicherorte identifiziert, die in die Bibliothek enthalten sein sollten. Jeder dieser Speicherorte kann auch über einen eindeutigen Satz von Eigenschaften verfügen. |



 

Bibliotheksdateien in Windows 7 werden im bekannten Ordner \_ FOLDERID-Bibliotheken gespeichert. Standardmäßig befindet sich der Ordner FOLDERID Libraries unter \_ %USERPROFILE% \\ AppData \\ Roaming Microsoft \\ Windows \\ \\ Libraries.

## <a name="namespace-versioning"></a>Namespaceversionsierung

Versionen des Dateiformats bibliotheksbeschreibung ( \* .library-ms) werden durch Ändern des Namespace nachverfolgt. Für Windows 7 hat das Dateiformat den folgenden Standardnamespace: https://schemas.microsoft.com/windows/2009/library .

Versionen des Bibliotheksinhalts werden jedoch mithilfe des -Elements [<version>](schema-library-version.md) in einer bestimmten Bibliotheksbeschreibungsdatei nachverfolgt.

## <a name="example-of-a-library-description-file"></a>Beispiel für eine Bibliotheksbeschreibungsdatei

Im Folgenden finden Sie ein Beispiel für eine Bibliotheksbeschreibungsdatei, die eine Bibliothek für Dokumentdateien definiert.


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

 

 
