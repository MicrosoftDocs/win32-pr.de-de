---
description: Bei einem Installationspaket enthält die Zusammenfassungs Eigenschaft Revisionsnummer den Paket Code für das Installer-Paket.
ms.assetid: 79702b44-846a-4672-8e22-9b6e3f4b4678
title: Zusammenfassungs Eigenschaft der Revisionsnummer
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e97df1eafec2d543be0f975b9f5daca7728267b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361461"
---
# <a name="revision-number-summary-property"></a><span data-ttu-id="e518e-103">Zusammenfassungs Eigenschaft der Revisionsnummer</span><span class="sxs-lookup"><span data-stu-id="e518e-103">Revision Number Summary property</span></span>

<span data-ttu-id="e518e-104">Bei einem Installationspaket enthält die **Zusammenfassungs Eigenschaft Revisionsnummer** den [*Paket Code*](p-gly.md) für das Installer-Paket.</span><span class="sxs-lookup"><span data-stu-id="e518e-104">For an installation package, the **Revision Number Summary** property contains the [*package code*](p-gly.md) for the installer package.</span></span> <span data-ttu-id="e518e-105">Weitere Informationen zu Paket Codes finden Sie unter [Paket Codes](package-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e518e-105">For more information about package codes, see [Package Codes](package-codes.md).</span></span>

<span data-ttu-id="e518e-106">Bei einer Transformation werden in der **Zusammenfassungs Eigenschaft Revisionsnummer** die Produktcode-GUIDs und die Version der neuen und ursprünglichen Produkte sowie die UpgradeCode-GUID aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e518e-106">For a transform, the **Revision Number Summary** property lists the product code GUIDs and version of the new and original products and the upgrade code GUID.</span></span> <span data-ttu-id="e518e-107">Die Liste wird wie folgt durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="e518e-107">The list is separated with semicolons as follows.</span></span>

<span data-ttu-id="e518e-108">"Original-Product-Code Original-Product-Version; New-Product Code New-Product-Version; UpgradeCode "</span><span class="sxs-lookup"><span data-stu-id="e518e-108">"Original-Product-Code Original-Product-Version ; New-Product Code New-Product-Version; Upgrade-Code"</span></span>

<span data-ttu-id="e518e-109">Bei einem Patchpaket gibt die **Zusammenfassungs Eigenschaft der Revisionsnummer** den GUID-Patchcode für den Patch an.</span><span class="sxs-lookup"><span data-stu-id="e518e-109">For a patch package, the **Revision Number Summary** property specifies the GUID patch code for the patch.</span></span> <span data-ttu-id="e518e-110">Auf diese Weise kann eine Liste von Patchcode-GUIDs für veraltete Patches folgen, die entfernt werden sollen, wenn dieser Patch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e518e-110">This can be followed by a list of patch code GUIDs for obsolete patches that are to be removed when this patch is applied.</span></span> <span data-ttu-id="e518e-111">Die Patchcodes werden ohne Trennzeichen verkettet, in denen GUIDs in der Liste getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e518e-111">The patch codes are concatenated with no delimiters separating GUIDs in the list.</span></span>

<span data-ttu-id="e518e-112">\* \* Windows Installer 3,0: \* \* Wenn in der [msipatchsequence-Tabelle](msipatchsequence-table.md)Sequenzierungs Informationen vorhanden sind, verwendet Windows Installer 3,0 die Sequenzierungs Informationen in der Tabelle und ignoriert die Liste veralteter Patches, die in der **Revisionsnummer-Zusammenfassungs** Eigenschaft enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e518e-112">\*\*Windows Installer 3.0:  \*\* If there is sequencing information present in the [MsiPatchSequence table](msipatchsequence-table.md), Windows Installer 3.0 uses the sequencing information in the table and ignores the list of obsolete patches included in the **Revision Number Summary** property.</span></span> <span data-ttu-id="e518e-113">In Windows Installer 3,0 können weiterhin die veralteten Patchinformationen in der **Revisionsnummer-Zusammenfassungs** Eigenschaft verwendet werden, wenn das Paket keine msipatchsequence-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="e518e-113">Windows Installer 3.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="e518e-114">\* \* Windows Installer 2,0: \* \* die [msipatchsequence-Tabelle](msipatchsequence-table.md) wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e518e-114">\*\*Windows Installer 2.0:  \*\* The [MsiPatchSequence table](msipatchsequence-table.md) is not supported.</span></span> <span data-ttu-id="e518e-115">In Windows Installer 2,0 können weiterhin die veralteten Patchinformationen in der **Revisionsnummer-Zusammenfassungs** Eigenschaft verwendet werden, wenn das Paket keine msipatchsequence-Tabelle enthält.</span><span class="sxs-lookup"><span data-stu-id="e518e-115">Windows Installer 2.0 can still use the obsolete patch information in the **Revision Number Summary** property if the package does not contain a MsiPatchSequence table.</span></span>

<span data-ttu-id="e518e-116">Diese Zusammenfassungs Eigenschaft ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e518e-116">This summary property is required.</span></span>

## <a name="requirements"></a><span data-ttu-id="e518e-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e518e-117">Requirements</span></span>



| <span data-ttu-id="e518e-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e518e-118">Requirement</span></span> | <span data-ttu-id="e518e-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e518e-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e518e-120">Version</span><span class="sxs-lookup"><span data-stu-id="e518e-120">Version</span></span><br/> | <span data-ttu-id="e518e-121">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e518e-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e518e-122">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e518e-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e518e-123">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="e518e-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e518e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e518e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e518e-125">Beschreibungen der Zusammenfassungs Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e518e-125">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




