---
description: Callcenter-Steuerelemente erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic calldistribution) zu unterstützen.
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Verwenden von callcentersteuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357422"
---
# <a name="using-call-center-controls"></a><span data-ttu-id="c24fd-103">Verwenden von callcentersteuerelementen</span><span class="sxs-lookup"><span data-stu-id="c24fd-103">Using Call Center Controls</span></span>

<span data-ttu-id="c24fd-104">Callcenter-Steuerelemente erweitern das TAPI 3-Objektmodell, um die Anforderungen von ACD-Systemen (Automatic calldistribution) zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c24fd-104">Call center controls extend the TAPI 3 object model to support the requirements of Automatic Call Distribution (ACD) systems.</span></span> <span data-ttu-id="c24fd-105">Ein Callcenter ist ein Ort, an dem Agents oder Operatoren an Telefon Telefonen entweder ausgehende Telefonanrufe tätigen oder eingehende Anrufe tätigen.</span><span class="sxs-lookup"><span data-stu-id="c24fd-105">A call center is a location with agents or operators at banks of telephones either making outgoing telephone calls or fielding incoming ones.</span></span> <span data-ttu-id="c24fd-106">Beispielsweise verwendet eine Bank oder ein Kreditkartenunternehmen ein Callcenter, um Konto Anfragen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="c24fd-106">For example, a bank or credit card company will use a call center to process account inquiries.</span></span>

<span data-ttu-id="c24fd-107">Callcenteranwendungen sind in drei grundlegende Typen unterteilt:</span><span class="sxs-lookup"><span data-stu-id="c24fd-107">Call center applications are divided into three basic types:</span></span>

-   <span data-ttu-id="c24fd-108">[ACD-Proxy](acd-proxy.md): verarbeitet eingehende oder ausgehende Sitzungen auf dem Server, die von einem proprietären Telefon Switch zu einem Internet Gateway verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="c24fd-108">[ACD Proxy](acd-proxy.md): Handles incoming or outgoing sessions at the server, which can be anything from a proprietary telephone switch to an Internet gateway.</span></span>
-   <span data-ttu-id="c24fd-109">[ACD-Agent-Client](acd-agent-client.md): dient zum Bereitstellen eines einzelnen Agents, der einen einzelnen Agent empfängt oder aufruft.</span><span class="sxs-lookup"><span data-stu-id="c24fd-109">[ACD Agent Client](acd-agent-client.md): Services an individual agent who is receiving or making calls.</span></span>
-   <span data-ttu-id="c24fd-110">ACD Supervisor Client: bietet eine allgemeine Ansicht der Agent-und ACD-Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="c24fd-110">ACD Supervisor Client: Provides an overall view of agent and ACD operations.</span></span>

> [!Note]  
> <span data-ttu-id="c24fd-111">Für Windows 2000 ist die Proxy Funktionalität mithilfe von TAPI 2,2 verfügbar, und Supervisor-Funktionen sind nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="c24fd-111">For Windows 2000, proxy functionality is available using TAPI 2.2, and supervisor functions are not implemented.</span></span>

 

<span data-ttu-id="c24fd-112">Der Abschnitt "Beispiele" der Windows SDK enthält ACD-Codebeispiele unter netds \\ TAPI \\ Tapi2 \\ ACD und netds \\ TAPI \\ Tapi3 \\ ACD.</span><span class="sxs-lookup"><span data-stu-id="c24fd-112">The samples section of the Windows SDK contains ACD code samples under Netds\\Tapi\\Tapi2\\Acd and Netds\\Tapi\\Tapi3\\Acd.</span></span>

 

 



