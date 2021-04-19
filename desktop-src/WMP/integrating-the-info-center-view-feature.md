---
title: Integrieren der Info Center-Ansichts Funktion
description: Integrieren der Info Center-Ansichts Funktion
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player Online Stores, integrieren der Info Center-Ansicht
- Online Stores, integrieren der Info Center-Ansicht
- Typ 1 Online Stores, Integration der Info Center-Ansicht
- Typ 2 Online Stores, Integration der Info Center-Ansicht
- Windows Media Player Online Stores, Info Center-Ansicht
- Online Stores, Info Center-Ansicht
- Typ 1 Online Stores, Info Center-Ansicht
- Typ 2 Online Stores, Info Center-Ansicht
- Integrieren der Info Center-Ansicht
- Info Center-Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9564a6210181e0500bd1e447f621568f634817c4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341883"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrieren der Info Center-Ansichts Funktion

Windows Media Player ermöglicht Benutzern das Öffnen und Schließen der Info Center-Ansichts Funktion. Die Info Center-Ansicht ist die Funktion, mit der Benutzer umfassende, erweiterte Informationen zu bestimmten digitalen Medieninhalten finden. Wenn der Benutzer die InfoCenter-Ansicht öffnet, ruft Windows Media Player auf dem aktuellen Musikspeicher auf, um die InfoCenter-Ansichts Webseite anzuzeigen, die durch das **URL** -Attribut des **Infocenter** -Elements des serviceInfo-Dokuments angegeben wird.

Zum Abrufen von Informationen über den Inhalt, der aktuell wiedergegeben wird, müssen Sie eine Instanz des Windows Media Player-Steuer Elements in Ihre Webseite einbetten und das Player-Objektmodell verwenden. Zum Abrufen des Titels können Sie z. b. den folgenden JScript-Code verwenden:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Richtlinien für die Info Center-Ansicht

Verwenden Sie beim Erstellen der **Info Center-Ansichts** Webseite die folgenden Richtlinien:

-   Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren. Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Vermeiden Sie die Seitennavigation innerhalb der Info Center-Ansichts Funktion, wenn möglich. Für die meisten Aktivitäten sollten Sie zu Ihrem Online Store navigieren.
-   Es empfiehlt sich, wertvolle Informationen bereitzustellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Extern. navigatetaskpaneurl**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**InfoCenter-Element**](infocenter-element.md)
</dt> <dt>

[**Informationen, die von Typ 1 und Typ 2 Online Stores gemeinsam sind**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuer Elements in einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




