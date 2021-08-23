---
description: Eine Windows-Assembly wird durch Manifeste beschrieben.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Informationen zu parallelen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e38ee058965b45c3094888aa34351114aa93e595e4e8b893889daaa685410a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142598"
---
# <a name="about-side-by-side-assemblies"></a>Informationen zu parallelen Assemblys

Eine Windows-Assembly wird durch [Manifeste](manifests.md)beschrieben. Eine side-by-side-Assembly enthält eine Sammlung von Ressourcen – eine Gruppe von DLLs, Windows Klassen, COM-Servern, Typbibliotheken oder Schnittstellen –, die anwendungen immer zusammen bereitgestellt werden. Diese werden im Assemblymanifest beschrieben.

In der Regel ist eine side-by-side-Assembly eine einzelne DLL. Beispielsweise ist die Microsoft COMCTL32-Assembly eine einzelne DLL mit einem Manifest, während die Assembly Microsoft Visual C++ Laufzeitbibliotheken des Entwicklungssystems mehrere Dateien enthält. Manifeste enthalten [*Metadaten,*](m-sbscs-gly.md) die nebenseitige Assemblys und abhängigkeiten von nebenseitigen Assemblys beschreiben.

Nebenassemblys werden vom Betriebssystem als grundlegende Einheiten für Benennung, Bindung, Versionierung, Bereitstellung und Konfiguration verwendet. Jede nebeneinander stehende Assembly verfügt über eine eindeutige Identität. Eines der Attribute der Assemblyidentität ist seine Version. Weitere Informationen finden Sie unter [Assemblyversionen.](assembly-versions.md)

Ab Windows XP können mehrere Versionen paralleler Assemblys von Anwendungen verwendet werden, die gleichzeitig ausgeführt werden. Manifeste und die Assemblyversionsnummer werden vom Ladeprogramm verwendet, um die richtige Bindung von Assemblyversionen an Anwendungen zu bestimmen. Parallele Assemblys und Manifeste funktionieren mit Anwendungen und dem parallelen Manager, wie in der folgenden Abbildung dargestellt.

![Darstellung einer typischen side-by-side-Assembly](images/sxsman.png)

Im vorherigen Beispiel befinden sich sowohl Comctl32.DLL Version 6.0 als auch Comctl32.DLL Version 5.0 im parallelen Assemblycache und sind für Anwendungen verfügbar. Wenn eine Anwendung aufruft, um die DLL zu laden, bestimmt der parallele Manager, ob für die Anwendung eine Versionsabhängigkeit vorliegt, die in einem Manifest beschrieben ist. Wenn kein relevantes Manifest vorhanden ist, lädt das System die Standardversion der Assembly. Für Windows XP ist Version 5.0 von Comctl32.DLL die Standardeinstellung des Systems. Wenn der parallele Manager eine Abhängigkeit von Version 6.0 findet, die in einem Manifest angegeben ist, wird diese Version geladen, um mit der Anwendung ausgeführt zu werden.

Mehrere wichtige Systemassemblys werden von Microsoft als nebenseitige Assemblys zur Verfügung gestellt. Weitere Informationen finden Sie unter [Unterstützte microsoftseitige Assemblys.](supported-microsoft-side-by-side-assemblies.md) Anwendungsentwickler können auch ihre eigenen nebenseitigen Assemblys erstellen. Weitere Informationen finden Sie unter [Guidelines for Creating Side-by-side Assemblies](guidelines-for-creating-side-by-side-assemblies.md). In vielen Fällen ist es möglich, vorhandene Anwendungen so zu aktualisieren, dass sie parallele Assemblys verwenden, ohne den Anwendungscode ändern zu müssen.

Entwicklern wird empfohlen, aus den folgenden Gründen die verwendung von assemblys nebeneinander zu verwenden, um [isolierte Anwendungen](isolated-applications.md)zu erstellen und vorhandene Anwendungen in isolierte Anwendungen zu aktualisieren:

-   Nebenseitige Assemblys verringern die Wahrscheinlichkeit von DLL-Versionskonflikten.
-   Durch die parallele Assemblyfreigabe können mehrere Versionen von COM- oder Windows Assemblys gleichzeitig ausgeführt werden.
-   Anwendungen und Administratoren können die Assemblykonfiguration nach [der](publisher-configuration.md) Bereitstellung entweder global [oder](per-application-configuration.md) anwendungsbezogen aktualisieren. Beispielsweise kann eine Anwendung so aktualisiert werden, dass sie eine nebenseitige Assembly verwendet, die ein Update enthält, ohne die Anwendung neu installieren zu müssen.

 

 



