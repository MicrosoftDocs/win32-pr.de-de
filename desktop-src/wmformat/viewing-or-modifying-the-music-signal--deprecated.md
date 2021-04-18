---
title: Anzeigen oder Ändern des Musik Signals (veraltet)
description: Anzeigen oder Ändern des Musik Signals (veraltet)
ms.assetid: 47150951-2ab5-4cbe-ae57-4ebd23943f1d
keywords:
- Windows Media-Format-SDK, Microsoft Secure-Audiopfad (SAP)
- Digital Rights Management (DRM), Microsoft Secure-Audiopfad (SAP)
- DRM (Digital Rights Management), Microsoft Secure-Audiopfad (SAP)
- Windows Media-Format-SDK, sicherer Audiopfad (SAP)
- Digital Rights Management (DRM), sicherer Audiopfad (SAP)
- DRM (Digital Rights Management), sicherer Audiopfad (SAP)
- Windows Media-Format-SDK, anzeigen oder Ändern von Musik Signalen
- Digital Rights Management (DRM), anzeigen oder Ändern von Musik Signalen
- DRM (Digital Rights Management), anzeigen oder Ändern von Musik Signalen
- Microsoft Secure-Audiopfad (SAP), anzeigen oder Ändern von Musik Signalen
- Sicherer Audiopfad (SAP), anzeigen oder Ändern von Musik Signalen
- SAP (sicherer Audiopfad), anzeigen oder Ändern von Musik Signalen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 673038c9769301d2820cd73e4a090b5e4770fc4a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338617"
---
# <a name="viewing-or-modifying-the-music-signal-deprecated"></a>Anzeigen oder Ändern des Musik Signals (veraltet)

Diese Seite dokumentiert eine Funktion, die in zukünftigen Versionen von Windows mit einer anderen technischen Lösung unterstützt wird.

Im Microsoft Secure audiopath (SAP)-Modell können Anwendungen geschützte Musik in keiner Weise ändern. Wenn eine Anwendung z. b. versucht, ein Musiksignal abzufangen, klingt das Signal wie zufälliges Rauschen. Folglich können Anwendungen, die in der Regel Signale ändern (z. b. ein Equalizer), den Sound der Musik nicht ändern.

Bei einigen Anwendungen wird lediglich ein Musiksignal angezeigt. Beispielsweise zeigen einige Anwendungen blinkende Beleuchtung rechtzeitig mit dem Musiksignal an, aber ändern Sie Sie nicht. Um Anwendungen, die Signale anzeigen, zu unterstützen, wird ein kleiner Teil der Musik entschlüsselt und als Klartext mit dem verschlüsselten Inhalt übermittelt. Das resultierende Signal ist sehr schlecht (schlimmer als die Telefonqualität), kann aber für Anwendungen, die Signale anzeigen, ausreichen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Microsoft Secure-Audiopfad**](microsoft-secure-audio-path--deprecated.md)
</dt> </dl>

 

 




