---
title: Komponenten von EAPHost
description: Erfahren Sie mehr über die drei Komponenten der EAPHost-Authentifizierung. Anzeigen zusätzlicher verfügbarer Ressourcen für die Verwendung der EAPHost-Authentifizierung.
ms.assetid: f875c3f8-d2fb-461e-b356-e1b2ccaf9981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ede2fc6a705ec77fe982778239a92c7ffb10ef9
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104474261"
---
# <a name="components-of-eaphost"></a>Komponenten von EAPHost

In diesem Thema werden die drei Komponenten der EAPHost-Authentifizierung beschrieben.

## <a name="eaphost-components"></a>EAPHost-Komponenten

Die EAPHost-Authentifizierung verfügt über die folgenden drei Komponenten:

-   Der Supplicant, der die Authentifizierungsanforderungen übernimmt.
-   Die EAP-Methoden des Peer (oder Clients), die die spezifischen EAP-Methoden implementieren und die Authentifizierungs Sitzung auf Clientseite verwalten.
-   Die EAP-Methoden des Authenticator (oder des Servers), die die Serverseite des EAP-Protokolls implementieren.

Die Supplicant-APIs werden direkt von einer Anwendung aufgerufen, die über EAPHost authentifiziert werden soll. Dabei handelt es sich jedoch um Funktionsprototypen, die für einen bestimmten EAP-Authentifizierungstyp implementiert werden müssen, z. b. das Microsoft Challenge Handshake Authentication-Protokoll, Version 2,0 (MS-CHAPv2).

Wenn Sie eine Anwendung erstellen, die EAPHost für die Authentifizierung verwendet, lesen Sie die API-Referenz für den [EAPHost-Supplicant](eap-host-supplicant-api-reference.md).

Wenn Sie eine neue EAP-Authentifizierungsmethode erstellen, die von EAPHost verwaltet werden soll, lesen Sie die API-Referenz für die [EAPHost-Peer Methode](eap-host-peer-method-api-reference.md) und die [APIs der EAPHost-Authenticator-Methode](eaphost-authenticator-method-apis.md). Beachten Sie, dass Sie Implementierungen dieser APIs erstellen, die in einer neuen DLL verfügbar gemacht werden, die EAPHost lädt, anstatt Sie direkt Aufrufs auszuführen.

 

 




