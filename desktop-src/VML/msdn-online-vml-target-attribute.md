---
title: VML-Ziel Attribut
description: VML-Ziel Attribut
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1cb4e438cef8d10093aa2788fc1493d9e2dcc75
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106339069"
---
# <a name="vml-target-attribute"></a>VML-Ziel Attribut

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Definiert einen Frame oder ein Fenster, in dem eine URL angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *Element* target = " *Expression* " >

**Anmerkungen**

Das **Ziel** Attribut ähnelt dem Standard-HTML- **Ziel** Attribut von Ankern.

Mögliche Werte:



| Wert      | BESCHREIBUNG                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Zeichenfolge, die den Namen des Frames oder Fensters enthält, in dem das Dokument geladen werden soll.                                                                                                                                                                                 |
| \_Blitz    | Gibt an, dass das verknüpfte Dokument in ein neues leeres Fenster geladen wird. Dieses Fenster hat keinen Namen.                                                                                                                                                                  |
| \_Medien    | Ab Internet Explorer 6 für Windows XP Service Pack 2 \_ ist das Medien Attribut veraltet und wird nicht mehr unterstützt. Der erste in Internet Explorer 6 verfügbare Wert gibt an, dass das verknüpfte Dokument in die Medien Leiste geladen werden soll.                |
| \_übergeordneten   | Gibt an, dass das verknüpfte Dokument in das direkt übergeordnete Element des Dokuments geladen wird, das den Link enthält.                                                                                                                                                      |
| \_Such   | Ab Internet Explorer 7 für Windows XP Service Pack 2: das \_ Search-Attribut ist veraltet und wird nicht mehr unterstützt. Der erste in Internet Explorer 6 verfügbare Wert gibt an, dass das verknüpfte Dokument in den Suchbereich des Browsers geladen werden soll. |
| \_self     | Gibt an, dass das verknüpfte Dokument in das Fenster geladen wird, in dem auf den Link geklickt wurde (das aktive Fenster).                                                                                                                                                  |
| \_top      | Gibt an, dass das verknüpfte Dokument in das oberste Fenster geladen wird.                                                                                                                                                                                            |



 

*VML-Standard Attribut*

**Beispiel**

Beim Klicken auf das Rechteck lädt der Browser die Microsoft Corporation-Startseite im selben Fenster.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Beispiel für das Ziel Attribut](/previous-versions/bb264096(v=vs.85)). (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 