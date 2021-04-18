---
description: Windows Installer können Win32-Assemblys und Assemblys, die vom Common Language Runtime des Microsoft .NET Frameworks verwendet werden, installieren, entfernen und aktualisieren.
ms.assetid: 88bee87c-fed2-45e9-8d8c-a5bbcc77f266
title: Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb0f2b91a46287262848aaa2174d6bec6688d0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347958"
---
# <a name="assemblies"></a>Assemblys

Windows Installer können Win32-Assemblys und Assemblys, die vom Common Language Runtime des Microsoft .NET Frameworks verwendet werden, installieren, entfernen und aktualisieren. Eine Assembly wird vom Windows Installer als einzelne installerkomponente behandelt. Alle Dateien, die eine Assembly bilden, müssen in einer einzelnen installerkomponente enthalten sein, die in der [Komponenten](component-table.md) Tabelle aufgeführt ist.

Windows Installer, die unter Windows Vista und Windows XP ausgeführt werden, können parallele Assemblys installiert werden. Parallele Assemblys können Assemblys auf sichere Weise für mehrere Anwendungen freigeben und die negativen Auswirkungen der assemblyfreigabe, wie z. b. dll-Konflikte, ausgleichen. Anstelle einer einzelnen Version einer Assembly, die die Abwärtskompatibilität mit allen Anwendungen annimmt, ermöglicht die parallele assemblyfreigabe, dass mehrere Versionen einer com-oder Win32-Assembly gleichzeitig auf dem System ausgeführt werden. Diese verbesserte Funktion zum Isolieren von Anwendungen ist ein wichtiger Bestandteil des Microsoft .NET-Frameworks. Weitere Informationen finden Sie unter [isolierte Anwendungen und](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)parallele Assemblys.

In den folgenden Abschnitten wird die Verwendung von Assemblys mit dem-Windows Installer beschrieben.

-   [Hinzufügen von Assemblys zu Paketen](adding-assemblies-to-a-package.md)
-   [Installieren und Entfernen von Assemblys](installing-and-removing-assemblies.md)
-   [Aktualisieren von Assemblys](updating-assemblies.md)
-   [Neuinstallations Modi von Common Language Runtime-Assemblys](reinstallation-modes-of-common-language-runtime-assemblies.md)
-   [Von Windows Installer geschriebene assemblyregistrierungsschlüssel](assembly-registry-keys-written-by-windows-installer-.md)

Informationen zum Installieren von com-und com+ 1,0-Anwendungen finden Sie unter [Installieren einer COM+-Anwendung mit dem Windows Installer](installing-a-com--application-with-the-windows-installer.md), [Installieren einer COM-Komponente an einem privaten Speicherort](installing-a-com-component-to-a-private-location.md)und [Erstellen einer COM-Komponente in einem vorhandenen Paket](make-a-com-component-in-an-existing-package-private.md).

 

 
