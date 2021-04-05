---
title: Häufige Fehler bei der Annahme, dass rpcserverregisterauthinfo das Aufrufen Ihres Servers durch nicht autorisierte Benutzer verhindert.
description: Wenn Sicherheitsanbieter auf dem Server mit der rpcserverregisterauthinfo-Funktion registriert werden, wird eine Option hinzugefügt, keine Anforderung.
ms.assetid: c8db8973-6d47-47b4-b927-72cfb464e9f0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 453a60c800d377dc122de561b87c41a5ec635328
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713338"
---
# <a name="common-mistake-assuming-rpcserverregisterauthinfo-prevents-unauthorized-users-from-calling-your-server"></a>Allgemeiner Fehler: die Annahme, dass rpcserverregisterauthinfo den Server nicht autorisiert

Wenn Sicherheitsanbieter auf dem Server mit der [**rpcserverregisterauthinfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) -Funktion registriert werden, wird eine Option hinzugefügt, keine Anforderung. Dies bedeutet, dass vorherige Registrierungen mit **rpcserverregisterauthinfo** nicht ersetzt werden. Dies bedeutet auch, dass nicht authentifizierte Clients weiterhin eine Verbindung herstellen können. Durch Aufrufen der **rpcserverregisterauthinfo** -Funktion ist es nicht zulässig, dass nicht authentifizierte Clients eine Verbindung herstellen. Sie können zwar eine Verbindung herstellen, aber Funktionsaufrufe wie [**RpcImpersonateClient**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcimpersonateclient) und [**rpcgetauthorizationcontextforclient**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcgetauthorizationcontextforclient) können nicht ausgeführt werden. Wenn also die **rpcserverregisterauthinfo** -Funktion aufgerufen wird, sind potenzielle Angreifer nicht mehr vorhanden – vielmehr können Clients, die Zugriff haben sollen, Ihre Identität nachweisen. Überprüfungen müssen immer noch vorhanden sein, um zu bestimmen, ob potenzielle Angreifer versuchen, eine Verbindung herzustellen.

 

 




