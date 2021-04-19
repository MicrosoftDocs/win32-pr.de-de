---
description: Entwickler von Windows Installer Paketen können einen benutzerdefinierten Aktionstyp 34 verwenden, wenn die Standard Aktionen nicht ausreichen, um die Installation auszuführen.
ms.assetid: 4d0e4f01-0530-4202-bc78-b6e52670b8e5
title: Benutzerdefinierter Aktionstyp 34
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76ba17c9a4dc5b35d8d03e9cca2707079cb15bf6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373195"
---
# <a name="custom-action-type-34"></a><span data-ttu-id="1d745-103">Benutzerdefinierter Aktionstyp 34</span><span class="sxs-lookup"><span data-stu-id="1d745-103">Custom Action Type 34</span></span>

<span data-ttu-id="1d745-104">Diese benutzerdefinierte Aktion ruft eine ausführbare Datei auf, die mit einer Befehlszeile gestartet wurde</span><span class="sxs-lookup"><span data-stu-id="1d745-104">This custom action calls an executable launched with a command line.</span></span> <span data-ttu-id="1d745-105">Weitere Informationen finden Sie unter [ausführbare Dateien](executable-files.md).</span><span class="sxs-lookup"><span data-stu-id="1d745-105">For more information, see [Executable Files](executable-files.md).</span></span>

## <a name="source"></a><span data-ttu-id="1d745-106">`Source`</span><span class="sxs-lookup"><span data-stu-id="1d745-106">Source</span></span>

<span data-ttu-id="1d745-107">Die ausführbare Datei wird aus einer Datei generiert.</span><span class="sxs-lookup"><span data-stu-id="1d745-107">The executable is generated from a file.</span></span> <span data-ttu-id="1d745-108">Das Quellfeld der Tabelle " [CustomAction](customaction-table.md) " enthält einen Schlüssel in der [Verzeichnis](directory-table.md) Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1d745-108">The Source field of the [CustomAction](customaction-table.md) table contains a key into the [Directory](directory-table.md) table.</span></span> <span data-ttu-id="1d745-109">Der Verzeichnis Tabelleneintrag, auf den verwiesen wird, wird verwendet, um den vollständigen Pfad zu einem Arbeitsverzeichnis aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="1d745-109">The referenced Directory table entry is used to resolve the full path to a working directory.</span></span> <span data-ttu-id="1d745-110">Dies ist nicht erforderlich, um den Pfad zu dem Verzeichnis zu sein, das die ausführbare Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="1d745-110">This is not required to be the path to the directory containing the executable.</span></span>

## <a name="type-value"></a><span data-ttu-id="1d745-111">Typwert</span><span class="sxs-lookup"><span data-stu-id="1d745-111">Type Value</span></span>

<span data-ttu-id="1d745-112">Fügen Sie den folgenden Wert in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um den grundlegenden numerischen Typ anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d745-112">Include the following value in the Type column of the [CustomAction](customaction-table.md) table to specify the basic numeric type.</span></span>



| <span data-ttu-id="1d745-113">Konstanten</span><span class="sxs-lookup"><span data-stu-id="1d745-113">Constants</span></span>                                                         | <span data-ttu-id="1d745-114">Hexadezimal</span><span class="sxs-lookup"><span data-stu-id="1d745-114">Hexadecimal</span></span> | <span data-ttu-id="1d745-115">Decimal</span><span class="sxs-lookup"><span data-stu-id="1d745-115">Decimal</span></span> |
|-------------------------------------------------------------------|-------------|---------|
| <span data-ttu-id="1d745-116">**msidbcustomaktiontypeexe**  +  **msidbcustomaktiontypedirectory**</span><span class="sxs-lookup"><span data-stu-id="1d745-116">**msidbCustomActionTypeExe** + **msidbCustomActionTypeDirectory**</span></span> | <span data-ttu-id="1d745-117">0x022</span><span class="sxs-lookup"><span data-stu-id="1d745-117">0x022</span></span>       | <span data-ttu-id="1d745-118">34</span><span class="sxs-lookup"><span data-stu-id="1d745-118">34</span></span>      |



 

## <a name="target"></a><span data-ttu-id="1d745-119">Ziel</span><span class="sxs-lookup"><span data-stu-id="1d745-119">Target</span></span>

<span data-ttu-id="1d745-120">Die Ziel Spalte der Tabelle [CustomAction](customaction-table.md) enthält den vollständigen Pfad und den Namen der ausführbaren Datei, gefolgt von optionalen Argumenten für die ausführbare Datei.</span><span class="sxs-lookup"><span data-stu-id="1d745-120">The Target column of the [CustomAction](customaction-table.md) table contains the full path and name of the executable file followed by optional arguments to the executable.</span></span> <span data-ttu-id="1d745-121">Der vollständige Pfad und Name der ausführbaren Datei ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1d745-121">The full path and name to the executable file is required.</span></span> <span data-ttu-id="1d745-122">Anführungszeichen müssen in Bezug auf lange Dateinamen oder-Pfade verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1d745-122">Quotation marks must be used around long file names or paths.</span></span> <span data-ttu-id="1d745-123">Der Wert wird als [formatierter](formatted.md) Text behandelt und kann Verweise auf Eigenschaften, Dateien, Verzeichnisse oder andere formatierte Text Attribute enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d745-123">The value is treated as [formatted](formatted.md) text and may contain references to properties, files, directories, or other formatted text attributes.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="1d745-124">Rückgabe Verarbeitungsoptionen</span><span class="sxs-lookup"><span data-stu-id="1d745-124">Return Processing Options</span></span>

<span data-ttu-id="1d745-125">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um die Rückgabe Verarbeitungsoptionen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d745-125">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify return processing options.</span></span> <span data-ttu-id="1d745-126">Eine Beschreibung der Optionen und Werte finden Sie unter " [benutzerdefinierte Aktion: Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md)".</span><span class="sxs-lookup"><span data-stu-id="1d745-126">For a description of the options and the values, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="1d745-127">Ausführungszeit Planungsoptionen</span><span class="sxs-lookup"><span data-stu-id="1d745-127">Execution Scheduling Options</span></span>

<span data-ttu-id="1d745-128">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um Optionen für die Ausführungsplanung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d745-128">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify execution scheduling options.</span></span> <span data-ttu-id="1d745-129">Diese Optionen steuern die mehrfache Ausführung von benutzerdefinierten Aktionen.</span><span class="sxs-lookup"><span data-stu-id="1d745-129">These options control the multiple execution of custom actions.</span></span> <span data-ttu-id="1d745-130">Eine Beschreibung der Optionen finden Sie unter Optionen für die [Ausführungsplanung für benutzerdefinierte Aktionen](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="1d745-130">For a description of the options, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="1d745-131">Ausführungs Optionen für In-Script</span><span class="sxs-lookup"><span data-stu-id="1d745-131">In-Script Execution Options</span></span>

<span data-ttu-id="1d745-132">Schließen Sie optionale Flagbits in die Spalte Type der Tabelle [CustomAction](customaction-table.md) ein, um eine in-Script-Ausführungs Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="1d745-132">Include optional flag bits in the Type column of the [CustomAction](customaction-table.md) table to specify an in-script execution option.</span></span> <span data-ttu-id="1d745-133">Diese Optionen kopieren den Aktions Code in das Ausführungs-, Rollback-oder Commit-Skript.</span><span class="sxs-lookup"><span data-stu-id="1d745-133">These options copy the action code into the execution, rollback, or commit script.</span></span> <span data-ttu-id="1d745-134">Eine Beschreibung der Optionen finden Sie unter [benutzerdefinierte Aktion In-Script Ausführungs Optionen](custom-action-in-script-execution-options.md).</span><span class="sxs-lookup"><span data-stu-id="1d745-134">For a description of the options, see [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).</span></span>

## <a name="return-values"></a><span data-ttu-id="1d745-135">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1d745-135">Return Values</span></span>

<span data-ttu-id="1d745-136">Benutzerdefinierte Aktionen, die [ausführbare Dateien](executable-files.md) sind, müssen für Erfolg den Wert 0 zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="1d745-136">Custom actions that are [executable files](executable-files.md) must return a value of 0 for success.</span></span> <span data-ttu-id="1d745-137">Der Installer interpretiert jeden anderen Rückgabewert als Fehler.</span><span class="sxs-lookup"><span data-stu-id="1d745-137">The installer interprets any other return value as failure.</span></span> <span data-ttu-id="1d745-138">Zum Ignorieren von Rückgabe Werten legen Sie das Bitflag " **msidbcustomaction typecontinue** " im type-Feld der Tabelle " [CustomAction](customaction-table.md) " fest.</span><span class="sxs-lookup"><span data-stu-id="1d745-138">To ignore return values set the **msidbCustomActionTypeContinue** bit flag in the Type field of the [CustomAction](customaction-table.md) table.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d745-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d745-139">Remarks</span></span>

<span data-ttu-id="1d745-140">Eine benutzerdefinierte Aktion, die eine ausführbare Datei startet, benötigt eine Befehlszeile, die häufig Eigenschaften enthält, die dynamisch festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="1d745-140">A custom action that launches an executable takes a command line, which commonly contains properties that are designated dynamically.</span></span> <span data-ttu-id="1d745-141">Wenn es sich auch um eine [benutzerdefinierte Aktion für die verzögerte Ausführung](deferred-execution-custom-actions.md)handelt, verwendet das Installationsprogramm [**zum Erstellen**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) des Prozesses den Prozess, wenn [**die benutzerdefinierte**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) Aktion aus dem Installationsskript aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1d745-141">If this is also a [deferred execution custom action](deferred-execution-custom-actions.md), the installer uses [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) or [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) to create the process when the custom action is invoked from the installation script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d745-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1d745-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d745-143">Benutzerdefinierte \_ Aktionen</span><span class="sxs-lookup"><span data-stu-id="1d745-143">Custom\_Actions</span></span>](custom-actions.md)
</dt> </dl>

 

 
