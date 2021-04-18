---
description: Der Installer legt die windowsvolume-Eigenschaft auf das Volume des Windows-Ordners fest.
ms.assetid: 56b78c88-ef58-4474-92ad-b42fe49a2f30
title: Windowsvolume-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6220a9844120e061eb680c76a32ce00dbc517f26
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371137"
---
# <a name="windowsvolume-property"></a><span data-ttu-id="b24ec-103">Windowsvolume-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b24ec-103">WindowsVolume property</span></span>

<span data-ttu-id="b24ec-104">Der Installer legt die **windowsvolume** -Eigenschaft auf das Volume des Windows-Ordners fest.</span><span class="sxs-lookup"><span data-stu-id="b24ec-104">The installer sets the **WindowsVolume** property to the volume of the windows folder.</span></span> <span data-ttu-id="b24ec-105">Die-Eigenschaft endet immer mit einem umgekehrten Schrägstrich.</span><span class="sxs-lookup"><span data-stu-id="b24ec-105">The property always ends with a backslash.</span></span> <span data-ttu-id="b24ec-106">Dies kann verwendet werden, um den Standard Speicherort auf das Volume festzulegen, auf dem sich der Windows-Ordner befindet, da die [**ROOTDRIVE**](rootdrive.md) -Eigenschaft nicht notwendigerweise mit diesem Laufwerk identisch ist.</span><span class="sxs-lookup"><span data-stu-id="b24ec-106">This can be used to set the default location to the volume the Windows folder is on because the [**ROOTDRIVE**](rootdrive.md) property does not necessarily equal this drive.</span></span>

## <a name="remarks"></a><span data-ttu-id="b24ec-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b24ec-107">Remarks</span></span>

<span data-ttu-id="b24ec-108">Verwenden Sie die **windowsvolume** -Eigenschaft nicht in der Verzeichnis-Spalte der [Verzeichnis](directory-table.md) Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b24ec-108">Do not use the **WindowsVolume** property in the Directory column of the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="b24ec-109">Die [**windowsfolder**](windowsfolder.md) -Eigenschaft enthält den Pfad zum Windows-Ordner.</span><span class="sxs-lookup"><span data-stu-id="b24ec-109">The [**WindowsFolder**](windowsfolder.md) property contains the path to the Windows folder.</span></span>

## <a name="requirements"></a><span data-ttu-id="b24ec-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b24ec-110">Requirements</span></span>



| <span data-ttu-id="b24ec-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b24ec-111">Requirement</span></span> | <span data-ttu-id="b24ec-112">Wert</span><span class="sxs-lookup"><span data-stu-id="b24ec-112">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b24ec-113">Version</span><span class="sxs-lookup"><span data-stu-id="b24ec-113">Version</span></span><br/> | <span data-ttu-id="b24ec-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b24ec-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b24ec-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b24ec-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b24ec-116">Windows Installer unter Windows Server 2003 oder Windows XP finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b24ec-116">Windows Installer on Windows Server 2003 or Windows XP See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b24ec-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b24ec-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b24ec-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b24ec-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




