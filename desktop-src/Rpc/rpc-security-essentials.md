---
title: RPC Security Essentials
description: Um einen Remoteprozeduraufruf abzuschließen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed8bce6f97ecfc7bd257d20eebbb35d068624fe017c01a662b47fceb463b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926031"
---
# <a name="rpc-security-essentials"></a>RPC Security Essentials

Um einen Remoteprozeduraufruf abzuschließen, müssen alle verteilten Anwendungen eine Bindung zwischen dem Client und dem Server erstellen. Weitere Informationen zu Bindungen finden Sie unter [Bindung und Handles.](binding-and-handles.md) Um einen sicheren Remoteprozeduraufruf abzuschließen, sind zusätzliche Schritte erforderlich. Zunächst muss der Server einen Sicherheitsanbieter (Authentifizierungsdienst in DCE-Terminologie) auswählen. Anschließend muss er über seinen Authentifizierungsmechanismus entscheiden. Danach ruft der Client eine Bindung an den Server ab und fordert einen sicheren Remoteprozeduraufruf von der RPC-Laufzeit an und gibt verschiedene Sicherheitsoptionen an, z. B. Sicherheitsanbieter, QOS-Sicherheitsoptionen usw.

In diesem Abschnitt werden die grundlegenden Konzepte und Informationen erläutert, die erforderlich sind, um die RPC-Funktionen zum Erstellen eines Clients und Servers für eine authentifizierte verteilte Anwendung zu verwenden. Es ist in die folgenden Themen unterteilt:

-   [Prinzipalnamen](principal-names.md)
-   [Authentifizierungsebenen](authentication-levels.md)
-   [Authentifizierungsdienste](authentication-services.md)
-   [Anmeldeinformationen für die Clientauthentifizierung](client-authentication-credentials.md)
-   [Autorisierungsdienste](authorization-services.md)
-   [Quality of Service (QoS, Dienstqualität)](quality-of-service.md)
-   [Autorisierungsfunktionen](authorization-functions.md)
-   [Schlüsselerfassungsfunktionen](key-acquisition-functions.md)
-   [Clientidentitätswechsel](client-impersonation.md)

 

 




