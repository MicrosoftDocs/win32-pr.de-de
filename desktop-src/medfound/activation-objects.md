---
description: Aktivierungs Objekte
ms.assetid: 767d5f1c-2b8d-43b6-916b-035129e93204
title: Aktivierungs Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa8741cbfa8bc3801a23b4976e60c0a3ad028b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129556"
---
# <a name="activation-objects"></a>Aktivierungs Objekte

Ein *Aktivierungs Objekt* ist ein Hilfsobjekt, das verwendet wird, um ein anderes Objekt zu erstellen, das einer Klassenfactory ähnelt. Aktivierungs Objekte machen die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle verfügbar.

Mit einem Aktivierungs Objekt können Sie die Erstellung des Zielobjekts verzögern, da Sie einen [**unfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger halten können, ohne das Zielobjekt zu erstellen. Aktivierungs Objekte können auch serialisiert und daher zum Erstellen des Zielobjekts in einem anderen Prozess verwendet werden. Beispielsweise werden Aktivierungs Objekte verwendet, um Pipeline Komponenten aus dem Anwendungsprozess in den PMP-Prozess (Protected Media Path) zu Mars Hallen. Aktivierungs Objekte werden auch von bestimmten Enumerationsfunktionen verwendet, die eine Liste von **imfaktivezeigern** zurückgeben. Bevor die Anwendung das Zielobjekt erstellt, kann Sie Informationen über das Objekt erhalten, indem die Attribute für das Aktivierungs Objekt untersucht werden.

Um das Zielobjekt aus einem Aktivierungs Objekt zu erstellen, rufen Sie die [**imfactivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode auf. Der Aufrufer muss [**imfaktivate:: shutdownobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-shutdownobject) aufgerufen werden, wenn er mithilfe des erstellten Objekts abgeschlossen wurde. Häufig erstellt die Anwendung das Aktivierungs Objekt, und die Medien Sitzung ruft **activateobject** auf. In diesem Fall muss die Medien Sitzung, nicht die Anwendung, **shutdownobject** aufzurufen. In anderen Situationen erhält die Anwendung einen [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger von der Medien Sitzung, und die Anwendung ruft **activateobject** und **shutdownobject** auf. (Informationen hierzu finden Sie beispielsweise [unter Wiedergabe geschützter Mediendateien](how-to-play-protected-media-files.md).)

Aktivierungs Objekte können über Attribute verfügen, und die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle erbt die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle. Einige Aktivierungs Objekte verwenden Attribute, um das erstellte Objekt zu konfigurieren. Die spezifischen Attribute, die von den einzelnen Objekten unterstützt werden, sind in der Referenz für die Erstellungs Funktion dieses Aktivierungs Objekts dokumentiert. Legen Sie die Attribute mit dem **imfaktivate** -Zeiger fest, den Sie von der Funktion erhalten.

Bei geschützter Wiedergabe werden Aktivierungs Objekte an den PMP-Prozess gemarshallt. Um das Marshalling zu unterstützen, muss ein Aktivierungs Objekt die **IPersistStream** -Schnittstelle verfügbar machen. Außerdem müssen das Aktivierungs Objekt und das erstellte Objekt vertrauenswürdige Komponenten sein, wenn das PMP in einem geschützten Prozess ausgeführt wird. Dies ist keine Anforderung, wenn das PMP in einen ungeschützten Prozess geladen wird.

Wenn Sie ein benutzerdefiniertes Pipeline Objekt (z. b. eine Medien Senke) im PMP-Prozess verwenden möchten, müssen Sie ein Aktivierungs Objekt für das Pipeline Objekt implementieren:

-   Das Aktivierungs Objekt muss [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) und **IPersistStream** verfügbar machen.
-   Die **ipersistent:: GetClassID** -Methode des Aktivierungs Objekts muss die CLSID des Aktivierungs Objekts zurückgeben.
-   Optional können Sie die **IPersistStream:: Save** -Methode und die **IPersistStream:: Load** -Methode implementieren, um alle Daten zu Mars Hallen, die Sie benötigen, um das Aktivierungs Objekt zu konfigurieren.

Wenn die Medien Sitzung die Topologie innerhalb des PMP-Prozesses lädt, wird **cokreateinstance** aufgerufen, um eine neue Instanz Ihres Aktivierungs Objekts zu erstellen. Anschließend wird [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) aufgerufen, um das Pipeline Objekt zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Plattform-APIs](media-foundation-platform-apis.md)
</dt> <dt>

[**Imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> </dl>

 

 



