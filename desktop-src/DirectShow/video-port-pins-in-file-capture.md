---
description: Video Port Pins in der Datei Erfassung
ms.assetid: 0fa6d88e-3c64-487f-b007-8c65bf47211d
title: Video Port Pins in der Datei Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2361c5a7cdaa7640ece9724000963f39f3f77ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347270"
---
# <a name="video-port-pins-in-file-capture"></a>Video Port Pins in der Datei Erfassung

Wenn das Erfassungsgerät über einen Videoport verfügt, muss die Videoport-PIN mit einem Videorenderer verbunden werden, auch wenn Sie nur in einer Datei erfassen möchten.

Wenn Sie " [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) " mit dem Wert " **Pin \_ Category \_ Capture** " und dem Gerät eine Videoport-Pin aufzurufen, verbindet der Erfassungs Diagramm-Generator automatisch die Videoport-PIN mit dem [Überlagerungs-Mischungs](overlay-mixer-filter.md) Filter und verbindet den Overlay-Mixer mit dem Videorenderer. Der Erfassungs Diagramm-Generator verbirgt das Videofenster durch Aufrufen von [**IVideoWindow::p UT \_ AutoShow**](/windows/desktop/api/Control/nf-control-ivideowindow-put_autoshow) mit dem Wert **oafalse**. Wenn die Anwendung später **RenderStream** mit der **Pin- \_ Kategorie \_ Vorschau** aufruft, ruft der Erfassungs Diagramm-Generator " **Put \_ AutoShow** " mit dem Wert " **oatrue**" auf, um das Videofenster anzuzeigen.

Nachdem Sie **RenderStream** mit **Pin \_ Category \_ Capture** aufgerufen haben, können Sie überprüfen, ob der Videorenderer hinzugefügt wurde, indem Sie den Filter Graph-Manager nach der [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) -Schnittstelle Abfragen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzeichnen von Videos in einer Datei](capturing-video-to-a-file.md)
</dt> </dl>

 

 



