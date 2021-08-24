---
description: Das <iconReference> -Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an. Dieses Element ist optional und verfügt über keine Attribute oder untergeordneten Elemente.
title: iconReference-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 7A35B014-1E01-4da2-AA64-4CFC3436C6D9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 84e200fa4969dc376661bd32851296d80c74120939afc995754cb2937ea04be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119820230"
---
# <a name="iconreference-element-library-schema"></a>iconReference-Element (Bibliotheksschema)

Das <iconReference> -Element gibt ein benutzerdefiniertes Symbol für diese Bibliothek an. Dieses Element ist optional und verfügt über keine Attribute oder untergeordneten Elemente.

## <a name="syntax"></a>Syntax


```
<!-- iconReference -->
    <xs:element name="iconReference" type="xs:string" minOccurs="0"/>
```



## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente |
|------------------------------------------------------------------------------|----------------|
| [libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Der Symbolverweis muss in einem für die [**PathParseIconLocation-Funktion**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathparseiconlocationa) geeigneten Formular angegeben werden. Beispiel: `ModuleFileName,IconResourceIndex`.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[folderType-Element (Bibliotheksschema)](schema-library-foldertype.md)
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

 

 



