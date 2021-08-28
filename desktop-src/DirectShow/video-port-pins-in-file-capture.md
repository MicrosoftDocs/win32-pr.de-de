---
description: Videoport-Pins in der Dateierfassung
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Videoport-Pins in der Dateierfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab348c7e378f4130b43eef45f2cf4ddd079b0e85a77397b767cadddde5a7d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049380"
---
# <a name="video-port-pins-in-file-capture"></a>Videoport-Pins in der Dateierfassung

Wenn das Erfassungsgerät über einen Videoport verfügt, muss der Videoportanschluss mit einem Videorenderer verbunden sein, auch wenn Sie nur eine Datei erfassen möchten.

Wenn Sie [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit dem Wert **PIN CATEGORY \_ \_ CAPTURE** aufrufen und das Gerät über einen Videoportanschluss verfügt, verbindet capture Graph Builder automatisch den Videoportanschluss mit dem [Overlay Mixer-Filter](overlay-mixer-filter.md) und verbindet die Overlay Mixer mit dem Videorenderer. Der Capture Graph Builder blendet das Videofenster durch Aufrufen von [**IVideoWindow::p ut \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert **OAFALSE aus.** Wenn die Anwendung **renderStream** später mit **PIN CATEGORY \_ \_ PREVIEW** aufruft, geben die Aufrufe von Capture Graph Builder **\_ AutoShow** mit dem Wert **OATRUE** ein, um das Videofenster anzuzeigen.

Nachdem Sie **RenderStream** mit **PIN CATEGORY \_ \_ CAPTURE** aufrufen, können Sie überprüfen, ob der Videorenderer hinzugefügt wurde, indem Sie den Filter Graph Manager für die [**IVideoWindow-Schnittstelle**](/windows/desktop/api/Control/nn-control-ivideowindow) abfragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erfassen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



