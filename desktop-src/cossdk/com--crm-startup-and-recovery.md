---
description: Com+-CRM-Start und-Wiederherstellung
ms.assetid: dee1f2df-dfe0-44c3-830b-871690e513e9
title: Com+-CRM-Start und-Wiederherstellung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a0e631e2e5ecef1621705c9af74aa48898d733b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345457"
---
# <a name="com-crm-startup-and-recovery"></a><span data-ttu-id="3ec5e-103">Com+-CRM-Start und-Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="3ec5e-103">COM+ CRM Startup and Recovery</span></span>

<span data-ttu-id="3ec5e-104">Wenn für eine Serveranwendung das Kontrollkästchen **kompensierende Ressourcen-Manager aktivieren aktiviert** ist (mithilfe des Verwaltungs Programms Komponenten Dienste auf der Registerkarte **erweitert** auf der Eigenschaften Seite der com+-Anwendung), wird beim ersten Start eine CRM-Protokolldatei erstellt, die von allen CRMs in diesem Server Anwendungsprozess verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-104">If a server application has the **Enable compensating resource managers** checkbox selected (using the Component Services administrative tool, on the **Advanced** tab of the COM+ application's property page), the first time it starts up it creates a CRM log file to be used by all CRMs in that server application process.</span></span> <span data-ttu-id="3ec5e-105">(Ausführliche Anweisungen zum Konfigurieren des CRM finden Sie unter [Konfigurieren von com+ CRM-Komponenten](configuring-com--crm-components.md).)</span><span class="sxs-lookup"><span data-stu-id="3ec5e-105">(For detailed instructions about configuring the CRM, see [Configuring COM+ CRM Components](configuring-com--crm-components.md).)</span></span>

<span data-ttu-id="3ec5e-106">Der Name der CRM-Protokolldatei, die für die Serveranwendung erstellt wurde, basiert auf der APP-ID (GUID) der Serveranwendung, und die CRM-Protokolldatei befindet sich im gleichen Verzeichnis wie die DTC-Protokolldatei (normalerweise das Verzeichnis% systemroot% \\ Winnt \\ system32 \\ dtclog).</span><span class="sxs-lookup"><span data-stu-id="3ec5e-106">The name of the CRM log file created for the server application is based on the AppId (a GUID) of the server application, and the CRM log file is placed in the same directory as the DTC log file (normally your %SystemRoot%\\winnt\\system32\\DtcLog directory).</span></span> <span data-ttu-id="3ec5e-107">CRM-Protokolldateien haben die Erweiterung ". crmlog".</span><span class="sxs-lookup"><span data-stu-id="3ec5e-107">CRM log files have the extension .crmlog.</span></span>

> [!Note]  
> <span data-ttu-id="3ec5e-108">Möglicherweise ist es erforderlich, den Standard Speicherort einer CRM-Protokolldatei aufgrund von Leistungsgründen (um die DTC-Protokolldatei auf einem anderen Datenträger als die CRM-Protokolldatei zu speichern) oder möglicherweise aufgrund der Verwendung von CRM in einer Cluster Umgebung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-108">It may be necessary to change the default location of a CRM log file due to performance reasons (to have the DTC log file on a different disk than the CRM log file) or perhaps due to use of the CRM in a cluster environment.</span></span> <span data-ttu-id="3ec5e-109">Der Speicherort der CRM-Protokolldateien kann mit dem com+-Verwaltungs-SDK geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-109">The location of the CRM log files can be changed using the COM+ administration SDK.</span></span> <span data-ttu-id="3ec5e-110">Der Eigenschaftsname ist crmlogfile und ist im [**Anwendungs**](applications.md) Sammlungsobjekt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-110">The property name is CRMLogFile, and it exists on the [**Applications**](applications.md) collection object.</span></span>

 

<span data-ttu-id="3ec5e-111">Wenn eine Serveranwendung (die CRM-fähig ist) gestartet wird und feststellt, dass bereits eine CRM-Protokolldatei für diese Serveranwendung vorhanden ist, führt Sie eine Wiederherstellung für diese CRM-Protokolldatei aus.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-111">When a server application (that is CRM-enabled) starts up and finds that a CRM log file already exists for that server application, it performs recovery on that CRM log file.</span></span> <span data-ttu-id="3ec5e-112">Bei der *Wiederherstellung* werden alle Transaktionen abgeschlossen, die durch einen Fehler unterbrochen wurden, und die CRM-Infrastruktur umfasst die CRM-Protokolldatei für Transaktionen, die nicht vollständig abgeschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-112">*Recovery* is the process of completing any transactions that were interrupted by a failure and involves the CRM infrastructure reading the CRM log file for any transactions that were not fully completed.</span></span> <span data-ttu-id="3ec5e-113">Wenn eine beliebige gefunden wird, kontaktiert Sie den DTC, um das Transaktions Ergebnis zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-113">If it finds any, it contacts the DTC to determine the transaction outcome.</span></span> <span data-ttu-id="3ec5e-114">Anschließend wird der CRM-Compensator erstellt, und die Commit-oder Abbruch Benachrichtigungen werden zusammen mit den zugehörigen Protokolldaten Sätzen nach Bedarf übergeben.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-114">It then creates the CRM Compensator and passes on the commit or abort notifications as required, together with the associated log records.</span></span>

<span data-ttu-id="3ec5e-115">Vorbereitungs Benachrichtigungen werden während der Wiederherstellung nicht vom CRM-kompenerer empfangen.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-115">Prepare notifications are not received by the CRM Compensator during recovery.</span></span> <span data-ttu-id="3ec5e-116">Der CRM-kompenerer verfügt über ein Flag, um zu unterscheiden, ob es während des normalen Betriebs oder während der Wiederherstellung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-116">The CRM Compensator has a flag to distinguish whether it is being called during normal operation or during recovery.</span></span>

<span data-ttu-id="3ec5e-117">Die Wiederherstellung findet in der Regel nur dann nicht abgeschlossene Transaktionen, wenn die Serveranwendung aufgrund eines Absturzes eines Server Anwendungsprozesses oder eines Computer Absturzes nicht ordnungsgemäß heruntergefahren wurde.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-117">Recovery will normally find uncompleted transactions only if the server application has been shutdown abnormally, due to either a server application process crash or a computer crash.</span></span> <span data-ttu-id="3ec5e-118">Wenn die Serveranwendung aufgrund des Leerlauf Timeouts oder durch manuelles Herunterfahren über das Verwaltungs Programmkomponenten Dienste normal heruntergefahren werden darf, ist die Protokolldatei bereinigt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-118">If the server application is allowed to shut down normally, due either to the idle time-out or to manual shutdown via the Component Services administrative tool, the log file will be clean.</span></span>

<span data-ttu-id="3ec5e-119">Das Starten einer CRM-Serveranwendung für die Wiederherstellung wird nicht automatisch initiiert.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-119">Starting of a CRM server application for recovery is not automatically initiated.</span></span> <span data-ttu-id="3ec5e-120">Zum Starten der CRM-Serveranwendung, bei der eine Wiederherstellung erforderlich ist, müssen einige externe Aktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-120">Some external action must be taken to start the CRM server application where recovery is required.</span></span> <span data-ttu-id="3ec5e-121">In der Regel wird dadurch eine Komponente in dieser Serveranwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="3ec5e-121">Typically this would be creating a component in that server application.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ec5e-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3ec5e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ec5e-123">Kompensierende com+-Ressourcen-Manager Konzepte</span><span class="sxs-lookup"><span data-stu-id="3ec5e-123">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> <dt>

[<span data-ttu-id="3ec5e-124">Com+-CRM-Betriebs Prozess</span><span class="sxs-lookup"><span data-stu-id="3ec5e-124">COM+ CRM Operating Process</span></span>](com--crm-operating-process.md)
</dt> </dl>

 

 



