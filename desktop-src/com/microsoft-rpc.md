---
title: Microsoft RPC
description: Microsoft RPC
ms.assetid: a9ca629a-2766-43d5-89da-73d0628b3c5e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53be9d46368ae01aee25815327aafeaf7f44525b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707253"
---
# <a name="microsoft-rpc"></a><span data-ttu-id="bf4de-103">Microsoft RPC</span><span class="sxs-lookup"><span data-stu-id="bf4de-103">Microsoft RPC</span></span>

<span data-ttu-id="bf4de-104">Microsoft RPC ist ein Modell für die Programmierung in einer verteilten Computerumgebung.</span><span class="sxs-lookup"><span data-stu-id="bf4de-104">Microsoft RPC is a model for programming in a distributed computing environment.</span></span> <span data-ttu-id="bf4de-105">Das Ziel von RPC besteht darin, eine transparente Kommunikation bereitzustellen, sodass der Client scheinbar direkt mit dem Server kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="bf4de-105">The goal of RPC is to provide transparent communication so that the client appears to be directly communicating with the server.</span></span> <span data-ttu-id="bf4de-106">Die Microsoft-Implementierung von RPC ist mit dem DCE-RPC (Open Software Foundation) der verteilten Rechen Umgebung (natürlich) kompatibel.</span><span class="sxs-lookup"><span data-stu-id="bf4de-106">Microsoft's implementation of RPC is compatible with the Open Software Foundation (OSF) Distributed Computing Environment (DCE) RPC.</span></span>

<span data-ttu-id="bf4de-107">Sie können RPC so konfigurieren, dass ein oder mehrere Transporte, mindestens ein Namensdienst und ein oder mehrere Sicherheitsserver verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf4de-107">You can configure RPC to use one or more transports, one or more name services, and one or more security servers.</span></span> <span data-ttu-id="bf4de-108">Die Schnittstellen zu diesen Anbietern werden von RPC verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bf4de-108">The interfaces to those providers are handled by RPC.</span></span> <span data-ttu-id="bf4de-109">Da Microsoft RPC für die Zusammenarbeit mit mehreren Anbietern konzipiert ist, können Sie die Anbieter auswählen, die für Ihr Netzwerk am besten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="bf4de-109">Because Microsoft RPC is designed to work with multiple providers, you can choose the providers that work best for your network.</span></span> <span data-ttu-id="bf4de-110">Der Transport ist dafür verantwortlich, die Daten über das Netzwerk zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="bf4de-110">The transport is responsible for transmitting the data across the network.</span></span> <span data-ttu-id="bf4de-111">Der Namensdienst nimmt einen Objektnamen, z. b. einen Moniker, auf und findet seinen Speicherort im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="bf4de-111">The name service takes an object name, such as a moniker, and finds its location on the network.</span></span> <span data-ttu-id="bf4de-112">Der Sicherheitsserver bietet Anwendungen die Möglichkeit, den Zugriff auf bestimmte Benutzer und/oder Gruppen zu verweigern.</span><span class="sxs-lookup"><span data-stu-id="bf4de-112">The security server offers applications the option of denying access to specific users and/or groups.</span></span> <span data-ttu-id="bf4de-113">Ausführlichere Informationen zur Anwendungssicherheit finden Sie unter [Schnittstellen Entwurfs Regeln](interface-design-rules.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4de-113">See [Interface Design Rules](interface-design-rules.md) for more detailed information about application security.</span></span>

<span data-ttu-id="bf4de-114">Zusätzlich zu den RPC-Laufzeitbibliotheken enthält Microsoft RPC die IDL (Interface Definition Language) und den zugehörigen Compiler.</span><span class="sxs-lookup"><span data-stu-id="bf4de-114">In addition to the RPC run-time libraries, Microsoft RPC includes the Interface Definition Language (IDL) and its compiler.</span></span> <span data-ttu-id="bf4de-115">Obwohl die IDL-Datei ein Standard Teil von RPC ist, hat Microsoft Sie erweitert, um ihre Funktionalität zur Unterstützung benutzerdefinierter COM-Schnittstellen zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="bf4de-115">Although the IDL file is a standard part of RPC, Microsoft has enhanced it to extend its functionality to support custom COM interfaces.</span></span> <span data-ttu-id="bf4de-116">Der Microsoft Interface Definition Language (mittlerer l)-Compiler verwendet die IDL-Datei, die die benutzerdefinierte Schnittstelle beschreibt, um mehrere Dateien zu generieren, die unter [Erstellen und Registrieren einer Proxy-dll](building-and-registering-a-proxy-dll.md)erläutert werden</span><span class="sxs-lookup"><span data-stu-id="bf4de-116">The Microsoft Interface Definition Language (MIDL) compiler uses the IDL file that describes your custom interface to generate several files discussed in [Building and Registering a Proxy DLL](building-and-registering-a-proxy-dll.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bf4de-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bf4de-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf4de-118">Kanal</span><span class="sxs-lookup"><span data-stu-id="bf4de-118">Channel</span></span>](channel.md)
</dt> <dt>

[<span data-ttu-id="bf4de-119">Kommunikation zwischen Objekten</span><span class="sxs-lookup"><span data-stu-id="bf4de-119">Inter-Object Communication</span></span>](inter-object-communication.md)
</dt> <dt>

[<span data-ttu-id="bf4de-120">Marshalling von Details</span><span class="sxs-lookup"><span data-stu-id="bf4de-120">Marshaling Details</span></span>](marshaling-details.md)
</dt> <dt>

[<span data-ttu-id="bf4de-121">Proxy</span><span class="sxs-lookup"><span data-stu-id="bf4de-121">Proxy</span></span>](proxy.md)
</dt> <dt>

[<span data-ttu-id="bf4de-122">Stub</span><span class="sxs-lookup"><span data-stu-id="bf4de-122">Stub</span></span>](stub.md)
</dt> </dl>

 

 




