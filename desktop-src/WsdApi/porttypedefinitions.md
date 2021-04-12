---
description: Generiert C-Konstanten für Porttypen.
ms.assetid: 6ad0d163-df51-48b6-aad7-a4b018688872
title: porttypeer Definitions Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60f55408df938ed95af14c69b2676473ac1bda71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216163"
---
# <a name="porttypedefinitions-element"></a>porttypeer Definitions Element

Generiert C-Konstanten für Porttypen.

## <a name="usage"></a>Verbrauch

``` syntax
<portTypeDefinitions>
  child elements
</portTypeDefinitions>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                   | BESCHREIBUNG                                                                                                                                                                       |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codeName**](codename.md)<br/>                   | Gibt den Namen an, der für den Porttyp im generierten Code verwendet werden soll. Standardmäßig wird der Codename aus dem qualifizierten Namen des Porttyps generiert.<br/> <br/>         |
| [**eventstubfunction**](eventstubfunction.md)<br/> | Gibt an, ob Stub-Funktions Verweise in den Vorgangs Strukturen in den Porttyp Definitionen für Benachrichtigungs Vorgänge enthalten sein sollen.<br/> <br/>        |
| [**Betriebs**](operation.md)<br/>                 | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>                                                                                                  |
| [**PortType**](porttype.md)<br/>                   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/>                                                                                                 |
| [**stubfunction**](stubfunction.md)<br/>           | Gibt an, ob stubfunktions Verweise in die Vorgangs Strukturen in den Porttyp Definitionen für unidirektionale und bidirektionale Vorgänge eingeschlossen werden sollen.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*, 
  stubFunction?, 
  eventStubFunction?, 
  codeName?
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Dieses Element wird im Allgemeinen in C-Quelldateien verwendet, um die von [**porttypeer Deklarationen deklarierten Porttyp**](porttypedeclarations.md)Konstanten bereitzustellen.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




