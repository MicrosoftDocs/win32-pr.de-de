---
description: SSPI-Optionen für verteilte Anwendungen
ms.assetid: e67cc054-7e48-43e7-a4b0-d1d90e9511f2
title: SSPI-Optionen für verteilte Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed7729b3c479c69b674120fe1fc9827f5edfd878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861883"
---
# <a name="sspi-options-for-distributed-applications"></a><span data-ttu-id="92be5-103">SSPI-Optionen für verteilte Anwendungen</span><span class="sxs-lookup"><span data-stu-id="92be5-103">SSPI Options for Distributed Applications</span></span>

<span data-ttu-id="92be5-104">Entwickler haben viele Optionen zum entwickeln verteilter Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="92be5-104">Developers have many options for building distributed applications.</span></span> <span data-ttu-id="92be5-105">Die [*Security Support Provider-Schnittstelle*](../secgloss/s-gly.md) (SSPI) bietet eine Abstraktions Ebene zwischen Protokollen auf Anwendungsebene und [*Sicherheitsprotokollen*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="92be5-105">[*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) provides an abstraction layer between application-level protocols and [*security protocols*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="92be5-106">Anwendungen können die SSPI-Sicherheitsprotokolle auf verschiedene Weise nutzen:</span><span class="sxs-lookup"><span data-stu-id="92be5-106">Applications can take advantage of the SSPI security protocols in several ways:</span></span>

-   <span data-ttu-id="92be5-107">Direkte Aufrufe von SSPI-Routinen (für herkömmliche, socketbasierte Anwendungen).</span><span class="sxs-lookup"><span data-stu-id="92be5-107">Call SSPI routines directly (for traditional, socket-based applications).</span></span>

    <span data-ttu-id="92be5-108">Die Routinen verwenden Anforderungs-/Antwort-Nachrichten, um das [*Anwendungsprotokoll*](../secgloss/a-gly.md) zu implementieren, das sicherheitsrelevante SSPI-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="92be5-108">The routines use request/response messages to implement the [*application protocol*](../secgloss/a-gly.md) that carries SSPI security-related data.</span></span>

-   <span data-ttu-id="92be5-109">Verwenden Sie com, um Sicherheitsoptionen aufzurufen, die mithilfe von authentifizierter RPC und SSPI auf niedrigeren Ebenen implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="92be5-109">Use COM to call security options that are implemented by using authenticated RPC and SSPI at lower levels.</span></span>

    <span data-ttu-id="92be5-110">Von diesen Anwendungen werden keine SSPI-Funktionen direkt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="92be5-110">These applications do not call SSPI functions directly.</span></span>

-   <span data-ttu-id="92be5-111">Verwenden Sie [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (Winsock) mit der erweiterten Winsock-Schnittstelle, damit Transportanbieter Sicherheitsfeatures verwenden können.</span><span class="sxs-lookup"><span data-stu-id="92be5-111">Use [Windows Sockets 2](../winsock/windows-sockets-start-page-2.md) (WinSock) with the extended WinSock interface to allow transport providers to use security features.</span></span>

    <span data-ttu-id="92be5-112">Bei diesem Ansatz wird der [*Security Support Provider*](../secgloss/s-gly.md) (SSP) in den Netzwerk Stapel integriert, und es werden Sicherheits-und Transportdienste über eine gemeinsame Oberfläche bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="92be5-112">This approach integrates the [*security support provider*](../secgloss/s-gly.md) (SSP) into the network stack and provides both security and transport services through a common interface.</span></span>

-   <span data-ttu-id="92be5-113">Verwenden Sie die [Windows Internet Extensions-API](../wininet/portal.md) (WinInet) und eine Schnittstelle, die für die Unterstützung von Internet Sicherheitsprotokollen wie dem [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL)-Protokoll konzipiert ist.</span><span class="sxs-lookup"><span data-stu-id="92be5-113">Use the [Windows Internet Extensions API](../wininet/portal.md) (WinInet) and an interface designed to support Internet security protocols such as the [*Secure Sockets Layer*](../secgloss/s-gly.md) (SSL) protocol.</span></span>

    <span data-ttu-id="92be5-114">Anwendungen verwenden die SSPI-Schnittstelle für den Sicherheitsanbieter [Secure Channel](secure-channel.md) (SChannel), um die WinInet-Sicherheit zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="92be5-114">Applications use the SSPI interface to the [Secure Channel](secure-channel.md) (Schannel) security provider to implement WinInet security.</span></span> <span data-ttu-id="92be5-115">SChannel ist die Microsoft-Implementierung von SSL.</span><span class="sxs-lookup"><span data-stu-id="92be5-115">Schannel is the Microsoft implementation of SSL.</span></span>

<span data-ttu-id="92be5-116">Mehrere SSPI-Funktionen geben Zeitstempel zurück, die die Lebensdauer verschiedener Objekte darstellen.</span><span class="sxs-lookup"><span data-stu-id="92be5-116">Several SSPI functions return time stamps that represent the life span of various objects.</span></span> <span data-ttu-id="92be5-117">[*Sicherheitspakete*](../secgloss/s-gly.md) können Zeit in Anspruch nehmen und Zeitstempel auf unterschiedliche Weise bereitstellen, aber die lokale Zeit vereinfacht die Arbeit von Anwendungen, die SSPI-Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="92be5-117">[*Security packages*](../secgloss/s-gly.md) can maintain time and provide time stamps in different ways, but using local time simplifies the work of applications that use SSPI functions.</span></span>

 

 
