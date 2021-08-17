---
description: Verwenden von Medienquellen mit der Mediensitzung
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Verwenden von Medienquellen mit der Mediensitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ffec1b854829b5b8a0317d10adf121463e539dde471bc5b3063b1479037ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117688724"
---
# <a name="using-media-sources-with-the-media-session"></a>Verwenden von Medienquellen mit der Mediensitzung

Wenn Sie die Mediensitzung verwenden, um die Wiedergabe zu steuern, ist der Satz von Methoden, die Sie für eine Medienquelle aufrufen sollten, eingeschränkt. In diesem Abschnitt wird beschrieben, wie Sie die Medienquelle in Verbindung mit der Mediensitzung verwenden.

Dies sind die grundlegenden Schritte, die Ihre Anwendung ausführen wird:

1.  Erstellen Sie die Medienquelle. Verwenden Sie den Quellre resolver, um eine Medienquelle zu erstellen. Weitere Informationen finden Sie unter [Quellre resolver](source-resolver.md). Der Quellre resolver gibt einen Zeiger auf die [**METHODEMediaSource-Schnittstelle der Quelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) zurück. (Wenn Sie eine benutzerdefinierte Medienquelle geschrieben haben, können Sie stattdessen eine benutzerdefinierte Erstellungsmethode bereitstellen.)

2.  Konfigurieren Sie die Präsentation. Um die Darstellung der Quelle zu konfigurieren, rufen [**Sie DIE MEDIENQUELLE::CreatePresentationDescriptor auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) Sie können diese Kopie ändern, aber die Änderungen werden erst aktiv, wenn die Wiedergabe beginnt. Ändern Sie den Präsentationsdeskriptor während der Wiedergabe nicht. Weitere Informationen finden Sie unter [Präsentationsdeskriptoren.](presentation-descriptors.md)

3.  Erstellen Sie eine Topologie, die die Medienquelle enthält. Weitere Informationen finden Sie unter [Topologien](topologies.md).

4.  Verwenden Sie die Mediensitzung, um die Wiedergabe zu steuern. Die Mediensitzung ruft Methoden für die Medienquelle auf. Die Anwendung sollte derzeit keine Methoden für die Medienquelle aufrufen.

5.  Rufen Sie vor dem Freigeben der Medienquelle [**DEN COMPUTERMEDIASource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf, um die Quelle herunter zu fahren.

    > [!Note]  
    > Wenn Sie die Sequencerquelle verwenden, übernimmt die Sequencerquelle das Herunterfahren der Segmentquellen. Weitere Informationen finden Sie unter [Sequencer Source](sequencer-source.md).

     

Wenn Sie die Mediensitzung verwenden, sollten Sie für die Medienquelle nur [**CreatePresentationDescriptor,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) [**GetCharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)und [**Shutdown aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) Dies gilt insbesondere für:

-   Rufen Sie nicht [**Start,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) [**Pause oder**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause) [**Stop auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) diese Methoden sollten nur von der Mediensitzung aufgerufen werden.

-   Rufen Sie keine [**METHODEN VOM 16. Bis zum 1.**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

-   Rufen Sie Ereignisse nicht direkt aus der Medienquelle oder einem der Streams ab. Die Mediensitzung muss diese Ereignisse empfangen, damit die Pipeline ordnungsgemäß funktioniert. Die Mediensitzung gibt alle Ereignisse weiter, die von der Anwendung benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mediensitzung](media-session.md)
</dt> </dl>

 

 



