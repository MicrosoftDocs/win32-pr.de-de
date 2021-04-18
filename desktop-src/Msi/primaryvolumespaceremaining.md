---
description: Das Installationsprogramm legt den Wert der Eigenschaft primaryvolumespaceremaineing auf eine Zeichenfolge fest, die die Gesamtzahl der verbleibenden Bytes auf dem Volume darstellt, auf das von der Eigenschaft primaryvolumepath verwiesen wird, wenn alle derzeit ausgewählten Funktionen installiert wurden.
ms.assetid: 8a59d22f-b8a1-47bf-90f3-f8cadfae8ecd
title: Primaryvolumespaceremaineing (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdae4e0895c18ca32ab65f68daa13cd6c702f62c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352165"
---
# <a name="primaryvolumespaceremaining-property"></a><span data-ttu-id="88115-103">Primaryvolumespaceremaineing (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="88115-103">PrimaryVolumeSpaceRemaining property</span></span>

<span data-ttu-id="88115-104">Das Installationsprogramm legt den Wert der Eigenschaft **primaryvolumespaceremaineing** auf eine Zeichenfolge fest, die die Gesamtzahl der verbleibenden Bytes auf dem Volume darstellt, auf das von der Eigenschaft [**primaryvolumepath**](primaryvolumepath.md) verwiesen wird, wenn alle derzeit ausgewählten Funktionen installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="88115-104">The installer sets the value of the **PrimaryVolumeSpaceRemaining** property to a string representing the total number of bytes remaining on the volume referenced by the [**PrimaryVolumePath**](primaryvolumepath.md) property, if all currently selected features were installed.</span></span> <span data-ttu-id="88115-105">Wie bei der [**primaryvolumespaceavailable**](primaryvolumespaceavailable.md) -Eigenschaft wird diese Zahl in Einheiten von 512 Byte angegeben.</span><span class="sxs-lookup"><span data-stu-id="88115-105">As with the [**PrimaryVolumeSpaceAvailable**](primaryvolumespaceavailable.md) property, this number is expressed in units of 512 bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="88115-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88115-106">Remarks</span></span>

<span data-ttu-id="88115-107">Hinweis Wenn dieser Wert in einem statischen [Text Steuer](text-control.md)Element angezeigt werden soll, kann das [formatsize](formatsize-control-attribute.md) -Bit verwendet werden, um diese Zahl nach Bedarf automatisch in Kilobyte oder Megabyte zu formatieren und zu bezeichnen.</span><span class="sxs-lookup"><span data-stu-id="88115-107">Note if this value is to be displayed within a static [Text control](text-control.md), the [FormatSize](formatsize-control-attribute.md) bit can be used to automatically format and label this number in units of kilobytes or megabytes as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="88115-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="88115-108">Requirements</span></span>



| <span data-ttu-id="88115-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="88115-109">Requirement</span></span> | <span data-ttu-id="88115-110">Wert</span><span class="sxs-lookup"><span data-stu-id="88115-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88115-111">Version</span><span class="sxs-lookup"><span data-stu-id="88115-111">Version</span></span><br/> | <span data-ttu-id="88115-112">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="88115-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="88115-113">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="88115-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="88115-114">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="88115-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="88115-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="88115-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88115-116">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="88115-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




