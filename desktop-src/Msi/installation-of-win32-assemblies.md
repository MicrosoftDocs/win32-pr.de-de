---
description: Installieren Sie Win32-Assemblys, indem Sie Sie zu einer Komponente Microsoft Windows Installer Pakets, das die Anwendung installiert oder aktualisiert.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installation von Win32-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9d47847c0c69185a28fa41bbe5c5a05deec1e66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348254"
---
# <a name="installation-of-win32-assemblies"></a>Installation von Win32-Assemblys

Installieren Sie Win32-Assemblys, indem Sie Sie zu einer Komponente Microsoft Windows Installer Pakets, das die Anwendung installiert oder aktualisiert. Wenn Sie die [MsiAssembly-Tabelle](msiassembly-table.md) und die [MsiAssemblyName-Tabelle](msiassemblyname-table.md)erstellen, wird die Komponente in der Component- \_ Spalte als Assembly identifiziert. Das Installationsprogramm legt die [**MsiWin32AssemblySupport**](msiwin32assemblysupport.md) -Eigenschaft auf die Dateiversion von Sxs.dll unter Betriebssystemen fest, die Win32-Assemblys unterstützen und andernfalls diese Eigenschaft nicht festlegen.

In Windows Vista und Windows XP werden von Windows Installer keine Assemblyinformationen in die Registrierung geschrieben. Außerdem können freigegebene Assemblys, private Assemblys und parallele Assemblys verwendet werden. Weitere Informationen finden Sie unter [frei](side-by-side-assemblies.md) [gegebene](shared-assemblies.md)Assemblys, [private](private-assemblies.md)Assemblys und parallele Assemblys.

In den folgenden Abschnitten wird beschrieben, wie ein Windows Installer Paket zum Installieren von Win32-Assemblys als freigegeben, privat oder nebeneinander auf verschiedenen Windows-Betriebssystemen erstellt wird.

-   [Installieren von Win32-Assemblys für die parallele Freigabe unter Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung unter Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



