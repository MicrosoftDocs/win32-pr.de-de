---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 38 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: bb50fcbf-3de5-4f5a-b799-cec5d68fdd9d
title: Benutzerdefinierter Aktionstyp 38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9372cd5035d27c02feaef3ed455ddeb756c449
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960266"
---
# <a name="custom-action-type-38"></a><span data-ttu-id="f8f21-103">Benutzerdefinierter Aktionstyp 38</span><span class="sxs-lookup"><span data-stu-id="f8f21-103">Custom Action Type 38</span></span>

<span data-ttu-id="f8f21-104">Diese benutzerdefinierte Aktion wird in VBScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="f8f21-105">Siehe auch [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="f8f21-105">See also [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="f8f21-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="f8f21-106">Source</span></span>

<span data-ttu-id="f8f21-107">Das Quellfeld der [CustomAction-Tabelle](customaction-table.md) enthält den Nullwert.</span><span class="sxs-lookup"><span data-stu-id="f8f21-107">The Source field of the [CustomAction table](customaction-table.md) contains the null value.</span></span> <span data-ttu-id="f8f21-108">Der Skriptcode für die benutzerdefinierte Aktion wird als Zeichenfolge mit literalem Skript Text im Feld Ziel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f8f21-108">The script code for the custom action is stored as a string of literal script text in the Target field.</span></span>

## <a name="type-value"></a><span data-ttu-id="f8f21-109">Typwert</span><span class="sxs-lookup"><span data-stu-id="f8f21-109">Type Value</span></span>

<span data-ttu-id="f8f21-110">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-110">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="f8f21-111">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f8f21-111">Constants</span></span>                                                              | <span data-ttu-id="f8f21-112">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f8f21-112">Hexadecimal</span></span> | <span data-ttu-id="f8f21-113">Decimal</span><span class="sxs-lookup"><span data-stu-id="f8f21-113">Decimal</span></span> |
|------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f8f21-114">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypedirectory**</span><span class="sxs-lookup"><span data-stu-id="f8f21-114">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="f8f21-115">0x026</span><span class="sxs-lookup"><span data-stu-id="f8f21-115">0x026</span></span>       | <span data-ttu-id="f8f21-116">38</span><span class="sxs-lookup"><span data-stu-id="f8f21-116">38</span></span>      |



 

<span data-ttu-id="f8f21-117">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f8f21-117">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="f8f21-118">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="f8f21-118">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="f8f21-119">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="f8f21-119">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="f8f21-120">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-120">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="f8f21-121">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f8f21-121">Constants</span></span>                                                                                                     | <span data-ttu-id="f8f21-122">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f8f21-122">Hexadecimal</span></span> | <span data-ttu-id="f8f21-123">Decimal</span><span class="sxs-lookup"><span data-stu-id="f8f21-123">Decimal</span></span> |
|---------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f8f21-124">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypedirectory**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="f8f21-124">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeDirectory** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="f8f21-125">0x0001026</span><span class="sxs-lookup"><span data-stu-id="f8f21-125">0x0001026</span></span>   | <span data-ttu-id="f8f21-126">4134</span><span class="sxs-lookup"><span data-stu-id="f8f21-126">4134</span></span>    |



 

## <a name="target"></a><span data-ttu-id="f8f21-127">Ziel</span><span class="sxs-lookup"><span data-stu-id="f8f21-127">Target</span></span>

<span data-ttu-id="f8f21-128">Das Zielfeld der [Tabelle "CustomAction](customaction-table.md) " enthält den Skriptcode für die benutzerdefinierte Aktion als eine Zeichenfolge mit literalem Skript Text.</span><span class="sxs-lookup"><span data-stu-id="f8f21-128">The Target field of the [CustomAction table](customaction-table.md) contains the script code for the custom action as a string of literal script text.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f8f21-129">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f8f21-129">Return Processing Options</span></span>

<span data-ttu-id="f8f21-130">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-130">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="f8f21-131">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="f8f21-131">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f8f21-132">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f8f21-132">Execution Scheduling Options</span></span>

<span data-ttu-id="f8f21-133">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="f8f21-134">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f8f21-134">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f8f21-135">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f8f21-135">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f8f21-136">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="f8f21-136">In-Script Execution Options</span></span>

<span data-ttu-id="f8f21-137">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f8f21-137">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="f8f21-138">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="f8f21-138">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="f8f21-139">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f8f21-139">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="f8f21-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f8f21-140">Return Values</span></span>

<span data-ttu-id="f8f21-141">Dieser benutzerdefinierte Aktionstyp gibt immer Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="f8f21-141">This custom action type always returns success.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8f21-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f8f21-142">Remarks</span></span>

<span data-ttu-id="f8f21-143">Für eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, ist das install [**Session**](session-object.md) -Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f8f21-143">A custom action that is written in JScript or VBScript requires the install [**Session**](session-object.md) object.</span></span> <span data-ttu-id="f8f21-144">Das Installationsprogramm fügt das **Sitzungs Objekt** mit dem Namen "Session" an das Skript an.</span><span class="sxs-lookup"><span data-stu-id="f8f21-144">The installer attaches the **Session Object** to the script with the name "Session".</span></span> <span data-ttu-id="f8f21-145">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f8f21-145">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f8f21-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8f21-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8f21-147">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="f8f21-147">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



