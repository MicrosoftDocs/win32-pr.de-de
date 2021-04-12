---
title: Remotedesktop Virtualisierungsschnittstellen
description: Die Remotedesktop virtualisierungsapi unterstützt die folgenden Schnittstellen.
ms.assetid: 150a3c9a-d504-4854-adaa-92e3a7e8ea70
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26674bfb4af3d858ed914ea48e210c7506d5f454
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315740"
---
# <a name="remote-desktop-virtualization-interfaces"></a><span data-ttu-id="35571-103">Remotedesktop Virtualisierungsschnittstellen</span><span class="sxs-lookup"><span data-stu-id="35571-103">Remote Desktop Virtualization Interfaces</span></span>

<span data-ttu-id="35571-104">Die Remotedesktop virtualisierungsapi unterstützt die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="35571-104">The Remote Desktop Virtualization API supports the following interfaces.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="35571-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="35571-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="35571-106">**Itssbbasenotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-106">**ITsSbBaseNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbbasenotifysink)
</dt> <dd>

<span data-ttu-id="35571-107">Macht Methoden verfügbar, die Status-und Fehlermeldungen an Remotedesktopverbindung Broker (RD-Verbindungsbroker) melden.</span><span class="sxs-lookup"><span data-stu-id="35571-107">Exposes methods that report status and error messages to Remote Desktop Connection Broker (RD Connection Broker).</span></span>

</dd> <dt>

[<span data-ttu-id="35571-108">**Itssbclientconnection**</span><span class="sxs-lookup"><span data-stu-id="35571-108">**ITsSbClientConnection**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbclientconnection)
</dt> <dd>

<span data-ttu-id="35571-109">Macht Methoden und Eigenschaften verfügbar, die Zustandsinformationen über eine eingehende Verbindungsanforderung von einem Remotedesktopverbindung-Client (RDC) speichern.</span><span class="sxs-lookup"><span data-stu-id="35571-109">Exposes methods and properties that store state information about an incoming connection request from a Remote Desktop Connection (RDC) client.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-110">**Itssbclientconnectionpropertyset**</span><span class="sxs-lookup"><span data-stu-id="35571-110">**ITsSbClientConnectionPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbclientconnectionpropertyset)
</dt> <dd>

<span data-ttu-id="35571-111">Kann verwendet werden, um benutzerdefinierte Eigenschaften einer Client Verbindung nach Bedarf zu definieren.</span><span class="sxs-lookup"><span data-stu-id="35571-111">Can be used to define custom properties of a client connection as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-112">**Itssbenvironment**</span><span class="sxs-lookup"><span data-stu-id="35571-112">**ITsSbEnvironment**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbenvironment)
</dt> <dd>

<span data-ttu-id="35571-113">Macht Methoden und Eigenschaften verfügbar, die Informationen über die Umgebung enthalten, die den Zielcomputer hostet.</span><span class="sxs-lookup"><span data-stu-id="35571-113">Exposes methods and properties that contain information about the environment that hosts the target computer.</span></span> <span data-ttu-id="35571-114">Diese Schnittstelle kann zum Speichern von Informationen zu einem physischen Server verwendet werden, der virtuelle Maschinen hostet.</span><span class="sxs-lookup"><span data-stu-id="35571-114">This interface can be used to store information about a physical server that hosts virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-115">**Itssbenvironmentpropertyset**</span><span class="sxs-lookup"><span data-stu-id="35571-115">**ITsSbEnvironmentPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbenvironmentpropertyset)
</dt> <dd>

<span data-ttu-id="35571-116">Kann verwendet werden, um benutzerdefinierte Eigenschaften einer Umgebung zu definieren, die Zielcomputer nach Bedarf hostet.</span><span class="sxs-lookup"><span data-stu-id="35571-116">Can be used to define custom properties of an environment that hosts target computers as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-117">**Itssbfilterpluginstore**</span><span class="sxs-lookup"><span data-stu-id="35571-117">**ITsSbFilterPluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbfilterpluginstore)
</dt> <dd>

<span data-ttu-id="35571-118">Plug-in-Speicher</span><span class="sxs-lookup"><span data-stu-id="35571-118">Filter Plugin Store</span></span>

</dd> <dt>

[<span data-ttu-id="35571-119">**Itssbgenericnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-119">**ITsSbGenericNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbgenericnotifysink)
</dt> <dd>

<span data-ttu-id="35571-120">Macht Methoden verfügbar, die den Abschluss und die Wartezeit von der RD-Verbindungsbroker melden.</span><span class="sxs-lookup"><span data-stu-id="35571-120">Exposes methods that reports completion to and gets wait time from the RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-121">**Itssbglobalstore**</span><span class="sxs-lookup"><span data-stu-id="35571-121">**ITsSbGlobalStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbglobalstore)
</dt> <dd>

<span data-ttu-id="35571-122">Macht Methoden verfügbar, die Zielcomputer, Sitzungen, Umgebungen und Farmen Abfragen, die dem RD-Verbindungsbroker-Speicher hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="35571-122">Exposes methods that query for target computers, sessions, environments, and farms that have been added to the RD Connection Broker store.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-123">**Itssbloadbalanceresult**</span><span class="sxs-lookup"><span data-stu-id="35571-123">**ITsSbLoadBalanceResult**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalanceresult)
</dt> <dd>

<span data-ttu-id="35571-124">Macht Methoden und Eigenschaften verfügbar, die den von einem Lasten Ausgleichs Algorithmus zurückgegebenen Zielnamen speichern.</span><span class="sxs-lookup"><span data-stu-id="35571-124">Exposes methods and properties that store the target name returned by a load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-125">**Itssbloadbalancing**</span><span class="sxs-lookup"><span data-stu-id="35571-125">**ITsSbLoadBalancing**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancing)
</dt> <dd>

<span data-ttu-id="35571-126">Macht Methoden verfügbar, die Sie verwenden können, um einen benutzerdefinierten Lasten Ausgleichs Algorithmus bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="35571-126">Exposes methods you can use to provide a custom load-balancing algorithm.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-127">**Itssbloadbalancingnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-127">**ITsSbLoadBalancingNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbloadbalancingnotifysink)
</dt> <dd>

<span data-ttu-id="35571-128">Macht Methoden verfügbar, die das Ergebnis eines Lasten Ausgleichs Algorithmus zum RD-Verbindungsbroker zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="35571-128">Exposes methods that return the result of a load-balancing algorithm to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-129">**Itssborchestration**</span><span class="sxs-lookup"><span data-stu-id="35571-129">**ITsSbOrchestration**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestration)
</dt> <dd>

<span data-ttu-id="35571-130">Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um sicherzustellen, dass das Ziel bereit ist, bevor ein Client dorthin umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="35571-130">Exposes methods that RD Connection Broker uses to ensure that the target is ready before a client is redirected to it.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-131">**Itssborchestrationnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-131">**ITsSbOrchestrationNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssborchestrationnotifysink)
</dt> <dd>

<span data-ttu-id="35571-132">Macht Methoden verfügbar, die ein [**itssbtarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) -Objekt an RD-Verbindungsbroker zurückgeben, nachdem das Ziel erfolgreich für eine Verbindung vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="35571-132">Exposes methods that return an [**ITsSbTarget**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget) object to RD Connection Broker after the target is successfully prepared for a connection.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-133">**Itssbplacement**</span><span class="sxs-lookup"><span data-stu-id="35571-133">**ITsSbPlacement**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacement)
</dt> <dd>

<span data-ttu-id="35571-134">Macht Methoden verfügbar, mit denen die Umgebung (der Computer, der die virtuelle Maschine hostet) vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="35571-134">Exposes methods that prepare the environment (the computer that hosts the virtual machine).</span></span>

</dd> <dt>

[<span data-ttu-id="35571-135">**Itssbplacementnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-135">**ITsSbPlacementNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplacementnotifysink)
</dt> <dd>

<span data-ttu-id="35571-136">Macht Methoden verfügbar, die Informationen zu Umgebungen zurückgeben, die RD-Verbindungsbroker werden.</span><span class="sxs-lookup"><span data-stu-id="35571-136">Exposes methods that return information about environments to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-137">**Itssbplugin**</span><span class="sxs-lookup"><span data-stu-id="35571-137">**ITsSbPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbplugin)
</dt> <dd>

<span data-ttu-id="35571-138">Macht Methoden verfügbar, die Plug-ins initialisieren und beenden.</span><span class="sxs-lookup"><span data-stu-id="35571-138">Exposes methods that initialize and terminate plug-ins.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-139">**Itssbpluginnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-139">**ITsSbPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbpluginnotifysink)
</dt> <dd>

<span data-ttu-id="35571-140">Macht Methoden verfügbar, die RD-Verbindungsbroker über die Initialisierung oder Beendigung eines Plug-ins benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="35571-140">Exposes methods that notify RD Connection Broker about initialization or termination of a plug-in.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-141">**Itssbpluginpropertyset**</span><span class="sxs-lookup"><span data-stu-id="35571-141">**ITsSbPluginPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpluginpropertyset)
</dt> <dd>

<span data-ttu-id="35571-142">Kann verwendet werden, um nach Bedarf benutzerdefinierte Plug-in-Eigenschaften zu definieren.</span><span class="sxs-lookup"><span data-stu-id="35571-142">Can be used to define custom plug-in properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-143">**Itssbpropertyset**</span><span class="sxs-lookup"><span data-stu-id="35571-143">**ITsSbPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbpropertyset)
</dt> <dd>

<span data-ttu-id="35571-144">Kann verwendet werden, um benutzerdefinierte Eigenschaften nach Bedarf zu definieren.</span><span class="sxs-lookup"><span data-stu-id="35571-144">Can be used to define custom properties as appropriate.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-145">**Itssbprovider**</span><span class="sxs-lookup"><span data-stu-id="35571-145">**ITsSbProvider**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovider)
</dt> <dd>

<span data-ttu-id="35571-146">Macht Methoden verfügbar, mit denen Standard Implementierungen von Objekten erstellt werden, die in Remotedesktop Virtualisierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35571-146">Exposes methods that create default implementations of objects that are used in Remote Desktop Virtualization.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-147">**Itssbprovisioning**</span><span class="sxs-lookup"><span data-stu-id="35571-147">**ITsSbProvisioning**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioning)
</dt> <dd>

<span data-ttu-id="35571-148">Macht Methoden verfügbar, mit denen virtuelle Maschinen erstellt und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="35571-148">Exposes methods that create and maintain virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-149">**Itssbprovisioningpluginnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-149">**ITsSbProvisioningPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbprovisioningpluginnotifysink)
</dt> <dd>

<span data-ttu-id="35571-150">Macht Methoden verfügbar, die RD-Verbindungsbroker über die Bereitstellung virtueller Maschinen benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="35571-150">Exposes methods that notify RD Connection Broker about the provisioning of virtual machines.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-151">**Itssbresourcenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="35571-151">**ITsSbResourceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotification)
</dt> <dd>

<span data-ttu-id="35571-152">Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die in den Sitzungs-, Ziel-und Client Verbindungs Objekten auftreten.</span><span class="sxs-lookup"><span data-stu-id="35571-152">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-153">**Itssbresourcenotificationex**</span><span class="sxs-lookup"><span data-stu-id="35571-153">**ITsSbResourceNotificationEx**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcenotificationex)
</dt> <dd>

<span data-ttu-id="35571-154">Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die in den Sitzungs-, Ziel-und Client Verbindungs Objekten auftreten.</span><span class="sxs-lookup"><span data-stu-id="35571-154">Exposes methods that RD Connection Broker uses to notify plug-ins of any state changes that occur in the session, target, and client connection objects.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-155">**Itssbresourceplugin**</span><span class="sxs-lookup"><span data-stu-id="35571-155">**ITsSbResourcePlugin**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbresourceplugin)
</dt> <dd>

<span data-ttu-id="35571-156">Macht Methoden verfügbar, mit denen die Funktionen von RD-Verbindungsbroker erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="35571-156">Exposes methods that extend the capabilities of RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-157">**Itssbresourcepluginstore**</span><span class="sxs-lookup"><span data-stu-id="35571-157">**ITsSbResourcePluginStore**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbresourcepluginstore)
</dt> <dd>

<span data-ttu-id="35571-158">Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.</span><span class="sxs-lookup"><span data-stu-id="35571-158">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-159">**Itssbresourcepluginstoreex**</span><span class="sxs-lookup"><span data-stu-id="35571-159">**ITsSbResourcePluginStoreEx**</span></span>](itssbresourcepluginstoreex.md)
</dt> <dd>

<span data-ttu-id="35571-160">Macht Methoden verfügbar, mit denen Ressourcen-Plug-ins Objekte wie Sitzungen und Ziele speichern können.</span><span class="sxs-lookup"><span data-stu-id="35571-160">Exposes methods that enable resource plug-ins to store objects such as sessions and targets.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-161">**Itssbservicenotifizierung**</span><span class="sxs-lookup"><span data-stu-id="35571-161">**ITsSbServiceNotification**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbservicenotification)
</dt> <dd>

<span data-ttu-id="35571-162">Macht Methoden verfügbar, die von RD-Verbindungsbroker verwendet werden, um die Plug-ins von Zustandsänderungen zu benachrichtigen, die im RD-Verbindungsbroker selbst auftreten.</span><span class="sxs-lookup"><span data-stu-id="35571-162">Exposes methods that RD Connection Broker uses to notify plug-ins of state changes that occur in the RD Connection Broker itself.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-163">**Itssbsession**</span><span class="sxs-lookup"><span data-stu-id="35571-163">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> <dd>

<span data-ttu-id="35571-164">Macht Eigenschaften verfügbar, die Informationen zu einer Benutzersitzung speichern.</span><span class="sxs-lookup"><span data-stu-id="35571-164">Exposes properties that store information about a user session.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-165">**Itssbtarget**</span><span class="sxs-lookup"><span data-stu-id="35571-165">**ITsSbTarget**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtarget)
</dt> <dd>

<span data-ttu-id="35571-166">Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.</span><span class="sxs-lookup"><span data-stu-id="35571-166">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-167">**Itssbtargetex**</span><span class="sxs-lookup"><span data-stu-id="35571-167">**ITsSbTargetEx**</span></span>](itssbtargetex.md)
</dt> <dd>

<span data-ttu-id="35571-168">Macht Eigenschaften verfügbar, die Konfigurations-und Zustandsinformationen zu einem Ziel speichern.</span><span class="sxs-lookup"><span data-stu-id="35571-168">Exposes properties that store configuration and state information about a target.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-169">**Itssbtargetpropertyset**</span><span class="sxs-lookup"><span data-stu-id="35571-169">**ITsSbTargetPropertySet**</span></span>](/windows/win32/api/sbtsv/nn-sbtsv-itssbtargetpropertyset)
</dt> <dd>

<span data-ttu-id="35571-170">Leiten Sie von dieser Schnittstelle ab, um einen benutzerdefinierten Zieleigenschaften Satz zu definieren.</span><span class="sxs-lookup"><span data-stu-id="35571-170">Derive from this interface to define a custom target property set.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-171">**Itssbtaskinfo**</span><span class="sxs-lookup"><span data-stu-id="35571-171">**ITsSbTaskInfo**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskinfo)
</dt> <dd>

<span data-ttu-id="35571-172">Macht Eigenschaften verfügbar, die vom Remotedesktopverbindung Broker zum Festlegen der Warteschlange eines Plug-ins verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="35571-172">Exposes properties that the Remote Desktop Connection Broker uses to set a plugin’s queue.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-173">**Itssbtaskplugin**</span><span class="sxs-lookup"><span data-stu-id="35571-173">**ITsSbTaskPlugin**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskplugin)
</dt> <dd>

<span data-ttu-id="35571-174">Macht Methoden verfügbar, die die Aufgaben Warteschlange für Remotedesktopverbindung Broker-Plug-ins aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="35571-174">Exposes methods that update the queue of tasks for Remote Desktop Connection Broker plugins.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-175">**Itssbtaskpluginnotifysink**</span><span class="sxs-lookup"><span data-stu-id="35571-175">**ITsSbTaskPluginNotifySink**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)
</dt> <dd>

<span data-ttu-id="35571-176">Macht Methoden verfügbar, die Status-und Fehlermeldungen zu zu RD-Verbindungsbroker Tasks melden.</span><span class="sxs-lookup"><span data-stu-id="35571-176">Exposes methods that report status and error messages about tasks to RD Connection Broker.</span></span>

</dd> <dt>

[<span data-ttu-id="35571-177">**Iwtssbplugin**</span><span class="sxs-lookup"><span data-stu-id="35571-177">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> <dd>

<span data-ttu-id="35571-178">Wird verwendet, um die Funktionen des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="35571-178">Used to extend the capabilities of Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="35571-179">Implementieren Sie diese Schnittstelle, wenn Sie ein Plug-in bereitstellen möchten, das die Umleitungs Logik des TS-Sitzungs Brokers überschreibt.</span><span class="sxs-lookup"><span data-stu-id="35571-179">Implement this interface when you want to provide a plug-in that overrides the redirection logic of TS Session Broker.</span></span>

</dd> </dl>

 

 