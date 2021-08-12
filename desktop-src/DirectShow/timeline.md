---
description: Zeitachse
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85809aed689d63ccdfc0b1dee1b5b792cafc9d7d0267d27e33bd7b6c1bea6cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651252"
---
# <a name="timeline"></a>Zeitachse

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das Zeitachsenobjekt verwaltet alle Objekte in einem Videobearbeitungsprojekt. Um dieses Objekt zu erstellen, rufen Sie **CoCreateInstance** auf. Der Klassenbezeichner ist CLSID \_ AMTimeline.

Um Windows Media™-Dateien zu lesen, muss die Anwendung ein Softwarezertifikat bereitstellen, das auch als Schlüssel bezeichnet wird. Registrieren Sie die Anwendung über die **IObjectWithSite-Schnittstelle** der Zeitachse als Schlüsselanbieter. Weitere Informationen finden Sie unter [Entsperren des Windows Media Format SDK.](unlocking-the-windows-media-format-sdk.md)

Das Zeitachsenobjekt macht die folgenden Schnittstellen verfügbar:

-   [**IAMSetErrorLog**](iamseterrorlog.md)
-   [**IAMTimeline**](iamtimeline.md)
-   **Iobjectwithsite**
-   **Ipersiststream**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Zeitachsenmodell](the-timeline-model.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



