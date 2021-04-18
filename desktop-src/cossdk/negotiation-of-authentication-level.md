---
description: Aushandlung der Authentifizierungs Ebene
ms.assetid: 31353d02-bfe2-48ac-81a1-0e38895a8a75
title: Aushandlung der Authentifizierungs Ebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38b9983bd2a2df1d85cc6df4bfc0ba2a757b200f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340133"
---
# <a name="negotiation-of-authentication-level"></a>Aushandlung der Authentifizierungs Ebene

Sowohl der Client als auch der Server müssen an der Authentifizierung teilnehmen, und jede Partei gibt an, dass Sie eine bestimmte Authentifizierungs Stufe ausführen möchte. Am Anfang eines Aufrufes wird die Authentifizierungs Ebene zwischen den beiden Parteien ausgehandelt, ein geeigneter Dienst ausgewählt, und der-Rückruf wird authentifiziert und wird (mit möglicher Verschlüsselung, abhängig von der gewählten Authentifizierungs Stufe) fortgesetzt. Die zwischen Client und Server ausgehandelte Authentifizierungs Ebene wird als Maximum (*Client* Einstellung, *Server* Einstellung) festgelegt. Dies hat zur Folge, dass der Server immer ein minimal Maß an Authentifizierung vorschreiben kann, mit dem es vertraut ist. Das heißt, die Authentifizierung kann vom Server administrativ vorgeschrieben werden.

Der Client gibt an, dass die Authentifizierung auf einer bestimmten Ebene wie bei einer beliebigen COM-Anwendung durchgeführt werden soll. Die Client Authentifizierungs Ebene kann wie folgt angegeben werden:

-   Pro Client Computer mit der Computer weiten com-Authentifizierungs Ebene, die entweder mithilfe von [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) oder dem Verwaltungs Programmkomponenten Dienste festgelegt wurde.
-   Mithilfe von [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) oder mithilfe des Verwaltungs Programms Komponenten Dienste, wenn der Client eine COM+-Anwendung sein sollte.
-   Programm gesteuert pro Client Prozess mit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).
-   Zu einem beliebigen Zeitpunkt Programm gesteuert mit [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).

Die COM+-Serveranwendung gibt eine Authentifizierungs Ebene administrativ mithilfe des Verwaltungs Programms Komponenten Dienste (oder über ein administratives Skript) an.

Das Aushandeln der Authentifizierung für einen-Rückruf erfolgt in der folgenden Reihenfolge:

1.  Die Authentifizierungs Ebene wird als Max (*Client*, *Server*) ausgewählt.
2.  Aushandlung des Authentifizierungs Protokolls.
3.  Der Server authentifiziert die Client Identität.
4.  Optional authentifiziert der Client die Server Identität, abhängig vom Authentifizierungsprotokoll.
5.  Methodenaufrufe werden mit der gewählten Authentifizierungs Ebene kommuniziert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Clientauthentifizierung](client-authentication.md)
</dt> </dl>

 

 
