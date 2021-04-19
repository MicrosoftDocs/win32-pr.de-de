---
description: Jede Skriptsprache, z. b. VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen. Anwendungen können auf WMI in C++ mithilfe der com-API für WMI oder in Visual Basic zugreifen, mithilfe der wbemdisp. tlb-Typbibliothek und der Skript-API für WMI. .
ms.assetid: c0d18827-6b36-4817-8cd9-06cd0f267b28
ms.tgt_platform: multiple
title: Erstellen einer WMI-Anwendung oder eines Skripts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b27e3cffd7e4d9bea4ce36e7c0da77ae5d72cdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349648"
---
# <a name="creating-a-wmi-application-or-script"></a><span data-ttu-id="289ae-105">Erstellen einer WMI-Anwendung oder eines Skripts</span><span class="sxs-lookup"><span data-stu-id="289ae-105">Creating a WMI Application or Script</span></span>

<span data-ttu-id="289ae-106">Jede Skriptsprache, z. b. VBScript, die mit ActiveX-Objekten funktioniert, kann auf WMI-Daten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="289ae-106">Any scripting language, such as VBScript, that works with ActiveX objects can access WMI data.</span></span> <span data-ttu-id="289ae-107">Anwendungen können auf WMI in C++ mithilfe der [com-API für WMI](com-api-for-wmi.md) oder in Visual Basic zugreifen, mithilfe der wbemdisp. tlb- [Typbibliothek](using-the-wmi-scripting-type-library.md) und der [Skript-API für WMI](scripting-api-for-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="289ae-107">Applications can access WMI in C++, using the [COM API for WMI](com-api-for-wmi.md) or in Visual Basic, using the Wbemdisp.tlb [type library](using-the-wmi-scripting-type-library.md) and the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="289ae-108">.</span><span class="sxs-lookup"><span data-stu-id="289ae-108">.</span></span> <span data-ttu-id="289ae-109">Sie können Daten über WMI abrufen, indem Sie ein Skript, eine Active Server Seite (ASP) oder eine HTML-Anwendung (HTA) schreiben.</span><span class="sxs-lookup"><span data-stu-id="289ae-109">You can obtain data through WMI by writing a script, an Active Server Page (ASP), or an HTML application (HTA).</span></span> <span data-ttu-id="289ae-110">Sie können auch Windows PowerShell verwenden, um Daten abzurufen oder Skripts zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="289ae-110">You can also use Windows PowerShell to obtain data or write scripts.</span></span> <span data-ttu-id="289ae-111">Weitere Informationen finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) und [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="289ae-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script) and [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span> <span data-ttu-id="289ae-112">Das technet scriptcenter [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) enthält Hunderte von Skript Beispielen.</span><span class="sxs-lookup"><span data-stu-id="289ae-112">The TechNet ScriptCenter at [https://www.microsoft.com/technet](https://technet.microsoft.com/default.aspx) contains hundreds of scripting examples.</span></span> <span data-ttu-id="289ae-113">Weitere Informationen zu Druck-und Online Ressourcen finden Sie unter [Weitere Informationen](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="289ae-113">For more information about print and online resources, see [Further Information](further-information.md).</span></span>

<span data-ttu-id="289ae-114">Im folgenden Verfahren wird beschrieben, wie eine Verbindung mit dem WMI-Dienst und dem Datenspeicher hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="289ae-114">The following procedure describes how to connect to the WMI service and data store.</span></span>

<span data-ttu-id="289ae-115">**So stellen Sie eine Verbindung mit dem WMI-Dienst und Datenspeicher her**</span><span class="sxs-lookup"><span data-stu-id="289ae-115">**To connect to the WMI service and data store**</span></span>

1.  <span data-ttu-id="289ae-116">Suchen Sie den WMI-Dienst auf einem bestimmten Computer.</span><span class="sxs-lookup"><span data-stu-id="289ae-116">Locate the WMI service on a specific machine.</span></span>
2.  <span data-ttu-id="289ae-117">Stellen Sie eine Verbindung mit einem oder mehreren WMI-Namespaces her.</span><span class="sxs-lookup"><span data-stu-id="289ae-117">Connect to one or more WMI namespaces.</span></span>

<span data-ttu-id="289ae-118">Diese Vorgänge unterscheiden sich in C++, Visual Basic, .NET Framework Sprachen oder bei Verwendung eines Skripts.</span><span class="sxs-lookup"><span data-stu-id="289ae-118">These operations are different in C++, Visual Basic, .NET Framework languages, or when using a script.</span></span> <span data-ttu-id="289ae-119">Skripts und Visual Basic Anwendungen müssen auf Klassen zugreifen, deren Instanzen von vorhandenen Anbietern mit Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="289ae-119">Scripts and Visual Basic applications must access classes whose instances are supplied with data by existing providers.</span></span> <span data-ttu-id="289ae-120">Anwendungen, die in C++ geschrieben wurden, können jedoch mehr tun.</span><span class="sxs-lookup"><span data-stu-id="289ae-120">But applications written in C++ can do more.</span></span> <span data-ttu-id="289ae-121">Beispielsweise kann eine in C++ geschriebene Anwendung Ereignisse senden, aber ein WMI-Skript kann nur Empfangs Ereignisse abonnieren.</span><span class="sxs-lookup"><span data-stu-id="289ae-121">For example, an application written in C++ can send events, but a WMI script can only subscribe to receive events.</span></span>

<span data-ttu-id="289ae-122">Ein WMI-Anbieter kann nur in C++ oder mithilfe der .NET Framework geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="289ae-122">A WMI provider can be written only in C++ or using the .NET Framework.</span></span> <span data-ttu-id="289ae-123">Weitere Informationen zum Schreiben von Anwendungen in c# oder Visual Basic .net finden Sie unter [Übersicht über WMI .net](/previous-versions/bb404655(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="289ae-123">For more information about writing applications in C# or Visual Basic .NET, see [WMI .NET Overview](/previous-versions/bb404655(v=vs.90)).</span></span>

<span data-ttu-id="289ae-124">Weitere Informationen zum Erstellen von Anwendungen und Skripts für WMI finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="289ae-124">For more information about creating applications and scripts for WMI, see:</span></span>

-   [<span data-ttu-id="289ae-125">Erstellen einer WMI-Anwendung mithilfe von C++</span><span class="sxs-lookup"><span data-stu-id="289ae-125">Creating a WMI Application Using C++</span></span>](creating-a-wmi-application-using-c-.md)
-   [<span data-ttu-id="289ae-126">Erstellen eines WMI-Skripts</span><span class="sxs-lookup"><span data-stu-id="289ae-126">Creating a WMI Script</span></span>](creating-a-wmi-script.md)
-   [<span data-ttu-id="289ae-127">Erstellen eines verwalteten WMI-Clients</span><span class="sxs-lookup"><span data-stu-id="289ae-127">Creating a Managed WMI Client</span></span>](creating-a-managed-wmi-client.md)

<span data-ttu-id="289ae-128">Verwenden Sie die vorinstallierten [WMI-Klassen](wmi-classes.md), um die meisten Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="289ae-128">To perform most tasks, use the preinstalled [WMI classes](wmi-classes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="289ae-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="289ae-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="289ae-130">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="289ae-130">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
