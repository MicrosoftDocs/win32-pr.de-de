---
description: Einführung in DirectShow-Anwendungsprogrammierung
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Einführung in DirectShow-Anwendungsprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a448d49939e69b7c8a3b244b27a91a93eaf941eebf1960b7b2a53e4ad9137341
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823514"
---
# <a name="introduction-to-directshow-application-programming"></a>Einführung in DirectShow-Anwendungsprogrammierung

In diesem Artikel werden die grundlegenden Begriffe und Konzepte beschrieben, die in DirectShow verwendet werden. Nach dem Lesen dieses Abschnitts können Sie Ihre erste DirectShow-Anwendung schreiben.

**Filter und Filterdiagramme**

Der Baustein von DirectShow ist eine Softwarekomponente, die als Filter *bezeichnet wird.* Ein Filter ist eine Softwarekomponente, die einen Vorgang für einen Multimediastream ausführt. DirectShow-Filter können z. B.

-   Dateien lesen
-   Video von einem Videoaufnahmegerät erhalten
-   Decodieren verschiedener Streamformate, z. B. MPEG-1-Video
-   Übergeben von Daten an die Grafik- oder Soundkarte

Filter empfangen Eingaben und erzeugen Ausgaben. Wenn beispielsweise ein Filter MPEG-1-Video decodiert, ist die Eingabe der MPEG-codierte Stream, und die Ausgabe ist eine Reihe von unkomprimierten Videoframes.

In DirectShow führt eine Anwendung jede Aufgabe aus, indem sie Ketten von Filtern miteinander verbindet, sodass die Ausgabe eines Filters zur Eingabe für einen anderen wird. Eine Reihe verbundener Filter wird als *Filterdiagramm bezeichnet.* Das folgende Diagramm zeigt beispielsweise ein Filterdiagramm für die Wiedergabe einer AVI-Datei.

![Filterdiagramm zum Wiederspielen einer Avi-Datei](images/avi-filter-graph.png)

Der Filter Dateiquelle liest die AVI-Datei von der Festplatte. Der AVI-Splitterfilter analysiert die Datei in zwei Streams: einen komprimierten Videostream und einen Audiostream. Der AVI-Dekomprimierungsfilter decodiert die Videoframes. Der Videorenderer-Filter zeichnet die Frames mit DirectDraw oder GDI in die Anzeige. Der DirectSound-Standardgerätefilter gibt den Audiostream mitHilfe von DirectSound wieder.

Die Anwendung muss nicht den ganzen Datenfluss verwalten. Stattdessen werden die Filter von einer komponente auf hoher Ebene gesteuert, die als Filter-Graph wird. Die Anwendung ruft auf hoher Ebene API-Aufrufe wie "Ausführen" (zum Verschieben von Daten durch das Diagramm) oder "Beenden" (zum Beenden des Datenflusses) ab. Wenn Sie mehr Kontrolle über die Streamvorgänge benötigen, können Sie direkt über COM-Schnittstellen auf die Filter zugreifen. Der Filter Graph Manager übergibt auch Ereignisbenachrichtigungen an die Anwendung.

Der Filter Graph-Manager dient auch einem anderen Zweck: Er stellt Methoden für die Anwendung zum Erstellen des Filterdiagramms zur Verfügung, indem die Filter miteinander verbunden werden. (DirectShow bietet auch verschiedene Hilfsobjekte, die diesen Prozess vereinfachen. Diese werden in der Dokumentation ausführlich beschrieben.)

**Schreiben einer DirectShow-Anwendung**

Im Allgemeinen gibt es drei Aufgaben, die jede DirectShow-Anwendung ausführen muss. Diese sind im folgenden Diagramm dargestellt.

![Typische DirectShow-Anwendung](images/fgm.png)

1.  Die Anwendung erstellt eine Instanz des Filter-Graph-Managers.
2.  Die Anwendung verwendet den Filter Graph Manager, um ein Filterdiagramm zu erstellen. Der genaue Satz von Filtern im Diagramm hängt von der Anwendung ab.
3.  Die Anwendung verwendet den Filter Graph Manager, um das Filterdiagramm zu steuern und Daten über die Filter zu streamen. Während dieses Prozesses reagiert die Anwendung auch auf Ereignisse vom Filter-Graph Manager.

Wenn die Verarbeitung abgeschlossen ist, gibt die Anwendung den Filter Graph Manager und alle Filter frei.

DirectShow basiert auf COM. Der Filter Graph-Manager und die Filter sind alle COM-Objekte. Sie sollten über allgemeine Kenntnisse der COM-Clientprogrammierung verfügen, bevor Sie mit der Programmierung von DirectShow beginnen. Viele Bücher zur COM-Programmierung sind verfügbar.

Informationen zu den ersten Schritten mit DirectShow finden Sie im Artikel How To Play a File (How [To Play a File),](how-to-play-a-file.md)in dem eine einfache Konsolenanwendung zum Wiederspielen einer Videodatei präsentiert wird. Im Abschnitt [About DirectShow](about-directshow.md) wird die DirectShow-Architektur ausführlicher erläutert, während im Abschnitt Using DirectShow (Verwenden von [DirectShow)](using-directshow.md) die wichtigsten Szenarien untersucht werden, die von DirectShow unterstützt werden, z. B. Erfassung, Videobearbeitung, DVD-Wiedergabe und Fernsehsendung.

 

 



