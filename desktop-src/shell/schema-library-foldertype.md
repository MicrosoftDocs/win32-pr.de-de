---
description: Das- <folderType> Element gibt eine GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional. Dieses Element hat keine Attribute und keine untergeordneten Elemente.
title: foldertype-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: c6d94906fa8c0debfa1ee49d95f5acd47aea2526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977857"
---
# <a name="foldertype-element-library-schema"></a>foldertype-Element (Bibliotheks Schema)

Das- <folderType> Element gibt eine GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional. Dieses Element hat keine Attribute und keine untergeordneten Elemente.

## <a name="syntax"></a>Syntax


```
<!-- folderType -->
    <xs:element name="templateInfo" minOccurs="0">
      <xs:complexType>
        <xs:all>
          <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
      </xs:complexType>
    </xs:element>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                           | Untergeordnete Elemente |
|--------------------------------------------------------------------------|----------------|
| [templateingefo-Element (Bibliotheks Schema)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Ordnertyp festlegen, werden die Spalten und Details, die standardmäßig in Windows Explorer angezeigt werden, bestimmt Ordnertyp-IDs ([**foldertypeid**](foldertypeid.md)) sind GUIDs, die in "shlguid. h" definiert sind. In der folgenden Tabelle sind die GUIDs der allgemeinen Ordner Typen aufgeführt.



| Ordnertyp      | GUID                                   |
|------------------|----------------------------------------|
| Generische Bibliothek  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Benutzer Bibliotheken  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Ordner "Dokumente" | {7d49d726-3c21-4f 05-99aa-f dc2c9474656} |
| Ordner "Bilder"  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Ordner "Videos"    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Ordner "Games"     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Ordner "Musik"     | {94d6ddcc-4a68-4175-A374-bd584a510 B78} |
| Kontakte         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

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

[PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md)
</dt> <dt>

[searchconnectordescription-Element (Bibliotheks Schema)](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchconnectordescriptionlist-Element (Bibliotheks Schema)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateingefo-Element (Bibliotheks Schema)](schema-library-templateinfo.md)
</dt> <dt>

[Version-Element (Bibliotheks Schema)](schema-library-version.md)
</dt> </dl>

 

 



