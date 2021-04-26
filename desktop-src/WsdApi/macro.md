---
description: Definiert Text oder CDATA, der vom include-Element wiederverwendet werden soll.
ms.assetid: bf5cc1e2-b08e-45b6-8e07-5c69865b695b
title: macro-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f794566b0fd789c463d404289644976c8301a2e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107994327"
---
# <a name="macro-element"></a>macro-Element

Definiert Text oder CDATA, der vom [**include-Element**](include.md) wiederverwendet werden soll.

## <a name="usage"></a>Verbrauch

``` syntax
<macro
  name = "character_string"/>
```

## <a name="attributes"></a>Attribute



| Attribut           | type                         | Erforderlich       | BESCHREIBUNG                                   |
|---------------------|------------------------------|----------------|-----------------------------------------------|
| **name**<br/> | Zeichenfolge \_<br/> | Ja<br/> | Der Name des Makros.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                                     | BESCHREIBUNG                                                                         |
|---------------------------------------------|-------------------------------------------------------------------------------------|
| [**wsdCodeGen**](wsdcodegen.md)<br/> | Das Stammelement einer WSDAPI-Codegenerator-XML-Skriptdatei.<br/> <br/> |



## <a name="remarks"></a>Hinweise

WsdCodeGen definiert ein Makro namens **DoNotModify.** Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweist, den generierten Code nicht zu ändern.

Der folgende XML-Code zeigt, wie das **DoNotModify-Makro** eingeschlossen wird. Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




