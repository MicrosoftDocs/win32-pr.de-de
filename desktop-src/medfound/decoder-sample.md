---
description: Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.
ms.assetid: 941e5400-e679-41f4-9830-3548dc6037aa
title: Decoder-Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd7586534876cfa7f530e675b0342a92bf46b8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958649"
---
# <a name="decoder-sample"></a>Decoder-Beispiel

Zeigt, wie ein Decoder für Microsoft Media Foundation geschrieben wird.

In diesem Beispiel wird ein Mock-MPEG-1-Video Decoder implementiert, der den Zeit Code für jeden Videorahmen anzeigt. Der MPEG-1-Bitstream wird nicht tatsächlich decodiert. Die folgende Abbildung zeigt die Videoausgabe des Decoders.

![Screenshot eines Video Frames vom Decoder](images/decodersample.png)

> [!Note]  
> Vor der Windows SDK für Windows 7 war dieses Beispiel als Teil des [MPEG1Source](mpeg1source-sample.md)-Beispiels enthalten.

 

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMF-Transformation**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/Decoder)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



