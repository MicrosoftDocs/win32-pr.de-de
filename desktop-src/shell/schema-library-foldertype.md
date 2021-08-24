---
description: Das <folderType> -Element gibt eine GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.
title: folderType-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 240550F0-B6AC-470e-8BF1-DB5A4068226B
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 8d35f09a10cc88ae3873a507b6fa7000812503890240ce0b808ffecc84f23fd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883950"
---
# <a name="foldertype-element-library-schema"></a>folderType-Element (Bibliotheksschema)

Das <folderType> -Element gibt eine GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist, andernfalls ist es optional. Dieses Element verfügt über keine Attribute und keine untergeordneten Elemente.

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
| [templateInfo-Element (Bibliotheksschema)](schema-library-templateinfo.md) |                |



 

## <a name="remarks"></a>Hinweise

Durch festlegen eines Ordnertyps werden die Spalten und Details bestimmt, die standardmäßig in Windows Explorer angezeigt werden. Ordnertypbezeichner ([**FOLDERTYPEID**](foldertypeid.md)) sind GUIDs, die in Shlguid.h definiert sind. In der folgenden Tabelle sind die GUIDs allgemeiner Ordnertypen aufgeführt.



| Ordnertyp      | GUID                                   |
|------------------|----------------------------------------|
| Generische Bibliothek  | {5f4eab9a-6833-4f61-899d-31cf46979d49} |
| Benutzerbibliotheken  | {C4D98F09-6124-4fe0-9942-826416082DA9} |
| Ordner "Dokumente" | {7D49D726-3C21-4F05-99AA-FDC2C9474656} |
| Ordner "Bilder"  | {B3690E58-E961-423B-B687-386EBFD83239} |
| Ordner "Videos"    | {5fa96407-7e77-483c-ac93-691d05850de8} |
| Ordner "Games"     | {b689b0d0-76d3-4cbb-87f7-585d0e0ce070} |
| Musik Ordner     | {94d6ddcc-4a68-4175-a374-bd584a510b78} |
| Kontakte         | {DE2B70EC-9BF7-4A93-BD3D-243F7881D492} |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

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

[propertyStore-Element (Bibliotheksschema)](schema-library-propertystore.md)
</dt> <dt>

[searchConnectorDescription-Element (Bibliotheksschema)](schema-library-searchconnectordescription.md)
</dt> <dt>

[searchConnectorDescriptionList-Element (Bibliotheksschema)](schema-library-searchconnectordescriptionlist.md)
</dt> <dt>

[templateInfo-Element (Bibliotheksschema)](schema-library-templateinfo.md)
</dt> <dt>

[version-Element (Bibliotheksschema)](schema-library-version.md)
</dt> </dl>

 

 



