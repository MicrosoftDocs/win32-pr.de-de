---
title: VML-Sichtbarkeits Attribut
description: VML-Sichtbarkeits Attribut
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342353"
---
# <a name="vml-visibility-attribute"></a>VML-Sichtbarkeits Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Bestimmt, ob eine Form angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* Style = "Visibility: *Expression* " >

**Skript Syntax**

*Element* . Style. Visibility = "*Ausdruck*"

*Ausdruck* = *Element*. Style. Visibility

**Anmerkungen**

Das **Visibility** -Attribut ähnelt dem Standard-HTML- **Sichtbarkeits** Attribut für Stile.

Mögliche Werte:



| Wert    | BESCHREIBUNG                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | Die Form ist sichtbar.                                                                                                                                                                   |
| hidden   | Die Form ist nicht sichtbar, aber ist noch Teil des Flusses der Objekte im Browser. Mausereignisse werden nicht verarbeitet.                                                                  |
| inherit  | Standard. Der Sichtbarkeits Zustand wird vom übergeordneten Element der Form geerbt. Microsoft Office Anwendungen verwenden nur " **erben** " und " **Hidden**". alle anderen Werte werden als **Vererbung** zugeordnet. |
| Reduzieren | Wird für grafische Bearbeitungsanwendungen verwendet, die Gruppen von Formen reduzieren können. beispielsweise outliners.                                                                                     |



 

*VML-Standard Attribut*

**Beispiel**

Der folgende Code erstellt eine Form, macht Sie jedoch ausgeblendet. Andere Objekte im Dokument fließen um diese, sodass ein Leerzeichen die gleiche Größe wie die Form hat.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Beispiel für das Sichtbarkeits Attribut](/previous-versions/bb264100(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 