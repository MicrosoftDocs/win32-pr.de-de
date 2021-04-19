---
description: WMI wird als Teil eines Hosts für gemeinsame Dienste ausgeführt, wobei Ports standardmäßig über DCOM zugewiesen werden. Sie können jedoch den WMI-Dienst so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festgelegten Port angeben.
ms.assetid: 62908445-2a43-4a20-a998-e497c6ecf48e
ms.tgt_platform: multiple
title: Einrichten eines festgelegten Ports für WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 49c6d6b0bf42951766cfd813ccb4b5eed041600a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362720"
---
# <a name="setting-up-a-fixed-port-for-wmi"></a><span data-ttu-id="679bd-104">Einrichten eines festgelegten Ports für WMI</span><span class="sxs-lookup"><span data-stu-id="679bd-104">Setting Up a Fixed Port for WMI</span></span>

<span data-ttu-id="679bd-105">WMI wird als Teil eines Hosts für gemeinsame Dienste ausgeführt, wobei Ports standardmäßig über DCOM zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="679bd-105">WMI runs as part of a shared service host with ports assigned through DCOM by default.</span></span> <span data-ttu-id="679bd-106">Sie können jedoch den WMI-Dienst so einrichten, dass er als einziger Prozess auf einem separaten Host ausgeführt wird, und einen festgelegten Port angeben.</span><span class="sxs-lookup"><span data-stu-id="679bd-106">However, you can set up the WMI service to run as the only process in a separate host and specify a fixed port.</span></span>

<span data-ttu-id="679bd-107">Das folgende Verfahren ist ein automatisiertes Setup, mit dem WMI über einen Fixed-Port verfügen kann.</span><span class="sxs-lookup"><span data-stu-id="679bd-107">The following procedure is an automated setup to allow WMI to have a fixed port.</span></span> <span data-ttu-id="679bd-108">Die Prozedur verwendet das [**WinMgmt**](winmgmt.md) -Befehlszeilen Tool.</span><span class="sxs-lookup"><span data-stu-id="679bd-108">The procedure uses the [**winmgmt**](winmgmt.md) command-line tool.</span></span>

<span data-ttu-id="679bd-109">**So richten Sie einen Fixed-Port für WMI ein**</span><span class="sxs-lookup"><span data-stu-id="679bd-109">**To set up a fixed port for WMI**</span></span>

1.  <span data-ttu-id="679bd-110">Geben Sie an der Eingabeaufforderung **winmgmt-standalonehost** ein.</span><span class="sxs-lookup"><span data-stu-id="679bd-110">At the command prompt, type **winmgmt -standalonehost**</span></span>
2.  <span data-ttu-id="679bd-111">Geben Sie den WMI-Dienst an, indem Sie den Befehl **net-"Windows-Verwaltungsinstrumentation"** eingeben, oder verwenden Sie den Kurznamen von net-" **WinMgmt** ".</span><span class="sxs-lookup"><span data-stu-id="679bd-111">Stop the WMI service by typing the command **net stop "Windows Management Instrumentation"**, or use the short name of **net stop winmgmt**</span></span>
3.  <span data-ttu-id="679bd-112">Starten Sie den WMI-Dienst erneut auf einem neuen Dienst Host, indem Sie **net Start "Windows-Verwaltungsinstrumentation" oder "** **net Start WinMgmt** " eingeben.</span><span class="sxs-lookup"><span data-stu-id="679bd-112">Restart the WMI service again in a new service host by typing **net start "Windows Management Instrumentation"** or **net start winmgmt**</span></span>
4.  <span data-ttu-id="679bd-113">Richten Sie eine neue Portnummer für den WMI-Dienst ein, indem **Sie netsh Firewall Add portopening TCP 24158 wmifixedport** eingeben.</span><span class="sxs-lookup"><span data-stu-id="679bd-113">Establish a new port number for the WMI service by typing **netsh firewall add portopening TCP 24158 WMIFixedPort**</span></span>

<span data-ttu-id="679bd-114">Wenn Sie an WMI vorgenommene Änderungen rückgängig machen möchten, geben Sie **WinMgmt/sharedhost** ein, und starten Sie dann den WinMgmt-Dienst erneut.</span><span class="sxs-lookup"><span data-stu-id="679bd-114">To undo any changes you make to WMI, type **winmgmt /sharedhost**, then stop and start the winmgmt service again.</span></span>

## <a name="examples"></a><span data-ttu-id="679bd-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="679bd-115">Examples</span></span>

<span data-ttu-id="679bd-116">Ein Skript, in dem ein fester Port für WMI eingerichtet wird, finden Sie im folgenden Skript Katalog- [Codebeispiel](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span><span class="sxs-lookup"><span data-stu-id="679bd-116">For a script that sets up a fixed port for WMI, see the following Scripting Gallery [code sample](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389 ).</span></span>

<span data-ttu-id="679bd-117">oder ein PowerShell-Codebeispiel, das die WMI-Port Einstellungen aktiviert oder deaktiviert, finden Sie im Beispiel für [Set-wmisingleport](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) in der TechNet Gallery.</span><span class="sxs-lookup"><span data-stu-id="679bd-117">or a PowerShell code example that enables or disables the WMI port settings, see the [Set-WmiSinglePort](https://Gallery.TechNet.Microsoft.Com/Set-WmiSinglePortps1-20fa8389) example on TechNet Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="679bd-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="679bd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="679bd-119">Herstellen einer Verbindung mit WMI auf einem Remote Computer</span><span class="sxs-lookup"><span data-stu-id="679bd-119">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="679bd-120">Problembehandlung bei WMI-Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="679bd-120">Troubleshooting a Remote WMI Connections</span></span>](connecting-to-wmi-remotely-starting-with-vista.md)
</dt> <dt>

[<span data-ttu-id="679bd-121">Anbieter Hosting und-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="679bd-121">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
</dt> </dl>

 

 



