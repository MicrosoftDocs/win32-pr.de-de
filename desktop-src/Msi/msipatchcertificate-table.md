---
description: Gibt die möglichen Signatur Geber Zertifikate an, die zum digitalen Signieren von Patches verwendet werden.
ms.assetid: 8f76c27d-92f1-4de7-a69c-fba877e0325d
title: MsiPatchCertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01648e792931fd856a1231a5d876c7db843479df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042388"
---
# <a name="msipatchcertificate-table"></a><span data-ttu-id="d8720-103">MsiPatchCertificate-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d8720-103">MsiPatchCertificate Table</span></span>

<span data-ttu-id="d8720-104">Die MsiPatchCertificate-Tabelle gibt Aufschluss über die möglichen Signatur Geber Zertifikate, mit denen Patches digital signiert werden.</span><span class="sxs-lookup"><span data-stu-id="d8720-104">The MsiPatchCertificate Table identifies the possible signer certificates used to digitally sign patches.</span></span> <span data-ttu-id="d8720-105">Die MsiPatchCertificate-Tabelle enthält die Informationen, die erforderlich sind, um das [Patchen von Benutzerkontensteuerung (UAC)](user-account-control--uac--patching.md) für eine Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d8720-105">The MsiPatchCertificate Table contains the information that is needed to enable [User Account Control (UAC) Patching](user-account-control--uac--patching.md) for an application.</span></span>

<span data-ttu-id="d8720-106">Die MsiPatchCertificate-Tabelle weist die folgenden Spalten auf:</span><span class="sxs-lookup"><span data-stu-id="d8720-106">The MsiPatchCertificate Table has the following columns:</span></span>



| <span data-ttu-id="d8720-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="d8720-107">Column</span></span>               | <span data-ttu-id="d8720-108">Typ</span><span class="sxs-lookup"><span data-stu-id="d8720-108">Type</span></span>                         | <span data-ttu-id="d8720-109">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d8720-109">Key</span></span> | <span data-ttu-id="d8720-110">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="d8720-110">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="d8720-111">Patchzertifikat</span><span class="sxs-lookup"><span data-stu-id="d8720-111">PatchCertificate</span></span>     | [<span data-ttu-id="d8720-112">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d8720-112">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8720-113">J</span><span class="sxs-lookup"><span data-stu-id="d8720-113">Y</span></span>   | <span data-ttu-id="d8720-114">N</span><span class="sxs-lookup"><span data-stu-id="d8720-114">N</span></span>        |
| <span data-ttu-id="d8720-115">Digitalcertificate\_</span><span class="sxs-lookup"><span data-stu-id="d8720-115">DigitalCertificate\_</span></span> | [<span data-ttu-id="d8720-116">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="d8720-116">Identifier</span></span>](identifier.md) | <span data-ttu-id="d8720-117">N</span><span class="sxs-lookup"><span data-stu-id="d8720-117">N</span></span>   | <span data-ttu-id="d8720-118">N</span><span class="sxs-lookup"><span data-stu-id="d8720-118">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="d8720-119">Spalten</span><span class="sxs-lookup"><span data-stu-id="d8720-119">Columns</span></span>

<dl> <dt>

<span data-ttu-id="d8720-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>Patchzertifikat</span><span class="sxs-lookup"><span data-stu-id="d8720-120"><span id="PatchCertificate"></span><span id="patchcertificate"></span><span id="PATCHCERTIFICATE"></span>PatchCertificate</span></span>
</dt> <dd>

<span data-ttu-id="d8720-121">Der eindeutige Bezeichner für diese Zeile in der MsiPatchCertificate-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d8720-121">The unique identifier for this row in the MsiPatchCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="d8720-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate</span><span class="sxs-lookup"><span data-stu-id="d8720-122"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="d8720-123">Ein externer Schlüssel in die erste Spalte der [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="d8720-123">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="d8720-124">Die in der Tabelle "msidigitalcertificate" angegebene Zeile enthält die binäre Darstellung des Signatur Geber Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="d8720-124">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d8720-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8720-125">Remarks</span></span>

<span data-ttu-id="d8720-126">Patches werden immer anhand der MsiPatchCertificate-Tabelle ausgewertet, die zum Zeitpunkt der Anwendung des Patches aktuell ist.</span><span class="sxs-lookup"><span data-stu-id="d8720-126">Patches are always evaluated against the MsiPatchCertificate Table that is current at the time the patch is applied.</span></span> <span data-ttu-id="d8720-127">Ein Patch kann die MsiPatchCertificate-Tabelle ändern, indem Einträge hinzugefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="d8720-127">A patch can modify the MsiPatchCertificate Table by adding or removing entries.</span></span> <span data-ttu-id="d8720-128">Dies ermöglicht es einem Patch, die Auswertung zukünftiger Patches zu ändern, die später in der patchingsequenz angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d8720-128">This enables a patch to modify the evaluation of future patches that are applied later in the patching sequence.</span></span> <span data-ttu-id="d8720-129">In der Tabelle können mehrere Zertifikate vorhanden sein, und der Patch muss mindestens einem anzuwendenden Zertifikat entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d8720-129">Multiple certificates can exist in the table, and the patch must match at least one certificate to be applied.</span></span>

## <a name="validation"></a><span data-ttu-id="d8720-130">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="d8720-130">Validation</span></span>

<dl>

[<span data-ttu-id="d8720-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="d8720-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="d8720-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="d8720-132">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="d8720-133">ICE32</span><span class="sxs-lookup"><span data-stu-id="d8720-133">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="d8720-134">ICE81</span><span class="sxs-lookup"><span data-stu-id="d8720-134">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="d8720-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8720-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8720-136">Disableluapatching</span><span class="sxs-lookup"><span data-stu-id="d8720-136">DisableLUAPatching</span></span>](disableluapatching.md)
</dt> <dt>

[<span data-ttu-id="d8720-137">Patching der Benutzerkontensteuerung (User Account Control, UAC)</span><span class="sxs-lookup"><span data-stu-id="d8720-137">User Account Control (UAC) Patching</span></span>](user-account-control--uac--patching.md)
</dt> <dt>

[<span data-ttu-id="d8720-138">**Msidisableluapatching**</span><span class="sxs-lookup"><span data-stu-id="d8720-138">**MSIDISABLELUAPATCHING**</span></span>](msidisableluapatching.md)
</dt> <dt>

[<span data-ttu-id="d8720-139">Digitale Signaturen und Windows Installer</span><span class="sxs-lookup"><span data-stu-id="d8720-139">Digital Signatures and Windows Installer</span></span>](digital-signatures-and-windows-installer.md)
</dt> <dt>

[<span data-ttu-id="d8720-140">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d8720-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



