---
title: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
description: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), Abrufen von komprimierten Beispielen
- ASF (Advanced Systems Format), Abrufen von komprimierten Beispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- synchrone Leser, Abrufen komprimierter Beispiele
- synchrone Reader, komprimierte Beispiele
- komprimierte Beispiele, Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72f0051fc14a14500b2c6e69c5e32f7ec0c39a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101258"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab

Ebenso wie der asynchrone Reader kann der synchrone Reader auch komprimierte Beispiele abrufen. Komprimierte Beispiele sollten beim Kopieren von Streams aus einer Datei in eine andere verwendet werden.

Das Windows Media-Format-SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem es aus einer ASF-Datei extrahiert wurde. Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dazu ihren eigenen Code bereitstellen. Eine Möglichkeit, diese Einschränkung zu umgehen, besteht darin, die komprimierten Beispiele in eine neue ASF-Datei zu schreiben und Sie dann in normale, nicht komprimierte Beispiele zu lesen.

Um komprimierte Beispiele mit dem synchronen Reader zu erhalten, nennen Sie [**iwmsynkreader:: abtreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) vor oder während der Wiedergabe. Übergeben Sie "true" für die *Komprimierung*.

> [!Note]  
> Bildstreams sind für die komprimierte Datenstrom Übermittlung ungültig. Wenn Sie einen Bildstream aus einer Datei in einen anderen kopieren, funktioniert er nicht in der neuen Datei. Um einen Bildstream aus einer Datei in eine Datei zu kopieren, rufen Sie die Abbild Datenstrom Beispiele nach Ausgabe Nummer ab, und fügen Sie Sie in die neue Datei ein, als ob Sie einen neuen Bildstream einschließen

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




