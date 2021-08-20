---
title: VML-Zielattribut
description: VML-Zielattribut
ms.assetid: 2e1cc002-65c9-4945-8c07-f23dc704d867
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79f290e6f1c6a2ed84959dc06efa47d1a5216bc1743f3b7c79ca3a5aa99df9f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754435"
---
# <a name="vml-target-attribute"></a>VML-Zielattribut

In diesem Thema wird VML beschrieben, ein Feature, das ab Windows Internet Explorer 9 als veraltet gilt. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Seit Dezember 2011 wurde dieses Thema archiviert. Daher wird sie nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [Archivierter Inhalt.](/previous-versions/windows/internet-explorer/ie-developer/) Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie unter [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Definiert einen Rahmen oder ein Fenster, in dem eine URL angezeigt wird. Lese-/Schreibzugriff. **Zeichenfolge**.

**Gilt für**

[Form](shape-element--vml.md)

**Tagsyntax**

<v: *element* target=" *ausdruck* ">

**Anmerkungen**

Das **Target-Attribut** ähnelt dem **HTML-Standardattribut Target** von Ankern.

Mögliche Werte:



| Wert      | Beschreibung                                                                                                                                                                                                                                                      |
|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TargetName | Zeichenfolge, die den Namen des Frames oder Fensters enthält, in dem das Dokument geladen werden soll.                                                                                                                                                                                 |
| \_leer    | Gibt an, dass das verknüpfte Dokument in ein neues leeres Fenster geladen wird. Dieses Fenster ist nicht benannt.                                                                                                                                                                  |
| \_Medien    | Ab Internet Explorer 6 für Windows XP Service Pack 2 ist das \_ Medienattribut veraltet und wird nicht mehr unterstützt. Dieser Wert ist erstmals in Internet Explorer 6 verfügbar und gibt an, dass das verknüpfte Dokument in die Medienleiste geladen werden soll.                |
| \_Elternteil   | Gibt an, dass das verknüpfte Dokument in das unmittelbar übergeordnete Dokument geladen wird, das den Link enthält.                                                                                                                                                      |
| \_Suche   | Ab Internet Explorer 7 für Windows XP Service Pack 2: Das \_ Suchattribut ist veraltet und wird nicht mehr unterstützt. Dieser Wert ist in Internet Explorer 6 erstmals verfügbar und gibt an, dass das verknüpfte Dokument in den Suchbereich des Browsers geladen werden soll. |
| \_self     | Gibt an, dass das verknüpfte Dokument in das Fenster geladen wird, in dem auf den Link geklickt wurde (das aktive Fenster).                                                                                                                                                  |
| \_Nach oben      | Gibt an, dass das verknüpfte Dokument in das oberste Fenster geladen wird.                                                                                                                                                                                            |



 

*VML-Standardattribut*

**Beispiel**

Wenn auf das Rechteck geklickt wird, lädt der Browser die Microsoft Corporation Startseite in dasselbe Fenster.


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com" target="_self"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



[Zielattribut – Beispiel.](/previous-versions/bb264096(v=vs.85)) (Erfordert Microsoft Internet Explorer 5 oder höher.)

 

 