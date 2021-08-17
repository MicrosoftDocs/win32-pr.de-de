---
description: Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Decoderbeispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 290f8b2db32b12d535feaeef65f37b77e1a29115cd8844a8d8aad29fb7ce699a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119449385"
---
# <a name="decoder-sample"></a>Decoderbeispiel

Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.

In diesem Beispiel wird ein MPEG-1-Pseudovideodecoder implementiert, der den Zeitcode für jeden Videoframe anzeigt. Der MPEG-1-Bitstream wird nicht tatsächlich decodiert. Die folgende Abbildung zeigt die Videoausgabe des Decoders.

![Screenshot eines Videoframes aus dem Decoder](images/decodersample.png)

> [!Note]  
> Vor dem Windows SDK für Windows 7 war dieses Beispiel als Teil des [MPEG1Source-Beispiels](mpeg1source-sample.md)enthalten.

 

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**ÜBERTRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [github-Repository mit Windows klassischen Beispielen](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



