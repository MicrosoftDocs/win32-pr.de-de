---
description: WMI bietet eine einheitliche Schnittstelle für lokale oder Remote Anwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen erhalten.
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: WMI-Architektur
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104563799"
---
# <a name="wmi-architecture"></a><span data-ttu-id="652c4-103">WMI-Architektur</span><span class="sxs-lookup"><span data-stu-id="652c4-103">WMI Architecture</span></span>

<span data-ttu-id="652c4-104">WMI bietet eine einheitliche Schnittstelle für lokale oder Remote Anwendungen oder Skripts, die Verwaltungsdaten von einem Computersystem, einem Netzwerk oder einem Unternehmen erhalten.</span><span class="sxs-lookup"><span data-stu-id="652c4-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="652c4-105">Die einheitliche Schnittstelle ist so konzipiert, dass WMI-Client Anwendungen und-Skripts keine Vielzahl von Betriebssystem-Anwendungs Programmierschnittstellen (APIs) aufzurufen müssen.</span><span class="sxs-lookup"><span data-stu-id="652c4-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="652c4-106">Viele APIs können nicht von Automatisierungs Clients wie Skripts oder Visual Basic Anwendungen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="652c4-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="652c4-107">Von anderen APIs werden keine Aufrufe an Remote Computer durchführen.</span><span class="sxs-lookup"><span data-stu-id="652c4-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="652c4-108">Zum Abrufen von Daten aus WMI schreiben Sie ein Client Skript oder eine Anwendung, die auf [WMI-Klassen](wmi-classes.md) zugreift oder WMI-Daten bereitstellt, indem Sie einen [*WMI-Anbieter*](gloss-p.md)schreiben.</span><span class="sxs-lookup"><span data-stu-id="652c4-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="652c4-109">Weitere Informationen finden Sie unter [Verwenden von WMI](using-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="652c4-110">Objekte, Consumer und Infrastruktur von WMI</span><span class="sxs-lookup"><span data-stu-id="652c4-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="652c4-111">Das folgende Diagramm zeigt die Beziehung zwischen der WMI-Infrastruktur und den WMI-Anbietern und den verwalteten Objekten und zeigt außerdem die Beziehung zwischen der WMI-Infrastruktur und den WMI-Consumern.</span><span class="sxs-lookup"><span data-stu-id="652c4-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![Beziehung zwischen WMI-Infrastruktur, WMI-Anbietern und verwalteten Objekten](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="652c4-113">WMI-Komponenten</span><span class="sxs-lookup"><span data-stu-id="652c4-113">WMI Components</span></span>

<span data-ttu-id="652c4-114">In der folgenden Liste werden die wichtigsten WMI-Komponenten beschrieben:</span><span class="sxs-lookup"><span data-stu-id="652c4-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="652c4-115">Verwaltete Objekte und WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="652c4-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="652c4-116">Ein WMI-Anbieter ist ein COM-Objekt, das ein oder mehrere [*verwaltete Objekte*](gloss-m.md) für WMI überwacht.</span><span class="sxs-lookup"><span data-stu-id="652c4-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="652c4-117">Ein verwaltetes Objekt ist eine logische oder physische Unternehmens Komponente, z. b. ein Festplattenlaufwerk, ein Netzwerkadapter, ein Datenbanksystem, ein Betriebssystem, ein Prozess oder ein Dienst.</span><span class="sxs-lookup"><span data-stu-id="652c4-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="652c4-118">Ähnlich wie bei einem Treiber stellt ein Anbieter WMI mit Daten aus einem verwalteten Objekt bereit und verarbeitet die Nachrichten von WMI an das verwaltete Objekt.</span><span class="sxs-lookup"><span data-stu-id="652c4-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="652c4-119">WMI-Anbieter bestehen aus einer DLL-Datei und einer [*Managed Object Format (MOF)*](gloss-m.md) -Datei, die die Klassen definiert, für die der Anbieter Daten zurückgibt und Vorgänge ausführt.</span><span class="sxs-lookup"><span data-stu-id="652c4-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="652c4-120">Anbieter, wie z. b. WMI C++-Anwendungen, verwenden die [com-API für WMI](com-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="652c4-121">Weitere Informationen finden Sie unter [Bereitstellen von Daten für WMI](providing-data-to-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="652c4-122">Ein Beispiel für einen-Anbieter ist der vorinstallierte [Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider), der auf Daten in der Systemregistrierung zugreift.</span><span class="sxs-lookup"><span data-stu-id="652c4-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="652c4-123">Der Registrierungs Anbieter verfügt über eine [*WMI-Klasse*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), mit vielen Methoden, aber ohne Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="652c4-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="652c4-124">Andere vorinstallierte Anbieter, z. b. der [Win32-Anbieter](/windows/desktop/CIMWin32Prov/win32-provider), verfügen normalerweise über Klassen mit vielen Eigenschaften, aber nur wenige Methoden, z. b. [**Win32- \_ Prozess**](/windows/desktop/CIMWin32Prov/win32-process) oder [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span><span class="sxs-lookup"><span data-stu-id="652c4-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="652c4-125">Die DLL-Datei des Registrierungs Anbieters (Stdprov.dll) enthält den Code, der Daten dynamisch zurückgibt, wenn Sie von Client Skripts oder Anwendungen angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="652c4-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="652c4-126">Die WMI-MOF-und dll-Dateien befinden sich in% windir% \\ system32 \\ WBEM, zusammen mit den [WMI-Command-Line Tools](wmi-command-line-tools.md)wie [**Winmgmt.exe**](winmgmt.md) und [**Mofcomp.exe**](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="652c4-127">Anbieter Klassen, wie z. b. [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), werden in MOF-Dateien definiert und beim Systemstart in das WMI-Repository kompiliert.</span><span class="sxs-lookup"><span data-stu-id="652c4-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="652c4-128">WMI-Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="652c4-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="652c4-129">Die WMI-Infrastruktur ist eine Komponente des Microsoft Windows-Betriebssystems, die als WMI-Dienst (Winmgmt) bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="652c4-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="652c4-130">Die WMI-Infrastruktur verfügt über zwei Komponenten: den WMI-Kern und das [*WMI-Repository*](gloss-w.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="652c4-131">Das WMI-Repository ist nach WMI- [*Namespaces*](gloss-n.md)organisiert.</span><span class="sxs-lookup"><span data-stu-id="652c4-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="652c4-132">Der WMI-Dienst erstellt beim Systemstart einige Namespaces, z. b. root \\ Default, root \\ CIMV2 und root- \\ Abonnement und führt eine Vorinstallation eines Standardsatzes von Klassendefinitionen durch, einschließlich der [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider), der [WMI-System Klassen](wmi-system-classes.md)und anderer.</span><span class="sxs-lookup"><span data-stu-id="652c4-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="652c4-133">Die verbleibenden Namespaces, die auf Ihrem System gefunden werden, werden von Anbietern für andere Teile des Betriebssystems oder der Produkte erstellt.</span><span class="sxs-lookup"><span data-stu-id="652c4-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="652c4-134">Weitere Informationen und eine Liste der WMI-Anbieter, die in den meisten Betriebssystemversionen gefunden werden, finden Sie unter [WMI-Anbieter](wmi-providers.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="652c4-135">Der WMI-Dienst fungiert als Vermittler zwischen den Anbietern, den Verwaltungs Anwendungen und dem WMI-Repository.</span><span class="sxs-lookup"><span data-stu-id="652c4-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="652c4-136">Nur statische Daten über Objekte werden im Repository gespeichert, z. b. die von Anbietern definierten Klassen.</span><span class="sxs-lookup"><span data-stu-id="652c4-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="652c4-137">Die meisten Daten werden von WMI dynamisch vom Anbieter abgerufen, wenn Sie von einem Client angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="652c4-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="652c4-138">Sie können auch Abonnements einrichten, um Ereignis Benachrichtigungen von einem Anbieter zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="652c4-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="652c4-139">Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="652c4-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="652c4-140">WMI-Consumer</span><span class="sxs-lookup"><span data-stu-id="652c4-140">WMI consumers</span></span>

    <span data-ttu-id="652c4-141">Ein WMI-Consumer ist eine Verwaltungs Anwendung oder ein Skript, das mit der WMI-Infrastruktur interagiert.</span><span class="sxs-lookup"><span data-stu-id="652c4-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="652c4-142">Eine Verwaltungs Anwendung kann Daten Abfragen, aufzählen, Anbieter Methoden ausführen oder Ereignisse abonnieren, indem Sie entweder die [com-API für WMI](com-api-for-wmi.md) oder die [Skript-API für WMI](scripting-api-for-wmi.md)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="652c4-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="652c4-143">Die einzigen Daten oder Aktionen, die für ein verwaltetes Objekt, z. b. ein Laufwerk oder einen Dienst, verfügbar sind, sind die von einem Anbieter bereitgestellten Daten.</span><span class="sxs-lookup"><span data-stu-id="652c4-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="652c4-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="652c4-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="652c4-145">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="652c4-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="652c4-146">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="652c4-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="652c4-147">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="652c4-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="652c4-148">WMI-Tasks für Skripts und Anwendungen</span><span class="sxs-lookup"><span data-stu-id="652c4-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="652c4-149">Bereitstellen von Daten für WMI</span><span class="sxs-lookup"><span data-stu-id="652c4-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="652c4-150">WMI-Klassen</span><span class="sxs-lookup"><span data-stu-id="652c4-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="652c4-151">Überwachen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="652c4-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="652c4-152">Aufrufen einer Methode</span><span class="sxs-lookup"><span data-stu-id="652c4-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
