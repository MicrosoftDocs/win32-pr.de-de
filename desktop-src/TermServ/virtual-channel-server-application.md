---
title: Virtual Channel-Server Anwendung
description: Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird. Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen.
ms.assetid: b593df5d-5e22-46c6-8f59-9e3fdfe765ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 377732b91d6f93645e23b0f0b93cc203a65ef471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711412"
---
# <a name="virtual-channel-server-application"></a><span data-ttu-id="4dbde-104">Virtual Channel-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="4dbde-104">Virtual Channel Server Application</span></span>

<span data-ttu-id="4dbde-105">Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4dbde-105">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="4dbde-106">Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="4dbde-106">Note that you must provide a method to start the server application.</span></span> <span data-ttu-id="4dbde-107">Dies kann auf verschiedene Weise erreicht werden: Beispielsweise können Sie ein Anmelde Skript oder ein Programm oder Skript im Startordner verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dbde-107">You can accomplish this in multiple ways; for example, you can use a logon script, or a program or script in the Startup folder.</span></span> <span data-ttu-id="4dbde-108">Benutzer können die Anwendung auch starten.</span><span class="sxs-lookup"><span data-stu-id="4dbde-108">Users could also launch the application.</span></span>

<span data-ttu-id="4dbde-109">Sie müssen den Namen der Virtual Channel-Serveranwendung in der Registrierung speichern, indem Sie einen Unterschlüssel unter folgendem Speicherort hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="4dbde-109">You must store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="4dbde-110">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **Terminal Server**- \\ **AddIns**</span><span class="sxs-lookup"><span data-stu-id="4dbde-110">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**Terminal Server**\\**Addins**</span></span>

<span data-ttu-id="4dbde-111">Weitere Informationen zum Unterschlüssel finden Sie unter über [Wachen von Sitzungs Verbindungen und Verbindungsunterbrechungen](monitoring-session-connections-and-disconnections.md).</span><span class="sxs-lookup"><span data-stu-id="4dbde-111">For more information about the subkey, see [Monitoring Session Connections and Disconnections](monitoring-session-connections-and-disconnections.md).</span></span>

<span data-ttu-id="4dbde-112">Die Serveranwendung kann die [**WFS virtualchannelopen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) -Funktion zum Öffnen eines Handles für einen virtuellen Channel aufruft.</span><span class="sxs-lookup"><span data-stu-id="4dbde-112">The server application can call the [**WTSVirtualChannelOpen**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelopen) function to open a handle to a virtual channel.</span></span> <span data-ttu-id="4dbde-113">Die Anwendung kann dann das Handle in einer der folgenden Funktionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4dbde-113">The application can then use the handle in any of the following functions.</span></span>

<dl> <dt>

[<span data-ttu-id="4dbde-114">**Wout virtualchannelclose**</span><span class="sxs-lookup"><span data-stu-id="4dbde-114">**WTSVirtualChannelClose**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelclose)
</dt> <dd>

<span data-ttu-id="4dbde-115">Schließt einen geöffneten virtuellen Kanal handle.</span><span class="sxs-lookup"><span data-stu-id="4dbde-115">Closes an open virtual channel handle.</span></span>

</dd> <dt>

[<span data-ttu-id="4dbde-116">**WGs virtualchannelpurgeinput**</span><span class="sxs-lookup"><span data-stu-id="4dbde-116">**WTSVirtualChannelPurgeInput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeinput)
</dt> <dd>

<span data-ttu-id="4dbde-117">Löscht alle in die Warteschlange eingereihten Eingabedaten, die vom Client an den Server in einem bestimmten virtuellen Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dbde-117">Deletes all queued input data sent from the client to the server on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="4dbde-118">Diese Funktion wird zurzeit nicht von Remotedesktopdienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="4dbde-118">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="4dbde-119">**Wzvirtualchannelpurgeoutput**</span><span class="sxs-lookup"><span data-stu-id="4dbde-119">**WTSVirtualChannelPurgeOutput**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelpurgeoutput)
</dt> <dd>

<span data-ttu-id="4dbde-120">Löscht alle in die Warteschlange eingereihten Ausgabedaten, die vom Server an den Client in einem bestimmten virtuellen Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="4dbde-120">Deletes all queued output data sent from the server to the client on a specific virtual channel.</span></span>

> [!Note]  
> <span data-ttu-id="4dbde-121">Diese Funktion wird zurzeit nicht von Remotedesktopdienste verwendet.</span><span class="sxs-lookup"><span data-stu-id="4dbde-121">This function currently is not used by Remote Desktop Services.</span></span>

 

</dd> <dt>

[<span data-ttu-id="4dbde-122">**Wout virtualchannelquery**</span><span class="sxs-lookup"><span data-stu-id="4dbde-122">**WTSVirtualChannelQuery**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelquery)
</dt> <dd>

<span data-ttu-id="4dbde-123">Gibt Informationen zu einem angegebenen virtuellen Kanal zurück.</span><span class="sxs-lookup"><span data-stu-id="4dbde-123">Returns information about a specified virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="4dbde-124">**Wout virtualchannelread**</span><span class="sxs-lookup"><span data-stu-id="4dbde-124">**WTSVirtualChannelRead**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelread)
</dt> <dd>

<span data-ttu-id="4dbde-125">Liest Daten vom Server Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="4dbde-125">Reads data from the server end of a virtual channel.</span></span>

</dd> <dt>

[<span data-ttu-id="4dbde-126">**Wout virtualchannelwrite**</span><span class="sxs-lookup"><span data-stu-id="4dbde-126">**WTSVirtualChannelWrite**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsvirtualchannelwrite)
</dt> <dd>

<span data-ttu-id="4dbde-127">Schreibt Daten auf das Server Ende eines virtuellen Kanals.</span><span class="sxs-lookup"><span data-stu-id="4dbde-127">Writes data to the server end of a virtual channel.</span></span>

</dd> </dl>

 

 




