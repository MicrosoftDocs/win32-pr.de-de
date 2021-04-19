---
description: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314943"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a>Verwenden von .NET Framework 4 mit Anwendungen, die auf früheren Versionen basieren

## <a name="platform"></a>Plattform

 **Clients** -Windows XP, Windows Vista, Windows 7  
**Server** -Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="feature-impact"></a>Auswirkungen von Features

 **Schweregrad** -niedrig  
**Häufigkeit** -hoch  






## <a name="description"></a>Beschreibung

Der .NET Framework 4 ist hochgradig kompatibel mit Anwendungen, die mit früheren .NET Framework Versionen erstellt wurden. Die wichtigsten Änderungen in .NET Framework 4 sind das Verbessern der Sicherheit, der Einhaltung von Standards, der Richtigkeit, Zuverlässigkeit und Leistung.

Allerdings verwendet .NET Framework 4 nicht automatisch seine Version des Common Language Runtime (CLR), um Anwendungen auszuführen, die mit früheren Versionen der .NET Framework erstellt wurden.

## <a name="manifestation"></a>Ausstrahlung

Wenn Sie eine Anwendung mit einer früheren .NET Framework erstellt haben und ein Benutzer diese Anwendung auf einem Computer öffnet, auf dem sowohl .NET Framework 4 als auch die frühere Version des .NET Framework installiert ist, verwendet die Anwendung die frühere CLR-Version.

Wenn das .NET Framework 4 jedoch die einzige auf dem Computer installierte Laufzeitversion ist, löst die Anwendung eine Ausnahme aus und fordert den Benutzer auf, die Laufzeitversion zu installieren, für die Sie die Anwendung erstellt haben.

## <a name="solution"></a>Lösung

Zum Ausführen von Anwendungen, die mit früheren .NET Framework Versionen mit .NET Framework 4 erstellt wurden, müssen Sie die Anwendung so kompilieren, dass Sie auf die .NET Framework 4-Version ausgerichtet ist, indem Sie Sie in den Eigenschaften für das Projekt in Microsoft Visual Studio angeben, oder Sie können .NET Framework 4 im- [**<supportedRuntime> Element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in einer Anwendungs Konfigurationsdatei angeben.

Weitere Informationen zum Migrieren auf die .NET Framework 4 finden Sie im [Migrations Handbuch zu den .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) und [Versions Kompatibilität im .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).

## <a name="compatibility-tests"></a>Kompatibilitäts Tests

Nachdem Sie die Änderungen vorgenommen haben, testen Sie Ihre Anwendung, um sicherzustellen, dass Sie ordnungsgemäß ausgeführt wird. Sie können die Kompatibilität wie im Thema [.NET Framework 4-Anwendungs Kompatibilität](/previous-versions/dd889541(v=msdn.10)) beschrieben testen.

Wenn Ihre Anwendung oder Komponente nach der Installation von .NET Framework 4 nicht funktioniert, senden Sie einen Fehler über die [Microsoft Connect](https://connect.microsoft.com/visualstudio) -Website.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

-   [**<supportedRuntime> gewisses**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))
-   [Migrationshandbuch zu .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))
-   [Kompatibilität von .NET Framework-Versionen](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))
-   **Exemplarische Vorgehensweise zur .NET Framework 4 RTM-Anwendungs Kompatibilität:**<https://msdn.microsoft.com/library/dd889541.aspx>
-   [Microsoft Connect](https://connect.microsoft.com/)

 

 
