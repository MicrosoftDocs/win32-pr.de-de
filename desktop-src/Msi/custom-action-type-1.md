---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 1 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 277b875f-37f1-4f4d-98ae-7a18131de4f0
title: Benutzerdefinierter Aktionstyp 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72efd083b2cd547ff1dbd7f3bc81a617b5da88e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050485"
---
# <a name="custom-action-type-1"></a><span data-ttu-id="180eb-103">Benutzerdefinierter Aktionstyp 1</span><span class="sxs-lookup"><span data-stu-id="180eb-103">Custom Action Type 1</span></span>

<span data-ttu-id="180eb-104">Diese benutzerdefinierte Aktion ruft eine Dynamic Link Library (dll) auf, die in C oder C++ geschrieben ist.</span><span class="sxs-lookup"><span data-stu-id="180eb-104">This custom action calls a dynamic link library (DLL) written in C or C++.</span></span>

## <a name="source"></a><span data-ttu-id="180eb-105">`Source`</span><span class="sxs-lookup"><span data-stu-id="180eb-105">Source</span></span>

<span data-ttu-id="180eb-106">Die dll wird aus einem temporären binären Stream generiert.</span><span class="sxs-lookup"><span data-stu-id="180eb-106">The DLL is generated from a temporary binary stream.</span></span> <span data-ttu-id="180eb-107">Das Quellfeld der [Tabelle "CustomAction](customaction-table.md) " enthält einen Schlüssel für die [binäre Tabelle](binary-table.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-107">The Source field of the [CustomAction table](customaction-table.md) contains a key to the [Binary table](binary-table.md).</span></span>

<span data-ttu-id="180eb-108">Die Datenspalte in der binären Tabelle enthält die Streamdaten.</span><span class="sxs-lookup"><span data-stu-id="180eb-108">The Data column in the Binary table contains the stream data.</span></span> <span data-ttu-id="180eb-109">Für jede Zeile wird ein separater Stream zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="180eb-109">A separate stream is allocated for each row.</span></span> <span data-ttu-id="180eb-110">Neue Binärdaten können mithilfe von " [**msirecordsetstream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) ", gefolgt von " [**msiviewmodify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) ", aus einer Datei eingefügt werden, um den Datensatz in die Tabelle einzufügen.</span><span class="sxs-lookup"><span data-stu-id="180eb-110">New binary data can be inserted from a file by using [**MsiRecordSetStream**](/windows/desktop/api/Msiquery/nf-msiquery-msirecordsetstreama) followed by [**MsiViewModify**](/windows/desktop/api/Msiquery/nf-msiquery-msiviewmodify) to insert the record into the table.</span></span> <span data-ttu-id="180eb-111">Wenn die benutzerdefinierte Aktion aufgerufen wird, werden die Streamdaten in eine temporäre Datei kopiert, die dann abhängig vom Typ der benutzerdefinierten Aktion verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="180eb-111">When the custom action is invoked, the stream data is copied to a temporary file, which is then processed depending upon the type of custom action.</span></span>

## <a name="type-value"></a><span data-ttu-id="180eb-112">Typwert</span><span class="sxs-lookup"><span data-stu-id="180eb-112">Type Value</span></span>

<span data-ttu-id="180eb-113">Fügen Sie die folgenden Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="180eb-113">Include the following flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify the basic numeric type.</span></span>



| <span data-ttu-id="180eb-114">Konstanten</span><span class="sxs-lookup"><span data-stu-id="180eb-114">Constants</span></span>                                                          | <span data-ttu-id="180eb-115">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="180eb-115">Hexadecimal</span></span> | <span data-ttu-id="180eb-116">Decimal</span><span class="sxs-lookup"><span data-stu-id="180eb-116">Decimal</span></span> |
|--------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="180eb-117">**msidbcustomaktiontypedll**  +  **msidbcustomaktiontypebinarydata**</span><span class="sxs-lookup"><span data-stu-id="180eb-117">**msidbCustomActionTypeDll** + **msidbCustomActionTypeBinaryData**</span></span> | <span data-ttu-id="180eb-118">0x001</span><span class="sxs-lookup"><span data-stu-id="180eb-118">0x001</span></span>       | <span data-ttu-id="180eb-119">1</span><span class="sxs-lookup"><span data-stu-id="180eb-119">1</span></span>       |



 

## <a name="target"></a><span data-ttu-id="180eb-120">Ziel</span><span class="sxs-lookup"><span data-stu-id="180eb-120">Target</span></span>

<span data-ttu-id="180eb-121">Die dll wird über den Einstiegspunkt aufgerufen, der im Feld Ziel der [Tabelle CustomAction](customaction-table.md)benannt ist. dabei wird ein einzelnes Argument übergeben, das das Handle für die aktuelle Installationssitzung ist.</span><span class="sxs-lookup"><span data-stu-id="180eb-121">The DLL is called through the entry point named in the Target field of the [CustomAction table](customaction-table.md), passing a single argument that is the handle to the current install session.</span></span> <span data-ttu-id="180eb-122">Der in der Tabelle angegebene Einstiegspunkt Name muss mit dem aus der DLL exportierten Namen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="180eb-122">The entry point name specified in the table must match that exported from the DLL.</span></span> <span data-ttu-id="180eb-123">Beachten Sie, dass die Einstiegs Funktion nicht von einem angegeben wird. Die DEF-Datei oder eine/Export: Linker-Spezifikation, der Name kann einen vorangeführenden Unterstrich und ein @4 Suffix "" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="180eb-123">Note that if the entry function is not specified by a .DEF file or by a /EXPORT: linker specification, the name may have a leading underscore and a "@4" suffix.</span></span> <span data-ttu-id="180eb-124">Die aufgerufene Funktion muss die Aufruf \_ \_ Konvention stdcall angeben.</span><span class="sxs-lookup"><span data-stu-id="180eb-124">The called function must specify the \_\_stdcall calling convention.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="180eb-125">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="180eb-125">Return Processing Options</span></span>

<span data-ttu-id="180eb-126">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="180eb-126">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify return processing options.</span></span> <span data-ttu-id="180eb-127">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="180eb-127">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="180eb-128">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="180eb-128">Execution Scheduling Options</span></span>

<span data-ttu-id="180eb-129">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="180eb-129">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify execution scheduling options.</span></span> <span data-ttu-id="180eb-130">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="180eb-130">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="180eb-131">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-131">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="180eb-132">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="180eb-132">In-Script Execution Options</span></span>

<span data-ttu-id="180eb-133">Schließen Sie optionale Flagbits in die Spalte Type der [Tabelle CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="180eb-133">Include optional flag bits in the Type column of the [CustomAction table](customaction-table.md) to specify an in-script execution option.</span></span> <span data-ttu-id="180eb-134">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="180eb-134">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="180eb-135">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-135">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="180eb-136">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="180eb-136">Return Values</span></span>

<span data-ttu-id="180eb-137">Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-137">See [Custom Action Return Values](custom-action-return-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="180eb-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="180eb-138">Remarks</span></span>

<span data-ttu-id="180eb-139">Eine benutzerdefinierte Aktion, die eine Dynamic Link Library (dll) aufruft, erfordert ein Handle für die Installationssitzung.</span><span class="sxs-lookup"><span data-stu-id="180eb-139">A custom action that calls a dynamic-link library (DLL) requires a handle to the installation session.</span></span> <span data-ttu-id="180eb-140">Wenn es sich auch um eine benutzerdefinierte Aktion für die verzögerte Ausführung handelt, ist die Sitzung während der Ausführung des Installations Skripts möglicherweise nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="180eb-140">If this is also a deferred execution custom action, the session may no longer exist during execution of the installation script.</span></span> <span data-ttu-id="180eb-141">Informationen dazu, wie eine benutzerdefinierte Aktion dieses Typs Kontextinformationen abrufen kann, finden Sie unter Abrufen von [Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="180eb-141">For information on how a custom action of this type can obtain context information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="180eb-142">Beim Exportieren einer Datenbanktabelle wird jeder Stream als separate Datei in den Unterordner geschrieben, der nach der Tabelle benannt ist. dabei wird der Primärschlüssel als Dateiname (Namensspalte für die binäre Tabelle) mit der Standard Erweiterung ". ibd" verwendet.</span><span class="sxs-lookup"><span data-stu-id="180eb-142">When a database table is exported, each stream is written as a separate file in the subfolder named after the table, using the primary key as the file name (Name column for the Binary table), with a default extension of ".ibd".</span></span> <span data-ttu-id="180eb-143">Der Name sollte das 8,3-Format verwenden, wenn das Dateisystem oder das Versionskontrollsystem keine langen Dateinamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="180eb-143">The name should use the 8.3 format if the file system or version control system does not support long file names.</span></span> <span data-ttu-id="180eb-144">Die permanente Archivdatei ersetzt die Streamdaten durch den verwendeten Dateinamen, damit die Daten beim Importieren der Tabelle gefunden werden können.</span><span class="sxs-lookup"><span data-stu-id="180eb-144">The persistent archive file replaces the stream data with the file name used, so that the data can be located when the table is imported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="180eb-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="180eb-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="180eb-146">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="180eb-146">Custom\_Actions</span></span>](custom-actions.md)
</dt> <dt>

[<span data-ttu-id="180eb-147">Dynamic Link Libraries</span><span class="sxs-lookup"><span data-stu-id="180eb-147">Dynamic-Link Libraries</span></span>](dynamic-link-libraries.md)
</dt> <dt>

[<span data-ttu-id="180eb-148">Abrufen von Kontextinformationen für benutzerdefinierte Aktionen der verzögerten Ausführung</span><span class="sxs-lookup"><span data-stu-id="180eb-148">Obtaining Context Information for Deferred Execution Custom Actions</span></span>](obtaining-context-information-for-deferred-execution-custom-actions.md)
</dt> </dl>

 

 



