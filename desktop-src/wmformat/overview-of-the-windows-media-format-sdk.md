---
title: Übersicht über das Windows Media-Format-SDK
description: Übersicht über das Windows Media-Format-SDK
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows Media-Format-SDK, Erstellung und Bearbeitung von ASF-Dateien
- Advanced Systems Format (ASF), Dateierstellung und-Bearbeitung
- ASF (Advanced Systems Format), Dateierstellung und-Bearbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4f58be5d377e44fc0f68c89ad580a554902c58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309411"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Übersicht über das Windows Media-Format-SDK

Das SDK für den Windows Media-Format enthält Objekte zum Ausführen von Aufgaben an drei Punkten während der Lebensdauer einer ASF-Datei: Erstellung, Bearbeitung und Wiedergabe. Bei einigen Anwendungen, insbesondere bei der Videobearbeitung, werden die allgemeinen Funktionen des Windows Media Format SDK verwendet, um den Inhalt von ASF-Dateien zu lesen, den Inhalt zu ändern und die Ergebnisse in eine neue Datei zu schreiben. Es ist jedoch am einfachsten, dieses SDK in den drei Phasen der Erstellung, Bearbeitung und Wiedergabe von Dateien zu betrachten.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>Erstellen von ASF-Dateien mit dem Windows Media-Format-SDK

Das Schreiben von ASF-Dateien mit dem Windows Media-Format SDK ist auf hoher Ebene recht einfach. Die Dateierstellung wird von einem Writer-Objekt verwaltet. Sie teilen dem Writer-Objekt mit, welche Art von Datei Sie erstellen möchten, indem Sie ein Profil Objekt für die Verwendung angeben. Jedes Profil Objekt enthält die Einstellungen für eine ASF-Datei. Einige Profile sind in diesem SDK enthalten, und die Unterstützung der Profilbearbeitung wird durch eine Reihe von Objekten bereitgestellt. Wenn Sie ein Profil für das zu verwendende Writer-Objekt festgelegt haben, können Sie damit beginnen, die Beispiele zur Verarbeitung an den Writer zu übergeben. In den meisten Fällen ist ein Beispiel ein Teil von Audiodaten oder Videos, die nicht komprimiert sind, aber ein Beispiel kann ein beliebiger Datentyp sein.

Intern führt der Writer drei Hauptaufgaben aus. Erstens: Wenn der Stream, zu dem ein Beispiel gehört, komprimiert werden soll, kommuniziert der Writer mit dem Codierungs Teil des Codecs (Kompressor/Dekompressor), um das Beispiel zu komprimieren. Sobald die Beispiele in der vom Profil angegebenen Form vorliegen, unterbricht der Writer die Beispiele in Pakete mit entsprechender Größe, die über ein Netzwerk gestreamt werden. Schließlich werden die Daten aus den verschiedenen Streams multiplext oder verschachtelt, sodass sich Beispiele mit ähnlichen Präsentations Zeiten über alle Streams hinweg im Daten Abschnitt der ASF-Datei befinden.

Das Writer-Objekt schreibt tatsächlich keine Datei selbst. Er kommuniziert mit einem oder mehreren Objekten namens senken, die die Daten vom Writer an das Ziel übermitteln. Bei lokalen Dateien verwaltet eine dateisenke das Schreiben der Daten in die Datei. Sie können Netzwerk senken auch so konfigurieren, dass die ASF-Daten über ein Netzwerk übertragen werden. Häufig wird mehr als eine Senke verwendet. Beispielsweise kann eine Anwendung eine Datei über ein Netzwerk streamen und eine Kopie als Datei auf einem lokalen Datenträger gleichzeitig speichern. Mithilfe einer Push-Senke können Sie Inhalte von der Schreib Anwendung an einen oder mehrere Server übertragen, auf denen Windows Media Services ausgeführt wird, die die Inhalte dann an Benutzer verteilen.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>ASF-Dateibearbeitung mit dem Windows Media-Format-SDK (Metadatenbearbeitung)

Wenn Sie den Inhalt des Daten Abschnitts einer ASF-Datei bearbeiten, muss die Datei neu geschrieben werden. Das Windows Media-Format-SDK stellt keine Objekte bereit, die den Daten Abschnitt direkt bearbeiten. Für einfache bearbeitvorgänge, z. b. das Verketten von zwei Dateien oder das Ausschnitten von Inhalten aus einer Datei, können Sie Beispiele lesen, ohne Sie zu dekomprimieren, und Sie dann in eine neue Datei mit denselben Header Informationen schreiben. Kompliziertere Bearbeitungen umfassen das vornehmen von Änderungen am Profil, das für die neue Datei verwendet wird.

Das Windows Media-Format-SDK unterstützt das Bearbeiten von Teilen des Header Abschnitts, ohne die Datei neu zu schreiben. Der Header einer ASF-Datei enthält viele verschiedene Arten von Daten. Die am häufigsten bearbeiteten Elemente sind Metadatenattribute, bei denen es sich um Name-Wert-Paare handelt, die Aspekte des Inhalts und die damit verbundenen Personen beschreiben. Sie können Metadaten mithilfe des Metadaten-Editor-Objekts des Windows Media SDK-Objekts bearbeiten. Dieses Objekt öffnet eine ASF-Datei, sodass Sie einige Inhalte der Kopfzeile ändern, die Änderungen in die Datei schreiben und die Datei schließen können. Die Metadatenbearbeitung ist sehr unkompliziert, mit einfachen Methoden aufrufen zum Abrufen und Festlegen von Werten.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Einlesen von ASF-Dateien mit dem Windows Media-Format-SDK

Das Windows Media-Format SDK bietet zwei unterschiedliche Objekte zum Lesen von ASF-Dateien: das Reader-Objekt und das synchrone Reader-Objekt. Das Reader-Objekt ist in allen Versionen des SDK verfügbar, während das synchrone Reader-Objekt das Windows Media-SDK der Serie 9 oder eine höhere Version benötigt. Der Hauptunterschied zwischen den beiden besteht darin, dass das Reader-Objekt der Anwendung Beispiele zur Verfügung stellt, indem Ereignisse für eine Rückruf Methode ausgelöst werden, während der synchrone Reader einzelne Beispiele als Reaktion auf Methodenaufrufe bereitstellt.

Um das Reader-Objekt verwenden zu können, müssen Sie mehrere Rückruf Methoden implementieren, um auf Status-und Beispiel Meldungen des Reader-Objekts zu reagieren. Sie konfigurieren den Reader so, dass der Inhalt wie gewünscht bereitstellt wird, starten Sie den Reader, und warten Sie auf die Beispiel Nachrichten. Der Prozess des Abrufens von Beispielen aus einer ASF-Datei ist im Grunde das Gegenteil des Schreibvorgangs. Das Reader-Objekt kommuniziert mit den Codecs, die zum Decodieren sämtlicher komprimierter Streams erforderlich sind, und liefert nicht komprimierte Daten an die Anwendung. Sie können das Reader-Objekt auch so konfigurieren, dass es Stichproben im komprimierten Zustand bereitstellt, damit Sie einen zuvor codierten Stream in eine neue Datei einfügen können.

Das synchrone Reader-Objekt funktioniert auf die gleiche Weise wie das Reader-Objekt. Anstatt Rückrufe zu konfigurieren, müssen Sie jedoch jede Stichprobe vom synchronen Reader einzeln anfordern. Die Verwendung des synchronen Readers erfordert nur einen einzigen Thread, während für die Verwendung des Readers mehrere Threads benötigt werden. Das synchrone Reader-Objekt hat unter bestimmten Umständen mehrere Vorteile gegenüber dem Reader-Objekt, hauptsächlich für Anwendungen zur Inhalts Bearbeitung, die schnell auf verschiedene Teile einer Datei zugreifen und Daten zwischen Dateien kopieren müssen. Das synchrone Reader-Objekt ist viel einfacher zu verwenden und macht das Suchen nach bestimmten Stellen im Daten Abschnitt leicht. Der synchrone Reader unterstützt jedoch nicht das Lesen von Dateien über ein Netzwerk und unterstützt Digital Rights Management nicht.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Weitere Vorgänge mit dem Windows Media-Format-SDK

Zusätzlich zu den drei wesentlichen Funktionsbereichen, die soeben beschrieben werden, verfügt das Windows Media Format SDK über Objekte zum Ausführen anderer Vorgänge im Zusammenhang mit den ASF-Dateien. Das Profil-Manager-Objekt wird verwendet, um Profile zu erstellen und darauf zuzugreifen und Sie zu speichern. Das Indexer-Objekt erstellt Index Objekte in ASF-Dateien, die das Suchen in Videodateien ermöglichen. Schließlich unterstützen das Reader-Objekt und das Writer-Objekt Digital Rights Management, um die geistigen Rechte der Inhalts Ersteller zu schützen.

**Hinweis** Der Zweck der ASF-Dateistruktur und dieses SDK im Allgemeinen ist die Erstellung digitaler Mediendateien, die Audiodaten und Videos enthalten, und diese Dokumentation wird in diesem Sinne geschrieben. Die Struktur der ASF-Datei kann jedoch auch für andere Inhaltstypen verwendet werden. Möglicherweise finden Sie viele Anwendungen für ASF-Dateien, die sich nicht auf Audiodaten und Videos beziehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media-Format-SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




