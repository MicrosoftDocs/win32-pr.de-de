---
description: Das <templateInfo> -Element ist ein Container für das folderType-Element, der einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und verfügt über keine Attribute.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: templateInfo-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eda0c42e71db2e47335371b51d9dc819620e6b28dfac63ee9c0e2a640ccab0b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119942090"
---
# <a name="templateinfo-element-library-schema"></a>templateInfo-Element (Bibliotheksschema)

Das <templateInfo> -Element ist ein Container für das [folderType-Element,](schema-library-foldertype.md) der einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und verfügt über keine Attribute.

## <a name="syntax"></a>Syntax

``` syntax
<!-- templateInfo -->
<xs:element name="templateInfo" minOccurs="0">
    <xs:complexType>
        <xs:all>
            <xs:element name="folderType" minOccurs="0"/>
        </xs:all>
    </xs:complexType>
</xs:element>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente                                                             |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md) | [folderType-Element (Bibliotheksschema)](schema-library-foldertype.md)       |
|                                                                              | [propertyStore-Element (Bibliotheksschema)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schema der Bibliotheksbeschreibung](library-schema-entry.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
