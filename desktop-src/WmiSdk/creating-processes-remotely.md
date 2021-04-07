---
description: Sie können Win32 \_ Process. Create verwenden, um ein Skript oder eine Anwendung auf einem Remote Computer auszuführen. Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein. Wenn Win32 \_ Process. Create auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.
ms.assetid: 11fea8b1-7d05-4f44-9103-ea804a1d4b38
ms.tgt_platform: multiple
title: Remote Erstellung von Prozessen mithilfe von WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e7b97f8f4fdddd608f6ee8c3368bde6ad6e854
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758748"
---
# <a name="creating-processes-remotely-using-wmi"></a><span data-ttu-id="7fe55-105">Remote Erstellung von Prozessen mithilfe von WMI</span><span class="sxs-lookup"><span data-stu-id="7fe55-105">Creating Processes Remotely using WMI</span></span>

<span data-ttu-id="7fe55-106">Sie können [**Win32 \_ Process. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) verwenden, um ein Skript oder eine Anwendung auf einem Remote Computer auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7fe55-106">You can use [**Win32\_Process.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) to execute a script or application on a remote computer.</span></span> <span data-ttu-id="7fe55-107">Aus Sicherheitsgründen kann der Prozess jedoch nicht interaktiv sein.</span><span class="sxs-lookup"><span data-stu-id="7fe55-107">However, for security reasons, the process cannot be interactive.</span></span> <span data-ttu-id="7fe55-108">Wenn **Win32 \_ Process. Create** auf dem lokalen Computer aufgerufen wird, kann der Prozess interaktiv sein.</span><span class="sxs-lookup"><span data-stu-id="7fe55-108">When **Win32\_Process.Create** is called on the local computer, the process can be interactive.</span></span>

> [!WARNING]
> <span data-ttu-id="7fe55-109">In diesem Thema wird das allgemeine Verfahren zum Erstellen eines Remote Prozesses mit WMI beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7fe55-109">This topic describes the general procedure for creating a remote process with WMI.</span></span> <span data-ttu-id="7fe55-110">Wenn Sie einfach ein Skript auf einem Remote System ausführen möchten, finden Sie weitere Informationen unter Herstellen einer Remote [Verbindung mit WMI ab Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md)oder [Herstellen einer Verbindung mit WMI auf einem Remote Computer mithilfe von Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span><span class="sxs-lookup"><span data-stu-id="7fe55-110">If you are simply looking to run a script on a remote system, see [Connecting to WMI Remotely Starting with Windows Vista](connecting-to-wmi-remotely-starting-with-vista.md), or [Connecting to WMI on a Remote Computer by Using Windows PowerShell](connecting-to-wmi-on-a-remote-computer-by-using-powershell.md).</span></span> <span data-ttu-id="7fe55-111">Weitere allgemeine Informationen zum Remoting mit PowerShell finden Sie unter [Ausführen von Remote Befehlen](https://technet.microsoft.com/library/dd819505.aspx).</span><span class="sxs-lookup"><span data-stu-id="7fe55-111">For more general information on remoting with PowerShell, see [Running Remote Commands](https://technet.microsoft.com/library/dd819505.aspx).</span></span>

 

<span data-ttu-id="7fe55-112">Der Remote Prozess hat keine Benutzeroberfläche, wird aber im Task- **Manager** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7fe55-112">The remote process has no user interface but it is listed in the **Task Manager**.</span></span> <span data-ttu-id="7fe55-113">Ein lokal erstelltes Prozess kann unter jedem Konto ausgeführt werden, wenn das Konto über die **Execute Method** -Berechtigung für den root \\ CIMV2-Namespace verfügt.</span><span class="sxs-lookup"><span data-stu-id="7fe55-113">A process created locally can run under any account if the account has the **Execute Method** permission for the root\\cimv2 namespace.</span></span> <span data-ttu-id="7fe55-114">Ein Remote erstellter Prozess kann unter jedem Konto ausgeführt werden, wenn das Konto über die **Execute-Methode** und die **Remote enable** -Berechtigung für root \\ CIMV2 verfügt.</span><span class="sxs-lookup"><span data-stu-id="7fe55-114">A process created remotely can run under any account if the account has the **Execute Method** and **Remote Enable** permissions for root\\cimv2.</span></span> <span data-ttu-id="7fe55-115">Die **Execute-Methode** und die **Remote Aktivierungs** Berechtigungen werden in der Systemsteuerung in der WMI-Steuerung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7fe55-115">The **Execute Method** and **Remote Enable** permissions are set in WMI Control in the Control Panel.</span></span> <span data-ttu-id="7fe55-116">Weitere Informationen finden Sie unter [Festlegen der Namespace Sicherheit mit dem WMI-Steuer](setting-namespace-security-with-the-wmi-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="7fe55-116">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>

<span data-ttu-id="7fe55-117">Sie können [**Win32 \_ ScheduledJob. Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) verwenden, um einen interaktiven Prozess Remote zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7fe55-117">You can use [**Win32\_ScheduledJob.Create**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-scheduledjob) to create an interactive process remotely.</span></span> <span data-ttu-id="7fe55-118">Prozesse, die von **Win32 \_ ScheduledJob. Create** gestartet werden, werden jedoch unter dem Konto LocalSystem ausgeführt, das zu viele Berechtigungen gewähren kann.</span><span class="sxs-lookup"><span data-stu-id="7fe55-118">But processes started by **Win32\_ScheduledJob.Create** run under the LocalSystem account that can confer too much privilege.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7fe55-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7fe55-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7fe55-120">Sichern einer Remote-WMI-Verbindung</span><span class="sxs-lookup"><span data-stu-id="7fe55-120">Securing a Remote WMI Connection</span></span>](securing-a-remote-wmi-connection.md)
</dt> <dt>

[<span data-ttu-id="7fe55-121">Herstellen einer Verbindung mit einer dritten Computer Delegierung</span><span class="sxs-lookup"><span data-stu-id="7fe55-121">Connecting to a 3rd Computer-Delegation</span></span>](connecting-to-a-3rd-computer-delegation.md)
</dt> </dl>

 

 
