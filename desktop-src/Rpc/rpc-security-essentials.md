---
title: Grundlagen zu RPC
description: Um einen Remote Prozedur aufzurufen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856767"
---
# <a name="rpc-security-essentials"></a>Grundlagen zu RPC

Um einen Remote Prozedur aufzurufen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen. Weitere Informationen zu Bindungen finden Sie unter [Bindung und Handles](binding-and-handles.md). Um einen sicheren Remote Prozedur aufzurufen, sind zusätzliche Schritte erforderlich. Zuerst muss der Server einen Sicherheitsanbieter (Authentifizierungsdienst in der DCE-Terminologie) auswählen. Anschließend muss er sich für den Authentifizierungsmechanismus entscheiden. Danach erhält der Client eine Bindung an den Server und fordert einen sicheren Remote Prozedur Aufruf von der RPC-Laufzeit an und gibt verschiedene Sicherheitsoptionen an, z. b. Sicherheitsanbieter, Sicherheits-QoS-Optionen usw.

In diesem Abschnitt werden die wesentlichen Konzepte und Informationen erläutert, die für die Verwendung der RPC-Funktionen erforderlich sind, um einen Client und Server für eine authentifizierte verteilte Anwendung zu erstellen. Es ist in die folgenden Themen unterteilt:

-   [Prinzipal Namen](principal-names.md)
-   [Authentifizierungs Ebenen](authentication-levels.md)
-   [Authentifizierungsdienste](authentication-services.md)
-   [Anmelde Informationen zur Client Authentifizierung](client-authentication-credentials.md)
-   [Autorisierungs Dienste](authorization-services.md)
-   [Quality of Service (QoS, Dienstqualität)](quality-of-service.md)
-   [Autorisierungs Funktionen](authorization-functions.md)
-   [Schlüssel Erwerbs Funktionen](key-acquisition-functions.md)
-   [Clientidentitätswechsel](client-impersonation.md)

 

 




