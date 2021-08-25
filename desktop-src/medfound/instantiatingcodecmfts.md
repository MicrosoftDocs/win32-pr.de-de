---
description: Instanziieren von Codec-MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Instanziieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a73af4055aee1d5b7e6a3ea137ab2204c9e59194f57ae4776e6c8368429db877
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827610"
---
# <a name="instantiating-codec-mfts"></a>Instanziieren von Codec-MFTs

[Media Foundation Transforms](media-foundation-transforms.md) (MFTs) sind COM-Objekte, die die [**NSTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) implementieren. Ein MFT ist ein Objekt zum Transformieren von Multimediadaten als Teil einer Pipeline. Eine Pipeline ist ein gerichteter azyklischer Graph, der aus Medienquellen, Medientransformationen und Mediensenken besteht. Eine Pipeline verarbeitet das Streaming von Multimediadaten asynchron.

Obwohl MFTs unabhängig von der Media Foundation-Pipelineinfrastruktur instanziiert und verwendet werden können, ist es vorzuziehen, nach Möglichkeit das MediaFoundation-Framework zu verwenden.

Sie können einen Codec-MFT erstellen, indem Sie die [**CoCreateInstance-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) aufrufen. Sie müssen den Klassenbezeichner des MFT, den Schnittstellenbezeichner [**von VERETRANSFORM**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)und einen Zeiger auf einen **NSTRANSFORM-Zeiger** übergeben.

Die Klassenbezeichner der Codec-MFTs werden als Konstanten in der Headerdatei wmcodecdsp.h definiert.

Die Konstante für den [**BEzeichner der BEzeichner der ENTTRANSFORM-Schnittstelle**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ist IID-KENNUNGTransform. \_

Im folgenden Codebeispiel wird veranschaulicht, wie eine Instanz eines Codec-MFT erstellt wird:


```
HRESULT CreateVideoEncoderMFT(IMFTransform** ppMFT)
{
    if (ppMFT == NULL)
        return E_POINTER;

    return CoCreateInstance(CLSID_CWMV9EncMediaObject,
                            NULL,
                            CLSCTX_INPROC_SERVER, 
                            IID_IMFTransform, 
                            (void**)ppMFT);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 
