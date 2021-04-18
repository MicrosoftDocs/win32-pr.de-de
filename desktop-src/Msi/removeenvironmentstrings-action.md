---
description: Die removeenvironment Strings-Aktion ändert die Werte von Umgebungsvariablen.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Removeumgebstrings-Aktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106365196"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="7db97-103">Removeumgebstrings-Aktion</span><span class="sxs-lookup"><span data-stu-id="7db97-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="7db97-104">Die removeenvironment Strings-Aktion ändert die Werte von Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="7db97-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="7db97-105">Beachten Sie, dass die Umgebungsvariablen für die laufende Installation nicht geändert werden, wenn entweder die Aktion "Schreiben von [Schreib Aktionen](writeenvironmentstrings-action.md) " oder "removeenvironment Strings" ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7db97-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="7db97-106">Unter Windows 2000 werden diese Informationen in der Registrierung gespeichert, und es wird eine Nachricht gesendet, um das System über Änderungen zu benachrichtigen, wenn die Installation abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7db97-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="7db97-107">Ein neuer Prozess oder ein anderer Prozess, bei dem diese Nachrichten überprüft werden, werden die neuen Umgebungsvariablen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7db97-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="7db97-108">Das Installationsprogramm führt die "Write Report Environment Strings"- [Aktion](writeenvironmentstrings-action.md) nur während der Installation oder erneuten Installation einer Komponente aus und führt die Aktion "removeumgebstrings" nur während des Entfernens einer Komponente aus.</span><span class="sxs-lookup"><span data-stu-id="7db97-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="7db97-109">Werte werden basierend auf der Auswahl der primären Aktionen und Modifizierer geschrieben oder entfernt.</span><span class="sxs-lookup"><span data-stu-id="7db97-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="7db97-110">Diese werden im folgenden Abschnitt "Aktions Daten Meldungen" beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7db97-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="7db97-111">Beachten Sie, dass mit "Write-Environment Strings" abhängig von der angegebenen Aktion Variablen entfernt werden können und dass removeumgebungszeichenfolgen diese basierend auf der Erstellung der [Umgebungs Tabelle](environment-table.md)hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="7db97-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="7db97-112">Sequenz Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="7db97-112">Sequence Restrictions</span></span>

<span data-ttu-id="7db97-113">Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der removeumgebstrings-Aktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="7db97-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="7db97-114">Da die Aktion "Schreiben von Schreib Aktionen" und "removeenvironment Strings" während der Installation oder Entfernung einer Komponente nie angewendet werden, ist die relative Sequenz nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="7db97-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="7db97-115">Aktions Daten Meldungen</span><span class="sxs-lookup"><span data-stu-id="7db97-115">ActionData Messages</span></span>



| <span data-ttu-id="7db97-116">Feld</span><span class="sxs-lookup"><span data-stu-id="7db97-116">Field</span></span> | <span data-ttu-id="7db97-117">Beschreibung der Aktions Daten</span><span class="sxs-lookup"><span data-stu-id="7db97-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db97-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="7db97-118">\[1\]</span></span> | <span data-ttu-id="7db97-119">Der Name der zu ändernden Umgebungsvariablen.</span><span class="sxs-lookup"><span data-stu-id="7db97-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="7db97-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="7db97-120">\[2\]</span></span> | <span data-ttu-id="7db97-121">Der Umgebungsvariablen Wert.</span><span class="sxs-lookup"><span data-stu-id="7db97-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="7db97-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="7db97-122">\[3\]</span></span> | <span data-ttu-id="7db97-123">Hierbei handelt es sich um ein Bitflags-Feld, das die auszuführende Aktion angibt.</span><span class="sxs-lookup"><span data-stu-id="7db97-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="7db97-124">Fügen Sie nur ein Bit für eine primäre Aktion ein.</span><span class="sxs-lookup"><span data-stu-id="7db97-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="7db97-125">In diesem Feld sind möglicherweise mehrere modifiziererbits enthalten.</span><span class="sxs-lookup"><span data-stu-id="7db97-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="7db97-126">Weitere Informationen finden Sie in den folgenden Bitflag-Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="7db97-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="7db97-127">Bitwert</span><span class="sxs-lookup"><span data-stu-id="7db97-127">Bit value</span></span> | <span data-ttu-id="7db97-128">Beschreibung der primären Aktionen</span><span class="sxs-lookup"><span data-stu-id="7db97-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db97-129">0x1</span><span class="sxs-lookup"><span data-stu-id="7db97-129">0x1</span></span>       | <span data-ttu-id="7db97-130">Festlegen.</span><span class="sxs-lookup"><span data-stu-id="7db97-130">Set.</span></span> <span data-ttu-id="7db97-131">Legt den Wert der Umgebungsvariablen in allen Fällen fest.</span><span class="sxs-lookup"><span data-stu-id="7db97-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="7db97-132">Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert durch die Aktion zu einem beliebigen vorhandenen Wert in der Variablen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7db97-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="7db97-133">0x2</span><span class="sxs-lookup"><span data-stu-id="7db97-133">0x2</span></span>       | <span data-ttu-id="7db97-134">Festlegen.</span><span class="sxs-lookup"><span data-stu-id="7db97-134">Set.</span></span> <span data-ttu-id="7db97-135">Legt den Wert fest, wenn die Variable nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7db97-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="7db97-136">Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert durch die Aktion zu einem beliebigen vorhandenen Wert in der Variablen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7db97-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="7db97-137">0x4</span><span class="sxs-lookup"><span data-stu-id="7db97-137">0x4</span></span>       | <span data-ttu-id="7db97-138">Entfernen</span><span class="sxs-lookup"><span data-stu-id="7db97-138">Remove.</span></span> <span data-ttu-id="7db97-139">Entfernt den Wert aus der Variablen.</span><span class="sxs-lookup"><span data-stu-id="7db97-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="7db97-140">Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert aus der vorhandenen Zeichenfolge entfernt, wenn der Wert vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7db97-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="7db97-141">Bitwert</span><span class="sxs-lookup"><span data-stu-id="7db97-141">Bit value</span></span>  | <span data-ttu-id="7db97-142">Beschreibung des Modifizierers</span><span class="sxs-lookup"><span data-stu-id="7db97-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7db97-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="7db97-143">0x20000000</span></span> | <span data-ttu-id="7db97-144">Wenn dieses Bit festgelegt ist, werden Aktionen auf die Umgebungsvariablen des Computers angewendet.</span><span class="sxs-lookup"><span data-stu-id="7db97-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="7db97-145">Wenn dieses Bit nicht festgelegt ist, werden Aktionen auf die Umgebungsvariablen des Benutzers angewendet.</span><span class="sxs-lookup"><span data-stu-id="7db97-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="7db97-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="7db97-146">0x40000000</span></span> | <span data-ttu-id="7db97-147">Anfügen.</span><span class="sxs-lookup"><span data-stu-id="7db97-147">Append.</span></span> <span data-ttu-id="7db97-148">Dieses Bit ist optional.</span><span class="sxs-lookup"><span data-stu-id="7db97-148">This bit is optional.</span></span> <span data-ttu-id="7db97-149">Legen Sie nicht die Anfüge-und Präfix Modifizierer fest.</span><span class="sxs-lookup"><span data-stu-id="7db97-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="7db97-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="7db97-150">0x80000000</span></span> | <span data-ttu-id="7db97-151">Vorsatz.</span><span class="sxs-lookup"><span data-stu-id="7db97-151">Prefix.</span></span> <span data-ttu-id="7db97-152">Dieses Bit ist optional.</span><span class="sxs-lookup"><span data-stu-id="7db97-152">This bit is optional.</span></span> <span data-ttu-id="7db97-153">Legen Sie nicht die Anfüge-und Präfix Modifizierer fest.</span><span class="sxs-lookup"><span data-stu-id="7db97-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




