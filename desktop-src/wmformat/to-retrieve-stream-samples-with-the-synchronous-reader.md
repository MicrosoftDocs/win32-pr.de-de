---
title: So rufen Sie streambeispiele mit dem synchronen Reader ab
description: So rufen Sie streambeispiele mit dem synchronen Reader ab
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- Advanced Systems Format (ASF), Abrufen von streambeispielen
- ASF (Advanced Systems Format), Abrufen von streambeispielen
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- synchrone Leser, Abrufen von streambeispielen
- Streams, Abrufen von Beispielen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101254"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a>So rufen Sie streambeispiele mit dem synchronen Reader ab

Wie der asynchrone Reader kann der synchrone Reader Beispiele nach streamnummer abrufen. Im Gegensatz zum asynchronen Reader kann der synchrone Reader sowohl komprimierte als auch unkomprimierte streambeispiele bereitzustellen.

Um streambeispiele zu erhalten, führen Sie die folgenden Schritte aus.

1.  Geben Sie in einem beliebigen Zeitraum vor oder während der Wiedergabe [**iwmsynkreader:: abtreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) an, und übergeben Sie die gewünschte streamnummer.
2.  Rufen Sie Beispiele mit fortgesetzten Aufrufen von [**iwmsynkreader:: getnextsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample)ab.

Sie können überprüfen, ob ein Datenstrom für die Beispiel Übermittlung ausgewählt ist, indem Sie [**iwmsyncreader:: getreadstreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples)aufrufen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von Dateien mit dem synchronen Reader**](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




