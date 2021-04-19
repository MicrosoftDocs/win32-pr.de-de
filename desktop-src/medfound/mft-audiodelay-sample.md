---
description: MFT \_ Audiodelay-Beispiel
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d382ce7d1c5e9475bef85f11ef9754345e123b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359938"
---
# <a name="mft_audiodelay-sample"></a>MFT \_ Audiodelay-Beispiel

Zeigt, wie ein Audioeffekt als Media Foundation Transformation (MFT) implementiert wird. Die MFT für die Audioverzögerung akzeptiert PCM-Audiodaten als Eingabe, wendet einen Verzögerungseffekt (ECHO) an und gibt die geänderten Audiodaten aus.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Verbrauch

Das MFT \_ Audiodelay-Beispiel erstellt eine DLL, bei der es sich um einen com-Server für die MFT handelt. Vor der Verwendung von MFT müssen Sie die dll registrieren. Mit dem Tool topoedit können Sie eine Topologie erstellen, die die MFT für die Audioverzögerung einschließt. Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md). Sie können auch das [playbackfx-Beispiel](/previous-versions//bb970336(v=vs.85)) ändern, um die MFT zu verwenden. Sie müssen die Funktion "addbranchtopartialtopology" in "Player. cpp" ändern. Ändern Sie die folgende Zeile in:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, GUID_NULL);
}
```

Nach:

``` syntax
else if (majorType == MFMediaType_Audio)
{
    hr = CreateAudioBranch(pTopology, pSourceNode, CLSID_DelayMFT);
}
```

Der Wert CLSID \_ delaymft wird in der Header Datei "audiodelta-UUIDs. h" im MFT- \_ Beispiel Ordner "Audiodelay" deklariert.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Beispiel für MFT \_ Grayscale](mft-grayscale-sample.md)
</dt> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
