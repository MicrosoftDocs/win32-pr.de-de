---
description: ICE11 wird bei gleichzeitigen Installationen verwendet. Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind. Weitere Informationen zu gleichzeitigen Installationen finden Sie unter Parallele Installationen.
ms.assetid: fbcc94fa-be94-4ad1-a3f0-ea7d50ee0a15
title: ICE11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3f85a4dc4d736acfbd4385324aa35565f399bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960041"
---
# <a name="ice11"></a><span data-ttu-id="294d0-105">ICE11</span><span class="sxs-lookup"><span data-stu-id="294d0-105">ICE11</span></span>

<span data-ttu-id="294d0-106">ICE11 wird bei gleichzeitigen Installationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="294d0-106">The ICE11 is used with concurrent installations.</span></span> <span data-ttu-id="294d0-107">Parallele Installationen werden nicht für die Installation von Anwendungen empfohlen, die für die öffentliche Veröffentlichung vorgesehen sind.</span><span class="sxs-lookup"><span data-stu-id="294d0-107">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="294d0-108">Weitere Informationen zu gleichzeitigen Installationen finden Sie unter [parallele Installationen](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="294d0-108">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

## <a name="result"></a><span data-ttu-id="294d0-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="294d0-109">Result</span></span>

<span data-ttu-id="294d0-110">ICE11 überprüft die Quell Spalte der [CustomAction-Tabelle](customaction-table.md) mit benutzerdefinierten Aktionen für die gleichzeitige Installation.</span><span class="sxs-lookup"><span data-stu-id="294d0-110">ICE11 validates the Source column of the [CustomAction table](customaction-table.md) of concurrent installation custom actions.</span></span> <span data-ttu-id="294d0-111">Die Quell Spalte muss eine gültige [GUID](guid.md) (MSI-Produktcode) enthalten.</span><span class="sxs-lookup"><span data-stu-id="294d0-111">The Source column must contain a valid [GUID](guid.md) (MSI product code).</span></span>

<span data-ttu-id="294d0-112">ICE11 gibt einen Fehler aus, wenn die Quell Spalte der Tabelle CustomAction nicht ordnungsgemäß für benutzerdefinierte Aktionen der gleichzeitigen Installation erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="294d0-112">ICE11 posts an error if the Source column of the CustomAction table is authored incorrectly for concurrent installation custom actions.</span></span>

## <a name="example"></a><span data-ttu-id="294d0-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="294d0-113">Example</span></span>

<span data-ttu-id="294d0-114">Ice gibt die folgenden Fehlermeldungen für das gezeigte Beispiel aus.</span><span class="sxs-lookup"><span data-stu-id="294d0-114">ICE posts the following error messages for the example shown.</span></span>

``` syntax
CustomAction: CA4 is a nested install of an advertised MSI.  The 'Source' must contain a valid MSI product code.  Current: ProductCode.
CustomAction: CA1 is a nested install of an advertised MSI.  It duplicates the ProductCode of the base MSI package.  Current: {BFB69273-F0AE-45C4-9853-0AF946714768}.
CustomAction: CA2 is a nested install of an advertised MSI.  The GUID must be all upper-case.  Current: {BFB69273-F0AE-55c5-9853-0AF946714768}.
```

<span data-ttu-id="294d0-115">[Eigenschaften Tabelle](property-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="294d0-115">[Property Table](property-table.md) (partial)</span></span>



| <span data-ttu-id="294d0-116">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="294d0-116">Property</span></span>        | <span data-ttu-id="294d0-117">Wert</span><span class="sxs-lookup"><span data-stu-id="294d0-117">Value</span></span>                                  |
|-----------------|----------------------------------------|
| <span data-ttu-id="294d0-118">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="294d0-118">**ProductCode**</span></span> | <span data-ttu-id="294d0-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="294d0-119">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |



 

<span data-ttu-id="294d0-120">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="294d0-120">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="294d0-121">CustomAction</span><span class="sxs-lookup"><span data-stu-id="294d0-121">CustomAction</span></span> | <span data-ttu-id="294d0-122">type</span><span class="sxs-lookup"><span data-stu-id="294d0-122">Type</span></span> | <span data-ttu-id="294d0-123">`Source`</span><span class="sxs-lookup"><span data-stu-id="294d0-123">Source</span></span>                                 |
|--------------|------|----------------------------------------|
| <span data-ttu-id="294d0-124">KA1</span><span class="sxs-lookup"><span data-stu-id="294d0-124">CA1</span></span>          | <span data-ttu-id="294d0-125">39</span><span class="sxs-lookup"><span data-stu-id="294d0-125">39</span></span>   | <span data-ttu-id="294d0-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="294d0-126">{BFB69273-F0AE-45C4-9853-0AF946714768}</span></span> |
| <span data-ttu-id="294d0-127">Ca2</span><span class="sxs-lookup"><span data-stu-id="294d0-127">CA2</span></span>          | <span data-ttu-id="294d0-128">39</span><span class="sxs-lookup"><span data-stu-id="294d0-128">39</span></span>   | <span data-ttu-id="294d0-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="294d0-129">{BFB69273-F0AE-55c5-9853-0AF946714768}</span></span> |
| <span data-ttu-id="294d0-130">CA3</span><span class="sxs-lookup"><span data-stu-id="294d0-130">CA3</span></span>          | <span data-ttu-id="294d0-131">39</span><span class="sxs-lookup"><span data-stu-id="294d0-131">39</span></span>   | <span data-ttu-id="294d0-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span><span class="sxs-lookup"><span data-stu-id="294d0-132">{BFB69273-F0AE-66C6-9853-0AF946714768}</span></span> |
| <span data-ttu-id="294d0-133">CA4</span><span class="sxs-lookup"><span data-stu-id="294d0-133">CA4</span></span>          | <span data-ttu-id="294d0-134">39</span><span class="sxs-lookup"><span data-stu-id="294d0-134">39</span></span>   | <span data-ttu-id="294d0-135">ProductCode</span><span class="sxs-lookup"><span data-stu-id="294d0-135">ProductCode</span></span>                            |



 

<span data-ttu-id="294d0-136">Um die Fehler zu beheben, können Sie für CA1 keine gleichzeitige Installation des "Basispakets" durchführen.</span><span class="sxs-lookup"><span data-stu-id="294d0-136">To fix the errors, for CA1, you cannot do a concurrent installation of the "base package".</span></span> <span data-ttu-id="294d0-137">Dies führt zu einer rekursiven Installation.</span><span class="sxs-lookup"><span data-stu-id="294d0-137">This would result in a recursive installation.</span></span> <span data-ttu-id="294d0-138">Dieser Eintrag sollte entfernt werden, oder die Quell Spalte sollte in eine GUID für eine angekündigte MSI geändert werden, die von der GUID des Basispakets abweicht.</span><span class="sxs-lookup"><span data-stu-id="294d0-138">This entry should be removed or the Source column should be changed to a GUID for an advertised MSI that differs from the base package's GUID.</span></span> <span data-ttu-id="294d0-139">Legen Sie für Ca2 alle Zeichen der GUID in Großbuchstaben ab.</span><span class="sxs-lookup"><span data-stu-id="294d0-139">For CA2, make all characters of the GUID uppercase.</span></span> <span data-ttu-id="294d0-140">Ändern Sie schließlich CA4's Source Column, um auf eine gültige GUID einer angekündigten MSI-Datei zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="294d0-140">Lastly, change CA4's Source column to reference a valid GUID of an advertised MSI.</span></span>

## <a name="related-topics"></a><span data-ttu-id="294d0-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="294d0-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="294d0-142">Parallele Installationen</span><span class="sxs-lookup"><span data-stu-id="294d0-142">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="294d0-143">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="294d0-143">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



