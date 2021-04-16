---
description: Einführung in die DirectShow-Anwendungsprogrammierung
ms.assetid: 21a72efa-95df-4754-8304-ad56965a914d
title: Einführung in die DirectShow-Anwendungsprogrammierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6218a346a7eb9711259c025aef09133ef2e58f6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392557"
---
# <a name="introduction-to-directshow-application-programming"></a>Einführung in die DirectShow-Anwendungsprogrammierung

In diesem Artikel werden die grundlegenden Begriffe und Konzepte erläutert, die in DirectShow verwendet werden. Nach dem Lesen dieses Abschnitts können Sie Ihre erste DirectShow-Anwendung schreiben.

**Filter und Filtern von Diagrammen**

Der Baustein von DirectShow ist eine Softwarekomponente, die als *Filter* bezeichnet wird. Ein Filter ist eine Softwarekomponente, die einen Vorgang für einen Multimedia-Stream ausführt. DirectShow-Filter können z. b.

-   Dateien lesen
-   Video von einem Video Erfassungsgerät erhalten
-   Decodieren verschiedener Streamformate, z. b. MPEG-1-Video
-   übergeben von Daten an die Grafik oder Soundkarte

Filter empfangen Eingaben und liefern Ausgaben. Wenn z. b. ein Filter das MPEG-1-Video decodiert, ist die Eingabe der MPEG-codierte Stream, und die Ausgabe ist eine Reihe von nicht komprimierten Video Frames.

In DirectShow führt eine Anwendung eine beliebige Aufgabe aus, indem Ketten von Filtern miteinander verbunden werden, sodass die Ausgabe eines Filters zur Eingabe für eine andere wird. Ein Satz verbundener Filter wird als *Filter Diagramm* bezeichnet. Das folgende Diagramm zeigt z. b. ein Filter Diagramm für die Wiedergabe einer AVI-Datei.

![Filter Diagramm zum Abspielen einer AVI-Datei](images/avi-filter-graph.png)

Der Datei Quell Filter liest die AVI-Datei von der Festplatte. Der avi-Splitter Filter analysiert die Datei in zwei Streams, einen komprimierten Videostream und einen Audiodatenstrom. Der AVI-Debug-Filter decodiert die Video Frames. Der Videorenderer-Filter zeichnet die Frames mithilfe von DirectDraw oder GDI in die Anzeige. Der standardmäßige DirectSound-Geräte Filter gibt den Audiostream mithilfe von DirectSound wieder.

Der gesamte Datenfluss muss von der Anwendung nicht verwaltet werden. Stattdessen werden die Filter durch eine Komponente auf hoher Ebene gesteuert, die als Filter Graph-Manager bezeichnet wird. Die Anwendung führt API-Aufrufe auf hoher Ebene aus, z. b. "ausführen" (um Daten durch das Diagramm zu verschieben) oder "anzuhalten" (um den Datenfluss zu verhindern). Wenn Sie mehr Kontrolle über die streamvorgänge benötigen, können Sie direkt über COM-Schnittstellen auf die Filter zugreifen. Der Filter Graph-Manager übergibt auch Ereignis Benachrichtigungen an die Anwendung.

Der Filter Graph-Manager dient ebenfalls einem anderen Zweck: Er stellt Methoden bereit, mit denen die Anwendung das Filter Diagramm erstellen kann, indem die Filter miteinander verbunden werden. (DirectShow bietet auch verschiedene Hilfsobjekte, die diesen Prozess vereinfachen. Diese werden in der-Dokumentation ausführlich beschrieben.)

**Schreiben einer DirectShow-Anwendung**

Im Allgemeinen gibt es drei Aufgaben, die jede DirectShow-Anwendung ausführen muss. Diese werden in der folgenden Abbildung veranschaulicht.

![Typische DirectShow-Anwendung](images/fgm.png)

1.  Die Anwendung erstellt eine Instanz des Filter Graph-Managers.
2.  Die Anwendung verwendet den Filter Graph-Manager, um ein Filter Diagramm zu erstellen. Der genaue Satz von Filtern im Diagramm hängt von der Anwendung ab.
3.  Die Anwendung verwendet den Filter Graph-Manager, um das Filter Diagramm zu steuern und Daten über die Filter zu streamen. Während dieses Vorgangs antwortet die Anwendung auch auf Ereignisse vom Filter Graph-Manager.

Wenn die Verarbeitung abgeschlossen ist, gibt die Anwendung den Filter Graph-Manager und alle Filter frei.

DirectShow basiert auf com; der Filter Graph-Manager und die Filter sind alle COM-Objekte. Sie sollten ein allgemeines Verständnis der com-Client Programmierung haben, bevor Sie mit dem Programmieren von DirectShow beginnen. Viele Bücher zur COM-Programmierung sind verfügbar.

Informationen zu den ersten Schritten mit DirectShow finden Sie im Artikel wiedergeben [einer Datei](how-to-play-a-file.md), die eine einfache Konsolenanwendung zum Abspielen einer Videodatei darstellt. Im Abschnitt [zu DirectShow](about-directshow.md) wird die DirectShow-Architektur ausführlicher erläutert, während der Abschnitt [using DirectShow](using-directshow.md) die wichtigsten Szenarien untersucht, die von DirectShow unterstützt werden, z. b. Erfassung, Videobearbeitung, DVD-Wiedergabe und Fernsehen.

 

 



