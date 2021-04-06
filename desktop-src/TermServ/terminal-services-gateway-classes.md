---
title: Remotedesktop Gateway-Klassen
description: Der WMI-Anbieter für Remotedesktop Gateway (RD-Gateway) stellt die folgenden Klassen bereit.
ms.assetid: 482ba056-0de7-4c91-816c-dd3c926662ef
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d17adca523833f3418661cd3f9851d7c814cdc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713290"
---
# <a name="remote-desktop-gateway-classes"></a><span data-ttu-id="ce3df-103">Remotedesktop Gateway-Klassen</span><span class="sxs-lookup"><span data-stu-id="ce3df-103">Remote Desktop Gateway classes</span></span>

<span data-ttu-id="ce3df-104">Der WMI-Anbieter für Remotedesktop Gateway (RD-Gateway) stellt die folgenden Klassen bereit.</span><span class="sxs-lookup"><span data-stu-id="ce3df-104">The Remote Desktop Gateway (RD Gateway) WMI provider provides the following classes.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ce3df-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ce3df-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="ce3df-106">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="ce3df-106">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dd>

<span data-ttu-id="ce3df-107">Stellt eine Verbindung zwischen einem Client Computer und einem RD-Gateway Server dar.</span><span class="sxs-lookup"><span data-stu-id="ce3df-107">Represents a connection from a client computer to a RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-108">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="ce3df-108">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="ce3df-109">Beschreibt eine Remotedesktop Verbindungs Autorisierungs Richtlinie (RD-CAP).</span><span class="sxs-lookup"><span data-stu-id="ce3df-109">Describes a Remote Desktop connection authorization policy (RD CAP).</span></span> <span data-ttu-id="ce3df-110">RD-CAPs werden verwendet, um zu bestimmen, ob ein Benutzer eine Verbindung mit dem RD-Gateway-Server herstellen darf.</span><span class="sxs-lookup"><span data-stu-id="ce3df-110">RD CAPs are used to determine whether a user is allowed to connect to the RD Gateway server.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-111">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="ce3df-111">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dd>

<span data-ttu-id="ce3df-112">Beschreibt eine Gruppe von RD-Gateway Lasten Ausgleichs Servern.</span><span class="sxs-lookup"><span data-stu-id="ce3df-112">Describes a set of RD Gateway load-balancing servers.</span></span> <span data-ttu-id="ce3df-113">Diese werden verwendet, um einen Lastenausgleich RD-Gateway Verbindungen über mehrere Server hinweg durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ce3df-113">These are used to load balance RD Gateway connections across multiple servers.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-114">**Win32-"t- \_ gatewayradiusserver"**</span><span class="sxs-lookup"><span data-stu-id="ce3df-114">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dd>

<span data-ttu-id="ce3df-115">Beschreibt einen Remote Authentication Dial-in User Service Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) verfügt.</span><span class="sxs-lookup"><span data-stu-id="ce3df-115">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-116">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="ce3df-116">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dd>

<span data-ttu-id="ce3df-117">Beschreibt eine Remotedesktop-Ressourcen Autorisierungs Richtlinie (RD-RAP).</span><span class="sxs-lookup"><span data-stu-id="ce3df-117">Describes a Remote Desktop resource authorization policy (RD RAP).</span></span> <span data-ttu-id="ce3df-118">Eine RD-RAP wird verwendet, um zu entscheiden, ob ein Benutzer über RD-Gateway autorisiert ist, eine Verbindung mit einer angegebenen Ressource herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ce3df-118">An RD RAP is used to decide whether a user is authorized to connect to a specified resource through RD Gateway.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-119">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="ce3df-119">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dd>

<span data-ttu-id="ce3df-120">Beschreibt eine Ressourcengruppe, die eine Gruppe von Ressourcen (Computernamen) einer einzelnen Entität zuordnet.</span><span class="sxs-lookup"><span data-stu-id="ce3df-120">Describes a resource group, which maps a set of resources (computer names) to a single entity.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-121">**Win32- \_ Gatewayserver**</span><span class="sxs-lookup"><span data-stu-id="ce3df-121">**Win32\_TSGatewayServer**</span></span>](win32-tsgatewayserver.md)
</dt> <dd>

<span data-ttu-id="ce3df-122">Wird für RD-Gateway Server spezifische Vorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="ce3df-122">Used for RD Gateway server-specific operations.</span></span>

</dd> <dt>

[<span data-ttu-id="ce3df-123">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="ce3df-123">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dd>

<span data-ttu-id="ce3df-124">Stellt Methoden und Eigenschaften zum Anzeigen und konfigurieren RD-Gateway Servereinstellungen bereit.</span><span class="sxs-lookup"><span data-stu-id="ce3df-124">Provides methods and properties to view and configure RD Gateway server settings.</span></span>

</dd> </dl>

 

 




