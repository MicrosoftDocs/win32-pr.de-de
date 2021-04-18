---
description: Generiert C-Strukturdefinitionen für Nachrichten Typen.
ms.assetid: 68459b22-0f35-444a-969e-29695e735774
title: messagestructuredefinitions-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8840e4493cb97d33cb0dac8ce1ace97cc1789e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354627"
---
# <a name="messagestructuredefinitions-element"></a>messagestructuredefinitions-Element

Generiert C-Strukturdefinitionen für Nachrichten Typen.

## <a name="usage"></a>Verbrauch

``` syntax
<messageStructureDefinitions>
  child elements
</messageStructureDefinitions>
```

## <a name="attributes"></a>Attribute

Es gibt keine Attribute.

## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                   | BESCHREIBUNG                                                                       |
|-------------------------------------------|-----------------------------------------------------------------------------------|
| [**Betriebs**](operation.md)<br/> | Gibt einen Vorgang an, für den Code generiert werden soll.<br/> <br/>  |
| [**PortType**](porttype.md)<br/>   | Gibt den Porttyp an, für den Code generiert werden soll.<br/> <br/> |



### <a name="child-element-sequence"></a>Sequenz untergeordneter Elemente

``` syntax
(
  portType?, 
  operation*
)
```

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                    |
|---------------------------------|----------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Gibt eine Datei aus dem Code-Generator aus.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Auf Nachrichten Strukturen wird durch generierten Proxy-und Stubcode verwiesen. Dieses Element wird zum Generieren von Include-Dateien verwendet.

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




