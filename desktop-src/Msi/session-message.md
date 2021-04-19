---
description: Die Message-Methode des Session-Objekts führt alle aktivierten Protokollierungs Vorgänge aus und führt die Ausführung für das UI-Handlerobjekt aus, das der Engine zugeordnet ist. Die Protokollierung kann selektiv für verschiedene Nachrichten Typen aktiviert werden. Siehe EnableLog-Methode.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. Message-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371773"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="d4a99-105">Session. Message-Methode</span><span class="sxs-lookup"><span data-stu-id="d4a99-105">Session.Message method</span></span>

<span data-ttu-id="d4a99-106">Die **Message** -Methode des [**Session**](session-object.md) -Objekts führt alle aktivierten Protokollierungs Vorgänge aus und führt die Ausführung für das UI-Handlerobjekt aus, das der Engine zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d4a99-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="d4a99-107">Die Protokollierung kann selektiv für verschiedene Nachrichten Typen aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d4a99-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="d4a99-108">Siehe [**EnableLog**](installer-enablelog.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d4a99-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="d4a99-109">Wenn das Daten Satz Feld 0 eine Formatierungs Zeichenfolge enthält, wird es verwendet, um die Daten in den anderen Feldern zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="d4a99-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="d4a99-110">Wenn es sich bei der Nachricht um einen Fehler, eine Warnung oder eine Benutzer Meldung handelt, wird versucht, eine Nachrichten Vorlage in der Fehler Tabelle für die aktuelle Datenbank mithilfe der Fehlernummer zu suchen, die in Feld 1 des Datensatzes für Nachrichten Typen und Rückgabewerte gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d4a99-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4a99-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4a99-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="d4a99-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4a99-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4a99-113">*Art*</span><span class="sxs-lookup"><span data-stu-id="d4a99-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a99-114">Der *Kind* -Parameter muss einer der folgenden Werte sein.</span><span class="sxs-lookup"><span data-stu-id="d4a99-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="d4a99-115">Wenn Sie ein Meldungs Feld mit pushschaltflächen und Symbolen anzeigen möchten, berechnen Sie den Wert der *Art* , indem Sie die von [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) und [**messageboxex**](/windows/win32/api/winuser/nf-winuser-messageboxexa) verwendeten Standardformate für Meldungs Felder zu **msimessagetypeerror**, **msimessagetypewarning** oder **msimessagetypeuser** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="d4a99-116">Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="d4a99-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="d4a99-117">Konstante</span><span class="sxs-lookup"><span data-stu-id="d4a99-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="d4a99-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d4a99-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="d4a99-119"><dt>**msimessagetypefatalexit**</dt> - <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="d4a99-120">Vorzeitige Beendigung, möglicherweise schwerwiegender Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d4a99-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="d4a99-121"><dt>**msimessagetypeerror**</dt> - <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="d4a99-122">Formatierte Fehlermeldung, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4a99-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="d4a99-123"><dt>**msimessagetypewarning**</dt> - <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="d4a99-124">Formatierte Warnmeldung, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4a99-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="d4a99-125"><dt> **msimessagetypeuser**</dt> - <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="d4a99-126">Benutzer Anforderungs Nachricht, \[ 1 \] ist Nachrichtennummer in der [Fehler Tabelle](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="d4a99-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="d4a99-127"><dt>**msimessagetypeingefo**</dt> - <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="d4a99-128">Informative Meldung für das Protokoll, die nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4a99-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="d4a99-129"><dt>**msimessagetypefilesinuse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="d4a99-130">Die Liste der zu verwendenden Dateien, die ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="d4a99-131"><dt>**msimessagetyperesolvesource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="d4a99-132">Anforderung zum Ermitteln eines gültigen Quell Speicher Orts.</span><span class="sxs-lookup"><span data-stu-id="d4a99-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="d4a99-133"><dt>**msimessagetypeouesf Disk Space**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="d4a99-134">Nicht genügend Speicherplatz Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d4a99-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="d4a99-135"><dt>**msimessagetypeactionstart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="d4a99-136">Start der Aktion, \[ 1 \] Aktionsname, \[ 2 \] Beschreibung, \[ 3 \] Vorlage für Action Data Messages.</span><span class="sxs-lookup"><span data-stu-id="d4a99-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="d4a99-137"><dt>**msimessagetypeactiondata**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="d4a99-138">Aktions Daten.</span><span class="sxs-lookup"><span data-stu-id="d4a99-138">Action data.</span></span> <span data-ttu-id="d4a99-139">Daten Satz Felder entsprechen der Vorlage der Aktions Start Nachricht.</span><span class="sxs-lookup"><span data-stu-id="d4a99-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="d4a99-140"><dt>**msimessagetypeprogress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="d4a99-141">Informationen zur Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="d4a99-141">Progress bar information.</span></span> <span data-ttu-id="d4a99-142">Weitere Informationen finden Sie unter Beschreibung der Daten Satz Felder unten.</span><span class="sxs-lookup"><span data-stu-id="d4a99-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="d4a99-143"><dt> **msimessagetypecommondata**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="d4a99-144">Um die Schaltfläche Abbrechen zu aktivieren, legen Sie \[ 1 \] bis 2 und \[ 2 \] auf 1 fest.</span><span class="sxs-lookup"><span data-stu-id="d4a99-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="d4a99-145">So deaktivieren Sie die Schaltfläche "Abbrechen" für \[ 1 \] bis 2 und \[ 2 \] bis 0</span><span class="sxs-lookup"><span data-stu-id="d4a99-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="d4a99-146">*record*</span><span class="sxs-lookup"><span data-stu-id="d4a99-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="d4a99-147">Erforderliches [**Daten Satz**](record-object.md) Objekt, das ein Nachrichten spezifisches Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="d4a99-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4a99-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4a99-148">Return value</span></span>



| <span data-ttu-id="d4a99-149">Konstante</span><span class="sxs-lookup"><span data-stu-id="d4a99-149">Constant</span></span>                                                                                              | <span data-ttu-id="d4a99-150">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a99-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="d4a99-151"><dt>**msimessagestatus userror**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="d4a99-152">-1</span><span class="sxs-lookup"><span data-stu-id="d4a99-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="d4a99-153"><dt>**msimessagestatus-None**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="d4a99-154">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-155"><dt>**msimessagestatuusok**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="d4a99-156">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-157"><dt>**msimessagestatus Cancel**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="d4a99-158">2</span><span class="sxs-lookup"><span data-stu-id="d4a99-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-159"><dt>**msimessagestatus-Abort**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="d4a99-160">3</span><span class="sxs-lookup"><span data-stu-id="d4a99-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-161"><dt>**msimessagestatus-Wiederholungsversuch**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="d4a99-162">4</span><span class="sxs-lookup"><span data-stu-id="d4a99-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-163"><dt>**msimessagestatusignore**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="d4a99-164">5</span><span class="sxs-lookup"><span data-stu-id="d4a99-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-165"><dt>**msimessagestatusyes**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="d4a99-166">6</span><span class="sxs-lookup"><span data-stu-id="d4a99-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="d4a99-167"><dt>**msimessagestatus-Nr**</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="d4a99-168">7</span><span class="sxs-lookup"><span data-stu-id="d4a99-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="d4a99-169">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4a99-169">Remarks</span></span>

<span data-ttu-id="d4a99-170">**Nachrichten Daten Satz Felder**</span><span class="sxs-lookup"><span data-stu-id="d4a99-170">**Message Record Fields**</span></span>

<span data-ttu-id="d4a99-171">Im folgenden werden die Definitionen der Daten Satz Felder beschrieben, wenn msimessagetypeprogress als Nachrichtentyp übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4a99-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="d4a99-172">Feld 1 gibt den Typ der Statusmeldung an.</span><span class="sxs-lookup"><span data-stu-id="d4a99-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="d4a99-173">Die Bedeutung der anderen Felder hängt von dem Wert in diesem Feld ab.</span><span class="sxs-lookup"><span data-stu-id="d4a99-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="d4a99-174">Die möglichen Werte, die in Feld 1 festgelegt werden können, lauten wie folgt.</span><span class="sxs-lookup"><span data-stu-id="d4a99-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="d4a99-175">Nachrichtenname</span><span class="sxs-lookup"><span data-stu-id="d4a99-175">Message name</span></span>     | <span data-ttu-id="d4a99-176">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a99-176">Value</span></span> | <span data-ttu-id="d4a99-177">Beschreibung von Feld 1</span><span class="sxs-lookup"><span data-stu-id="d4a99-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-178">Masterreset</span><span class="sxs-lookup"><span data-stu-id="d4a99-178">MasterReset</span></span>      | <span data-ttu-id="d4a99-179">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-179">0</span></span>     | <span data-ttu-id="d4a99-180">Setzt die Statusanzeige zurück und legt die erwartete Gesamtzahl der Ticks in der Leiste fest.</span><span class="sxs-lookup"><span data-stu-id="d4a99-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="d4a99-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="d4a99-181">ActionInfo</span></span>       | <span data-ttu-id="d4a99-182">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-182">1</span></span>     | <span data-ttu-id="d4a99-183">Stellt Informationen im Zusammenhang mit Fortschrittsmeldungen bereit, die von der aktuellen Aktion gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="d4a99-184">Progressreport</span><span class="sxs-lookup"><span data-stu-id="d4a99-184">ProgressReport</span></span>   | <span data-ttu-id="d4a99-185">2</span><span class="sxs-lookup"><span data-stu-id="d4a99-185">2</span></span>     | <span data-ttu-id="d4a99-186">Erhöht die Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="d4a99-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="d4a99-187">Progressaddition</span><span class="sxs-lookup"><span data-stu-id="d4a99-187">ProgressAddition</span></span> | <span data-ttu-id="d4a99-188">3</span><span class="sxs-lookup"><span data-stu-id="d4a99-188">3</span></span>     | <span data-ttu-id="d4a99-189">Ermöglicht einer Aktion (z. b. CustomAction), Ticks zur erwarteten Gesamtzahl der Statusanzeige hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="d4a99-190">Die Bedeutung von Feld 2 hängt wie folgt von dem Wert in Feld 1 ab.</span><span class="sxs-lookup"><span data-stu-id="d4a99-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d4a99-191">Wert für Feld 1</span><span class="sxs-lookup"><span data-stu-id="d4a99-191">Field 1 value</span></span> | <span data-ttu-id="d4a99-192">Beschreibung von Feld 2</span><span class="sxs-lookup"><span data-stu-id="d4a99-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-193">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-193">0</span></span>             | <span data-ttu-id="d4a99-194">Erwartete Gesamtzahl der Ticks in der Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="d4a99-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="d4a99-195">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-195">1</span></span>             | <span data-ttu-id="d4a99-196">Anzahl der Ticks, die die Statusanzeige für jede Aktions Daten Nachricht verschiebt.</span><span class="sxs-lookup"><span data-stu-id="d4a99-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="d4a99-197">Dieses Feld wird ignoriert, wenn Feld 3 den Wert 0 hat.</span><span class="sxs-lookup"><span data-stu-id="d4a99-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="d4a99-198">2</span><span class="sxs-lookup"><span data-stu-id="d4a99-198">2</span></span>             | <span data-ttu-id="d4a99-199">Anzahl der Ticks, die die Statusanzeige verschoben hat.</span><span class="sxs-lookup"><span data-stu-id="d4a99-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="d4a99-200">3</span><span class="sxs-lookup"><span data-stu-id="d4a99-200">3</span></span>             | <span data-ttu-id="d4a99-201">Anzahl der Ticks, die dem erwarteten Gesamtfortschritt hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="d4a99-202">Die Bedeutung von Feld 3 hängt wie folgt von dem Wert in Feld 1 ab.</span><span class="sxs-lookup"><span data-stu-id="d4a99-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d4a99-203">Wert für Feld 1</span><span class="sxs-lookup"><span data-stu-id="d4a99-203">Field 1 value</span></span> | <span data-ttu-id="d4a99-204">Feld 3-Wert</span><span class="sxs-lookup"><span data-stu-id="d4a99-204">Field 3 value</span></span> | <span data-ttu-id="d4a99-205">Beschreibung von Feld 3</span><span class="sxs-lookup"><span data-stu-id="d4a99-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-206">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-206">0</span></span>             | <span data-ttu-id="d4a99-207">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-207">0</span></span>             | <span data-ttu-id="d4a99-208">Fortschrittsleiste weiterleiten (von links nach rechts)</span><span class="sxs-lookup"><span data-stu-id="d4a99-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="d4a99-209">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-209">1</span></span>             | <span data-ttu-id="d4a99-210">Rückwärts Statusanzeige (von rechts nach links)</span><span class="sxs-lookup"><span data-stu-id="d4a99-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="d4a99-211">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-211">1</span></span>             | <span data-ttu-id="d4a99-212">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-212">0</span></span>             | <span data-ttu-id="d4a99-213">Mit der aktuellen Aktion werden explizite progressreport-Meldungen gesendet.</span><span class="sxs-lookup"><span data-stu-id="d4a99-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="d4a99-214">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-214">1</span></span>             | <span data-ttu-id="d4a99-215">Erhöhen Sie die Statusanzeige um die Anzahl der Ticks, die in Feld 2 jedes Mal angegeben werden, wenn eine Aktions Daten Nachricht gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d4a99-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="d4a99-216">2</span><span class="sxs-lookup"><span data-stu-id="d4a99-216">2</span></span>             | <span data-ttu-id="d4a99-217">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="d4a99-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="d4a99-218">3</span><span class="sxs-lookup"><span data-stu-id="d4a99-218">3</span></span>             | <span data-ttu-id="d4a99-219">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="d4a99-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="d4a99-220">Die Bedeutung von Feld 4 hängt wie folgt von dem Wert in Feld 1 ab.</span><span class="sxs-lookup"><span data-stu-id="d4a99-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="d4a99-221">Wert für Feld 1</span><span class="sxs-lookup"><span data-stu-id="d4a99-221">Field 1 value</span></span> | <span data-ttu-id="d4a99-222">Wert für Feld 4</span><span class="sxs-lookup"><span data-stu-id="d4a99-222">Field 4 value</span></span> | <span data-ttu-id="d4a99-223">Beschreibung von Feld 4</span><span class="sxs-lookup"><span data-stu-id="d4a99-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-224">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-224">0</span></span>             | <span data-ttu-id="d4a99-225">0</span><span class="sxs-lookup"><span data-stu-id="d4a99-225">0</span></span>             | <span data-ttu-id="d4a99-226">Die Ausführung wird ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4a99-226">Execution is in progress.</span></span> <span data-ttu-id="d4a99-227">In diesem Fall kann die Benutzeroberfläche die verbleibende Zeit berechnen und anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="d4a99-228">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-228">1</span></span>             | <span data-ttu-id="d4a99-229">Erstellen des Ausführungs Skripts.</span><span class="sxs-lookup"><span data-stu-id="d4a99-229">Creating the execution script.</span></span> <span data-ttu-id="d4a99-230">In diesem Fall könnte die Benutzeroberfläche eine Meldung anzeigen, die gewartet werden soll, während das Installationsprogramm die Installation vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="d4a99-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="d4a99-231">1</span><span class="sxs-lookup"><span data-stu-id="d4a99-231">1</span></span>             | <span data-ttu-id="d4a99-232">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="d4a99-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="d4a99-233">2</span><span class="sxs-lookup"><span data-stu-id="d4a99-233">2</span></span>             | <span data-ttu-id="d4a99-234">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="d4a99-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="d4a99-235">3</span><span class="sxs-lookup"><span data-stu-id="d4a99-235">3</span></span>             | <span data-ttu-id="d4a99-236">Nicht verwendet</span><span class="sxs-lookup"><span data-stu-id="d4a99-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="d4a99-237">**Anzeigen von Meldungs Feldern**</span><span class="sxs-lookup"><span data-stu-id="d4a99-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="d4a99-238">Wenn Sie ein Meldungs Feld mit pushschaltflächen und Symbolen anzeigen möchten, berechnen Sie den Wert der *Art* , indem Sie die von **MessageBox** und **messageboxex** verwendeten Standardformate für Meldungs Felder zu **msimessagetypeerror**, **msimessagetypewarning** oder **msitypeuser** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="d4a99-239">Die verfügbaren Optionen für pushschaltflächen für VBScript sind vbOKOnly (MB \_ OK), vbOKCancel (MB \_ okabbrechen), vbAbortRetryIgnore (MB \_ AbortRetryIgnore), vbYesNoCancel (MB \_ YesNoCancel), vbYesNo (MB \_ YesNo) und vbRetryCancel (MB \_ RetryCancel).</span><span class="sxs-lookup"><span data-stu-id="d4a99-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="d4a99-240">Die verfügbaren Symbol Optionen für VBScript sind vbCritical (MB \_ iconerror), vbQuestion (MB \_ iconquestion), vbExclamation (MB \_ iconwarning) und vbInformation (MB \_ iconinformation).</span><span class="sxs-lookup"><span data-stu-id="d4a99-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="d4a99-241">Der folgende-Befehl sendet z. b. eine **msimessagetypeerror** -Meldung mit dem vbExclamation-Symbol und den vbYesNo-Schaltflächen.</span><span class="sxs-lookup"><span data-stu-id="d4a99-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="d4a99-242">Wenn eine benutzerdefinierte Aktion die **Message** -Methode aufruft, sollte die benutzerdefinierte Aktion in der Lage sein, einen Abbruch durch den Benutzer zu verarbeiten und muss **msidoaction statususerexit** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d4a99-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4a99-243">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4a99-243">Requirements</span></span>



| <span data-ttu-id="d4a99-244">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4a99-244">Requirement</span></span> | <span data-ttu-id="d4a99-245">Wert</span><span class="sxs-lookup"><span data-stu-id="d4a99-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4a99-246">Version</span><span class="sxs-lookup"><span data-stu-id="d4a99-246">Version</span></span><br/> | <span data-ttu-id="d4a99-247">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d4a99-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d4a99-248">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d4a99-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d4a99-249">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="d4a99-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d4a99-250">DLL</span><span class="sxs-lookup"><span data-stu-id="d4a99-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="d4a99-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4a99-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d4a99-252">IID</span><span class="sxs-lookup"><span data-stu-id="d4a99-252">IID</span></span><br/>     | <span data-ttu-id="d4a99-253">IID \_ ISession ist definiert als 000c109e-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d4a99-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
