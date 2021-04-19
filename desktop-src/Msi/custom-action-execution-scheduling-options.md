---
description: Da eine benutzerdefinierte Aktion sowohl in der UI-als auch in der Execute Sequence-Tabelle geplant werden kann und entweder im Dienst-oder Client Prozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.
ms.assetid: a3ffeecb-cdd6-43af-a3fe-48e3e843ec8b
title: Ausführungszeit Planungsoptionen für benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfa5aee44f3ad357eefc6f9dd9c5ee5ae45797c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348662"
---
# <a name="custom-action-execution-scheduling-options"></a><span data-ttu-id="08751-103">Ausführungszeit Planungsoptionen für benutzerdefinierte Aktionen</span><span class="sxs-lookup"><span data-stu-id="08751-103">Custom Action Execution Scheduling Options</span></span>

<span data-ttu-id="08751-104">Da eine benutzerdefinierte Aktion sowohl in der UI-als auch in der Execute Sequence-Tabelle geplant werden kann und entweder im Dienst-oder Client Prozess ausgeführt werden kann, kann eine benutzerdefinierte Aktion möglicherweise mehrmals ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="08751-104">Because a custom action can be scheduled in both the UI and execute sequence tables, and can be executed either in the service or client process, a custom action can potentially execute multiple times.</span></span>

<span data-ttu-id="08751-105">Beachten Sie, dass das Installationsprogramm:</span><span class="sxs-lookup"><span data-stu-id="08751-105">Note that the installer:</span></span>

-   <span data-ttu-id="08751-106">Führt Aktionen in einer Sequenz Tabelle sofort standardmäßig aus.</span><span class="sxs-lookup"><span data-stu-id="08751-106">Executes actions in a sequence table immediately by default.</span></span>
-   <span data-ttu-id="08751-107">Führt keine Aktion aus, wenn das Feld für den bedingten Ausdruck der Sequenz Tabelle als false ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="08751-107">Does not execute an action if the conditional expression field of the sequence table evaluates to False.</span></span>
-   <span data-ttu-id="08751-108">Verarbeitet die UI-Sequenz Tabelle im Client Prozess, wenn die Schnittstellen Ebene des internen Benutzers auf den vollständigen Benutzeroberflächen Modus festgelegt ist (Weitere Informationen finden Sie unter [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) für eine Beschreibung der UI-Ebenen).</span><span class="sxs-lookup"><span data-stu-id="08751-108">Processes the UI sequence table in the client process if the internal user's interface level is set to the full UI mode (see [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui) for a description of UI levels).</span></span>
-   <span data-ttu-id="08751-109">Ist ein Dienst, der bei Verwendung von Windows 2000 standardmäßig registriert ist, und in diesem Fall wird die Execute Sequence-Tabelle im Installerdienst verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="08751-109">Is a service registered by default when using Windows 2000 and, in this case, the execute sequence table is processed in the installer service.</span></span>

<span data-ttu-id="08751-110">Sie können die folgenden Optionsflags verwenden, um die sofortige Ausführung von benutzerdefinierten Aktionen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="08751-110">You can use the following option flags to control multiple immediate execution of custom actions.</span></span> <span data-ttu-id="08751-111">Fügen Sie zum Festlegen einer Option den Wert in dieser Tabelle dem Wert im Feld Typ der [Tabelle CustomAction](customaction-table.md)hinzu.</span><span class="sxs-lookup"><span data-stu-id="08751-111">To set an option, add the value in this table to the value in the Type field of the [CustomAction table](customaction-table.md).</span></span> <span data-ttu-id="08751-112">Keines der folgenden Flags sollte mit [benutzerdefinierten Aktionen für die verzögerte Ausführung](deferred-execution-custom-actions.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08751-112">None of the following flags should be used with [deferred execution custom actions](deferred-execution-custom-actions.md).</span></span>

<dl> <dt>

<span data-ttu-id="08751-113"><span id="_default_"></span><span id="_DEFAULT_"></span>vorgegebene</span><span class="sxs-lookup"><span data-stu-id="08751-113"><span id="_default_"></span><span id="_DEFAULT_"></span>(default)</span></span>
</dt> <dd>

<span data-ttu-id="08751-114">Hexadezimalwert: 0x00000000</span><span class="sxs-lookup"><span data-stu-id="08751-114">Hexadecimal: 0x00000000</span></span>

<span data-ttu-id="08751-115">Dezimalwert: 0</span><span class="sxs-lookup"><span data-stu-id="08751-115">Decimal: 0</span></span>

<span data-ttu-id="08751-116">Immer ausführen.</span><span class="sxs-lookup"><span data-stu-id="08751-116">Always execute.</span></span> <span data-ttu-id="08751-117">Die Aktion kann zweimal ausgeführt werden, wenn Sie in beiden Sequenz Tabellen vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="08751-117">Action may run twice if present in both sequence tables.</span></span>

</dd> <dt>

<span data-ttu-id="08751-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbcustomaktiontypefirstsequence**</span><span class="sxs-lookup"><span data-stu-id="08751-118"><span id="msidbCustomActionTypeFirstSequence_"></span><span id="msidbcustomactiontypefirstsequence_"></span><span id="MSIDBCUSTOMACTIONTYPEFIRSTSEQUENCE_"></span>**msidbCustomActionTypeFirstSequence**</span></span> 
</dt> <dd>

<span data-ttu-id="08751-119">Hexadezimalwert: 0x00000100</span><span class="sxs-lookup"><span data-stu-id="08751-119">Hexadecimal: 0x00000100</span></span>

<span data-ttu-id="08751-120">Dezimalzahl: 256</span><span class="sxs-lookup"><span data-stu-id="08751-120">Decimal: 256</span></span>

<span data-ttu-id="08751-121">Führen Sie nicht mehr als einmal aus, wenn Sie in beiden Sequenz Tabellen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="08751-121">Execute no more than once if present in both sequence tables.</span></span> <span data-ttu-id="08751-122">Überspringt immer die Aktion in der Ausführungssequenz, wenn die UI-Sequenz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="08751-122">Always skips action in execute sequence if UI sequence has run.</span></span> <span data-ttu-id="08751-123">Keine Auswirkung in der UI-Sequenz.</span><span class="sxs-lookup"><span data-stu-id="08751-123">No effect in UI sequence.</span></span> <span data-ttu-id="08751-124">Die Aktion muss nicht in der UI-Sequenz vorhanden sein oder ausgeführt werden, damit Sie in der Ausführungssequenz übersprungen werden kann.</span><span class="sxs-lookup"><span data-stu-id="08751-124">The action is not required to be present or run in the UI sequence to be skipped in the execute sequence.</span></span> <span data-ttu-id="08751-125">Von der Installations Dienst Registrierung nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="08751-125">Not affected by install service registration.</span></span>

</dd> <dt>

<span data-ttu-id="08751-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbcustomaktiontypeonceperprocess**</span><span class="sxs-lookup"><span data-stu-id="08751-126"><span id="msidbCustomActionTypeOncePerProcess"></span><span id="msidbcustomactiontypeonceperprocess"></span><span id="MSIDBCUSTOMACTIONTYPEONCEPERPROCESS"></span>**msidbCustomActionTypeOncePerProcess**</span></span>
</dt> <dd>

<span data-ttu-id="08751-127">Hexadezimalwert: 0x00000200</span><span class="sxs-lookup"><span data-stu-id="08751-127">Hexadecimal: 0x00000200</span></span>

<span data-ttu-id="08751-128">Dezimalzahl: 512</span><span class="sxs-lookup"><span data-stu-id="08751-128">Decimal: 512</span></span>

<span data-ttu-id="08751-129">Ausführung einmal pro Prozess, wenn in beiden Sequenz Tabellen.</span><span class="sxs-lookup"><span data-stu-id="08751-129">Execute once per process if in both sequence tables.</span></span> <span data-ttu-id="08751-130">Überspringt die Aktion in der Ausführungssequenz, wenn die UI-Sequenz im selben Prozess ausgeführt wurde, z. b. beide werden im Client Prozess ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08751-130">Skips action in execute sequence if UI sequence has been run in same process, for example both run in the client process.</span></span> <span data-ttu-id="08751-131">Wird verwendet, um zu verhindern, dass Aktionen, die den Sitzungszustand ändern (z. b. Eigenschaften-und Datenbankdaten), zweimal</span><span class="sxs-lookup"><span data-stu-id="08751-131">Used to prevent actions that modify the session state, such as property and database data, from running twice.</span></span>

</dd> <dt>

<span data-ttu-id="08751-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbcustomaktiontypeclientrepeat**</span><span class="sxs-lookup"><span data-stu-id="08751-132"><span id="msidbCustomActionTypeClientRepeat"></span><span id="msidbcustomactiontypeclientrepeat"></span><span id="MSIDBCUSTOMACTIONTYPECLIENTREPEAT"></span>**msidbCustomActionTypeClientRepeat**</span></span>
</dt> <dd>

<span data-ttu-id="08751-133">Hexadezimalwert: 0x00000300</span><span class="sxs-lookup"><span data-stu-id="08751-133">Hexadecimal: 0x00000300</span></span>

<span data-ttu-id="08751-134">Dezimalzahl: 768</span><span class="sxs-lookup"><span data-stu-id="08751-134">Decimal: 768</span></span>

<span data-ttu-id="08751-135">Nur ausführen, wenn auf dem Client ausgeführt wird, nachdem die UI-Sequenz ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="08751-135">Execute only if running on client after UI sequence has run.</span></span> <span data-ttu-id="08751-136">Die Aktion wird nur ausgeführt, wenn die Ausführungssequenz auf dem Client nach der Benutzeroberflächen Sequenz ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08751-136">The action runs only if the execute sequence is run on the client following UI sequence.</span></span> <span data-ttu-id="08751-137">Kann verwendet werden, um entweder/oder Logik bereitzustellen oder um die UI-bezogene Verarbeitung zu unterdrücken, falls dies für die Client Sitzung bereits erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="08751-137">May be used to provide either/or logic, or to suppress the UI-related processing if already done for the client session.</span></span>

</dd> </dl>

<span data-ttu-id="08751-138">Beachten Sie, dass zum Ausführen einer benutzerdefinierten Aktion in zwei verschiedenen Laufzeiten zwei Einträge in der [Tabelle CustomAction](customaction-table.md) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="08751-138">Note that to run a custom action during two different run modes, author two entries into the [CustomAction table](customaction-table.md) .</span></span> <span data-ttu-id="08751-139">Um z. b. eine benutzerdefinierte Aktion zu haben, die eine C/C++ Dynamic Link Library (dll) aufruft ( [benutzerdefinierter Aktionstyp 1](custom-action-type-1.md)), wenn der Modus msirunmode \_ geplant und msirunmode \_ Rollback ist, fügen Sie zwei Einträge in die Tabelle CustomAction ein, die dieselbe DLL aufrufen, aber unterschiedliche numerische Typen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="08751-139">For example, to have a custom action that calls a C/C++ dynamic link library (DLL) ( [Custom Action Type 1](custom-action-type-1.md)) both when the mode is MSIRUNMODE\_SCHEDULED and MSIRUNMODE\_ROLLBACK, put two entries in the CustomAction table that call the same DLL but that have different numeric types.</span></span> <span data-ttu-id="08751-140">Fügen Sie Code ein, der [**msigetmode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) aufruft, um zu bestimmen, wann welche benutzerdefinierte Aktion auszuführen ist.</span><span class="sxs-lookup"><span data-stu-id="08751-140">Include code that calls [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) to determine when to run which custom action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="08751-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="08751-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08751-142">Referenz zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="08751-142">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="08751-143">Informationen zu benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="08751-143">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="08751-144">Verwenden von benutzerdefinierten Aktionen</span><span class="sxs-lookup"><span data-stu-id="08751-144">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



