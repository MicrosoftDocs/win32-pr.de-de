---
description: Verwenden von Multimedia-Streams in Anwendungen
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Verwenden von Multimedia-Streams in Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f30dab204bc7b0bddbdc293708daecbe0558e8f9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961163"
---
# <a name="using-multimedia-streams-in-applications"></a>Verwenden von Multimedia-Streams in Anwendungen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Beispiel-Grabber**](sample-grabber-filter.md) Filter verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filter Diagramm zu erhalten.

 

Die multimediastreamingschnittstellen vereinfachen den Prozess der Bearbeitung von Multimedia-Daten erheblich, indem die Abhängigkeit von bestimmten Merkmalen der Hardware oder Software Quelle entfernt wird und Unterstützung für alle Microsoft DirectX®-Medienformate bereitgestellt wird. Streams abstrahiert die Daten auf einen sehr hohen Grad. Anwendungen können sogar Daten von einem Stream in einen anderen verschieben, ohne etwas über das Datenformat zu wissen.

Führen Sie die folgenden Schritte aus, um einen multimediarestream zu erstellen.

1.  Erstellen Sie den Multimedia-Stream. Die Methode der Erstellung und Initialisierung des Streams ist architekturspezifisch. DirectShow unterstützt die [**iammultimediastream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) -Schnittstelle, die zum Initialisieren des Streams verwendet wird. Andere Prozess interne Server Implementierungen von [**imultimediastream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) werden mithilfe verschiedener Mechanismen erstellt und initialisiert.
2.  Nachdem das multimediastreamobjekt initialisiert wurde, verwendet die Anwendung **QueryInterface** , um die **imultimediastream** -Schnittstelle für das Objekt abzurufen. Verwenden Sie diese Schnittstelle, um die Eigenschaften des Streams zu ermitteln und die Streams selbst aufzulisten. Sie können einen bestimmten Stream abrufen, indem Sie die [**imultimediastream:: getmediastream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) -Methode mit einer bestimmten Zweck-ID aufrufen. Mspid \_ primaryvideo und mspid \_ primaryaudiodaten, die die primären Video-und Audiodatenströme darstellen, sind die am häufigsten verwendeten Zweck-IDs.
3.  Ruft **IUnknown:: QueryInterface** für eine Schnittstelle auf, die für den Medientyp des Streams spezifisch ist. Wenn Sie z. b. einen Videostream Rendering möchten, rufen Sie die [**idirectdrawmediastream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) -Schnittstelle ab. Medienspezifische Schnittstellen definieren zusätzliche Methoden, die erforderlich sind, um die Funktionen eines Formats in vollem Umfang zu nutzen.
4.  Erstellen Sie ein oder mehrere Beispiele aus den Streamdaten. Jeder Mediendaten Strom unterstützt die [**imediastream::**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) -Methode zum Erstellen von Beispielen. Das resultierende Beispiel unterstützt die [**istreamsample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) -Schnittstelle, die die Kontrolle über das Beispiel und seine Merkmale bietet. In der Regel unterstützt der Mediendaten Strom eine Format spezifische Methode der Beispiel Erstellung, die leistungsfähiger als die oben erwähnten **istreamsample** -Methoden ist. **Idirectdrawmediastream** kann z. b. Beispiele erstellen, die an eine gewünschte DirectDraw-Oberfläche und ein Clippingrechteck angefügt sind. In einigen Situationen müssen Sie jedoch Daten verarbeiten, ohne sich über das Datenformat zu wissen. Wenn Sie Daten unabhängig von Ihrem Format streamen möchten, verwenden Sie die **imediastream:: deesesharedsample** -Methode, um die Daten Beispiele zu erstellen.
5.  Nachdem Sie alle gewünschten streambeispiele erstellt haben, starten Sie den Datenstrom, indem Sie die [**imultimediastream:: SetState**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) -Methode aufrufen und das streamstate- \_ Run-Flag als Parameter übergeben.
6.  Nennen Sie [**istreamsample:: Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) , um das streambeispiel zu aktualisieren. Wenn die **istreamsample:: Update** -Methode beendet wird, können Sie auf die Beispiel Daten zugreifen. Wenn Sie einen bestimmten Ereignis-oder Funktions Rückruf bei der Aktualisierung zurückgeben möchten, übergeben Sie die entsprechenden Zeiger an die **istreamsample:: Update** -Methode.

Weitere Informationen zu den multimediastreaming-Schnittstellen finden Sie unter [Multimedia Streaming](multimedia-streaming.md).

 

 



