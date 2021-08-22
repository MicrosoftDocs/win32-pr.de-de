---
description: Installieren Sie Win32-Assemblys, indem Sie sie zu einer Komponente des Microsoft Windows Installer-Pakets machen, das Ihre Anwendung installiert oder aktualisiert.
ms.assetid: 09aecb55-ed45-45b3-b27a-d0946223392a
title: Installation von Win32-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27c680d53e1c4702bab3b9a24920b18a2fdb644a86c41207712ec3726a310a8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633840"
---
# <a name="installation-of-win32-assemblies"></a>Installation von Win32-Assemblys

Installieren Sie Win32-Assemblys, indem Sie sie zu einer Komponente des Microsoft Windows Installer-Pakets machen, das Ihre Anwendung installiert oder aktualisiert. Wenn Sie die [MsiAssembly-Tabelle](msiassembly-table.md) und [die MsiAssemblyName-Tabelle](msiassemblyname-table.md)erstellen, identifiziert dies die Komponente in der Component -Spalte \_ als Assembly. Das Installationsprogramm setzt die [**MsiWin32AssemblySupport-Eigenschaft**](msiwin32assemblysupport.md) auf die Dateiversion von Sxs.dll auf Betriebssystemen, die Win32-Assemblys unterstützen können, und diese Eigenschaft andernfalls nicht fest.

In Windows Vista und Windows XP schreibt Windows Installer keine Assemblyinformationen in die Registrierung. Darüber hinaus können freigegebene Assemblys, private Assemblys und side-by-side-Assemblys verwendet werden. Weitere Informationen finden Sie unter [Freigegebene Assemblys,](shared-assemblies.md) [private Assemblys](private-assemblies.md)und [nebeneinander seitige Assemblys.](side-by-side-assemblies.md)

In den folgenden Abschnitten wird beschrieben, wie Sie ein Windows Installer-Paket erstellen, um Win32-Assemblys auf verschiedenen Betriebssystemen als freigegebene, private oder Windows zu installieren.

-   [Installieren von Win32-Assemblys für die side-by-side-Freigabe auf Windows XP](installing-win32-assemblies-for-side-by-side-sharing-on-windows-xp.md)
-   [Installieren von Win32-Assemblys für die private Verwendung einer Anwendung auf Windows XP](installing-win32-assemblies-for-the-private-use-of-an-application-on-windows-xp.md)

 

 



