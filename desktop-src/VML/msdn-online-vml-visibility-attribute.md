---
title: VML-Sichtbarkeitsattribut
description: VML-Sichtbarkeitsattribut
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2087a8c5915b400f32f6007d58c5c20344f9abab1e2c5bc5d4c93da74ddf1182
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346182"
---
# <a name="vml-visibility-attribute"></a>VML-Sichtbarkeitsattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Version 9 Windows Internet Explorer ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen weit verbreiteten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Bestimmt, ob eine Form angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge.**

**Gilt für**

[Formen](shape-element--vml.md)

**Tagsyntax**

<v: *element* style="visibility: *expression* ">

**Skriptsyntax**

*element* .style.visibility="*expression*"

*expression* = *Element*.style.visibility

**Anmerkungen**

Das **Visibility-Attribut** ähnelt dem STANDARDMÄßIGEN **HTML-Sichtbarkeitsattribut** für Stile.

Mögliche Werte:



| Wert    | BESCHREIBUNG                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| visible  | Die Form ist sichtbar.                                                                                                                                                                   |
| hidden   | Die Form ist nicht sichtbar, ist aber weiterhin Teil des Flusses der Objekte im Browser. Mausereignisse werden nicht verarbeitet.                                                                  |
| inherit  | Standard. Der Sichtbarkeitszustand wird vom übergeordneten Element der Form geerbt. Microsoft Office Anwendungen verwenden nur **erben** und **ausgeblendet.** alle anderen Werte werden zugeordnet, um zu **erben.** |
| Reduzieren | Wird für grafische Bearbeitungsanwendungen verwendet, die Gruppen von Formen reduzieren können. z. B. Gliederungen.                                                                                     |



 

*VML-Standardattribut*

**Beispiel**

Mit dem folgenden Code wird eine Form erstellt, aber ausgeblendet. Andere Objekte im Dokument werden um ihn herum fließen, und ein Raum bleibt die gleiche Größe wie die Form.


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



[Sichtbarkeitsattribut – Beispiel.](/previous-versions/bb264100(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 