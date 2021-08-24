---
description: Aktivierungsobjekte
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Aktivierungsobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 401b4643e7e19c8cf0b7235218eaed2e355565fdb82a9d3756558e1f11991cbe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035598"
---
# <a name="activation-objects"></a>Aktivierungsobjekte

Ein *Aktivierungsobjekt* ist ein Hilfsobjekt, das zum Erstellen eines anderen Objekts verwendet wird, ähnlich wie eine Klassen factory. Aktivierungsobjekte machen die [**BERACTIVate-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) verfügbar.

Mit einem Aktivierungsobjekt können Sie die Erstellung des Zielobjekts zurückhalten, da Sie sich an einem [**VERWERTer-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) halten können, ohne das Zielobjekt zu erstellen. Aktivierungsobjekte können auch serialisiert und somit verwendet werden, um das Zielobjekt in einem anderen Prozess zu erstellen. Aktivierungsobjekte werden beispielsweise verwendet, um Pipelinekomponenten aus dem Anwendungsprozess in den PMP-Prozess (Protected Media Path) zu marshallen. Aktivierungsobjekte werden auch von bestimmten Enumerationsfunktionen verwendet, die eine Liste mit **DEN -ZEIGERn VOM DATENTYP (ACTIVate)** zurückgeben. Bevor die Anwendung das Zielobjekt erstellt, kann sie Informationen zum Objekt durch Untersuchen von Attributen für das Aktivierungsobjekt erhalten.

Um das Zielobjekt aus einem Aktivierungsobjekt zu erstellen, rufen Sie [**die METHODEACTIVate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf. Der Aufrufer muss [**DANNACTIVate::ShutdownObject aufrufen,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) wenn es mit dem erstellten Objekt fertig ist. Häufig erstellt die Anwendung das Aktivierungsobjekt, und die Mediensitzung ruft **ActivateObject auf.** In diesem Fall muss die Mediensitzung und nicht die Anwendung **ShutdownObject aufrufen.** In anderen Situationen empfängt die Anwendung einen [**VORZEIGERAktivierungszeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) aus der Mediensitzung, und die Anwendung ruft **ActivateObject** und **ShutdownObject auf.** (Siehe z.B. [How to Play Protected Media Files](how-to-play-protected-media-files.md).)

Aktivierungsobjekte können Attribute aufweisen, und die [**SCHNITTSTELLE FÜR DIES-Aktivierung**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) erbt die [**SCHNITTSTELLE DURCHATTRIBUTAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Einige Aktivierungsobjekte verwenden Attribute, um das erstellte Objekt zu konfigurieren. Die spezifischen Attribute, die von den einzelnen Objekten unterstützt werden, sind in der Referenz für die Erstellungsfunktion dieses Aktivierungsobjekts dokumentiert. Legen Sie die Attribute fest, indem Sie den VON der Funktion empfangenen **POINTERActivate-Zeiger** verwenden.

Für die geschützte Wiedergabe werden Aktivierungsobjekte an den PMP-Prozess gemarshallt. Um Marshalling zu unterstützen, muss ein Aktivierungsobjekt die **IPersistStream-Schnittstelle** verfügbar machen. Darüber hinaus müssen sowohl das Aktivierungsobjekt als auch das erstellte Objekt vertrauenswürdige Komponenten sein, wenn der PMP in einem geschützten Prozess ausgeführt wird. Dies ist nicht erforderlich, wenn der PMP in einem ungeschützten Prozess geladen wird.

Um ein benutzerdefiniertes Pipelineobjekt (z. B. eine Mediensenke) innerhalb des PMP-Prozesses zu verwenden, müssen Sie ein Aktivierungsobjekt für Ihr Pipelineobjekt implementieren:

-   Das Aktivierungsobjekt muss [**DIESACTIVate und**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) **IPersistStream verfügbar machen.**
-   Die **IPersist::GetClassID-Methode** des Aktivierungsobjekts muss die CLSID des Aktivierungsobjekts zurückgeben.
-   Optional können Sie die **Methoden IPersistStream::Save** und **IPersistStream::Load** implementieren, um alle Daten zu marshallen, die Sie zum Konfigurieren Ihres Aktivierungsobjekts benötigen.

Wenn die Mediensitzung die Topologie innerhalb des PMP-Prozesses lädt, ruft sie **CoCreateInstance** auf, um eine neue Instanz Ihres Aktivierungsobjekts zu erstellen. Anschließend ruft sie ZUM Erstellen [**des Pipelineobjekts DIEACTIVATE::ActivateObject-Klasse**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> <dt>

[**ACTIVate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



