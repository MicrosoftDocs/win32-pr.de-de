---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespacerequired auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Funktionen auf dem Volume erforderlich sind, auf das von der Eigenschaft primaryvolumepath verwiesen wird.
ms.assetid: 44c89bd8-774a-4b4f-9608-9a1926ef3b7d
title: Primaryvolumespacerequired (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ae1b210e57ee054191d908e4962c7568f0c6acf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364494"
---
# <a name="primaryvolumespacerequired-property"></a><span data-ttu-id="c3f22-103">Primaryvolumespacerequired (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="c3f22-103">PrimaryVolumeSpaceRequired property</span></span>

<span data-ttu-id="c3f22-104">Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespacerequired** auf eine Zeichenfolge fest, die die Gesamtzahl der Bytes darstellt, die für alle ausgewählten Funktionen auf dem Volume erforderlich sind, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c3f22-104">The installer sets the value of the **PrimaryVolumeSpaceRequired** property to a string representing the total number of bytes required by all selected features on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property.</span></span> <span data-ttu-id="c3f22-105">Wie bei der [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) -Eigenschaft wird diese Zahl in Einheiten von 512 Byte angegeben.</span><span class="sxs-lookup"><span data-stu-id="c3f22-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f22-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c3f22-106">Remarks</span></span>

<span data-ttu-id="c3f22-107">Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="c3f22-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f22-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c3f22-108">Requirements</span></span>



| <span data-ttu-id="c3f22-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c3f22-109">Requirement</span></span> | <span data-ttu-id="c3f22-110">Wert</span><span class="sxs-lookup"><span data-stu-id="c3f22-110">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f22-111">Version</span><span class="sxs-lookup"><span data-stu-id="c3f22-111">Version</span></span><br/> | <span data-ttu-id="c3f22-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c3f22-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c3f22-113">Windows Installer 4,0 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c3f22-113">Windows Installer 4.0 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c3f22-114">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="c3f22-114">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="c3f22-115">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f22-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c3f22-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3f22-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f22-117">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c3f22-117">Properties</span></span>](properties.md)
</dt> </dl>

 

 




