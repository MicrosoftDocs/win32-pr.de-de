---
description: Das- <version> Element gibt die Inhalts Version dieser Bibliothek an. Dieses Element hat keine Attribute und keine untergeordneten Elemente.
ms.assetid: 77FD5EF6-6B6F-48e1-973F-AC069F729613
title: Version-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7b16a6078a16f4ebbe5e995503114996572f1b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977848"
---
# <a name="version-element-library-schema"></a>Version-Element (Bibliotheks Schema)

Das- <version> Element gibt die Inhalts Version dieser Bibliothek an. Dieses Element hat keine Attribute und keine untergeordneten Elemente.

## <a name="syntax"></a>Syntax

``` syntax
<!-- version -->
<xs:element name="version" type="xs:int" minOccurs="0"/>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente |
|------------------------------------------------------------------------------|----------------|
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) | Keine           |



 

## <a name="remarks"></a>Bemerkungen

Die Inhalts Version der Bibliothek unterscheidet sich von der Dateiformat \* Version (. Library-MS) der Bibliothek. Die Dateiformat Version der Bibliothek wird im- [Namespace](library-schema-entry.md)angegeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bibliotheks Beschreibungs Schema](library-schema-entry.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
