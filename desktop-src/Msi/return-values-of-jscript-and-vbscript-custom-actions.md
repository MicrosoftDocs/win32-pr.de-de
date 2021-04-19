---
description: In JScript oder Visual Basic geschriebene benutzerdefinierte Aktionen, Scripting Edition (VBScript) können eine optionale Funktion aufzurufen. Diese Funktionen müssen einen der in der folgenden Tabelle dargestellten Werte zurückgeben.
ms.assetid: f05d0b94-e79e-440e-9f2b-99fe0e9e2646
title: Rückgabewerte von benutzerdefinierten JScript-und VBScript-Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cae96ecba320914b7b00dfa718deffdd56ae7eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355592"
---
# <a name="return-values-of-jscript-and-vbscript-custom-actions"></a><span data-ttu-id="880af-104">Rückgabewerte von benutzerdefinierten JScript-und VBScript-Aktionen</span><span class="sxs-lookup"><span data-stu-id="880af-104">Return Values of JScript and VBScript Custom Actions</span></span>

<span data-ttu-id="880af-105">In JScript oder Visual Basic geschriebene benutzerdefinierte Aktionen, Scripting Edition (VBScript) können eine optionale Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="880af-105">Custom actions written in JScript or Visual Basic, Scripting Edition (VBScript) can call an optional function.</span></span> <span data-ttu-id="880af-106">Diese Funktionen müssen einen der in der folgenden Tabelle dargestellten Werte zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="880af-106">These functions must return one of the values shown in the following table.</span></span>



| <span data-ttu-id="880af-107">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="880af-107">Return value</span></span>              | <span data-ttu-id="880af-108">Wert</span><span class="sxs-lookup"><span data-stu-id="880af-108">Value</span></span>        | <span data-ttu-id="880af-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="880af-109">Description</span></span>                                                                                                |
|---------------------------|--------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="880af-110">msidoaction Status-NoAction</span><span class="sxs-lookup"><span data-stu-id="880af-110">msiDoActionStatusNoAction</span></span> | <span data-ttu-id="880af-111">0</span><span class="sxs-lookup"><span data-stu-id="880af-111">0</span></span>            | <span data-ttu-id="880af-112">Die Aktion wurde nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="880af-112">Action not executed.</span></span>                                                                                       |
| <span data-ttu-id="880af-113">msidoaktionstatus-Erfolg</span><span class="sxs-lookup"><span data-stu-id="880af-113">msiDoActionStatusSuccess</span></span>  | <span data-ttu-id="880af-114">IDOK = 1</span><span class="sxs-lookup"><span data-stu-id="880af-114">IDOK = 1</span></span>     | <span data-ttu-id="880af-115">Die Aktion wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="880af-115">Action completed successfully.</span></span>                                                                             |
| <span data-ttu-id="880af-116">msidoaktionstatus ususerexit</span><span class="sxs-lookup"><span data-stu-id="880af-116">msiDoActionStatusUserExit</span></span> | <span data-ttu-id="880af-117">IDCANCEL = 2</span><span class="sxs-lookup"><span data-stu-id="880af-117">IDCANCEL = 2</span></span> | <span data-ttu-id="880af-118">Vorzeitige Beendigung durch den Benutzer.</span><span class="sxs-lookup"><span data-stu-id="880af-118">Premature termination by user.</span></span>                                                                             |
| <span data-ttu-id="880af-119">msidoaktionstatus-Fehler</span><span class="sxs-lookup"><span data-stu-id="880af-119">msiDoActionStatusFailure</span></span>  | <span data-ttu-id="880af-120">Idabort = 3</span><span class="sxs-lookup"><span data-stu-id="880af-120">IDABORT = 3</span></span>  | <span data-ttu-id="880af-121">Nicht BEHEB barer Fehler.</span><span class="sxs-lookup"><span data-stu-id="880af-121">Unrecoverable error.</span></span> <span data-ttu-id="880af-122">Wird zurückgegeben, wenn während der Verarbeitung oder Ausführung von JScript oder VBScript ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="880af-122">Returned if there is an error during parsing or execution of the JScript or VBScript.</span></span> |
| <span data-ttu-id="880af-123">msidoaktionstatus-Suspend</span><span class="sxs-lookup"><span data-stu-id="880af-123">msiDoActionStatusSuspend</span></span>  | <span data-ttu-id="880af-124">Idretry = 4</span><span class="sxs-lookup"><span data-stu-id="880af-124">IDRETRY = 4</span></span>  | <span data-ttu-id="880af-125">Angehaltene Sequenz, die später fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="880af-125">Suspended sequence to be resumed later.</span></span>                                                                    |
| <span data-ttu-id="880af-126">msidoaktionstatus "beendet"</span><span class="sxs-lookup"><span data-stu-id="880af-126">msiDoActionStatusFinished</span></span> | <span data-ttu-id="880af-127">IDIGNORE = 5</span><span class="sxs-lookup"><span data-stu-id="880af-127">IDIGNORE = 5</span></span> | <span data-ttu-id="880af-128">Verbleibende Aktionen überspringen.</span><span class="sxs-lookup"><span data-stu-id="880af-128">Skip remaining actions.</span></span> <span data-ttu-id="880af-129">Kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="880af-129">Not an error.</span></span>                                                                      |



 

<span data-ttu-id="880af-130">Beachten Sie, dass Windows Installer die Rückgabewerte aller Aktionen übersetzt, wenn der Rückgabewert in die Protokolldatei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="880af-130">Note that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="880af-131">Wenn der Rückgabewert der Aktion z. b. als 1 (eins) in der Protokolldatei angezeigt wird, bedeutet dies, dass die Aktion msidoaction Status-Success zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="880af-131">For example, if the action return value appears as 1 (one) in the log file, this means that the action returned msiDoActionStatusSuccess.</span></span> <span data-ttu-id="880af-132">Weitere Informationen zu dieser Übersetzung finden Sie [unter Protokollieren von Aktions Rückgabe Werten](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="880af-132">For more information about this translation see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="880af-133">Wenn Sie einen anderen Wert als Success aus einer benutzerdefinierten Skript Aktion zurückgeben möchten, müssen Sie für die benutzerdefinierte Aktion ein Funktions Ziel verwenden.</span><span class="sxs-lookup"><span data-stu-id="880af-133">To return a value other than success from a script custom action, you must use a function target for the custom action.</span></span> <span data-ttu-id="880af-134">Die Zielfunktion wird in der Ziel Spalte der [CustomAction-Tabelle](customaction-table.md)angegeben.</span><span class="sxs-lookup"><span data-stu-id="880af-134">The target function is specified in the Target column of the [CustomAction Table](customaction-table.md).</span></span>

<span data-ttu-id="880af-135">Im folgenden Skript Beispiel wird gezeigt, wie Sie Erfolg oder Fehler von einer benutzerdefinierten VBScript-Aktion zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="880af-135">The following script example shows you how to return success or failure from a VBScript custom action.</span></span>


```VB
Function MyVBScriptCA()

    If Session.Property("CustomErrorStatus") <> "0" Then
        'return error
        MyVBScriptCA = 3
        Exit Function
    End If

    ' return success
    MyVBScriptCA = 1
    Exit Function

End Function
```



<span data-ttu-id="880af-136">Wenn dieses VBScript als MyCA.vbs in die [binäre Tabelle](binary-table.md) des Installationspakets eingebettet wurde, lautet der [CustomAction-Tabellen](customaction-table.md) Eintrag für das Skript wie folgt:</span><span class="sxs-lookup"><span data-stu-id="880af-136">If this VBScript were embedded in the [Binary table](binary-table.md) of the installation package as MyCA.vbs, the [CustomAction Table](customaction-table.md) entry for the script would be the following:</span></span>



| <span data-ttu-id="880af-137">Aktion</span><span class="sxs-lookup"><span data-stu-id="880af-137">Action</span></span>         | <span data-ttu-id="880af-138">type</span><span class="sxs-lookup"><span data-stu-id="880af-138">Type</span></span> | <span data-ttu-id="880af-139">`Source`</span><span class="sxs-lookup"><span data-stu-id="880af-139">Source</span></span>   | <span data-ttu-id="880af-140">Ziel</span><span class="sxs-lookup"><span data-stu-id="880af-140">Target</span></span>       |
|----------------|------|----------|--------------|
| <span data-ttu-id="880af-141">MyCustomAction</span><span class="sxs-lookup"><span data-stu-id="880af-141">MyCustomAction</span></span> | <span data-ttu-id="880af-142">6</span><span class="sxs-lookup"><span data-stu-id="880af-142">6</span></span>    | <span data-ttu-id="880af-143">MyCA.vbs</span><span class="sxs-lookup"><span data-stu-id="880af-143">MyCA.vbs</span></span> | <span data-ttu-id="880af-144">Myvbscriptca</span><span class="sxs-lookup"><span data-stu-id="880af-144">MyVBScriptCA</span></span> |



 

 

 



