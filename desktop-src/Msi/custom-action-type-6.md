---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 6 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: d63449e1-231a-4601-b39e-1b69857ccb86
title: Benutzerdefinierter Aktionstyp 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 007cd224caff801592bdde7389cfe3e77820f650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348705"
---
# <a name="custom-action-type-6"></a><span data-ttu-id="85975-103">Benutzerdefinierter Aktionstyp 6</span><span class="sxs-lookup"><span data-stu-id="85975-103">Custom Action Type 6</span></span>

<span data-ttu-id="85975-104">Diese benutzerdefinierte Aktion wird in VBScript geschrieben.</span><span class="sxs-lookup"><span data-stu-id="85975-104">This custom action is written in VBScript.</span></span> <span data-ttu-id="85975-105">Weitere Informationen finden Sie unter [Skripts](scripts.md).</span><span class="sxs-lookup"><span data-stu-id="85975-105">For more information, see [Scripts](scripts.md).</span></span>

## <a name="source"></a><span data-ttu-id="85975-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="85975-106">Source</span></span>

<span data-ttu-id="85975-107">Das Skript wird aus einem temporären binären Stream generiert.</span><span class="sxs-lookup"><span data-stu-id="85975-107">The script is generated from a temporary binary stream.</span></span> <span data-ttu-id="85975-108">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="85975-108">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="85975-109">Die Datenspalte in der binären Tabelle enthält die Streamdaten.</span><span class="sxs-lookup"><span data-stu-id="85975-109">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="85975-110">Für jede Zeile wird ein separater Stream zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="85975-110">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="85975-111">Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="85975-111">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="85975-112">Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="85975-112">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="85975-113">Typwert</span><span class="sxs-lookup"><span data-stu-id="85975-113">Type Value</span></span>

<span data-ttu-id="85975-114">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 32-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85975-114">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 32-bit custom action.</span></span>



| <span data-ttu-id="85975-115">Konstanten</span><span class="sxs-lookup"><span data-stu-id="85975-115">Constants</span></span>                                                               | <span data-ttu-id="85975-116">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="85975-116">Hexadecimal</span></span> | <span data-ttu-id="85975-117">Decimal</span><span class="sxs-lookup"><span data-stu-id="85975-117">Decimal</span></span> |
|-------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="85975-118">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypebinarydata**</span><span class="sxs-lookup"><span data-stu-id="85975-118">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="85975-119">0x006</span><span class="sxs-lookup"><span data-stu-id="85975-119">0x006</span></span>       | <span data-ttu-id="85975-120">6</span><span class="sxs-lookup"><span data-stu-id="85975-120">6</span></span>       |



 

<span data-ttu-id="85975-121">Windows Installer können benutzerdefinierte 64-Bit-Aktionen auf 64-Bit-Betriebssystemen verwenden.</span><span class="sxs-lookup"><span data-stu-id="85975-121">Windows Installer may use 64-bit custom actions on 64-bit operating systems.</span></span> <span data-ttu-id="85975-122">Eine benutzerdefinierte 64-Bit-Aktion, die auf Skripts basiert, muss das **msidbCustomActionType64BitScript** -Bit in den numerischen Typ einschließen.</span><span class="sxs-lookup"><span data-stu-id="85975-122">A 64-bit custom action based on scripts must include the **msidbCustomActionType64BitScript** bit in its numeric type.</span></span> <span data-ttu-id="85975-123">Weitere Informationen finden Sie unter [benutzerdefinierte 64-Bit-Aktionen](64-bit-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="85975-123">For information see [64-bit Custom Actions](64-bit-custom-actions.md).</span></span> <span data-ttu-id="85975-124">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ einer benutzerdefinierten 64-Bit-Aktion anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85975-124">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type of a 64-bit custom action.</span></span>



| <span data-ttu-id="85975-125">Konstanten</span><span class="sxs-lookup"><span data-stu-id="85975-125">Constants</span></span>                                                                                                      | <span data-ttu-id="85975-126">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="85975-126">Hexadecimal</span></span> | <span data-ttu-id="85975-127">Decimal</span><span class="sxs-lookup"><span data-stu-id="85975-127">Decimal</span></span> |
|----------------------------------------------------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="85975-128">**msidbcustomaktiontypevbscript**  +  **msidbcustomaktiontypebinarydata**  +  **msidbCustomActionType64BitScript**</span><span class="sxs-lookup"><span data-stu-id="85975-128">**msidbCustomActionTypeVBScript** + **msidbCustomActionTypeBinaryData** + **msidbCustomActionType64BitScript**</span></span> | <span data-ttu-id="85975-129">0x0001006</span><span class="sxs-lookup"><span data-stu-id="85975-129">0x0001006</span></span>   | <span data-ttu-id="85975-130">4102</span><span class="sxs-lookup"><span data-stu-id="85975-130">4102</span></span>    |



 

## <a name="target"></a><span data-ttu-id="85975-131">Ziel</span><span class="sxs-lookup"><span data-stu-id="85975-131">Target</span></span>

<span data-ttu-id="85975-132">Das Zielfeld der [CustomAction-Tabelle](customaction-table.md) enthält eine optionale Skriptfunktion.</span><span class="sxs-lookup"><span data-stu-id="85975-132">The Target field of the [CustomAction table](customaction-table.md) contains an optional script function.</span></span> <span data-ttu-id="85975-133">Die Verarbeitung sendet zuerst das Skript für die Verarbeitung und ruft dann die optionale Skriptfunktion auf.</span><span class="sxs-lookup"><span data-stu-id="85975-133">Processing first sends the script for parsing and then calls the optional script function.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="85975-134">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="85975-134">Return Processing Options</span></span>

<span data-ttu-id="85975-135">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85975-135">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="85975-136">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="85975-136">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="85975-137">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="85975-137">Execution Scheduling Options</span></span>

<span data-ttu-id="85975-138">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85975-138">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="85975-139">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="85975-139">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="85975-140">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="85975-140">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="85975-141">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="85975-141">In-Script Execution Options</span></span>

<span data-ttu-id="85975-142">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="85975-142">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="85975-143">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="85975-143">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="85975-144">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="85975-144">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="85975-145">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="85975-145">Return Values</span></span>

<span data-ttu-id="85975-146">Optionale Funktionen, die im Skript geschrieben werden, müssen einen der Werte zurückgeben, die unter [Rückgabewerte der benutzerdefinierten Aktionen JScript und VBScript](return-values-of-jscript-and-vbscript-custom-actions.md)beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="85975-146">Optional functions written in script must return one of the values described in [Return Values of JScript and VBScript Custom Actions](return-values-of-jscript-and-vbscript-custom-actions.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="85975-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85975-147">Remarks</span></span>

<span data-ttu-id="85975-148">Eine benutzerdefinierte Aktion, die in JScript oder VBScript geschrieben ist, erfordert die Installation des [**Session-Objekts**](session-object.md).</span><span class="sxs-lookup"><span data-stu-id="85975-148">A custom action that is written in JScript or VBScript requires the installation of the [**Session Object**](session-object.md).</span></span> <span data-ttu-id="85975-149">Das Installationsprogramm fügt das **Sitzungs** Objekt mit der namens *Sitzung* an das Skript an.</span><span class="sxs-lookup"><span data-stu-id="85975-149">The installer attaches the **Session** object to the script with the name *Session*.</span></span> <span data-ttu-id="85975-150">Da das **Sitzungs** Objekt während eines Installations Rollbacks möglicherweise nicht vorhanden ist, muss eine verzögerte benutzerdefinierte Aktion, die im Skript geschrieben ist, eine der Methoden oder Eigenschaften des **Sitzungs** Objekts verwenden, das im Abschnitt Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen für die verzögerte Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md) beschrieben wird, um den Kontext abzurufen.</span><span class="sxs-lookup"><span data-stu-id="85975-150">Because the **Session** object may not exist during an installation rollback, a deferred custom action written in script must use one of the methods or properties of the **Session** object described in the section [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md) to retrieve its context.</span></span>

<span data-ttu-id="85975-151">Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet.</span><span class="sxs-lookup"><span data-stu-id="85975-151">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="85975-152">Der Name sollte das Format "8,3 File Name" verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85975-152">The name should use the 8.3 file name format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="85975-153">Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="85975-153">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="85975-154">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85975-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85975-155">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="85975-155">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 



