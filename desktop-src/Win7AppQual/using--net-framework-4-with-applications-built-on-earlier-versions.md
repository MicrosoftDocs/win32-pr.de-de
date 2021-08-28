---
description: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen aufbauen
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen aufbauen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a12eb34b00cfe14a18e83e7726f1ffa962ba03f8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884742"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen aufbauen

## <a name="platform"></a>Plattform

 **Clients** – Windows XP, Windows Vista, Windows 7  
**Server** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Auswirkungen auf Features

 **Schweregrad –** Niedrig  
**Frequency** – High  






## <a name="description"></a>Beschreibung

Die .NET Framework 4 ist hochkompatibel mit Anwendungen, die mit früheren .NET Framework Versionen erstellt wurden. Die wichtigsten Änderungen in .NET Framework 4 sind die Verbesserung der Sicherheit, Standardskonformität, Richtigkeit, Zuverlässigkeit und Leistung.

.NET Framework 4 verwendet jedoch nicht automatisch die Version der Common Language Runtime (CLR), um Anwendungen auszuführen, die mit früheren Versionen der .NET Framework erstellt wurden.

## <a name="manifestation"></a>Manifestation

Wenn Sie eine Anwendung mithilfe eines früheren .NET Framework erstellt haben und ein Benutzer diese Anwendung auf einem Computer öffnet, auf dem sowohl .NET Framework 4 als auch die frühere Version des .NET Framework installiert ist, verwendet die Anwendung die frühere CLR-Version.

Wenn jedoch die .NET Framework 4 die einzige Runtimeversion ist, die auf dem Computer installiert ist, löst die Anwendung eine Ausnahme aus und fordert den Benutzer auf, die Runtimeversion zu installieren, für die Sie die Anwendung erstellt haben.

## <a name="solution"></a>Lösung

Zum Ausführen von Anwendungen, die mit früheren .NET Framework Versionen mit .NET Framework 4 erstellt wurden, müssen Sie die Anwendung kompilieren, um die Version .NET Framework 4 zu verwenden, indem Sie sie in den Eigenschaften für Ihr Projekt in Microsoft Visual Studio angeben. Alternativ können Sie .NET Framework 4 im [**&lt; supportedRuntime-Element &gt;**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in einer Anwendungskonfigurationsdatei angeben.

Weitere Informationen zum Migrieren zum .NET Framework 4 finden Sie im [Migrationshandbuch zu .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) und [Versionskompatibilität im .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Kompatibilitätstests

Nachdem Sie die Änderungen vorgenommen haben, testen Sie Ihre Anwendung, um sicherzustellen, dass sie ordnungsgemäß ausgeführt wird. Sie können die Kompatibilität wie im Thema [.NET Framework 4 Anwendungskompatibilität](/previous-versions/dd889541(v=msdn.10)) beschrieben testen.

Wenn Ihre Anwendung oder Komponente nach der Installation von .NET Framework 4 nicht funktioniert, übermitteln Sie einen Fehler über die [Microsoft Verbinden-Website.](https://connect.microsoft.com/visualstudio)

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [**&lt;&gt;supportedRuntime-Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Migrationshandbuch zu .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Kompatibilität von .NET Framework-Versionen](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework 4 RTM-Anwendungskompatibilität Exemplarische Vorgehensweise:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
