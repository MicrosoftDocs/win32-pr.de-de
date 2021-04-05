---
description: ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Speicherorten, die sich von einer System definierten Eigenschaft nur durch die Groß-/Kleinschreibung von einem oder mehreren Zeichen unterscheiden.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756223"
---
# <a name="ice46"></a><span data-ttu-id="55cd0-103">ICE46</span><span class="sxs-lookup"><span data-stu-id="55cd0-103">ICE46</span></span>

<span data-ttu-id="55cd0-104">ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Speicherorten, die sich von einer System definierten Eigenschaft nur durch die Groß-/Kleinschreibung von einem oder mehreren Zeichen unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="55cd0-104">ICE46 checks for custom properties in conditions, formatted text, and other locations that differ from a system defined property only by the case of one or more characters.</span></span>

## <a name="result"></a><span data-ttu-id="55cd0-105">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="55cd0-105">Result</span></span>

<span data-ttu-id="55cd0-106">ICE46 gibt eine Informations Meldung aus, wenn eine benutzerdefinierte Eigenschaft in einer Bedingung, einem formatierten Text und einem anderen Speicherort vorhanden ist, der sich von einer System definierten Eigenschaft nur im Fall von mindestens einem Zeichen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="55cd0-106">ICE46 posts an informational message if there is a custom property in a condition, formatted text, and other location that differs from a system defined properties only in the case of one or more characters.</span></span>

## <a name="example"></a><span data-ttu-id="55cd0-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="55cd0-107">Example</span></span>

<span data-ttu-id="55cd0-108">ICE46 meldet die folgenden Fehler für das gezeigte Beispiel.</span><span class="sxs-lookup"><span data-stu-id="55cd0-108">ICE46 reports the following errors for the example shown.</span></span>



| <span data-ttu-id="55cd0-109">ICE46-Fehler</span><span class="sxs-lookup"><span data-stu-id="55cd0-109">ICE46 error</span></span>                                                                                                                                            | <span data-ttu-id="55cd0-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55cd0-110">Description</span></span>                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55cd0-111">Die in der Eigenschaften Tabelle definierte Eigenschaft "REINSTALLMODE" unterscheidet sich von einer anderen definierten Eigenschaft nur durch den Fall</span><span class="sxs-lookup"><span data-stu-id="55cd0-111">Property ReinstallMode defined in property table differs from another defined property only by case.</span></span>                                                   | <span data-ttu-id="55cd0-112">Der vom System definierte Eigenschaftsname " **REINSTALLMODE** " unterscheidet sich nur in der Groß-/Kleinschreibung von</span><span class="sxs-lookup"><span data-stu-id="55cd0-112">The system defined property name **REINSTALLMODE** differs from the custom property by case only.</span></span> <span data-ttu-id="55cd0-113">Bei Eigenschaften wird die Groß-/Kleinschreibung beachtet, sodass die benutzerdefinierte Eigenschaft nicht mit der System Eigenschaft identisch ist.</span><span class="sxs-lookup"><span data-stu-id="55cd0-113">Properties are case sensitive, so custom property is not the same as the system property.</span></span> <span data-ttu-id="55cd0-114">Dies ist eine häufige Ursache für Fehler.</span><span class="sxs-lookup"><span data-stu-id="55cd0-114">This is a common cause of errors.</span></span> |
| <span data-ttu-id="55cd0-115">Die Eigenschaft "MyProperty", auf die in der Spalte "InstallExecuteSequence" verwiesen wird. Die Bedingung ' der Zeile ' InstallFinalize ' unterscheidet sich von einer definierten Eigenschaft nur nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="55cd0-115">Property 'Myproperty' referenced in column 'InstallExecuteSequence'.'Condition' of row 'InstallFinalize' differs from a defined property by case only.</span></span> | <span data-ttu-id="55cd0-116">In der Eigenschafts Tabelle ist die MyProperty-Tabelle definiert, aber die referenzierte Eigenschaft ist MyProperty.</span><span class="sxs-lookup"><span data-stu-id="55cd0-116">The property table defines the table MyProperty, but the referenced property is Myproperty.</span></span> <span data-ttu-id="55cd0-117">Bei den Eigenschaften wird die Groß-/Kleinschreibung beachtet, sodass die beiden Eigenschaften nicht identisch sind.</span><span class="sxs-lookup"><span data-stu-id="55cd0-117">Properties are case sensitive, so the two properties are NOT the same.</span></span> <span data-ttu-id="55cd0-118">Dies ist eine häufige Ursache für Fehler.</span><span class="sxs-lookup"><span data-stu-id="55cd0-118">This is a common cause of errors.</span></span>                          |



 

[<span data-ttu-id="55cd0-119">Eigenschaften Tabelle</span><span class="sxs-lookup"><span data-stu-id="55cd0-119">Property Table</span></span>](property-table.md)



| <span data-ttu-id="55cd0-120">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="55cd0-120">Property</span></span>      | <span data-ttu-id="55cd0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="55cd0-121">Value</span></span>   |
|---------------|---------|
| <span data-ttu-id="55cd0-122">Rein Stall Mode</span><span class="sxs-lookup"><span data-stu-id="55cd0-122">ReinstallMode</span></span> | <span data-ttu-id="55cd0-123">omus REINSTALL</span><span class="sxs-lookup"><span data-stu-id="55cd0-123">omus</span></span>    |
| <span data-ttu-id="55cd0-124">MyProperty</span><span class="sxs-lookup"><span data-stu-id="55cd0-124">MyProperty</span></span>    | <span data-ttu-id="55cd0-125">ein-Wert</span><span class="sxs-lookup"><span data-stu-id="55cd0-125">a value</span></span> |



 

<span data-ttu-id="55cd0-126">[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)</span><span class="sxs-lookup"><span data-stu-id="55cd0-126">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="55cd0-127">Aktion</span><span class="sxs-lookup"><span data-stu-id="55cd0-127">Action</span></span>          | <span data-ttu-id="55cd0-128">Bedingung</span><span class="sxs-lookup"><span data-stu-id="55cd0-128">Condition</span></span>  |
|-----------------|------------|
| <span data-ttu-id="55cd0-129">InstallFinalize wurde</span><span class="sxs-lookup"><span data-stu-id="55cd0-129">InstallFinalize</span></span> | <span data-ttu-id="55cd0-130">MyProperty</span><span class="sxs-lookup"><span data-stu-id="55cd0-130">Myproperty</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="55cd0-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55cd0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55cd0-132">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="55cd0-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



