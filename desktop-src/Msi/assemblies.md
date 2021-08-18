---
description: Windows Das Installationsprogramm kann Win32-Assemblys und -Assemblys installieren, entfernen und aktualisieren, die von der Common Language Runtime des Microsoft-.NET Framework.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a228dfad8155b9282f7ed5ee5c288a858f55c74c432ec6d21fd98aae58f98472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118639272"
---
# <a name="assemblies"></a>Assemblys

Windows Das Installationsprogramm kann Win32-Assemblys und -Assemblys installieren, entfernen und aktualisieren, die von der Common Language Runtime des Microsoft-.NET Framework. Eine Assembly wird vom Windows Installer als einzelne Installerkomponente behandelt. Alle Dateien, aus denen eine Assembly besteht, müssen in einer einzelnen Installationskomponente enthalten sein, die in der Tabelle [Komponente aufgeführt](component-table.md) ist.

Windows Installationsprogramme, die auf Windows Vista und Windows XP ausgeführt werden, können nebenseitige Assemblys installieren. Gleichzeitige Assemblys können Assemblys sicher für mehrere Anwendungen freigeben und die negativen Auswirkungen der Assemblyfreigabe, z. B. DLL-Konflikte, ausgleichen. Anstelle einer einzelnen Version einer Assembly, die Abwärtskompatibilität mit allen Anwendungen voraus setzt, ermöglicht die parallele Assemblyfreigabe die gleichzeitige Ausführung mehrerer Versionen einer COM- oder Win32-Assembly auf dem System. Diese verbesserte Funktion zum Isolieren von Anwendungen ist ein wichtiger Bestandteil der Microsoft-.NET Framework. Weitere Informationen finden Sie unter [Isolierte Anwendungen und nebenseitige Assemblys.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

In den folgenden Abschnitten wird die Verwendung von Assemblys mit dem Windows beschrieben.

-   [Hinzufügen von Assemblys zu einem Paket](adding-assemblies-to-a-package.md)
-   [Installieren und Entfernen von Assemblys](installing-and-removing-assemblies.md)
-   [Aktualisieren von Assemblys](updating-assemblies.md)
-   [Neuinstallationsmodi von Common Language Runtime-Assemblys](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Assemblyregistrierungsschlüssel, die vom Windows geschrieben wurden](assembly-registry-keys-written-by-windows-installer-.md)

Informationen zum Installieren von COM- und COM+1.0-Anwendungen finden Sie unter Installieren einer [COM+-Anwendung](installing-a-com--application-with-the-windows-installer.md)mit dem Windows-Installer, Installieren einer [COM-Komponente](installing-a-com-component-to-a-private-location.md)an einem privaten Speicherort und Erstellen einer COM-Komponente in einem vorhandenen privaten [Paket.](make-a-com-component-in-an-existing-package-private.md)

 

 
