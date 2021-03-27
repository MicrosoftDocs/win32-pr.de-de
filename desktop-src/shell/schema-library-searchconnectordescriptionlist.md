---
description: Dieses <searchConnectorDescriptionList> Element enthält eine Liste von Suchconnectors, die in dieser Bibliothek enthaltene Standorte zugeordnet sind. Jeder Suchconnector wird durch ein- <searchConnectorDescription> Element definiert. Dieses Element ist optional und besitzt keine Attribute.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: searchconnectordescriptionlist-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4d7295796f205ca0d20f220ba827abfd5470bdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980464"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>searchconnectordescriptionlist-Element (Bibliotheks Schema)

Dieses <searchConnectorDescriptionList> Element enthält eine Liste von Suchconnectors, die in dieser Bibliothek enthaltene Standorte zugeordnet sind. Jeder Suchconnector wird durch ein- <searchConnectorDescription> Element definiert. Dieses Element ist optional und besitzt keine Attribute.

## <a name="syntax"></a>Syntax

``` syntax
<!-- searchConnectorDescriptionList -->
    <xs:element name="searchConnectorDescriptionList" minOccurs="0">
          <xs:complexType>
            <xs:sequence minOccurs="0">
              <xs:element name="searchConnectorDescription" type="searchConnectorDescriptionType" minOccurs="0" maxOccurs="unbounded"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente                                                                                       |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) | [searchconnectordescription-Element (Bibliotheks Schema)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Bemerkungen

Suchconnectors für die Windows-Verbund Suche und die protokollhandlerbereiche können nicht in einer Bibliothek enthalten sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
