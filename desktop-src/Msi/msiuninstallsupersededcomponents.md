---
description: Legen Sie in der Eigenschaften Tabelle oder in einer Befehlszeile die msiuninstallablösung dedcomponents-Eigenschaft auf 1 fest.
ms.assetid: ba9b1b2d-1667-48c8-8f1a-9958a1d170da
title: Msiuninstallablösung dedcomponents (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcc930a258d8faebe71480f466f2b097fe1eda68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370252"
---
# <a name="msiuninstallsupersededcomponents-property"></a><span data-ttu-id="b7d04-103">Msiuninstallablösung dedcomponents (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b7d04-103">MSIUNINSTALLSUPERSEDEDCOMPONENTS property</span></span>

<span data-ttu-id="b7d04-104">Legen Sie in der [Eigenschaften Tabelle](property-table.md) oder in einer Befehlszeile die **msiuninstallablösung dedcomponents** -Eigenschaft auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="b7d04-104">Set the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** property to 1 in the [Property table](property-table.md) or on a command line.</span></span> <span data-ttu-id="b7d04-105">Wenn diese Eigenschaft auf 1 festgelegt wurde, ermittelt das Installationsprogramm, ob die Komponenten in abgelösten Patches zu redundant werden.</span><span class="sxs-lookup"><span data-stu-id="b7d04-105">When this property has been set to 1, the installer determines whether the components in any superseded patches are becoming redundant.</span></span> <span data-ttu-id="b7d04-106">Das Installationsprogramm kann die Registrierung von redundanten Komponenten aufheben und deinstallieren, um zu verhindern, dass verwaiste Komponenten auf dem Computer bleiben</span><span class="sxs-lookup"><span data-stu-id="b7d04-106">The installer can unregister and uninstall redundant components to prevent leaving behind orphan components on the computer.</span></span>

<span data-ttu-id="b7d04-107">Das Festlegen dieser Eigenschaft wirkt sich auf die Komponenten in allen Patches aus, die abgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="b7d04-107">Setting this property affects the components in all patches being superseded.</span></span> <span data-ttu-id="b7d04-108">Um diese Funktionalität für einzelne Komponenten zu aktivieren, verwenden Sie das **msidbcomponentattributesuninstallonabgelöst** -Attribut in der [Component-Tabelle](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="b7d04-108">To enable this functionality for single components, use the **msidbComponentAttributesUninstallOnSupersedence** attribute in the [Component table](component-table.md).</span></span>

<span data-ttu-id="b7d04-109">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7d04-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="b7d04-110">In früheren Versionen als Windows Installer 4,5 wird die **msiuninstallablösen** -Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b7d04-110">Versions earlier than Windows Installer 4.5 ignore the **MSIUNINSTALLSUPERSEDEDCOMPONENTS** Property.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7d04-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7d04-111">Requirements</span></span>



| <span data-ttu-id="b7d04-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7d04-112">Requirement</span></span> | <span data-ttu-id="b7d04-113">Wert</span><span class="sxs-lookup"><span data-stu-id="b7d04-113">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d04-114">Version</span><span class="sxs-lookup"><span data-stu-id="b7d04-114">Version</span></span><br/> | <span data-ttu-id="b7d04-115">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b7d04-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b7d04-116">Windows Installer 4,5 oder Windows Installer 4,5 unter Windows Vista, Windows XP, Windows Server 2003 und Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b7d04-116">Windows Installer 4.5 or Windows Installer 4.5 on Windows Vista, Windows XP, Windows Server 2003, and Windows Server 2008.</span></span> <span data-ttu-id="b7d04-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b7d04-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b7d04-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7d04-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7d04-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b7d04-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




