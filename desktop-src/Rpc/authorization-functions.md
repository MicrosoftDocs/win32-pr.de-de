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
# <a name="authorization-functions"></a><span data-ttu-id="250f9-103">Autorisierungs Funktionen</span><span class="sxs-lookup"><span data-stu-id="250f9-103">Authorization Functions</span></span>

<span data-ttu-id="250f9-104">Jedes Mal, wenn ein Serverprogramm eine Client Anforderung für den Zugriff auf eine der Verwaltungs Remote Prozeduren empfängt, ruft die RPC-Lauf Zeit Bibliothek eine standardmäßige Autorisierungs Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="250f9-104">Each time a server program receives a client request for access to one of the management remote procedures, the RPC run-time library invokes a default authorization function.</span></span> <span data-ttu-id="250f9-105">Diese Funktion verwendet den SSP, um die Anmelde Informationen des Clients zu überprüfen und die Anforderung zu autorisieren oder abzulehnen.</span><span class="sxs-lookup"><span data-stu-id="250f9-105">This function uses the SSP to check the client's credentials and authorize or reject the request.</span></span>

<span data-ttu-id="250f9-106">Das Serverprogramm kann die von der SSP bereitgestellte Autorisierungs Funktion überschreiben.</span><span class="sxs-lookup"><span data-stu-id="250f9-106">Your server program can override the authorization function that the SSP provides.</span></span> <span data-ttu-id="250f9-107">Rufen Sie die [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) -Funktion auf, und übergeben Sie Sie an die Adresse der Autorisierungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="250f9-107">Invoke the function [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) and pass it to the address of your authorization function.</span></span> <span data-ttu-id="250f9-108">Nachdem das Serverprogramm die Autorisierungs Funktion festgelegt hat, ruft die RPC-Lauf Zeit Bibliothek Sie jedes Mal auf, wenn das Serverprogramm eine Client Anforderung an eine der Verwaltungsfunktionen empfängt.</span><span class="sxs-lookup"><span data-stu-id="250f9-108">Once the server program sets the authorization function, the RPC run-time library calls it every time the server program receives a client request to one of the management functions.</span></span> <span data-ttu-id="250f9-109">Weitere Informationen finden Sie unter [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)und [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span><span class="sxs-lookup"><span data-stu-id="250f9-109">For more information, see [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening), [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening), [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids), [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname), and [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats).</span></span>

 

 




