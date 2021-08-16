---
description: Videobeispiele
ms.assetid: 1ee2ad6f-5e84-45ba-9849-cd3bd8e7eb29
title: Videobeispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3883b3a62cd907c89dd46d14681e28ad9a4d4d94653a9f04a9097707d22cff9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972599"
---
# <a name="video-samples"></a>Videobeispiele

Das Videobeispielobjekt ist eine spezielle Implementierung der [**INTERFACESSample-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) für die Verwendung mit dem [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR). Um eine Instanz dieses Objekts zu erstellen, rufen Sie die [**MFCreateVideoSampleFromSurface-Funktion**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) auf. Die -Funktion verwendet einen Zeiger auf eine Direct3D-Oberfläche und gibt einen Zeiger auf die **SCHNITTSTELLE "POINTERSample"** zurück. Die folgenden Objekttypen sollten Mithilfe dieser Funktion Beispiele zuordnen:

-   Benutzerdefinierte EVR-Moderatoren. Eine Moderatorin ordnet Videobeispiele zu und sendet sie an die [**MIXERTransform::P rocessOutput-Methode**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) des Mixers. Weitere Informationen finden Sie unter [Schreiben eines EVR-Presenters.](how-to-write-an-evr-presenter.md)

-   Videodecoder, die die Videobeschleunigung unterstützen. Weitere Informationen finden Sie unter [Unterstützen von DXVA 2.0 in Media Foundation](supporting-dxva-2-0-in-media-foundation.md).

Das Videobeispielobjekt implementiert die folgenden Schnittstellen:

-   [**1000000000**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

-   [**ÜBER DASIREDSAMPLE**](/windows/desktop/api/evr/nn-evr-imfdesiredsample)

-   [**VERURSACHERNachverfolgungSample**](/windows/win32/api/mfidl/nn-mfidl-imftrackedsample)

Wenn der *pUnkSurface-Parameter* von [**MFCreateVideoSampleFromSurface**](/windows/desktop/api/evr/nc-evr-mfcreatevideosamplefromsurface) ungleich **NULL** ist, enthält das resultierende Videobeispiel einen einzelnen Medienpuffer, der die Direct3D-Oberfläche kapselt. Dieses Pufferobjekt verfügt über eingeschränkte Funktionalität:

-   Die [**BUFFERMediaBuffer::Lock-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-lock) des Puffers gibt E \_ NOTIMPL zurück.

-   Der Puffer implementiert nicht die [**INTERFACES2DBuffer-Schnittstelle.**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer)

Die einzige Möglichkeit, über den Puffer auf die Oberfläche zuzugreifen, besteht darin, [**DEN DIENSTBEzeichner**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice)MR BUFFER SERVICE \_ aufzurufen. \_

Wenn der *pUnkSurface-Parameter* **NULL** ist, wird das Videobeispiel mit 0 Medienpuffern erstellt. Gehen Sie wie folgt vor, um dem Beispiel einen Puffer hinzuzufügen:

1.  Erstellen Sie eine Direct3D-Oberfläche.

2.  Erstellen Sie einen Oberflächenpuffer, indem Sie [**MFCreateDXSurfaceBuffer**](/windows/desktop/api/mfapi/nf-mfapi-mfcreatedxsurfacebuffer)aufrufen. Weitere Informationen finden Sie unter [DirectX Surface Buffer](directx-surface-buffer.md).

3.  Fügen Sie den Puffer zum Beispiel hinzu, indem Sie [**DENSAMPLE::AddBuffer**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-addbuffer)aufrufen.

Verwenden Sie diesen Ansatz, wenn sie benötigen, dass der Oberflächenspeicher über die [**INTERFACES2DBuffer-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imf2dbuffer) zugänglich ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienpuffer](media-buffers.md)
</dt> <dt>

[Medienbeispiele](media-samples.md)
</dt> </dl>

 

 
