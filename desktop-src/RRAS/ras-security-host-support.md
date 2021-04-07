---
title: Unterstützung für RAS-Sicherheits Host
description: Windows NT 4,0 bietet eine Möglichkeit für eine Drittanbieter-RAS-Sicherheits-DLL, um die integrierten RAS-Sicherheitsfeatures zu verbessern. Windows 95 bietet diese Unterstützung nicht.
ms.assetid: 1cbacd7f-c9b9-4fb4-b505-a4b1d1b6f632
keywords:
- Host Unterstützung, RAS
- Unterstützung von Sicherheits Hosts, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99145f80d347ccd4ee9fbf4a4cdc23ca5af373e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711741"
---
# <a name="ras-security-host-support"></a>Unterstützung für RAS-Sicherheits Host

Windows NT 4,0 bietet eine Möglichkeit für eine Drittanbieter-RAS-Sicherheits-DLL, um die integrierten RAS-Sicherheitsfeatures zu verbessern. Windows 95 bietet diese Unterstützung nicht.

Ein Windows NT/Windows 2000-RAS-Server stellt Sicherheitsmechanismen für die Überprüfung des Netzwerk Zugriffs von Remote Benutzern bereit. Wenn ein RAS-Server einen-Befehl empfängt, überprüft er die Anmelde Informationen des Benutzers anhand der lokalen oder Domänen Konto Datenbank. RAS unterstützt auch die Rückruf Sicherheit, bei der der RAS-Server nicht mehr aktiv ist, und ruft dann den Remote Benutzer zum Herstellen der Verbindung zurück. Bei Netzwerken, in denen diese Sicherheitsstufe nicht ausreicht, können Sie eine Drittanbieter-RAS-Sicherheits-DLL installieren. Die Sicherheits-DLL kann dann einen Remote Benutzer authentifizieren, indem er Sicherheitsinformationen aus einer anderen Datenbank als der Standardbenutzer Konten Datenbank liest.

Wenn der RAS-Server einen Aufruf empfängt, ruft er die Sicherheits-DLL auf, um den Remote Benutzer zu authentifizieren. Die Unterstützung des RAS-Sicherheits Hosts bietet einen Mechanismus, mit dem die Sicherheits-DLL über ein Terminalfenster auf dem Remote Computer mit dem Remote Benutzer kommunizieren können. In einem typischen Szenario fordert die Sicherheits-DLL den Anmelde Namen des Remote Benutzers an. Die dll verwendet dann die private Sicherheitsdatenbank, um eine Herausforderung für das Senden an das Remote Terminal zu formulieren. Die Herausforderung könnte z. b. ein Code sein, den der Benutzer als Eingabe für einen cardkey-Reader bereitstellen muss. Der cardkey-Reader zeigt dann eine Antwort an, die der Remote Benutzer im Terminalfenster eingibt. Die Sicherheits-DLL überprüft dann die Antwort auf die Informationen des Benutzers in der privaten Sicherheitsdatenbank.

Wenn die Sicherheits-DLL den Remote Benutzer authentifiziert, führt der RAS-Server eine eigene Authentifizierung durch. Dadurch wird sichergestellt, dass RAS-Sicherheit immer einen Remote Benutzer authentifiziert, auch wenn eine Sicherheits-DLL installiert ist, die allen Benutzern Zugriff gewährt.

> [!Note]  
> Windows NT/Windows 2000 bietet zurzeit Unterstützung für RAS-Sicherheits Hosts nur für asynchrone Modemverbindungen. andere Typen von Verbindungen, wie z. b. Ethernet (keine Modemverbindung), VPN (auch keine Modemverbindung) oder ISDN (synchron), werden nicht unterstützt.

 

 

 




