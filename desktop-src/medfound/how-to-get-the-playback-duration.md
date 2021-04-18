---
description: In diesem Thema wird beschrieben, wie Sie die Wiedergabedauer einer Mediendatei mithilfe von mfplay erhalten.
ms.assetid: b1ea4f21-55d1-47b0-b6d3-8951dce79f7c
title: So erhalten Sie die Wiedergabedauer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21dd98a916109c8fb3d0ad3311643b1ffdc0a03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357416"
---
# <a name="how-to-get-the-playback-duration"></a>So erhalten Sie die Wiedergabedauer

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie die Wiedergabedauer einer Mediendatei mithilfe von mfplay erhalten.

**So erhalten Sie die Wiedergabedauer**

1.  Rufen Sie [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) oder [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) auf, um ein Medien Element für die Datei zu erstellen.
2.  [**Imfpmediaitem:: getduration**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration)aufrufen. Geben Sie für den ersten Parameter **MFP \_ PositionType \_ 100 ns** an. Die Dauer wird als **PROPVARIANT** zurückgegeben, das einen **großen \_ ganzzahligen** Wert enthält. Die Dauer wird in 100-Nanosecond-Einheiten angegeben.

Das folgende Beispiel zeigt Schritt 2:


```C++
#include <propvarutil.h>

HRESULT GetPlaybackDuration(IMFPMediaItem *pItem, ULONGLONG *phnsDuration)
{
    PROPVARIANT var;

    HRESULT hr = pItem->GetDuration(MFP_POSITIONTYPE_100NS, &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt64(var, phnsDuration);
        PropVariantClear(&var);
    }

    return hr;
}
```



## <a name="requirements"></a>Anforderungen

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



