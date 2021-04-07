---
description: Definiert die serviceid-und Types-Elemente für den Dienst Host.
ms.assetid: 95066c04-5bdc-4c97-98b8-1da9928d9395
title: Host-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec073a89cf1911ab363d757d36cd264c85c8a5c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863992"
---
# <a name="host-element"></a>Host-Element

Definiert die [**serviceid**](serviceid.md) -und [**types**](types.md) -Elemente für den Dienst Host.

## <a name="usage"></a>Verbrauch

``` syntax
<host>
  child elements
</host>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                 |
|-------------------------------------------|-----------------------------------------------------------------------------|
| [**ServiceID**](serviceid.md)<br/> | Definiert den Dienst Bezeichner für den Dienst Host.<br/> <br/> |
| [**Typen**](types.md)<br/>         | Definiert eine Liste der qualifizierten XSD-Namen.<br/> <br/>               |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  ServiceID, 
  Types
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                         | BESCHREIBUNG                                                                   |
|-------------------------------------------------|-------------------------------------------------------------------------------|
| [**hostmetadata**](hostmetadata.md)<br/> | Die hostingmetadaten für das Gerät, das implementiert werden soll.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




