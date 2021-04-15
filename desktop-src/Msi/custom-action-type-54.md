---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 54 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: ab348a8e-f5df-4e03-a1b7-1ab1a7fbcb3b
title: Benutzerdefinierter Aktionstyp 54
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 623e8d4ffe955c73ef95a5948aa6e043702a35f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485491"
---
# <a name="custom-action-type-54"></a><span data-ttu-id="173b9-103">Benutzerdefinierter Aktionstyp 54</span><span class="sxs-lookup"><span data-stu-id="173b9-103">Custom Action Type 54</span></span>

<span data-ttu-id="173b9-104">Diese benutzerdefinierte Aktion wird in VBScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="173b9-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="173b9-105">Siehe auch [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="173b9-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="173b9-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="173b9-106">Source</span></span>

<span data-ttu-id="173b9-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Eigenschaftsnamen oder einen Schlüssel für die [Eigenschaften Tabelle](property-table.md) für eine Eigenschaft, die den Skript Text enthält.</span><span class="sxs-lookup"><span data-stu-id="173b9-107">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="173b9-108">Typwert</span><span class="sxs-lookup"><span data-stu-id="173b9-108">Type Value</span></span>

<span data-ttu-id="173b9-109">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="173b9-109">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="173b9-110">Konstanten</span><span class="sxs-lookup"><span data-stu-id="173b9-110">Constants</span></span>                                                             | <span data-ttu-id="173b9-111">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="173b9-111">Hexadecimal</span></span> | <span data-ttu-id="173b9-112">Decimal</span><span class="sxs-lookup"><span data-stu-id="173b9-112">Decimal</span></span> |
|-----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="173b9-113">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypeproperty**</span><span class="sxs-lookup"><span data-stu-id="173b9-113">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="173b9-114">0x036</span><span class="sxs-lookup"><span data-stu-id="173b9-114">0x036</span></span>       | <span data-ttu-id="173b9-115">54</span><span class="sxs-lookup"><span data-stu-id="173b9-115">54</span></span>      |



 

<span data-ttu-id="173b9-116">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="173b9-116">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="173b9-117">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="173b9-117">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="173b9-118">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="173b9-118">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="173b9-119">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="173b9-119">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="173b9-120">Konstanten</span><span class="sxs-lookup"><span data-stu-id="173b9-120">Constants</span></span>                                                                                                    | <span data-ttu-id="173b9-121">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="173b9-121">Hexadecimal</span></span> | <span data-ttu-id="173b9-122">Decimal</span><span class="sxs-lookup"><span data-stu-id="173b9-122">Decimal</span></span> |
|--------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="173b9-123">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypeproperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="173b9-123">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="173b9-124">0x0001036</span><span class="sxs-lookup"><span data-stu-id="173b9-124">0x0001036</span></span>   | <span data-ttu-id="173b9-125">4150</span><span class="sxs-lookup"><span data-stu-id="173b9-125">4150</span></span>    |



 

## <a name="target"></a><span data-ttu-id="173b9-126">Ziel</span><span class="sxs-lookup"><span data-stu-id="173b9-126">Target</span></span>

<span data-ttu-id="173b9-127">Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion.</span><span class="sxs-lookup"><span data-stu-id="173b9-127">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="173b9-128">Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="173b9-128">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="173b9-129">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="173b9-129">Return Processing Options</span></span>

<span data-ttu-id="173b9-130">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="173b9-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="173b9-131">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="173b9-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="173b9-132">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="173b9-132">Execution Scheduling Options</span></span>

<span data-ttu-id="173b9-133">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="173b9-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="173b9-134">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="173b9-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="173b9-135">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="173b9-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="173b9-136">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="173b9-136">In-Script Execution Options</span></span>

<span data-ttu-id="173b9-137">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="173b9-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="173b9-138">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="173b9-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="173b9-139">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="173b9-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="173b9-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="173b9-140">Return Values</span></span>

<span data-ttu-id="173b9-141">Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="173b9-141">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="173b9-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="173b9-142">Remarks</span></span>

<span data-ttu-id="173b9-143">Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="173b9-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="173b9-144">Das Installationsprogramm fügt das **Sitzungs Objekt** mit der namens *Sitzung* an das Skript an.</span><span class="sxs-lookup"><span data-stu-id="173b9-144">The installer attaches the **Session Object** to the script with the name *Session*.</span></span> <span data-ttu-id="173b9-145">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="173b9-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="173b9-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="173b9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="173b9-147">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="173b9-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



