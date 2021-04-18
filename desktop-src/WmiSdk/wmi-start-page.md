---
description: Windows-Verwaltungsinstrumentation (WMI) ist die Infrastruktur für Verwaltungsdaten und Vorgänge auf Windows-basierten Betriebssystemen.
ms.assetid: 4804152f-2042-4c6a-83c6-75c5e1ab7a04
ms.tgt_platform: multiple
title: Windows-Verwaltungsinstrumentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ec2313ca7ee744ebe6f14be42a33e2e5878960b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347913"
---
# <a name="windows-management-instrumentation"></a><span data-ttu-id="a1ba2-103">Windows-Verwaltungsinstrumentation</span><span class="sxs-lookup"><span data-stu-id="a1ba2-103">Windows Management Instrumentation</span></span>

## <a name="purpose"></a><span data-ttu-id="a1ba2-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="a1ba2-104">Purpose</span></span>

<span data-ttu-id="a1ba2-105">Windows-Verwaltungsinstrumentation (WMI) ist die Infrastruktur für Verwaltungsdaten und Vorgänge auf Windows-basierten Betriebssystemen.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-105">Windows Management Instrumentation (WMI) is the infrastructure for management data and operations on Windows-based operating systems.</span></span> <span data-ttu-id="a1ba2-106">Sie können WMI-Skripts oder-Anwendungen schreiben, um administrative Aufgaben auf Remote Computern zu automatisieren, aber WMI stellt auch Verwaltungsdaten für andere Teile des Betriebssystems und der Produkte bereit, z. b. System Center Operations Manager, früher Microsoft Operations Manager (MOM) oder Windows-Remoteverwaltung ([WinRM](/windows/desktop/WinRM/portal)).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-106">You can write WMI scripts or applications to automate administrative tasks on remote computers but WMI also supplies management data to other parts of the operating system and products, for example System Center Operations Manager, formerly Microsoft Operations Manager (MOM), or Windows Remote Management ([WinRM](/windows/desktop/WinRM/portal)).</span></span>

> [!Note]  
> <span data-ttu-id="a1ba2-107">Die folgende Dokumentation richtet sich an Entwickler und IT-Administratoren.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-107">The following documentation is targeted for developers and IT administrators.</span></span> <span data-ttu-id="a1ba2-108">Wenn Sie ein Endbenutzer sind, bei dem eine Fehlermeldung zu WMI aufgetreten ist, sollten Sie [Microsoft-Support](https://support.microsoft.com/) aufrufen und nach dem Fehlercode suchen, der in der Fehlermeldung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-108">If you are an end-user that has experienced an error message concerning WMI, you should go to [Microsoft Support](https://support.microsoft.com/) and search for the error code you see on the error message.</span></span> <span data-ttu-id="a1ba2-109">Weitere Informationen zur Behebung von Problemen mit WMI-Skripts und dem WMI-Dienst finden Sie unter [WMI funktioniert nicht!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="a1ba2-109">For more information about troubleshooting problems with WMI scripts and the WMI service, see [WMI Isn't Working!](/previous-versions/tn-archive/ff406382(v=msdn.10))</span></span>

 

> [!Note]  
> <span data-ttu-id="a1ba2-110">WMI wird von Microsoft vollständig unterstützt. die neueste Version von administrativer Skripterstellung und-Steuerung ist jedoch über die Windows-Verwaltungsinfrastruktur (Mi) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-110">WMI is fully supported by Microsoft; however, the latest version of administrative scripting and control is available through the Windows Management Infrastructure (MI).</span></span> <span data-ttu-id="a1ba2-111">Mi ist vollständig kompatibel mit früheren Versionen von WMI und bietet eine Reihe von Features und Vorteilen, mit denen das Entwerfen und entwickeln von Anbietern und Clients einfacher als je zuvor ist.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-111">MI is fully compatible with previous versions of WMI, and provides a host of features and benefits that make designing and developing providers and clients easier than ever.</span></span> <span data-ttu-id="a1ba2-112">Weitere Informationen finden Sie unter [Windows Management Infrastructure (Mi)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-112">For more information, see [Windows Management Infrastructure (MI)](/previous-versions/windows/desktop/wmi_v2/windows-management-infrastructure).</span></span>

 

## <a name="where-applicable"></a><span data-ttu-id="a1ba2-113">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="a1ba2-113">Where applicable</span></span>

<span data-ttu-id="a1ba2-114">WMI kann in allen Windows-basierten Anwendungen verwendet werden und ist am nützlichsten in Unternehmensanwendungen und administrativen Skripts.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-114">WMI can be used in all Windows-based applications, and is most useful in enterprise applications and administrative scripts.</span></span>

<span data-ttu-id="a1ba2-115">System Administratoren finden Informationen zur Verwendung von WMI im TechNet [scriptcenter](https://www.microsoft.com/technet/scriptcenter/default.mspx)und in verschiedenen Büchern zu WMI.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-115">System administrators can find information about using WMI at the TechNet [ScriptCenter](https://www.microsoft.com/technet/scriptcenter/default.mspx), and in various books about WMI.</span></span> <span data-ttu-id="a1ba2-116">Weitere Informationen finden Sie unter [Weitere Informationen](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-116">For more information, see [Further Information](further-information.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a1ba2-117">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="a1ba2-117">Developer audience</span></span>

<span data-ttu-id="a1ba2-118">WMI ist für Programmierer konzipiert, die C/C++, die Microsoft Visual Basic-Anwendung oder eine Skriptsprache verwenden, die über eine Engine unter Windows verfügt und Microsoft ActiveX-Objekte verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-118">WMI is designed for programmers who use C/C++, the Microsoft Visual Basic application, or a scripting language that has an engine on Windows and handles Microsoft ActiveX objects.</span></span> <span data-ttu-id="a1ba2-119">Obwohl eine gewisse Vertrautheit mit der com-Programmierung hilfreich ist, können C++-Entwickler, die Anwendungen schreiben, gute Beispiele für den Einstieg in die [Erstellung einer WMI-Anwendung mit C++](creating-a-wmi-application-using-c-.md)finden.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-119">While some familiarity with COM programming is helpful, C++ developers who are writing applications can find good examples for getting started at [Creating a WMI Application Using C++](creating-a-wmi-application-using-c-.md).</span></span>

<span data-ttu-id="a1ba2-120">Informationen zum Entwickeln von verwalteten Code Anbietern oder-Anwendungen in c# oder Visual Basic .NET mithilfe der .NET Framework finden Sie unter [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-120">To develop managed code providers or applications in C# or Visual Basic .NET using the .NET Framework, see [WMI in .NET Framework](/previous-versions/dotnet/netframework-1.1/aa720264(v=vs.71)).</span></span>

<span data-ttu-id="a1ba2-121">Viele Administratoren und IT-Spezialisten greifen über PowerShell auf WMI zu.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-121">Many administrators and IT professionals access WMI through PowerShell.</span></span> <span data-ttu-id="a1ba2-122">Mit dem Cmdlet "Get-WMI" für PowerShell können Sie Informationen für ein lokales oder Remote-WMI-Repository abrufen.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-122">The Get-WMI cmdlet for PowerShell enables you to retrieve information for a local or remote WMI repository.</span></span> <span data-ttu-id="a1ba2-123">Eine Reihe von Themen und Klassen, insbesondere im Abschnitt [Erstellen von WMI-Clients](creating-wmi-clients.md) , enthalten beispielsweise PowerShell-Beispiele.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-123">As such, a number of topics and classes, especially in the [Creating WMI Clients](creating-wmi-clients.md) section, contain PowerShell examples.</span></span> <span data-ttu-id="a1ba2-124">Weitere Informationen zur Verwendung von PowerShell finden Sie unter [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) und [Skripterstellung mit Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-124">For additional information on using PowerShell, see [Windows PowerShell](https://msdn.microsoft.com/library/dd835506.aspx) and [Scripting with Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx).</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a1ba2-125">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="a1ba2-125">Run-time requirements</span></span>

<span data-ttu-id="a1ba2-126">Weitere Informationen über das Betriebssystem, das für die Verwendung eines bestimmten API-Elements oder einer WMI-Klasse erforderlich ist, finden Sie im Abschnitt "Anforderungen" jedes Themas in der WMI-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-126">For more information about which operating system is required to use a specific API element or WMI class, see the Requirements section of each topic in the WMI documentation.</span></span>

<span data-ttu-id="a1ba2-127">Wenn eine erwartete Komponente fehlt, finden Sie weitere Informationen unter [Betriebs System Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-127">If an expected component appears to be missing, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

<span data-ttu-id="a1ba2-128">Sie müssen keine bestimmte Softwareentwicklung (SDK) herunterladen oder installieren, um Skripts oder Anwendungen für WMI zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-128">You do not need to download or install a specific software development (SDK) in order to create scripts or applications for WMI.</span></span> <span data-ttu-id="a1ba2-129">Es gibt jedoch einige WMI-Verwaltungs Tools, die Entwickler nützlich finden.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-129">However, there are some WMI administrative tools that developers find useful.</span></span> <span data-ttu-id="a1ba2-130">Weitere Informationen finden Sie im Abschnitt "Downloads" unter [Weitere Informationen](further-information.md).</span><span class="sxs-lookup"><span data-stu-id="a1ba2-130">For more information, see the Downloads section in [Further Information](further-information.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="a1ba2-131">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a1ba2-131">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="a1ba2-132">Informationen zu WMI</span><span class="sxs-lookup"><span data-stu-id="a1ba2-132">About WMI</span></span>](about-wmi.md)
</dt> <dd>

<span data-ttu-id="a1ba2-133">Allgemeine Informationen zu WMI.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-133">General information about WMI.</span></span>

</dd> <dt>

[<span data-ttu-id="a1ba2-134">Verwenden von WMI</span><span class="sxs-lookup"><span data-stu-id="a1ba2-134">Using WMI</span></span>](using-wmi.md)
</dt> <dd>

<span data-ttu-id="a1ba2-135">Informationen zum Entwickeln von Anwendungen für die Verwendung von WMI, einschließlich Informationen zu-Tools.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-135">Information about how to develop applications to use WMI, which includes information about tools.</span></span>

</dd> <dt>

[<span data-ttu-id="a1ba2-136">WMI-Referenz</span><span class="sxs-lookup"><span data-stu-id="a1ba2-136">WMI Reference</span></span>](wmi-reference.md)
</dt> <dd>

<span data-ttu-id="a1ba2-137">Dokumentation zu den WMI-Klassen, WMI-C++-Klassen, WMI-com-API, Skript-API und anderem WMI-Referenzmaterial.</span><span class="sxs-lookup"><span data-stu-id="a1ba2-137">Documentation about the WMI classes, WMI C++ classes, WMI COM API, Scripting API, and other WMI reference material.</span></span>

</dd> </dl>

 

 
