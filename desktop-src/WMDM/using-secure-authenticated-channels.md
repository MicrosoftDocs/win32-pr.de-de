---
title: Verwenden von sicheren authentifizierten Kanälen
description: Verwenden von sicheren authentifizierten Kanälen
ms.assetid: ca4ab93c-0a3e-4fb5-be7f-a8f4eea3c9b7
keywords:
- Windows Medien Geräte-Manager,Authentifizierung
- Geräte-Manager,Authentifizierung
- Desktopanwendungen,Authentifizierung
- Dienstanbieter,Authentifizierung
- Programmierhandbuch,Authentifizierung
- authentication
- Windows Medien Geräte-Manager,sichere Kommunikation
- Geräte-Manager,sichere Kommunikation
- Desktopanwendungen,sichere Kommunikation
- Dienstanbieter,sichere Kommunikation
- Programmierhandbuch,sichere Kommunikation
- Sichere Kommunikation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37a86eb364baca933eea1c81e587f99c9381786c5c3f62f2cefcfe3ceaed6e51
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124110"
---
# <a name="using-secure-authenticated-channels"></a>Verwenden von sicheren authentifizierten Kanälen

Windows Media Geräte-Manager ermöglicht die Authentifizierung und sichere Kommunikation zwischen Komponenten, indem zwei Hilfsklassen bereitgestellt werden: [CSecureChannelClient](csecurechannelclient-class.md) (für Anwendungen) und [CSecureChannelServer](csecurechannelserver-class.md) (für Dienstanbieter) und eine Schnittstelle, [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) (für beide). Zusammen stellen diese eine API für die Verwendung von sicheren authentifizierten Kanälen (SECURE Authenticated Channels, SAC) zusammen. SAC verarbeitet die folgenden drei Aufgaben für Dienstanbieter oder Anwendungen, die Windows Media Geräte-Manager:

-   [Komponentenauthentifizierung](component-authentication.md)
-   [Verschlüsselung und Entschlüsselung](encryption-and-decryption.md)
-   [Nachrichtenauthentifizierung](message-authentication.md)

Eine Anwendung oder ein Dienstanbieter muss die Komponentenauthentifizierung, -verschlüsselung und -entschlüsselung verarbeiten. Die Nachrichtenauthentifizierung ist optional.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Allgemeine Aufgaben für Anwendungen und Dienstanbieter**](tasks-common-to-applications-and-service-providers.md)
</dt> </dl>

 

 




