---
description: Ereignis Bezeichner identifizieren ein bestimmtes Ereignis eindeutig.
ms.assetid: 83a84db4-572b-48bd-bc0f-071b2089a5ca
title: Ereignis Bezeichner (Ereignisprotokollierung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 402337cb2c7e862785a88ec604c6382152736fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527272"
---
# <a name="event-identifiers-event-logging"></a><span data-ttu-id="4516b-103">Ereignis Bezeichner (Ereignisprotokollierung)</span><span class="sxs-lookup"><span data-stu-id="4516b-103">Event Identifiers (Event Logging)</span></span>

<span data-ttu-id="4516b-104">Ereignis Bezeichner identifizieren ein bestimmtes Ereignis eindeutig.</span><span class="sxs-lookup"><span data-stu-id="4516b-104">Event identifiers uniquely identify a particular event.</span></span> <span data-ttu-id="4516b-105">Jede [Ereignis Quelle](event-sources.md) kann Ihre eigenen nummerierten Ereignisse und die Beschreibungs Zeichenfolgen definieren, denen Sie in ihrer Nachrichtendatei zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4516b-105">Each [event source](event-sources.md) can define its own numbered events and the description strings to which they are mapped in its message file.</span></span> <span data-ttu-id="4516b-106">Ereignis Betrachter können diese Zeichen folgen für den Benutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="4516b-106">Event viewers can present these strings to the user.</span></span> <span data-ttu-id="4516b-107">Sie sollten dem Benutzer helfen, zu verstehen, was schief gelaufen ist, und die zu übergreifenden Maßnahmen vorzuschlagen.</span><span class="sxs-lookup"><span data-stu-id="4516b-107">They should help the user understand what went wrong and suggest what actions to take.</span></span> <span data-ttu-id="4516b-108">Leiten Sie die Beschreibung an Benutzer weiter, die ihre eigenen Probleme lösen, nicht bei Administratoren oder Support Technikern.</span><span class="sxs-lookup"><span data-stu-id="4516b-108">Direct the description at users solving their own problems, not at administrators or support technicians.</span></span> <span data-ttu-id="4516b-109">Weitere Informationen finden Sie unter [Richtlinien für Fehlermeldungen](/windows/desktop/Debug/error-message-guidelines).</span><span class="sxs-lookup"><span data-stu-id="4516b-109">For more information, see [Error Message Guidelines](/windows/desktop/Debug/error-message-guidelines).</span></span>

## <a name="format"></a><span data-ttu-id="4516b-110">Format</span><span class="sxs-lookup"><span data-stu-id="4516b-110">Format</span></span>

<span data-ttu-id="4516b-111">Das folgende Diagramm veranschaulicht das Format eines Ereignis Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="4516b-111">The following diagram illustrates the format of an event identifier.</span></span>

``` syntax
  3 3 2 2 2 2 2 2 2 2 2 2 1 1 1 1 1 1 1 1 1 1
  1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0
 +---+-+-+-----------------------+-------------------------------+
 |Sev|C|R|     Facility          |               Code            |
 +---+-+-+-----------------------+-------------------------------+
```

<dl> <dt>

<span data-ttu-id="4516b-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Schweregrad</span><span class="sxs-lookup"><span data-stu-id="4516b-112"><span id="Sev"></span><span id="sev"></span><span id="SEV"></span>Sev</span></span>
</dt> <dd>

<span data-ttu-id="4516b-113">Schweregrad</span><span class="sxs-lookup"><span data-stu-id="4516b-113">Severity.</span></span> <span data-ttu-id="4516b-114">Der Schweregrad wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4516b-114">The severity is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="4516b-115">00-Erfolg</span><span class="sxs-lookup"><span data-stu-id="4516b-115">00 - Success</span></span></dd> <dd><span data-ttu-id="4516b-116">01-Information</span><span class="sxs-lookup"><span data-stu-id="4516b-116">01 - Informational</span></span></dd> <dd><span data-ttu-id="4516b-117">10-Warnung</span><span class="sxs-lookup"><span data-stu-id="4516b-117">10 - Warning</span></span></dd> <dd><span data-ttu-id="4516b-118">11-Fehler</span><span class="sxs-lookup"><span data-stu-id="4516b-118">11 - Error</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4516b-119"><span id="C"></span><span id="c"></span>Scher</span><span class="sxs-lookup"><span data-stu-id="4516b-119"><span id="C"></span><span id="c"></span>C</span></span>
</dt> <dd>

<span data-ttu-id="4516b-120">Customer-Bit.</span><span class="sxs-lookup"><span data-stu-id="4516b-120">Customer bit.</span></span> <span data-ttu-id="4516b-121">Dieses Bit wird wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="4516b-121">This bit is defined as follows:</span></span>

<dl> <dd><span data-ttu-id="4516b-122">0-System Code</span><span class="sxs-lookup"><span data-stu-id="4516b-122">0 - System code</span></span></dd> <dd><span data-ttu-id="4516b-123">1: Kundencode</span><span class="sxs-lookup"><span data-stu-id="4516b-123">1 - Customer code</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="4516b-124"><span id="R"></span><span id="r"></span>R</span><span class="sxs-lookup"><span data-stu-id="4516b-124"><span id="R"></span><span id="r"></span>R</span></span>
</dt> <dd>

<span data-ttu-id="4516b-125">Reservierte Bitzahl.</span><span class="sxs-lookup"><span data-stu-id="4516b-125">Reserved bit.</span></span>

</dd> <dt>

<span data-ttu-id="4516b-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Maschine</span><span class="sxs-lookup"><span data-stu-id="4516b-126"><span id="Facility"></span><span id="facility"></span><span id="FACILITY"></span>Facility</span></span>
</dt> <dd>

<span data-ttu-id="4516b-127">Betriebs Code.</span><span class="sxs-lookup"><span data-stu-id="4516b-127">Facility code.</span></span> <span data-ttu-id="4516b-128">Dieser Wert kann eine Anlage \_ NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4516b-128">This value can be FACILITY\_NULL.</span></span>

</dd> <dt>

<span data-ttu-id="4516b-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Ordnung</span><span class="sxs-lookup"><span data-stu-id="4516b-129"><span id="Code"></span><span id="code"></span><span id="CODE"></span>Code</span></span>
</dt> <dd>

<span data-ttu-id="4516b-130">Status Code für die Einrichtung.</span><span class="sxs-lookup"><span data-stu-id="4516b-130">Status code for the facility.</span></span>

</dd> </dl>

## <a name="message-definitions"></a><span data-ttu-id="4516b-131">Nachrichten Definitionen</span><span class="sxs-lookup"><span data-stu-id="4516b-131">Message Definitions</span></span>

<span data-ttu-id="4516b-132">Nachrichten werden in der Ereignis Nachrichtendatei definiert.</span><span class="sxs-lookup"><span data-stu-id="4516b-132">Messages are defined in the event message file.</span></span> <span data-ttu-id="4516b-133">Die Beschreibungs Zeichenfolgen in der Ereignis Meldungs Datei werden anhand der Ereignis Kennung indiziert, sodass Ereignisanzeige ereignisspezifischen Text für ein beliebiges Ereignis basierend auf dem Ereignis Bezeichner anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="4516b-133">The description strings in the event message file are indexed by event identifier, enabling Event Viewer to display event-specific text for any event based on the event identifier.</span></span> <span data-ttu-id="4516b-134">Alle Beschreibungen sind lokalisiert und von der Sprache abhängig.</span><span class="sxs-lookup"><span data-stu-id="4516b-134">All descriptions are localized and language dependent.</span></span> <span data-ttu-id="4516b-135">Weitere Informationen zum Aufbau einer Nachrichtendatei finden Sie unter [Message Text Files](message-text-files.md).</span><span class="sxs-lookup"><span data-stu-id="4516b-135">For more information on building a message file, see [Message Text Files](message-text-files.md).</span></span>

<span data-ttu-id="4516b-136">Die Beschreibungs Zeichenfolgen enthalten möglicherweise Einfügungs Zeichenfolgen im Format "%*n*", wobei "%1" die erste Einfügezeichenfolge angibt usw.</span><span class="sxs-lookup"><span data-stu-id="4516b-136">The description strings may contain insertion string placeholders, of the form %*n*, where %1 indicates the first insertion string, and so on.</span></span> <span data-ttu-id="4516b-137">Das folgende Beispiel zeigt einen Beispiel Eintrag in der MC-Datei:</span><span class="sxs-lookup"><span data-stu-id="4516b-137">For example, the following is a sample entry in the .mc file:</span></span>

``` syntax
MessageId=0x4
Severity=Error
Facility=System
SymbolicName=MSG_CMD_DELETE
Language=English
File %1 contains %2, which is in error.
.
```

<span data-ttu-id="4516b-138">In diesem Fall enthält der von [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) zurückgegebene Puffer Einfügezeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="4516b-138">In this case, the buffer returned by [**ReadEventLog**](/windows/desktop/api/Winbase/nf-winbase-readeventloga) contains insertion strings.</span></span> <span data-ttu-id="4516b-139">Der **numstrings** -Member der [**EventLogRecord**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) -Struktur gibt die Anzahl der Einfügezeichenfolgen an.</span><span class="sxs-lookup"><span data-stu-id="4516b-139">The **NumStrings** member of the [**EVENTLOGRECORD**](/windows/desktop/api/Winnt/ns-winnt-eventlogrecord) structure indicates the number of insertion strings.</span></span> <span data-ttu-id="4516b-140">Der **stringoffset** -Member der **EventLogRecord** -Struktur gibt den Speicherort der ersten Einfügezeichenfolge im Puffer an.</span><span class="sxs-lookup"><span data-stu-id="4516b-140">The **StringOffset** member of the **EVENTLOGRECORD** structure indicates the location of the first insertion string in the buffer.</span></span> <span data-ttu-id="4516b-141">Sie können ein Array von DWORD \_ -PTRS übergeben, das auf die Adresse jeder Zeichenfolge im Puffer zeigt, wenn Sie die [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) -Funktion aufrufen, und Sie fügt die Zeichen folgen in die Nachricht ein.</span><span class="sxs-lookup"><span data-stu-id="4516b-141">You can pass an array of DWORD\_PTRs that point to the address each string in the buffer when calling the [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) function and it will insert the strings into the message.</span></span>

<span data-ttu-id="4516b-142">Die Beschreibungs Zeichenfolge kann auch Platzhalter für Parameter Zeichenfolgen aus der Parameter Nachrichtendatei enthalten.</span><span class="sxs-lookup"><span data-stu-id="4516b-142">The description string can also contain placeholders for parameter strings from the parameter message file.</span></span> <span data-ttu-id="4516b-143">Die Platzhalter weisen das Format%%*n* auf, wobei% %1 durch die Parameter Zeichenfolge mit dem Bezeichner 1 ersetzt wird usw.</span><span class="sxs-lookup"><span data-stu-id="4516b-143">The placeholders are of the form %%*n*, where %%1 is replaced by the parameter string with the identifier of 1, and so on.</span></span> <span data-ttu-id="4516b-144">Allerdings müssen Sie die Parameter Zeichenfolgen in die von [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) zurückgegebene Meldungs Zeichenfolge einfügen.</span><span class="sxs-lookup"><span data-stu-id="4516b-144">However, it is up to you to insert the parameter strings into the message string that [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) returns.</span></span> <span data-ttu-id="4516b-145">In der Regel rufen Sie **FormatMessage** auf, um die Meldungs Zeichenfolge für das Ereignis zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4516b-145">Typically, you call **FormatMessage** to get the message string for the event.</span></span> <span data-ttu-id="4516b-146">Anschließend analysieren Sie die Meldungs Zeichenfolge für%%*n* Parameter.</span><span class="sxs-lookup"><span data-stu-id="4516b-146">You then parse the message string for %%*n* parameters.</span></span> <span data-ttu-id="4516b-147">Wenn die Nachricht einen oder mehrere Parameter enthält, laden Sie den **ParameterMessageFile** -Registrierungs Wert für die Quelle.</span><span class="sxs-lookup"><span data-stu-id="4516b-147">If the message contains one or more parameters, load the **ParameterMessageFile** registry value for the source.</span></span> <span data-ttu-id="4516b-148">Rufen Sie für jeden Parameter in der Meldungs Zeichenfolge den Bezeichner ab, und übergeben Sie ihn an **FormatMessage** , um den Parameter String zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4516b-148">For each parameter in the message string, get the identifier and pass it to **FormatMessage** to get the parameter string.</span></span> <span data-ttu-id="4516b-149">Ersetzen Sie den-Parameter in der Nachrichten Zeichenfolge durch die von **FormatMessage** zurückgegebene Parameter Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4516b-149">Replace the parameter in the message string with the parameter string that **FormatMessage** returned.</span></span>

## <a name="insertion-strings"></a><span data-ttu-id="4516b-150">Einfügen von Zeichen folgen</span><span class="sxs-lookup"><span data-stu-id="4516b-150">Insertion Strings</span></span>

<span data-ttu-id="4516b-151">Einfügezeichenfolgen sind optionale sprachunabhängige Zeichen folgen, mit denen Werte für Platzhalter in Beschreibungs Zeichenfolgen ausgefüllt werden</span><span class="sxs-lookup"><span data-stu-id="4516b-151">Insertion strings are optional language-independent strings used to fill in values for placeholders in description strings.</span></span> <span data-ttu-id="4516b-152">Da die Zeichen folgen nicht lokalisiert werden, ist es wichtig, dass diese Platzhalter nur zur Darstellung von sprachunabhängigen Zeichen folgen verwendet werden, wie z. b. numerische Werte, Dateinamen, Benutzernamen usw.</span><span class="sxs-lookup"><span data-stu-id="4516b-152">Because the strings are not localized, it is critical that these placeholders be used only to represent language-independent strings such as numeric values, file names, user names, and so on.</span></span> <span data-ttu-id="4516b-153">Die Zeichen folgen Länge darf nicht länger als 32 Kilobyte-1 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="4516b-153">The string length must not exceed 32 kilobytes - 1 characters.</span></span>

<span data-ttu-id="4516b-154">Vermeiden Sie die Verwendung mehrerer Zeichen folgen, um eine größere Beschreibung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4516b-154">Avoid using several strings to create a larger description.</span></span> <span data-ttu-id="4516b-155">Eine Einfügezeichenfolge sollte als Daten und nicht als Text behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="4516b-155">An insertion string should be treated as data, not text.</span></span> <span data-ttu-id="4516b-156">Im folgenden Beispiel sollten z. b. pszString1 und pszString2 nicht als Einfügezeichenfolgen für pszdescription verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4516b-156">For example, in the following example, pszString1 and pszString2 should not be used as insertion strings for pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "successfully"; 
LPSTR pszString2 = "not"; 
LPSTR pszDescription = "The user was %1 added to the database.";
```

<span data-ttu-id="4516b-157">Im folgenden Beispiel ist es sinnvoll, für die Einfügezeichenfolge in pszdescription entweder pszString1 oder pszString2 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="4516b-157">In the following example, it is appropriate to use either pszString1 or pszString2 for the insertion string in pszDescription.</span></span>

``` syntax
LPSTR pszString1 = "c:\\testapp1.c"; 
LPSTR pszString2 = "c:\\testapp2.c"; 
LPSTR pszDescription = "Access denied. Attempted to open the file %1."
```

 

 
