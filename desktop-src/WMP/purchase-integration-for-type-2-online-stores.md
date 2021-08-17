---
title: Integration des Kaufs für Onlineshops vom Typ 2
description: Integration des Kaufs für Onlineshops vom Typ 2
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Onlineshops,Integration des Kaufs
- Onlineshops,Integration des Kaufs
- 'Typ 2: Onlineshops,Integration des Kaufs'
- Windows Media Player Onlineshops,Integration von Käufen
- Onlineshops,Integrieren von Käufen
- 'Typ 2: Onlineshops,Integrieren von Käufen'
- Windows Media Player,Integration des Kaufs
- Windows Media Player,Integrieren von Käufen
- Integration des Kaufs
- Integrieren von Käufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d854ecfd91cd0a887c242ad743874a6ec1a469ebcca3aa788bf57c2c59041d6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746694"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Integration des Kaufs für Onlineshops vom Typ 2

Wenn Windows Media Player Digitale Medieninhalte wieder gibt oder der Benutzer Albuminformationen suchen auswählt, bietet der Player dem Benutzer einen Link zum Kauf der CD oder DVD, von der der Inhalt stammt, wenn ein solcher Link verfügbar ist. Wenn der Benutzer auf den Link klickt, Windows Media Player 10 oder höher aufruft den aktuellen Musikspeicher, um die Kaufanforderung zu verarbeiten. In diesem Fall navigiert der Player zum ersten Dienst-Aufgabenbereich (in Windows Media Player 10) oder zur Registerkarte Onlineshops (in Windows Media Player 11) und zeigt die Webseite an, die durch das **MediaPlayerURL-Attribut** des **BuyCD-Elements** des ServiceInfo-Dokuments angegeben wird. (Die **Attribute MediaCenterURL** und **BrowserURL** werden auf ähnliche Weise verwendet, um Aufrufe von Windows XP Media Center Edition 2004 und Windows XP Service Pack 2) zu verarbeiten.

Windows Media Player fügt eine Abfragezeichenfolge an die URL an, um dem Onlineshop Informationen zu dem Inhalt zur Verfügung zu stellen, den der Benutzer kaufen wollte. Die Abfragezeichenfolge enthält Attribute wie **Title**, **Album** und **Interpret**, die der Onlineshop verwenden kann, um das richtige zu verkaufende Album zu bestimmen. Die Referenzdokumentation für das **BuyCD-Element** enthält die vollständige Liste der Abfragezeichenfolgenattribute und deren Beschreibungen.

## <a name="guidelines-for-the-buycd-page"></a>Richtlinien für die BuyCD-Seite

Wenn Sie Ihre BuyCD-Webseite erstellen, befolgen Sie die folgenden Richtlinien:

-   Auf der Seite muss der Onlineshop, der die Informationen enthält, eindeutig identifiziert werden. Sie können dies tun, indem Sie z. B. Ihr Logo an prominenter Stelle anzeigen.
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Es ist am besten, anfängliche Kaufinformationen zu liefern, ohne dass der Benutzer Programme installieren oder sich bei Ihrem Onlineshop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Onlineshops vom Typ 2**](about-type-2-online-stores.md)
</dt> <dt>

[**BuyCD-Element**](buycd-element.md)
</dt> </dl>

 

 




