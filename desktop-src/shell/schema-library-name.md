---
description: Das &lt; &gt; Name-Element gibt den Namen dieser Bibliothek an. Dieses Element ist erforderlich und verfügt über keine Attribute oder untergeordneten Elemente.
ms.assetid: 1F433405-5943-4579-BDAD-423C4E1A6E76
title: name-Element (Bibliotheksschema)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d32b6d929a58f19cc2b87a79af846d22fc0ebda
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122880856"
---
# <a name="name-element-library-schema"></a>name-Element (Bibliotheksschema)

Das &lt; &gt; Name-Element gibt den Namen dieser Bibliothek an. Dieses Element ist erforderlich und verfügt über keine Attribute oder untergeordneten Elemente.

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
| [libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md) |                |



 

## <a name="remarks"></a>Hinweise

Der Name ist der Anzeigebibliotheksname, der im Windows angezeigt wird. Der Name kann wie im folgenden Beispiel in einem &lt; DLL-Namen &gt; und &lt; &gt; Indexformat angegeben werden.


```
<?xml version="1.0" encoding="UTF-8"?>
<libraryDescription xmlns="http://schemas.microsoft.com/windows/2009/library">
  <name>@shell32.dll,-34575</name>
...
</libraryDescription>
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[libraryDescription-Element (Bibliotheksschema)](schema-librarydescription.md)
</dt> <dt>

[Suchconnectorbeschreibungsschema](../search/search-sconn-desc-schema-entry.md)
</dt> </dl>

 

 
