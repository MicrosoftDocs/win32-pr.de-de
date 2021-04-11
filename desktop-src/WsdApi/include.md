---
description: Schließt den Inhalt eines Makros oder einer Datei in die generierte Ausgabe ein.
ms.assetid: 450ccfa6-b189-4557-bcb9-4aa29ac2356e
title: include-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f22cfde339ca218d4cd10525bbca3e57b8d836f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042679"
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
| **datei**<br/>  | Zeichen \_ Folge<br/> | Nein<br/> | Der Pfad zu der Datei, die eingeschlossen werden soll.<br/> <br/>  |
| **Hilfen**<br/> | Zeichen \_ Folge<br/> | Nein<br/> | Der Name des einzuschließenden Makros.<br/> <br/> |



## <a name="child-elements"></a>Untergeordnete Elemente

Es gibt keine untergeordneten Elemente.

## <a name="parent-elements"></a>Übergeordnete Elemente



| Element                         | BESCHREIBUNG                                                                                              |
|---------------------------------|----------------------------------------------------------------------------------------------------------|
| [**Datei**](file.md)<br/> | Weist den Code Generator an, eine Datei zu generieren, und gibt den Namen der Ausgabedatei an.<br/> <br/> |



## <a name="remarks"></a>Bemerkungen

Es muss entweder das **Macro** -Attribut oder das **File** -Attribut angegeben werden. Geben Sie nicht beide Attribute an.

Wsdcodegen definiert ein Makro mit dem Namen " **donotmodify**". Wenn dieses Makro enthalten ist, enthält der generierte Code einen Kommentar Block mit hoher Sichtbarkeit, der Entwicklern anweist, den generierten Code nicht zu ändern.

## <a name="examples"></a>Beispiele

Der folgende XML-Code zeigt, wie das **donotmodify** -Makro eingeschlossen wird. Diese XML-Datei kann einer XML-Konfigurationsdatei für wsdcodegen hinzugefügt werden.

``` syntax
<include macro="DoNotModify">
```

## <a name="element-information"></a>Elementinformationen



|                                     |               |
|-------------------------------------|---------------|
| Unterstützte Mindestversion (System)<br/> | Windows Vista |
| Kann leer bleiben                        | Ja           |



 

 




