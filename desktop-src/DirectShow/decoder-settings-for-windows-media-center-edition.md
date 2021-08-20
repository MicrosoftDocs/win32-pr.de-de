---
description: Decoder Einstellungen für Windows Media Center Edition
ms.assetid: 019b063f-f215-44d8-a916-3125bee6af93
title: Decoder Einstellungen für Windows Media Center Edition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfc373f2ea58bc169748ff42841650cf979822014e579a78459e47da5c694814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953159"
---
# <a name="decoder-settings-for-windows-media-center-edition"></a>Decoder Einstellungen für Windows Media Center Edition

Windows XP Media Center Edition 2005 und höher verwendet die [**ICodecAPI-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-icodecapi) um den Audiodecoderfilter für die Wiedergabe von Fernseh- und DVD-Dateien zu konfigurieren. Die folgenden Eigenschaften werden unterstützt.



| Eigenschaften-GUID                   | BESCHREIBUNG                                      |
|---------------------------------|--------------------------------------------------|
| \_ \_ CODECAPI-AUDIOAUSGABEFORMAT \_ | Konfiguriert das Audioausgabeformat. Siehe Hinweise. |



 

## <a name="remarks"></a>Hinweise

Der Wert der CODECAPI AUDIO OUTPUT FORMAT-Eigenschaft ist eine Zeichenfolgendarstellung einer \_ \_ \_ GUID, die als **BSTR-Wert gespeichert** ist. Die folgenden GUIDs sind definiert.



| GUID                                                        | Beschreibung                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CODECAPI \_ AUDIO \_ OUTPUT \_ FORMAT \_ PCM \_ STEREO \_ MATRIXENCODED | Der Softwareaudiofilter sollte die Softwaredecodierung durchführen und einen Stereo-Audiostream mit der Multichannel-Audiomatrix, die an die beiden Kanäle codiert ist, aus geben.                                                   |
| CODECAPI \_ AUDIO \_ OUTPUT \_ FORMAT \_ PCM \_ STEREO                | Der Softwareaudiofilter sollte die Softwaredecodierung durchführen und einen Stereo-Audiostream aus geben.                                                                                                                   |
| \_CODECAPI-AUDIOAUSGABEFORMAT \_ \_ \_ \_ :PCMIF                 | Der Softwareaudiofilter sollte die Softwareaudiodecodierung durchführen, auch wenn die physische Ausgabe des PCs eine digitale Schnittstelle sein kann, z. B. S/PDIF.                                                      |
| \_CODECAPI-AUDIOAUSGABEFORMAT \_ \_ : \_ \_ BITSTREAMIF           | Der Softwareaudiofilter sollte keine Softwareaudiodecodierung durchführen, sondern den unformatierten digitalen Audiobitstream für die externe Verarbeitung durch ein Gerät übergeben, das mit einem digitalen Audiolink wie S/PDIF verbunden ist. |
| \_CODECAPI-AUDIOAUSGABEFORMAT \_ \_ \_ \_ PCM-FEHLER            | Der Softwareaudiofilter sollte die Softwareaudiodecodierung durchführen und proprietäre Verarbeitung anwenden, um die Optimierung für Dies zu optimieren. Die Unterstützung für diese Einstellung ist optional.                                     |



 

> [!Note]  
> Die **ICodecAPI-Schnittstelle** speichert Codeceigenschaften als Schlüssel-Wert-Paare, wobei der Schlüssel eine GUID und der Wert ein **VARIANT-Typ** ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Encoder- und Decoderentwicklung](encoder-and-decoder-development.md)
</dt> </dl>

 

 



