---
description: Die MsiNetAssemblySupport-Eigenschaft gibt an, ob der Computer Common Language Run-Time-Assemblys unterstützt.
ms.assetid: 32f4f971-8e42-46b0-96e4-b3505abd2314
title: MsiNetAssemblySupport (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eebe81bbde8bb7c97fe2f9a535d0bd9ac82ebec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367639"
---
# <a name="msinetassemblysupport-property"></a><span data-ttu-id="3b189-103">MsiNetAssemblySupport (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="3b189-103">MsiNetAssemblySupport property</span></span>

<span data-ttu-id="3b189-104">Die **MsiNetAssemblySupport** -Eigenschaft gibt an, ob der Computer Common Language Run-Time-Assemblys unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b189-104">The **MsiNetAssemblySupport** property indicates whether the computer supports common language run-time assemblies.</span></span> <span data-ttu-id="3b189-105">Auf Systemen, die Common Language Run-Time-Assemblys unterstützen, legt das Installationsprogramm den Wert von **MsiNetAssemblySupport** auf die Dateiversion von Fusion.dll fest.</span><span class="sxs-lookup"><span data-stu-id="3b189-105">On systems that support common language run-time assemblies, the installer sets the value of **MsiNetAssemblySupport** to the file version of Fusion.dll.</span></span> <span data-ttu-id="3b189-106">Diese Eigenschaft wird vom Installationsprogramm nicht festgelegt, wenn das Betriebssystem keine Common Language Run-Time-Assemblys unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b189-106">The installer does not set this property if the operating system does not support common language run-time assemblies.</span></span> <span data-ttu-id="3b189-107">Wenn mehrere Versionen von Fusion.dll nebeneinander auf dem Computer des Benutzers installiert sind, wird diese Eigenschaft auf die neueste Version der Fusion.dll Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b189-107">When multiple versions of Fusion.dll are installed side-by-side on the user's computer, this property is set to the latest version of the Fusion.dll file.</span></span> <span data-ttu-id="3b189-108">Wenn z. b. .NET Framework Version 1.0.3705 (Fusion.dll Version 1.0.3705.15) und .NET Framework Version 1.1.4322 (Fusion.dll Version 1.1.4322.314) nebeneinander installiert sind, wird die Eigenschaft **MsiNetAssemblySupport** auf 1.1.4322.314 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3b189-108">For example, if .NET Framework version 1.0.3705 (Fusion.dll version 1.0.3705.15)and .NET Framework version 1.1.4322 (Fusion.dll version 1.1.4322.314) are installed side-by-side, the **MsiNetAssemblySupport** property is set to 1.1.4322.314.</span></span> <span data-ttu-id="3b189-109">Weitere Informationen finden Sie unter [](assemblies.md)Assemblys.</span><span class="sxs-lookup"><span data-stu-id="3b189-109">For more information, see [Assemblies](assemblies.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b189-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b189-110">Requirements</span></span>



| <span data-ttu-id="3b189-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b189-111">Requirement</span></span> | <span data-ttu-id="3b189-112">Wert</span><span class="sxs-lookup"><span data-stu-id="3b189-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b189-113">Version</span><span class="sxs-lookup"><span data-stu-id="3b189-113">Version</span></span><br/> | <span data-ttu-id="3b189-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3b189-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3b189-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b189-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3b189-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="3b189-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="3b189-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="3b189-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b189-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b189-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b189-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3b189-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




