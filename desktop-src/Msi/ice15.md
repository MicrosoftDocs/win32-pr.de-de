---
description: ICE15 überprüft, ob Inhaltstyp-und Erweiterungs Verweise in den MIME-und Erweiterungs Tabellen einander einander entsprechen. Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungs Tabelle auf denselben Inhaltstyp zurückverweist.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042539"
---
# <a name="ice15"></a><span data-ttu-id="0c093-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="0c093-104">ICE15</span></span>

<span data-ttu-id="0c093-105">ICE15 überprüft, ob Inhaltstyp-und Erweiterungs Verweise in den [MIME](mime-table.md) -und [Erweiterungs](extension-table.md) Tabellen einander einander entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0c093-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="0c093-106">Die MIME-Tabelle muss auf einen Inhaltstyp auf eine Erweiterung verweisen, auf die die Erweiterungs Tabelle auf denselben Inhaltstyp zurückverweist.</span><span class="sxs-lookup"><span data-stu-id="0c093-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="0c093-107">Mehrere Erweiterungen können auf denselben MIME-Typ verweisen, solange der MIME-Typ auf eine der Erweiterungen zurückverweist.</span><span class="sxs-lookup"><span data-stu-id="0c093-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="0c093-108">Mehrere MIME-Typen können auf dieselbe Erweiterung verweisen, solange die Erweiterung auf einen der MIME-Typen zurückverweist.</span><span class="sxs-lookup"><span data-stu-id="0c093-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="0c093-109">Beachten Sie, dass die MIME- \_ Spalte in der Erweiterungs Tabelle nicht auf NULL festgelegt werden kann, wenn ein MIME auf eine Erweiterung verweist.</span><span class="sxs-lookup"><span data-stu-id="0c093-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="0c093-110">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="0c093-110">Result</span></span>

<span data-ttu-id="0c093-111">ICE15 gibt einen Fehler aus, wenn der Inhaltstyp und die Erweiterungs Verweise nicht gegenseitig sind.</span><span class="sxs-lookup"><span data-stu-id="0c093-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="0c093-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0c093-112">Example</span></span>

<span data-ttu-id="0c093-113">ICE15 gibt zwei Fehlermeldungen für das folgende Beispiel aus:</span><span class="sxs-lookup"><span data-stu-id="0c093-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="0c093-114">Der Inhaltstyp "Test/x-Flas" in der MIME-Tabelle verweist auf die Erweiterung "TST", aber die Erweiterung "TST" in der Erweiterungs Tabelle verweist auf "Flas/x-</span><span class="sxs-lookup"><span data-stu-id="0c093-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="0c093-115">Dies ist kein gegenseitiger Wert.</span><span class="sxs-lookup"><span data-stu-id="0c093-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="0c093-116">Die Inhaltstyp-Klappen/x-Klappen verweisen auf die Erweiterungs-FLP, aber diese Erweiterung weist einen NULL-Eintrag in der MIME- \_ Spalte der Erweiterungs Tabelle auf.</span><span class="sxs-lookup"><span data-stu-id="0c093-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="0c093-117">[MIME-Tabelle](mime-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0c093-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="0c093-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="0c093-118">ContentType</span></span>   | <span data-ttu-id="0c093-119">Durchwahl\_</span><span class="sxs-lookup"><span data-stu-id="0c093-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="0c093-120">Test/x-Test</span><span class="sxs-lookup"><span data-stu-id="0c093-120">test/x-test</span></span>   | <span data-ttu-id="0c093-121">TST</span><span class="sxs-lookup"><span data-stu-id="0c093-121">tst</span></span>         |
| <span data-ttu-id="0c093-122">Klappen/x-Klappen</span><span class="sxs-lookup"><span data-stu-id="0c093-122">flaps/x-flaps</span></span> | <span data-ttu-id="0c093-123">FLP</span><span class="sxs-lookup"><span data-stu-id="0c093-123">flp</span></span>         |



 

<span data-ttu-id="0c093-124">[Erweiterungs Tabelle](extension-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="0c093-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="0c093-125">Durchwahl</span><span class="sxs-lookup"><span data-stu-id="0c093-125">Extension</span></span> | <span data-ttu-id="0c093-126">Medi\_</span><span class="sxs-lookup"><span data-stu-id="0c093-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="0c093-127">TST</span><span class="sxs-lookup"><span data-stu-id="0c093-127">tst</span></span>       | <span data-ttu-id="0c093-128">Klappen/x-Klappen</span><span class="sxs-lookup"><span data-stu-id="0c093-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="0c093-129">FLP</span><span class="sxs-lookup"><span data-stu-id="0c093-129">flp</span></span>       | <span data-ttu-id="0c093-130">Null</span><span class="sxs-lookup"><span data-stu-id="0c093-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="0c093-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0c093-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c093-132">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="0c093-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



