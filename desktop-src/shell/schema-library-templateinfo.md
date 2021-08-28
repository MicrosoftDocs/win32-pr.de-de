---
description: Das templateInfo-Element ist ein Container für das folderType-Element, der einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über &lt; &gt; diese Bibliothek angibt. Dieses Element ist optional und verfügt über keine Attribute.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: templateInfo-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f55fec64bf7418eef8e70c4cf8fa1ee47006c5f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885526"
---
# <a name="templateinfo-element-library-schema"></a>templateInfo-Element (Bibliotheksschema)

Das templateInfo-Element ist ein Container für das &lt; &gt; [folderType-Element,](schema-library-foldertype.md) der einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und verfügt über keine Attribute.

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

 

 
