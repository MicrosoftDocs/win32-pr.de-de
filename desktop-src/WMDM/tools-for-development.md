---
title: Tools für die Entwicklung
description: Tools für die Entwicklung
ms.assetid: 7932f599-a073-4fc8-82da-c0e7001c1809
keywords:
- Windows Media Device Manager, Entwicklungs Tools
- Device Manager, Entwicklungs Tools
- Windows Media Device Manager, Zertifikate
- Device Manager, Zertifikate
- Windows Media-Device Manager, Schlüssel
- Device Manager, Schlüssel
- Windows Media-Device Manager, Bibliotheken
- Device Manager, Bibliotheken
- Windows Media Device Manager, Software Development Kit (SDK)
- Device Manager, Software Development Kit (SDK)
- Windows Media Device Manager SDK
- Device Manager SDK
- Windows Media Player SDK
- SDK für Windows Media-Format
- Windows Media Rights Manager SDK
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45a3e419b87c56a447ad2412234a80432b1598e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "106340288"
---
# <a name="tools-for-development"></a>Tools für die Entwicklung

In diesem Abschnitt werden die verschiedenen Zertifikate und Schlüssel, Bibliotheken und SDKs beschrieben, die Sie zum Programmieren mit dem Windows Media Device Manager SDK benötigen.

Zertifikate und Schlüssel

Das Windows Media Device Manager SDK wird mit einem Testschlüssel/-Zertifikat Paar (in der Key. c-Datei) ausgeliefert, das von einer Anwendung oder einem Dienstanbieter verwendet werden kann, um Windows Media Device Manager-Methoden für ungeschützten Inhalt zu verwenden. Mit diesem Schlüssel-/zertifikatpaar kann die Anwendung oder der Dienstanbieter den größten Teil der Windows Media Device Manager-Funktionalität nutzen.

Wenn Sie jedoch eine Anwendung oder einen Dienstanbieter entwickeln möchten, die von DRM-geschützten Inhalten verarbeitet werden kann, müssen Sie ein oder mehrere Zertifikate (jedes mit einem Schlüssel) von der [Windows Media Licensing-Seite](https://www.microsoft.com/licensing/default)anfordern. Für die folgenden Anwendungen oder Objekte sind Zertifikate erforderlich:

-   Dienstanbieter, die von DRM geschützten Inhalten verarbeiten, benötigen ein Windows Media Device Manager-Dienstanbieter Zertifikat (und einen Schlüssel).
-   Anwendungen, die DRM-geschützten Inhalt übertragen, benötigen ein Windows Media Device Manager Transfer Certificate (und einen Schlüssel)
-   Anwendungen, die DRM-geschützten Inhalt abspielen, benötigen ein DRM-Zertifikat (und einen Schlüssel).
-   Für Lizenz Messungs Komponenten ist ein Messungs Zertifikat erforderlich. Diese wird von einem Lizenz Messungs Dienst bereitgestellt, der auf dem Windows Media Rights Manager SDK basiert und auf der Seite Windows Media-Lizenzierung angefordert werden kann.

Bibliotheken und Header

Zusätzlich zu den Bibliotheken und Headern, die in [erforderlichen Bibliotheks-und Header Dateien für eine Anwendung](required-library-and-header-files-for-an-application.md) oder [erforderliche Bibliotheken und Header für einen Dienstanbieter](required-libraries-and-headers-for-a-service-provider.md)erwähnt wurden, sollten alle Anwendungen und Plug-ins, die zuvor mit wmdrmsdk. lib verknüpft waren, um die Windows Media-Format-SDK-Funktionen aufzurufen, jetzt mit wmdrmsdkstub. lib verknüpfen. Diese Bibliotheksdatei wird verwendet, um auf von DRM geschützte Dateien zuzugreifen. Sie können diese Bibliothek auch auf der Seite Windows Media-Lizenzierung anfordern.

Verwandte sdche

Die folgenden Microsoft sdert stellen Elemente bereit, die Sie möglicherweise beim Entwerfen von Lösungen für tragbare Mediengeräte benötigen.



| SDK erforderlich                     | Erforderlich für...                                                                                                                                                                                                                       |
|----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Media Device Manager SDK | Desktop Media Player-Anwendungen, die mit tragbaren Geräten kommunizieren<br/> Desktop Anwendungen, die Dateien oder Informationen mit tragbaren Geräten austauschen können<br/> Windows Media Player Messungs-com-Objekte<br/> |
| Windows Media Player SDK         | Windows Media Player-Plug-ins<br/> Windows Media Player Messungs-com-Objekte<br/> Windows Media Player Skins<br/>                                                                                                   |
| SDK für Windows Media-Format         | Audio-oder Video Player, die Dateien erstellen oder wiedergeben können (vor allem bei ASF-Dateien)<br/> Anwendungen für die Audiobearbeitung oder Videobearbeitung<br/>                                                                                               |
| Windows Media Rights Manager SDK | Anwendungen und Plug-ins, die die Anzahl von spielen Messen, werden auf dem Desktop oder Gerät angezeigt.                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Einstieg**](getting-started.md)
</dt> </dl>

 

 





