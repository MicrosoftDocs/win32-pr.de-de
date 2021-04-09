---
description: Zeigt, wie ein Videoeffekt als Media Foundation Transformation (MFT) implementiert wird.
ms.assetid: ad7d20bc-5eab-4390-a48b-5ea8e97ead7d
title: MFT_Grayscale Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273c562eb5985d0a329c434a8e4aa44119744496
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130509"
---
# <a name="mft_grayscale-sample"></a>Beispiel für MFT \_ Grayscale

Zeigt, wie ein Videoeffekt als Media Foundation Transformation (MFT) implementiert wird. Das Graustufen-MFT konvertiert das YUV-Video in Graustufen, indem die Chroma-Werte im Video auf neutral festgelegt werden. Die MFT akzeptiert unkomprimierte Videos in den Formaten "UYVY", "im YUY2" oder "NV12".

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Microsoft Media Foundation Schnittstellen veranschaulicht:

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="usage"></a>Verbrauch

Das Beispiel MFT \_ Grayscale erstellt eine DLL, bei der es sich um einen com-Server für die MFT handelt. Vor der Verwendung von MFT müssen Sie die dll registrieren.

Führen Sie das [playbackfx-Beispiel](/previous-versions//bb970336(v=vs.85))aus, um die verwendete Graustufen-MFT anzuzeigen. Sie können auch das Tool topoedit verwenden, um eine Topologie zu erstellen, die das Graustufen-MFT enthält. Weitere Informationen zu topoedit finden Sie unter [topoedit](topoedit.md).

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mft_grayscale)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu YUV-Videos](about-yuv-video.md)
</dt> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[MFT \_ Audiodelay-Beispiel](mft-audiodelay-sample.md)
</dt> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 
