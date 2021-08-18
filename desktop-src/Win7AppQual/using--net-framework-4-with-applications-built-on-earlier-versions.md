---
description: Verwenden .NET Framework 4 mit Anwendungen, die auf früheren Versionen basiert
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Verwenden .NET Framework 4 mit Anwendungen, die auf früheren Versionen basiert
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c400f38efe93d2fc77d5de1f700b550f455f3e29db8ba96ef778771d82158c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994570"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Verwenden .NET Framework 4 mit Anwendungen, die auf früheren Versionen basiert

## <a name="platform"></a>Plattform

 **Clients** – Windows XP, Windows Vista, Windows 7  
**Server** – Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Auswirkung von Features

 **Schweregrad:** Niedrig  
**Häufigkeit** – Hoch  






## <a name="description"></a>Beschreibung

Die .NET Framework 4 ist hochkompatibel mit Anwendungen, die mit früheren Versionen .NET Framework wurden. Die wichtigsten Änderungen in .NET Framework 4 sind die Verbesserung von Sicherheit, Standardskonformität, Richtigkeit, Zuverlässigkeit und Leistung.

In .NET Framework 4 wird die Version der Common Language Runtime (CLR) jedoch nicht automatisch zum Ausführen von Anwendungen verwendet, die mit früheren Versionen des -.NET Framework.

## <a name="manifestation"></a>Manifestation

Wenn Sie eine Anwendung mit einer früheren .NET Framework erstellt haben und ein Benutzer diese Anwendung auf einem Computer öffnet, auf dem sowohl .NET Framework 4 als auch die frühere Version von .NET Framework installiert sind, verwendet die Anwendung die frühere CLR-Version.

Wenn jedoch .NET Framework 4 die einzige Runtimeversion ist, die auf dem Computer installiert ist, löst die Anwendung eine Ausnahme aus und fordert den Benutzer auf, die Runtimeversion zu installieren, für die Sie die Anwendung erstellt haben.

## <a name="solution"></a>Lösung

Zum Ausführen von Anwendungen, die mit früheren .NET Framework-Versionen mit .NET Framework 4 erstellt wurden, müssen Sie die Anwendung kompilieren, um die .NET Framework 4-Version als Ziel festzulegen, indem Sie sie in den Eigenschaften für Ihr Projekt in Microsoft Visual Studio angeben, oder Sie können .NET Framework 4 im -Element [**<supportedRuntime> in**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) einer Anwendungskonfigurationsdatei angeben.

Weitere Informationen zum Migrieren zu .NET Framework 4 finden Sie im Migrationshandbuch zu [.NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) und unter [Versionskompatibilität im .NET Framework.](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))

## <a name="compatibility-tests"></a>Kompatibilitätstests

Nachdem Sie die Änderungen vorgenommen haben, testen Sie die Anwendung, um sicherzustellen, dass sie ordnungsgemäß ausgeführt wird. Sie können die Kompatibilität testen, wie im Thema [.NET Framework 4 Anwendungskompatibilität beschrieben.](/previous-versions/dd889541(v=msdn.10))

Wenn Ihre Anwendung oder Komponente nach der Installation von .NET Framework 4 nicht funktioniert, übermitteln Sie einen Fehler über die [Microsoft Verbinden](https://connect.microsoft.com/visualstudio) Website.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [**<supportedRuntime> Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Migrationshandbuch zu .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Kompatibilität von .NET Framework-Versionen](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **.NET Framework 4 RTM-Anwendungskompatibilität – Exemplarische Vorgehensweise:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
