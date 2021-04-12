---
description: Wenn eine Assembly an einem isolierten Speicherort für eine bestimmte Anwendung installiert wird, muss die Anwendung in der Datei \_ Anwendungs Spalte der MsiAssembly-Tabelle angegeben werden.
ms.assetid: 8d7fc09c-1017-4a30-be00-b7b0e5f2a057
title: Installieren und Entfernen von Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44dee05940ab3c05e97a7145f9b2363226bb07c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218539"
---
# <a name="installing-and-removing-assemblies"></a><span data-ttu-id="6e0ab-103">Installieren und Entfernen von Assemblys</span><span class="sxs-lookup"><span data-stu-id="6e0ab-103">Installing and Removing Assemblies</span></span>

<span data-ttu-id="6e0ab-104">Wenn eine Assembly an einem isolierten Speicherort für eine bestimmte Anwendung installiert wird, muss die Anwendung in der Datei \_ Anwendungs Spalte der [MsiAssembly-Tabelle](msiassembly-table.md)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-104">When installing an assembly to an isolated location for a specific application, the application must be specified in the File\_Application column of the [MsiAssembly table](msiassembly-table.md).</span></span> <span data-ttu-id="6e0ab-105">Dieses Feld ist ein Schlüssel in die [Dateitabelle](file-table.md).</span><span class="sxs-lookup"><span data-stu-id="6e0ab-105">This field is a key into the [File table](file-table.md).</span></span> <span data-ttu-id="6e0ab-106">Das Installationsprogramm verwendet die in der [Verzeichnis Tabelle](directory-table.md) angegebene Verzeichnisstruktur, um die Assembly im gleichen Verzeichnis wie die Komponente zu installieren, in der diese Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-106">The installer uses the directory structure that is specified in the [Directory table](directory-table.md) to install the assembly into the same directory as the component that contains this file.</span></span>

<span data-ttu-id="6e0ab-107">Wenn eine Assembly in den globalen Assemblycache installiert wird, muss der Wert in der Datei \_ Anwendungs Spalte der [MsiAssembly-Tabelle](msiassembly-table.md) NULL sein.</span><span class="sxs-lookup"><span data-stu-id="6e0ab-107">When installing an assembly to the global assembly cache, the value in the File\_Application column of the [MsiAssembly Table](msiassembly-table.md) must be Null.</span></span>

<span data-ttu-id="6e0ab-108">In den folgenden Abschnitten wird die Installation von Win32-und Common Language Runtime-Assemblys beschrieben:</span><span class="sxs-lookup"><span data-stu-id="6e0ab-108">The following sections describe the installation of Win32 and common language runtime assemblies:</span></span>

-   [<span data-ttu-id="6e0ab-109">Installation von Win32-Assemblys</span><span class="sxs-lookup"><span data-stu-id="6e0ab-109">Installation of Win32 Assemblies</span></span>](installation-of-win32-assemblies.md)
-   [<span data-ttu-id="6e0ab-110">Installation von Common Language Runtime-Assemblys</span><span class="sxs-lookup"><span data-stu-id="6e0ab-110">Installation of Common Language Runtime Assemblies</span></span>](installation-of-common-language-runtime-assemblies.md)

 

 



