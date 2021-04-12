---
title: Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"
description: Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"
ms.assetid: dec88d72-718c-42ab-8d48-eddf906051ef
keywords:
- Windows Media-Format-SDK, Windows Media DRM 10 für Netzwerkgeräte
- Windows Media-Format-SDK, DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), Windows Media DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), Windows Media DRM 10 für Netzwerkgeräte
- Advanced Systems Format (ASF), DRM 10 für Netzwerkgeräte
- ASF (Advanced Systems Format), DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), Windows Media DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), Windows Media DRM 10 für Netzwerkgeräte
- Digital Rights Management (DRM), DRM 10 für Netzwerkgeräte
- DRM (Digital Rights Management), DRM 10 für Netzwerkgeräte
- Windows Media DRM 10 für Netzwerkgeräte, Protokolle
- DRM 10 für Netzwerkgeräte, Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73908c66dbffe7f50f4f28beb520861611d59962
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309887"
---
# <a name="using-the-windows-media-drm-10-for-network-devices-protocol"></a>Verwenden des Protokolls "Windows Media DRM 10 for Network Devices"

Das Windows Media-Format SDK bietet einige Features zur Unterstützung des sicheren Netzwerkgeräte Protokolls, Windows Media DRM 10 für Netzwerkgeräte. Dieses Protokoll definiert die Nachrichten, die zwischen einem digitalen Medienwiedergabe Gerät (z. b. einem Top-Video Player) und dem Computer, der Daten für das Gerät bedient, gesendet werden. Die zwischen dem Server und dem Gerät gesendeten Mediendaten werden verschlüsselt, um Sie vor dem abfangen zu schützen.

Die Kommunikation zwischen Ihrer Anwendung und Geräten, die Windows Media DRM 10 für Netzwerkgeräte unterstützen, kann alle von Ihnen bevorzugten Netzwerkprotokolle verwenden. Das Windows Media-Format-SDK stellt keine Objekte bereit, die die Netzwerkkommunikation für Sie ausführen. Stattdessen verarbeiten die Objekte dieses SDK einige Windows Media DRM 10 für Netzwerkgeräte Nachrichten, nachdem Sie von Ihrer Anwendung empfangen wurden.

Zu den Features, die Windows Media DRM 10 für Netzwerkgeräte unterstützen, gehören die Geräteregistrierung, die Near-Erkennung und die Typumwandlung von DRM-geschützten Dateien Diese Features werden in den folgenden Abschnitten beschrieben.



| `Section`                                                                                                                                                                          | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [Geräteregistrierung](device-registration.md)                                                                                                                                   | Beschreibt, wie Registrierungs Anforderungs Nachrichten von Geräten verarbeitet werden.                                                                       |
| [Ausführen der Near-Erkennung](performing-proximity-detection.md)                                                                                                             | Beschreibt den Prozess der Near-Erkennung.                                                                                                 |
| [Wandeln Sie eine DRM-Protected Datei in eine Windows Media DRM 10 for Network Devices Stream-Datei um.](converting-a-drm-protected-file-to-a-windows-media-drm-10-for-network-devices-stream.md) | Beschreibt, wie eine DRM-geschützte Datei in einen Stream konvertiert wird, der an ein Gerät gesendet werden kann, das Windows Media DRM 10 für Netzwerkgeräte verwendet. |



 

> [!Note]  
> DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 




