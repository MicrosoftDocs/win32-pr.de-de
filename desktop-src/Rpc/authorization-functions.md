---
title: Autorisierungs Funktionen (RPC)
description: Jedes Mal, wenn ein Serverprogramm eine Client Anforderung für den Zugriff auf eine der Verwaltungs Remote Prozeduren empfängt, ruft die RPC-Lauf Zeit Bibliothek eine standardmäßige Autorisierungs Funktion auf.
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/12/2019
ms.locfileid: "104038296"
---
# <a name="authorization-functions"></a>Autorisierungs Funktionen

Jedes Mal, wenn ein Serverprogramm eine Client Anforderung für den Zugriff auf eine der Verwaltungs Remote Prozeduren empfängt, ruft die RPC-Lauf Zeit Bibliothek eine standardmäßige Autorisierungs Funktion auf. Diese Funktion verwendet den SSP, um die Anmelde Informationen des Clients zu überprüfen und die Anforderung zu autorisieren oder abzulehnen.

Das Serverprogramm kann die von der SSP bereitgestellte Autorisierungs Funktion überschreiben. Rufen Sie die [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) -Funktion auf, und übergeben Sie Sie an die Adresse der Autorisierungs Funktion. Nachdem das Serverprogramm die Autorisierungs Funktion festgelegt hat, ruft die RPC-Lauf Zeit Bibliothek Sie jedes Mal auf, wenn das Serverprogramm eine Client Anforderung an eine der Verwaltungsfunktionen empfängt. Weitere Informationen finden Sie unter [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)und [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).

 

 




