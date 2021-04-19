---
description: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ef252d128ae5d3c8f5b85ef486828fb82e152d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363846"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="dbe9d-103">Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren</span><span class="sxs-lookup"><span data-stu-id="dbe9d-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="dbe9d-104">Plattform</span><span class="sxs-lookup"><span data-stu-id="dbe9d-104">Platform</span></span>

 <span data-ttu-id="dbe9d-105">**Clients** -Windows XP \| Windows Vista \| Windows 7</span><span class="sxs-lookup"><span data-stu-id="dbe9d-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  
<span data-ttu-id="dbe9d-106">**Server** -Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="dbe9d-106">**Servers** - Windows Server 2003 \| Windows Server 2008 \| Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="dbe9d-107">Auswirkungen von Features</span><span class="sxs-lookup"><span data-stu-id="dbe9d-107">Feature Impact</span></span>

 <span data-ttu-id="dbe9d-108">**Schweregrad** -niedrig</span><span class="sxs-lookup"><span data-stu-id="dbe9d-108">**Severity** - Low</span></span>  
<span data-ttu-id="dbe9d-109">**Häufigkeit** -hoch</span><span class="sxs-lookup"><span data-stu-id="dbe9d-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="dbe9d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dbe9d-110">Description</span></span>

<span data-ttu-id="dbe9d-111">Der .NET Framework 4 ist hochgradig kompatibel mit Anwendungen, die mit früheren .NET Framework Versionen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="dbe9d-112">Die wichtigsten Änderungen in .NET Framework 4 sind das Verbessern der Sicherheit, der Einhaltung von Standards, der Richtigkeit, Zuverlässigkeit und Leistung.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="dbe9d-113">Allerdings verwendet .NET Framework 4 nicht automatisch seine Version des Common Language Runtime (CLR), um Anwendungen auszuführen, die mit früheren Versionen der .NET Framework erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="dbe9d-114">Ausstrahlung</span><span class="sxs-lookup"><span data-stu-id="dbe9d-114">Manifestation</span></span>

<span data-ttu-id="dbe9d-115">Wenn Sie eine Anwendung mit einer früheren .NET Framework erstellt haben und ein Benutzer diese Anwendung auf einem Computer öffnet, auf dem sowohl .NET Framework 4 als auch die frühere Version des .NET Framework installiert ist, verwendet die Anwendung die frühere CLR-Version.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="dbe9d-116">Wenn das .NET Framework 4 jedoch die einzige auf dem Computer installierte Laufzeitversion ist, löst die Anwendung eine Ausnahme aus und fordert den Benutzer auf, die Laufzeitversion zu installieren, für die Sie die Anwendung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="dbe9d-117">Lösung</span><span class="sxs-lookup"><span data-stu-id="dbe9d-117">Solution</span></span>

<span data-ttu-id="dbe9d-118">Zum Ausführen von Anwendungen, die mit früheren .NET Framework Versionen mit .NET Framework 4 erstellt wurden, müssen Sie die Anwendung so kompilieren, dass Sie auf die .NET Framework 4-Version ausgerichtet ist, indem Sie Sie in den Eigenschaften für das Projekt in Microsoft Visual Studio angeben, oder Sie können .NET Framework 4 im- [**<supportedRuntime> Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in einer Anwendungs Konfigurationsdatei angeben.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="dbe9d-119">Weitere Informationen zum Migrieren auf die .NET Framework 4 finden Sie im [Migrations Handbuch zu den .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) und [Versions Kompatibilität im .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="dbe9d-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="dbe9d-120">Kompatibilitäts Tests</span><span class="sxs-lookup"><span data-stu-id="dbe9d-120">Compatibility Tests</span></span>

<span data-ttu-id="dbe9d-121">Nachdem Sie die Änderungen vorgenommen haben, testen Sie Ihre Anwendung, um sicherzustellen, dass Sie ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="dbe9d-122">Sie können die Kompatibilität wie im Thema [.NET Framework 4-Anwendungs Kompatibilität](/previous-versions/dd889541(v=msdn.10)) beschrieben testen.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="dbe9d-123">Wenn Ihre Anwendung oder Komponente nach der Installation von .NET Framework 4 nicht funktioniert, senden Sie einen Fehler über die [Microsoft Connect](https://connect.microsoft.com/visualstudio) -Website.</span><span class="sxs-lookup"><span data-stu-id="dbe9d-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="dbe9d-124">Links zu anderen Ressourcen</span><span class="sxs-lookup"><span data-stu-id="dbe9d-124">Links to Other Resources</span></span>

-   <span data-ttu-id="dbe9d-125">[**<supportedRuntime> gewisses**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="dbe9d-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="dbe9d-126">[Migrationshandbuch zu .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dbe9d-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="dbe9d-127">[Kompatibilität von .NET Framework-Versionen](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dbe9d-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="dbe9d-128">**Exemplarische Vorgehensweise zur .NET Framework 4 RTM-Anwendungs Kompatibilität:**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="dbe9d-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="dbe9d-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="dbe9d-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
