---
title: Tools für die Entwicklung
description: Tools für die Entwicklung
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Medien Geräte-Manager, Entwicklungstools
- Geräte-Manager,Entwicklungstools
- Windows Medien Geräte-Manager,Zertifikate
- Geräte-Manager, Zertifikate
- Windows Medien Geräte-Manager, Schlüssel
- Geräte-Manager, Schlüssel
- Windows Medien Geräte-Manager,Bibliotheken
- Geräte-Manager,Bibliotheken
- Windows Media Geräte-Manager, Software Development Kit (SDK)
- Geräte-Manager, Software Development Kit (SDK)
- Windows Media Geräte-Manager SDK
- Geräte-Manager SDK
- Windows Media Player Sdk
- Windows Medienformat-SDK
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e517a97246c2bf9b2ac5670a7cf696e714777a2f5926a37e1b2d37ecbe45c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031610"
---
# <a name="tools-for-development"></a>Tools für die Entwicklung

In diesem Abschnitt werden die verschiedenen Zertifikate und Schlüssel, Bibliotheken und SDKs beschrieben, die Sie mithilfe des Windows Media Geräte-Manager SDK programmieren müssen.

Zertifikate und Schlüssel

Das Windows Media Geräte-Manager SDK wird mit einem Testschlüssel-/Zertifikatpaar (in der Datei key.c) ausgeliefert, das von einer Anwendung oder einem Dienstanbieter verwendet werden kann, um Windows Media Geräte-Manager-Methoden für ungeschützte Inhalte zu verwenden. Dieses Schlüssel-Zertifikat-Paar ermöglicht es der Anwendung oder dem Dienstanbieter, den Großteil der Windows Media Geräte-Manager-Funktionalität zu verwenden.

Um jedoch eine Anwendung oder einen Dienstanbieter zu entwickeln, die DRM-geschützte Inhalte verarbeiten können, müssen Sie mindestens ein Zertifikat (jeweils mit einem Schlüssel) von der [Windows Medienlizenzierungsseite](https://www.microsoft.com/licensing/default)anfordern. Zertifikate sind für die folgenden Anwendungen oder Objekte erforderlich:

-   Dienstanbieter, die DRM-geschützte Inhalte verarbeiten, erfordern ein Windows Media Geräte-Manager Service Provider Certificate (und einen Schlüssel)
-   Anwendungen, die DRM-geschützte Inhalte übertragen, erfordern ein Windows Media Geräte-Manager Transfer Certificate (und einen Schlüssel)
-   Anwendungen, die DRM-geschützte Inhalte wiedergeben, erfordern ein DRM-Zertifikat (und einen Schlüssel).
-   Lizenzmessungskomponenten erfordern ein Messungszertifikat. Dies wird von einem Lizenzmessungsdienst bereitgestellt, der auf dem Windows Media Rights Manager SDK basiert und auf der Seite Windows Medienlizenzierung angefordert werden kann.

Bibliotheken und Header

Zusätzlich zu den Bibliotheken und Headern, die in [Erforderliche Bibliotheks- und Headerdateien für eine Anwendung](required-library-and-header-files-for-an-application.md) oder erforderliche Bibliotheken und Header für einen Dienstanbieter erwähnt werden, sollten alle Anwendungen oder Plug-Ins, die zuvor mit WMDRMSDK.lib verknüpft waren, um Windows Medienformat-SDK-Funktionen aufzurufen, jetzt stattdessen mit WMDRMSDKStub.Lib verknüpft werden. [](required-libraries-and-headers-for-a-service-provider.md) Diese Bibliotheksdatei wird verwendet, um auf DRM-geschützte Dateien zuzugreifen. Sie können diese Bibliothek auch auf der Seite Windows Medienlizenzierung anfordern.

Zugehörige SDKs

Die folgenden Microsoft SDKs stellen Elemente bereit, die Sie möglicherweise beim Entwerfen von Lösungen für portable Mediengeräte benötigen.



| SDK erforderlich                     | Erforderlich für...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Geräte-Manager SDK | Desktop-Media Player-Anwendungen, die mit portablen Geräten kommunizieren<br/> Desktopanwendungen, die Dateien oder Informationen mit portablen Geräten austauschen können<br/> Windows Media Player Messung von COM-Objekten<br/> |
| Windows Media Player Sdk         | Windows Media Player-Plug-Ins<br/> Windows Media Player Messung von COM-Objekten<br/> Windows Media Player Skins<br/>                                                                                                   |
| Windows Medienformat-SDK         | Audio- oder Videoplayer, die Dateien erstellen oder wiedergeben können (insbesondere ASF-Dateien)<br/> Anwendungen zur Audio- oder Videobearbeitung<br/>                                                                                               |
| Windows Media Rights Manager SDK | Anwendungen oder Plug-Ins, die die Anzahl der Wiedergaben auf dem Desktop oder Gerät gemessen haben.                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erste Schritte**](getting-started.md)
</dt> </dl>

 

 





