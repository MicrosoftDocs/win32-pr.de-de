---
title: Sicherheitsmethoden
description: Microsoft RPC unterstützt zwei verschiedene Methoden zum Hinzufügen von Sicherheit zu ihrer verteilten Anwendung.
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037415"
---
# <a name="security-methods"></a><span data-ttu-id="0a02a-103">Sicherheitsmethoden</span><span class="sxs-lookup"><span data-stu-id="0a02a-103">Security Methods</span></span>

<span data-ttu-id="0a02a-104">Microsoft RPC unterstützt zwei verschiedene Methoden zum Hinzufügen von Sicherheit zu ihrer verteilten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0a02a-104">Microsoft RPC supports two different methods for adding security to your distributed application.</span></span> <span data-ttu-id="0a02a-105">Die erste Methode ist die Verwendung der Security Support Provider-Schnittstelle (SSPI), auf die mithilfe der RPC-Funktionen zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0a02a-105">The first method is to use the Security Support Provider Interface (SSPI), which can be accessed using the RPC functions.</span></span> <span data-ttu-id="0a02a-106">Im Allgemeinen empfiehlt es sich, diese Methode zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a02a-106">In general, it is best to use this method.</span></span> <span data-ttu-id="0a02a-107">Die SSPI bietet die flexibelsten und Netzwerk unabhängigen Authentifizierungs Features.</span><span class="sxs-lookup"><span data-stu-id="0a02a-107">The SSPI provides the most flexible and network-independent authentication features.</span></span>

<span data-ttu-id="0a02a-108">Die zweite Methode besteht darin, die Sicherheitsfunktionen zu verwenden, die in die System Transportprotokolle integriert sind.</span><span class="sxs-lookup"><span data-stu-id="0a02a-108">The second method is to use the security features built into the system transport protocols.</span></span> <span data-ttu-id="0a02a-109">Die Sicherheitsmethode auf Transport Ebene ist nicht die bevorzugte Methode.</span><span class="sxs-lookup"><span data-stu-id="0a02a-109">The transport-level security method is not the preferred method.</span></span> <span data-ttu-id="0a02a-110">Die Verwendung der SSPI wird empfohlen, da Sie für alle Transporte, plattformübergreifend, funktioniert und ein hohes Maß an Sicherheit bietet, einschließlich Datenschutz.</span><span class="sxs-lookup"><span data-stu-id="0a02a-110">Using the SSPI is recommended because it works on all transports, across platforms, and provides high levels of security, including privacy.</span></span>

<span data-ttu-id="0a02a-111">Dieser Abschnitt enthält Übersichten zu SSPI und Sicherheit auf Transport Ebene in den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="0a02a-111">This section provides overviews of both SSPI and transport-level security in the following topics:</span></span>

-   [<span data-ttu-id="0a02a-112">Security Support Provider Interface (SSPI)</span><span class="sxs-lookup"><span data-stu-id="0a02a-112">Security Support Provider Interface (SSPI)</span></span>](security-support-provider-interface-sspi-.md)
-   [<span data-ttu-id="0a02a-113">Transport Sicherheit</span><span class="sxs-lookup"><span data-stu-id="0a02a-113">Transport Security</span></span>](transport-security.md)

 

 




