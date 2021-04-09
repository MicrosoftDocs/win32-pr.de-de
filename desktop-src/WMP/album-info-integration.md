---
title: Integration von Album Informationen
description: Integration von Album Informationen
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online Stores, Integration von Albuminformationen
- Online Stores, Integration von Album-Informationen
- Typ 2 Online Stores, Integration von Albuminformationen
- Windows Media Player Online Stores, integrieren von Albuminformationen
- Online Stores, integrieren von Albuminformationen
- Typ 2 Online Stores, integrieren von Albuminformationen
- Windows Media Player, integrieren von Albuminformationen
- Windows Media Player, Integration von Albuminformationen
- Integration von Albuminformationen
- Integrieren von Albuminformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b03586217ec0a0eebd9abd0a9acae62790f838f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036881"
---
# <a name="album-info-integration"></a>Integration von Album Informationen

Windows Media Player ermöglicht es Benutzern, ausführliche Informationen über die CD oder DVD anzufordern, von denen aus Inhalte für digitale Medien stammen, indem Sie auf eine Schaltfläche klicken, z. b. **Weitere Informationen**. Wenn der Benutzer auf die Schaltfläche klickt, ruft Windows Media Player 10 oder höher im aktuellen Musikspeicher auf, um die Details zum Album anzuzeigen. Wenn dies der Fall ist, öffnet der Spieler den Bereich "Informationen zum Album" und zeigt die Webseite an, die vom Attribut " **URL** " des Elements " **Albuminfo** " des serviceInfo-Dokuments angegeben wird.

Windows Media Player Fügt eine Abfrage Zeichenfolge an die URL an, um dem Onlinespeicher Informationen über den vom Benutzer angeforderten Inhalt bereitzustellen. Die Abfrage Zeichenfolge enthält Attribute wie " **Title**", " **Album**" und " **Artist**", mit denen der Online Shop das richtige Album zum Anzeigen bestimmen kann. Die Referenz Dokumentation für das Element " **Albuminfo** " enthält die komplette Liste der Attribute der Abfrage Zeichenfolge und deren Beschreibungen.

## <a name="guidelines-for-album-info"></a>Richtlinien für die Album Informationen

Beachten Sie beim Erstellen der Webseite mit den Albuminformationen die folgenden Richtlinien:

-   Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren. Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Vermeiden Sie die Seitennavigation innerhalb der Album Informationsfunktion, wenn dies möglich ist. Für die meisten Aktivitäten sollten Sie zu Ihrem Online Store navigieren.
-   Es wird empfohlen, dass Sie wertvolle Informationen bereitstellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 2 Online Stores**](about-type-2-online-stores.md)
</dt> <dt>

[**Albuminfo-Element**](albuminfo-element.md)
</dt> </dl>

 

 




