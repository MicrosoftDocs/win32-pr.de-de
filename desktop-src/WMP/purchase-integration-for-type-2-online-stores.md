---
title: Kauf Integration für den Typ 2-Online Speicher
description: Kauf Integration für den Typ 2-Online Speicher
ms.assetid: aedaa6a0-d559-44b7-9c14-2abf44478b1c
keywords:
- Windows Media Player Online Stores, Kauf Integration
- Online Stores, Kauf Integration
- Typ 2 Online Stores, Kauf Integration
- Windows Media Player Online Stores, integrieren von Käufen
- Online Stores, integrieren von Käufen
- Typ 2 Online Stores, integrieren von Käufen
- Windows Media Player, Kauf Integration
- Windows Media Player, integrieren von Käufen
- Kauf Integration
- Integrieren von Käufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3d8fb56b286b66de12bb59412e7f9077eb398f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338398"
---
# <a name="purchase-integration-for-type-2-online-stores"></a>Kauf Integration für den Typ 2-Online Speicher

Wenn Windows Media Player Inhalt digitaler Medien wieder gibt oder der Benutzer die **Suche nach Album Informationen** auswählt, bietet der Player dem Benutzer einen Link, um die CD oder DVD zu kaufen, von der der Inhalt stammt, wenn ein solcher Link verfügbar ist. Wenn der Benutzer auf den Link klickt, ruft Windows Media Player 10 oder höher den aktuellen Musikspeicher auf, um die Kauf Anforderung zu verarbeiten. In diesem Fall navigiert der Player zum ersten Dienstaufgaben Bereich (in Windows Media Player 10) oder der Registerkarte "Online Stores" (in Windows Media Player 11) und zeigt die Webseite an, die vom Attribut " **mediaplayerurl** " des Elements " **buycd** " des serviceInfo-Dokuments angegeben wird. (Die Attribute " **mediacenterurl** " und " **browserurl** " werden auf ähnliche Weise verwendet, um Aufrufe von Windows XP Media Center Edition 2004 und Windows XP Service Pack 2) zu verarbeiten.

Windows Media Player Fügt eine Abfrage Zeichenfolge an die URL an, um dem Online Shop Informationen zu den Inhalten bereitzustellen, die der Benutzer erworben hat. Die Abfrage Zeichenfolge enthält Attribute wie " **Title**", " **Album**" und " **Artist**", die der Online Shop zum Ermitteln des richtigen zu verkaufenden Albums verwenden kann. Die Referenz Dokumentation für das **buycd** -Element enthält die komplette Liste der Attribute der Abfrage Zeichenfolge und deren Beschreibungen.

## <a name="guidelines-for-the-buycd-page"></a>Richtlinien für die Seite "buycd"

Verwenden Sie beim Erstellen der Webseite für die buycd die folgenden Richtlinien:

-   Die Seite muss den Online Store, der die Informationen bereitstellt, eindeutig identifizieren. Dies ist möglich, indem Sie Ihr Logo hervorgehoben anzeigen, z. b..
-   Die Seite muss einen Link zu den Datenschutzbestimmungen Ihres Unternehmens enthalten.
-   Es empfiehlt sich, anfängliche Kauf Informationen bereitzustellen, ohne dass der Benutzer Programme installieren oder sich beim Online Shop anmelden muss.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu Typ 2 Online Stores**](about-type-2-online-stores.md)
</dt> <dt>

[**Buycd-Element**](buycd-element.md)
</dt> </dl>

 

 




