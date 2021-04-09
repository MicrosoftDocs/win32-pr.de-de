---
description: Eine parallele Windows-Assembly wird durch Manifeste beschrieben.
ms.assetid: 501BBFFE-5927-4656-8EEE-1F6ECFAFEF5E
title: Informationen zu parallelen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e190e6428f2e366af45a4f0961ad6ea6fb3561fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959646"
---
# <a name="about-side-by-side-assemblies"></a>Informationen zu parallelen Assemblys

Eine parallele Windows-Assembly wird durch [Manifeste](manifests.md)beschrieben. Eine parallele Assembly enthält eine Sammlung von Ressourcen – eine Gruppe von DLLs, Windows-Klassen, com-Servern, Typbibliotheken oder Schnittstellen –, die für Anwendungen immer zusammen bereitgestellt werden. Diese werden im Assemblymanifest beschrieben.

In der Regel ist eine parallele Assembly eine einzelne DLL. Beispielsweise ist die Microsoft ComCtl32-Assembly eine einzelne DLL mit einem Manifest, während die Assembly der Laufzeitbibliotheken für Microsoft Visual C++ Entwicklungssystem mehrere Dateien enthält. Manifeste enthalten [*Metadaten*](m-sbscs-gly.md) , die parallele Assemblys und parallele Assemblyabhängigkeiten beschreiben.

Parallele Assemblys werden vom Betriebssystem als grundlegende Einheiten für Benennung, Bindung, Versionsverwaltung, Bereitstellung und Konfiguration verwendet. Jede parallele Assembly verfügt über eine eindeutige Identität. Eines der Attribute der Assemblyidentität ist seine Version. Weitere Informationen finden Sie unter [Assemblyversionen](assembly-versions.md).

Ab Windows XP können von Anwendungen, die gleichzeitig ausgeführt werden, mehrere Versionen paralleler Assemblys verwendet werden. Manifeste und die Assemblyversionsnummer werden vom Lade Programme verwendet, um die korrekte Bindung von Assemblyversionen an Anwendungen zu bestimmen. Parallele Assemblys und Manifeste arbeiten mit Anwendungen und dem parallelen Manager, wie in der folgenden Abbildung veranschaulicht.

![Darstellung typischer paralleler Assemblys](images/sxsman.png)

Im vorherigen Beispiel befinden sich sowohl die Comctl32.DLL Version 6,0 als auch Comctl32.DLL Version 5,0 im parallelen Assemblycache und sind für Anwendungen verfügbar. Wenn eine Anwendung aufruft, um die dll zu laden, bestimmt der parallele Manager, ob die Anwendung eine Versionsabhängigkeit hat, die in einem Manifest beschrieben wird. Wenn kein relevantes Manifest vorhanden ist, lädt das System die Standardversion der Assembly. Bei Windows XP ist Version 5,0 von Comctl32.DLL der System Standardwert. Wenn der parallele Manager eine Abhängigkeit von der in einem Manifest angegebenen Version 6,0 findet, wird diese Version geladen, damit Sie mit der Anwendung ausgeführt wird.

Mehrere schlüsselsystemassemblys werden von Microsoft als parallele Assemblys zur Verfügung gestellt. Weitere Informationen finden Sie [unter Unterstützte](supported-microsoft-side-by-side-assemblies.md)parallele Assemblys von Microsoft. Anwendungsentwickler können auch Ihre eigenen parallelen Assemblys erstellen. Weitere Informationen finden Sie unter [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md)paralleler Assemblys. In vielen Fällen ist es möglich, vorhandene Anwendungen so zu aktualisieren, dass Sie parallele Assemblys verwenden, ohne den Anwendungscode ändern zu müssen.

Entwicklern wird empfohlen, parallele Assemblys zu verwenden, um [isolierte Anwendungen](isolated-applications.md)zu erstellen und vorhandene Anwendungen aus folgenden Gründen in isolierte Anwendungen zu aktualisieren:

-   Parallele Assemblys reduzieren die Wahrscheinlichkeit von dll-Versions Konflikten.
-   Die parallele assemblyfreigabe ermöglicht das gleichzeitige Ausführen mehrerer Versionen von com-oder Windows-Assemblys.
-   Anwendungen und Administratoren können die Assemblykonfiguration nach der Bereitstellung entweder auf [globaler](publisher-configuration.md) oder [Anwendungs](per-application-configuration.md) Basis aktualisieren. Beispielsweise kann eine Anwendung so aktualisiert werden, dass Sie eine parallele Assembly verwendet, die ein Update enthält, ohne dass die Anwendung neu installiert werden muss.

 

 



