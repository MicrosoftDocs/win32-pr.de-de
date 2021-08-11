---
description: Wichtig Veraltet.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: MFPlayer2-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ead2df415af1584f34661a0c1d18751350d59bd1a94ac48f41d3bf9dca2070f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241731"
---
# <a name="mfplayer2-sample"></a>MFPlayer2-Beispiel

> [!IMPORTANT]
> Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows. Anwendungen sollten die [Mediensitzung für die](media-session.md) Wiedergabe verwenden.

 

Veranschaulicht einige der Wiedergabefeatures, die im [SimplePlay-Beispiel](simpleplay-sample.md) weggelassen werden, z. B.:

-   Suchen
-   Steuerung der Rate (schnelles Vor- und Zurücksenden)
-   Audio volume and mute controls (Audiovolumen und Stummschaltungssteuerelemente)
-   Videozoom

Die folgende Abbildung zeigt die steuerelemente, die für diese Features verwendet werden.

![Screenshot des mfplayer-Beispiels ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden APIs veranschaulicht.

-   [**IAudioSessionControl**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**IAudioSessionManager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**IMFPMediaPlayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**IMFPMediaPlayerCallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**IMMDevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**ISimpleAudioVolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
