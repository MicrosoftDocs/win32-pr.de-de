---
description: Zeigt, wie Sie Microsoft Media Foundation zum Decodieren von Audiodaten aus einer Mediendatei verwenden.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Beispiel für Audioclips
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f180dfb7c4b0e456f45169d36fdfb1f77701b0e82250690706208a715fdd3ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035488"
---
# <a name="audio-clip-sample"></a>Beispiel für Audioclips

Zeigt, wie Sie Microsoft Media Foundation zum Decodieren von Audiodaten aus einer Mediendatei verwenden.

Die Beispielanwendung Audioclip liest Audiodaten aus einer Mediendatei und schreibt die unkomprimierten Audiodaten in eine WAVE-Datei.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation veranschaulicht:

-   [**VERERBUNGQuelleReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Verbrauch

Dieses Beispiel ist eine Befehlszeilenanwendung. Es werden die folgenden Befehlszeilenargumente verwendet:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   inputfile: Der Name einer Datei, die einen Audiostream enthält.
-   outputfile.wav: Der Name der zu schreibenden WAVE-Datei.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Quellleser](source-reader.md)
</dt> <dt>

[Tutorial: Decodieren von Audio](tutorial--decoding-audio.md)
</dt> </dl>

 

 



