---
title: Rendern von Inhalt
description: Rendern von Inhalt
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Medienformat-SDK, Rendern von Inhalt
- Advanced Systems Format (ASF), Rendern von Inhalten
- ASF (Advanced Systems Format), Rendern von Inhalt
- Advanced Systems Format (ASF), Inhaltsrendering
- ASF (Advanced Systems Format), Inhaltsrendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7add8d31f1fd025327325256e56c9f38faa4c97fd7e2aa206cedfebcc84c1302
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929657"
---
# <a name="rendering-content"></a>Rendern von Inhalt

Das Windows Media Format SDK stellt keine Routinen zum Rendern von Inhalten bereit, die vom Readerobjekt bereitgestellt werden. Wenn Sie Anwendungen schreiben, um den Inhalt in ASF-Dateien wieder zu übernehmen, müssen Sie Ihre eigenen Renderingroutinen implementieren.

Beim Rendern von Inhalten müssen Sie vorsichtig sein, um sicherzustellen, dass Beispiele in der Reihenfolge der Präsentationszeit gerendert werden und dass Stichproben aus verschiedenen Streams beim Rendern synchronisiert werden. Die Methode, die Sie verwenden, um sicherzustellen, dass die Streamsynchronisierung von der Renderingtechnik abhängig ist, die Sie für Ihre Anwendung verwenden. Wenn Sie über Audio- und Videostreams verfügen, sollten Sie im Allgemeinen eine Synchronisierung mit dem Audiostream verwenden, da die Inkonsistenz im Audiostream deutlicher ist als einige wenige verworfene Frames in einem Videostream.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**So rufen Sie Medienbeispiele mit dem asynchronen Reader ab**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**So rufen Sie Medienbeispiele mit dem synchronen Reader ab**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




