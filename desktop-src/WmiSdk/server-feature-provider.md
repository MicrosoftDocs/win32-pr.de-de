---
description: Ab Windows Server 2008 liefert der Server Funktions Anbieter Informationen dazu, welche Server Funktionen auf dem Server installiert sind. Mit dieser Klasse können Administratoren ihre Server Rollen und Features inventarisieren und verwalten.
ms.assetid: f7932eaa-6730-4301-9809-32de9c1a20de
ms.tgt_platform: multiple
title: Server Funktions Anbieter
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 73666dc810a40f33e3d35acb1b9d7ade5d2b021a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350271"
---
# <a name="server-feature-provider"></a><span data-ttu-id="3be49-104">Server Funktions Anbieter</span><span class="sxs-lookup"><span data-stu-id="3be49-104">Server Feature Provider</span></span>

<span data-ttu-id="3be49-105">Ab Windows Server 2008 liefert der Server Funktions Anbieter Informationen dazu, welche Server Funktionen auf dem Server installiert sind.</span><span class="sxs-lookup"><span data-stu-id="3be49-105">Starting with Windows Server 2008, the Server Feature Provider supplies information on what server features are installed on the server.</span></span> <span data-ttu-id="3be49-106">Mit dieser Klasse können Administratoren ihre Server Rollen und Features inventarisieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="3be49-106">This class allows administrators to inventory and manage their server roles and features.</span></span>

<span data-ttu-id="3be49-107">Eine Server Rolle ist als eine Gruppe von Komponenten definiert, die Funktionen für einen bestimmten Funktionsbereich bereitstellen, z. b. Drucken, Dateien, Domänen Steuerung usw.</span><span class="sxs-lookup"><span data-stu-id="3be49-107">A server role is defined as a group of components that provide functions for a specific area of functionality, such as printing, files, domain control, and so on.</span></span> <span data-ttu-id="3be49-108">Typische Server Rollen sind Dateiserver, e-Mail-Server, DNS-Server, Domänen Controller, Anwendungsserver usw.</span><span class="sxs-lookup"><span data-stu-id="3be49-108">Typical server roles are File Server, Mail Server, DNS Server, Domain Controller, Application Server, and so on.</span></span>

<span data-ttu-id="3be49-109">Wenn in einem Unternehmen keine Verwaltungssoftware ausgeführt wird, die Server Rollen meldet (z. b. Microsoft Operations Manager mit installierten Management Packs), können Sie diese Informationen abrufen, indem Sie die Win32-Klasse " [**\_ Serverfeature**](win32-serverfeature.md) " Abfragen.</span><span class="sxs-lookup"><span data-stu-id="3be49-109">If an enterprise is not running management software that reports server roles, such as Microsoft Operations Manager with management packs installed, then you can obtain that information by querying the [**Win32\_ServerFeature**](win32-serverfeature.md) class.</span></span> <span data-ttu-id="3be49-110">Server Rollen-und Featureinformationen von Remote Computern sind über normale WMI-Remote Verbindungen oder mithilfe des Windows-Remoteverwaltung-Dienstanbieter (WinRM) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3be49-110">Server role and feature information from remote computers is available through normal WMI remote connections or by using the Windows Remote Management (WinRM) service.</span></span> <span data-ttu-id="3be49-111">Weitere Informationen zu Remote-WMI-DCOM-Verbindungen finden [Sie unter Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span><span class="sxs-lookup"><span data-stu-id="3be49-111">For more information about remote WMI DCOM connections, see [Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md).</span></span> <span data-ttu-id="3be49-112">Weitere Informationen zu Verbindungen mit dem [*WS-Verwaltungs*](/windows/desktop/WinRM/windows-remote-management-glossary) Protokoll finden Sie unter [Windows-Remoteverwaltung](/windows/desktop/WinRM/portal).</span><span class="sxs-lookup"><span data-stu-id="3be49-112">For more information about connections using the [*WS-Management*](/windows/desktop/WinRM/windows-remote-management-glossary) protocol, see [Windows Remote Management](/windows/desktop/WinRM/portal).</span></span>

<span data-ttu-id="3be49-113">Der Server Funktions Anbieter unterstützt die folgenden WMI-Klassen:</span><span class="sxs-lookup"><span data-stu-id="3be49-113">The Server Feature Provider supports the following WMI classes:</span></span>

-   [<span data-ttu-id="3be49-114">**Win32- \_ Server Funktion**</span><span class="sxs-lookup"><span data-stu-id="3be49-114">**Win32\_ServerFeature**</span></span>](win32-serverfeature.md)

## <a name="related-topics"></a><span data-ttu-id="3be49-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3be49-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3be49-116">WMI-Anbieter</span><span class="sxs-lookup"><span data-stu-id="3be49-116">WMI Providers</span></span>](wmi-providers.md)
</dt> </dl>

 

 
