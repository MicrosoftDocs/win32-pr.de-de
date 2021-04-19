---
description: Der Installer legt den Wert der Eigenschaft msisystemrebootpending auf 1 fest, wenn ein Vorgang aussteht, um eine Datei umzubenennen.
ms.assetid: 8bbbf42e-fb55-4e5d-a574-2c3aaa87a73a
title: Msisystemrebootpending (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec5db7550be3fa27b0ed272ff08d88a4cad915a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367709"
---
# <a name="msisystemrebootpending-property"></a><span data-ttu-id="68484-103">Msisystemrebootpending (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="68484-103">MsiSystemRebootPending property</span></span>

<span data-ttu-id="68484-104">Der Installer legt den Wert der Eigenschaft **msisystemrebootpending** auf 1 fest, wenn ein Vorgang aussteht, um eine Datei umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="68484-104">The installer sets the value of the **MsiSystemRebootPending** property to 1 if there is an operation pending to rename a file.</span></span>

<span data-ttu-id="68484-105">Paket Autoren können eine Bedingung in der [LaunchCondition-Tabelle](launchcondition-table.md) für diese Eigenschaft basieren, um die Installation des Pakets zu verhindern, wenn ein Vorgang aussteht, um eine Datei umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="68484-105">Package authors can base a condition in the [LaunchCondition table](launchcondition-table.md) on this property to prevent the installation of their package in cases where there is an operation pending to rename a file.</span></span> <span data-ttu-id="68484-106">Dies kann durchgeführt werden, um einen Neustart des Betriebssystems zu verhindern, das durch das Umbenennen der Datei verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="68484-106">This may be done to prevent a restart of the operating system caused by the renaming of the file.</span></span> <span data-ttu-id="68484-107">Der Installer legt die **msisystemrebootpending** -Eigenschaft nicht in allen Fällen fest, für die ein Neustart des Systems erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="68484-107">The installer does not set the **MsiSystemRebootPending** property in all cases that require a restart of the system.</span></span>

## <a name="requirements"></a><span data-ttu-id="68484-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="68484-108">Requirements</span></span>



| <span data-ttu-id="68484-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="68484-109">Requirement</span></span> | <span data-ttu-id="68484-110">Wert</span><span class="sxs-lookup"><span data-stu-id="68484-110">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68484-111">Version</span><span class="sxs-lookup"><span data-stu-id="68484-111">Version</span></span><br/> | <span data-ttu-id="68484-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="68484-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="68484-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="68484-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="68484-114">Windows Installer 4,5 unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="68484-114">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="68484-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="68484-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="68484-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68484-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68484-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="68484-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="68484-118">System Neustarts</span><span class="sxs-lookup"><span data-stu-id="68484-118">System Reboots</span></span>](system-reboots.md)
</dt> <dt>

[<span data-ttu-id="68484-119">Wird in Windows Installer 3,1 und früheren Versionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="68484-119">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




