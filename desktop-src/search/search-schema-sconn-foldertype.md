---
description: Das &lt; &gt; folderType-Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn &lt; das &gt; templateInfo-Element vorhanden ist. Sie verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: folderType-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b693a1ff7007e6d63e108d16abe77ee421b3821a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882465"
---
# <a name="foldertype-element-search-connector-schema"></a>folderType-Element (Search Connector Schema)

Das &lt; &gt; folderType-Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn &lt; das &gt; templateInfo-Element vorhanden ist. Sie verfügt über keine Attribute und keine untergeordneten Elemente.

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



| Übergeordnetes Element                                                                         | Untergeordnete Elemente |
|----------------------------------------------------------------------------------------|----------------|
| [templateInfo-Element (Search Connector Schema)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Hinweise

Die Standard-GUID ist {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, ein allgemeiner Ordnertyp für Connectors für die Verbundsuche (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Beispiel für ein folderType-Element


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



