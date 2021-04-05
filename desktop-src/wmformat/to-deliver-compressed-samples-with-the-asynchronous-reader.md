---
title: So liefern Sie komprimierte Beispiele mit dem asynchronen Reader
description: So liefern Sie komprimierte Beispiele mit dem asynchronen Reader
ms.assetid: 488baa3c-8863-4afc-89b2-fe55823e5db9
keywords:
- Advanced Systems Format (ASF), Bereitstellung von komprimierten Beispielen
- ASF (Advanced Systems Format), Bereitstellung von komprimierten Beispielen
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- asynchrone Leser, Bereitstellung von komprimierten Beispielen
- asynchrone Leser, komprimierte Beispiele
- komprimierte Beispiele, Bereitstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4ce835075f5bd760014a3b1b776ba3627adb076
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723536"
---
# <a name="to-deliver-compressed-samples-with-the-asynchronous-reader"></a>So liefern Sie komprimierte Beispiele mit dem asynchronen Reader

Der asynchrone Reader kann komprimierte Beispiele aus Streams in ASF-Dateien bereitzustellen. Anwendungen stellen in der Regel komprimierte Beispiele bereit, wenn Sie einen Stream aus einer Datei in eine andere kopieren. Es ist nicht empfehlenswert, Daten, die aus einem komprimierten Stream rekonstruiert wurden, erneut zu komprimieren, da die Daten beim Codierungs Vorgang verloren gehen. Digitale Medien, die mehr als einmal komprimiert werden, haben eine spürbare Abnahme der Qualität.

Das Windows Media-Format-SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem es aus einer ASF-Datei extrahiert wurde. Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dazu ihren eigenen Code bereitstellen. Eine Möglichkeit, diese Einschränkung zu umgehen, besteht darin, die komprimierten Beispiele in eine neue ASF-Datei zu schreiben und Sie dann in normale, nicht komprimierte Beispiele zu lesen.

Um komprimierte Beispiele mit dem asynchronen Reader zu erhalten, führen Sie die folgenden Schritte aus.

1.  Implementieren Sie den " [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) "-Rückruf. Dieser Rückruf ist im Grunde identisch mit [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , mit dem Unterschied, dass er Beispiele nach streamnummer liefert und die Beispiele weiterhin komprimiert sind.
2.  Rufen Sie vor dem Starten der Wiedergabe einen Zeiger auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts ab, indem Sie **iwmreader:: QueryInterface** aufrufen.
3.  Konfigurieren Sie den Reader so, dass komprimierte Beispiele für den gewünschten Stream durch Aufrufen von [**iwmreaderadvanced:: setreceivestreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples)bereitgestellt werden.
4.  Wiederholen Sie Schritt 3 für jeden Stream, für den eine komprimierte Beispiel Übermittlung gewünscht ist.

> [!Note]  
> Bildstreams sind für die komprimierte Datenstrom Übermittlung ungültig. Wenn Sie einen Bildstream aus einer Datei in einen anderen kopieren, funktioniert er nicht in der neuen Datei. Um einen Bildstream aus einer Datei in eine Datei zu kopieren, rufen Sie die Abbild Datenstrom Beispiele nach Ausgabe Nummer ab, und fügen Sie Sie in die neue Datei ein, als ob Sie einen neuen Bildstream einschließen

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreadercallbackadvanced-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[**Lesen von Dateien mit dem asynchronen Reader**](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




