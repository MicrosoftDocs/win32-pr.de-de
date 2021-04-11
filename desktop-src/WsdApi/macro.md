---
description: Definiert Text oder CDATA, der vom Include-Element wieder verwendet werden soll.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: Macro-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8759d4afb61883b8bf41472f276882643cfa552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216310"
---
# <a name="macro-element"></a>Macro-Element

Definiert Text oder CDATA, der vom [**include**](include.md) -Element wieder verwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attribute



| Attribut           | type                         | Erforderlich       | BESCHREIBUNG                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | Zeichen \_ Folge<br/> | Ja<br/> | Der Name des Makros.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdcodegen**](wsdcodegen.md)<br/> | Das Stamm Element einer XML-Skriptdatei des WSDAPI-Code-Generators.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Wsdcodegen definiert ein Makro mit dem Namen " **donotmodify**". Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentar Block mit hoher Sichtbarkeit, der Entwicklern anweist, den generierten Code nicht zu ändern.

Der folgende XML-Code zeigt, wie das **donotmodify** -Makro eingeschlossen wird. Diese XML-Datei kann einer XML-Konfigurationsdatei für wsdcodegen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




