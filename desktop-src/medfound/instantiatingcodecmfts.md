---
description: Instanziieren von Codec-MFTs
ms.assetid: 171f9a0f-effb-4ed7-8aff-d7b1ee6e4973
title: Instanziieren von Codec-MFTs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa886f24f7dbd1acc373c7e505baddf71bc3aa8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214695"
---
# <a name="instantiating-codec-mfts"></a>Instanziieren von Codec-MFTs

[Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) sind COM-Objekte, die die [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle implementieren. Ein MFT ist ein Objekt zum Transformieren von Multimedia-Daten als Teil einer Pipeline. Eine Pipeline ist ein gerichtetes azyklisches Diagramm, das aus Medienquellen, Medien Transformationen und Medien senken besteht. Eine Pipeline verarbeitet asynchron Streaming-Multimediadaten.

Obwohl MFTs unabhängig von der Media Foundation Pipeline Infrastruktur instanziiert und verwendet werden können, empfiehlt es sich, nach Möglichkeit das mediafoundations-Framework zu verwenden.

Sie können eine Codec-MFT erstellen, indem Sie die [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) -Funktion aufrufen. Sie müssen den Klassen Bezeichner der MFT, den Schnittstellen Bezeichner von [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)und einen Zeiger auf einen **imftransform** -Zeiger übergeben.

Die Klassen Bezeichner der Codec-MFTs werden als Konstanten in der Header Datei "wmcodecdsp. h" definiert.

Die Konstante für den [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstellen Bezeichner ist IID \_ IMF Transform.

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

 

 
