---
title: Integrieren des Infocenter-Ansichtsfeatures
description: Integrieren des Infocenter-Ansichtsfeatures
ms.assetid: ce6692d2-a780-4aab-809f-c63236edd912
keywords:
- Windows Media Player,Integration der Infocenteransicht
- Onlineshops,Integration der Infocenteransicht
- Geben Sie 1 Onlineshops ein, und integrieren Sie die Infocenteransicht.
- Typ 2 Onlineshops,Integration der InfoCenter-Ansicht
- Windows Media Player,Info Center-Ansicht
- Onlineshops,Info Center-Ansicht
- Typ 1 Onlineshops, Infocenteransicht
- Typ 2 Onlineshops,Info Center-Ansicht
- Integrieren der Infocenteransicht
- Infocenteransicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caea279f933c3cbb411da72aab9ddf971df5f38c69d7291ae4ac67f7b96ed91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135463"
---
# <a name="integrating-the-info-center-view-feature"></a>Integrieren des Infocenter-Ansichtsfeatures

Windows Media Player können Benutzer das Feature Infocenteransicht öffnen und schließen. Infocenteransicht ist das Feature, mit dem Benutzer umfangreiche, erweiterte Informationen zu bestimmten digitalen Medieninhalten erwarten. Wenn der Benutzer die Infocenteransicht öffnet, ruft Windows Media Player im aktuellen Musikspeicher auf, um die Webseite infocenteransicht anzuzeigen, die durch das **URL-Attribut** des **InfoCenter-Elements** des ServiceInfo-Dokuments angegeben wird.

Um Informationen zu den aktuell abspielten digitalen Medieninhalten abzurufen, müssen Sie eine Instanz des Windows Media Player-Steuerelements in Ihre Webseite einbetten und das Player-Objektmodell verwenden. Um beispielsweise den Titel abzurufen, können Sie den folgenden Code JScript verwenden:


```C++
// The control was created with ID = "Player"
var title = Player.currentMedia.getItemInfoByType("Title", "", 0);
```



## <a name="guidelines-for-info-center-view"></a>Richtlinien für die Infocenteransicht

Befolgen Sie beim Erstellen Ihrer Infocenter-Ansichtswebseite die folgenden Richtlinien: 

-   Auf der Seite muss der Onlineshop, der die Informationen enthält, eindeutig identifiziert werden. Sie können dies tun, indem Sie z. B. Ihr Logo an prominenter Stelle anzeigen.
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Vermeiden Sie nach Möglichkeit die Seitennavigation in der Infocenteransicht. Sie sollten für die meisten Aktivitäten zu Ihrem Onlineshop navigieren.
-   Es ist am besten, wertvolle Informationen zur Verfügung zu stellen, ohne dass der Benutzer Programme installieren oder sich bei Ihrem Onlineshop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**External.NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> <dt>

[**InfoCenter-Element**](infocenter-element.md)
</dt> <dt>

[**Allgemeine Informationen zu Onlineshops vom Typ 1 und 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Verwenden des Windows Media Player-Steuerelements auf einer Webseite**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




