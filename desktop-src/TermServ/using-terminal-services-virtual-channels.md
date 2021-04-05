---
title: Verwenden von Remotedesktopdienste virtuellen Kanälen
description: Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit.
ms.assetid: 3b378071-ebd6-47b0-8a9c-3e671505011a
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539eafca38c19855fdb057ceeb6e79cb4613773a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708753"
---
# <a name="using-remote-desktop-services-virtual-channels"></a><span data-ttu-id="4fcde-103">Verwenden von Remotedesktopdienste virtuellen Kanälen</span><span class="sxs-lookup"><span data-stu-id="4fcde-103">Using Remote Desktop Services virtual channels</span></span>

<span data-ttu-id="4fcde-104">Zum Implementieren eines virtuellen Kanals stellen Sie die Server-und Client Module der Anwendung eines virtuellen Kanals bereit.</span><span class="sxs-lookup"><span data-stu-id="4fcde-104">To implement a virtual channel, you provide the server and client modules of a virtual channel's application.</span></span> <span data-ttu-id="4fcde-105">Das Servermodul kann eine Benutzermodusanwendung oder ein Kernelmodustreiber sein.</span><span class="sxs-lookup"><span data-stu-id="4fcde-105">The server module can be a user-mode application or a kernel-mode driver.</span></span> <span data-ttu-id="4fcde-106">Das Client Modul muss eine DLL sein.</span><span class="sxs-lookup"><span data-stu-id="4fcde-106">The client module must be a DLL.</span></span>

<span data-ttu-id="4fcde-107">Beschreibungen dieser Module finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="4fcde-107">For descriptions of these modules, see the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4fcde-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4fcde-108">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="4fcde-109">Virtual Channel-Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="4fcde-109">Virtual Channel Server Application</span></span>](virtual-channel-server-application.md)
</dt> <dd>

<span data-ttu-id="4fcde-110">Das Servermodul einer Anwendung, die virtuelle Kanäle verwendet, muss eine Benutzermodusanwendung sein, die in einer Client Sitzung auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4fcde-110">The server module of an application that uses virtual channels must be a user-mode application running in a client session on the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="4fcde-111">Beachten Sie, dass Sie eine Methode zum Starten der Serveranwendung bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="4fcde-111">Note that you must provide a method to start the server application.</span></span>

</dd> <dt>

[<span data-ttu-id="4fcde-112">Client-DLL des virtuellen Kanals</span><span class="sxs-lookup"><span data-stu-id="4fcde-112">Virtual Channel Client DLL</span></span>](virtual-channel-client-dll.md)
</dt> <dd>

<span data-ttu-id="4fcde-113">Der Client einer virtuellen Channels-Anwendung ist eine DLL, die während der Remotedesktopdienste Initialisierung auf dem Client Computer geladen wird.</span><span class="sxs-lookup"><span data-stu-id="4fcde-113">The client of a virtual channels application is a DLL that is loaded during the Remote Desktop Services initialization on the client computer.</span></span> <span data-ttu-id="4fcde-114">Die dll muss auf dem Client Computer registriert werden.</span><span class="sxs-lookup"><span data-stu-id="4fcde-114">The DLL must be registered on the client computer.</span></span>

</dd> <dt>

[<span data-ttu-id="4fcde-115">Client Registrierung des virtuellen Kanals</span><span class="sxs-lookup"><span data-stu-id="4fcde-115">Virtual Channel Client Registration</span></span>](virtual-channel-client-registration.md)
</dt> <dd>

<span data-ttu-id="4fcde-116">Der Name der Client-DLL muss in der Registrierung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="4fcde-116">You must store the name of the client DLL in the registry.</span></span>

</dd> <dt>

[<span data-ttu-id="4fcde-117">Persistente virtuelle Kanäle für die Remote Steuerung</span><span class="sxs-lookup"><span data-stu-id="4fcde-117">Remote Control Persistent Virtual Channels</span></span>](remote-control-persistent-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="4fcde-118">Ein persistenter virtueller Kanal für die Remote Steuerung wird nicht geschlossen, wenn eine Remote Steuerung die Verbindung mit dem Client herstellt oder die Verbindung trennt.</span><span class="sxs-lookup"><span data-stu-id="4fcde-118">A remote control persistent virtual channel is not closed when a remote control connects or disconnects for the session connected to the client.</span></span> <span data-ttu-id="4fcde-119">Daten werden weiterhin über diesen Kanal übertragen und empfangen.</span><span class="sxs-lookup"><span data-stu-id="4fcde-119">Data will continue to be transmitted and received through this channel.</span></span>

</dd> <dt>

[<span data-ttu-id="4fcde-120">Dynamische virtuelle Kanäle</span><span class="sxs-lookup"><span data-stu-id="4fcde-120">Dynamic Virtual Channels</span></span>](dynamic-virtual-channels.md)
</dt> <dd>

<span data-ttu-id="4fcde-121">Die APIs des dynamischen virtuellen Kanals (DVC) erweitern die vorhandenen virtuellen Channel-APIs für Remotedesktopdienste, die als statische virtuelle Kanal-APIs bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4fcde-121">Dynamic virtual channel (DVC) APIs extend the existing virtual channel APIs for Remote Desktop Services, known as static virtual channel (SVC) APIs.</span></span>

</dd> </dl>

<span data-ttu-id="4fcde-122">Wenn Sie die Anwendung eines virtuellen Kanals in der Remotedesktopdienste-Bereitstellung aktiviert haben, können Sie die Anwendung auch Client Computern zur Verfügung stellen, die mithilfe des Remotedesktop ActiveX-Steuer Elements auf den RD-Sitzungshost Server zugreifen.</span><span class="sxs-lookup"><span data-stu-id="4fcde-122">If you have enabled a virtual channel's application in your Remote Desktop Services deployment, you can also make the application available to client computers that access the RD Session Host server by means of the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="4fcde-123">Weitere Informationen finden Sie unter [Verwenden des Remotedesktop ActiveX-Steuer Elements mit virtuellen Kanälen](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span><span class="sxs-lookup"><span data-stu-id="4fcde-123">For more information, see [Using the Remote Desktop ActiveX Control with Virtual Channels](using-the-remote-desktop-activex-control-with-virtual-channels.md).</span></span>

 

 




