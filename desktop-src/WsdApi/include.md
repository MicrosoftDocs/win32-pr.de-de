---
description: Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8029f58d9d1627a315fcfd02aa4f311d0a717361abf587aa92c52134b78e5958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119856590"
---
# <a name="include-element"></a>include-Element

Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.

## <a name="usage"></a>Verbrauch

``` syntax
<include
  macro = "character_string"
  file = "character_string"/>
```

## <a name="attributes"></a>Attribute



| attribute            | type                         | Erforderlich      | BESCHREIBUNG                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **datei**<br/>  | Zeichenfolge \_<br/> | Nein<br/> | Der Pfad zur einzufügende Datei.<br/> <br/>  |
| **Makro**<br/> | Zeichenfolge \_<br/> | Nein<br/> | Der Name des einzufügende Makros.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | Beschreibung                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Weist den Codegenerator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Entweder  das Makroattribut oder das **Dateiattribut** muss angegeben werden. Geben Sie nicht beide Attribute an.

WsdCodeGen definiert ein Makro namens **DoNotModify.** Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweist, den generierten Code nicht zu ändern.

## <a name="examples"></a>Beispiele

Der folgende XML-Code zeigt, wie das **DoNotModify-Makro** eingeschlossen wird. Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




