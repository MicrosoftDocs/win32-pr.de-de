---
description: In der Tabelle msipackagecertificate sind digitale Signatur Zertifikate aufgeführt, die zum Überprüfen der Identität der Installationspakete verwendet werden, die diese Multiple-Package der Installation machen.
ms.assetid: d3a97325-2136-4745-8a7d-57e4d6b9d27e
title: Msipackagecertificate-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd39ac93ff24da2fa8334a6e4865172471080b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218532"
---
# <a name="msipackagecertificate-table"></a><span data-ttu-id="1654a-103">Msipackagecertificate-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1654a-103">MsiPackageCertificate Table</span></span>

<span data-ttu-id="1654a-104">In der Tabelle msipackagecertificate sind digitale Signatur Zertifikate aufgeführt, mit denen die Identität der Installationspakete überprüft wird, die diese [Installation mit mehreren Paketen](multiple-package-installations.md)vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1654a-104">The MsiPackageCertificate Table lists digital signature certificates used to verify the identity of the installation packages that make this [Multiple-Package Installation](multiple-package-installations.md).</span></span>

<span data-ttu-id="1654a-105">Verwenden Sie diese Tabelle, um eine [Installation mit mehreren](multiple-package-installations.md) Paketen für ein Produkt zu erstellen, das mehrere Windows Installer Pakete enthält.</span><span class="sxs-lookup"><span data-stu-id="1654a-105">Use this table to author a [multiple-package installation](multiple-package-installations.md) for a product containing multiple Windows Installer packages.</span></span> <span data-ttu-id="1654a-106">Wenn das erste Paket digital signiert ist und eine msipackagecertificate-Tabelle enthält, die digitale Zertifikate für alle verbleibenden Pakete im Produkt angibt, muss der Administrator nur die Eingabeaufforderung für die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) akzeptieren, die für das erste Paket angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1654a-106">If the first package is digitally signed, and contains a MsiPackageCertificate Table specifying digital certificates for all the remaining packages in the product, the administrator needs only accept the [*User Account Control*](u-gly.md) (UAC) prompt displayed for the first package.</span></span> <span data-ttu-id="1654a-107">Nachdem die Eingabeaufforderung der Benutzerkontensteuerung für das erste Paket angenommen wurde, können die benutzerdefinierten Funktionen in der [Tabelle msiembeddedchainer](msiembeddedchainer-table.md) die verbleibenden Pakete in die Installation mit mehreren Paketen einbinden, ohne dass eine UAC-Eingabeaufforderung angezeigt wird und für jedes Paket eine Administrator Antwort erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1654a-107">After accepting the UAC's prompt for the first package, the user-defined functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) can then join the remaining packages to the multiple-package installation without displaying a UAC prompt and requiring an administrator response for each package.</span></span>

<span data-ttu-id="1654a-108">Wenn eine oder mehrere Funktionen in der [msiembeddedchainer-Tabelle](msiembeddedchainer-table.md) ein nicht signiertes Paket anfordern, wird für jedes nicht signierte Paket eine andere UAC-Eingabeaufforderung angezeigt, die eine Administrator Interaktion erfordert.</span><span class="sxs-lookup"><span data-stu-id="1654a-108">If one or more of the functions in the [MsiEmbeddedChainer table](msiembeddedchainer-table.md) request an unsigned package, another UAC prompt requiring administrator interaction is displayed for each unsigned package.</span></span> <span data-ttu-id="1654a-109">Wenn der Administrator diese UAC-Eingabeaufforderung annimmt, wird die Multi-Package-Installation fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1654a-109">If the administrator accepts this UAC prompt, the multi-package installation continues.</span></span> <span data-ttu-id="1654a-110">Wenn ein Administrator die Anmelde Informationen für ein Paket eingegeben hat, wird während der Installation des Multi-Pakets für das Paket keine UAC-Eingabeaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1654a-110">Once an administrator has provided credentials for a package, no UAC prompt will again be displayed for that package during this multi-package installation.</span></span> <span data-ttu-id="1654a-111">Wenn der Administrator eine UAC-Eingabeaufforderung für ein Paket ablehnt, führt Windows Installer ein Rollback der multipaketinstallation aus, bevor es einen Commit für die Installation der Pakete ausführt, die zum Produkt gehören.</span><span class="sxs-lookup"><span data-stu-id="1654a-111">If the administrator rejects a UAC prompt for a package, the Windows installer rolls back the multi-package installation before it commits to install any packages belonging to the product.</span></span>

<span data-ttu-id="1654a-112">**[Windows Installer 4,0 oder früher](not-supported-in-windows-installer-4-0.md):** Nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1654a-112">**[Windows Installer 4.0 or earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="1654a-113">Diese Tabelle ist ab Windows Installer 4,5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1654a-113">This table is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="1654a-114">Die msipackagecertificate-Tabelle weist die folgenden Spalten auf:</span><span class="sxs-lookup"><span data-stu-id="1654a-114">The MsiPackageCertificate Table has the following columns:</span></span>



| <span data-ttu-id="1654a-115">Spalte</span><span class="sxs-lookup"><span data-stu-id="1654a-115">Column</span></span>               | <span data-ttu-id="1654a-116">Typ</span><span class="sxs-lookup"><span data-stu-id="1654a-116">Type</span></span>                         | <span data-ttu-id="1654a-117">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="1654a-117">Key</span></span> | <span data-ttu-id="1654a-118">Nullwerte zulässig</span><span class="sxs-lookup"><span data-stu-id="1654a-118">Nullable</span></span> |
|----------------------|------------------------------|-----|----------|
| <span data-ttu-id="1654a-119">Packagecertificate</span><span class="sxs-lookup"><span data-stu-id="1654a-119">PackageCertificate</span></span>   | [<span data-ttu-id="1654a-120">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1654a-120">Identifier</span></span>](identifier.md) | <span data-ttu-id="1654a-121">J</span><span class="sxs-lookup"><span data-stu-id="1654a-121">Y</span></span>   | <span data-ttu-id="1654a-122">N</span><span class="sxs-lookup"><span data-stu-id="1654a-122">N</span></span>        |
| <span data-ttu-id="1654a-123">Digitalcertificate\_</span><span class="sxs-lookup"><span data-stu-id="1654a-123">DigitalCertificate\_</span></span> | [<span data-ttu-id="1654a-124">Bezeichner</span><span class="sxs-lookup"><span data-stu-id="1654a-124">Identifier</span></span>](identifier.md) | <span data-ttu-id="1654a-125">N</span><span class="sxs-lookup"><span data-stu-id="1654a-125">N</span></span>   | <span data-ttu-id="1654a-126">N</span><span class="sxs-lookup"><span data-stu-id="1654a-126">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="1654a-127">Spalten</span><span class="sxs-lookup"><span data-stu-id="1654a-127">Columns</span></span>

<dl> <dt>

<span data-ttu-id="1654a-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>Packagecertificate</span><span class="sxs-lookup"><span data-stu-id="1654a-128"><span id="PackageCertificate"></span><span id="packagecertificate"></span><span id="PACKAGECERTIFICATE"></span>PackageCertificate</span></span>
</dt> <dd>

<span data-ttu-id="1654a-129">Der eindeutige Bezeichner für diese Zeile in der msipackagecertificate-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1654a-129">The unique identifier for this row in the MsiPackageCertificate Table.</span></span>

</dd> <dt>

<span data-ttu-id="1654a-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>Digitalcertificate</span><span class="sxs-lookup"><span data-stu-id="1654a-130"><span id="DigitalCertificate"></span><span id="digitalcertificate"></span><span id="DIGITALCERTIFICATE"></span>DigitalCertificate</span></span>
</dt> <dd>

<span data-ttu-id="1654a-131">Ein externer Schlüssel in die erste Spalte der [msidigitalcertificate-Tabelle](msidigitalcertificate-table.md).</span><span class="sxs-lookup"><span data-stu-id="1654a-131">An external key into the first column of the [MsiDigitalCertificate Table](msidigitalcertificate-table.md).</span></span> <span data-ttu-id="1654a-132">Die in der Tabelle "msidigitalcertificate" angegebene Zeile enthält die binäre Darstellung des Signatur Geber Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="1654a-132">The row indicated in the MsiDigitalCertificate Table contains the binary representation of the signer certificate.</span></span>

</dd> </dl>

## <a name="validation"></a><span data-ttu-id="1654a-133">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="1654a-133">Validation</span></span>

<dl>

[<span data-ttu-id="1654a-134">ICE39</span><span class="sxs-lookup"><span data-stu-id="1654a-134">ICE39</span></span>](ice39.md)  
[<span data-ttu-id="1654a-135">ICE81</span><span class="sxs-lookup"><span data-stu-id="1654a-135">ICE81</span></span>](ice81.md)  
</dl>

## <a name="related-topics"></a><span data-ttu-id="1654a-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1654a-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1654a-137">Msiembeddecodchainer</span><span class="sxs-lookup"><span data-stu-id="1654a-137">MsiEmbeddedChainer</span></span>](msiembeddedchainer-table.md)
</dt> <dt>

[<span data-ttu-id="1654a-138">Msidigitalcertificate-Tabelle</span><span class="sxs-lookup"><span data-stu-id="1654a-138">MsiDigitalCertificate Table</span></span>](msidigitalcertificate-table.md)
</dt> </dl>

 

 



