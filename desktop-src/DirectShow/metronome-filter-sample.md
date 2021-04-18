---
description: Metronome-Filter Beispiel
ms.assetid: bb279898-875a-4ce4-ac69-6c58f640fbbd
title: Metronome-Filter Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 361b46aafa84590243cfcc05445d91a56ce56e83
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343940"
---
# <a name="metronome-filter-sample"></a>Metronome-Filter Beispiel

## <a name="description"></a>BESCHREIBUNG

Dieser Beispiel Filter zeigt, wie eine verweisuhr implementiert wird. Der Filter verwendet die standardmäßige Mikrofon Eingabe, um Audiospitzen (z. b. Klicks, Hand-claps oder coughs) zu lauschen, die zur Bestimmung der Taktfrequenz verwendet werden.

## <a name="usage"></a>Verbrauch

Erstellen Sie das Beispiel Projekt, und kopieren Sie die Filter-DLL (Metronom.ax) in Ihr Windows-System Verzeichnis. Führen Sie die Datei Metronom. reg aus, um die dll zu registrieren.

So verwenden Sie den Filter:

1.  Erstellen eines Filter Diagramms in GraphEdit, das einen Videostream rendert.
2.  Löscht alle gerenderten Audiodatenströme.
3.  Fügen Sie dem Diagramm den Metronome-Filter hinzu. Sie wird in der Kategorie DirectShow-Filter angezeigt.
4.  Führen Sie das Diagramm aus. Das Video beginnt mit normaler Geschwindigkeit.
5.  Legen Sie Ihre Hände, oder verwenden Sie ein Metronome, um eine neue Geschwindigkeit festzulegen.

## <a name="programming-notes"></a>Programmier Hinweise

Dieser Filter funktioniert nur für Videos. Der audiorenderer ist nicht in der Lage, eine Synchronisierung mit einer sehr unterschiedlichen Takt Rate durchzusetzen.

Wenn Sie 92-mal pro Minute (einmal alle ~ 652 MS) angleichen, wird das Video mit dem normalen Satz abgespielt. Sie können diese Standardeinstellung ändern, indem Sie den Wert der Konstante `BPM` in Metronom. cpp ändern.

Wenn Sie das applaudieren für einen bestimmten Zeitraum abbrechen und dann erneut mit dem applaudieren beginnen, müssen Sie mit ungefähr derselben Geschwindigkeit erneut starten, oder der Filter ignoriert es. Außerdem wird die Geschwindigkeit der Videowiedergabe durch die CPU-Geschwindigkeit eingeschränkt. Wenn Sie den Grenzwert für eine beliebige Zeitspanne überschreiten, reagiert der Filter nicht mehr auf Raten Änderungen. Wenn dies der Fall ist, wird das Diagramm angehalten und neu gestartet.

Wenn Sie Ihre eigene Uhr implementieren, sind die wichtigsten Regeln, dass die Referenzuhren nicht rückwärts gehen dürfen. Das heißt, Sie müssen niemals einen Zeitwert melden, der kleiner als der vorherige Zeitwert ist.

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Zum Herunterladen der DirectShow SDK-Beispiele installieren Sie die neueste Version der [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Dieses Beispiel wird unter folgendem Pfad installiert: *\[ SDK Root \]* \\ Samples \\ Multimedia \\ DirectShow \\ Filters \\ Metronome.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> <dt>

[DirectShow-Beispiele](directshow-samples.md)
</dt> </dl>

 

 



