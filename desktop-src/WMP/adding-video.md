---
title: Hinzufügen von Videos
description: Hinzufügen von Videos
ms.assetid: 6f20a9ad-e92e-4774-868d-ad0e071f4935
keywords:
- Erstellen von Skins,Video
- Windows Media Player Skins,Video
- Skins,Video
- Video in Skins, hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099778395146cb0bf0f27b483d55dd75c0fb8a0b28b879cc2d388f8e8cb7ba75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055408"
---
# <a name="adding-video"></a>Hinzufügen von Videos

Sie können Ihrer Datei ein Video hinzufügen, indem Sie einfach das **VIDEO-Element** verwenden und definieren, wo das Videofenster platziert werden soll.

Verwenden Sie den gleichen Code wie im Abschnitt Auswählen von Dateien. Sie müssen nur das **VIDEO-Element** mit den Attributen "top", "left", "width" und "height" hinzufügen.


```C++
        <VIDEO
            top = "10"
            left = "80"
            width = "180"
            height = "180"/>

```



Wenn Sie dann ein Video wieder geben, wird es im Fenster angezeigt. Die Art für das Videobeispiel wurde geändert, um eine etwas größere Skin zu erhalten. Da Ebenen in Buttons verwendet wurden, konnten die Schaltflächen problemlos verschoben werden, und eine neue Gruppe wurde sehr schnell erstellt. Nur das Hintergrundbild wurde geändert. Eine Füllung wurde in einer leeren Ebene verwendet, und ein Abschräge- und Einbettungseffekt wurde hinzugefügt.

Eine ähnliche funktionierende Video-Skin finden Sie im Beispielabschnitt des SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Handbuch zur Erstellung von Skins**](skin-creation-guide.md)
</dt> </dl>

 

 




