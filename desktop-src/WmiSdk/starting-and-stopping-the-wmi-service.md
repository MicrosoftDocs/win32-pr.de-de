---
description: WMI wird als Dienst mit dem anzeigen Amen &\# 0034; ausgeführt. Windows-Verwaltungsinstrumentation&\# 0034; und der Dienst Name &\# 0034; WinMgmt&\# 0034;.
ms.assetid: 8dff43bf-71d0-4d5a-91bc-6f474186d4ba
ms.tgt_platform: multiple
title: Starten und Beenden des WMI-Dienstanbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54b820283aac089ad6191ee587e6beadea6dc030
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215325"
---
# <a name="starting-and-stopping-the-wmi-service"></a><span data-ttu-id="76543-103">Starten und Beenden des WMI-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="76543-103">Starting and Stopping the WMI Service</span></span>

<span data-ttu-id="76543-104">WMI wird als Dienst mit dem anzeigen Amen "Windows-Verwaltungsinstrumentation" und dem Dienstnamen "winmgmt" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76543-104">WMI runs as a service with the display name "Windows Management Instrumentation" and the service name "winmgmt".</span></span> <span data-ttu-id="76543-105">WMI wird automatisch beim Systemstart unter dem Konto "LocalSystem" ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76543-105">WMI runs automatically at system startup under the LocalSystem account.</span></span> <span data-ttu-id="76543-106">Wenn WMI nicht ausgeführt wird, wird es automatisch gestartet, wenn die erste Verwaltungs Anwendung oder das erste Skript eine Verbindung mit einem WMI-Namespace anfordert.</span><span class="sxs-lookup"><span data-stu-id="76543-106">If WMI is not running, it automatically starts when the first management application or script requests connection to a WMI namespace.</span></span>

<span data-ttu-id="76543-107">Abhängig von der Betriebssystemversion, die auf dem System ausgeführt wird, sind mehrere andere Dienste abhängig von der Betriebssystemversion, die auf dem WMI-Dienst</span><span class="sxs-lookup"><span data-stu-id="76543-107">Several other services are dependent upon the WMI service, depending on the operating system version that the system is running.</span></span>

## <a name="starting-winmgmt-service"></a><span data-ttu-id="76543-108">WinMgmt-Dienst wird gestartet</span><span class="sxs-lookup"><span data-stu-id="76543-108">Starting Winmgmt Service</span></span>

<span data-ttu-id="76543-109">Im folgenden Verfahren wird beschrieben, wie der WMI-Dienst gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="76543-109">The following procedure describes how to start the WMI service.</span></span>

<span data-ttu-id="76543-110">**So starten Sie den WinMgmt-Dienst**</span><span class="sxs-lookup"><span data-stu-id="76543-110">**To start Winmgmt Service**</span></span>

1.  <span data-ttu-id="76543-111">Geben Sie an einer Eingabeaufforderung **net** **Start** **WinMgmt** ein \[ */<switch>* \] .</span><span class="sxs-lookup"><span data-stu-id="76543-111">At a command prompt, enter **net** **start** **winmgmt** \[*/<switch>*\].</span></span>

    <span data-ttu-id="76543-112">Weitere Informationen zu den verfügbaren Switches finden Sie unter [WinMgmt](winmgmt.md).</span><span class="sxs-lookup"><span data-stu-id="76543-112">For more information about the switches that are available, see [winmgmt](winmgmt.md).</span></span> <span data-ttu-id="76543-113">Verwenden Sie das integrierte Administrator Konto oder ein Konto in der Gruppe Administratoren, die mit erhöhten Rechten ausgeführt wird, um den WMI-Dienst zu starten.</span><span class="sxs-lookup"><span data-stu-id="76543-113">You use the built-in Administrator account or an account in the Administrators group running with elevated rights to start the WMI service.</span></span> <span data-ttu-id="76543-114">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](user-account-control-and-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="76543-114">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

2.  <span data-ttu-id="76543-115">Andere Dienste, die vom WMI-Dienst abhängig sind, z. b. der SMS-Agent-Host oder die Windows-Firewall, werden nicht automatisch neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="76543-115">Other services that are dependent on the WMI service, such as SMS Agent Host or Windows Firewall, will not automatically be restarted.</span></span>

## <a name="stopping-winmgmt-service"></a><span data-ttu-id="76543-116">WinMgmt-Dienst wird beendet.</span><span class="sxs-lookup"><span data-stu-id="76543-116">Stopping Winmgmt Service</span></span>

<span data-ttu-id="76543-117">Im folgenden Verfahren wird beschrieben, wie der WMI-Dienst beendet wird.</span><span class="sxs-lookup"><span data-stu-id="76543-117">The following procedure describes how to stop the WMI Service.</span></span>

<span data-ttu-id="76543-118">**So verhindern Sie den WinMgmt-Dienst**</span><span class="sxs-lookup"><span data-stu-id="76543-118">**To stop Winmgmt Service**</span></span>

1.  <span data-ttu-id="76543-119">Geben Sie an einer Eingabeaufforderung **net stoppt WinMgmt** ein.</span><span class="sxs-lookup"><span data-stu-id="76543-119">At a command prompt, enter **net stop winmgmt**.</span></span>

2.  <span data-ttu-id="76543-120">Andere Dienste, die vom WMI-Dienst abhängig sind, werden ebenfalls angehalten, z. b. SMS-Agent-Host oder Windows-Firewall</span><span class="sxs-lookup"><span data-stu-id="76543-120">Other services that are dependent on the WMI service also halt, such as SMS Agent Host or Windows Firewall.</span></span>

## <a name="examples"></a><span data-ttu-id="76543-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76543-121">Examples</span></span>

<span data-ttu-id="76543-122">Die TechNet Gallery enthält das [WMI-Service Watchdog-Skript](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), das beschreibt, wie der WinMgmt-Dienst mit PowerShell Programm gesteuert heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="76543-122">The TechNet Gallery contains the [WMI service watchdog script](https://Gallery.TechNet.Microsoft.Com/WMI-service-watchdog-script-4fab1282), which describes how to programmatically shut down and restart the winmgmt service with PowerShell.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76543-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="76543-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76543-124">Verwenden der WMI-Command-Line Tools</span><span class="sxs-lookup"><span data-stu-id="76543-124">Using the WMI Command-Line Tools</span></span>](using-the-wmi-command-line-tools.md)
</dt> </dl>

 

 



