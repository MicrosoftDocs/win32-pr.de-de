---
title: Integration von Albuminformationen
description: Integration von Albuminformationen
ms.assetid: c59c0c1b-eddc-4061-87cc-a5c44ae0c15d
keywords:
- Windows Media Player Online Stores,Integration von Albuminformationen
- Onlineshops, Integration von Albuminformationen
- Typ 2 Onlineshops,Integration von Albuminformationen
- Windows Media Player online stores,integrating album info
- Onlineshops,Integration von Albuminformationen
- Typ 2 Onlineshops,Integration von Albuminformationen
- Windows Media Player,Integration von Albuminformationen
- Windows Media Player,Integration von Albuminformationen
- Integration von Albuminformationen
- Integrieren von Albuminformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcdd8c0c200d0d1779ecc9d4f90da3f3755f276431792f7a6b6450dd43e51cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055428"
---
# <a name="album-info-integration"></a>Integration von Albuminformationen

Windows Media Player können Benutzer detaillierte Informationen über die CD oder DVD anfordern, von der digitale Medieninhalte stammen, indem sie auf eine Schaltfläche klicken, z. B. **Weitere Informationen.** Wenn der Benutzer auf die Schaltfläche klickt, ruft Windows Media Player 10 oder höher im aktuellen Musikspeicher auf, um die Albumdetails anzuzeigen. In diesem Fall öffnet der Player den Bereich mit den Albuminformationen und zeigt die Webseite an, die durch das **URL-Attribut** des **AlbumInfo-Elements** des ServiceInfo-Dokuments angegeben wird.

Windows Media Player fügt eine Abfragezeichenfolge an die URL an, um dem Onlineshop Informationen zu dem vom Benutzer angeforderten Inhalt zur Verfügung zu stellen. Die Abfragezeichenfolge enthält Attribute wie **Title**, **Album** und **Interpret**, die der Onlineshop verwenden kann, um das richtige anzuzeigende Album zu bestimmen. Die Referenzdokumentation für das **AlbumInfo-Element** enthält die vollständige Liste der Abfragezeichenfolgenattribute und deren Beschreibungen.

## <a name="guidelines-for-album-info"></a>Richtlinien für Albuminformationen

Befolgen Sie beim Erstellen Ihrer Webseite mit Den Albuminformationen die folgenden Richtlinien:

-   Auf der Seite muss der Onlineshop, der die Informationen enthält, eindeutig identifiziert werden. Sie können dies tun, indem Sie z. B. Ihr Logo an prominenter Stelle anzeigen.
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Vermeiden Sie nach Möglichkeit die Seitennavigation innerhalb der Funktion für Albuminformationen. Sie sollten für die meisten Aktivitäten zu Ihrem Onlineshop navigieren.
-   Es wird empfohlen, wertvolle Informationen zur Verfügung zu stellen, ohne dass der Benutzer Programme installieren oder sich bei Ihrem Onlineshop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 2**](about-type-2-online-stores.md)
</dt> <dt>

[**AlbumInfo-Element**](albuminfo-element.md)
</dt> </dl>

 

 




