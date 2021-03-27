---
description: Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann. Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt.
ms.assetid: B6D4C879-3E52-4010-9B2E-3BCD81BB6C93
title: Verwenden des Verb Auswahl Modells
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 724cd1c15b18657e27f9cfc53e9362685c6e2e7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979576"
---
# <a name="how-to-employ-the-verb-selection-model"></a><span data-ttu-id="5ab53-104">Verwenden des Verb Auswahl Modells</span><span class="sxs-lookup"><span data-stu-id="5ab53-104">How to Employ the Verb Selection Model</span></span>

<span data-ttu-id="5ab53-105">Registrierungs Werte müssen für Verben festgelegt werden, um Situationen zu behandeln, in denen ein Benutzer ein einzelnes Element, mehrere Elemente oder eine Auswahl aus einem Element auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="5ab53-105">Registry values must be set for verbs to handle situations where a user can select a single item, multiple items, or a selection from an item.</span></span> <span data-ttu-id="5ab53-106">Ein Verb erfordert separate Registrierungs Werte für jede dieser drei Situationen, die das Verb unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5ab53-106">A verb requires separate registry values for each of these three situations that the verb supports.</span></span>

## <a name="instructions"></a><span data-ttu-id="5ab53-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="5ab53-107">Instructions</span></span>


<span data-ttu-id="5ab53-108">Geben Sie den multiselectmodel-Wert für alle Verben an.</span><span class="sxs-lookup"><span data-stu-id="5ab53-108">Specify the MultiSelectModel value for all verbs.</span></span> <span data-ttu-id="5ab53-109">Wenn der multiselectmodel-Wert nicht angegeben wird, wird er vom Typ der Verb-Implementierung abgeleitet, den Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="5ab53-109">If the MultiSelectModel value is not specified, it is inferred from the type of verb implementation you have chosen.</span></span> <span data-ttu-id="5ab53-110">Für com- **basierte Methoden (** z. b. "DropTarget" und "ExecuteCommand") wird angenommen, und für die anderen **Methoden wird angenommen** .</span><span class="sxs-lookup"><span data-stu-id="5ab53-110">For COM-based methods (such as DropTarget and ExecuteCommand) **Player** is assumed, and for the other methods **Document** is assumed.</span></span>

<span data-ttu-id="5ab53-111">Die möglichen Werte für das Verb Auswahl Modell lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="5ab53-111">The possible values for the verb selection model are as follows:</span></span>

1.  <span data-ttu-id="5ab53-112">Geben Sie **Single** für Verben an, die nur eine einzelne Auswahl unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5ab53-112">Specify **Single** for verbs that support only a single selection.</span></span>
2.  <span data-ttu-id="5ab53-113">Geben Sie **Player** für Verben an, die eine beliebige Anzahl von Elementen unterstützen</span><span class="sxs-lookup"><span data-stu-id="5ab53-113">Specify **Player** for verbs that support any number of items.</span></span>
3.  <span data-ttu-id="5ab53-114">Geben Sie ein **Dokument** für Verben an, die für jedes Element ein Fenster auf oberster Ebene erstellen.</span><span class="sxs-lookup"><span data-stu-id="5ab53-114">Specify **Document** for verbs that create a top-level window for each item.</span></span> <span data-ttu-id="5ab53-115">Dadurch wird die Anzahl der aktivierten Elemente beschränkt, und es wird vermieden, dass Systemressourcen nicht mehr genügend Systemressourcen haben, wenn der Benutzer zu viele Fenster öffnet.</span><span class="sxs-lookup"><span data-stu-id="5ab53-115">Doing so limits the number of items that are activated and helps avoid running out of system resources if the user opens too many windows.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ab53-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ab53-116">Remarks</span></span>

<span data-ttu-id="5ab53-117">Wenn die Anzahl der ausgewählten Elemente nicht mit dem Verb Auswahl Modell identisch ist oder größer als die in der folgenden Tabelle aufgeführten Standard Limits ist, wird das Verb nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5ab53-117">When the number of items selected does not match the verb selection model or is greater than the default limits outlined in the following table, the verb fails to appear.</span></span>



| <span data-ttu-id="5ab53-118">Typ der Verb Implementierung</span><span class="sxs-lookup"><span data-stu-id="5ab53-118">Type of verb implementation</span></span> | <span data-ttu-id="5ab53-119">Dokument</span><span class="sxs-lookup"><span data-stu-id="5ab53-119">Document</span></span> | <span data-ttu-id="5ab53-120">Player</span><span class="sxs-lookup"><span data-stu-id="5ab53-120">Player</span></span>    |
|-----------------------------|----------|-----------|
| <span data-ttu-id="5ab53-121">Alt</span><span class="sxs-lookup"><span data-stu-id="5ab53-121">Legacy</span></span>                      | <span data-ttu-id="5ab53-122">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="5ab53-122">15 items</span></span> | <span data-ttu-id="5ab53-123">100 Elemente</span><span class="sxs-lookup"><span data-stu-id="5ab53-123">100 items</span></span> |
| <span data-ttu-id="5ab53-124">COM</span><span class="sxs-lookup"><span data-stu-id="5ab53-124">COM</span></span>                         | <span data-ttu-id="5ab53-125">15 Elemente</span><span class="sxs-lookup"><span data-stu-id="5ab53-125">15 items</span></span> | <span data-ttu-id="5ab53-126">Keine Begrenzung</span><span class="sxs-lookup"><span data-stu-id="5ab53-126">No limit</span></span>  |



 

<span data-ttu-id="5ab53-127">Im folgenden finden Sie Beispiel Registrierungseinträge, die den multiselectmodel-Wert verwenden.</span><span class="sxs-lookup"><span data-stu-id="5ab53-127">The following are example registry entries that use the MultiSelectModel value.</span></span>

```
HKEY_CLASSES_ROOT
   Folder
      shell
         open
             = MultiSelectModel = Document
```

```
HKEY_CLASSES_ROOT
   ProgID
      shell
         verb
             = MultiSelectModel = Single | Document | Player
```

 

 



