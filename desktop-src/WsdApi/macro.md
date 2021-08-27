---
description: Definiert Text oder CDATA, der vom include-Element wiederverwendet werden soll.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee876e04934a328e73b6e45d8442249ad3d749fc3b40fa45652c89979fcff6e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991720"
---
# <a name="macro-element"></a>macro-Element

Definiert Text oder CDATA, der vom include-Element wiederverwendet [**werden**](include.md) soll.

## <a name="usage"></a>Verbrauch

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attribute



| attribute           | type                         | Erforderlich       | Beschreibung                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | \_Zeichenfolge<br/> | Ja<br/> | Der Name des Makros.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | Beschreibung                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer XML-Skriptdatei des WSDAPI-Codegenerators.<br/> <br/> |



## <a name="remarks"></a>Hinweise

WsdCodeGen definiert ein Makro mit dem Namen **DoNotModify.** Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweisen soll, den generierten Code nicht zu ändern.

Der folgende XML-Code zeigt, wie das **DoNotModify-Makro enthalten** ist. Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




