---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 2 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 79ae0582-c991-4c0a-860b-0f5197ad0c7c
title: Benutzerdefinierter Aktionstyp 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0497b2a76dc2fac7f5e56f7347b50deac867757f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352429"
---
# <a name="custom-action-type-2"></a><span data-ttu-id="f6e9b-103">Benutzerdefinierter Aktionstyp 2</span><span class="sxs-lookup"><span data-stu-id="f6e9b-103">Custom Action Type 2</span></span>

<span data-ttu-id="f6e9b-104">Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="f6e9b-104">This custom action calls an executable launched with a command line.</span></span>

## <a name="source"></a><span data-ttu-id="f6e9b-105">`Source`</span><span class="sxs-lookup"><span data-stu-id="f6e9b-105">Source</span></span>

<span data-ttu-id="f6e9b-106">Die ausführbare Datei wird aus einem temporären binären Stream generiert.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-106">The executable is generated from a temporary binary stream.</span></span> <span data-ttu-id="f6e9b-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="f6e9b-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span> <span data-ttu-id="f6e9b-108">Die Datenspalte in der binären Tabelle enthält die Streamdaten.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="f6e9b-109">Für jede Zeile wird ein separater Stream zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-109">A separate stream is allocated for each row.</span></span>

<span data-ttu-id="f6e9b-110">Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="f6e9b-111">Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="f6e9b-112">Typwert</span><span class="sxs-lookup"><span data-stu-id="f6e9b-112">Type Value</span></span>

<span data-ttu-id="f6e9b-113">Fügen Sie den folgenden Wert in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-113">Include the following value in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="f6e9b-114">Konstanten</span><span class="sxs-lookup"><span data-stu-id="f6e9b-114">Constants</span></span>                                                          | <span data-ttu-id="f6e9b-115">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="f6e9b-115">Hexadecimal</span></span> | <span data-ttu-id="f6e9b-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="f6e9b-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="f6e9b-117">**msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypebinarydata**</span><span class="sxs-lookup"><span data-stu-id="f6e9b-117">**msidbCustomActionTypeExe** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="f6e9b-118">0x002</span><span class="sxs-lookup"><span data-stu-id="f6e9b-118">0x002</span></span>       | <span data-ttu-id="f6e9b-119">2</span><span class="sxs-lookup"><span data-stu-id="f6e9b-119">2</span></span>       |



 

## <a name="target"></a><span data-ttu-id="f6e9b-120">Ziel</span><span class="sxs-lookup"><span data-stu-id="f6e9b-120">Target</span></span>

<span data-ttu-id="f6e9b-121">Die Ziel Spalte der [CustomAction-Tabelle](customaction-table.md) enthält die Befehlszeilen Zeichenfolge für die ausführbare Datei, die in der Quell Spalte benannt ist.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-121">The Target column of the [CustomAction table](customaction-table.md) contains the command line string for the executable named in the Source column.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="f6e9b-122">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f6e9b-122">Return Processing Options</span></span>

<span data-ttu-id="f6e9b-123">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-123">Include optional flag bits in the Type column of the CustomAction table to specify return processing options.</span></span> <span data-ttu-id="f6e9b-124">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="f6e9b-124">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="f6e9b-125">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="f6e9b-125">Execution Scheduling Options</span></span>

<span data-ttu-id="f6e9b-126">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-126">Include optional flag bits in the Type column of the CustomAction table to specify execution scheduling options.</span></span> <span data-ttu-id="f6e9b-127">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-127">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="f6e9b-128">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="f6e9b-128">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="f6e9b-129">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="f6e9b-129">In-Script Execution Options</span></span>

<span data-ttu-id="f6e9b-130">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle CustomAction ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-130">Include optional flag bits in the Type column of the CustomAction table to specify an in-script execution option.</span></span> <span data-ttu-id="f6e9b-131">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-131">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="f6e9b-132">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="f6e9b-132">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="f6e9b-133">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f6e9b-133">Return Values</span></span>

<span data-ttu-id="f6e9b-134">Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-134">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="f6e9b-135">Der Installer interpretiert jeden anderen Rückgabewert als Fehler.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-135">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="f6e9b-136">Wenn Sie Rückgabewerte ignorieren möchten, legen Sie das **msidbcustomaction typecontinue** -Bitflag im type-Feld der CustomAction-Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-136">To ignore return values, set the **msidbCustomActionTypeContinue** bit flag in the Type field of the CustomAction table.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6e9b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f6e9b-137">Remarks</span></span>

<span data-ttu-id="f6e9b-138">Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-138">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="f6e9b-139">Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-139">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

<span data-ttu-id="f6e9b-140">Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-140">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="f6e9b-141">Der Name sollte das 8,3-Format verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-141">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="f6e9b-142">Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="f6e9b-142">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f6e9b-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f6e9b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6e9b-144">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="f6e9b-144">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="f6e9b-145">Ausführbare Dateien</span><span class="sxs-lookup"><span data-stu-id="f6e9b-145">Executable Files</span></span>](executable-files.md)
</dt> </dl>

 

 
