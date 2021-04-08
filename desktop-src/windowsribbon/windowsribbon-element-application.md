---
title: Application-Element
description: Stellt das Element der obersten Ebene in der Markup Spezifikation des Windows-Menü Band Frameworks dar.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Windows-Menüband für Anwendungs Element
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9b116879a918ca0437c7f2bdd201ef4ffd6d3c61
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "103734713"
---
# <a name="application-element"></a>Application-Element

Stellt das Element der obersten Ebene in der Markup Spezifikation des Windows-Menü Band Frameworks dar.

## <a name="usage"></a>Verbrauch

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Attribute



| Attribut            | type                 | Erforderlich       | BESCHREIBUNG                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Ja<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> Der URI für die Markup-Namespace Bindung des Menübands. <br/> </dd> </dl> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | BESCHREIBUNG                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application. Commands**](windowsribbon-element-application-commands.md)<br/> | Kann höchstens einmal vorkommen<br/> <br/>  |
| [**Application. views**](windowsribbon-element-application-views.md)<br/>       | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente

Es gibt keine übergeordneten Elemente.

## <a name="remarks"></a>Bemerkungen

Erforderlich.

Muss genau einmal als Container für alle Menü Band Markup vorkommen.

Die untergeordneten Elemente des **Application** -Elements müssen in der angegebenen Reihenfolge vorkommen:

1.  [**Application. Commands**](windowsribbon-element-application-commands.md)
2.  [**Application. views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine Deklaration eines **Anwendungs** Elements.


```XML
<Application xmlns="http://schemas.microsoft.com/windows/2009/Ribbon">
...
</Application>
```



## <a name="element-information"></a>Elementinformationen



|                                     |           |
|-------------------------------------|-----------|
| Unterstützte Mindestversion (System)<br/> | Windows 7 |
| Kann leer bleiben                        | Nein        |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Deklarieren von Befehlen und Steuerelementen mit Menüband-Markup](windowsribbon-schema.md)
</dt> </dl>

 

 





