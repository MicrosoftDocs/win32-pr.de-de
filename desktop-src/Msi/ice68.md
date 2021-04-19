---
description: ICE68 prüft, ob alle für eine Installation benötigten benutzerdefinierten Aktions Typen gültig sind.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373343"
---
# <a name="ice68"></a><span data-ttu-id="e1381-103">ICE68</span><span class="sxs-lookup"><span data-stu-id="e1381-103">ICE68</span></span>

<span data-ttu-id="e1381-104">ICE68 prüft, ob alle für eine Installation benötigten benutzerdefinierten Aktions Typen gültig sind.</span><span class="sxs-lookup"><span data-stu-id="e1381-104">ICE68 checks that all custom action types needed for an installation are valid.</span></span> <span data-ttu-id="e1381-105">Wenn Sie den von ICE68 gemeldeten Fehler nicht beheben, bewirkt dies, dass eine Installation fehlschlägt, die versucht, die Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e1381-105">Failure to fix the error reported by ICE68 causes an installation that attempts to execute the action to fail.</span></span> <span data-ttu-id="e1381-106">ICE68 gibt eine Warnung aus, wenn das **msidbcustomaktiontypoidentitäts Ate** -Attribut festgelegt wird, ohne dass auch das **msidbcustomaktiontypeinscript** -Attribut festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="e1381-106">ICE68 issues a warning if the **msidbCustomActionTypeNoImpersonate** attribute is set without also setting the **msidbCustomActionTypeInScript** attribute.</span></span>

## <a name="result"></a><span data-ttu-id="e1381-107">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="e1381-107">Result</span></span>

<span data-ttu-id="e1381-108">ICE68 gibt einen Fehler zurück, wenn ein für eine Installation benötigter Aktionstyp ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="e1381-108">ICE68 returns an error if an action type needed for an installation is invalid.</span></span>

## <a name="example"></a><span data-ttu-id="e1381-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1381-109">Example</span></span>

<span data-ttu-id="e1381-110">ICE68 gibt die folgende Warnung aus, wenn für eine benutzerdefinierte Aktion das **msidbcustomaction typoidentitäts Ate** -Bit im type-Feld der CustomAction-Tabelle festgelegt ist, ohne dass **msidbcustomaction typeinscript** ebenfalls festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e1381-110">ICE68 posts the following warning if a custom action has the **msidbCustomActionTypeNoImpersonate** bit set in the Type field of the CustomAction table without the **msidbCustomActionTypeInScript** also set.</span></span>

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

<span data-ttu-id="e1381-111">Um diese Warnung zu beheben, schließen Sie **msidbcustomaction typeinscript** (0x400) ein, wenn die benutzerdefinierte Aktion **msidbcustomaction typoidentitäts Ate** (0x800) einschließt.</span><span class="sxs-lookup"><span data-stu-id="e1381-111">To fix this warning, include **msidbCustomActionTypeInScript** (0x400) if the custom action includes **msidbCustomActionTypeNoImpersonate** (0x800).</span></span> <span data-ttu-id="e1381-112">Andernfalls ignoriert das Installationsprogramm das **msidbcustomaktiontypoidentitäts Ate** -Attribut.</span><span class="sxs-lookup"><span data-stu-id="e1381-112">Otherwise the installer ignores the **msidbCustomActionTypeNoImpersonate** attribute.</span></span> <span data-ttu-id="e1381-113">Weitere Informationen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="e1381-113">For more information, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

<span data-ttu-id="e1381-114">ICE68 meldet den folgenden Fehler für das gezeigte Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e1381-114">ICE68 reports the following error for the example shown:</span></span>

``` syntax
Invalid custom action type for action 'Action1'.
```

<span data-ttu-id="e1381-115">1027 ist kein gültiger Aktionstyp.</span><span class="sxs-lookup"><span data-stu-id="e1381-115">1027 is not a valid action type.</span></span>

<span data-ttu-id="e1381-116">Wählen Sie einen gültigen benutzerdefinierten Aktionstyp aus, um diesen Fehler zu beheben.</span><span class="sxs-lookup"><span data-stu-id="e1381-116">To fix this error, choose a valid custom action type.</span></span>

<span data-ttu-id="e1381-117">[CustomAction-Tabelle](customaction-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="e1381-117">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="e1381-118">Aktion</span><span class="sxs-lookup"><span data-stu-id="e1381-118">Action</span></span>  | <span data-ttu-id="e1381-119">type</span><span class="sxs-lookup"><span data-stu-id="e1381-119">Type</span></span> | <span data-ttu-id="e1381-120">`Source`</span><span class="sxs-lookup"><span data-stu-id="e1381-120">Source</span></span>   | <span data-ttu-id="e1381-121">Ziel</span><span class="sxs-lookup"><span data-stu-id="e1381-121">Target</span></span>     |
|---------|------|----------|------------|
| <span data-ttu-id="e1381-122">Action1</span><span class="sxs-lookup"><span data-stu-id="e1381-122">Action1</span></span> | <span data-ttu-id="e1381-123">1027</span><span class="sxs-lookup"><span data-stu-id="e1381-123">1027</span></span> | <span data-ttu-id="e1381-124">Argument</span><span class="sxs-lookup"><span data-stu-id="e1381-124">Argument</span></span> | <span data-ttu-id="e1381-125">Component1</span><span class="sxs-lookup"><span data-stu-id="e1381-125">Component1</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e1381-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e1381-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1381-127">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="e1381-127">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



