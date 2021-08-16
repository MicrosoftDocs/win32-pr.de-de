---
description: Verwenden von Multimedia-Streams in Anwendungen
ms.assetid: 73cfe89b-df46-445a-92c7-2f7323672441
title: Verwenden von Multimedia-Streams in Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: faadcf755019291ae394d03aac5fb16aa632605b5e1c5bc2a8a457de55343757
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525960"
---
# <a name="using-multimedia-streams-in-applications"></a>Verwenden von Multimedia-Streams in Anwendungen

> [!Note]  
> Diese APIs sind veraltet. Anwendungen sollten den [**Sample Grabber-Filter**](sample-grabber-filter.md) verwenden oder einen benutzerdefinierten Filter implementieren, um Daten aus einem DirectShow-Filterdiagramm zu erhalten.

 

Die Multimediastreamingschnittstellen vereinfachen den Prozess der Bearbeitung von Multimediadaten sehr, indem sie die Abhängigkeit von bestimmten Merkmalen der Hardware- oder Softwarequelle entfernen und Unterstützung für alle Microsoft DirectX®-Medienformate bereitstellen. Streams die Daten auf eine sehr hohe Ebene abstrahieren; -Anwendungen können sogar Daten aus einem Stream in einen anderen verschieben, ohne etwas über das Format der Daten zu wissen.

Führen Sie die folgenden Schritte aus, um einen Multimediastream zu erstellen.

1.  Erstellen Sie den Multimediastream. Die Methode zum Erstellen und Initialisieren des Streams ist architekturspezifisch. DirectShow unterstützt die [**IAMMultiMediaStream-Schnittstelle,**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) die zum Initialisieren des Streams verwendet wird. Andere prozessintern ausgeführte Serverimplementierungen von [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) werden mit unterschiedlichen Mechanismen erstellt und initialisiert.
2.  Nachdem das Multimediastreamobjekt initialisiert wurde, verwendet die Anwendung **QueryInterface,** um die **IMultiMediaStream-Schnittstelle** für das Objekt abzurufen. Verwenden Sie diese Schnittstelle, um die Eigenschaften des Streams zu bestimmen und die Streams selbst aufzählen. Sie können einen bestimmten Stream abrufen, indem Sie die [**IMultiMediaStream::GetMediaStream-Methode**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) mit einer bestimmten Zweck-ID aufrufen. MSPID PrimaryVideo und MSPID PrimaryAudio, die die primären Video- und Audiostreams darstellen, sind die am häufigsten verwendeten \_ \_ Zweck-IDs.
3.  Rufen **Sie IUnknown::QueryInterface** für eine Schnittstelle auf, die für den Medientyp des Streams spezifisch ist. Wenn Sie beispielsweise einen Videostream rendern möchten, rufen Sie dessen [**IDirectDrawMediaStream-Schnittstelle**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) ab. Medienspezifische Schnittstellen definieren zusätzliche Methoden, die erforderlich sind, um die Funktionen eines Formats voll zu nutzen.
4.  Erstellen Sie ein oder mehrere Beispiele aus den Datenstromdaten. Jeder Medienstream unterstützt die [**IMediaStream::CreateSharedSample-Methode**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) für die Beispielerstellung. Das resultierende Beispiel unterstützt die [**IStreamSample-Schnittstelle,**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) die die Kontrolle über das Beispiel und seine Merkmale bietet. In der Regel unterstützt der Medienstream eine formatspezifische Methode zur Beispielerstellung, die leistungsfähiger als die oben genannten **IStreamSample-Methoden** ist. **IDirectDrawMediaStream** kann z. B. Beispiele erstellen, die an eine gewünschte DirectDraw-Oberfläche angefügt sind, und ein Clippingrechteck erstellen. In einigen Situationen müssen Sie jedoch Daten verarbeiten, ohne ihr Datenformat zu kennen. Wenn Sie Daten unabhängig vom Format streamen möchten, verwenden Sie die **IMediaStream::CreateSharedSample-Methode,** um die Datenbeispiele zu erstellen.
5.  Nachdem Sie alle gewünschten Streambeispiele erstellt haben, starten Sie den Stream, indem Sie die [**IMultiMediaStream::SetState-Methode**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-setstate) aufrufen und das STREAMSTATE \_ RUN-Flag als Parameter übergeben.
6.  Rufen [**Sie IStreamSample::Update auf,**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) um das Streambeispiel zu aktualisieren. Wenn die **IStreamSample::Update-Methode** beendet wird, können Sie auf die Daten des Beispiels zugreifen. Wenn sie ein bestimmtes Ereignis oder einen Funktionsaufruf auslösen möchten, wenn das Update zurückgegeben wird, übergeben Sie die entsprechenden Zeiger an die **IStreamSample::Update-Methode.**

Weitere Informationen zu den Multimediastreamingschnittstellen finden Sie unter [Multimedia Streaming](multimedia-streaming.md).

 

 



