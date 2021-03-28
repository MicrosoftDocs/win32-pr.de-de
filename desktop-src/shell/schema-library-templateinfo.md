---
description: Das- <templateInfo> Element ist ein Container für das foldertype-Element, das einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: C555097A-E7B8-45ef-8CFA-19CFBC5E9D5A
title: templateingefo-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dae06a57a1b30407e2513e03f30ae6a4da13e849
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527305"
---
# <a name="templateinfo-element-library-schema"></a>templateingefo-Element (Bibliotheks Schema)

Das- <templateInfo> Element ist ein Container für das [foldertype](schema-library-foldertype.md) -Element, das einen Ordnertyp zum Anzeigen der Ergebnisse einer Abfrage über diese Bibliothek angibt. Dieses Element ist optional und besitzt keine Attribute.

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
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) | [foldertype-Element (Bibliotheks Schema)](schema-library-foldertype.md)       |
|                                                                              | [PropertyStore-Element (Bibliotheks Schema)](schema-library-propertystore.md) |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
