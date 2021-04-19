---
description: Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und Quell Abbild Generierung für Mergemodule implementiert. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungs Clients, einschließlich Visual Basic und VBScript.
ms.assetid: 877d3691-948f-4aea-89d8-0ff008126ccc
title: Modul Automatisierung zusammenführen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8ae27370b2ad898cf9413567285afc41d117815
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366219"
---
# <a name="merge-module-automation"></a><span data-ttu-id="12188-104">Modul Automatisierung zusammenführen</span><span class="sxs-lookup"><span data-stu-id="12188-104">Merge Module Automation</span></span>

<span data-ttu-id="12188-105">Mergemod.dll stellt ein COM-Objekt bereit, das Mergevorgänge und Quell Abbild Generierung für Mergemodule implementiert.</span><span class="sxs-lookup"><span data-stu-id="12188-105">Mergemod.dll provides a COM object that implements merge operations and source image generation for merge modules.</span></span> <span data-ttu-id="12188-106">Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme und Automatisierungs Clients, einschließlich Visual Basic und VBScript.</span><span class="sxs-lookup"><span data-stu-id="12188-106">The main object implements interfaces for C/C++ programs and automation clients, including Visual Basic and VBScript.</span></span>

<span data-ttu-id="12188-107">Die bevorzugte Methode zum Installieren von Mergemod.dll ist die Verwendung der Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="12188-107">The preferred method for installing Mergemod.dll is by using the Windows Installer.</span></span> <span data-ttu-id="12188-108">Die Komponenten-ID der Komponente, die die Mergemod.dll com-Schnittstelle enthält, ist {FD153241-37EC-11d2-8892-00A0C981B015}.</span><span class="sxs-lookup"><span data-stu-id="12188-108">The Component ID for the component containing the Mergemod.dll COM interface is {FD153241-37EC-11D2-8892-00A0C981B015}.</span></span> <span data-ttu-id="12188-109">Die gleiche Binärdatei kann auf allen Windows-Systemen verwendet werden, und die dll wird über regsvr32 auf älteren Systemen selbst registriert.</span><span class="sxs-lookup"><span data-stu-id="12188-109">The same binary can be used on all Windows systems and the dll will self-register through regsvr32 on older systems.</span></span>

<span data-ttu-id="12188-110">Beachten Sie, dass Mergemod.dll erfordert, dass die Msvcrt.dll auf dem System installiert ist.</span><span class="sxs-lookup"><span data-stu-id="12188-110">Note that Mergemod.dll requires that the Msvcrt.dll be installed on the system.</span></span>

<span data-ttu-id="12188-111">Beachten Sie, dass Mergemod.dll 2,0 erforderlich ist, um [konfigurierbare Mergemodule](configurable-merge-modules.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="12188-111">Note that Mergemod.dll 2.0 is required to create [Configurable Merge Modules](configurable-merge-modules.md).</span></span> <span data-ttu-id="12188-112">Mergemod.dll Version 2,0 bietet erweiterte Funktionalität zur Buildzeit über die [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="12188-112">Mergemod.dll version 2.0 provides extended functionality at build time through the [**IMsmMerge2**](/windows/desktop/api/Mergemod/nn-mergemod-imsmmerge2) Interface.</span></span> <span data-ttu-id="12188-113">Diese CLSID unterstützt alle vorhandenen Funktionen der [**imsmmerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) -Schnittstelle, die von Mergemod.dll Version 1,0 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12188-113">This CLSID supports all the existing functionality of the [**IMsmMerge**](/windows/win32/api/mergemod/nn-mergemod-imsmmerge) Interface provided by Mergemod.dll version 1.0.</span></span> <span data-ttu-id="12188-114">Die Standardschnittstelle für das [**Merge**](merge-object.md) -Objekt von Mergemod.dll 2,0 ist die **IMsmMerge2** -Schnittstelle anstelle der **imsmmerge** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="12188-114">The default interface on the [**Merge**](merge-object.md) object of Mergemod.dll 2.0 is the **IMsmMerge2** interface instead of the **IMsmMerge** interface.</span></span>

[<span data-ttu-id="12188-115">Objektmodell für Mergemod.dll Version 1,0</span><span class="sxs-lookup"><span data-stu-id="12188-115">Object Model for Mergemod.dll Version 1.0</span></span>](object-model-for-mergemod-dll-version-1-0.md)

[<span data-ttu-id="12188-116">Objektmodell für Mergemod.dll Version 2,0</span><span class="sxs-lookup"><span data-stu-id="12188-116">Object Model for Mergemod.dll Version 2.0</span></span>](object-model-for-mergemod-dll-version-2-0.md)

 

 
