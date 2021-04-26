---
description: Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.
ms.assetid: d43baeff-c941-4ce9-a6ae-8aa61ef44048
title: stubDeclarations-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1543883b4d41e7571cd4a4725e2aeab181530d30
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996407"
---
# <a name="stubdeclarations-element"></a>stubDeclarations-Element

Generiert Deklarationen für Stubfunktionen für Porttypvorgänge.

## <a name="usage"></a>Verbrauch

``` syntax
<stubDeclarations>
  child elements
</stubDeclarations>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                                      |
|-------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**events**](events.md)<br/>       | Gibt an, ob verknüpfte Ereignisse in den generierten Funktionen enthalten sind.<br/> <br/> |
| [**Vorgang**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                 |
| [**Porttype**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  events?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Codegenerator aus.<br/> <br/> |



## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




