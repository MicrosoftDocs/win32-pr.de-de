---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespaceavailable auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der Eigenschaft primaryvolumepath verwiesen wird.
ms.assetid: fff546d5-d26c-48cf-8d00-595a23c0a2af
title: Primaryvolumespaceavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d464626b68f9d8ccb32ceb08c52af0cf7efa5920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364695"
---
# <a name="primaryvolumespaceavailable-property"></a><span data-ttu-id="79934-103">Primaryvolumespaceavailable (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="79934-103">PrimaryVolumeSpaceAvailable property</span></span>

<span data-ttu-id="79934-104">Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespaceavailable** auf eine Zeichenfolge fest, die die Gesamtzahl der verfügbaren Bytes in Einheiten von 512 auf dem Volume darstellt, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="79934-104">The installer sets the value of the **PrimaryVolumeSpaceAvailable** property to a string that represents the total number of bytes available, in units of 512, on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="79934-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79934-105">Remarks</span></span>

<span data-ttu-id="79934-106">Wenn [**primaryvolumepath**](primaryvolumepath.md) z. b. auf "D:" festgelegt ist und Volume D: 446.134.272 Bytes frei ist, wird **primaryvolumespaceavailable** auf 871356 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="79934-106">For example, if [**PrimaryVolumePath**](primaryvolumepath.md) is set to "D:", and volume D: has 446,134,272 bytes free, **PrimaryVolumeSpaceAvailable** is set to 871356.</span></span>

<span data-ttu-id="79934-107">Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="79934-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="79934-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79934-108">Requirements</span></span>



| <span data-ttu-id="79934-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79934-109">Requirement</span></span> | <span data-ttu-id="79934-110">Wert</span><span class="sxs-lookup"><span data-stu-id="79934-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79934-111">Version</span><span class="sxs-lookup"><span data-stu-id="79934-111">Version</span></span><br/> | <span data-ttu-id="79934-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79934-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="79934-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="79934-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="79934-114">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="79934-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="79934-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="79934-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="79934-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79934-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79934-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="79934-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




