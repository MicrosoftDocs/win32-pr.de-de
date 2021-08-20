---
title: Komponenten von EAPHost
description: Erfahren Sie mehr über die drei Komponenten der EAPHost-Authentifizierung. Zeigen Sie zusätzliche verfügbare Ressourcen für die Verwendung der EAPHost-Authentifizierung an.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9aa86f09473b14df6dbcc8bbc667dc4a1cc1badf9e0b6dd67ac95f8d11f2bae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118086414"
---
# <a name="components-of-eaphost"></a>Komponenten von EAPHost

In diesem Thema werden die drei Komponenten der EAPHost-Authentifizierung beschrieben.

## <a name="eaphost-components"></a>EAPHost-Komponenten

Die EAPHost-Authentifizierung verfügt über die folgenden drei Komponenten.

-   Der Supplicant, der die Authentifizierungsanforderungen stellt.
-   Die Peer- (oder Client-) EAP-Methoden, die die spezifischen EAP-Methoden implementieren und die Authentifizierungssitzung auf clientseitiger Seite verwalten.
-   Die Authentator-EAP-Methoden (oder Servermethoden), die die Serverseite des EAP-Protokolls implementieren.

Die supplicant-APIs werden direkt von einer Anwendung aufgerufen, die sich über EAPHost authentifizieren möchte. Die Peermethode und die Authentisierungsmethoden-APIs sind jedoch Funktionsprototypen, die für einen bestimmten EAP-Authentifizierungsmethodentyp implementiert werden müssen, z. B. Microsoft Challenge Handshake Authentication Protocol Version 2.0 (MS-CHAPv2).

Wenn Sie eine Anwendung erstellen, die EAPHost für die Authentifizierung verwendet, lesen Sie die [EAPHost Supplicant-API-Referenz](eap-host-supplicant-api-reference.md).

Wenn Sie eine neue EAP-Authentifizierungsmethode erstellen, die von EAPHost verwaltet werden soll, lesen Sie die API-Referenz für die [EAPHost-Peermethode](eap-host-peer-method-api-reference.md) und die [EAPHost Authenticator-Methoden-APIs.](eaphost-authenticator-method-apis.md) Beachten Sie, dass Sie Implementierungen dieser APIs erstellen, die in einer neuen DLL verfügbar gemacht werden, die EAPHost lädt, anstatt sie direkt auf aufruft.

 

 




