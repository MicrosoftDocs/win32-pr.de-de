---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 37 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 1c1e4f4f-1ccb-444c-940a-a1963d97714d
title: Benutzerdefinierter Aktionstyp 37
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30a42d4837af6fe2878f33624251d9c06550855b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042706"
---
# <a name="custom-action-type-37"></a><span data-ttu-id="52379-103">Benutzerdefinierter Aktionstyp 37</span><span class="sxs-lookup"><span data-stu-id="52379-103">Custom Action Type 37</span></span>

<span data-ttu-id="52379-104">Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. b. ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="52379-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="52379-105">Die Windows Installer unterstützt JScript 1,0 nicht.</span><span class="sxs-lookup"><span data-stu-id="52379-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="52379-106">Weitere Informationen finden Sie unter [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="52379-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="52379-107">`Source`</span><span class="sxs-lookup"><span data-stu-id="52379-107">Source</span></span>

<span data-ttu-id="52379-108">Das Quellfeld der [CustomAction-Tabelle](customaction-table.md) enthält den Nullwert.</span><span class="sxs-lookup"><span data-stu-id="52379-108">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="52379-109">Der Skriptcode für die benutzerdefinierte Aktion wird als Zeichenfolge mit literalem Skript Text im Feld Ziel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52379-109">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="52379-110">Typwert</span><span class="sxs-lookup"><span data-stu-id="52379-110">Type Value</span></span>

<span data-ttu-id="52379-111">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52379-111">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="52379-112">Konstanten</span><span class="sxs-lookup"><span data-stu-id="52379-112">Constants</span></span>                                                             | <span data-ttu-id="52379-113">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="52379-113">Hexadecimal</span></span> | <span data-ttu-id="52379-114">Decimal</span><span class="sxs-lookup"><span data-stu-id="52379-114">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="52379-115">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypedirectory**</span><span class="sxs-lookup"><span data-stu-id="52379-115">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="52379-116">0x025</span><span class="sxs-lookup"><span data-stu-id="52379-116">0x025</span></span>       | <span data-ttu-id="52379-117">37</span><span class="sxs-lookup"><span data-stu-id="52379-117">37</span></span>      |



 

<span data-ttu-id="52379-118">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="52379-118">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="52379-119">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="52379-119">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="52379-120">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="52379-120">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="52379-121">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52379-121">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="52379-122">Konstanten</span><span class="sxs-lookup"><span data-stu-id="52379-122">Constants</span></span>                                                                                                    | <span data-ttu-id="52379-123">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="52379-123">Hexadecimal</span></span> | <span data-ttu-id="52379-124">Decimal</span><span class="sxs-lookup"><span data-stu-id="52379-124">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="52379-125">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypedirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="52379-125">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="52379-126">0x0001025</span><span class="sxs-lookup"><span data-stu-id="52379-126">0x0001025</span></span>   | <span data-ttu-id="52379-127">4133</span><span class="sxs-lookup"><span data-stu-id="52379-127">4133</span></span>    |



 

## <a name="target"></a><span data-ttu-id="52379-128">Ziel</span><span class="sxs-lookup"><span data-stu-id="52379-128">Target</span></span>

<span data-ttu-id="52379-129">Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält den Skriptcode für die benutzerdefinierte Aktion als eine Zeichenfolge mit literalem Skript Text.</span><span class="sxs-lookup"><span data-stu-id="52379-129">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="52379-130">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="52379-130">Return Processing Options</span></span>

<span data-ttu-id="52379-131">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52379-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="52379-132">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="52379-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="52379-133">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="52379-133">Execution Scheduling Options</span></span>

<span data-ttu-id="52379-134">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52379-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="52379-135">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="52379-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="52379-136">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="52379-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="52379-137">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="52379-137">In-Script Execution Options</span></span>

<span data-ttu-id="52379-138">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="52379-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="52379-139">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="52379-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="52379-140">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="52379-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="52379-141">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="52379-141">Return Values</span></span>

<span data-ttu-id="52379-142">Dieser benutzerdefinierte Aktionstyp gibt immer Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="52379-142">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="52379-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="52379-143">Remarks</span></span>

<span data-ttu-id="52379-144">Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="52379-144">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="52379-145">Das Installationsprogramm fügt das **Sitzungs Objekt** mit dem Namen "Session" an das Skript an.</span><span class="sxs-lookup"><span data-stu-id="52379-145">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="52379-146">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="52379-146">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="52379-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="52379-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="52379-148">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="52379-148">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



