---
description: Video Beispiele
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Video Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 239fecd0947271627abc7fc50ed16f6a7c682b84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863924"
---
# <a name="video-samples"></a>Video Beispiele

Das Video Sample-Objekt ist eine spezialisierte Implementierung der [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle für die Verwendung mit dem [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR). Rufen Sie die [**mfcreatevideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) -Funktion auf, um eine Instanz dieses Objekts zu erstellen. Die Funktion nimmt einen Zeiger auf eine Direct3D-Oberfläche und gibt einen Zeiger auf die **imfsample** -Schnittstelle zurück. Die folgenden Objekttypen sollten mithilfe dieser Funktion Beispiele zuordnen:

-   Benutzerdefinierte EVR-Moderatoren. Ein Presenter ordnet Videobeispiele zu und sendet Sie an die [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) -Methode des Mischers. Weitere Informationen finden Sie unter [How to Write a EVR Presenter](how-to-write-an-evr-presenter.md).

-   Video-Decoder, die Videobeschleunigung unterstützen. Weitere Informationen finden Sie [unter unterstützen von DXVA 2,0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

Das Video Sample-Objekt implementiert die folgenden Schnittstellen:

-   [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**IMF-redsample**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**IMF trackedsample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Wenn der *punksurface* -Parameter von [**MF createvideosamplefromsurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) nicht **null** ist, enthält das resultierende Video Beispiel einen einzelnen Medien Puffer, der die Direct3D-Oberfläche kapselt. Dieses Puffer Objekt verfügt über eingeschränkte Funktionalität:

-   Die [**imfmediabuffer:: Lock**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) -Methode des Puffers gibt E \_ notimpl zurück.

-   Die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle wird vom Puffer nicht implementiert.

Die einzige Möglichkeit für den Zugriff auf die-Oberfläche aus dem Puffer besteht darin, [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)mit dem Dienst Bezeichner Mr- \_ Puffer Dienst aufzurufen \_ .

Wenn der Parameter " *punksurface* " **null** ist, wird das Video Beispiel mit NULL Medien Puffern erstellt. Um dem Beispiel einen Puffer hinzuzufügen, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie eine Direct3D-Oberfläche.

2.  Erstellen Sie einen Oberflächen Puffer, indem Sie [**mfcreatedxsurfacebuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer)aufrufen. Weitere Informationen finden Sie unter [DirectX-Oberflächen Puffer](directx-surface-buffer.md).

3.  Fügen Sie den Puffer dem Beispiel hinzu, indem Sie [**imfsample:: addbuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)aufrufen.

Verwenden Sie diesen Ansatz, wenn Sie den Surface-Speicher über die [**IMF2DBuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) -Schnittstelle zugänglich sein müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Puffer](media-buffers.md)
</dt> <dt>

[Medien Beispiele](media-samples.md)
</dt> </dl>

 

 
