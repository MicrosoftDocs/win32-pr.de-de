---
description: Das- <name> Element gibt den Namen dieser Bibliothek an. Dieses Element ist erforderlich und besitzt keine Attribute oder untergeordneten Elemente.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: Name-Element (Bibliotheks Schema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d38baa32587ee04c62c8c3086d5353e8eed9e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995175"
---
# <a name="name-element-library-schema"></a>Name-Element (Bibliotheks Schema)

Das- <name> Element gibt den Namen dieser Bibliothek an. Dieses Element ist erforderlich und besitzt keine Attribute oder untergeordneten Elemente.

## <a name="syntax"></a>Syntax

``` syntax
<!-- name -->
<xs:element name="libraryDescription">
    <xs:complexType>
        <xs:all>
            <xs:element name="name" type="xs:string"/>
...
</libraryDescription>
```

## <a name="element-information"></a>Elementinformationen



| Übergeordnetes Element                                                               | Untergeordnete Elemente |
|------------------------------------------------------------------------------|----------------|
| [librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Bemerkungen

Der Name ist der Anzeige Name der Bibliothek, der in Windows-Explorer angezeigt wird. Der Name kann <dllname> <index> wie im folgenden Beispiel in einem Format wie im folgenden Beispiel angegeben werden.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[librarydescription-Element (Bibliotheks Schema)](schema-librarydescription.md)
</dt> <dt>

[Suchdienst-Beschreibungs Schema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
