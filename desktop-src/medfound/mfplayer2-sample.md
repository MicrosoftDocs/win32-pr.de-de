---
description: Wichtig ist veraltet.
ms.assetid: bb71e792-d09c-4338-9cf4-4854e14042f9
title: MFPlayer2-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1904dcc6e64024dacb76e9109f2e785ec8d5a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863431"
---
# <a name="mfplayer2-sample"></a>MFPlayer2-Beispiel

> [!IMPORTANT]
> Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden. Anwendungen sollten die [Medien Sitzung](media-session.md) für die Wiedergabe verwenden.

 

Veranschaulicht einige der Wiedergabe Features, die im [simpleplay](simpleplay-sample.md) -Beispiel ausgelassen werden, wie z. b.:

-   Diejenigen
-   Raten Kontrolle (schnelles vorwärts und Zurückspulen)
-   Audiovolume und stumm Steuerelemente
-   Video Zoom

Die folgende Abbildung zeigt die Steuerelemente, die für diese Funktionen verwendet werden.

![Screenshot des MF Player-Beispiels ](images/mfplayer2.png)

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden APIs veranschaulicht.

-   [**Iaudiosessioncontrol**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessioncontrol)
-   [**Iaudiosessionmanager**](/windows/win32/api/audiopolicy/nn-audiopolicy-iaudiosessionmanager)
-   [**Imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
-   [**Imfpmediaplayer**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer)
-   [**Imfpmediaplayercallback**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback)
-   [**Immdevice**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdevice)
-   [**Immdeviceenumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator)
-   [**Isimpleaudiovolume**](/windows/win32/api/audioclient/nn-audioclient-isimpleaudiovolume)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/MFPlayer2)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 
