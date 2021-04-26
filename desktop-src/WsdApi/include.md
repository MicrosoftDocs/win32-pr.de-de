---
description: Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c8237ec865cd3cfbb80f500358e8f363be8f230
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995777"
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



| Attribut            | type                         | Erforderlich      | BESCHREIBUNG                                              |
|----------------------|------------------------------|---------------|----------------------------------------------------------|
| **datei**<br/>  | \_Zeichenfolge<br/> | Nein<br/> | Der Pfad zu der datei, die enthalten sein soll.<br/> <br/>  |
| **Makro**<br/> | \_Zeichenfolge<br/> | Nein<br/> | Der Name des makros, das enthalten sein soll.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Leitet den Codegenerator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.<br/> <br/> |



## <a name="remarks"></a>Hinweise

Entweder das **Makroattribut** oder **das Dateiattribut** muss angegeben werden. Geben Sie nicht beide Attribute an.

WsdCodeGen definiert ein Makro mit dem Namen **DoNotModify.** Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentarblock mit hoher Sichtbarkeit, der Entwickler anweisen soll, den generierten Code nicht zu ändern.

## <a name="examples"></a>Beispiele

Der folgende XML-Code zeigt, wie das **DoNotModify-Makro enthalten** ist. Dieser XML-Code kann einer XML-Konfigurationsdatei für WsdCodeGen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



| Bezeichnung | Wert |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




