---
title: Rendern von Inhalten
description: Rendern von Inhalten
ms.assetid: 9a3baa33-dac4-4742-8f80-33b05caada09
keywords:
- Windows Media-Format-SDK, Rendern von Inhalten
- Advanced Systems Format (ASF), Rendern von Inhalten
- ASF (Advanced Systems Format), Rendern von Inhalten
- Advanced Systems Format (ASF), Inhalts Rendering
- ASF (Advanced Systems Format), Inhalts Rendering
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d6a171ce9b404c4cc16862ffd64b53ada5821b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856848"
---
# <a name="rendering-content"></a>Rendern von Inhalten

Das Windows Media-Format-SDK stellt keine Routinen zum Rendern von Inhalten bereit, die vom Reader-Objekt bereitgestellt werden. Wenn Sie Anwendungen schreiben, um die Inhalte in ASF-Dateien wiederzugeben, müssen Sie Ihre eigenen renderingroutinen implementieren.

Beim Rendern von Inhalten müssen Sie vorsichtig sein, um sicherzustellen, dass Beispiele in der Reihenfolge der Präsentationszeit gerendert werden und dass beim Rendern Beispiele aus unterschiedlichen Streams synchronisiert werden Die Methode, die Sie verwenden, um die streamsynchronisierung sicherzustellen, hängt von der für Ihre Anwendung verwendeten renderingtechnik ab. Im Allgemeinen sollten Sie, wenn Sie über Audiodaten und Videostreams verfügen, eine Synchronisierung mit dem Audiostream durchzuführen, da die Inkonsistenz im Audiostream merkbarer ist als einige wenige gelöschte Frames in einem Videostream.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**So rufen Sie Medien Beispiele mit dem asynchronen Reader ab**](to-retrieve-media-samples-with-the-asynchronous-reader.md)
</dt> <dt>

[**So rufen Sie Medien Beispiele mit dem synchronen Reader ab**](to-retrieve-media-samples-with-the-synchronous-reader.md)
</dt> </dl>

 

 




