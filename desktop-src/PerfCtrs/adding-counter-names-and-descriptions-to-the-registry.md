---
description: Die Namen und Beschreibungen aller Leistungs Objekte und deren Indikatoren werden in der Registrierung gespeichert.
ms.assetid: 6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4
title: Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e9d2c97ebe80a8ef2a8396ca42583cbad874859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359047"
---
# <a name="adding-counter-names-and-descriptions-to-the-registry"></a><span data-ttu-id="85e81-103">Hinzufügen von Zählernamen und Beschreibungen zum RegisterHinzufügen von Namen und Beschreibungen von Leistungsindikatoren zur Registrierung</span><span class="sxs-lookup"><span data-stu-id="85e81-103">Adding Counter Names and Descriptions to the Registry</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85e81-104">Aufgrund erheblicher Leistungs-und Zuverlässigkeits Beschränkungen ist die Methode zum Bereitstellen von Leistungsdaten, die in diesem Thema beschrieben werden, möglicherweise in Zukunft geändert oder nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="85e81-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="85e81-105">Stattdessen empfiehlt Microsoft die Verwendung der unter [Bereitstellen von Indikator Daten mit Version 2,0](providing-counter-data-using-version-2-0.md) beschriebenen Methode zum Erstellen neuer Leistungsindikatoren und die Migration vorhandener Leistungsindikatoren zur Verwendung dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="85e81-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters and that you migrate existing performance counters to use that method.</span></span>

<span data-ttu-id="85e81-106">Die Namen und Beschreibungen aller v1-Leistungs Objekte und deren Zähler müssen auf dem System installiert sein.</span><span class="sxs-lookup"><span data-stu-id="85e81-106">The names and descriptions of all V1 performance objects and their counters must be installed the system.</span></span> <span data-ttu-id="85e81-107">So speichern Sie Namen und Beschreibungen für die Objekte und Leistungsindikatoren Ihres [v1-Anbieters](providing-counter-data.md):</span><span class="sxs-lookup"><span data-stu-id="85e81-107">To store names and descriptions for the objects and counters from your [V1 provider](providing-counter-data.md):</span></span>

- <span data-ttu-id="85e81-108">[Erstellen Sie eine h-Header Datei](#creating-a-symbolic-constants-h-file) , die die symbolischen Konstanten für die Offsets für die Objekte und Leistungsindikatoren enthält.</span><span class="sxs-lookup"><span data-stu-id="85e81-108">[Create a .h header file](#creating-a-symbolic-constants-h-file) that contains the symbolic constants for the offsets to your objects and counters.</span></span>
- <span data-ttu-id="85e81-109">[Erstellen Sie eine Initialisierung (. INI-Datei](#creating-an-initialization-ini-file) , die die Zeichen folgen enthält.</span><span class="sxs-lookup"><span data-stu-id="85e81-109">[Create an initialization (.INI) file](#creating-an-initialization-ini-file) that contains the strings.</span></span>
- <span data-ttu-id="85e81-110">Wenn Sie die Komponente installieren, [führen Sie das **Lodctr** -Tool](#running-the-lodctr-tool) aus, um die Namen und Beschreibungen in der Registrierung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="85e81-110">When installing your component, [run the **lodctr** tool](#running-the-lodctr-tool) to install the names and descriptions into the registry.</span></span>
- <span data-ttu-id="85e81-111">Wenn Sie die Komponente deinstallieren, führen Sie das unlodctr-Tool aus, um die Namen und Beschreibungen aus der Registrierung zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="85e81-111">When uninstalling your component, run the unlodctr tool to remove the names and descriptions from the registry.</span></span>

## <a name="creating-a-symbolic-constants-h-file"></a><span data-ttu-id="85e81-112">Erstellen einer symbolischen Konstanten Datei (. h)</span><span class="sxs-lookup"><span data-stu-id="85e81-112">Creating a symbolic constants (.h) file</span></span>

<span data-ttu-id="85e81-113">Erstellen Sie eine h-Header Datei, die Konstanten (Makros) für die Offsets für die Objekte und Leistungsindikatoren definiert, die Ihr Anbieter bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="85e81-113">Create a .h header file that defines constants (macros) for the offsets to the objects and counters that your provider provides.</span></span> <span data-ttu-id="85e81-114">Der. h-Header wird während der Installation des Anbieters als Eingabe für **Lodctr** verwendet und kann auch vom C/C++-Code des Anbieters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-114">The .h header is used as input to **lodctr** during installation of your provider, and may also be used by the C/C++ code of your provider.</span></span>

<span data-ttu-id="85e81-115">Die Konstanten Werte müssen aufeinander folgen, auch Zahlen, die mit 0 (null) beginnen.</span><span class="sxs-lookup"><span data-stu-id="85e81-115">The constant values must be consecutive, even numbers beginning with zero.</span></span> <span data-ttu-id="85e81-116">Gruppieren Sie die Konstanten nach Objekten (d. h. Starten Sie jede Gruppe mit dem Objekt Offset, und folgen Sie dann den Offsets der Zähler für dieses Objekt).</span><span class="sxs-lookup"><span data-stu-id="85e81-116">Group the constants by objects (i.e. start each group with the object offset, then follow with the offsets of the counters for that object).</span></span>

<span data-ttu-id="85e81-117">Die Konstanten in der Kopfzeile bestimmen die Reihenfolge, in der die Indikatoren dem Namen und dem Hilfetext in der Registrierung hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-117">The constants in the header determine the order in which the counters are added to the name and help text in the registry.</span></span> <span data-ttu-id="85e81-118">Der Anbieter verwendet die Offsets, um zu bestimmen, welches Objekt abgefragt wird und welche Indexwerte verwendet werden sollen, wenn die Daten zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-118">The provider uses the offsets to determine which object is being queried and the index values to use when returning the data.</span></span> <span data-ttu-id="85e81-119">Weitere Informationen finden Sie unter [Implementieren von openperformancedata](implementing-openperformancedata.md).</span><span class="sxs-lookup"><span data-stu-id="85e81-119">For details, see [Implementing OpenPerformanceData](implementing-openperformancedata.md).</span></span>

<span data-ttu-id="85e81-120">Im folgenden finden Sie ein Beispiel für eine symbolische Konstante Datei mit dem Namen counteroffsets. h, die im Beispiel zum [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85e81-120">The following shows an example of a symbolic constant file, named CounterOffsets.h, that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) example.</span></span>

```C++
#ifndef OFFSETS_H
#define OFFSETS_H

// Symbol file that defines constant values for the objects
// and counters that the provider provides. The counters should be
// grouped by object.

#define TRANSFER_OBJECT      0 // First object must be at offset 0.
#define BYTES_SENT           2 // Counters for the object follow.
#define AVAILABLE_BANDWIDTH  4 // Offsets must be even numbers.

// Not required, but for convenience in implementing the Open function:
#define LAST_TRANSFER_OBJECT_COUNTER_OFFSET  AVAILABLE_BANDWIDTH

#define PEER_OBJECT          6 // Second object must be at the next offset.
#define BYTES_SERVED         8 // Counter for the second object.

// Not required, but for convenience in implementing the Open function:
#define LAST_PEER_OBJECT_COUNTER_OFFSET  BYTES_SERVED

#endif // OFFSETS_H
```

## <a name="creating-an-initialization-ini-file"></a><span data-ttu-id="85e81-121">Erstellen einer Initialisierung (. INI-Datei</span><span class="sxs-lookup"><span data-stu-id="85e81-121">Creating an initialization (.INI) file</span></span>

<span data-ttu-id="85e81-122">Die Initialisierung (. INI) enthält den Namen und die Hilfe Zeichenfolgen für die einzelnen Objekte und Leistungsdaten, die in der Symbol Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="85e81-122">The initialization (.INI) file contains the name and help strings for each object and counter defined in your symbol file.</span></span> <span data-ttu-id="85e81-123">Die. Die INI-Datei wird während der Installation des Anbieters als Eingabe für **Lodctr** verwendet.</span><span class="sxs-lookup"><span data-stu-id="85e81-123">The .INI file is used as input to **lodctr** during installation of your provider.</span></span>

<span data-ttu-id="85e81-124">Die. Die INI-Datei muss als UTF-16LE (mit Byte Reihenfolge Markierung) codiert werden und sollte die folgenden Abschnitte und Schlüssel aufweisen:</span><span class="sxs-lookup"><span data-stu-id="85e81-124">The .INI file should be encoded as UTF-16LE (with byte order mark) and should have the following sections and keys:</span></span>

```ini
[info]
drivername=ServiceKeyName
symbolfile=SymbolFile.h
trusted=(Unused)

[objects]
<symbol>_<langid>_NAME=(Unused)

[languages]
<langid>=(Unused)

[text]
<symbol>_<langid>_NAME=Name
<symbol>_<langid>_HELP=Description
```

### <a name="info-section"></a><span data-ttu-id="85e81-125">Abschnitt [Info]</span><span class="sxs-lookup"><span data-stu-id="85e81-125">[info] section</span></span>

<span data-ttu-id="85e81-126">Der `[info]` Abschnitt enthält allgemeine Informationen zum Anbieter.</span><span class="sxs-lookup"><span data-stu-id="85e81-126">The `[info]` section contains general information about the provider.</span></span> <span data-ttu-id="85e81-127">Die Abschnitts Schlüssel werden wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="85e81-127">The section keys are defined as follows:</span></span>

|<span data-ttu-id="85e81-128">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="85e81-128">Key</span></span>|<span data-ttu-id="85e81-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85e81-129">Description</span></span>
|---|-----------
|<span data-ttu-id="85e81-130">**DriverName**</span><span class="sxs-lookup"><span data-stu-id="85e81-130">**DriverName**</span></span>| <span data-ttu-id="85e81-131">Geben Sie den Namen des Leistungs Schlüssels des Anbieters an, der sich in der Registrierung unter dem `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` Schlüssel befindet.</span><span class="sxs-lookup"><span data-stu-id="85e81-131">Specify the name of the provider's performance key located in the registry under the `HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services` key.</span></span> <span data-ttu-id="85e81-132">Weitere Informationen zum Erstellen dieses Schlüssels finden Sie unter [Erstellen des Leistungs Schlüssels der Anwendung](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="85e81-132">For information on creating this key, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span>
|<span data-ttu-id="85e81-133">**Symbol file**</span><span class="sxs-lookup"><span data-stu-id="85e81-133">**SymbolFile**</span></span>| <span data-ttu-id="85e81-134">Geben Sie die. h-Header Datei an, die symbolische Werte der Objekte und Leistungsindikatoren Ihres Anbieters enthält.</span><span class="sxs-lookup"><span data-stu-id="85e81-134">Specify the .h header file that contains symbolic values of your provider's objects and counters.</span></span> <span data-ttu-id="85e81-135">Während der Installation (beim Aufrufen von **Lodctr**) muss sich die Header Datei im selben Verzeichnis wie das befinden. INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="85e81-135">During installation (when invoking **lodctr**), the header file must be in the same directory as the .INI file.</span></span>
|<span data-ttu-id="85e81-136">**Würdiges**</span><span class="sxs-lookup"><span data-stu-id="85e81-136">**Trusted**</span></span>| <span data-ttu-id="85e81-137">Wenn Sie diesen Schlüssel in den `[info]` Abschnitt einschließen, fügt **Lodctr** dem Leistungs Schlüssel einen Bibliotheks Überprüfungs Code-Registrierungs Wert mit einer binären Signatur ihrer Leistungs-dll hinzu.</span><span class="sxs-lookup"><span data-stu-id="85e81-137">If you include this key in the `[info]` section, **lodctr** will add a Library Validation Code registry value to your performance key with a binary signature of your performance DLL.</span></span> <span data-ttu-id="85e81-138">Wenn Perflib Ihre DLL aufruft, vergleicht Sie die Signatur mit der dll, um zu bestimmen, ob die DLL geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="85e81-138">When PERFLIB calls your DLL it compares the signature with your DLL to determine if the DLL has been modified.</span></span> <span data-ttu-id="85e81-139">Der Wert des **vertrauenswürdigen** Schlüssels wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="85e81-139">The value of the **Trusted** key is ignored.</span></span>

<span data-ttu-id="85e81-140">Die `DriverName` `SymbolFile` Schlüssel und sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85e81-140">The `DriverName` and `SymbolFile` keys are required.</span></span>

### <a name="objects-section"></a><span data-ttu-id="85e81-141">Abschnitt [Objekte]</span><span class="sxs-lookup"><span data-stu-id="85e81-141">[objects] section</span></span>

<span data-ttu-id="85e81-142">Der `[objects]` Abschnitt enthält eine Liste der Leistungs Objekte, die vom Anbieter unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-142">The `[objects]` section provides a list of the performance objects that the provider supports.</span></span> <span data-ttu-id="85e81-143">Dies wird verwendet, um zu bestimmen, ob jedes Symbol aus dem `[text]` Abschnitt auf ein Objekt oder einen Zählers verweist.</span><span class="sxs-lookup"><span data-stu-id="85e81-143">This is used to determine whether each symbol from the `[text]` section refers an object or a counter.</span></span>

<span data-ttu-id="85e81-144">Fügen Sie für jedes Objekt (Counter Set), das vom Anbieter unterstützt wird, dem Abschnitt einen Schlüssel mit dem Namen hinzu `<symbol>_<langid>_NAME=` `[objects]` , wobei `<symbol>` der Name des Objekts und `<langid>` die Sprach-ID einer der unterstützten Sprachen ist.</span><span class="sxs-lookup"><span data-stu-id="85e81-144">For each object (counterset) supported by your provider, add one key named `<symbol>_<langid>_NAME=` to the `[objects]` section, where `<symbol>` is the name of the object and `<langid>` is the language id of one of the supported languages.</span></span> <span data-ttu-id="85e81-145">Der Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="85e81-145">The value is ignored.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="85e81-146">Der `[objects]` Abschnitt verbessert die Leistung des Systems.</span><span class="sxs-lookup"><span data-stu-id="85e81-146">The `[objects]` section improves the performance of the system.</span></span> <span data-ttu-id="85e81-147">Obwohl der Abschnitt "Objects" optional ist, sollten Sie diesen Abschnitt stets in ihren einschließen. INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="85e81-147">Although the objects section is optional, you should always include this section in your .INI file.</span></span> <span data-ttu-id="85e81-148">Wenn Sie diesen Abschnitt einschließen, wird die Leistungs-dll nur aufgerufen, wenn Sie das angeforderte Objekt unterstützen.</span><span class="sxs-lookup"><span data-stu-id="85e81-148">If you include this section, your performance DLL is called only if you support the requested object.</span></span> <span data-ttu-id="85e81-149">Wenn Sie den Objekt Abschnitt nicht einschließen, wird die DLL für jede Abfrage aufgerufen, da das System nicht weiß, welche Objekte der Anbieter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85e81-149">If you do not include the objects section, your DLL is called for every query because the system does not know which objects your provider supports.</span></span> <span data-ttu-id="85e81-150">Wenn der Objekt Abschnitt nicht enthalten ist, generiert **Lodctr** im Anwendungs Ereignisprotokoll eine Meldung, die besagt, dass die. Die INI-Datei enthielt keinen Objekte Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="85e81-150">If the object section is not included, **lodctr** generates a message in the application event log stating that the .INI file did not contain an objects section.</span></span> <span data-ttu-id="85e81-151">Der Ereignis Bezeichner dieser Nachricht ist 2000.</span><span class="sxs-lookup"><span data-stu-id="85e81-151">The event identifier of this message is 2000.</span></span>

### <a name="languages-section"></a><span data-ttu-id="85e81-152">Abschnitt [Sprachen]</span><span class="sxs-lookup"><span data-stu-id="85e81-152">[languages] section</span></span>

<span data-ttu-id="85e81-153">Der `[languages]` Abschnitt enthält eine Liste der sprach Bezeichner jeder Sprache, für die Ihr Anbieter Name und Hilfe Zeichenfolgen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="85e81-153">The `[languages]` section provides a list of the language identifiers of each language for which your provider supplies name and help strings.</span></span> <span data-ttu-id="85e81-154">Alle Anbieter sollten `009` (Englisch) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="85e81-154">All providers should support `009` (English).</span></span>

<span data-ttu-id="85e81-155">Fügen Sie für jede unterstützte Sprache einen Schlüssel mit dem Namen hinzu `<langid>=` .</span><span class="sxs-lookup"><span data-stu-id="85e81-155">For each supported language, add one key named `<langid>=`.</span></span> <span data-ttu-id="85e81-156">Der Wert wird ignoriert, aber zu Dokumentationszwecken wird der Wert normalerweise auf den Namen der entsprechenden Sprache festgelegt, z. b. `009=English` .</span><span class="sxs-lookup"><span data-stu-id="85e81-156">The value is ignored, but for documentation purposes the value is normally set to the name of the corresponding language, e.g. `009=English`.</span></span>

<span data-ttu-id="85e81-157">In den meisten Sprachen sollten Sie den Bezeichner der primären Sprache verwenden.</span><span class="sxs-lookup"><span data-stu-id="85e81-157">For most languages, you should use the primary language identifier.</span></span> <span data-ttu-id="85e81-158">Die komplette Liste der Sprachen-IDs finden Sie in der Header Datei "Winnt. h" unter der Überschrift "primäre Sprach-IDs".</span><span class="sxs-lookup"><span data-stu-id="85e81-158">The complete list of language identifiers is in the Winnt.h header file, under the heading "Primary Language Ids."</span></span> <span data-ttu-id="85e81-159">Konvertieren Sie den in Winnt. h gefundenen Wert in eine Sequenz von 3 hexadezimalen Ziffern, indem Sie das `0x` Präfix entfernen und führende Ziffern hinzufügen, `0` bis die Sequenz 3 Ziffern lang ist.</span><span class="sxs-lookup"><span data-stu-id="85e81-159">Convert the value found in Winnt.h into a sequence of 3 hexadecimal digits by removing the `0x` prefix and adding leading `0` digits until the sequence is 3 digits long.</span></span> <span data-ttu-id="85e81-160">Um z. b. englische Zeichen folgen (0x9) anzugeben, verwenden Sie 009.</span><span class="sxs-lookup"><span data-stu-id="85e81-160">For example, to specify English strings (0x9), use 009.</span></span> <span data-ttu-id="85e81-161">Zum Angeben von italienischen Zeichen folgen (0x10) verwenden Sie 010.</span><span class="sxs-lookup"><span data-stu-id="85e81-161">To specify Italian strings (0x10), use 010.</span></span>

<span data-ttu-id="85e81-162">Für chinesische und portugiesische Sprachen sind sowohl die primären als auch die unter Sprachen Bezeichner erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85e81-162">Chinese and Portuguese languages require both the primary and sublanguage identifiers.</span></span> <span data-ttu-id="85e81-163">Verwenden Sie 404, 804, 416 oder 816 anstelle von 004 oder 016.</span><span class="sxs-lookup"><span data-stu-id="85e81-163">Use 404, 804, 416, or 816 instead of 004 or 016.</span></span>

### <a name="text-section"></a><span data-ttu-id="85e81-164">[Text]-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="85e81-164">[text] section</span></span>

<span data-ttu-id="85e81-165">Der `[text]` -Abschnitt enthält den Namen und die Hilfe Zeichenfolgen für die Objekte und Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="85e81-165">The `[text]` section provides the name and help strings for your objects and counters.</span></span>

<span data-ttu-id="85e81-166">Für jedes Objekt oder jeden Gegenstand und für jede unterstützte Sprache müssen Sie einen namens Schlüssel angeben (mit dem Namen oder der Titel Zeichenfolge für das Objekt oder den Counter), und Sie können optional eine Hilfe Taste (mit der Beschreibung oder der Beschreibungs Zeichenfolge für das Objekt oder den Counter) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="85e81-166">For each object or counter, and for each supported language, you must provide a NAME key (containing the name or title string for your object or counter) and you may optionally provide a HELP key (containing the description or explanation string for your object or counter).</span></span> <span data-ttu-id="85e81-167">Die Schlüssel sollten und lauten `<symbol>_<langid>_NAME` `<symbol>_<langid>_HELP` , wobei `<symbol>` die symbolische Konstante für das Objekt oder den Leistungs Bezeichner (wie in der Datei "symbolische Konstante. h" definiert) und `<langid>` die für diese Zeichenfolge verwendete Sprachen-ID ist.</span><span class="sxs-lookup"><span data-stu-id="85e81-167">The keys should be named `<symbol>_<langid>_NAME` and `<symbol>_<langid>_HELP`, where `<symbol>` is the symbolic constant for the object or counter (as defined in the symbolic constant .h file), and `<langid>` is the language identifier used for this string.</span></span>

<span data-ttu-id="85e81-168">Beispielsweise werden die englischen Zeichen folgen für einen Counter mit dem Symbol `MY_COUNTER` wie folgt angegeben:</span><span class="sxs-lookup"><span data-stu-id="85e81-168">For example, the English strings for a counter with symbol `MY_COUNTER` would be specified as:</span></span>

```ini
MY_COUNTER_009_NAME=My Counter
MY_COUNTER_009_HELP=Description for My Counter.
```

<span data-ttu-id="85e81-169">Die Text Schlüssel können in beliebiger Reihenfolge angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-169">The text keys can appear in any order.</span></span> <span data-ttu-id="85e81-170">Die Text Zeichenfolgen dürfen keine Formatierungszeichen wie Registerkarten enthalten.</span><span class="sxs-lookup"><span data-stu-id="85e81-170">The text strings should not contain formatting characters such as tabs.</span></span>

### <a name="example-ini-file"></a><span data-ttu-id="85e81-171">INI-Beispieldatei</span><span class="sxs-lookup"><span data-stu-id="85e81-171">Example INI file</span></span>

<span data-ttu-id="85e81-172">Im folgenden finden Sie ein Beispiel einer Initialisierungsdatei, die im Beispiel zum [Erstellen einer Leistungs Erweiterungs-DLL](creating-a-performance-extension-dll.md) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85e81-172">The following is an example of an initialization file that is used in the [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md) sample.</span></span>

```ini
[info]
drivername=MyApplication
symbolfile=CounterOffsets.h
trusted=

[objects]
TRANSFER_OBJECT_009_NAME=
PEER_OBJECT_009_NAME=

[languages]
009=English
00C=French

[text]

// English strings

TRANSFER_OBJECT_009_NAME=Transfer
TRANSFER_OBJECT_009_HELP=Provides information related to transferring files.

BYTES_SENT_009_NAME=Bytes Sent
BYTES_SENT_009_HELP=Number of bytes sent in the last transfer.

AVAILABLE_BANDWIDTH_009_NAME=Available Bandwidth
AVAILABLE_BANDWIDTH_009_HELP=Available bandwidth on the network, in bytes.

PEER_OBJECT_009_NAME=Peer
PEER_OBJECT_009_HELP=Provides information related to peer-caching.

BYTES_SERVED_009_NAME=Bytes Served
BYTES_SERVED_009_HELP=Number of bytes served from the cache.

// French strings

TRANSFER_OBJECT_00C_NAME=Transfert
TRANSFER_OBJECT_00C_HELP=Fournit des informations liées aux transferts de fichiers.

BYTES_SENT_00C_NAME=Octets Envoyés
BYTES_SENT_00C_HELP=Nombre d'octets envoyés dans le dernier transfert.

AVAILABLE_BANDWIDTH_00C_NAME=Bande Passante Disponible
AVAILABLE_BANDWIDTH_00C_HELP=Bande passante disponible sur le réseau, en octets.

PEER_OBJECT_00C_NAME=Pair
PEER_OBJECT_00C_HELP=Fournit des informations liées é mise en cache homologue.

BYTES_SERVED_00C_NAME=Octets Servis
BYTES_SERVED_00C_HELP=Le nombre d'octets servis du cache.
```

## <a name="running-the-lodctr-tool"></a><span data-ttu-id="85e81-173">Ausführen des lodctr-Tools</span><span class="sxs-lookup"><span data-stu-id="85e81-173">Running the Lodctr tool</span></span>

<span data-ttu-id="85e81-174">, Um die in Ihrem definierten Namen und Hilfe Zeichenfolgen zu laden. INI-Datei (während der Installation des Anbieters) führen Sie das **Lodctr** -Tool aus dem Ordner aus, der die enthält. INI-Datei und Header Datei.</span><span class="sxs-lookup"><span data-stu-id="85e81-174">To load the names and help strings defined in your .INI file (during the installation of your provider), run the **lodctr** tool from the folder that contains your .INI file and header file.</span></span> <span data-ttu-id="85e81-175">Das Tool ist auf dem Computer enthalten.</span><span class="sxs-lookup"><span data-stu-id="85e81-175">The tool is included with the computer.</span></span> <span data-ttu-id="85e81-176">Sie müssen **Lodctr** mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="85e81-176">You must run **lodctr** with elevated privileges.</span></span> <span data-ttu-id="85e81-177">Der-Parameter für **Lodctr** ist der Pfad zu Ihrem. INI-Datei.</span><span class="sxs-lookup"><span data-stu-id="85e81-177">The parameter to **lodctr** is the path to your .INI file.</span></span> <span data-ttu-id="85e81-178">Beispiel: `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span><span class="sxs-lookup"><span data-stu-id="85e81-178">For example, `lodctr "C:\Program Files\MyCompany\MyProvider\MyProvider.ini"`.</span></span>

<span data-ttu-id="85e81-179">Zum Entladen der Namen und Hilfe Zeichenfolgen (während der Deinstallation) führen Sie das **unlodctr** -Tool aus.</span><span class="sxs-lookup"><span data-stu-id="85e81-179">To unload the names and help strings (during uninstall), run the **unlodctr** tool.</span></span> <span data-ttu-id="85e81-180">Sie müssen **unlodctr** mit erhöhten Rechten ausführen.</span><span class="sxs-lookup"><span data-stu-id="85e81-180">You must run **unlodctr** with elevated privileges.</span></span> <span data-ttu-id="85e81-181">Der Parameter für **unlodctr** ist der DriverName des Anbieters (der Name des Leistungs Schlüssels des Anbieters).</span><span class="sxs-lookup"><span data-stu-id="85e81-181">The parameter to **unlodctr** is the DriverName of your provider (the name of the provider's performance key).</span></span> <span data-ttu-id="85e81-182">Beispiel: `unlodctr "MyProvider"`.</span><span class="sxs-lookup"><span data-stu-id="85e81-182">For example, `unlodctr "MyProvider"`.</span></span>

<span data-ttu-id="85e81-183">Vergewissern Sie sich vor dem Ausführen von **Lodctr**, dass Ihre Anwendung über einen Eintrag unter dem **Dienst** Schlüssel verfügt.</span><span class="sxs-lookup"><span data-stu-id="85e81-183">Before running **lodctr**, be sure that your application has an entry under the **Services** key.</span></span> <span data-ttu-id="85e81-184">Weitere Informationen finden Sie unter [Erstellen des Leistungs Schlüssels der Anwendung](creating-the-applications-performance-key.md).</span><span class="sxs-lookup"><span data-stu-id="85e81-184">For details, see [Creating the Application's Performance Key](creating-the-applications-performance-key.md).</span></span> <span data-ttu-id="85e81-185">Wenn der Schlüssel nicht vorhanden ist, wird die Registrierung von **Lodctr** nicht mit ihren Namen und Beschreibungen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="85e81-185">If the key does not exist, **lodctr** will not update the registry with your names and descriptions.</span></span>

<span data-ttu-id="85e81-186">Als Alternative zum Ausführen von **Lodctr** können Sie [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (definiert in "LoadPerf. h") aus dem Installationsprogramm abrufen, um die Beschreibungen der Indikator Namen zu laden.</span><span class="sxs-lookup"><span data-stu-id="85e81-186">As an alternative to running **lodctr**, you can call [**LoadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-loadperfcountertextstringsw) (defined in Loadperf.h) from your installation program to load your counter names descriptions.</span></span> <span data-ttu-id="85e81-187">Sie können dann [**unloadperfcountertextstrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) während der Deinstallation von aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="85e81-187">You can then call [**UnloadPerfCounterTextStrings**](/windows/win32/api/loadperf/nf-loadperf-unloadperfcountertextstringsw) during uninstall.</span></span>

<span data-ttu-id="85e81-188">Das Hilfsprogramm **Lodctr** kopiert die Zeichen folgen aus. INI **-Datei** zu den Indikatoren und **Hilfe** Registrierungs Werten unter den entsprechenden sprach unter Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="85e81-188">The **lodctr** utility copies the strings from the .INI file to the **Counters** and **Help** registry values under the appropriate language subkeys.</span></span> <span data-ttu-id="85e81-189">Wenn der entsprechende sprach Unterschlüssel nicht vorhanden ist, werden die Zeichen folgen für diese Sprache nicht kopiert.</span><span class="sxs-lookup"><span data-stu-id="85e81-189">If the corresponding language subkey does not exist, the strings for that language are not copied.</span></span> <span data-ttu-id="85e81-190">Das Hilfsprogramm aktualisiert auch den letzten Wert des **Zählers** und den **letzten Hilfe** Wert.</span><span class="sxs-lookup"><span data-stu-id="85e81-190">The utility also updates the **Last Counter** and **Last Help** value.</span></span> <span data-ttu-id="85e81-191">Die Namen und Beschreibungen von Leistungs Zählern werden an folgendem Speicherort in der Registrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="85e81-191">The performance counter names and descriptions are stored in the following location in the registry.</span></span>

```
HKEY_LOCAL_MACHINE
   \SOFTWARE
      \Microsoft
         \Windows NT
            \CurrentVersion
               \Perflib
                  Last Counter = highest counter index
                  Last Help = highest help index
                  \009
                     Counters = 2 System 4 Memory...
                     Help = 3 The System Object Type...
                  \supported language, other than English
                     Counters = ...
                     Help = ...
```

<span data-ttu-id="85e81-192">Zusätzlich zum Hinzufügen von Werten unter dem **Perflib** -Schlüssel fügt das **Lodctr** -Tool auch die folgenden Werte zum Knoten **Dienste** für die Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="85e81-192">In addition to adding values under the **PerfLib** key, the **lodctr** tool also adds the following values to the **Services** node for the application.</span></span> <span data-ttu-id="85e81-193">In den meisten Fällen haben die Anwendung und der Anbieter eine 1:1-Beziehung. Es ist jedoch möglich, dass ein Anbieter gegen Daten für mehrere Anwendungen bereitstellt. aus diesem Grund basiert der Schlüssel auf der Anwendung und nicht auf dem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="85e81-193">In most cases, the application and provider will have a one-to-one relationship; however, it is possible for a provider to provide counter data for multiple applications, which is why the key is based on the application and not the provider.</span></span>

```
HKEY_LOCAL_MACHINE
   \SYSTEM
      \CurrentControlSet
         \Services
            \MyApplication
               \Performance
                  First Counter = lowest counter index assigned to provider
                  First Help = lowest help index assigned to provider
                  Last Counter = highest counter index assigned to provider
                  Last Help = highest help index assigned to provider
                  Object List = list of object index values if the .INI includes the [objects] section
                  Library Validation Code = if the [info] section contains a "trusted" key
```
