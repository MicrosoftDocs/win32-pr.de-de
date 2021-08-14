---
title: Übersicht über das Windows Media Format SDK
description: Übersicht über das Windows Media Format SDK
ms.assetid: 9e5d6254-6261-4ca8-84d6-38050c93db22
keywords:
- Windows Medienformat-SDK, Erstellen und Bearbeiten von ASF-Dateien
- Advanced Systems Format (ASF), Dateierstellung und -bearbeitung
- ASF (Advanced Systems Format), Dateierstellung und -bearbeitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b80436415a6017d0429493b1d4b5be92dcb682f572796e5e9e1c3cfaa8795e66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846426"
---
# <a name="overview-of-the-windows-media-format-sdk"></a>Übersicht über das Windows Media Format SDK

Das Windows Media Format SDK enthält Objekte zum Ausführen von Aufgaben an drei Stellen in der Lebensdauer einer ASF-Datei: Erstellung, Bearbeitung und Wiedergabe. Einige Anwendungen, insbesondere anwendungen für die Videobearbeitung, verwenden die umfassende Funktionalität des Windows Media Format SDK, um den Inhalt von ASF-Dateien zu lesen, diesen Inhalt zu ändern und die Ergebnisse in eine neue Datei zu schreiben. Es ist jedoch am einfachsten, sich dieses SDK in den drei Phasen der Dateierstellung, -bearbeitung und -wiedergabe zu vorstellen.

## <a name="asf-file-creation-with-the-windows-media-format-sdk"></a>ASF-Dateierstellung mit dem Windows Media Format SDK

Das Schreiben von ASF-Dateien mit dem Windows Media Format SDK ist auf hoher Ebene recht einfach. Die Dateierstellung wird von einem Writer-Objekt verwaltet. Sie teilen dem Writer-Objekt mit, welche Art von Datei Sie erstellen möchten, indem Sie ein Profilobjekt für die Verwendung angeben. Jedes Profilobjekt enthält die Einstellungen für eine ASF-Datei. Einige Profile sind in diesem SDK enthalten, und die Unterstützung für die Profilbearbeitung wird von einer Reihe von -Objekten bereitgestellt. Wenn Sie ein Profil für das zu verwendende Writer-Objekt festgelegt haben, können Sie mit der Übergabe von Beispielen zur Verarbeitung an den Writer beginnen. In den meisten Fällen ist ein Beispiel ein Audio- oder Videoteil, das nicht komprimiert ist, aber ein Beispiel kann eine beliebige Art von Daten sein.

Intern führt der Writer drei Hauptaufgaben aus. Erstens: Wenn der Stream, zu dem ein Beispiel gehört, komprimiert werden soll, kommuniziert der Writer mit dem Codierungsteil des Codecs (Entsprechung/Dekomprimierung), um das Beispiel zu komprimieren. Sobald die Beispiele in der vom Profil angegebenen Form vorliegen, unterteilt der Writer die Stichproben in Pakete mit entsprechender Größe, die über ein Netzwerk gestreamt werden sollen. Schließlich werden die Daten aus den verschiedenen Streams multiplexiert oder verschachtelt, sodass Stichproben mit ähnlichen Präsentationszeiten in allen Streams im Datenabschnitt der ASF-Datei nah beieinander liegen.

Das Writer-Objekt schreibt keine Datei selbst. Es kommuniziert mit einem oder mehreren Objekten, die als Senken bezeichnet werden und die Daten vom Writer an das Ziel übermitteln. Bei lokalen Dateien verwaltet eine Dateisenke das Schreiben der Daten in die Datei. Sie können auch Netzwerksenken konfigurieren, um die ASF-Daten über ein Netzwerk zu übermitteln. In der Regel werden mehr als eine Senke verwendet. Beispielsweise kann eine Anwendung eine Datei über ein Netzwerk streamen und eine Kopie gleichzeitig als Datei auf einem lokalen Datenträger speichern. Mithilfe einer Pushsenke können Sie Inhalte aus Ihrer Schreibanwendung an einen oder mehrere Server übertragen, auf denen Windows Media-Dienste ausgeführt wird. Dadurch werden die Inhalte dann an Benutzer verteilt.

## <a name="asf-file-editing-with-the-windows-media-format-sdk-metadata-editing"></a>ASF-Dateibearbeitung mit dem Windows Media Format SDK (Metadatenbearbeitung)

Zum Bearbeiten des Inhalts des Datenabschnitts einer ASF-Datei muss die Datei neu geschrieben werden. Das Windows Media Format SDK stellt keine Objekte bereit, die den Datenabschnitt an Ort und Stelle bearbeiten. Für einfache Bearbeitungen, z. B. das Verketten von zwei Dateien oder das Ausschneiden von Inhalten aus einer Datei, können Sie Beispiele lesen, ohne sie zu dekomprimieren, und sie dann mit den gleichen Headerinformationen in eine neue Datei schreiben. Kompliziertere Änderungen umfassen das Vornehmen von Änderungen am Profil, das für die neue Datei verwendet wird.

Das Windows Media Format SDK unterstützt die Bearbeitung von Teilen des Headerabschnitts, ohne die Datei neu zu schreiben. Der Header einer ASF-Datei enthält viele verschiedene Datentypen. Die am häufigsten bearbeiteten Metadatenattribute sind Name-Wert-Paare, die Aspekte des Inhalts und die Personen beschreiben, die an der Erstellung beteiligt sind. Sie können Metadaten mit dem Metadaten-Editor-Objekt des Windows Media Format SDK bearbeiten. Dieses Objekt öffnet eine ASF-Datei, ermöglicht es Ihnen, einen Teil des Inhalts des Headers zu ändern, die Änderungen in die Datei zu schreiben und die Datei zu schließen. Die Bearbeitung von Metadaten ist sehr einfach, mit einfachen Methodenaufrufen zum Abrufen und Festlegen von Werten.

## <a name="asf-file-reading-with-the-windows-media-format-sdk"></a>Lesen von ASF-Dateien mit dem Windows Media Format SDK

Das Windows Media Format SDK stellt zwei unterschiedliche Objekte zum Lesen von ASF-Dateien bereit: das Readerobjekt und das synchrone Readerobjekt. Das Readerobjekt ist in allen Versionen des SDK verfügbar, während das synchrone Readerobjekt das Windows Media Format 9 Series SDK oder eine höhere Version erfordert. Der Hauptunterschied zwischen den beiden besteht darin, dass das Readerobjekt Stichproben an Ihre Anwendung übermittelt, indem Ereignisse an eine Rückrufmethode ausgelöst werden, während der synchrone Reader als Reaktion auf Methodenaufrufe einzelne Stichproben bereitstellt.

Um das Readerobjekt zu verwenden, müssen Sie mehrere Rückrufmethoden implementieren, um auf Status- und Beispielmeldungen aus dem Readerobjekt zu reagieren. Sie konfigurieren den Reader so, dass er den Inhalt nach Belieben übermittelt, den Reader startet und auf die Beispielmeldungen wartet. Der Prozess des Abrufens von Beispielen aus einer ASF-Datei ist im Grunde das Gegenteil des Schreibvorgangs. Das Readerobjekt kommuniziert mit den Codecs, die zum Decodieren komprimierter Datenströme erforderlich sind, und übermittelt unkomprimierte Daten an Ihre Anwendung. Sie können das Readerobjekt auch so konfigurieren, dass es Stichproben im komprimierten Zustand übermittelt, sodass Sie einen zuvor codierten Stream in eine neue Datei einschließen können.

Das synchrone Readerobjekt funktioniert in etwa auf die gleiche Weise wie das Readerobjekt. Anstatt Rückrufe zu konfigurieren, müssen Sie jedoch jedes Beispiel vom synchronen Reader einzeln anfordern. Die Verwendung des synchronen Readers erfordert nur einen einzelnen Thread, während die Verwendung des Readers mehrere Threads erfordert. Das synchrone Readerobjekt hat unter bestimmten Umständen mehrere Vorteile gegenüber dem Readerobjekt, hauptsächlich für Inhaltsbearbeitungsanwendungen, die schnell auf verschiedene Teile einer Datei zugreifen und Daten zwischen Dateien kopieren müssen. Das synchrone Readerobjekt ist viel einfacher zu verwenden und erleichtert die Suche nach bestimmten Stellen im Datenabschnitt. Der synchrone Reader unterstützt jedoch nicht das Lesen von Dateien über ein Netzwerk und keine Verwaltung digitaler Rechte.

## <a name="other-operations-with-the-windows-media-format-sdk"></a>Andere Vorgänge mit dem Windows Media Format SDK

Zusätzlich zu den drei soeben beschriebenen Hauptfunktionsbereichen verfügt das Windows Media Format SDK über Objekte, mit denen andere Vorgänge im Zusammenhang mit ASF-Dateien ausgeführt werden können. Das Profil-Manager-Objekt wird verwendet, um Profile zu erstellen und darauf zuzugreifen und sie zu speichern. Das Indexerobjekt erstellt Indexobjekte in ASF-Dateien, die das Suchen in Videodateien ermöglichen. Schließlich unterstützen das Readerobjekt und das Writer-Objekt die Verwaltung digitaler Rechte, um die geistigen Rechte von Inhaltserstellern zu schützen.

**Hinweis** Die Absicht der ASF-Dateistruktur und dieses SDK im Allgemeinen besteht darin, digitale Mediendateien mit Audio und Video zu erstellen. Diese Dokumentation wird zu diesem Zweck geschrieben. Die ASF-Dateistruktur funktioniert jedoch auch für andere Inhaltstypen. Möglicherweise finden Sie viele Anwendungen für ASF-Dateien, die sich nicht auf Audio und Video beziehen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Windows Media Format SDK**](about-the-windows-media-format-sdk.md)
</dt> </dl>

 

 




