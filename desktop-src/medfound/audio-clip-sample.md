---
description: Zeigt, wie Microsoft Media Foundation verwendet wird, um Audiodaten aus einer Mediendatei zu decodieren.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Beispiel für Audioclip
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346257"
---
# <a name="audio-clip-sample"></a>Beispiel für Audioclip

Zeigt, wie Microsoft Media Foundation verwendet wird, um Audiodaten aus einer Mediendatei zu decodieren.

Die Beispielanwendung Audioclip liest Audiodaten aus einer Mediendatei und schreibt die nicht komprimierte Audiodatei in eine Wave-Datei.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Verbrauch

Bei diesem Beispiel handelt es sich um eine Befehlszeilen Anwendung. Es verwendet die folgenden Befehlszeilenargumente:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   Input file: der Name einer Datei, die einen Audiostream enthält.
-   OutputFile. WAV: der Name der zu schreibenden Wave-Datei.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Quell Leser](source-reader.md)
</dt> <dt>

[Tutorial: Decodieren von Audiodaten](tutorial--decoding-audio.md)
</dt> </dl>

 

 



