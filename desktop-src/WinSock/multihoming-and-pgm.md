---
description: Besondere Überlegungen müssen für mehrfach vernetzte PGM-Absender oder-Empfänger angegeben werden. Auf dieser Seite werden die Überlegungen beschrieben und Richtlinien für Best Practices für die Programmierung bereitstellt.
ms.assetid: 10fb56dd-3c96-4944-9b53-aee76c269528
title: Multihosting und PGM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 142527c7fdf3e5d34d80c51e4002bc21ad47691c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347164"
---
# <a name="multihoming-and-pgm"></a><span data-ttu-id="09e2e-104">Multihosting und PGM</span><span class="sxs-lookup"><span data-stu-id="09e2e-104">Multihoming and PGM</span></span>

<span data-ttu-id="09e2e-105">Besondere Überlegungen müssen für mehrfach vernetzte PGM-Absender oder-Empfänger angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="09e2e-105">Special consideration must be given to multihomed PGM senders or receivers.</span></span> <span data-ttu-id="09e2e-106">Auf dieser Seite werden die Überlegungen beschrieben und Richtlinien für Best Practices für die Programmierung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="09e2e-106">This page describes the considerations, and provides guidelines for best programming practices.</span></span>

## <a name="multihomed-pgm-sender"></a><span data-ttu-id="09e2e-107">Mehrfach vernetzter PGM-Sender</span><span class="sxs-lookup"><span data-stu-id="09e2e-107">Multihomed PGM Sender</span></span>

<span data-ttu-id="09e2e-108">Wenn eine Anwendung beim Aufrufen der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) -Funktion keine Schnittstelle angibt, wird die erste verfügbare Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="09e2e-108">When an application fails to specify an interface upon calling the [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) function, the first available interface is used.</span></span> <span data-ttu-id="09e2e-109">Wenn keine Schnittstelle verfügbar ist, schlägt die **Verbindungs** Herstellung fehl.</span><span class="sxs-lookup"><span data-stu-id="09e2e-109">If no interface is available, **connect** fails.</span></span>

<span data-ttu-id="09e2e-110">Wenn eine Anwendung mithilfe der Option [RM \_ Set \_ Send \_ if](socket-options.md) Socket eine Schnittstelle angibt, wird ein [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Versuch implizit an diese Schnittstelle mithilfe von TCP/IP vorgenommen und schlägt fehl, wenn TCP/IP die Bindungs Anforderung nicht erfüllt.</span><span class="sxs-lookup"><span data-stu-id="09e2e-110">When an application specifies an interface using the [RM\_SET\_SEND\_IF](socket-options.md) socket option, a [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) attempt is made implicitly to that interface using TCP/IP, and fails if TCP/IP fails the bind request.</span></span> <span data-ttu-id="09e2e-111">Wenn die Schnittstelle mithilfe von RM \_ Set \_ Send \_ , wenn mehrmals festgelegt wird, gilt nur die letzte erfolgreich festgelegte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="09e2e-111">If the interface is set using RM\_SET\_SEND\_IF multiple times, only the last interface set successfully is applicable.</span></span>

<span data-ttu-id="09e2e-112">Windows Sockets verwaltet, welche Schnittstelle festgelegt ist. wenn diese Schnittstelle nicht mehr angezeigt wird, wird die Sitzung getrennt.</span><span class="sxs-lookup"><span data-stu-id="09e2e-112">Windows Sockets maintains which interface is set, and if that interface disappears, the session is disconnected.</span></span>

## <a name="multihomed-pgm-receiver"></a><span data-ttu-id="09e2e-113">Mehrfach vernetzter PGM-Empfänger</span><span class="sxs-lookup"><span data-stu-id="09e2e-113">Multihomed PGM Receiver</span></span>

<span data-ttu-id="09e2e-114">Wenn eine Anwendung beim Aufrufen der Funktion " [**lauschen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) " keine Schnittstelle angibt, wird die Standardschnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="09e2e-114">When an application fails to specify an interface upon calling the [**listen**](/windows/desktop/api/Winsock2/nf-winsock2-listen) function, the default interface is used.</span></span> <span data-ttu-id="09e2e-115">Wenn keine Schnittstelle verfügbar ist, schlägt [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) fehl.</span><span class="sxs-lookup"><span data-stu-id="09e2e-115">If no interface is available, [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) fails.</span></span>

<span data-ttu-id="09e2e-116">Wenn eine Anwendung eine oder mehrere Schnittstellen angibt, auf die gelauscht werden soll, wird bei Verwendung von [RM \_ Add \_ Receive \_ if](socket-options.md)der Versuch unternommen, mit TCP/IP eine Bindung an die angeforderte Schnittstelle herzustellen.</span><span class="sxs-lookup"><span data-stu-id="09e2e-116">When an application specifies one or more interfaces on which to listen, using [RM\_ADD\_RECEIVE\_IF](socket-options.md), Windows Sockets attempts to bind to the requested interface or interfaces using TCP/IP.</span></span> <span data-ttu-id="09e2e-117">Jeder Fehler von TCP/IP bewirkt, dass diese Anforderung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="09e2e-117">Any error from TCP/IP causes this request to fail.</span></span> <span data-ttu-id="09e2e-118">Anders als bei der PGM-Absender Anfrage führt das Hinzufügen einer Empfangs Schnittstelle mehrmals dazu, dass auf allen erfolgreich hinzugefügten Schnittstellen lauscht.</span><span class="sxs-lookup"><span data-stu-id="09e2e-118">Unlike the PGM sender case, adding a receive interface multiple times result in the listens being posted on all the successfully added interfaces.</span></span> <span data-ttu-id="09e2e-119">Verwenden Sie die \_ Option RM del \_ Receive \_ if Socket, um das lauschen an einer Schnittstelle zu beenden.</span><span class="sxs-lookup"><span data-stu-id="09e2e-119">Use the RM\_DEL\_RECEIVE\_IF socket option to stop listening on an interface.</span></span>

<span data-ttu-id="09e2e-120">Windows Sockets behält den Zustand über mehrere angegebene Überwachungsschnittstellen bei und basiert stattdessen auf TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="09e2e-120">Windows Sockets does not maintain state about multiple specified listening interfaces, and instead relies on TCP/IP to do so.</span></span> <span data-ttu-id="09e2e-121">Sobald eine Sitzung ausgeführt wird, verfolgt Windows Sockets jedoch die eingehende Schnittstelle für diese Sitzung. wenn diese Schnittstelle nicht mehr angezeigt wird, trennt Windows Sockets die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="09e2e-121">Once a session is in progress, however, Windows Sockets track the incoming interface for that session, and if that interface disappears, Windows Sockets disconnects the session.</span></span>

 

 



