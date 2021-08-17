---
description: Definiert die Elemente ServiceID und Types für den Diensthost.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: host-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe0637c358fabe27f2a1203306cd53407d85ab8b52f2dcd7a827dd49becffda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738606"
---
# <a name="host-element"></a>host-Element

Definiert die [**Elemente ServiceID**](serviceid.md) und [**Types**](types.md) für den Diensthost.

## <a name="usage"></a>Verbrauch

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | Beschreibung                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Definiert den Dienstbezeichner für den Diensthost.<br/> <br/> |
| [**Typen**](types.md)<br/>         | Definiert eine Liste der qualifizierten XSD-Namen.<br/> <br/>               |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                         | Beschreibung                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostMetadata**](hostmetadata.md)<br/> | Die Hostingmetadaten für das zu implementierende Gerät.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




