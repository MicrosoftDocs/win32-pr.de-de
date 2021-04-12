---
title: So schreiben Sie Beispiele
description: So schreiben Sie Beispiele
ms.assetid: 9ce10a77-9e80-45e0-a7e7-2ffdf8b57773
keywords:
- Advanced Systems Format (ASF), Schreiben von Beispielen
- ASF (Advanced Systems Format), Schreiben von Beispielen
- Advanced Systems Format (ASF), übergeben von Beispielen an den Writer
- ASF (Advanced Systems Format), übergeben von Beispielen an den Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 738014b3c42441e878105d12a8ebf23ce4b266f7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389862"
---
# <a name="to-write-samples"></a>So schreiben Sie Beispiele

Wenn Sie die Eingaben für die Datei, die Sie schreiben, identifiziert und konfiguriert haben, können Sie mit dem übergeben von Beispielen an den Writer beginnen. Sie sollten Beispiele in der Präsentationszeit Reihenfolge übergeben, um den Schreibvorgang effizienter zu gestalten.

Vor dem übergeben von Beispielen müssen Sie den Writer festlegen, um Sie durch Aufrufen von [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting)zu akzeptieren.

Führen Sie die folgenden Schritte aus, um ein Beispiel an den Writer zu übergeben:

1.  Zuordnen eines Puffers und Abrufen eines Zeigers auf die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle durch Aufrufen von [**iwmwriter:: allopriesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-allocatesample).
2.  Rufen Sie die Adresse des Puffers ab, der in Schritt 1 erstellt wurde, indem Sie [**inssbuffer:: GetBuffer**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbuffer)aufrufen.
3.  Kopieren Sie die Beispiel Daten in den Puffer Speicherort, und stellen Sie sicher, dass das Beispiel erfolgreich in den zugeordneten Puffer passt. Sie können eine beliebige Speicher Kopierfunktion verwenden, um die Daten zu kopieren. Eine gängige Wahl ist "memcpy", die in der Standard-C-Lauf Zeit Bibliothek enthalten ist.
4.  Aktualisieren Sie die im Puffer verwendete Datenmenge, um die tatsächliche Größe des Beispiels durch Aufrufen von " [**inssbuffer:: SetLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-setlength)" widerzuspiegeln.
5.  Übergeben Sie die Puffer Schnittstelle zusammen mit der Eingabe Nummer und der Stichproben Zeit mithilfe der [**iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) -Methode an den Writer. Alle Audiobeispiele für eine Eingabe repräsentieren dieselbe Dauer von Inhalten, sodass Sie die Stichproben Zeit ermitteln können, indem Sie die Stichproben Dauer einem laufenden Gesamtwert hinzufügen. Für ein Video müssen Sie die Uhrzeit basierend auf der Framerate berechnen.

**Writesample** arbeitet asynchron und beendet das Schreiben der Daten aus dem Puffer möglicherweise nicht, bevor die Anwendung bereit ist, die Methode erneut aufzurufen. Daher ist es wichtig, dass Sie  für jeden Aufrufe von " **Write**" "" "" "" "" "" "" "" Allerdings können Sie die **inssbuffer** -Schnittstelle sofort nach dem Aufruf von " **Write-ample**" freigeben.

Wenn Sie die Übergabe von Beispielen abgeschlossen haben, nennen Sie [**iwmwriter:: EndWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting).

**Hinweis** Es ist wichtig, dass die Beispiele aus allen Streams in der Datei in der Synchronisierung miteinander an den Writer übermittelt werden. Das heißt, wann immer es möglich ist, sollten Sie in der Präsentationszeit in der angegebenen Synchronisierungs Toleranz in [**iwmschreiteradvanced:: setsynctolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance)Beispiele an den Writer übergeben. Optimale Ergebnisse werden erzielt, wenn Daten an jeden Stream in Einheiten von mindestens einer Sekunde zugestellt werden.

Streams sollten auch ungefähr zur gleichen Zeit enden. Sie sollten z. b. keine Datei mit einem Audiostream mit einer Länge von 45 Sekunden schreiben und einen Videostream mit einer Länge von 50 Sekunden. Wenn Sie eine solche Datei mit unveränderten Eingaben codieren, werden einige der Audiodaten am Ende des Streams gelöscht (auch wenn es sich um den kürzeren Datenstrom handelt). Damit die Datei Codierung funktioniert, sollten Sie der Audioeingabe 5 Sekunden Ruhe Wert hinzufügen, damit ein Stream nicht mehrere Sekunden vor einem anderen Datenstrom endet. Es ist nicht erforderlich, dass Streamtypen mit zeitweiligen Stichproben wie Text-oder bildstreams auf diese Weise aufgefüllt werden. Skript befehlsstreams sollten auch all diese Regeln einhalten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Inssbuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer)
</dt> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




