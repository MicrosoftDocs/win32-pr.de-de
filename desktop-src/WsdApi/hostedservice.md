---
description: Definiert einen Dienst, der in einer Host-Generatorfunktion gehostet werden soll.
ms.assetid: 87ff447a-ced0-4079-b46d-239f0db37250
title: hostedService-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e96c9f6e010989f4844d93299bb34f1ab8893236
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994787"
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



| Element                                     | BESCHREIBUNG                                                                                                                                                               |
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



| Element                         | BESCHREIBUNG                                                                  |
|---------------------------------|------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Die Ausgabedateispezifikation für den Codegenerator.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Nein            |



 

 




