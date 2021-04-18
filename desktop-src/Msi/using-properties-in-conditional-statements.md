---
description: Der logische Wert einer Eigenschaft, die festgelegt wurde, ist "true".
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Verwenden von Eigenschaften in Bedingungs Anweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354488"
---
# <a name="using-properties-in-conditional-statements"></a><span data-ttu-id="c3643-103">Verwenden von Eigenschaften in Bedingungs Anweisungen</span><span class="sxs-lookup"><span data-stu-id="c3643-103">Using Properties in Conditional Statements</span></span>

<span data-ttu-id="c3643-104">Der logische Wert einer Eigenschaft, die festgelegt wurde, ist "true".</span><span class="sxs-lookup"><span data-stu-id="c3643-104">The logical value of a property that has been set is True.</span></span> <span data-ttu-id="c3643-105">Um zu ermitteln, ob eine Eigenschaft festgelegt wurde, ohne tatsächlich ihren Wert zu erhalten, testen Sie den logischen Ausdruck "MyProperty" oder "Not MyProperty".</span><span class="sxs-lookup"><span data-stu-id="c3643-105">To determine whether a property is set without actually getting its value, test the logical expression "MyProperty" or "Not MyProperty".</span></span> <span data-ttu-id="c3643-106">Wenn die Eigenschaft MyProperty festgelegt ist, wird die erste als true ausgewertet und letztere als false.</span><span class="sxs-lookup"><span data-stu-id="c3643-106">When the property MyProperty is set, the former evaluates as True and the latter as False.</span></span>

<span data-ttu-id="c3643-107">Eine oder mehrere Eigenschaften können mit Operatoren kombiniert werden, um logische Ausdrücke zu bilden, die in Bedingungs Anweisungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3643-107">One or more properties can be combined with operators to form logical expressions used in a conditional statements.</span></span> <span data-ttu-id="c3643-108">Weitere Informationen zu den Operatoren, die in Bedingungs Anweisungen verwendet werden können, finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="c3643-108">For more information about the operators that can be used in conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

<span data-ttu-id="c3643-109">Eine Bedingungs Anweisung, die Eigenschaften verwendet, kann in die Spalte Bedingung der Bedingungs [Tabelle](condition-table.md) eingegeben werden, um den Auswahl Zustand eines beliebigen Eintrags in der [Featuretabelle](feature-table.md)zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c3643-109">A conditional statement using properties can be entered into the Condition column of the [Condition table](condition-table.md) to modify the selection state of any entry in the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="c3643-110">Bedingte Anweisungen mit einer oder mehreren Eigenschaften werden häufig in der Spalte Bedingung der Datenbanktabellen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3643-110">Conditional statements with one or more properties are commonly used in the Condition column of database tables.</span></span>

<span data-ttu-id="c3643-111">Die folgenden Tabellen verfügen jeweils über eine-Spalte für bedingte Ausdrücke:</span><span class="sxs-lookup"><span data-stu-id="c3643-111">The following tables each have a column for conditional expressions:</span></span>

-   [<span data-ttu-id="c3643-112">Bedingungs Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-112">Condition table</span></span>](condition-table.md)
-   [<span data-ttu-id="c3643-113">ControlEvent-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-113">ControlEvent table</span></span>](controlevent-table.md)
-   [<span data-ttu-id="c3643-114">LaunchCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-114">LaunchCondition table</span></span>](launchcondition-table.md)
-   [<span data-ttu-id="c3643-115">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-115">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="c3643-116">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-116">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="c3643-117">ControlCondition-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-117">ControlCondition table</span></span>](controlcondition-table.md)
-   [<span data-ttu-id="c3643-118">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-118">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="c3643-119">AdvtExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-119">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)
-   [<span data-ttu-id="c3643-120">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c3643-120">AdminUISequence table</span></span>](adminuisequence-table.md)

<span data-ttu-id="c3643-121">Beachten Sie, dass die sechs Aktions Sequenz Tabellen Felder für eine Bedingung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="c3643-121">Note that the six action sequence tables have fields for a condition.</span></span> <span data-ttu-id="c3643-122">Wenn der bedingte Ausdruck in diesem Feld false ergibt, überspringt das Installationsprogramm diese Aktion.</span><span class="sxs-lookup"><span data-stu-id="c3643-122">If the conditional expression in this field evaluates to False, the installer skips that action.</span></span>

<span data-ttu-id="c3643-123">Wenn Sie in der UI-Sequenz eine [private Eigenschaft](private-properties.md) festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächen-Sequenz Tabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c3643-123">If you set a [private property](private-properties.md) in the UI sequence by authoring a custom action in one of the user interface sequence tables, that property is not set in the execution sequence.</span></span> <span data-ttu-id="c3643-124">Wenn Sie die-Eigenschaft in der Ausführungssequenz festlegen möchten, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenz Tabelle einfügen.</span><span class="sxs-lookup"><span data-stu-id="c3643-124">To set the property in the execution sequence you must also put a custom action in an execution sequence table.</span></span> <span data-ttu-id="c3643-125">Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft einschließen.</span><span class="sxs-lookup"><span data-stu-id="c3643-125">Alternatively, you can make the property a [public property](public-properties.md) and include it in the [**SecureCustomProperties**](securecustomproperties.md) property.</span></span>

<span data-ttu-id="c3643-126">Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) oder [Verwenden von Eigenschaften](using-properties.md).</span><span class="sxs-lookup"><span data-stu-id="c3643-126">For more information, see [Using a Sequence Table](using-a-sequence-table.md) or [Using Properties](using-properties.md).</span></span>

 

 



