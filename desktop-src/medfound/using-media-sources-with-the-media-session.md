---
description: Verwenden von Medienquellen mit der Medien Sitzung
ms.assetid: b50d3d6e-728b-4ba5-9b79-413d2108ade1
title: Verwenden von Medienquellen mit der Medien Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf08edf1d68ea11b05e8f8db83e247bc844cd85c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961138"
---
# <a name="using-media-sources-with-the-media-session"></a>Verwenden von Medienquellen mit der Medien Sitzung

Wenn Sie die Medien Sitzung zum Steuern der Wiedergabe verwenden, ist der Satz von Methoden, den Sie für eine Medienquelle aufzurufen sollten, eingeschränkt. In diesem Abschnitt wird beschrieben, wie Medienquellen in Verbindung mit der Medien Sitzung verwendet werden.

Im folgenden finden Sie die grundlegenden Schritte, die Ihre Anwendung ausführt:

1.  Erstellen Sie die Medienquelle. Verwenden Sie zum Erstellen einer Medienquelle den quellresolver. Weitere Informationen finden Sie unter [quellresolver](source-resolver.md). Der quellresolver gibt einen Zeiger auf die [**imfmediasource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) -Schnittstelle der Quelle zurück. (Wenn Sie eine benutzerdefinierte Medienquelle geschrieben haben, können Sie stattdessen eine benutzerdefinierte Erstellungs Methode bereitstellen.)

2.  Konfigurieren Sie die Präsentation. Um die Darstellung der Quelle zu konfigurieren, müssen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen. Sie können diese Kopie ändern, aber die Änderungen werden erst nach dem Start der Wiedergabe aktiv. Ändern Sie den Präsentations Deskriptor während der Wiedergabe nicht. Weitere Informationen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).

3.  Erstellen Sie eine Topologie, die die Medienquelle enthält. Weitere Informationen finden Sie unter [Topologien](topologies.md).

4.  Verwenden Sie die Medien Sitzung zum Steuern der Wiedergabe. In der Medien Sitzung werden Methoden für die Medienquelle aufgerufen. Die Anwendung sollte zu diesem Zeitpunkt keine Methoden für die Medienquelle abrufen.

5.  Bevor Sie die Medienquelle freigeben, wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Quelle zu schließen.

    > [!Note]  
    > Wenn Sie die Sequencer-Quelle verwenden, verarbeitet die Sequencer-Quelle das Herunterfahren der Segment Quellen. Weitere Informationen finden Sie unter [Sequencer-Quelle](sequencer-source.md).

     

Wenn Sie die Medien Sitzung verwenden, sind die einzigen Methoden, die Sie für die Medienquelle aufrufen sollten, " [**kreatepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)", " [**getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-getcharacteristics)" und " [**Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown)". Dies gilt insbesondere für:

-   " [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start)", " [**Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-pause)" oder " [**Anhalten**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop)" nicht aufzurufen. Diese Methoden sollten nur von der Medien Sitzung aufgerufen werden.

-   Es werden keine [**imfmediastream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) -Methoden aufgerufen.

-   Rufen Sie keine Ereignisse direkt aus der Medienquelle oder einem der Streams ab. Die Medien Sitzung muss diese Ereignisse empfangen, damit die Pipeline ordnungsgemäß funktioniert. Die Medien Sitzung leitet alle Ereignisse weiter, die von der Anwendung benötigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Sitzung](media-session.md)
</dt> </dl>

 

 



