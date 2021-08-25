---
title: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
description: So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab
ms.assetid: 1f6da1aa-c26a-486a-bb44-cc4305c71979
keywords:
- Advanced Systems Format (ASF), Abrufen komprimierter Beispiele
- ASF (Advanced Systems Format), Abrufen komprimierter Beispiele
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), komprimierte Beispiele
- ASF (Advanced Systems Format), komprimierte Beispiele
- Synchrone Reader,Abrufen komprimierter Beispiele
- Synchrone Reader,komprimierte Beispiele
- Komprimierte Beispiele,Abrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb2e3c7f1f6e00bd3f1c215a3b6783387fd3e19c268afe58862aa4b4d61889
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807460"
---
# <a name="to-retrieve-compressed-samples-with-the-synchronous-reader"></a>So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab

Wie der asynchrone Reader kann auch der synchrone Reader komprimierte Stichproben abrufen. Komprimierte Beispiele sollten beim Kopieren von Datenströmen aus einer Datei in eine andere verwendet werden.

Das Windows Media Format SDK stellt keine Methoden zum Decodieren von Daten bereit, nachdem sie aus einer ASF-Datei extrahiert wurden. Wenn Sie komprimierte Beispiele erhalten und diese später dekomprimieren möchten, müssen Sie dafür Ihren eigenen Code bereitstellen. Eine Möglichkeit, diese Einschränkung zu umgehen, besteht im Schreiben der komprimierten Beispiele in eine neue ASF-Datei und dem anschließenden erneuten Lesen in normale, unkomprimierte Beispiele.

Um komprimierte Beispiele mit dem synchronen Reader zu erhalten, rufen Sie VOR oder während der Wiedergabe [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) auf. Übergeben Sie true für *fCompressed*.

> [!Note]  
> Bildstreams sind für die Übermittlung komprimierter Datenströme ungültig. Wenn Sie einen Bilddatenstrom aus einer Datei in eine andere kopieren, funktioniert er in der neuen Datei nicht. Um einen Bilddatenstrom aus einer Datei in eine Datei zu kopieren, rufen Sie die Bilddatenstrombeispiele nach Ausgabenummer ab und fügen sie in die neue Datei ein, als würde ein neuer Bilddatenstrom enthalten sein.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




