---
title: Einrichten eines von der Quelle initiierten Abonnements
description: Mit Quellen initiierten Abonnements können Sie ein Abonnement auf einem Ereignis Sammler Computer definieren, ohne die Ereignis Quellcomputer zu definieren. Anschließend können mehrere Remote Ereignis Quellcomputer eingerichtet werden (mithilfe einer Gruppenrichtlinien Einstellung), um Ereignisse an den Ereignis Sammler Computer weiterzuleiten.
ms.assetid: c02b5075-d685-44cf-937f-a1edfd2550ca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 12/17/2018
ms.openlocfilehash: de31b23821fb1315a690612e5b337c5bb47a016d
ms.sourcegitcommit: 39a48585ed40e1cb466dcbf085847d0eb10f0da7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/04/2020
ms.locfileid: "104390116"
---
# <a name="setting-up-a-source-initiated-subscription"></a><span data-ttu-id="b231f-103">Einrichten eines von der Quelle initiierten Abonnements</span><span class="sxs-lookup"><span data-stu-id="b231f-103">Setting up a Source Initiated Subscription</span></span>

<span data-ttu-id="b231f-104">Mit Quellen initiierten Abonnements können Sie ein Abonnement auf einem Ereignis Sammler Computer definieren, ohne die Ereignis Quellcomputer zu definieren. Anschließend können mehrere Remote Ereignis Quellcomputer eingerichtet werden (mithilfe einer Gruppenrichtlinien Einstellung), um Ereignisse an den Ereignis Sammler Computer weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b231f-104">Source-initiated subscriptions allow you to define a subscription on an event collector computer without defining the event source computers, and then multiple remote event source computers can be set up (using a group policy setting) to forward events to the event collector computer.</span></span> <span data-ttu-id="b231f-105">Dies unterscheidet sich von einem vom Collector initiierten Abonnement, da der Ereignis Sammler im vom Collector initiierten Abonnement Modell alle Ereignis Quellen im Ereignis Abonnement definieren muss.</span><span class="sxs-lookup"><span data-stu-id="b231f-105">This differs from a collector initiated subscription because in the collector initiated subscription model, the event collector must define all the event sources in the event subscription.</span></span>

<span data-ttu-id="b231f-106">Beachten Sie beim Einrichten eines von der Quelle initiierten Abonnements, ob sich die Ereignis Quellcomputer in derselben Domäne wie der Ereignis Sammler Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="b231f-106">When setting up a source-initiated subscription, consider whether the event source computers are in the same domain as the event collector computer.</span></span> <span data-ttu-id="b231f-107">In den folgenden Abschnitten werden die Schritte beschrieben, die befolgt werden müssen, wenn sich die Ereignis Quellen in derselben Domäne oder nicht in derselben Domäne wie der Ereignis Sammler Computer befinden.</span><span class="sxs-lookup"><span data-stu-id="b231f-107">The following sections describe the steps to follow when the event sources are in the same domain or not in the same domain as the event collector computer.</span></span>

> [!Note]  
> <span data-ttu-id="b231f-108">Jeder Computer in einer Domäne, lokal oder Remote, kann ein Ereignis Sammler sein.</span><span class="sxs-lookup"><span data-stu-id="b231f-108">Any computer in a domain, local or remote, can be an event collector.</span></span> <span data-ttu-id="b231f-109">Bei der Auswahl eines Ereignis Sammlers ist es jedoch wichtig, einen Computer auszuwählen, der in der Nähe der Mehrzahl der Ereignisse liegt.</span><span class="sxs-lookup"><span data-stu-id="b231f-109">However, when choosing an event collector, it is important to select a machine that is topologically close to where the majority of the events will be generated.</span></span> <span data-ttu-id="b231f-110">Das Senden von Ereignissen an einen Computer an einem entfernten Netzwerk Speicherort in einem WAN kann die Gesamtleistung und Effizienz bei der Ereignis Erfassung verringern.</span><span class="sxs-lookup"><span data-stu-id="b231f-110">Sending events to a machine at a distant network location on a WAN can reduce overall performance and efficiency in event collection.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="b231f-111">Einrichten eines von der Quelle initiierten Abonnements, in dem sich die Ereignis Quellen in derselben Domäne wie der Ereignis Sammler Computer befinden</span><span class="sxs-lookup"><span data-stu-id="b231f-111">Setting up a source-initiated subscription where the event sources are in the same domain as the event collector computer</span></span>

<span data-ttu-id="b231f-112">Die Ereignis Quellcomputer und der Ereignis Sammler Computer müssen so konfiguriert werden, dass ein von der Quelle initiiertes Abonnement eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="b231f-112">Both the event source computers and the event collector computer must be configured to set up a source initiated subscription.</span></span>

> [!Note]  
> <span data-ttu-id="b231f-113">Bei diesen Anweisungen wird vorausgesetzt, dass Sie über Administrator Zugriff auf den Windows Server-Domänen Controller verfügen, der für die Domäne zuständig ist, in der der Remote Computer für die Erfassung von Ereignissen konfiguriert wird</span><span class="sxs-lookup"><span data-stu-id="b231f-113">These instructions assume that you have administrator access to the Windows Server domain controller serving the domain in which the remote computer or computers will be configured to collect events.</span></span>

### <a name="configuring-the-event-source-computer"></a><span data-ttu-id="b231f-114">Konfigurieren des Ereignis Quell Computers</span><span class="sxs-lookup"><span data-stu-id="b231f-114">Configuring the event source computer</span></span>

1. <span data-ttu-id="b231f-115">Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um Windows-Remoteverwaltung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-115">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="b231f-116">**WinRM-QC-q**</span><span class="sxs-lookup"><span data-stu-id="b231f-116">**winrm qc -q**</span></span>

2. <span data-ttu-id="b231f-117">Starten Sie die Gruppenrichtlinie, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="b231f-117">Start group policy by running the following command:</span></span>

    <span data-ttu-id="b231f-118">**% Systemroot% \\ system32 \\ gpeer dit. msc**</span><span class="sxs-lookup"><span data-stu-id="b231f-118">**%SYSTEMROOT%\\System32\\gpedit.msc**</span></span>

3. <span data-ttu-id="b231f-119">Erweitern Sie unter dem Knoten **Computer Konfiguration** den Knoten **Administrative Vorlagen** , erweitern Sie dann den Knoten **Windows-Komponenten** , und wählen Sie dann den Knoten **Ereignis Weiterleitung** aus.</span><span class="sxs-lookup"><span data-stu-id="b231f-119">Under the **Computer Configuration** node, expand the **Administrative Templates** node, then expand the **Windows Components** node, then select the **Event Forwarding** node.</span></span>

4. <span data-ttu-id="b231f-120">Klicken Sie mit der rechten Maustaste auf die Einstellung **Abonnement-Manager** , und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="b231f-120">Right-click the **SubscriptionManager** setting, and select **Properties**.</span></span> <span data-ttu-id="b231f-121">Aktivieren Sie die Einstellung " **Abonnement-Manager** ", und klicken Sie auf die Schaltfläche **anzeigen** , um der Einstellung eine Server Adresse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b231f-121">Enable the **SubscriptionManager** setting, and click the **Show** button to add a server address to the setting.</span></span> <span data-ttu-id="b231f-122">Fügen Sie mindestens eine Einstellung hinzu, die den Ereignis Sammler Computer angibt.</span><span class="sxs-lookup"><span data-stu-id="b231f-122">Add at least one setting that specifies the event collector computer.</span></span> <span data-ttu-id="b231f-123">Das **Eigenschaften** Fenster für den Abonnement-Manager enthält eine Registerkarte " **Erklärung** ", die die Syntax der Einstellung beschreibt.</span><span class="sxs-lookup"><span data-stu-id="b231f-123">The **SubscriptionManager Properties** window contains an **Explain** tab that describes the syntax for the setting.</span></span>

5. <span data-ttu-id="b231f-124">Nachdem die Einstellung für den **Abonnement-Manager** hinzugefügt wurde, führen Sie den folgenden Befehl aus, um sicherzustellen, dass die Richtlinie angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="b231f-124">After the **SubscriptionManager** setting has been added, run the following command to ensure the policy is applied:</span></span>

    <span data-ttu-id="b231f-125">**gpupdate /force**</span><span class="sxs-lookup"><span data-stu-id="b231f-125">**gpupdate /force**</span></span>

### <a name="configuring-the-event-collector-computer"></a><span data-ttu-id="b231f-126">Konfigurieren des Ereignis Sammler Computers</span><span class="sxs-lookup"><span data-stu-id="b231f-126">Configuring the event collector computer</span></span>

1. <span data-ttu-id="b231f-127">Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um Windows-Remoteverwaltung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-127">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to configure Windows Remote Management:</span></span>

    <span data-ttu-id="b231f-128">**WinRM-QC-q**</span><span class="sxs-lookup"><span data-stu-id="b231f-128">**winrm qc -q**</span></span>

2. <span data-ttu-id="b231f-129">Führen Sie den folgenden Befehl aus, um den Event Collector-Dienst zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-129">Run the following command to configure the Event Collector service:</span></span>

    <span data-ttu-id="b231f-130">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="b231f-130">**wecutil qc /q**</span></span>

3. <span data-ttu-id="b231f-131">Erstellen eines von der Quelle initiierten Abonnements</span><span class="sxs-lookup"><span data-stu-id="b231f-131">Create a source initiated subscription.</span></span> <span data-ttu-id="b231f-132">Dies kann entweder Programm gesteuert, mithilfe des Ereignisanzeige oder mithilfe [**Wecutil.exe**](wecutil.md)erfolgen.</span><span class="sxs-lookup"><span data-stu-id="b231f-132">This can either be done programmatically, by using the Event Viewer, or by using [**Wecutil.exe**](wecutil.md).</span></span> <span data-ttu-id="b231f-133">Weitere Informationen zum programmgesteuerten Erstellen des Abonnements finden Sie im Codebeispiel unter [Erstellen eines von der Quelle initiierten Abonnements](creating-a-source-initiated-subscription.md).</span><span class="sxs-lookup"><span data-stu-id="b231f-133">For more information about how to create the subscription programmatically, see the code example in [Creating a Source Initiated Subscription](creating-a-source-initiated-subscription.md).</span></span> <span data-ttu-id="b231f-134">Wenn Sie Wecutil.exe verwenden, müssen Sie eine XML-Datei mit Ereignis Abonnements erstellen und den folgenden Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="b231f-134">If you use Wecutil.exe, you must create an event subscription XML file and use the following command:</span></span>

    <span data-ttu-id="b231f-135">**wecutil** - *configurationFile.xml*</span><span class="sxs-lookup"><span data-stu-id="b231f-135">**wecutil cs** *configurationFile.xml*</span></span>

    <span data-ttu-id="b231f-136">Der folgende XML-Code ist ein Beispiel für den Inhalt einer Abonnement Konfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll auf dem Ereignis Sammler Computer weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="b231f-136">The following XML is an example of the contents of a subscription configuration file that creates a source-initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log on the event collector computer.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <SubscriptionId>SampleSISubscription</SubscriptionId>
        <SubscriptionType>SourceInitiated</SubscriptionType>
        <Description>Source Initiated Subscription Sample</Description>
        <Enabled>true</Enabled>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

        <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
        <ConfigurationMode>Custom</ConfigurationMode>

        <Delivery Mode="Push">
            <Batching>
                <MaxItems>1</MaxItems>
                <MaxLatencyTime>1000</MaxLatencyTime>
            </Batching>
            <PushSettings>
                <Heartbeat Interval="60000"/>
            </PushSettings>
        </Delivery>

        <Expires>2018-01-01T00:00:00.000Z</Expires>

        <Query>
            <![CDATA[
                <QueryList>
                    <Query Path="Application">
                        <Select>Event[System/EventID='999']</Select>
                    </Query>
                </QueryList>
            ]]>
        </Query>

        <ReadExistingEvents>true</ReadExistingEvents>
        <TransportName>http</TransportName>
        <ContentFormat>RenderedText</ContentFormat>
        <Locale Language="en-US"/>
        <LogFile>ForwardedEvents</LogFile>
        <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
        <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
    </Subscription>
    ```

    > [!Note]  
    > <span data-ttu-id="b231f-137">Beim Erstellen eines von der Quelle initiierten Abonnements, wenn "zugswedsourcedomaincomputers", "zugswedsourcenondomaincomputers/issuercalist", "zugswedsubjetlist" und "deniedsubjetlist" leer sind, dann "o:NSG: nsd: (a;; GA;;;D C) (A;; GA;;; NS) "wird als Standard Sicherheits Beschreibung für" zustellwedsourcedomaincomputers "verwendet.</span><span class="sxs-lookup"><span data-stu-id="b231f-137">When creating a source initiated subscription, if AllowedSourceDomainComputers, AllowedSourceNonDomainComputers/IssuerCAList, AllowedSubjectList, and DeniedSubjectList are all empty, then "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)" will be used as the default security descriptor for AllowedSourceDomainComputers.</span></span> <span data-ttu-id="b231f-138">Der Standard Deskriptor gewährt Mitgliedern der Domänen Gruppe Domänen Computer sowie der Gruppe lokaler Netzwerkdienst (für die lokale Weiterleitung) die Möglichkeit, Ereignisse für dieses Abonnement zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="b231f-138">The default descriptor grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

### <a name="to-validate-that-the-subscription-works-correctly"></a><span data-ttu-id="b231f-139">So überprüfen Sie, ob das Abonnement ordnungsgemäß funktioniert</span><span class="sxs-lookup"><span data-stu-id="b231f-139">To validate that the subscription works correctly</span></span>

1. <span data-ttu-id="b231f-140">Führen Sie auf dem Computer mit dem Ereignis Sammler die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="b231f-140">On the event collector computer complete the following steps:</span></span>

    1. <span data-ttu-id="b231f-141">Führen Sie den folgenden Befehl an einer Eingabeaufforderung mit erhöhten Rechten auf dem Windows Server-Domänen Controller aus, um den Lauf Zeit Status des Abonnements zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b231f-141">Run the following command from an elevated privilege command prompt on the Windows Server domain controller to get the runtime status of the subscription:</span></span>

        <span data-ttu-id="b231f-142">*&lt; Abonnement-ID &gt;* für **wecutil GR**</span><span class="sxs-lookup"><span data-stu-id="b231f-142">**wecutil gr** *&lt;subscriptionID&gt;*</span></span>

    2. <span data-ttu-id="b231f-143">Überprüfen Sie, ob die Ereignis Quelle verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="b231f-143">Verify that the event source has connected.</span></span> <span data-ttu-id="b231f-144">Möglicherweise müssen Sie warten, bis das Aktualisierungs Intervall, das in der Richtlinie angegeben ist, übersteigt, nachdem Sie das Abonnement erstellt haben, damit die Ereignis Quelle verbunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="b231f-144">You might need to wait until the refresh interval specified in the policy is over after you create the subscription for the event source to be connected.</span></span>
    3. <span data-ttu-id="b231f-145">Führen Sie den folgenden Befehl aus, um die Abonnement Informationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b231f-145">Run the following command to get the subscription information:</span></span>

        <span data-ttu-id="b231f-146">*&lt; Abonnement-ID &gt;* für **wecutil GS**</span><span class="sxs-lookup"><span data-stu-id="b231f-146">**wecutil gs** *&lt;subscriptionID&gt;*</span></span>

    4. <span data-ttu-id="b231f-147">Den Wert deliverymaxitems aus den Abonnement Informationen erhalten.</span><span class="sxs-lookup"><span data-stu-id="b231f-147">Get the DeliveryMaxItems value from the subscription information.</span></span>

2. <span data-ttu-id="b231f-148">Stellen Sie auf dem Ereignis Quellcomputer die Ereignisse aus dem Ereignis Abonnement aus, die der Abfrage entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b231f-148">On the event source computer, raise the events that match the query from the event subscription.</span></span> <span data-ttu-id="b231f-149">Die Anzahl der deliverymaxitems-Ereignisse muss ausgelöst werden, damit die Ereignisse weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b231f-149">The DeliveryMaxItems number of events must be raised for the events to be forwarded.</span></span>
3. <span data-ttu-id="b231f-150">Überprüfen Sie auf dem Ereignis Sammler Computer, ob die Ereignisse an das Protokoll ForwardedEvents oder an das im Abonnement angegebene Protokoll weitergeleitet wurden.</span><span class="sxs-lookup"><span data-stu-id="b231f-150">On the event collector computer, validate that the events have been forwarded to the ForwardedEvents log or to the log specified in the subscription.</span></span>

## <a name="forwarding-the-security-log"></a><span data-ttu-id="b231f-151">Weiterleiten des Sicherheitsprotokolls</span><span class="sxs-lookup"><span data-stu-id="b231f-151">Forwarding the security log</span></span>

<span data-ttu-id="b231f-152">Um das Sicherheitsprotokoll weiterleiten zu können, müssen Sie das Netzwerkdienst Konto der Gruppe "EventLog Readers" hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b231f-152">To be able to forward the Security log you need to add the NETWORK SERVICE account to the EventLog Readers group.</span></span>

## <a name="setting-up-a-source-initiated-subscription-where-the-event-sources-are-not-in-the-same-domain-as-the-event-collector-computer"></a><span data-ttu-id="b231f-153">Einrichten eines von der Quelle initiierten Abonnements, in dem sich die Ereignis Quellen nicht in derselben Domäne wie der Ereignis Sammler Computer befinden</span><span class="sxs-lookup"><span data-stu-id="b231f-153">Setting up a source initiated subscription where the event sources are not in the same domain as the event collector computer</span></span>

> [!Note]  
> <span data-ttu-id="b231f-154">Bei diesen Anweisungen wird davon ausgegangen, dass Sie über Administrator Zugriff auf einen Windows Server-Domänen Controller verfügen.</span><span class="sxs-lookup"><span data-stu-id="b231f-154">These instructions assume that you have administrator access to a Windows Server domain controller.</span></span> <span data-ttu-id="b231f-155">Da sich die Computer oder Computer der Remote-Ereignis Sammlung nicht in der vom Domänen Controller bereitgestellten Domäne befinden, müssen Sie in diesem Fall einen einzelnen Client starten, indem Sie Windows-Remoteverwaltung mithilfe der Dienste (Services. msc) auf "automatisch" festlegen.</span><span class="sxs-lookup"><span data-stu-id="b231f-155">In this case, since the remote event collector computer or computer(s) are not in the domain served by the domain controller, it is essential to start an individual client by setting Windows Remote Management to "automatic" using Services (services.msc).</span></span> <span data-ttu-id="b231f-156">Alternativ können Sie "WinRM quickconfig" auf jedem Remote Client ausführen.</span><span class="sxs-lookup"><span data-stu-id="b231f-156">Alternatively, you can run "winrm quickconfig" on each remote client.</span></span>

<span data-ttu-id="b231f-157">Die folgenden Voraussetzungen müssen erfüllt sein, bevor das Abonnement erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b231f-157">The following prerequisites must be met before the subscription is created.</span></span>

1. <span data-ttu-id="b231f-158">Führen Sie auf dem Ereignis Sammler Computer die folgenden Befehle an einer Eingabeaufforderung mit erhöhten Rechten aus, um Windows-Remoteverwaltung und den Ereignis Sammlungs Dienst zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-158">On the event collector computer, run the following commands from an elevated privilege command prompt to configure Windows Remote Management and the Event Collector service:</span></span>

    <span data-ttu-id="b231f-159">**WinRM-QC-q**</span><span class="sxs-lookup"><span data-stu-id="b231f-159">**winrm qc -q**</span></span>

    <span data-ttu-id="b231f-160">**wecutil QC/q**</span><span class="sxs-lookup"><span data-stu-id="b231f-160">**wecutil qc /q**</span></span>

2. <span data-ttu-id="b231f-161">Der Collector-Computer muss über ein Server Authentifizierungszertifikat (Zertifikat mit einem Server Authentifizierungs Zweck) in einem Zertifikat Speicher des lokalen Computers verfügen.</span><span class="sxs-lookup"><span data-stu-id="b231f-161">The collector computer should have a server authentication certificate (certificate with a server authentication purpose) in a local computer certificate store.</span></span>
3. <span data-ttu-id="b231f-162">Führen Sie auf dem Ereignis Quellcomputer den folgenden Befehl aus, um Windows-Remoteverwaltung zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-162">On the event source computer, run the following command to configure Windows Remote Management:</span></span>

    <span data-ttu-id="b231f-163">**WinRM-QC-q**</span><span class="sxs-lookup"><span data-stu-id="b231f-163">**winrm qc -q**</span></span>

4. <span data-ttu-id="b231f-164">Der Quellcomputer muss ein Client Authentifizierungszertifikat (Zertifikat mit einem Client Authentifizierungs Zweck) in einem Zertifikat Speicher des lokalen Computers haben.</span><span class="sxs-lookup"><span data-stu-id="b231f-164">The source machine should have a client authentication certificate (certificate with a client authentication purpose) in a local computer certificate store .</span></span>
5. <span data-ttu-id="b231f-165">Port 5986 wird auf dem Ereignis Sammler Computer geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b231f-165">Port 5986 is opened on the event collector computer.</span></span> <span data-ttu-id="b231f-166">Um diesen Port zu öffnen, führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="b231f-166">To open this port, run the command:</span></span>

    <span data-ttu-id="b231f-167">**netsh Firewall Add portopening TCP 5986 "WinRM HTTPS Remote Management"**</span><span class="sxs-lookup"><span data-stu-id="b231f-167">**netsh firewall add portopening TCP 5986 "Winrm HTTPS Remote Management"**</span></span>

### <a name="certificates-requirements"></a><span data-ttu-id="b231f-168">Zertifikat Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b231f-168">Certificates requirements</span></span>

- <span data-ttu-id="b231f-169">Auf dem Ereignis Sammler Computer muss ein Server Authentifizierungszertifikat im persönlichen Speicher des lokalen Computers installiert sein.</span><span class="sxs-lookup"><span data-stu-id="b231f-169">A server authentication certificate has to be installed on the Event Collector computer in the Personal store of the Local machine.</span></span> <span data-ttu-id="b231f-170">Der Betreff dieses Zertifikats muss dem FQDN des Sammlers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b231f-170">The subject of this certificate has to match the FQDN of the collector.</span></span>
- <span data-ttu-id="b231f-171">Ein Client Authentifizierungszertifikat muss auf den Ereignis Quell Computern im persönlichen Speicher des lokalen Computers installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b231f-171">A client authentication certificate has to be installed on the Event Source computers in the Personal store of the Local machine.</span></span> <span data-ttu-id="b231f-172">Der Betreff dieses Zertifikats muss dem FQDN des Computers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b231f-172">The subject of this certificate has to match the FQDN of the computer.</span></span>
- <span data-ttu-id="b231f-173">Wenn das Client Zertifikat von einer anderen Zertifizierungsstelle als der Ereignis Sammlung ausgestellt wurde, müssen die Stamm-und zwischen Zertifikate ebenfalls auf dem Ereignis Sammler installiert werden.</span><span class="sxs-lookup"><span data-stu-id="b231f-173">If the client certificate has been issued by a different Certification Authority than the one of the Event Collector then those Root and Intermediate certificates needs to be installed on the Event Collector as well.</span></span>
- <span data-ttu-id="b231f-174">Wenn das Client Zertifikat von einer zwischen Zertifizierungsstelle ausgestellt wurde und auf dem Collector Windows 2012 oder höher ausgeführt wird, müssen Sie den folgenden Registrierungsschlüssel konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="b231f-174">If the client certificate was issued by an Intermediate certification authority and the collector is running Windows 2012 or later you will have to configure the following registry key:</span></span>

    <span data-ttu-id="b231f-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span><span class="sxs-lookup"><span data-stu-id="b231f-175">**HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\Schannel\ClientAuthTrustMode (DWORD) = 2**</span></span>
 
- <span data-ttu-id="b231f-176">Vergewissern Sie sich, dass sowohl der Server als auch der Client den Sperr Status für alle Zertifikate erfolgreich überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="b231f-176">Verify that both the server and client are able to successfully check revocation status on all certificates.</span></span> <span data-ttu-id="b231f-177">Die Verwendung des **certutil** -Befehls kann bei der Problembehandlung hilfreich sein.</span><span class="sxs-lookup"><span data-stu-id="b231f-177">Use of the **certutil** command can assist in troubleshooting any errors.</span></span>

<span data-ttu-id="b231f-178">Weitere Informationen finden Sie in diesem Artikel: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span><span class="sxs-lookup"><span data-stu-id="b231f-178">Find more information in this article: https://technet.microsoft.com/library/dn786429(v=ws.11).aspx</span></span>

### <a name="setup-the-listener-on-the-event-collector"></a><span data-ttu-id="b231f-179">Einrichten des Listener auf dem Ereignis Sammler</span><span class="sxs-lookup"><span data-stu-id="b231f-179">Setup the listener on the Event collector</span></span>

1. <span data-ttu-id="b231f-180">Legen Sie die Zertifikat Authentifizierung mit dem folgenden Befehl fest:</span><span class="sxs-lookup"><span data-stu-id="b231f-180">Set the certificate authentication with the following command:</span></span>

    <span data-ttu-id="b231f-181">**WinRM Set WinRM/config/Service/auth @ {Certificate = "true"}**</span><span class="sxs-lookup"><span data-stu-id="b231f-181">**winrm set winrm/config/service/auth @{Certificate="true"}**</span></span>

2. <span data-ttu-id="b231f-182">Ein WinRM-HTTPS-Listener mit dem Fingerabdruck des Zertifikats für die Server Authentifizierung sollte auf dem Ereignis Sammler Computer vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="b231f-182">A WinRM HTTPS listener with the server authentication certificate thumb print should exist on the event collector computer.</span></span> <span data-ttu-id="b231f-183">Dies kann mit dem folgenden Befehl überprüft werden:</span><span class="sxs-lookup"><span data-stu-id="b231f-183">This can be verified with the following command:</span></span>

    <span data-ttu-id="b231f-184">**WinRM e WinRM/config/Listener**</span><span class="sxs-lookup"><span data-stu-id="b231f-184">**winrm e winrm/config/listener**</span></span>

3. <span data-ttu-id="b231f-185">Wenn der HTTPS-Listener nicht angezeigt wird, oder wenn der Thumb-Fingerabdruck des HTTPS-Listener nicht mit dem Fingerabdruck des Server Authentifizierungs Zertifikats auf dem Collector-Computer identisch ist, können Sie diesen Listener löschen und einen neuen mit dem richtigen Thumb-Druck erstellen.</span><span class="sxs-lookup"><span data-stu-id="b231f-185">If you do not see the HTTPS listener, or if the HTTPS listener's thumb print is not same as the thumb print of the server authentication certificate on collector computer, then you can delete that listener and create a new one with the correct thumb print.</span></span> <span data-ttu-id="b231f-186">Um den HTTPS-Listener zu löschen, verwenden Sie den folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="b231f-186">To delete the https listener, use the following command:</span></span>

    <span data-ttu-id="b231f-187">**WinRM-DELETE WinRM/config/Listener? Address = \* + Transport = HTTPS**</span><span class="sxs-lookup"><span data-stu-id="b231f-187">**winrm delete winrm/config/Listener?Address=\*+Transport=HTTPS**</span></span>

    <span data-ttu-id="b231f-188">Verwenden Sie den folgenden Befehl, um einen neuen Listener zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="b231f-188">To create a new listener, use the following command:</span></span>

    <span data-ttu-id="b231f-189">**WinRM erstellt WinRM/config/Listener? Address =&#42;+ Transport = HTTPS @ {Hostname = "** voll &lt; _qualifizierter Name des Sammlers_ &gt; **"; Certificatethbibprint = "** &lt; _Thumb Print des Server Authentifizierungs Zertifikats_ &gt; **"}**</span><span class="sxs-lookup"><span data-stu-id="b231f-189">**winrm create winrm/config/Listener?Address=&#42;+Transport=HTTPS @{Hostname="**&lt;_FQDN of the collector_&gt;**";CertificateThumbprint="**&lt;_Thumb print of the server authentication certificate_&gt;**"}**</span></span>

### <a name="configure-certificate-mapping-on-the-event-collector"></a><span data-ttu-id="b231f-190">Konfigurieren der Zertifikat Zuordnung für den Ereignis Sammler</span><span class="sxs-lookup"><span data-stu-id="b231f-190">Configure certificate mapping on the Event Collector</span></span>

1. <span data-ttu-id="b231f-191">Erstellen Sie einen neuen lokalen Benutzer, und fügen Sie ihn der lokalen Administrator Gruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="b231f-191">Create new local user and add it to the local Administrators group.</span></span>
2. <span data-ttu-id="b231f-192">Erstellen Sie die Zertifikat Zuordnung mithilfe eines Zertifikats, das auf dem Computer "Vertrauenswürdige Stamm Zertifizierungsstellen" oder "zwischen Zertifizierungsstellen" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b231f-192">Create the certificate mapping using a certificate that is present in the machine’s “Trusted Root Certification Authorities” or “Intermediate Certification Authorities”.</span></span>

    <span data-ttu-id="b231f-193">Dabei handelt es sich um das Zertifikat der Stamm-oder zwischen Zertifizierungsstelle, die die auf den Ereignis Quell Computern installierten Zertifikate ausgestellt *hat (um Verwirrung zu vermeiden, ist dies die Zertifizierungsstelle, die sich direkt oberhalb des Zertifikats in der Zertifikat Kette befindet)*:</span><span class="sxs-lookup"><span data-stu-id="b231f-193">This is the certificate of the Root or Intermediate CA that issued the certificates installed on the Event Source computers *(to avoid confusion, this is the CA immediately above the certificate in the certificate chain)*:</span></span>

    <span data-ttu-id="b231f-194">**WinRM erstellt WinRM/config/Service/certmapping? Aussteller** = &lt; _Fingerabdruck des ausstellenden Zertifizierungsstellen Zertifikats_ &gt; **+ Betreff =&#42;+ URI =&#42; @ {username = "** &lt; _username_ &gt; **"; Password = "** &lt; _Password_ &gt; **"}-Remote: localhost**</span><span class="sxs-lookup"><span data-stu-id="b231f-194">**winrm create winrm/config/service/certmapping?Issuer**=&lt;_Thumbprint of the issuing CA certificate_&gt;**+Subject=&#42;+URI=&#42; @{UserName="**&lt;_username_&gt;**";Password="**&lt;_password_&gt;**"} -remote:localhost**</span></span>

3. <span data-ttu-id="b231f-195">Testen Sie den Listener und die Zertifikat Zuordnung von einem Client mit dem folgenden Befehl:</span><span class="sxs-lookup"><span data-stu-id="b231f-195">From a client test the listener and the certificate mapping with the following command:</span></span>

    <span data-ttu-id="b231f-196">**WinRM g WinRM/config-r:https://** &lt; _Ereignis Sammler_ &gt; -voll qualifizierten Namen **: 5986-a:Certificate-Certificate: "** &lt; Finger _Abdruck des Client Authentifizierungs Zertifikats_ &gt; **"**</span><span class="sxs-lookup"><span data-stu-id="b231f-196">**winrm g winrm/config -r:https://**&lt;_Event Collector FQDN_&gt;**:5986 -a:certificate -certificate:"**&lt;_Thumbprint of the client authentication certificate_&gt;**"**</span></span>

    <span data-ttu-id="b231f-197">Dadurch sollte die WinRM-Konfiguration des Ereignis Sammlers zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b231f-197">This should return the WinRM configuration of the Event collector.</span></span> <span data-ttu-id="b231f-198">Verschieben Sie diesen Schritt **nicht** , wenn die Konfiguration nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="b231f-198">**Do not** move past this step if the configuration is not displayed.</span></span>

    <span data-ttu-id="b231f-199">**Was geschieht in diesem Schritt?**</span><span class="sxs-lookup"><span data-stu-id="b231f-199">**What happens at this step?**</span></span>
    - <span data-ttu-id="b231f-200">Der Client stellt eine Verbindung mit dem Ereignis Sammler her und sendet das angegebene Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="b231f-200">The client connects to the Event Collector and sends the specified certificate</span></span>
    - <span data-ttu-id="b231f-201">Die Ereignis Sammlung sucht nach der ausstellenden Zertifizierungsstelle und überprüft, ob eine übereinstimmende Zertifikat Zuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="b231f-201">The Event Collector looks for the issuing CA and checks if the is a matching certificate mapping</span></span>
    - <span data-ttu-id="b231f-202">Der Ereignis Sammler überprüft die Client Zertifikatskette und den Status der Widerruf enden Daten.</span><span class="sxs-lookup"><span data-stu-id="b231f-202">The Event Collector validates the client certificate chain and revocations status</span></span>
    - <span data-ttu-id="b231f-203">Wenn die oben genannten Schritte erfolgreich sind, ist die Authentifizierung abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b231f-203">If the above steps succeeds the authentication is completed.</span></span>

> [!NOTE]
> <span data-ttu-id="b231f-204">Möglicherweise erhalten Sie den Fehler "Zugriff verweigert", der sich über die Authentifizierungsmethode beschwert, was irreführend sein könnte.</span><span class="sxs-lookup"><span data-stu-id="b231f-204">You might get an Access denied error complaining about the authentication method, which could be misleading.</span></span> <span data-ttu-id="b231f-205">Um Probleme zu beheben, überprüfen Sie das CAPI-Protokoll auf dem Ereignis Sammler.</span><span class="sxs-lookup"><span data-stu-id="b231f-205">To troubleshoot, check the CAPI log on the Event Collector.</span></span>

4. <span data-ttu-id="b231f-206">Listet die konfigurierten certmapping-Einträge mit dem folgenden Befehl auf: **WinRM Enumeration WinRM/config/Service/certmapping**</span><span class="sxs-lookup"><span data-stu-id="b231f-206">List the configured certmapping entries with the command: **winrm enum winrm/config/service/certmapping**</span></span>

### <a name="event-source-computer-configuration"></a><span data-ttu-id="b231f-207">Konfiguration der Ereignis Quellcomputer</span><span class="sxs-lookup"><span data-stu-id="b231f-207">Event Source computer Configuration</span></span>

1. <span data-ttu-id="b231f-208">Melden Sie sich mit einem Administrator Konto an, und öffnen Sie die Editor für lokale Gruppenrichtlinien (gpeer dit. msc).</span><span class="sxs-lookup"><span data-stu-id="b231f-208">Logon with an administrator account and open the Local Group Policy Editor (gpedit.msc)</span></span>
2. <span data-ttu-id="b231f-209">Navigieren Sie zum lokalen Computer policy\computerkonfiguration\administrative Vorlagen\Windows-komponents\ereignisweiterleitung.</span><span class="sxs-lookup"><span data-stu-id="b231f-209">Navigate to the Local Computer Policy\Computer Configuration\Administrative Templates\Windows Components\Event Forwarding.</span></span>
3. <span data-ttu-id="b231f-210">Öffnen Sie die Richtlinie zum Konfigurieren der Server Adresse, des Aktualisierungs Intervalls und der Aussteller Zertifizierungsstelle einer Ziel Abonnement-Manager-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="b231f-210">Open “Configure the server address, refresh interval, and issuer certificate authority of a target Subscription Manager” policy.</span></span>
4. <span data-ttu-id="b231f-211">Aktivieren Sie die Richtlinie, und klicken Sie auf Abonnement-Manager "anzeigen...". gedrückt.</span><span class="sxs-lookup"><span data-stu-id="b231f-211">Enable the policy and click the SubscriptionManagers “Show...” button.</span></span>
5. <span data-ttu-id="b231f-212">Geben Sie im Fenster "Abonnement-Manager" die folgende Zeichenfolge ein:</span><span class="sxs-lookup"><span data-stu-id="b231f-212">In the SubscriptionManagers window enter the following string:</span></span>

    <span data-ttu-id="b231f-213">**Server = https://** &lt; Voll _qualifizierter Name des Ereignis Sammler Servers_ &gt; **: 5986/WSMAN/Abonnement-Manager/WEC, Refresh =** &lt; _Aktualisierungs Intervall in Sekunden_ &gt; **, Issuerca =** &lt; Finger _Abdruck des ausstellenden Zertifizierungsstellen Zertifikats_&gt;</span><span class="sxs-lookup"><span data-stu-id="b231f-213">**Server=HTTPS://**&lt;_FQDN of the Event Collector server_&gt;**:5986/wsman/SubscriptionManager/WEC,Refresh=** &lt;_Refresh interval in seconds_&gt;**,IssuerCA=**&lt;_Thumbprint of the issuing CA certificate_&gt;</span></span>

6. <span data-ttu-id="b231f-214">Führen Sie die folgende Befehlszeile aus, um die lokalen Gruppenrichtlinie Einstellungen zu aktualisieren: gpupdate/force</span><span class="sxs-lookup"><span data-stu-id="b231f-214">Run the following command line to refresh Local Group Policy settings:Gpupdate /force</span></span>
7. <span data-ttu-id="b231f-215">Diese Schritte sollten das Ereignis 104 auf dem Quellcomputer Ereignisanzeige Anwendungs-und dienstprotokolle\microsoft\windows\eventlog-forwardingplugin\operational Log mit folgender Meldung erstellen:</span><span class="sxs-lookup"><span data-stu-id="b231f-215">These steps should produce event 104 in your source computer Event Viewer Applications and Services Logs\Microsoft\Windows\Eventlog-ForwardingPlugin\Operational log with the following message:</span></span>

    <span data-ttu-id="b231f-216">"Die Weiterleitung hat erfolgreich eine Verbindung mit dem Abonnement-Manager am Adress- &lt; FQDN &gt; gefolgt von Ereignis 100 mit der folgenden Meldung hergestellt:" das Abonnement &lt; sub_name &gt; erfolgreich erstellt. "</span><span class="sxs-lookup"><span data-stu-id="b231f-216">"The forwarder has successfully connected to the subscription manager at address &lt;FQDN&gt;followed by event 100 with the message: "The subscription &lt;sub_name&gt; is created successfully."</span></span>

8. <span data-ttu-id="b231f-217">Auf dem Ereignis Sammler wird der Abonnement Lauf Zeit Status jetzt 1 aktiver Computer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b231f-217">On the Event Collector, the Subscription Runtime Status will show now 1 Active computer.</span></span>
9. <span data-ttu-id="b231f-218">Öffnen Sie das Protokoll ForwardedEvents auf dem Ereignis Sammler, und überprüfen Sie, ob die Ereignisse von den Quell Computern weitergeleitet wurden.</span><span class="sxs-lookup"><span data-stu-id="b231f-218">Open the ForwardedEvents log on the Event Collector and check if you have the events forwarded from the Source computers.</span></span>

### <a name="grant-permission-on-the-private-key-of-the-client-certificate-on-the-event-source"></a><span data-ttu-id="b231f-219">Erteilen Sie die Berechtigung für den privaten Schlüssel des Client Zertifikats für die Ereignis Quelle.</span><span class="sxs-lookup"><span data-stu-id="b231f-219">Grant permission on the private key of the client certificate on the Event Source</span></span>

1. <span data-ttu-id="b231f-220">Öffnen Sie die Zertifikat Verwaltungskonsole für den lokalen Computer auf dem Ereignis Quellcomputer.</span><span class="sxs-lookup"><span data-stu-id="b231f-220">Open the Certificates management console for Local machine on the Event Source computer.</span></span>
2. <span data-ttu-id="b231f-221">Klicken Sie mit der rechten Maustaste auf das Client Zertifikat, und verwalten Sie private Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b231f-221">Right click on the client certificate then Manage Private keys.</span></span>
3. <span data-ttu-id="b231f-222">Erteilen Sie dem Netzwerkdienst Benutzer Leseberechtigungen.</span><span class="sxs-lookup"><span data-stu-id="b231f-222">Grant Read permission to the NETWORK SERVICE user.</span></span>

### <a name="event-subscription-configuration"></a><span data-ttu-id="b231f-223">Konfiguration des Ereignis Abonnements</span><span class="sxs-lookup"><span data-stu-id="b231f-223">Event subscription configuration</span></span>

1. <span data-ttu-id="b231f-224">Öffnen Sie Ereignisanzeige in der Ereignis Sammlung, und navigieren Sie zum Knoten "Abonnements".</span><span class="sxs-lookup"><span data-stu-id="b231f-224">Open Event Viewer in the Event Collector and navigate to the Subscriptions node.</span></span>
2. <span data-ttu-id="b231f-225">Klicken Sie mit der rechten Maustaste auf Abonnements, und wählen Sie Abonnement erstellen... aus.</span><span class="sxs-lookup"><span data-stu-id="b231f-225">Right-click Subscriptions and choose “Create Subscription…”</span></span>
3. <span data-ttu-id="b231f-226">Benennen Sie einen Namen und eine optionale Beschreibung für das neue Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b231f-226">Give a name and an optional description for the new Subscription.</span></span>
4. <span data-ttu-id="b231f-227">Wählen Sie die Option "Quellcomputer initiiert" aus, und klicken Sie auf "Computer Gruppen auswählen...".</span><span class="sxs-lookup"><span data-stu-id="b231f-227">Select “Source computer initiated” option and click “Select Computer Groups…”.</span></span>
5. <span data-ttu-id="b231f-228">Klicken Sie in Computer Gruppen auf "nicht-Domänen Computer hinzufügen...".</span><span class="sxs-lookup"><span data-stu-id="b231f-228">In Computer Groups click on “Add Non-Domain Computers…”</span></span> <span data-ttu-id="b231f-229">und geben den Ereignis Quell Hostnamen ein.</span><span class="sxs-lookup"><span data-stu-id="b231f-229">and type the event source hostname.</span></span>
6. <span data-ttu-id="b231f-230">Klicken Sie auf "Zertifikate hinzufügen".</span><span class="sxs-lookup"><span data-stu-id="b231f-230">Click “Add Certificates…”</span></span> <span data-ttu-id="b231f-231">Fügen Sie das Zertifikat der Zertifizierungsstelle hinzu, von der die Client Zertifikate ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b231f-231">and add the certificate of the Certification authority that issue the client certificates.</span></span> <span data-ttu-id="b231f-232">Sie können in Zertifikat anzeigen klicken, um das Zertifikat zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b231f-232">You can click in View Certificate to validate the certificate.</span></span>
7. <span data-ttu-id="b231f-233">Klicken Sie in den Zertifizierungsstellen auf OK, um das Zertifikat hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b231f-233">In Certificate Authorities click OK to add the certificate.</span></span>
8. <span data-ttu-id="b231f-234">Klicken Sie nach dem Hinzufügen von Computern auf OK.</span><span class="sxs-lookup"><span data-stu-id="b231f-234">When finished adding Computers click OK.</span></span>
9. <span data-ttu-id="b231f-235">Klicken Sie zurück zu den Abonnement Eigenschaften, und klicken Sie auf Ereignisse auswählen...</span><span class="sxs-lookup"><span data-stu-id="b231f-235">Back to the Subscription Properties, click in Select Events...</span></span>
10. <span data-ttu-id="b231f-236">Konfigurieren Sie den Abfrage Filter Ereignisse, indem Sie die Ereignis Ebene (n), das Ereignisprotokoll (n) oder die Ereignis Quelle (en), die Ereignis-ID (en) und andere Filteroptionen angeben.</span><span class="sxs-lookup"><span data-stu-id="b231f-236">Configure the Events Query Filter by specifying the event level(s), event log(s) or event source(s), the event ID(s) and any other filtering options.</span></span>
11. <span data-ttu-id="b231f-237">Klicken Sie zurück zu den Abonnement Eigenschaften, und klicken Sie auf erweitert...</span><span class="sxs-lookup"><span data-stu-id="b231f-237">Back to the Subscription Properties, click on Advanced...</span></span>
12. <span data-ttu-id="b231f-238">Wählen Sie eine der Optimierungs Optionen für die Ereignis Übermittlung vom Quell Ereignis an den Ereignis Sammler aus, oder überlassen Sie die Standardeinstellung:</span><span class="sxs-lookup"><span data-stu-id="b231f-238">Choose one of the optimization options for event delivery from the Source Event to the Event Collector, or leave the default Normal:</span></span> 
    1. <span data-ttu-id="b231f-239">**Bandbreite minimieren**: die übermittelten Ereignisse werden weniger häufig verwendet, um Bandbreite zu sparen.</span><span class="sxs-lookup"><span data-stu-id="b231f-239">**Minimize Bandwidth**: Events will be delivered will less frequency to save bandwidth.</span></span>
    2. <span data-ttu-id="b231f-240">**Minimieren der Latenz**: Ereignisse werden bereitgestellt, sobald sie auftreten, um die Latenz von Ereignissen zu verringern.</span><span class="sxs-lookup"><span data-stu-id="b231f-240">**Minimize Latency**: Events will be delivered as soon as they occur to reduce events latency.</span></span>
13. <span data-ttu-id="b231f-241">Ändern Sie das Protokoll in HTTPS, und klicken Sie auf OK.</span><span class="sxs-lookup"><span data-stu-id="b231f-241">Change the Protocol to HTTPS and click OK.</span></span>
14. <span data-ttu-id="b231f-242">Klicken Sie auf OK, um das neue Abonnement zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b231f-242">Click OK to create the new subscription.</span></span>
15. <span data-ttu-id="b231f-243">Überprüfen Sie den Lauf Zeit Status des Abonnements, indem Sie mit der rechten Maustaste klicken und "Lauf Zeit Status" auswählen</span><span class="sxs-lookup"><span data-stu-id="b231f-243">Check the runtime status of the Subscription by right-clicking and choosing “Runtime Status”</span></span>
