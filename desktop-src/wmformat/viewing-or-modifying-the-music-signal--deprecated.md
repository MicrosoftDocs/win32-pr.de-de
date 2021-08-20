---
title: Anzeigen oder Ändern des Musik Signals (veraltet)
description: Anzeigen oder Ändern des Musik Signals (veraltet)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media Format SDK, Microsoft Secure Audio Path (SAP)
- Digital Rights Management (DRM), Microsoft Secure Audio Path (SAP)
- DRM (Digital Rights Management), Microsoft Secure Audio Path (SAP)
- Windows Medienformat-SDK, Sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), Sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), Sicherer Audiopfad (SAP)
- Windows Medienformat-SDK, Musiksignalanzeige oder -änderung
- Digital Rights Management (DRM), Musiksignalanzeige oder -änderung
- DRM (Digital Rights Management), Musiksignalanzeige oder -änderung
- Microsoft Secure Audio Path (SAP), Musiksignalanzeige oder -änderung
- Sicherer Audiopfad (SAP), Musiksignalanzeige oder -änderung
- SAP (Sicherer Audiopfad), Musiksignalanzeige oder -änderung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33f3c30af26cdc8bf2f018ee9487cbab756ab69e01756d810e04a710e7d191da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117844875"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Anzeigen oder Ändern des Musik Signals (veraltet)

Auf dieser Seite wird ein Feature dokumentiert, das in zukünftigen Versionen von mit einer anderen technischen Lösung unterstützt Windows.

Im SAP-Modell (Microsoft Secure Audio Path) können Anwendungen geschützte Musik in irgendeiner Weise ändern. Wenn eine Anwendung beispielsweise versucht, ein Musiksignal abzufangen, klingt das Signal wie zufälliges Rauschen. Daher können Anwendungen, die normalerweise Signale ändern (z. B. ein Equalizer), den Sound der Musik nicht ändern.

Einige Anwendungen zeigen lediglich ein Musiksignal an. Einige Anwendungen zeigen z. B. blinkende Lichtlichter mit dem Musiksignal an, ändern es jedoch nicht. Um Anwendungen zu unterstützen, die Signale anzeigen, wird ein kleiner Teil der Musik entschlüsselt und in klarer Form mit dem verschlüsselten Inhalt übergeben. Das resultierende Signal ist sehr schlecht (schlechter als die Telefonqualität), kann aber für Anwendungen ausreichen, die Signale anzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Sicherer Audiopfad von Microsoft**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




