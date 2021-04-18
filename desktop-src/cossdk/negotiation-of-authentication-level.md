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
# <a name="negotiation-of-authentication-level"></a><span data-ttu-id="a8aa6-103">Aushandlung der Authentifizierungs Ebene</span><span class="sxs-lookup"><span data-stu-id="a8aa6-103">Negotiation of Authentication Level</span></span>

<span data-ttu-id="a8aa6-104">Sowohl der Client als auch der Server müssen an der Authentifizierung teilnehmen, und jede Partei gibt an, dass Sie eine bestimmte Authentifizierungs Stufe ausführen möchte.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-104">Both client and server must participate in authentication, and each party indicates that it wants to perform a certain level of authentication.</span></span> <span data-ttu-id="a8aa6-105">Am Anfang eines Aufrufes wird die Authentifizierungs Ebene zwischen den beiden Parteien ausgehandelt, ein geeigneter Dienst ausgewählt, und der-Rückruf wird authentifiziert und wird (mit möglicher Verschlüsselung, abhängig von der gewählten Authentifizierungs Stufe) fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-105">At the beginning of a call, the authentication level is negotiated between the two parties, an appropriate service is chosen, and the call is authenticated and proceeds (with possible encryption, depending on the authentication level chosen).</span></span> <span data-ttu-id="a8aa6-106">Die zwischen Client und Server ausgehandelte Authentifizierungs Ebene wird als Maximum (*Client* Einstellung, *Server* Einstellung) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-106">The authentication level negotiated between client and server is determined as Maximum(*Client preference*, *Server preference*).</span></span> <span data-ttu-id="a8aa6-107">Dies hat zur Folge, dass der Server immer ein minimal Maß an Authentifizierung vorschreiben kann, mit dem es vertraut ist. Das heißt, die Authentifizierung kann vom Server administrativ vorgeschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-107">The effect of this means that the server can always dictate a minimum level of authentication that it is comfortable with; that is, authentication can be administratively dictated from the server.</span></span>

<span data-ttu-id="a8aa6-108">Der Client gibt an, dass die Authentifizierung auf einer bestimmten Ebene wie bei einer beliebigen COM-Anwendung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-108">The client specifies that it wants to perform authentication at a certain level as with any COM application.</span></span> <span data-ttu-id="a8aa6-109">Die Client Authentifizierungs Ebene kann wie folgt angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a8aa6-109">The client authentication level can be indicated as follows:</span></span>

-   <span data-ttu-id="a8aa6-110">Pro Client Computer mit der Computer weiten com-Authentifizierungs Ebene, die entweder mithilfe von [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) oder dem Verwaltungs Programmkomponenten Dienste festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-110">Per client machine, with the machine-wide COM authentication level set by using either [DCOMCNFG](/windows/desktop/com/setting-machine-wide-security-using-dcomcnfg) or the Component Services administrative tool.</span></span>
-   <span data-ttu-id="a8aa6-111">Mithilfe von [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) oder mithilfe des Verwaltungs Programms Komponenten Dienste, wenn der Client eine COM+-Anwendung sein sollte.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-111">Per client application administratively, using [DCOMCNFG](/windows/desktop/com/setting-processwide-security-using-dcomcnfg) or using the Component Services administrative tool if the client should be a COM+ application.</span></span>
-   <span data-ttu-id="a8aa6-112">Programm gesteuert pro Client Prozess mit [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a8aa6-112">Per client process programmatically, with [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span>
-   <span data-ttu-id="a8aa6-113">Zu einem beliebigen Zeitpunkt Programm gesteuert mit [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span><span class="sxs-lookup"><span data-stu-id="a8aa6-113">At any point programmatically, using [**CoSetProxyBlanket**](/windows/desktop/api/combaseapi/nf-combaseapi-cosetproxyblanket).</span></span>

<span data-ttu-id="a8aa6-114">Die COM+-Serveranwendung gibt eine Authentifizierungs Ebene administrativ mithilfe des Verwaltungs Programms Komponenten Dienste (oder über ein administratives Skript) an.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-114">The COM+ server application specifies an authentication level administratively by using the Component Services administrative tool (or through an administrative script).</span></span>

<span data-ttu-id="a8aa6-115">Das Aushandeln der Authentifizierung für einen-Rückruf erfolgt in der folgenden Reihenfolge:</span><span class="sxs-lookup"><span data-stu-id="a8aa6-115">Negotiating authentication for a call proceeds in the following sequence:</span></span>

1.  <span data-ttu-id="a8aa6-116">Die Authentifizierungs Ebene wird als Max (*Client*, *Server*) ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-116">Authentication level is chosen as MAX(*client*, *server*).</span></span>
2.  <span data-ttu-id="a8aa6-117">Aushandlung des Authentifizierungs Protokolls.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-117">Negotiation of authentication protocol.</span></span>
3.  <span data-ttu-id="a8aa6-118">Der Server authentifiziert die Client Identität.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-118">Server authenticates client identity.</span></span>
4.  <span data-ttu-id="a8aa6-119">Optional authentifiziert der Client die Server Identität, abhängig vom Authentifizierungsprotokoll.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-119">Optionally, client authenticates server identity, depending on the authentication protocol.</span></span>
5.  <span data-ttu-id="a8aa6-120">Methodenaufrufe werden mit der gewählten Authentifizierungs Ebene kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="a8aa6-120">Method calls are communicated with the chosen level of authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8aa6-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a8aa6-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8aa6-122">Clientauthentifizierung</span><span class="sxs-lookup"><span data-stu-id="a8aa6-122">Client Authentication</span></span>](client-authentication.md)
</dt> </dl>

 

 
