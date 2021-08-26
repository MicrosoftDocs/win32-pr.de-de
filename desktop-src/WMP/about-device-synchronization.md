---
title: Informationen zur Gerätesynchronisierung
description: Informationen zur Gerätesynchronisierung
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player,Synchronisieren von Geräten
- Windows Media Player Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX,Synchronisieren von Geräten
- ActiveX,Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX,Synchronisieren von Geräten
- Windows Media Player Mobil,Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen
- Gerätesynchronisierung, Informationen
- Synchronisieren von Geräten, manuelle Übertragung
- Gerätesynchronisierung, manuelle Übertragung
- Synchronisieren von Geräten, automatische Synchronisierung
- Gerätesynchronisierung, automatische Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed6a03781121a58bee36fd9ff1f74bf21a85347f81384f30c2db5afb4ef3e1f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903560"
---
# <a name="about-device-synchronization"></a>Informationen zur Gerätesynchronisierung

Windows Media Player 10 wurde ein neues Modell für die Synchronisierung digitaler Medieninhalte mit portablen Geräten eingeführt. Aus Sicht des Benutzers bedeutet dies, dass Sie angeben können, welche Wiedergabelisten (einschließlich automatischer Wiedergabelisten) automatisch mit Geräten synchronisiert werden. Sie können digitale Medieninhalte auch manuell auf Geräte übertragen. Aus Sicht des Entwicklers bedeutet dies, dass neue Funktionen verfügbar gemacht werden, die Sie in Ihren Anwendungen nutzen können. Hierzu müssen Sie eine Remoteinstanz des -Steuerelements Windows Media Player erstellen.

Es gibt zwei Möglichkeiten, wie ein Benutzer digitale Medieninhalte auf ein Gerät kopieren kann:

-   **Manuelle Übertragung.** Der Benutzer wählt digitale Medieninhalte in der Bibliothek aus und initiiert dann eine Übertragung des Inhalts auf das Gerät. Dies ähnelt der Funktionalität, die von früheren Versionen von bereitgestellt Windows Media Player. Das Windows Media Player SDK bietet keine Methoden zum Übertragen digitaler Medien auf ein Gerät.
-   **Automatische Synchronisierung.** Der Benutzer gibt Wiedergabelisten an, die automatisch mit dem Gerät synchronisiert werden. Dies ist ein Feature von Windows Media Player 10 oder höher. Das Windows Media Player SDK bietet Funktionen zum Verwalten der automatischen Synchronisierung. Diese Funktionalität ist so konzipiert, dass Sie eine benutzerdefinierte Benutzeroberfläche für Ihre Anwendung erstellen können, um anzugeben, wie die Gerätesynchronisierung erfolgt, und um Benutzern Statusinformationen zur Verfügung zu stellen.

Damit die automatische Synchronisierung funktioniert, muss eine besondere Beziehung zwischen dem Windows Media Player und dem Gerät eingerichtet werden. Diese Beziehung wird als Partnerschaft *bezeichnet.*

Die folgenden Abschnitte enthalten weitere Informationen zur Gerätesynchronisierung.

-   [Informationen zu Geräten](about-devices.md)
-   [Informationen zu Partnerschaften](about-partnerships.md)
-   [Informationen zur Synchronisierungs-Engine](about-the-synchronization-engine.md)
-   [Informationen zur Wiedergabelistensynchronisierung](about-playlist-synchronization.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Arbeiten mit portablen Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




