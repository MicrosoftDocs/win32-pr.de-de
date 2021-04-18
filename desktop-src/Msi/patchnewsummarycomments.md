---
description: Die patchnewsummarycomments-Eigenschaft aktualisiert während des Patchens die Eigenschaft für die Kommentar Zusammenfassung einer administrativen Installation.
ms.assetid: 555813d8-6cb2-4b93-aa01-32d30b75b3d5
title: Patchnewsummarycomments (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbe2bff9613fa5d39ae300e15c3ee816c5c6fce5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351223"
---
# <a name="patchnewsummarycomments-property"></a><span data-ttu-id="f690b-103">Patchnewsummarycomments (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f690b-103">PATCHNEWSUMMARYCOMMENTS property</span></span>

<span data-ttu-id="f690b-104">Die **patchnewsummarycomments** -Eigenschaft aktualisiert während des Patchens die Eigenschaft für die [**Kommentar Zusammenfassung**](comments-summary.md) einer administrativen Installation.</span><span class="sxs-lookup"><span data-stu-id="f690b-104">The **PATCHNEWSUMMARYCOMMENTS** property updates the [**Comments Summary**](comments-summary.md) property of an administrative installation during patching.</span></span> <span data-ttu-id="f690b-105">Diese Eigenschaft wird nur durch eine Transformation in einer MSP-Datei festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f690b-105">This property is only set by a transform in a .msp file.</span></span> <span data-ttu-id="f690b-106">Die MSP-Datei muss eine Transformation enthalten, die diese Eigenschaft der [Eigenschaften Tabelle](property-table.md) hinzufügt und deren Wert festlegt.</span><span class="sxs-lookup"><span data-stu-id="f690b-106">The .msp file must include a transform that adds this property to the [Property table](property-table.md) and sets its value.</span></span> <span data-ttu-id="f690b-107">Das Installationsprogramm schreibt dann den Wert von " **patchnewsummarycomments** " in die Eigenschaft " [**Revisionsnummer-Zusammenfassung**](revision-number-summary.md) ".</span><span class="sxs-lookup"><span data-stu-id="f690b-107">The installer then writes the value of **PATCHNEWSUMMARYCOMMENTS** to the [**Revision Number Summary**](revision-number-summary.md) property.</span></span>

## <a name="remarks"></a><span data-ttu-id="f690b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f690b-108">Remarks</span></span>

<span data-ttu-id="f690b-109">Die Eigenschaften " [**patchnewpackagecode**](patchnewpackagecode.md)", " **patchnewsummarycomments**" und " [**patchnewsummarysubject**](patchnewsummarysubject.md) " werden verwendet, um die Zusammenfassungs Informationen zu aktualisieren, wenn ein Patch für ein administratives Image installiert wird.</span><span class="sxs-lookup"><span data-stu-id="f690b-109">The [**PATCHNEWPACKAGECODE**](patchnewpackagecode.md), **PATCHNEWSUMMARYCOMMENTS**, and [**PATCHNEWSUMMARYSUBJECT**](patchnewsummarysubject.md) properties are used to update the summary information when a patch is installed to an administrative image.</span></span>

## <a name="requirements"></a><span data-ttu-id="f690b-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f690b-110">Requirements</span></span>



| <span data-ttu-id="f690b-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f690b-111">Requirement</span></span> | <span data-ttu-id="f690b-112">Wert</span><span class="sxs-lookup"><span data-stu-id="f690b-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f690b-113">Version</span><span class="sxs-lookup"><span data-stu-id="f690b-113">Version</span></span><br/> | <span data-ttu-id="f690b-114">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="f690b-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="f690b-115">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="f690b-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="f690b-116">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="f690b-116">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="f690b-117">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="f690b-117">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f690b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f690b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f690b-119">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f690b-119">Properties</span></span>](properties.md)
</dt> </dl>

 

 




