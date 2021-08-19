---
description: Konfigurieren der Audiocodierung
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Konfigurieren der Audiocodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2344808decffd4b50d5926074dbf71d60445580adb4556703367369e1e146d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880365"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Konfigurieren der Audiocodierung (Microsoft Media Foundation)

Der Windows Media Audio Encoder listet alle unterstützten Ausgabetypen in der vollständigen Form auf. Rufen Sie den typ ab, den Sie wünschen, indem Sie **IMediaObject::GetOutputType** oder **EINETRANSFORM::GetAvailableOutputType** aufrufen, und legen Sie dann den abgerufenen Typ unverändert als Ausgabetyp fest, indem **Sie IMediaObject::SetOutputType** oder **ENUMERATIONTransform::SetOutputType aufrufen.**

Die vom Audioencoder unterstützten Ausgabemedientypen ändern sich, wenn Encodereigenschaften konfiguriert werden. Sie müssen alle Encodereigenschaften konfigurieren, die Sie verwenden möchten, bevor Sie den Ausgabetyp aufzählen.

Die Modi "Two-Pass" und "VBR" werden von den Audioencodern unterstützt, sind jedoch anders konfiguriert als für Videos. Weitere Informationen finden Sie unter [Aufzählen von Audiotypen für bestimmte Codierungsmodi.](enumeratingaudiotypesforspecificencodingmodes.md)

Die vom Audioencoder unterstützten Eingabetypen sind erst verfügbar, wenn Sie den Ausgabetyp festgelegt haben. Wenn Sie **IMediaObject::GetInputType** oder VOR dem Festlegen eines Ausgabetyps VOR DEM FESTLEGEN EINES **AUSGABETYPs aufrufen,** gibt die Methode DMO E NO MORE ITEMS bzw. \_ \_ \_ \_ MFT E NO MORE TYPES \_ \_ \_ \_ zurück. Nachdem der Ausgabetyp festgelegt wurde, enumeriert der Encoder die Eingabetypen, die er für den ausgewählten Ausgabetyp unterstützt.

Der Medienaudioencoder Windows keine Audio-Resamplings. Dies bedeutet, dass der Encoderausgabetyp und der Encodereingabetyp die gleiche Anzahl von Kanälen, Bits pro Stichprobe und Abtastrate haben müssen. Weitere Informationen finden Sie unter [Finding Audio Encoder Output Types](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Jeder vom Audioencoder aufzählte Ausgabetyp enthält eine **WAVEFORMATEX-Struktur** (auf die **AM MEDIA \_ \_ TYPE.pbFormat** verweist), an die erweiterte Daten angefügt sind. Die Größe der erweiterten Daten wird durch **WAVEFORMATEX.cbSize angegeben.** Diese Daten müssen mit dem codierten Inhalt beibehalten werden, damit sie an den Decoder übermittelt werden können. Der Inhalt kann ohne die Daten im erweiterten Format nicht dekomprimiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audio](workingwithaudio.md)
</dt> </dl>

 

 



