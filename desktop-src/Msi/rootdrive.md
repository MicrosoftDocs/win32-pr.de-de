---
description: Die ROOTDRIVE-Eigenschaft gibt das Standard Laufwerk für das Zielverzeichnis der Installation an.
ms.assetid: 9f36dc2a-2fb5-4787-a630-c7cc93ef51ec
title: ROOTDRIVE (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e16f64b50105727d307867b5ed2910aed042cd28
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372308"
---
# <a name="rootdrive-property"></a><span data-ttu-id="d04ae-103">ROOTDRIVE (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d04ae-103">ROOTDRIVE property</span></span>

<span data-ttu-id="d04ae-104">Die **ROOTDRIVE** -Eigenschaft gibt das Standard Laufwerk für das Zielverzeichnis der Installation an.</span><span class="sxs-lookup"><span data-stu-id="d04ae-104">The **ROOTDRIVE** property specifies the default drive for the destination directory of the installation.</span></span> <span data-ttu-id="d04ae-105">Wenn in der Verzeichnis-Spalte der [Verzeichnis Tabelle](directory-table.md) das Stammverzeichnis durch einen nicht definierten Eigenschaftsnamen angegeben ist, verwendet das Installationsprogramm den Wert der **ROOTDRIVE** -Eigenschaft, um den Pfad zum Zielverzeichnis aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="d04ae-105">If the Directory column of the [Directory table](directory-table.md) indicates the root destination directory by a property name that is undefined, the installer uses the value of the **ROOTDRIVE** property to resolve the path to the destination directory.</span></span>

<span data-ttu-id="d04ae-106">Wenn **ROOTDRIVE** nicht in einer Befehlszeile festgelegt oder in der [Eigenschaften Tabelle](property-table.md)erstellt wurde, legt das Installationsprogramm diese Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="d04ae-106">If **ROOTDRIVE** is not set at a command line or authored into the [Property table](property-table.md), the installer sets this property.</span></span> <span data-ttu-id="d04ae-107">Während einer [administrativen Installation](administrative-installation.md) legt das Installationsprogramm **ROOTDRIVE** auf das erste gefundene Netzwerklaufwerk fest, in das geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d04ae-107">During an [administrative installation](administrative-installation.md) the installer sets **ROOTDRIVE** to the first connected network drive it finds that can be written to.</span></span> <span data-ttu-id="d04ae-108">Wenn es sich nicht um eine administrative Installation handelt, oder wenn das Installationsprogramm keine Netzwerklaufwerke finden kann, legt das Installationsprogramm **ROOTDRIVE** auf das lokale Laufwerk fest, das mit dem meisten freien Speicherplatz geschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="d04ae-108">If it is not an administrative installation, or if the installer can find no network drives, the installer sets **ROOTDRIVE** to the local drive that can be written to having the most free space.</span></span>

<span data-ttu-id="d04ae-109">Der Wert für diese Eigenschaft muss auf " \\ " enden.</span><span class="sxs-lookup"><span data-stu-id="d04ae-109">The value for this property must end with '\\'.</span></span>

## <a name="requirements"></a><span data-ttu-id="d04ae-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d04ae-110">Requirements</span></span>



| <span data-ttu-id="d04ae-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d04ae-111">Requirement</span></span> | <span data-ttu-id="d04ae-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d04ae-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d04ae-113">Version</span><span class="sxs-lookup"><span data-stu-id="d04ae-113">Version</span></span><br/> | <span data-ttu-id="d04ae-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d04ae-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d04ae-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d04ae-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d04ae-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="d04ae-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d04ae-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="d04ae-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d04ae-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d04ae-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d04ae-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="d04ae-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




