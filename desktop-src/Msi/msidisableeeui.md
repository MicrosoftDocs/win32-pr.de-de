---
description: Um die eingebettete Benutzeroberfläche für die in der msiembeddedui-Tabelle definierte Installation zu deaktivieren, legen Sie die msidisableeeui-Eigenschaft in der Befehlszeile auf 1 fest.
ms.assetid: c5ada690-c5dd-455f-babe-8c09750525c4
title: Msidisableeeui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d89ce43f649d406e4ae086db236375c02c43e2d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361310"
---
# <a name="msidisableeeui-property"></a><span data-ttu-id="efb49-103">Msidisableeeui (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="efb49-103">MSIDISABLEEEUI property</span></span>

<span data-ttu-id="efb49-104">Um die eingebettete Benutzeroberfläche für die in der [msiembeddedui-Tabelle](msiembeddedui-table.md)definierte Installation zu deaktivieren, legen Sie die msidisableeeui-Eigenschaft in der Befehlszeile auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="efb49-104">To disable the embedded user interface for the installation defined in the [MsiEmbeddedUI table](msiembeddedui-table.md), set the MSIDISABLEEEUI property to 1 on the command line.</span></span>

<span data-ttu-id="efb49-105">**[Windows Installer 4,0 und früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="efb49-105">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="efb49-106">In früheren Versionen als Windows Installer 4,5 wird die msidisableeeui-Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="efb49-106">Versions earlier than Windows Installer 4.5 ignore the MSIDISABLEEEUI Property.</span></span>

## <a name="remarks"></a><span data-ttu-id="efb49-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="efb49-107">Remarks</span></span>

<span data-ttu-id="efb49-108">Bei einer Installation mit mehreren Paketen sollte ein untergeordnetes Paket in der Regel die Benutzeroberfläche des übergeordneten Pakets verwenden und seine eigene eingebettete Benutzeroberfläche nicht initialisieren.</span><span class="sxs-lookup"><span data-stu-id="efb49-108">In a multiple-package installation, a child package should typically use the user interface of the parent package and not initialize its own embedded UI.</span></span> <span data-ttu-id="efb49-109">Wenn die msidisableeeui-Eigenschaft nicht innerhalb des übergeordneten Pakets festgelegt wird, verwendet das untergeordnete Paket standardmäßig die eingebettete Benutzeroberfläche des übergeordneten Pakets und ignoriert die msidisableeeui-Eigenschaft innerhalb des untergeordneten Pakets.</span><span class="sxs-lookup"><span data-stu-id="efb49-109">If the MSIDISABLEEEUI property is not set inside the parent package, the child package uses the embedded UI of the parent package by default and ignores the MSIDISABLEEEUI property within the child package.</span></span>

<span data-ttu-id="efb49-110">Die msidisableeeui-Eigenschaft deaktiviert die eingebettete Benutzeroberfläche für ein einzelnes Paket.</span><span class="sxs-lookup"><span data-stu-id="efb49-110">The MSIDISABLEEEUI property disables the embedded user interface for a single package.</span></span> <span data-ttu-id="efb49-111">Sie können die Richtlinie " [msidisableembeddedui](msidisableembeddedui.md) " verwenden, um eingebettete Benutzeroberflächen für alle Pakete auf dem Computer zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="efb49-111">You can use the [MsiDisableEmbeddedUI](msidisableembeddedui.md) policy to disable embedded user interfaces for all packages on the computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="efb49-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="efb49-112">Requirements</span></span>



| <span data-ttu-id="efb49-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="efb49-113">Requirement</span></span> | <span data-ttu-id="efb49-114">Wert</span><span class="sxs-lookup"><span data-stu-id="efb49-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efb49-115">Version</span><span class="sxs-lookup"><span data-stu-id="efb49-115">Version</span></span><br/> | <span data-ttu-id="efb49-116">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="efb49-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="efb49-117">Windows Installer 4,5 unter Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="efb49-117">Windows Installer 4.5 on Windows Server 2008, Windows Vista, Windows Server 2003, and Windows XP.</span></span> <span data-ttu-id="efb49-118">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="efb49-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="efb49-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efb49-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efb49-120">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="efb49-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




