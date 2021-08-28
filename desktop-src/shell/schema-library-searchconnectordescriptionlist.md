---
description: Dieses &lt; searchConnectorDescriptionList-Element &gt; enthält eine Liste von Suchconnectors, die den in dieser Bibliothek enthaltenen Standorten zugeordnet sind. Jeder Suchconnector wird durch ein &lt; searchConnectorDescription-Element &gt; definiert. Dieses Element ist optional und weist keine Attribute auf.
ms.assetid: 58A7BC21-0EB8-4bcf-98EE-31A56A4BC58C
title: searchConnectorDescriptionList-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04edc3a3cb7353529dccca66ffa15e1604bdd1c0
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885606"
---
# <a name="searchconnectordescriptionlist-element-library-schema"></a>searchConnectorDescriptionList-Element (Bibliotheksschema)

Dieses &lt; searchConnectorDescriptionList-Element &gt; enthält eine Liste von Suchconnectors, die den in dieser Bibliothek enthaltenen Standorten zugeordnet sind. Jeder Suchconnector wird durch ein &lt; searchConnectorDescription-Element &gt; definiert. Dieses Element ist optional und weist keine Attribute auf.

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
| [libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md) | [searchConnectorDescription-Element (Bibliotheksschema)](schema-library-searchconnectordescription.md) |



 

## <a name="remarks"></a>Hinweise

Suchconnectors für Windows Verbundsuche und Protokollhandlerbereiche können nicht in einer Bibliothek enthalten sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheksbeschreibungsschema](library-schema-entry.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](/previous-versions//dd743009(v=vs.85))
</dt> </dl>

 

 
