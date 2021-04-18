---
title: Informationen zur Geräte Synchronisierung
description: Informationen zur Geräte Synchronisierung
ms.assetid: 87976357-f819-41ac-9645-36e799876881
keywords:
- Windows Media Player, Synchronisieren von Geräten
- Windows Media Player-Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX-Steuerelement, Synchronisieren von Geräten
- ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile, Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen zu
- Geräte Synchronisierung, Informationen zu
- Synchronisieren von Geräten, manuelle Übertragung
- Geräte Synchronisierung, manuelle Übertragung
- Synchronisieren von Geräten, automatische Synchronisierung
- Geräte Synchronisierung, automatische Synchronisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ad6b6526698def2f7d58ec7afc04c8e22e89c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340617"
---
# <a name="about-device-synchronization"></a>Informationen zur Geräte Synchronisierung

In Windows Media Player 10 wurde ein neues Modell für die Synchronisierung von Inhalten digitaler Medien mit tragbaren Geräten eingeführt. Aus Sicht des Benutzers bedeutet dies, dass Sie angeben können, welche Wiedergabelisten (einschließlich automatischer Wiedergabelisten) automatisch mit Geräten synchronisiert werden sollen. Sie können auch den Inhalt digitaler Medien manuell auf Geräte übertragen. Aus Sicht des Entwicklers bedeutet dies, dass neue Funktionen verfügbar gemacht werden, die Sie in Ihren Anwendungen nutzen können. Zu diesem Zweck müssen Sie eine Remote Instanz des Windows Media Player-Steuer Elements erstellen.

Es gibt zwei Möglichkeiten, wie ein Benutzer Digital Media-Inhalte auf ein Gerät kopieren kann:

-   **Manuelle Übertragung.** Der Benutzer wählt den Inhalt digitaler Medien in der Bibliothek aus und initiiert dann eine Übertragung des Inhalts auf das Gerät. Dies ist vergleichbar mit der Funktionalität, die in früheren Versionen von Windows Media Player bereitgestellt wurde. Das Windows Media Player SDK bietet keine Methoden zum Übertragen digitaler Medien auf ein Gerät.
-   **Automatische Synchronisierung.** Der Benutzer gibt Wiedergabelisten an, die automatisch mit dem Gerät synchronisiert werden. Dies ist ein Feature von Windows Media Player 10 oder höher. Das Windows Media Player SDK bietet Funktionen zum Verwalten der automatischen Synchronisierung. Mit dieser Funktion können Sie eine benutzerdefinierte Benutzeroberfläche für Ihre Anwendung erstellen, um anzugeben, wie die Geräte Synchronisierung durchgeführt wird, und um den Benutzern Statusinformationen bereitzustellen.

Damit die automatische Synchronisierung funktioniert, muss zwischen Windows Media Player und dem Gerät eine besondere Beziehung hergestellt werden. Diese Beziehung wird als *Partnerschaft* bezeichnet.

In den folgenden Abschnitten finden Sie weitere Informationen zur Geräte Synchronisierung.

-   [Informationen zu Geräten](about-devices.md)
-   [Informationen zu Partnerschaften](about-partnerships.md)
-   [Informationen zur Synchronisierungs-Engine](about-the-synchronization-engine.md)
-   [Informationen zur Wiedergabeliste](about-playlist-synchronization.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zum Player-Objektmodell**](about-the-player-object-model.md)
</dt> <dt>

[**Remoting des Windows Media Player-Steuerelements**](remoting-the-windows-media-player-control.md)
</dt> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




