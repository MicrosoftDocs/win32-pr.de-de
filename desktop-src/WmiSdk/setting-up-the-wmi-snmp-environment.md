---
description: Die Kommunikation mit einem Netzwerkgerät mithilfe der WMI-SNMP-Schnittstelle erfordert die Konfiguration des Geräts, des SNMP-Diensts und des WMI-Diensts. In den Informationen in diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.
ms.assetid: 8074175a-af66-49b2-9723-dfb38a08fb63
ms.tgt_platform: multiple
title: Einrichten der WMI-SNMP-Umgebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eeed470b1e38bf853bd6b023fa0f07b01c5df47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349228"
---
# <a name="setting-up-the-wmi-snmp-environment"></a><span data-ttu-id="c215b-104">Einrichten der WMI-SNMP-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c215b-104">Setting up the WMI SNMP Environment</span></span>

<span data-ttu-id="c215b-105">Die Kommunikation mit einem Netzwerkgerät mithilfe der WMI-SNMP-Schnittstelle erfordert die Konfiguration des Geräts, des SNMP-Diensts und des WMI-Diensts.</span><span class="sxs-lookup"><span data-stu-id="c215b-105">Communicating with a network device using the WMI SNMP interface requires the configuration of the device, SNMP, and WMI services.</span></span> <span data-ttu-id="c215b-106">In den Informationen in diesem Thema wird erläutert, wie Sie die WMI-SNMP-Umgebung einrichten.</span><span class="sxs-lookup"><span data-stu-id="c215b-106">The information in this topic explains how to set up the WMI SNMP environment.</span></span>

<span data-ttu-id="c215b-107">In diesem Thema werden die folgenden Abschnitte erläutert:</span><span class="sxs-lookup"><span data-stu-id="c215b-107">The following sections are discussed in this topic:</span></span>

## <a name="installing-the-snmp-provider"></a><span data-ttu-id="c215b-108">Installieren des SNMP-Anbieters</span><span class="sxs-lookup"><span data-stu-id="c215b-108">Installing the SNMP Provider</span></span>

<span data-ttu-id="c215b-109">Der SNMP-Dienst ist standardmäßig nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c215b-109">The SNMP service is not enabled by default.</span></span> <span data-ttu-id="c215b-110">Sie können den SNMP-Dienst und den WMI-SNMP-Anbieter über die Systemsteuerung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c215b-110">You can enable the SNMP service and the WMI SNMP Provider through the Control Panel.</span></span> <span data-ttu-id="c215b-111">Beachten Sie, dass der SNMP-Dienst aktiviert und ausgeführt werden muss, damit der WMI-SNMP-Anbieter funktioniert.</span><span class="sxs-lookup"><span data-stu-id="c215b-111">Be aware that the SNMP service must be enabled and running for the WMI SNMP provider to work.</span></span>

<span data-ttu-id="c215b-112">Verwenden Sie ab Windows Vista das folgende Verfahren, um den SNMP-Anbieter zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c215b-112">Starting with Windows Vista, use the following procedure to install the SNMP provider.</span></span>

<span data-ttu-id="c215b-113">**So installieren Sie den SNMP-Anbieter**</span><span class="sxs-lookup"><span data-stu-id="c215b-113">**To install the SNMP Provider**</span></span>

1.  <span data-ttu-id="c215b-114">Wählen Sie in der **Systemsteuerung** **Programme** aus.</span><span class="sxs-lookup"><span data-stu-id="c215b-114">From the **Control Panel**, select **Programs**.</span></span>
2.  <span data-ttu-id="c215b-115">Wählen Sie unter **Programme und Funktionen** die Option Windows-Funktionen ein- **oder ausschalten** aus.</span><span class="sxs-lookup"><span data-stu-id="c215b-115">Under **Programs and Features**, select **Turn Windows features on or off**.</span></span>
3.  <span data-ttu-id="c215b-116">Scrollen Sie in der Liste Windows-Features nach unten zu **SNMP-Feature** , und erweitern Sie die Liste, sodass Sie den **WMI-SNMP-Anbieter** sehen können.</span><span class="sxs-lookup"><span data-stu-id="c215b-116">In the Windows features list, scroll down to **SNMP feature** and expand the list so that you can see **WMI SNMP Provider**.</span></span>
4.  <span data-ttu-id="c215b-117">Aktivieren Sie das Kontrollkästchen für den **WMI-SNMP-Anbieter**.</span><span class="sxs-lookup"><span data-stu-id="c215b-117">Select the check box for **WMI SNMP Provider**.</span></span> <span data-ttu-id="c215b-118">Das Kontrollkästchen für das **SNMP-Feature** wird automatisch ausgewählt, da der Anbieter SNMP erfordert.</span><span class="sxs-lookup"><span data-stu-id="c215b-118">The check box for **SNMP feature** is selected automatically because the provider requires SNMP.</span></span>
5.  <span data-ttu-id="c215b-119">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c215b-119">Click **OK**.</span></span>
6.  <span data-ttu-id="c215b-120">Führen Sie an einer Eingabeaufforderung oder im **Startmenü** Services. msc aus, und vergewissern Sie sich, dass der SNMP-Dienst gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="c215b-120">From a command prompt or the **Start** menu, run Services.msc and ensure that the SNMP service is started.</span></span>

## <a name="creating-an-snmp-namespace"></a><span data-ttu-id="c215b-121">Erstellen eines SNMP-Namespace</span><span class="sxs-lookup"><span data-stu-id="c215b-121">Creating an SNMP Namespace</span></span>

<span data-ttu-id="c215b-122">Ein SNMP-Namespace definiert eine Ansicht eines Netzwerkgeräts.</span><span class="sxs-lookup"><span data-stu-id="c215b-122">An SNMP namespace defines a view of a network device.</span></span>

> [!Note]  
> <span data-ttu-id="c215b-123">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="c215b-123">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="c215b-124">Im folgenden Verfahren wird beschrieben, wie Sie einen SNMP-WMI- [*Namespace*](gloss-n.md)erstellen.</span><span class="sxs-lookup"><span data-stu-id="c215b-124">The following procedure describes how to create an SNMP WMI [*namespace*](gloss-n.md).</span></span>

<span data-ttu-id="c215b-125">**So erstellen Sie einen SNMP-Namespace**</span><span class="sxs-lookup"><span data-stu-id="c215b-125">**To create an SNMP namespace**</span></span>

1.  <span data-ttu-id="c215b-126">Erstellen Sie eine Instanz der [**\_ \_ Namespace**](--namespace.md) -System Klasse, indem Sie entweder eine [*Managed Object Format*](gloss-m.md) . MOF-Datei kompilieren oder die [com-API für WMI](com-api-for-wmi.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="c215b-126">Create an instance of the [**\_\_Namespace**](--namespace.md) system class either by compiling a [*Managed Object Format*](gloss-m.md) .mof file or by using the [COM API for WMI](com-api-for-wmi.md).</span></span>

    <span data-ttu-id="c215b-127">Weitere Informationen finden Sie unter [Erstellen von Hierarchien in WMI](creating-hierarchies-within-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="c215b-127">For more information, see [Creating Hierarchies Within WMI](creating-hierarchies-within-wmi.md).</span></span>

2.  <span data-ttu-id="c215b-128">Ordnen Sie SNMP-Anbieter [*Qualifizierer*](gloss-q.md) der Namespace Definition zu.</span><span class="sxs-lookup"><span data-stu-id="c215b-128">Associate SNMP provider [*qualifiers*](gloss-q.md) with the namespace definition.</span></span>

    <span data-ttu-id="c215b-129">Die SNMP-Anbieter Qualifizierer enthalten Implementierungs spezifische Kontextinformationen und Transporteigenschaften, die definieren, wie der SNMP-Anbieter auf ein SNMP-Gerät zugreift.</span><span class="sxs-lookup"><span data-stu-id="c215b-129">The SNMP provider qualifiers contain implementation-specific context information and transport properties that define how the SNMP provider accesses an SNMP device.</span></span> <span data-ttu-id="c215b-130">Weitere Informationen finden Sie unter [**Qualifizierer für den SNMP-Anbieter**](qualifiers-specific-to-the-snmp-provider.md).</span><span class="sxs-lookup"><span data-stu-id="c215b-130">For more information, see [**Qualifiers Specific to the SNMP Provider**](qualifiers-specific-to-the-snmp-provider.md).</span></span>

3.  <span data-ttu-id="c215b-131">Verwenden Sie das Befehlszeilen Tool " [wfcomp](mofcomp.md) ", um den MOF-Code in das WMI-Repository zu laden.</span><span class="sxs-lookup"><span data-stu-id="c215b-131">Use the [mofcomp](mofcomp.md) command line tool to load the MOF code into the WMI repository.</span></span>

    <span data-ttu-id="c215b-132">Weitere Informationen finden Sie unter [Kompilieren von MOF-Dateien](compiling-mof-files.md).</span><span class="sxs-lookup"><span data-stu-id="c215b-132">For more information, see [Compiling MOF files](compiling-mof-files.md).</span></span>

<span data-ttu-id="c215b-133">Im folgenden MOF-Codebeispiel \\ wird der SNMP--Namespace mit einer Teilmenge der Qualifizierer definiert, die einem SNMP--Namespace zugeordnet werden können.</span><span class="sxs-lookup"><span data-stu-id="c215b-133">The following MOF code example defines the \\snmp namespace with a subset of the qualifiers that can be associated with an SNMP namespace.</span></span>

``` syntax
// Load classes and instances into <\\.\root> namespace

#pragma namespace("\\\\.\\root")               

[ 
  AgentAddress( "localhost" ), 
  AgentReadCommunityName( "public"), 
  AgentWriteCommunityName( "private"), 
  AgentRetryCount( 1 ), 
  AgentRetryTimeout( 500 ), 
  AgentVarBindsPerPdu( 10 ),
  AgentFlowControlWindowSize ( 3 ) 
]

  instance of __Namespace
  {
      Name = "snmp" ;
  };
```

## <a name="inserting-snmp-mib-data-into-wmi"></a><span data-ttu-id="c215b-134">Einfügen von SNMP-MIB-Daten in WMI</span><span class="sxs-lookup"><span data-stu-id="c215b-134">Inserting SNMP MIB Data into WMI</span></span>

<span data-ttu-id="c215b-135">Als Anbieter fungiert der SNMP-Anbieter als Brücke zwischen SNMP-Daten und WMI-Klassen.</span><span class="sxs-lookup"><span data-stu-id="c215b-135">As a provider, the SNMP provider acts as a bridge between SNMP data and WMI classes.</span></span> <span data-ttu-id="c215b-136">Daher müssen Sie über Klassen in WMI verfügen, die unterschiedliche Aspekte eines SNMP-fähigen Geräts darstellen.</span><span class="sxs-lookup"><span data-stu-id="c215b-136">Therefore, you must have classes in WMI that represent different aspects of an SNMP-enabled device.</span></span> <span data-ttu-id="c215b-137">Hierzu müssen Sie den SNMP-Informationsmodul Compiler ([Smi2smir](smi2smir.md)) verwenden, um SNMP-Verwaltungsinformationen aus dem SNMP-Format in die entsprechenden CIM-Schema Definitionen zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="c215b-137">To do so, you must use the SNMP information module compiler ([smi2smir](smi2smir.md)) to compile SNMP management information from the SNMP format into the equivalent CIM schema definitions.</span></span> <span data-ttu-id="c215b-138">Anschließend können Sie die Ausgabe des Informations Compilers in eine SNMP-Schema Datenbank mit dem Namen "SNMP Module Information Repository (SMIR)" oder mehrere verschiedene Arten von MOF-Dateien weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="c215b-138">You can then direct the output of the information compiler into an SNMP schema database called the "SNMP Module Information Repository (SMIR)" or to several different kinds of MOF files.</span></span>

<span data-ttu-id="c215b-139">Der Compiler wird im Befehlszeilen Modus ausgeführt, wobei eine MIB-Datei als Eingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c215b-139">The compiler runs in the command-line mode, using one MIB file as input.</span></span> <span data-ttu-id="c215b-140">Mit dem folgenden Befehl wird die angegebene MIB-Datei in SMIR geladen.</span><span class="sxs-lookup"><span data-stu-id="c215b-140">The following command loads the specified MIB file into the SMIR.</span></span>

<span data-ttu-id="c215b-141">\**Smi2smir/a\*\*\*<MIB file>*</span><span class="sxs-lookup"><span data-stu-id="c215b-141">**smi2smir /a** *<MIB file>*</span></span>

## <a name="setting-up-snmp-communities"></a><span data-ttu-id="c215b-142">Einrichten von SNMP-Communitys</span><span class="sxs-lookup"><span data-stu-id="c215b-142">Setting Up SNMP Communities</span></span>

<span data-ttu-id="c215b-143">Als Sicherheitsmaßnahme wird die öffentliche SNMP-Community standardmäßig nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="c215b-143">As a security measure, the SNMP "public" community is not created by default.</span></span> <span data-ttu-id="c215b-144">Sie können die Community erstellen, wie unter [](/previous-versions/windows/embedded/ms907028(v=msdn.10))communityregistrierungseinstellungen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c215b-144">You can create the community as described in [Communities Registry Settings](/previous-versions/windows/embedded/ms907028(v=msdn.10)).</span></span> <span data-ttu-id="c215b-145">Wenn Sie keine Community haben, erstellen Sie die Public-Community für den Zugriff auf den SNMP-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="c215b-145">If you do not have any community, then create the "public" community to access the SNMP provider.</span></span>

## <a name="generating-mof-files-from-mib-files"></a><span data-ttu-id="c215b-146">Erstellen von MOF-Dateien aus MIB-Dateien</span><span class="sxs-lookup"><span data-stu-id="c215b-146">Generating MOF Files from MIB Files</span></span>

<span data-ttu-id="c215b-147">Die folgenden Befehle sind ein Beispiel für das Generieren von MOF-Dateien aus den MIB-Dateien, die bei der Installation des SNMP-Anbieters installiert werden.</span><span class="sxs-lookup"><span data-stu-id="c215b-147">The following commands are an example of how to generate MOF files from the MIB files that are installed when the SNMP provider is installed.</span></span>

<span data-ttu-id="c215b-148">**CD** *% windir% \\ system32 \\ WBEM \\ SNMP*</span><span class="sxs-lookup"><span data-stu-id="c215b-148">**cd** *%windir%\\system32\\wbem\\SNMP*</span></span>

<span data-ttu-id="c215b-149">**Smi2smir/g** *. \\ \\ .. hostmib. MIB* **>** *hostmib. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-149">**Smi2smir /g** *..\\..\\hostmib.mib* **>** *hostmib.mof*</span></span>

<span data-ttu-id="c215b-150">**Smi2smir/g** *. \\ \\ .. ipforwd. MIB* **>** *ipforwd. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-150">**Smi2smir /g** *..\\..\\ipforwd.mib* **>** *ipforwd.mof*</span></span>

<span data-ttu-id="c215b-151">**Smi2smir/g** *. \\ \\ .. nipx. MIB* **>** *nipx. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-151">**Smi2smir /g** *..\\..\\nipx.mib* **>** *nipx.mof*</span></span>

<span data-ttu-id="c215b-152">**Smi2smir/g** *. \\ \\ .. MIB \_ II. MIB* **>** *MIB \_ II. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-152">**Smi2smir /g** *..\\..\\mib\_ii.mib* **>** *mib\_ii.mof*</span></span>

<span data-ttu-id="c215b-153">**Smi2smir/g** *. \\ \\ .. lmmib2. MIB* **>** *lmmib2. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-153">**Smi2smir /g** *..\\..\\lmmib2.mib* **>** *lmmib2.mof*</span></span>

<span data-ttu-id="c215b-154">**Smi2smir/g** *. \\ \\ .. mcastmib. MIB* **>** *mcastmib. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-154">**Smi2smir /g** *..\\..\\mcastmib.mib* **>** *mcastmib.mof*</span></span>

<span data-ttu-id="c215b-155">**Smi2smir/g** *. \\ \\ .. rfc2571. MIB* **>** *rfc2571. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-155">**Smi2smir /g** *..\\..\\rfc2571.mib* **>** *rfc2571.mof*</span></span>

<span data-ttu-id="c215b-156">**Smi2smir/g** *. \\ \\ .. wfospf. MIB* **>** *wfospf. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-156">**Smi2smir /g** *..\\..\\wfospf.mib* **>** *wfospf.mof*</span></span>

<span data-ttu-id="c215b-157">**Smi2smir/g** *. \\ \\ .. DHCP. MIB.. \\ . \\ msft. MIB* **>** *DHCP. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-157">**Smi2smir /g** *..\\..\\dhcp.mib..\\..\\msft.mib* **>** *dhcp.mof*</span></span>

<span data-ttu-id="c215b-158">**Smi2smir/g** *. \\ \\ .. WINS. MIB.. \\ . \\ msft. MIB* **>** *WINS. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-158">**Smi2smir /g** *..\\..\\wins.mib..\\..\\msft.mib* **>** *wins.mof*</span></span>

<span data-ttu-id="c215b-159">**Smi2smir/g** *. \\ \\ .. mipx. MIB.. \\ . \\ msft. MIB* **>** *mipx. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-159">**Smi2smir /g** *..\\..\\mipx.mib..\\..\\msft.mib* **>** *mipx.mof*</span></span>

<span data-ttu-id="c215b-160">**Smi2smir/g** *. \\ \\ .. mripsap. MIB. \\ \\ .. msft. MIB* **>** *mripsap. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-160">**Smi2smir /g** *..\\..\\mripsap.mib..\\..\\msft.mib* **>** *mripsap.mof*</span></span>

<span data-ttu-id="c215b-161">**Smi2smir/g** *. \\ \\ .. msipbtp. MIB \\ \\ .... msft. MIB* **>** *msipbtp. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-161">**Smi2smir /g** *..\\..\\msipbtp.mib..\\..\\msft.mib* **>** *msipbtp.mof*</span></span>

<span data-ttu-id="c215b-162">**Smi2smir/g** *. \\ \\ .. msiprip2. MIB.. \\ . \\ msft. MIB* **>** *msiprip2. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-162">**Smi2smir /g** *..\\..\\msiprip2.mib..\\..\\msft.mib* **>** *msiprip2.mof*</span></span>

## <a name="adding-snmp-mof-files-to-the-wmi-repository"></a><span data-ttu-id="c215b-163">Hinzufügen von SNMP-MOF-Dateien zum WMI-Repository</span><span class="sxs-lookup"><span data-stu-id="c215b-163">Adding SNMP MOF Files to the WMI Repository</span></span>

<span data-ttu-id="c215b-164">Die folgenden Befehle sind ein Beispiel dafür, wie die MOF-Dateien, die aus den MIB-Dateien generiert werden, dem WMI-Repository hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c215b-164">The following commands are an example of how to add the MOF files that are generated from the MIB files to the WMI repository.</span></span> <span data-ttu-id="c215b-165">Wenn Sie die MOF-Dateien der Liste der Dateien hinzufügen möchten, die automatisch in einer Wiederherstellung des [*WMI-Repository*](gloss-w.md) wieder hergestellt werden sollen, fügen Sie am Ende jedes Befehls das Flag **-AutoRecover** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c215b-165">If you want to add the MOF files to the list of files to be automatically restored in a [*WMI repository*](gloss-w.md) recovery, add the **-AUTORECOVER** flag to the end of each command.</span></span> <span data-ttu-id="c215b-166">Weitere Informationen zum WMI-Mofcomp.exe Befehlszeilen Tool finden Sie unter " [**MUF**](mofcomp.md)".</span><span class="sxs-lookup"><span data-stu-id="c215b-166">For more information about the WMI Mofcomp.exe command-line tool, see [**mofcomp**](mofcomp.md).</span></span>

<span data-ttu-id="c215b-167">" **mamacomp** *hostmib. MOF* "</span><span class="sxs-lookup"><span data-stu-id="c215b-167">**mofcomp** *hostmib.mof*</span></span>

<span data-ttu-id="c215b-168">" *ipforwd. mof" von* " **mumacomp** "</span><span class="sxs-lookup"><span data-stu-id="c215b-168">**mofcomp** *ipforwd.mof*</span></span>

<span data-ttu-id="c215b-169">" **mamacomp** *nipx. MOF* "</span><span class="sxs-lookup"><span data-stu-id="c215b-169">**mofcomp** *nipx.mof*</span></span>

<span data-ttu-id="c215b-170">" **mamacomp** *MIB \_ II. MOF* "</span><span class="sxs-lookup"><span data-stu-id="c215b-170">**mofcomp** *mib\_ii.mof*</span></span>

<span data-ttu-id="c215b-171"> *lmmib2. MOF* -Datei</span><span class="sxs-lookup"><span data-stu-id="c215b-171">**mofcomp** *lmmib2.mof*</span></span>

<span data-ttu-id="c215b-172">" *mcastmib. mof" von* " **mumacomp** "</span><span class="sxs-lookup"><span data-stu-id="c215b-172">**mofcomp** *mcastmib.mof*</span></span>

<span data-ttu-id="c215b-173"> *rfc2571. MOF* -Datei</span><span class="sxs-lookup"><span data-stu-id="c215b-173">**mofcomp** *rfc2571.mof*</span></span>

<span data-ttu-id="c215b-174">**mufcomp** *wfospf. MOF*</span><span class="sxs-lookup"><span data-stu-id="c215b-174">**mofcomp** *wfospf.mof*</span></span>

<span data-ttu-id="c215b-175">" *DHCP. mof" von* " **MUF** "</span><span class="sxs-lookup"><span data-stu-id="c215b-175">**mofcomp** *dhcp.mof*</span></span>

<span data-ttu-id="c215b-176">" **mumacomp** *mipx. MOF* "</span><span class="sxs-lookup"><span data-stu-id="c215b-176">**mofcomp** *mipx.mof*</span></span>

<span data-ttu-id="c215b-177">" *mrippsap. mof" von* " **MUF** "</span><span class="sxs-lookup"><span data-stu-id="c215b-177">**mofcomp** *mripsap.mof*</span></span>

<span data-ttu-id="c215b-178">" *msipbtp. mof" von* " **MUF** "</span><span class="sxs-lookup"><span data-stu-id="c215b-178">**mofcomp** *msipbtp.mof*</span></span>

<span data-ttu-id="c215b-179"> *msiprip2. MOF* -Datei</span><span class="sxs-lookup"><span data-stu-id="c215b-179">**mofcomp** *msiprip2.mof*</span></span>

## <a name="related-topics"></a><span data-ttu-id="c215b-180">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c215b-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c215b-181">Zugreifen auf SNMP-Geräte</span><span class="sxs-lookup"><span data-stu-id="c215b-181">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 
