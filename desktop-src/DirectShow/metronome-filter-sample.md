---
description: Beispiel für Metronomfilter
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Beispiel für Metronomfilter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ea1b321dd2602829697862e2716c9017573a44b6162b355e78e586e14d85003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072984"
---
# <a name="metronome-filter-sample"></a>Beispiel für Metronomfilter

## <a name="description"></a>Beschreibung

Dieser Beispielfilter zeigt, wie eine Verweisuhr implementiert wird. Der Filter verwendet Ihre Standardmikrofoneingabe, um auf Audiospitzen (z. B. Klicks, Handklicks oder Klammern) zu lauschen, die er verwendet, um eine Taktrate zu bestimmen.

## <a name="usage"></a>Verwendung

Erstellen Sie das Beispielprojekt, und kopieren Sie die Filter-DLL (Metronom.ax) Windows Systemverzeichnis. Führen Sie die Datei Metronom.reg aus, um die DLL zu registrieren.

So verwenden Sie den Filter:

1.  Erstellen Sie ein Filterdiagramm in GraphEdit, das einen Videostream rendert.
2.  Löscht alle gerenderten Audiostreams.
3.  Fügen Sie dem Diagramm den Filter Metronome hinzu. Sie wird in der Kategorie DirectShow-Filter angezeigt.
4.  Führen Sie das Diagramm aus. Das Video wird mit normaler Geschwindigkeit abspielt.
5.  Klammern Sie ihre Hände, oder verwenden Sie ein Metronom, um eine neue Geschwindigkeit zu setzen.

## <a name="programming-notes"></a>Programmierhinweise

Dieser Filter funktioniert nur für Videos. Der Audiorenderer kann nicht mit unterschiedlichen Taktraten synchronisiert werden.

Wenn Sie 92-mal pro Minute (einmal alle ca. 652 ms) lauten, wird das Video mit der normalen Rate abspielt. Sie können diese Standardeinstellung ändern, indem Sie den Wert der Konstante `BPM` in Metronom.cpp ändern.

Wenn Sie die Klammer für einen bestimmten Zeitraum beenden und dann erneut mit dem Clapping beginnen, müssen Sie mit ungefähr der gleichen Geschwindigkeit erneut beginnen, da der Filter dies ignoriert. Außerdem wird die Videowiedergaberate durch die CPU-Geschwindigkeit beschränkt. Wenn Sie den Grenzwert für einen beliebigen Zeitraum überschreiten, reagiert der Filter nicht mehr auf Änderungen der Rate. Beenden Sie in diesem Fall den Graphen, und starten Sie ihn neu.

Wenn Sie Ihre eigene Uhr implementieren, ist die wichtigste Regel, dass Verweisuhren nicht rückwärts gehen dürfen. Das heißt, sie dürfen niemals einen Zeitwert melden, der kleiner als der vorherige Zeitwert ist.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Um die DirectShow SDK-Beispiele herunterzuladen, installieren Sie die neueste Version des [Windows SDK.](https://msdn.microsoft.com/windowsvista/bb980924.aspx)

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK \] Root* Samples Multimedia \\ \\ \\ DirectShow Filters \\ \\ Metronome.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



