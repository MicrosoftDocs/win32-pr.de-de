---
description: Debug-Ausgabefunktionen
ms.assetid: dfe44c8c-43ec-461f-952f-b87256b82ee6
title: Debug-Ausgabefunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87470b44717bb76c1a029bd885bb9149a4636b5d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342965"
---
# <a name="debug-output-functions"></a><span data-ttu-id="e5995-103">Debug-Ausgabefunktionen</span><span class="sxs-lookup"><span data-stu-id="e5995-103">Debug Output Functions</span></span>

<span data-ttu-id="e5995-104">Die [DirectShow-Basisklassen](directshow-base-classes.md) stellen mehrere Makros zum Anzeigen von Debuginformationen bereit.</span><span class="sxs-lookup"><span data-stu-id="e5995-104">The [DirectShow Base Classes](directshow-base-classes.md) provide several macros for displaying debugging information.</span></span>



| <span data-ttu-id="e5995-105">Funktion</span><span class="sxs-lookup"><span data-stu-id="e5995-105">Function</span></span>                                               | <span data-ttu-id="e5995-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5995-106">Description</span></span>                                                                                          |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e5995-107">**Dbgcheckmodulelevel**</span><span class="sxs-lookup"><span data-stu-id="e5995-107">**DbgCheckModuleLevel**</span></span>](dbgcheckmodulelevel.md)     | <span data-ttu-id="e5995-108">Überprüft, ob die Protokollierung für die angegebenen Nachrichten Typen und die angegebene Ebene aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e5995-108">Checks whether logging is enabled for the given message types and level.</span></span>                             |
| [<span data-ttu-id="e5995-109">**Dbgdumpobjectregiester**</span><span class="sxs-lookup"><span data-stu-id="e5995-109">**DbgDumpObjectRegister**</span></span>](dbgdumpobjectregister.md) | <span data-ttu-id="e5995-110">Zeigt Informationen zu aktiven Objekten an.</span><span class="sxs-lookup"><span data-stu-id="e5995-110">Displays information about active objects.</span></span>                                                           |
| [<span data-ttu-id="e5995-111">**Dbginitialise**</span><span class="sxs-lookup"><span data-stu-id="e5995-111">**DbgInitialise**</span></span>](dbginitialise.md)                 | <span data-ttu-id="e5995-112">Initialisiert die Debugbibliothek.</span><span class="sxs-lookup"><span data-stu-id="e5995-112">Initializes the debug library.</span></span>                                                                       |
| [<span data-ttu-id="e5995-113">**Dbglog**</span><span class="sxs-lookup"><span data-stu-id="e5995-113">**DbgLog**</span></span>](dbglog.md)                               | <span data-ttu-id="e5995-114">Sendet eine Zeichenfolge an den debugausgabeort, wenn die Protokollierung für den angegebenen Typ und die angegebene Ebene aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e5995-114">Sends a string to the debug output location, if logging is enabled for the specified type and level.</span></span> |
| [<span data-ttu-id="e5995-115">**Dbgoutstring**</span><span class="sxs-lookup"><span data-stu-id="e5995-115">**DbgOutString**</span></span>](dbgoutstring.md)                   | <span data-ttu-id="e5995-116">Sendet eine Zeichenfolge an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="e5995-116">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="e5995-117">**Dbgsetmodulelevel**</span><span class="sxs-lookup"><span data-stu-id="e5995-117">**DbgSetModuleLevel**</span></span>](dbgsetmodulelevel.md)         | <span data-ttu-id="e5995-118">Legt den Protokolliergrad für einen oder mehrere Nachrichten Typen fest.</span><span class="sxs-lookup"><span data-stu-id="e5995-118">Sets the logging level for one or more message types.</span></span>                                                |
| [<span data-ttu-id="e5995-119">**Dbgbeenden**</span><span class="sxs-lookup"><span data-stu-id="e5995-119">**DbgTerminate**</span></span>](dbgterminate.md)                   | <span data-ttu-id="e5995-120">Bereinigt die Debug-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="e5995-120">Cleans up the debug library.</span></span>                                                                         |
| [<span data-ttu-id="e5995-121">**Display Type**</span><span class="sxs-lookup"><span data-stu-id="e5995-121">**DisplayType**</span></span>](displaytype.md)                     | <span data-ttu-id="e5995-122">Sendet Informationen über einen Medientyp an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="e5995-122">Sends information about a media type to the debug output location.</span></span>                                   |
| [<span data-ttu-id="e5995-123">**Dumpgraph**</span><span class="sxs-lookup"><span data-stu-id="e5995-123">**DumpGraph**</span></span>](dumpgraph.md)                         | <span data-ttu-id="e5995-124">Sendet Informationen zu einem Filter Diagramm an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="e5995-124">Sends information about a filter graph to the debug output location.</span></span>                                 |
| [<span data-ttu-id="e5995-125">**Guidnames**</span><span class="sxs-lookup"><span data-stu-id="e5995-125">**GuidNames**</span></span>](guidnames.md)                         | <span data-ttu-id="e5995-126">Globales Array, das Zeichen folgen enthält, die die in "UUIDs. h" definierten GUIDs darstellen.</span><span class="sxs-lookup"><span data-stu-id="e5995-126">Global array that contains strings representing the GUIDs defined in Uuids.h.</span></span>                        |
| [<span data-ttu-id="e5995-127">**Benennen**</span><span class="sxs-lookup"><span data-stu-id="e5995-127">**NAME**</span></span>](name.md)                                   | <span data-ttu-id="e5995-128">Generiert eine reine debugzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e5995-128">Generates a debug-only string.</span></span>                                                                       |
| [<span data-ttu-id="e5995-129">**Nebenbei**</span><span class="sxs-lookup"><span data-stu-id="e5995-129">**NOTE**</span></span>](note.md)                                   | <span data-ttu-id="e5995-130">Sendet eine Zeichenfolge an den debugausgabespeicherort.</span><span class="sxs-lookup"><span data-stu-id="e5995-130">Sends a string to the debug output location.</span></span>                                                         |
| [<span data-ttu-id="e5995-131">**Erinnern**</span><span class="sxs-lookup"><span data-stu-id="e5995-131">**REMIND**</span></span>](remind.md)                               | <span data-ttu-id="e5995-132">Generiert zum Zeitpunkt der Kompilierung eine Erinnerung.</span><span class="sxs-lookup"><span data-stu-id="e5995-132">Generates a reminder at compile time.</span></span>                                                                |



 

<span data-ttu-id="e5995-133">**Registrierungsschlüssel**</span><span class="sxs-lookup"><span data-stu-id="e5995-133">**Registry Keys**</span></span>

<span data-ttu-id="e5995-134">Die Debug-Ausgabefunktion in DirectShow verwendet einen Satz von Registrierungs Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="e5995-134">The debug output function in DirectShow use a set of registry keys.</span></span> <span data-ttu-id="e5995-135">Der Speicherort dieser Registrierungsschlüssel hängt von der Windows-Version ab.</span><span class="sxs-lookup"><span data-stu-id="e5995-135">The location of these registry keys depends on the version of Windows.</span></span>

<span data-ttu-id="e5995-136">*Vor Windows Vista* befinden sich die debugschlüssel unter folgendem Pfad:</span><span class="sxs-lookup"><span data-stu-id="e5995-136">*Prior to Windows Vista*, the debugging keys are located under the following path:</span></span>

<span data-ttu-id="e5995-137">**HKEY \_ \_** \\ **Software** \\ **Debuggen** des lokalen Computers</span><span class="sxs-lookup"><span data-stu-id="e5995-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Debug**</span></span>

<span data-ttu-id="e5995-138">In Windows Vista oder höher befinden sich diese unter folgendem Pfad:</span><span class="sxs-lookup"><span data-stu-id="e5995-138">In Windows Vista or later, they are located under the following path:</span></span>

<span data-ttu-id="e5995-139">**HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **DirectShow** \\ **Debug**</span><span class="sxs-lookup"><span data-stu-id="e5995-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**DirectShow**\\**Debug**</span></span>

<span data-ttu-id="e5995-140">Für Filter von Drittanbietern hängt der Speicherort davon ab, welche Version der [DirectShow-Basisklassen](directshow-base-classes.md) verwendet wurde, um den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e5995-140">For third-party filters, the location depends on which version of the [DirectShow Base Classes](directshow-base-classes.md) was used to build the filter.</span></span> <span data-ttu-id="e5995-141">Die Version, die im Windows SDK für Windows Vista enthalten ist, verwendet den neueren Pfad.</span><span class="sxs-lookup"><span data-stu-id="e5995-141">The version included in the Windows SDK for Windows Vista uses the newer path.</span></span> <span data-ttu-id="e5995-142">In früheren Versionen wurde der ältere Pfad verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5995-142">Previous versions used the older path.</span></span>

<span data-ttu-id="e5995-143">In den folgenden Anmerkungen wird die Bezeichnung *<DebugRoot>* verwendet, um diese beiden Pfade anzugeben.</span><span class="sxs-lookup"><span data-stu-id="e5995-143">In the remarks that follow, the label *<DebugRoot>* is used to indicate these two paths.</span></span> <span data-ttu-id="e5995-144">Ersetzen Sie abhängig von der Windows-Version oder der-Version der Basisklassen den korrekten Pfad.</span><span class="sxs-lookup"><span data-stu-id="e5995-144">Substitute the correct path, depending on the version of Windows or the version of the base classes.</span></span>

<span data-ttu-id="e5995-145">**Debugprotokollierung**</span><span class="sxs-lookup"><span data-stu-id="e5995-145">**Debug Logging**</span></span>

<span data-ttu-id="e5995-146">In DirectShow werden mehrere Nachrichten Typen definiert, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e5995-146">DirectShow defines several message types, shown in the following table.</span></span>



| <span data-ttu-id="e5995-147">Wert</span><span class="sxs-lookup"><span data-stu-id="e5995-147">Value</span></span>                   | <span data-ttu-id="e5995-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e5995-148">Description</span></span>                                             |
|-------------------------|---------------------------------------------------------|
| <span data-ttu-id="e5995-149">Protokoll \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="e5995-149">LOG\_ERROR</span></span>              | <span data-ttu-id="e5995-150">Fehler Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="e5995-150">Error notification.</span></span>                                     |
| <span data-ttu-id="e5995-151">Protokoll \_ Sperren</span><span class="sxs-lookup"><span data-stu-id="e5995-151">LOG\_LOCKING</span></span>            | <span data-ttu-id="e5995-152">Sperren und entsperren kritischer Abschnitte.</span><span class="sxs-lookup"><span data-stu-id="e5995-152">Locking and unlocking of critical sections.</span></span>             |
| <span data-ttu-id="e5995-153">Protokoll \_ Speicher</span><span class="sxs-lookup"><span data-stu-id="e5995-153">LOG\_MEMORY</span></span>             | <span data-ttu-id="e5995-154">Speicher Belegung und Objekt Erstellung und-Zerstörung.</span><span class="sxs-lookup"><span data-stu-id="e5995-154">Memory allocation, and object creation and destruction.</span></span> |
| <span data-ttu-id="e5995-155">Protokoll \_ zeitliche Steuerung</span><span class="sxs-lookup"><span data-stu-id="e5995-155">LOG\_TIMING</span></span>             | <span data-ttu-id="e5995-156">Zeitliche Steuerung und Leistungsmessungen.</span><span class="sxs-lookup"><span data-stu-id="e5995-156">Timing and performance measurements.</span></span>                    |
| <span data-ttu-id="e5995-157">Protokoll Ablauf \_ Verfolgung</span><span class="sxs-lookup"><span data-stu-id="e5995-157">LOG\_TRACE</span></span>              | <span data-ttu-id="e5995-158">Allgemeine Rückruf-Ablauf Verfolgung.</span><span class="sxs-lookup"><span data-stu-id="e5995-158">General call tracing.</span></span>                                   |
| <span data-ttu-id="e5995-159">CUSTOM1 bis CUSTOM5</span><span class="sxs-lookup"><span data-stu-id="e5995-159">CUSTOM1 through CUSTOM5</span></span> | <span data-ttu-id="e5995-160">Verfügbar für benutzerdefinierte Debugmeldungen</span><span class="sxs-lookup"><span data-stu-id="e5995-160">Available for custom debug messages</span></span>                     |



 

<span data-ttu-id="e5995-161">Jede der DirectShow-Debug-Protokollierungsfunktionen gibt einen Nachrichtentyp und eine Protokollebene an.</span><span class="sxs-lookup"><span data-stu-id="e5995-161">Each of the DirectShow debug logging functions specifies a message type and a log level.</span></span> <span data-ttu-id="e5995-162">Die Debugmeldung wird nur angezeigt, wenn die aktuelle Debugebene für diesen Nachrichtentyp größer oder gleich der in der Protokollierungsfunktion angegebenen Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="e5995-162">The debug message is displayed only when the current debugging level for that message type is equal to or greater than the level specified in the logging function.</span></span> <span data-ttu-id="e5995-163">Andernfalls wird die Meldung ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e5995-163">Otherwise, the message is ignored.</span></span>

<span data-ttu-id="e5995-164">Der folgende Code gibt beispielsweise die Zeichenfolge "This is a Debug Message" aus, wenn die Protokoll Ablauf \_ Verfolgungs Ebene 3 oder höher ist:</span><span class="sxs-lookup"><span data-stu-id="e5995-164">For example, the following code outputs the string "This is a debug message" if the LOG\_TRACE level is 3 or higher:</span></span>

``` syntax
DbgLog((LOG_TRACE, 3, TEXT("This is a debug message")));
```

<span data-ttu-id="e5995-165">Jedes Modul kann seine eigene Debugebene für jeden Nachrichtentyp festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5995-165">Every module can set its own debugging level for each message type.</span></span> <span data-ttu-id="e5995-166">(Ein *Modul* ist eine DLL-Datei oder ausführbare Datei, die mithilfe der **LoadLibrary** -Funktion geladen werden kann.) Die debugebenen eines Moduls werden in der Registrierung unter dem folgenden Schlüssel angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e5995-166">(A *module* is a DLL or executable that can be loaded using the **LoadLibrary** function.) A module's debugging levels appear in the registry under the following key:</span></span>

<span data-ttu-id="e5995-167">**lokaler HKEY- \_ \_ Computer**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span><span class="sxs-lookup"><span data-stu-id="e5995-167">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<ModuleName>**\\**<MessageType>**</span></span>

<span data-ttu-id="e5995-168">dabei *<Message Type>* ist der Nachrichtentyp abzüglich des anfänglichen "Protokolls \_ ", z. b. **Sperren** für Protokoll \_ Sperr Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="e5995-168">where *<Message Type>* is the message type minus the initial "LOG\_"; for example, **LOCKING** for LOG\_LOCKING messages.</span></span> <span data-ttu-id="e5995-169">Wenn ein Modul geladen wird, sucht die Debugbibliothek die Protokolliergrade des Moduls in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="e5995-169">When a module is loaded, the debug library finds the module's logging levels in the registry.</span></span> <span data-ttu-id="e5995-170">Wenn die Registrierungsschlüssel nicht vorhanden sind, werden Sie von der Debugbibliothek erstellt.</span><span class="sxs-lookup"><span data-stu-id="e5995-170">If the registry keys do not exist, the debug library creates them.</span></span>

<span data-ttu-id="e5995-171">Ein Modul kann mithilfe der [**dbgsetmodulelevel**](dbgsetmodulelevel.md) -Funktion auch seine eigenen Ebenen zur Laufzeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="e5995-171">A module can also set its own levels at run time, using the [**DbgSetModuleLevel**](dbgsetmodulelevel.md) function.</span></span> <span data-ttu-id="e5995-172">Um eine Nachricht an die Debugausgabe zu senden, nennen Sie das [**dbglog**](dbglog.md) -Makro.</span><span class="sxs-lookup"><span data-stu-id="e5995-172">To send a message to the debug output, call the [**DbgLog**](dbglog.md) macro.</span></span> <span data-ttu-id="e5995-173">Im folgenden Beispiel wird eine Nachricht der Ebene 3 des Typs log \_ Trace erstellt:</span><span class="sxs-lookup"><span data-stu-id="e5995-173">The following example creates a level 3 message of type LOG\_TRACE:</span></span>

<span data-ttu-id="e5995-174">Sie können auch globale Protokollierungs Stufen mit dem folgenden Registrierungsschlüssel angeben:</span><span class="sxs-lookup"><span data-stu-id="e5995-174">You can also specify global logging levels, with the following registry key:</span></span>


```C++
\HKEY_LOCAL_MACHINE\<DebugRoot>\GLOBAL\<Message Type>
```



<span data-ttu-id="e5995-175">Die Debug-Bibliothek verwendet, je nachdem, auf welcher Ebene größer, auf der globalen Ebene oder auf der Modulebene.</span><span class="sxs-lookup"><span data-stu-id="e5995-175">The debug library uses whichever level is greater, the global level or the module level.</span></span>

<span data-ttu-id="e5995-176">**Ausgabepfad Debuggen**</span><span class="sxs-lookup"><span data-stu-id="e5995-176">**Debug Output Location**</span></span>

<span data-ttu-id="e5995-177">Der Speicherort der Debugausgabe wird durch einen anderen Registrierungsschlüssel bestimmt:</span><span class="sxs-lookup"><span data-stu-id="e5995-177">The debug output location is determined by another registry key:</span></span>

<span data-ttu-id="e5995-178">**HKEY \_ \_** \\ **<DebugRoot>** \\ **<Modile Name>** \\ **Protokolldatei** des lokalen Computers</span><span class="sxs-lookup"><span data-stu-id="e5995-178">**HKEY\_LOCAL\_MACHINE**\\**<DebugRoot>**\\**<Modile Name>**\\**LogToFile**</span></span>

<span data-ttu-id="e5995-179">Wenn der Wert dieses Schlüssels ist `Console` , wird die Ausgabe in das Konsolenfenster ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="e5995-179">If the value of this key is `Console`, the output goes to the console window.</span></span> <span data-ttu-id="e5995-180">Wenn der Wert `Deb` , `Debug` , `Debugger` oder eine leere Zeichenfolge ist, wird die Ausgabe an das Debuggerfenster weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="e5995-180">If the value is `Deb`, `Debug`, `Debugger`, or an empty string, the output goes to the debugger window.</span></span> <span data-ttu-id="e5995-181">Andernfalls wird die Ausgabe in eine Datei geschrieben, die durch den Registrierungsschlüssel angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e5995-181">Otherwise, the output is written to a file specified by the registry key.</span></span>

<span data-ttu-id="e5995-182">Bevor eine ausführbare Datei die DirectShow-Debugbibliothek verwendet, muss Sie die [**dbginitialise**](dbginitialise.md) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="e5995-182">Before an executable uses the DirectShow debug library, it must call the [**DbgInitialise**](dbginitialise.md) function.</span></span> <span data-ttu-id="e5995-183">Danach muss Sie die [**dbgend**](dbgterminate.md) -Funktion abrufen.</span><span class="sxs-lookup"><span data-stu-id="e5995-183">Afterward, it must call the [**DbgTerminate**](dbgterminate.md) function.</span></span> <span data-ttu-id="e5995-184">DLLs müssen diese Funktionen nicht aufrufen, da Sie vom DLL-Einstiegspunkt (in der Basisklassen Bibliothek definiert) automatisch aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e5995-184">DLLs do not need to call these functions, because the DLL entry point (defined in the base class library) calls them automatically.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5995-185">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5995-185">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5995-186">Debugging-Hilfsprogramme</span><span class="sxs-lookup"><span data-stu-id="e5995-186">Debugging Utilities</span></span>](debugging-utilities.md)
</dt> </dl>

 

 



