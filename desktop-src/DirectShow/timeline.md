---
description: Zeitachse
ms.assetid: 6cc36034-224c-4126-873b-0cfeceec9781
title: Zeitachse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10d1f802f12df6ca3469b8283bd4fe8b27e22412
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351593"
---
# <a name="timeline"></a>Zeitachse

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das Timeline-Objekt verwaltet alle-Objekte in einem Video Bearbeitungs Projekt. Um dieses Objekt zu erstellen, rufen Sie **cokreateinstance** auf. Der Klassen Bezeichner ist CLSID \_ amtimeline.

Um Windows Media™-Dateien zu lesen, muss die Anwendung ein Software Zertifikat bereitstellen, das auch als Schlüssel bezeichnet wird. Registrieren Sie die Anwendung als Schlüssel Anbieter über die **IObjectWithSite** -Schnittstelle der Zeitachse. Weitere Informationen finden Sie unter [Entsperren des Windows Media-Format](unlocking-the-windows-media-format-sdk.md)-SDKs.

Das Timeline-Objekt macht die folgenden Schnittstellen verfügbar:

-   [**Iameinterrorlog**](iamseterrorlog.md)
-   [**Iamtimeline**](iamtimeline.md)
-   **IObjectWithSite**
-   **IPersistStream**

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Das Zeitachsen Modell](the-timeline-model.md)
</dt> <dt>

[Erstellen einer Zeitachse](constructing-a-timeline.md)
</dt> </dl>

 

 



