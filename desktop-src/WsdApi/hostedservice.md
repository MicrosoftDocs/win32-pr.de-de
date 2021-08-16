---
description: Definiert einen Dienst, der in einer Host-Generatorfunktion gehostet werden soll.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08479e88214e5fe6d1fbbb6ff5a3fffb7bb2047e8b7ca08cde92d64dd7dd6b2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130792"
---
# <a name="hostedservice-element"></a>hostedService-Element

Definiert einen Dienst, der in einer Host-Generatorfunktion gehostet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                     | Beschreibung                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Codename**](codename.md)<br/>     | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**Porttype**](porttype.md)<br/>     | Porttyp, für den Code generiert werden soll.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Klassenname, der aus der Generatorfunktion generiert werden soll.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | Ein URI, der den Dienstbezeichner darstellt.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Die Ausgabedateispezifikation für den Codegenerator.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




