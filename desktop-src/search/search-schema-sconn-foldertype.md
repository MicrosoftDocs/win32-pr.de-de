---
description: Das <folderType> -Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist. Es verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: folderType-Element (Search Connector Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6b9d5682a85126a467c051b9f1103a4ac10f2f6936cc24dd4438a5f8c75d44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117862599"
---
# <a name="foldertype-element-search-connector-schema"></a>folderType-Element (Search Connector Schema)

Das <folderType> -Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das <templateInfo> Element vorhanden ist. Es verfügt über keine Attribute und keine untergeordneten Elemente.

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
| [templateInfo-Element (Connectorschema suchen)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Hinweise

Die Standard-GUID ist {8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}, ein allgemeiner Ordnertyp für Connectors für die Verbundsuche (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Beispiel für ein folderType-Element


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



