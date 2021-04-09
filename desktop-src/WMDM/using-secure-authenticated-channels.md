---
title: Verwenden sicherer authentifizierter Kanäle
description: Verwenden sicherer authentifizierter Kanäle
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Media-Device Manager, Authentifizierung
- Device Manager, Authentifizierung
- Desktop Anwendungen, Authentifizierung
- Dienstanbieter, Authentifizierung
- Programmier Handbuch, Authentifizierung
- authentication
- Windows Media Device Manager, sichere Kommunikation
- Device Manager, sichere Kommunikation
- Desktop Anwendungen, sichere Kommunikation
- Dienstanbieter, sichere Kommunikation
- Programmier Handbuch, sichere Kommunikation
- sichere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88c271cecc2e9252a3f7af0540beef3dc57d2b9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036591"
---
# <a name="using-secure-authenticated-channels"></a>Verwenden sicherer authentifizierter Kanäle

Windows Media Device Manager ermöglicht die Authentifizierung und die sichere Kommunikation zwischen Komponenten durch Bereitstellung von zwei Hilfsklassen, [csecurechannelclient](csecurechannelclient-class.md) (für Anwendungen) und [csecurechannelserver](csecurechannelserver-class.md) (für Dienstanbieter) und einer Schnittstelle, [**icomponentauthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (für beides). Zusammen bilden diese eine API für die Verwendung von Secure authentifiziert Channels (SAC). SAC verarbeitet die folgenden drei Aufgaben für Dienstanbieter oder Anwendungen, die Windows Media Device Manager verwenden:

-   [Komponenten Authentifizierung](component-authentication.md)
-   [Verschlüsselung und Entschlüsselung](encryption-and-decryption.md)
-   [Nachrichten Authentifizierung](message-authentication.md)

Eine Anwendung oder ein Dienstanbieter muss die Komponenten Authentifizierung, Verschlüsselung und Entschlüsselung verarbeiten. die Nachrichten Authentifizierung ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




