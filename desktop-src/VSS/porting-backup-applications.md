---
description: Binärdateien von Windows Server 2003 mit Service Pack 1 (SP1) sind kompatibel mit Windows Vista und Windows Server 2008. Allerdings müssen Binärdateien aus früheren Versionen von Windows neu kompiliert werden.
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: Portieren von Sicherungs Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528709"
---
# <a name="porting-backup-applications"></a><span data-ttu-id="29860-104">Portieren von Sicherungs Anwendungen</span><span class="sxs-lookup"><span data-stu-id="29860-104">Porting Backup Applications</span></span>

<span data-ttu-id="29860-105">Binärdateien von Windows Server 2003 mit Service Pack 1 (SP1) sind kompatibel mit Windows Vista und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="29860-105">Binaries from Windows Server 2003 with Service Pack 1 (SP1) are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="29860-106">Allerdings müssen Binärdateien aus früheren Versionen von Windows neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="29860-106">However, binaries from earlier versions of Windows must be recompiled.</span></span>

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a><span data-ttu-id="29860-107">Portieren von Windows XP-Sicherungs Anwendungen auf Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29860-107">Porting Windows XP Backup Applications to Windows Vista</span></span>

<span data-ttu-id="29860-108">Mehrere VSS-Schnittstellen wurden seit Windows XP geändert.</span><span class="sxs-lookup"><span data-stu-id="29860-108">Several VSS interfaces have changed since Windows XP.</span></span> <span data-ttu-id="29860-109">Windows XP-Anwendungen müssen mindestens mithilfe von Header Dateien und Bibliotheken aus dem VSS 7,2 SDK oder dem Windows Vista-oder Windows Server 2008 SDK neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="29860-109">At a minimum, Windows XP applications must be recompiled using header files and libraries from the VSS 7.2 SDK or the Windows Vista or Windows Server 2008 SDK.</span></span>

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a><span data-ttu-id="29860-110">Portieren von Windows Server 2003 SP1-Sicherungs Anwendungen auf Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29860-110">Porting Windows Server 2003 SP1 Backup Applications to Windows Vista</span></span>

<span data-ttu-id="29860-111">Binärdateien von Windows Server 2003 mit SP1 sind kompatibel mit Windows Vista und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="29860-111">Binaries from Windows Server 2003 with SP1 are compatible with Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="29860-112">Die meisten Windows Server 2003 mit SP1-Sicherungs Anwendungen müssen jedoch aktualisiert werden, um neue Features zu berücksichtigen, die in den folgenden Abschnitten beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="29860-112">However, most Windows Server 2003 with SP1 backup applications must be updated to account for new features, which are described in the following sections.</span></span>

## <a name="compiling-backup-applications-for-windows-vista"></a><span data-ttu-id="29860-113">Kompilieren von Sicherungs Anwendungen für Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29860-113">Compiling Backup Applications for Windows Vista</span></span>

<span data-ttu-id="29860-114">Anwendungen, die in Windows Server 2003 verfügbare Schnittstellen verwenden, können mithilfe von Header Dateien und Bibliotheken kompiliert werden, die im VSS 7,2 SDK bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="29860-114">Applications that use interfaces available in Windows Server 2003 can be compiled using header files and libraries provided in the VSS 7.2 SDK.</span></span> <span data-ttu-id="29860-115">Zum Verwenden neuer Schnittstellen müssen Anwendungen mithilfe der Header Dateien und Bibliotheken, die im Windows Vista SDK enthalten sind, neu kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="29860-115">To use new interfaces, applications must be recompiled using the header files and libraries included in the Windows Vista SDK.</span></span>

> [!Note]  
> <span data-ttu-id="29860-116">Mit Windows Vista oder Windows Server 2008 kompilierte Binärdateien sind nicht mit Windows Server 2003 mit SP1 oder früheren Windows-Versionen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="29860-116">Binaries compiled using Windows Vista or Windows Server 2008 are not compatible with Windows Server 2003 with SP1 or earlier versions of Windows.</span></span>

 

 

 



