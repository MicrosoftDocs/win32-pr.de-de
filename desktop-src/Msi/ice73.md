---
description: ICE73 überprüft, ob Paket Codes, upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele von Ihrem Paket nicht wieder verwendet werden. Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts niemals wieder verwenden.
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac0e192f7c2ab7fb6f6236e45e0e4da70157e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347826"
---
# <a name="ice73"></a><span data-ttu-id="035d1-104">ICE73</span><span class="sxs-lookup"><span data-stu-id="035d1-104">ICE73</span></span>

<span data-ttu-id="035d1-105">ICE73 überprüft, ob Paket Codes, upgradecodes oder Produktcodes der Windows Installer SDK-Beispiele von Ihrem Paket nicht wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="035d1-105">ICE73 verifies that your package does not reuse package codes, upgrade codes, or product codes of the Windows Installer SDK samples.</span></span> <span data-ttu-id="035d1-106">Pakete sollten das Paket, das Upgrade oder die Produktcodes eines anderen Produkts niemals wieder verwenden.</span><span class="sxs-lookup"><span data-stu-id="035d1-106">Packages should never reuse the package, upgrade, or product codes of another product.</span></span>

## <a name="result"></a><span data-ttu-id="035d1-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="035d1-107">Result</span></span>

<span data-ttu-id="035d1-108">ICE73 gibt eine Warnung aus, wenn das Paket des Produkts ein Paket oder einen Produktcode eines Windows Installer SDK-Beispiels erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="035d1-108">ICE73 outputs a warning if your product's package reuses a package or product code of a Windows Installer SDK sample.</span></span>

## <a name="example"></a><span data-ttu-id="035d1-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="035d1-109">Example</span></span>

<span data-ttu-id="035d1-110">ICE73 meldet die folgenden Fehler für das gezeigte Beispiel:</span><span class="sxs-lookup"><span data-stu-id="035d1-110">ICE73 reports the following errors for the example shown:</span></span>

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> <span data-ttu-id="035d1-111">Die Sternchen ( \* \* \* \* ) in der GUID stellen den Bereich von GUIDs dar, der für nachfolgende Windows Installer SDK-Pakete reserviert ist.</span><span class="sxs-lookup"><span data-stu-id="035d1-111">The asterisks (\*\*\*\*) in the GUID represent the range of GUIDs reserved for subsequent Windows Installer SDK packages.</span></span>

 

<span data-ttu-id="035d1-112">Um die Fehler zu beheben, generieren Sie eine neue eindeutige GUID für das Produkt und die Paket Codes Ihres Pakets.</span><span class="sxs-lookup"><span data-stu-id="035d1-112">To fix the errors, generate a new unique GUID for your package's product and package codes.</span></span> <span data-ttu-id="035d1-113">Außerdem benötigen Sie eine neue eindeutige GUID für den UpgradeCode des Pakets.</span><span class="sxs-lookup"><span data-stu-id="035d1-113">You will also need a new unique GUID for your package's upgrade code.</span></span>

<span data-ttu-id="035d1-114">[Zusammenfassungs Informationsdaten Strom](summary-information-stream.md) (teilweise)</span><span class="sxs-lookup"><span data-stu-id="035d1-114">[Summary Information Stream](summary-information-stream.md) (partial)</span></span>



| <span data-ttu-id="035d1-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="035d1-115">Property</span></span>       | <span data-ttu-id="035d1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="035d1-116">Value</span></span>                                  |
|----------------|----------------------------------------|
| <span data-ttu-id="035d1-117">PID- \_ revnumber</span><span class="sxs-lookup"><span data-stu-id="035d1-117">PID\_REVNUMBER</span></span> | <span data-ttu-id="035d1-118">{000c1101-0000-0000-C000-000000000047}</span><span class="sxs-lookup"><span data-stu-id="035d1-118">{000C1101-0000-0000-C000-000000000047}</span></span> |



 

<span data-ttu-id="035d1-119">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="035d1-119">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="035d1-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="035d1-120">Property</span></span>                           | <span data-ttu-id="035d1-121">Wert</span><span class="sxs-lookup"><span data-stu-id="035d1-121">Value</span></span>                                  |
|------------------------------------|----------------------------------------|
| [<span data-ttu-id="035d1-122">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="035d1-122">**ProductCode**</span></span>](productcode.md) | <span data-ttu-id="035d1-123">{80F 030-a751-11d2-A7D4-006097c99860}</span><span class="sxs-lookup"><span data-stu-id="035d1-123">{80F7E030-A751-11D2-A7D4-006097C99860}</span></span> |
| [<span data-ttu-id="035d1-124">**UpgradeCode auch**</span><span class="sxs-lookup"><span data-stu-id="035d1-124">**UpgradeCode**</span></span>](upgradecode.md) | <span data-ttu-id="035d1-125">{8fc70000-88a0-4b41-82b8-8905d4aa904c}</span><span class="sxs-lookup"><span data-stu-id="035d1-125">{8FC70000-88A0-4b41-82B8-8905D4AA904C}</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="035d1-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="035d1-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="035d1-127">Paket Codes</span><span class="sxs-lookup"><span data-stu-id="035d1-127">Package Codes</span></span>](package-codes.md)
</dt> <dt>

[<span data-ttu-id="035d1-128">Produkt Codes</span><span class="sxs-lookup"><span data-stu-id="035d1-128">Product Codes</span></span>](product-codes.md)
</dt> <dt>

[<span data-ttu-id="035d1-129">**Zusammenfassungs Eigenschaft der Revisionsnummer**</span><span class="sxs-lookup"><span data-stu-id="035d1-129">**Revision Number Summary Property**</span></span>](revision-number-summary.md)
</dt> <dt>

[<span data-ttu-id="035d1-130">**UpgradeCode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="035d1-130">**UpgradeCode Property**</span></span>](upgradecode.md)
</dt> <dt>

[<span data-ttu-id="035d1-131">**ProductCode-Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="035d1-131">**ProductCode Property**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="035d1-132">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="035d1-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



