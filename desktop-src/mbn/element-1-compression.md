---
description: ModemDMConfigProfile \/ ... \/ Komprimierung (v4)
MS-HAID: WWAN\_profile\_v4.element\_1\_Compression
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Komprimierung (v4)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8dc3acd6-5997-47a5-bd30-899569b9aad9
api_name:
- Compression
api_type:
- Schema
api_location: ''
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7d25f2b1946e55e8a5768c0f599330d26ad5cc6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480006"
---
# <a name="span-idwwan_profile_v4element_1_compressionspanmodemdmconfigprofilecompression-v4"></a><span id="WWAN_profile_v4.element_1_Compression"></span>ModemDMConfigProfile \/ ... \/ Komprimierung (v4)

Gibt an, ob die Komprimierung am Datenlink für Header und Datenübertragung verwendet wird.

Weitere Informationen finden Sie in der Dokumentation zum [**v1-Komprimierungselement.**](./schema-compression-contexttype-element.md)

## <a name="element-hierarchy"></a>Elementhierarchie

[\<MBNProfileExt\>](element-mbnprofileext.md)  
&nbsp;&nbsp;[\<Context\>](element-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

[\<ModemDMConfigProfile\>](element-modemdmconfigprofile.md)  
&nbsp;&nbsp;[\<Context\>](element-1-context.md)  
&nbsp;&nbsp;&nbsp;&nbsp;**\<Compression\>**

## <a name="syntax"></a>Syntax

``` syntax
<Compression>

  "DISABLE" | "ENABLE"

</Compression>
```

## <a name="span-idattributes_and_elementsspanspan-idattributes_and_elementsspanspan-idattributes_and_elementsspanattributes-and-elements"></a><span id="Attributes_and_Elements"></span><span id="attributes_and_elements"></span><span id="ATTRIBUTES_AND_ELEMENTS"></span>Attribute und Elemente

### <a name="span-idattributesspanspan-idattributesspanattributes"></a><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute

Keine.

### <a name="span-idchild_elementsspanspan-idchild_elementsspanspan-idchild_elementsspanchild-elements"></a><span id="Child_Elements"></span><span id="child_elements"></span><span id="CHILD_ELEMENTS"></span>Untergeordnete Elemente

Keine.

### <a name="span-idparent_elementsspanspan-idparent_elementsspanparent-elements"></a><span id="parent_elements"></span><span id="PARENT_ELEMENTS"></span>Übergeordnete Elemente


| Übergeordnetes Element | BESCHREIBUNG | 
|----------------|-------------|
| <a href="element-1-context.md">Context</a> | <p>Gibt die Parameter an, die zum Herstellen einer Datenverbindung erforderlich sind.</p> | 


 

## <a name="requirements"></a>Anforderungen


| | | <p>Namespace</p> | <p>https://www.microsoft.com/networking/WWAN/profile/v4</p> | 


 

 
