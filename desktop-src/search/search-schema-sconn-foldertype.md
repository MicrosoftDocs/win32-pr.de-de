---
description: Das- <folderType> Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das- <templateInfo> Element vorhanden ist. Sie verfügt über keine Attribute und keine untergeordneten Elemente.
ms.assetid: 2361bbf5-adeb-4189-a8ff-5fdd1c9b0ec6
title: foldertype-Element (Suchconnector-Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7d2a9e7f83dbe225427a8370cd8f5e948a46cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484403"
---
# <a name="foldertype-element-search-connector-schema"></a>foldertype-Element (Suchconnector-Schema)

Das- <folderType> Element gibt die GUID für den Ordnertyp an. Dieses Element ist erforderlich, wenn das- <templateInfo> Element vorhanden ist. Sie verfügt über keine Attribute und keine untergeordneten Elemente.

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
| [templateingefo-Element (Suchconnector-Schema)](search-schema-sconn-templateinfo.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Die Standard-GUID ist {8faf9629-1980-46ff-8023-9dceab9c3ee3}, ein allgemeiner Ordnertyp für Verbund Suchconnectors (OpenSearch).

## <a name="example-of-a-foldertype-element"></a>Beispiel für ein foldertype-Element


```
<!-- templateInfo and folderType -->
<templateInfo>
    <folderType>{8FAF9629-1980-46FF-8023-9DCEAB9C3EE3}</folderType>
</templateInfo
```



 

 



