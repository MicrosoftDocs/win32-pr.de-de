---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 53 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: d024c73e-c2dc-4187-a8ae-ed96dc7c107e
title: Benutzerdefinierter Aktionstyp 53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a016d3b3f5a282567b909215d6ab7b32759417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960066"
---
# <a name="custom-action-type-53"></a><span data-ttu-id="bc2c9-103">Benutzerdefinierter Aktionstyp 53</span><span class="sxs-lookup"><span data-stu-id="bc2c9-103">Custom Action Type 53</span></span>

<span data-ttu-id="bc2c9-104">Diese benutzerdefinierte Aktion wird in JScript geschrieben, z. b. ECMA 262.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-104">This custom action is written in JScript, such as ECMA 262.</span></span> <span data-ttu-id="bc2c9-105">Die Windows Installer unterstützt JScript 1,0 nicht.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-105">Windows Installer does not support JScript 1.0.</span></span> <span data-ttu-id="bc2c9-106">Weitere Informationen finden Sie unter [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="bc2c9-106">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="bc2c9-107">`Source`</span><span class="sxs-lookup"><span data-stu-id="bc2c9-107">Source</span></span>

<span data-ttu-id="bc2c9-108">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Eigenschaftsnamen oder einen Schlüssel für die [Eigenschaften Tabelle](property-table.md) für eine Eigenschaft, die den Skript Text enthält.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-108">The Source field of the [CustomAction table](customaction-table.md) contains a property name or a key to the [Property table](property-table.md) for a property containing the script text.</span></span>

## <a name="type-value"></a><span data-ttu-id="bc2c9-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="bc2c9-109">Type Value</span></span>

<span data-ttu-id="bc2c9-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="bc2c9-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bc2c9-111">Constants</span></span>                                                            | <span data-ttu-id="bc2c9-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="bc2c9-112">Hexadecimal</span></span> | <span data-ttu-id="bc2c9-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="bc2c9-113">Decimal</span></span> |
|----------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="bc2c9-114">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypeproperty**</span><span class="sxs-lookup"><span data-stu-id="bc2c9-114">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty**</span></span> | <span data-ttu-id="bc2c9-115">0x035</span><span class="sxs-lookup"><span data-stu-id="bc2c9-115">0x035</span></span>       | <span data-ttu-id="bc2c9-116">53</span><span class="sxs-lookup"><span data-stu-id="bc2c9-116">53</span></span>      |



 

<span data-ttu-id="bc2c9-117">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="bc2c9-118">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="bc2c9-119">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="bc2c9-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="bc2c9-120">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="bc2c9-121">Konstanten</span><span class="sxs-lookup"><span data-stu-id="bc2c9-121">Constants</span></span>                                                                                                   | <span data-ttu-id="bc2c9-122">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="bc2c9-122">Hexadecimal</span></span> | <span data-ttu-id="bc2c9-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="bc2c9-123">Decimal</span></span> |
|-------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="bc2c9-124">**msidbcustomaktiontypejscript**  +  **msidbcustomaktiontypeproperty**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="bc2c9-124">**msidbCustomActionTypeJScript** + **msidbCustomActionTypeProperty** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="bc2c9-125">0x0001035</span><span class="sxs-lookup"><span data-stu-id="bc2c9-125">0x0001035</span></span>   | <span data-ttu-id="bc2c9-126">4149</span><span class="sxs-lookup"><span data-stu-id="bc2c9-126">4149</span></span>    |



 

## <a name="target"></a><span data-ttu-id="bc2c9-127">Ziel</span><span class="sxs-lookup"><span data-stu-id="bc2c9-127">Target</span></span>

<span data-ttu-id="bc2c9-128">Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-128">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="bc2c9-129">Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-129">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="bc2c9-130">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="bc2c9-130">Return Processing Options</span></span>

<span data-ttu-id="bc2c9-131">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-131">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="bc2c9-132">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="bc2c9-132">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="bc2c9-133">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="bc2c9-133">Execution Scheduling Options</span></span>

<span data-ttu-id="bc2c9-134">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-134">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="bc2c9-135">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-135">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="bc2c9-136">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="bc2c9-136">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="bc2c9-137">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="bc2c9-137">In-Script Execution Options</span></span>

<span data-ttu-id="bc2c9-138">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="bc2c9-139">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-139">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="bc2c9-140">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="bc2c9-140">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="bc2c9-141">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="bc2c9-141">Return Values</span></span>

<span data-ttu-id="bc2c9-142">Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-142">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bc2c9-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc2c9-143">Remarks</span></span>

<span data-ttu-id="bc2c9-144">Eine benutzerdefinierte Aktion, die in JScript geschrieben ist, erfordert das Installations [**Sitzungs**](session-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-144">A custom action that is written in JScript requires the installation [**Session**](session-object.md) object.</span></span> <span data-ttu-id="bc2c9-145">Da das **Sitzungs** Objekt während eines Installations Rollbacks nicht vorhanden ist, verwendet eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben wurde, eine der Methoden, die unter Abrufen [von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="bc2c9-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script uses one of the methods described in [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc2c9-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bc2c9-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc2c9-147">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="bc2c9-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



