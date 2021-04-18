---
description: Die Eigenschaft "patchnewpackagecode" aktualisiert während des Patchens die Zusammenfassungs Eigenschaft "Revisionsnummer" eines administrativen Bilds.
ms.assetid: 5ca0058a-b4eb-48df-89eb-fbc7da7224e8
title: Patchnewpackagecode (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb7c1c70c91ede5788258c67626cdf429df74e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364796"
---
# <a name="patchnewpackagecode-property"></a><span data-ttu-id="6d6af-103">Patchnewpackagecode (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6d6af-103">PATCHNEWPACKAGECODE property</span></span>

<span data-ttu-id="6d6af-104">Die Eigenschaft " **patchnewpackagecode** " aktualisiert während des Patchens die [**Zusammenfassungs Eigenschaft "Revisionsnummer**](revision-number-summary.md) " eines administrativen Bilds.</span><span class="sxs-lookup"><span data-stu-id="6d6af-104">The **PATCHNEWPACKAGECODE** property updates the [**Revision Number Summary**](revision-number-summary.md) property of an administrative image during patching.</span></span> <span data-ttu-id="6d6af-105">Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6d6af-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="6d6af-106">Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Eigenschaften Tabelle](property-table.md) hinzufügt und deren Wert festlegt.</span><span class="sxs-lookup"><span data-stu-id="6d6af-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="6d6af-107">Das Installationsprogramm schreibt dann den Wert von " **patchnewpackagecode** " in die **Revisionsnummer-Zusammenfassungs** Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d6af-107">The installer then writes the value of **PATCHNEWPACKAGECODE** to the **Revision Number Summary** property.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d6af-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6d6af-108">Remarks</span></span>

<span data-ttu-id="6d6af-109">Die Eigenschaften " **patchnewpackagecode**", " [**patchnewsummarycomments**](patchnewsummarycomments.md)" und " [**patchnewsummarysubject**](patchnewsummarysubject.md) " werden verwendet, um die Zusammenfassungs Informationen zu aktualisieren, wenn ein Patch für ein administratives Image installiert wird.</span><span class="sxs-lookup"><span data-stu-id="6d6af-109">The **PATCHNEWPACKAGECODE**, [**PATCHNEWSUMMARYCOMMENTS**](patchnewsummarycomments.md), and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d6af-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6d6af-110">Requirements</span></span>



| <span data-ttu-id="6d6af-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6d6af-111">Requirement</span></span> | <span data-ttu-id="6d6af-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6d6af-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d6af-113">Version</span><span class="sxs-lookup"><span data-stu-id="6d6af-113">Version</span></span><br/> | <span data-ttu-id="6d6af-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="6d6af-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="6d6af-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="6d6af-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="6d6af-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="6d6af-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="6d6af-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="6d6af-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6d6af-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d6af-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d6af-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6d6af-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




