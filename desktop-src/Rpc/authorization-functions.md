---
title: Autorisierungsfunktionen (RPC)
description: Jedes Mal, wenn ein Serverprogramm eine Clientanforderung für den Zugriff auf eines der Remoteverwaltungsprozeduren empfängt, ruft die RPC-Laufzeitbibliothek eine Standardautorisierungsfunktion auf.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47234f83ae76ab6ee29ed434099ba3e4a7dbb3f9c7a01a2448d0cb0dad0267dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023411"
---
# <a name="authorization-functions"></a>Autorisierungsfunktionen

Jedes Mal, wenn ein Serverprogramm eine Clientanforderung für den Zugriff auf eines der Remoteverwaltungsprozeduren empfängt, ruft die RPC-Laufzeitbibliothek eine Standardautorisierungsfunktion auf. Diese Funktion verwendet den SSP, um die Anmeldeinformationen des Clients zu überprüfen und die Anforderung zu autorisieren oder abzulehnen.

Ihr Serverprogramm kann die autorisierungsfunktion überschreiben, die der SSP bietet. Rufen Sie die [**Funktion RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) auf, und übergeben Sie sie an die Adresse Ihrer Autorisierungsfunktion. Sobald das Serverprogramm die Autorisierungsfunktion legt, ruft die RPC-Laufzeitbibliothek sie jedes Mal auf, wenn das Serverprogramm eine Clientanforderung an eine der Verwaltungsfunktionen empfängt. Weitere Informationen finden Sie unter [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)und [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




