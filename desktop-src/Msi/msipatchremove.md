---
description: Die msipatchremove-Eigenschaft gibt die Liste der Patches an, die während einer Installation entfernt werden sollen.
ms.assetid: 76f8daa9-d32c-4845-85bc-52b728f53d1f
title: Msipatchremove (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf83583c5b15311e175e67a867ff5aca71394b7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352904"
---
# <a name="msipatchremove-property"></a><span data-ttu-id="b2a18-103">Msipatchremove (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b2a18-103">MSIPATCHREMOVE property</span></span>

<span data-ttu-id="b2a18-104">Die **msipatchremove** -Eigenschaft gibt die Liste der Patches an, die während einer Installation entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b2a18-104">The **MSIPATCHREMOVE** property specifies the list of patches to remove during an installation.</span></span> <span data-ttu-id="b2a18-105">Einzelne Patches in der Liste werden durch Semikolons getrennt und können durch die Patchcode-GUID oder den vollständigen Pfad zum Patch dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b2a18-105">Individual patches in the list are separated by semicolons and can be represented by patch code GUID or the full path to the patch.</span></span> <span data-ttu-id="b2a18-106">Die [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) -Funktion und die [**removepatches**](installer-removepatches.md) -Methode des [Installer](installer-object.md) -Objekts legen die **msipatchremove** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b2a18-106">The [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) function and the [**RemovePatches**](installer-removepatches.md) method of the [Installer](installer-object.md) object set the **MSIPATCHREMOVE** property.</span></span>

<span data-ttu-id="b2a18-107">Die **msipatchremove** -Eigenschaft kann wie folgt in der Befehlszeile festgelegt werden, um einen Patch zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b2a18-107">The **MSIPATCHREMOVE** property can be set on the command line as follows to remove a patch.</span></span>

<span data-ttu-id="b2a18-108">**msiexec/i A: \\Example.msi msipatchremove = c: \\ Patches \\ qfe1. msp; { 0bbb87f1-3186-409c-8cdd-c88aa2a4a7e0}; {A86B443B-E3BF-4009-ADED-F716FC735858}/QB**</span><span class="sxs-lookup"><span data-stu-id="b2a18-108">**msiexec /i A:\\Example.msi MSIPATCHREMOVE=c:\\patches\\qfe1.msp;{0BBB87F1-3186-409C-8CDD-C88AA2A4A7E0};{A86B443B-E3BF-4009-ADED-F716FC735858}/qb**</span></span>

## <a name="requirements"></a><span data-ttu-id="b2a18-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b2a18-109">Requirements</span></span>



| <span data-ttu-id="b2a18-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b2a18-110">Requirement</span></span> | <span data-ttu-id="b2a18-111">Wert</span><span class="sxs-lookup"><span data-stu-id="b2a18-111">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2a18-112">Version</span><span class="sxs-lookup"><span data-stu-id="b2a18-112">Version</span></span><br/> | <span data-ttu-id="b2a18-113">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b2a18-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b2a18-114">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b2a18-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b2a18-115">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b2a18-115">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="b2a18-116">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="b2a18-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b2a18-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2a18-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2a18-118">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b2a18-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="b2a18-119">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b2a18-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




