---
description: '\_MFT-AudioDelay-Beispiel'
ms.assetid: 08f119f9-cacd-4000-96b6-60c8c0055e9c
title: MFT_AudioDelay Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea4af3d89c7dda4a67a2fece09ff9e6d3bc0a63927e94b259df40334fd9ba29b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012670"
---
# <a name="mft_audiodelay-sample"></a>\_MFT-AudioDelay-Beispiel

Zeigt, wie sie einen Audioeffekt als Media Foundation Transform (MFT) implementieren. Die Audioverzögerung MFT akzeptiert PCM-Audio als Eingabe, wendet einen Verzögerungseffekt (Echo) an und gibt die geänderten Audiodaten aus.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Microsoft Media Foundation veranschaulicht:

-   [**VORRÜBERSETZUNGTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Verbrauch

Im Beispiel MFT \_ AudioDelay wird eine DLL erstellt, bei der es sich um einen COM-Server für MFT handelt. Bevor Sie MFT verwenden, müssen Sie die DLL registrieren. Sie können das TopoEdit-Tool verwenden, um eine Topologie zu erstellen, die den MFT-Audioverzögerungs-MFT enthält. Weitere Informationen zu TopoEdit finden Sie unter [TopoEdit](topoedit.md). Sie können auch das [PlaybackFX-Beispiel ändern, um](/previous-versions//bb970336(v=vs.85)) MFT zu verwenden. Sie müssen die AddBranchToPartialTopology-Funktion in Player.cpp ändern. Ändern Sie die folgende Zeile von:

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

Der Wert CLSID DelayMFT wird in der Headerdatei \_ AudioDelayUuids.h im MFT \_ AudioDelay-Beispielordner deklariert.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository Windows klassischen Beispielen verfügbar.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_audiodelay)

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

 

 
