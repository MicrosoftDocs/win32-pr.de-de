---
description: ICE26 überprüft Sequenz Tabellen in einer Windows Installer Datenbank.
ms.assetid: 7ea47452-3147-4d39-961d-a10eca8328c9
title: ICE26
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7b110d0b15b37441170980d0fd3e96e2eb00d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866292"
---
# <a name="ice26"></a><span data-ttu-id="312e8-103">ICE26</span><span class="sxs-lookup"><span data-stu-id="312e8-103">ICE26</span></span>

<span data-ttu-id="312e8-104">ICE26 überprüft, ob jede der folgenden [*Sequenz Tabellen*](s-gly.md) die von der Tabelle benötigten Aktionen enthält und keine Aktionen enthält, die in der Tabelle nicht zulässig sind:</span><span class="sxs-lookup"><span data-stu-id="312e8-104">ICE26 validates that each of the following [*sequence tables*](s-gly.md) contain the actions that are required by the table and does not contain any actions disallowed in the table:</span></span>

-   [<span data-ttu-id="312e8-105">AdminUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="312e8-105">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="312e8-106">AdminExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="312e8-106">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="312e8-107">InstallUISequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="312e8-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="312e8-108">InstallExecuteSequence-Tabelle</span><span class="sxs-lookup"><span data-stu-id="312e8-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)

## <a name="result"></a><span data-ttu-id="312e8-109">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="312e8-109">Result</span></span>

<span data-ttu-id="312e8-110">ICE26 gibt eine Fehlermeldung aus, wenn das Installationspaket eine Sequenz Tabelle enthält, für die eine erforderliche Aktion fehlt oder die eine Aktion enthält, die für die Tabelle nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="312e8-110">ICE26 posts an error message if the installation package has a sequence table that lacks a required action or that contains an action that is disallowed for the table.</span></span>

## <a name="example"></a><span data-ttu-id="312e8-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="312e8-111">Example</span></span>



| <span data-ttu-id="312e8-112">ICE26-Fehler</span><span class="sxs-lookup"><span data-stu-id="312e8-112">ICE26 error</span></span>                                                                   | <span data-ttu-id="312e8-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="312e8-113">Description</span></span>                                                                                                                                                                    |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="312e8-114">Aktion: ' Action1 ' ist in der InstallExecuteSequence-Sequenz Tabelle erforderlich.</span><span class="sxs-lookup"><span data-stu-id="312e8-114">Action: 'Action1' is required in the InstallExecuteSequence Sequence table.</span></span>   | <span data-ttu-id="312e8-115">Eine erforderliche Aktion fehlt in der angegebener Sequenz Tabelle.</span><span class="sxs-lookup"><span data-stu-id="312e8-115">A required action is missing from the indicated sequence table.</span></span> <span data-ttu-id="312e8-116">Weitere Informationen finden Sie in den template.msi oder den vorgeschlagenen Sequenz Tabellen unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="312e8-116">See the template.msi or the suggested sequence tables in [Using a Sequence Table](using-a-sequence-table.md).</span></span> |
| <span data-ttu-id="312e8-117">Aktion: ' Action2 ' ist in der InstallExecuteSequence-Sequenz Tabelle nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="312e8-117">Action: 'Action2' is prohibited in the InstallExecuteSequence Sequence table.</span></span> | <span data-ttu-id="312e8-118">Diese Aktion kann nicht in der angegeben Sequenz Tabelle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="312e8-118">This action cannot be in the indicated sequence table.</span></span> <span data-ttu-id="312e8-119">Entfernen Sie diese Aktion aus der Sequenz Tabelle.</span><span class="sxs-lookup"><span data-stu-id="312e8-119">Remove this action from the sequence table.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="312e8-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="312e8-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312e8-121">Ice-Referenz</span><span class="sxs-lookup"><span data-stu-id="312e8-121">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



