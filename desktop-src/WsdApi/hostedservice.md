---
description: Definiert einen Dienst, der in einer Host Generatorfunktion gehostet werden soll.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: tustedservice-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfcf2f4c67cadf90279221fd5bdfd518e285e844
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863991"
---
# <a name="hostedservice-element"></a>tustedservice-Element

Definiert einen Dienst, der in einer Host Generatorfunktion gehostet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<hostedService>
  child elements
</hostedService>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                                                                                                               |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>     | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/> |
| [**PortType**](porttype.md)<br/>     | Der Porttyp, für den Code generiert werden soll.<br/> <br/>                                                                                                       |
| [**proxyClass**](proxyclass.md)<br/> | Der Klassenname, der aus der Generatorfunktion generiert wird.<br/> <br/>                                                                                                      |
| [**ServiceID**](serviceid.md)<br/>   | Ein URI, der den Dienst Bezeichner darstellt.<br/> <br/>                                                                                                      |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
codeName(
  ServiceID, 
  proxyClass, 
  portType+
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Die Ausgabedatei Spezifikation für den Code-Generator.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




