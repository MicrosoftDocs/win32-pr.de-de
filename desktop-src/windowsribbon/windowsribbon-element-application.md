---
title: Application-Element
description: Stellt das Element der obersten Ebene in der Markupspezifikation für Windows Menübandframework dar.
ms.assetid: 05396d8b-fbd1-40bb-8d0f-8ac11506e7db
keywords:
- Anwendungselement Windows Menüband
topic_type:
- apiref
api_name:
- Application
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4055e271ecf3313596b73aa36a5cbea37250416d9b517fb4512b89fbc203293a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810810"
---
# <a name="application-element"></a>Application-Element

Stellt das Element der obersten Ebene in der Markupspezifikation für Windows Menübandframework dar.

## <a name="usage"></a>Verwendung

``` syntax
<Application
  xmlns = "xs:string">
  child elements
</Application>
```

## <a name="attributes"></a>Attribute



| attribute            | Typ                 | Erforderlich       | Beschreibung                                                                                                                                                                                                       |
|----------------------|----------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **xmlns**<br/> | xs:string<br/> | Ja<br/> | <dt>`http://schemas.microsoft.com/windows/2009/Ribbon`<br/> </dt> <dd> Der URI für die Markupnamespacebindung des Menübands. <br/> </dd> </dl> |



## <a name="child-elements"></a>Untergeordnete Elemente



| Element                                                                               | Beschreibung                                    |
|---------------------------------------------------------------------------------------|------------------------------------------------|
| [**Application.Commands**](windowsribbon-element-application-commands.md)<br/> | Kann höchstens einmal auftreten.<br/> <br/>  |
| [**Application.Views**](windowsribbon-element-application-views.md)<br/>       | Muss genau einmal auftreten<br/> <br/> |



## <a name="parent-elements"></a>Übergeordnete Elemente

Es gibt keine übergeordneten Elemente.

## <a name="remarks"></a>Hinweise

Erforderlich.

Muss genau einmal als Container für das gesamte Menübandmarkup auftreten.

Die untergeordneten Elemente des **Application-Elements** müssen in der angegebenen Reihenfolge auftreten:

1.  [**Application.Commands**](windowsribbon-element-application-commands.md)
2.  [**Application.Views**](windowsribbon-element-application-views.md)

## <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt eine **Application-Elementdeklaration.**


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

[Deklarieren von Befehlen und Steuerelementen mit Menübandmarkup](windowsribbon-schema.md)
</dt> </dl>

 

 





