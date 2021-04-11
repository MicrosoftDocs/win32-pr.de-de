---
description: Vorbereiten einer Ressourcen Konfigurationsdatei
ms.assetid: 292b57ea-1c7e-49b6-876c-4ad307a2ec43
title: Vorbereiten einer Ressourcen Konfigurationsdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac162ad7f6d20148e0ef60cb9dc15da41cc27186
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128925"
---
# <a name="preparing-a-resource-configuration-file"></a><span data-ttu-id="55362-103">Vorbereiten einer Ressourcen Konfigurationsdatei</span><span class="sxs-lookup"><span data-stu-id="55362-103">Preparing a Resource Configuration File</span></span>

<span data-ttu-id="55362-104">Sowohl das in den [Ressourcen Dienstprogrammen](resource-utilities.md) beschriebene-Compilerdienstprogramm "muunct" als auch "RC" stellen eine Befehlszeilenoption bereit, mit der Sie eine Ressourcen Konfigurationsdatei für die Basis Sprachen Ressourcen angeben können</span><span class="sxs-lookup"><span data-stu-id="55362-104">Both the MUIRCT and the RC Compiler utilities described in [Resource Utilities](resource-utilities.md) provide a command line option that allows you to specify a resource configuration file for the base language resources.</span></span> <span data-ttu-id="55362-105">Die Verwendung dieser öffentlichen, lesbaren XML-Datei ermöglicht mehr Kontrolle über das Aufteilen von Ressourcen, als über die regulären Befehls Zeilenschalter der Hilfsprogramme abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="55362-105">Use of this public, human-readable XML file allows more control over the splitting of resources than can be obtained using the regular command line switches of the utilities.</span></span> <span data-ttu-id="55362-106">Auch wenn Sie keine Ressourcen Konfigurationsdatei als Eingabe bereitstellen, enthalten die LN-und sprachspezifischen Ressourcen Dateien Ressourcen Konfigurationsdaten.</span><span class="sxs-lookup"><span data-stu-id="55362-106">However, even if you do not provide a resource configuration file as an input, the LN and language-specific resource files will contain resource configuration data.</span></span>

<span data-ttu-id="55362-107">Alle Ressourcen Konfigurationsdateien für Win32-Anwendungen beginnen und enden identisch:</span><span class="sxs-lookup"><span data-stu-id="55362-107">All resource configuration files for Win32 applications begin and end identically:</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>

<resources>
        
        <!-- a single win32Resources element goes here -->

</resources>
</localization>
```



<span data-ttu-id="55362-108">Dieses Thema konzentriert sich auf die Aspekte des XML-Schemas, die beim Entwickeln von nicht verwaltetem Code unter Windows Vista und höher nützlich sind.</span><span class="sxs-lookup"><span data-stu-id="55362-108">This topic focuses on the aspects of the XML schema that are useful in building unmanaged code on Windows Vista and later.</span></span> <span data-ttu-id="55362-109">Insbesondere geht es nur um das Verhalten des win32Resources-Elements.</span><span class="sxs-lookup"><span data-stu-id="55362-109">In particular, it is only concerned with the behavior of the win32Resources element.</span></span>

## <a name="win32resources-element"></a><span data-ttu-id="55362-110">win32Resources-Element</span><span class="sxs-lookup"><span data-stu-id="55362-110">win32Resources Element</span></span>

<span data-ttu-id="55362-111">Das win32Resources-Element verfügt über die in der folgenden Tabelle beschriebenen Attribute.</span><span class="sxs-lookup"><span data-stu-id="55362-111">The win32Resources element has the attributes described in the following table.</span></span>



| <span data-ttu-id="55362-112">Attributname</span><span class="sxs-lookup"><span data-stu-id="55362-112">Attribute name</span></span>           | <span data-ttu-id="55362-113">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="55362-113">Mandatory</span></span> | <span data-ttu-id="55362-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55362-114">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55362-115">fileType</span><span class="sxs-lookup"><span data-stu-id="55362-115">fileType</span></span>                 | <span data-ttu-id="55362-116">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-116">No</span></span>        | <span data-ttu-id="55362-117">Dateityp.</span><span class="sxs-lookup"><span data-stu-id="55362-117">Type of file.</span></span> <span data-ttu-id="55362-118">Sollte immer "Application" lauten.</span><span class="sxs-lookup"><span data-stu-id="55362-118">Should always be "Application".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="55362-119">Prüfsumme</span><span class="sxs-lookup"><span data-stu-id="55362-119">checksum</span></span>                 | <span data-ttu-id="55362-120">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-120">No</span></span>        | <span data-ttu-id="55362-121">Der Prüfsummen Wert, der in den Ressourcen Konfigurationsdaten der LN-Datei und der sprachspezifischen Ressourcen Dateien angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55362-121">Checksum value to appear in the resource configuration data of the LN file and language-specific resource files.</span></span> <span data-ttu-id="55362-122">Mit diesem Attribut können Sie z. b. die Prüfsumme aus einer einzelnen sprachspezifischen Ressourcen Datei kopieren, gemäß der Konvention für Englisch (USA), und platzieren Sie die Prüfsumme in einer anderen sprachspezifischen Ressourcen Datei.</span><span class="sxs-lookup"><span data-stu-id="55362-122">For example, this attribute allows you to copy the checksum from a single language-specific resource file, by convention the one for English (United States), and place the checksum in a different language-specific resource file.</span></span> <span data-ttu-id="55362-123">Die Prüfsumme kann als hexadezimale Zahlen Zeichenfolge angegeben werden, die nicht länger als 32 Zeichen ist.</span><span class="sxs-lookup"><span data-stu-id="55362-123">The checksum can be specified as a hexadecimal number string that is no longer than 32 characters.</span></span> <span data-ttu-id="55362-124">Der numerische Wert muss in eine 128-Bit-Zahl containerbar sein.</span><span class="sxs-lookup"><span data-stu-id="55362-124">The numerical value must be containable in a 128-bit number.</span></span> |
| <span data-ttu-id="55362-125">language</span><span class="sxs-lookup"><span data-stu-id="55362-125">language</span></span>                 | <span data-ttu-id="55362-126">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-126">No</span></span>        | <span data-ttu-id="55362-127">Die Sprache wird mit einem Namensformat angegeben, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. b. "en-US" für Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="55362-127">Language specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="55362-128">ultimatefallbacklanguage</span><span class="sxs-lookup"><span data-stu-id="55362-128">ultimateFallbackLanguage</span></span> | <span data-ttu-id="55362-129">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-129">No</span></span>        | <span data-ttu-id="55362-130">Die Sprache, die in die Ressourcen Konfigurationsdaten für die LN-Datei eingefügt werden soll, und stellt die endgültige Fall Back Sprache dar, die bei einer Suche nach einer entsprechenden sprachspezifischen Ressourcen Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="55362-130">Language to insert into the resource configuration data for the LN file, representing the ultimate fallback language to use in a search for a corresponding language-specific resource file.</span></span> <span data-ttu-id="55362-131">Wenn das Ressourcen Lade Modul eine angeforderte Ressourcen Datei nicht von den bevorzugten Benutzeroberflächen Sprachen des Threads lädt, wird als letzter Versuch eine ultimative Fall Back Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="55362-131">If the resource loader fails to load a requested resource file from the thread preferred UI languages, it uses an ultimate fallback language as its last attempt.</span></span> <span data-ttu-id="55362-132">Die Sprache wird mit einem Namensformat angegeben, das mit RFC 4646 (Windows Vista und höher) kompatibel ist, z. b. en-US für Englisch (USA).</span><span class="sxs-lookup"><span data-stu-id="55362-132">The language is specified using a name format compliant with RFC 4646 (Windows Vista and later), for example, en-US for English (United States).</span></span>       |
| <span data-ttu-id="55362-133">ultimatefallbacklocation</span><span class="sxs-lookup"><span data-stu-id="55362-133">ultimateFallbackLocation</span></span> | <span data-ttu-id="55362-134">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-134">No</span></span>        | <span data-ttu-id="55362-135">Fall Back Speicherort.</span><span class="sxs-lookup"><span data-stu-id="55362-135">Fallback location.</span></span> <span data-ttu-id="55362-136">Geben Sie "Internal" an, wenn Ultimate-Fall Back Ressourcen in die LN-Datei kompiliert werden.</span><span class="sxs-lookup"><span data-stu-id="55362-136">Specify "internal" if ultimate fallback resources are compiled into the LN file.</span></span> <span data-ttu-id="55362-137">Geben Sie "extern" (Standard) an, wenn die LN-Datei auf eine sprachspezifische Ressourcen Datei für die letzten Fall Back Ressourcen verweisen soll.</span><span class="sxs-lookup"><span data-stu-id="55362-137">Specify "external" (default) if the LN file is to reference a language-specific resource file for its ultimate fallback resources.</span></span>                                                                                                                                                                                                                                                                                |



 

<span data-ttu-id="55362-138">In der Ressourcen Konfigurationsdatei enthält das win32Resources-Element die untergeordneten Elemente, die in der folgenden Tabelle beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="55362-138">In the resource configuration file, the win32Resources element has the sub-elements described in the next table.</span></span>



| <span data-ttu-id="55362-139">Elementname</span><span class="sxs-lookup"><span data-stu-id="55362-139">Element Name</span></span>       | <span data-ttu-id="55362-140">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55362-140">Description</span></span>                                                                                                                              |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55362-141">Das localizedresources</span><span class="sxs-lookup"><span data-stu-id="55362-141">localizedResources</span></span> | <span data-ttu-id="55362-142">Ressourcen, die Informationen zu den Ressourcentypen und den einzelnen Ressourcen enthalten, die in einer sprachspezifischen Ressourcen Datei enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="55362-142">Resources that encapsulate information about the resource types and individual resources contained in a language-specific resource file.</span></span> |
| <span data-ttu-id="55362-143">neutralresources</span><span class="sxs-lookup"><span data-stu-id="55362-143">neutralResources</span></span>   | <span data-ttu-id="55362-144">Ressourcen, die Informationen zu den in einer LN-Datei enthaltenen Ressourcentypen Kapseln.</span><span class="sxs-lookup"><span data-stu-id="55362-144">Resources that encapsulate information about the resource types contained in an LN file.</span></span>                                                 |



 

## <a name="localizedresources-element"></a><span data-ttu-id="55362-145">localizedresources-Element</span><span class="sxs-lookup"><span data-stu-id="55362-145">localizedResources Element</span></span>

<span data-ttu-id="55362-146">Lokalisiertes Ressourcen Element.</span><span class="sxs-lookup"><span data-stu-id="55362-146">Localized resources element.</span></span> <span data-ttu-id="55362-147">Standardmäßig hat dieses Element keine Attribute und nur einen Typ von Unterelement.</span><span class="sxs-lookup"><span data-stu-id="55362-147">By default, this element has no attributes and only one type of sub-element.</span></span> <span data-ttu-id="55362-148">Es handelt sich lediglich um einen Container für ResourceType-Elemente.</span><span class="sxs-lookup"><span data-stu-id="55362-148">It is just a container for resourceType elements.</span></span>



| <span data-ttu-id="55362-149">Attributname</span><span class="sxs-lookup"><span data-stu-id="55362-149">Attribute Name</span></span> | <span data-ttu-id="55362-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55362-150">Description</span></span>                                                                    |
|----------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="55362-151">resourceType</span><span class="sxs-lookup"><span data-stu-id="55362-151">resourceType</span></span>   | <span data-ttu-id="55362-152">Der Typ einer einzelnen Ressource, die in einer sprachspezifischen Ressourcen Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="55362-152">Type of an individual resource contained in a language-specific resource file.</span></span> |



 

## <a name="neutralresources-element"></a><span data-ttu-id="55362-153">neutralresources-Element</span><span class="sxs-lookup"><span data-stu-id="55362-153">neutralResources Element</span></span>

<span data-ttu-id="55362-154">Neutrales Ressourcen Element.</span><span class="sxs-lookup"><span data-stu-id="55362-154">Neutral resources element.</span></span> <span data-ttu-id="55362-155">Dieses Element ist nur ein Container für ResourceType-Elemente.</span><span class="sxs-lookup"><span data-stu-id="55362-155">This element is just a container for resourceType elements.</span></span>



| <span data-ttu-id="55362-156">Attributname</span><span class="sxs-lookup"><span data-stu-id="55362-156">Attribute Name</span></span> | <span data-ttu-id="55362-157">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55362-157">Description</span></span>                                        |
|----------------|----------------------------------------------------|
| <span data-ttu-id="55362-158">resourceType</span><span class="sxs-lookup"><span data-stu-id="55362-158">resourceType</span></span>   | <span data-ttu-id="55362-159">Der Typ einer einzelnen Ressource, die in einer LN-Datei enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="55362-159">Type of a single resource contained in an LN file.</span></span> |



 

## <a name="resourcetype-element"></a><span data-ttu-id="55362-160">ResourceType-Element</span><span class="sxs-lookup"><span data-stu-id="55362-160">resourceType Element</span></span>

<span data-ttu-id="55362-161">Das ResourceType-Element kapselt Informationen zu einem einzelnen Ressourcentyp oder einer einzelnen Ressource.</span><span class="sxs-lookup"><span data-stu-id="55362-161">The resourceType element encapsulates information about a single resource type or individual resource.</span></span> <span data-ttu-id="55362-162">Die Attribute sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="55362-162">It has the attributes listed below.</span></span>

> [!Caution]  
> <span data-ttu-id="55362-163">Einige Ressourcen Konfigurationsfehler werden nur durch den RC-Compiler oder muunct abgefangen, abhängig von der Eingabe Ressourcen Datei oder dem Binärdatei Inhalt.</span><span class="sxs-lookup"><span data-stu-id="55362-163">Some resource configuration defects are caught only by RC Compiler or MUIRCT, depending on the input resource file or binary file content.</span></span> <span data-ttu-id="55362-164">Die ResourceType-Fehler in der Ressourcen Konfigurationsdatei, die in der Eingabedatei nicht vorhanden sind, werden nicht abgefangen, was zu unerwartetem Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="55362-164">The resourceType errors in the resource configuration file that do not exist in the input file are not caught, resulting in unexpected behavior.</span></span> <span data-ttu-id="55362-165">Benutzer können eine fehlerhafte Ressourcen Konfigurationsdatei verwenden und wissen nicht, bis Sie Binärdateien einführen, die die fehlerhaften Teile der Ressourcen Konfigurationsdatei verwenden. Dadurch wird die Darstellung der Unterbrechungen aus den aktuellen Binärdateien erstellt.</span><span class="sxs-lookup"><span data-stu-id="55362-165">Users can be using a defective resource configuration file and do not know until they introduce binaries that use the broken parts of the resource configuration file, which creates the appearance that the breaks are from the current binaries.</span></span>

 



| <span data-ttu-id="55362-166">Attributname</span><span class="sxs-lookup"><span data-stu-id="55362-166">Attribute name</span></span> | <span data-ttu-id="55362-167">Obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="55362-167">Mandatory</span></span> | <span data-ttu-id="55362-168">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="55362-168">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|----------------|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55362-169">typameid</span><span class="sxs-lookup"><span data-stu-id="55362-169">typeNameId</span></span>     | <span data-ttu-id="55362-170">Ja</span><span class="sxs-lookup"><span data-stu-id="55362-170">Yes</span></span>       | <span data-ttu-id="55362-171">Typname oder Bezeichner für die Ressource.</span><span class="sxs-lookup"><span data-stu-id="55362-171">Type name or identifier for the resource.</span></span> <span data-ttu-id="55362-172">Geben Sie einen Zeichen folgen Namen oder eine Zahl an.</span><span class="sxs-lookup"><span data-stu-id="55362-172">Specify a string name or a number.</span></span> <span data-ttu-id="55362-173">Wenn eine Zahl verwendet wird, wird der Zeichenfolge ein " \# " vorangestellt, um anzugeben, dass es sich um eine Zahl handelt.</span><span class="sxs-lookup"><span data-stu-id="55362-173">If using a number, prepend the string with a "\#" to indicate that it represents a number.</span></span> <span data-ttu-id="55362-174">Jedes ResourceType-Element darf nur über ein *typenameid* -Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="55362-174">Each resourceType element must have only one *typeNameId* attribute.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="55362-175">itemName</span><span class="sxs-lookup"><span data-stu-id="55362-175">itemName</span></span>       | <span data-ttu-id="55362-176">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-176">No</span></span>        | <span data-ttu-id="55362-177">Die Elementnamen Zeichenfolge für die Ressource, die in der sprachspezifischen Ressourcen Datei abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55362-177">Item name string for the resource, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="55362-178">Sie können mehrere Namen angeben, die durch Leerzeichen getrennt sind, z. b. "HTML-MUF-Daten".</span><span class="sxs-lookup"><span data-stu-id="55362-178">You can specify multiple names, separated by white spaces, for example, "HTML MOFDATA".</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="55362-179">itemId</span><span class="sxs-lookup"><span data-stu-id="55362-179">itemId</span></span>         | <span data-ttu-id="55362-180">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-180">No</span></span>        | <span data-ttu-id="55362-181">Der Bezeichner des einzelnen Ressourcen Elements, das in der sprachspezifischen Ressourcen Datei abgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55362-181">Identifier of individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="55362-182">Das Element kann als Bereich (z. b. "1-12") oder von einzelnen bezeichlern, getrennt durch Leerzeichen (z. b. "1 3 4"), angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="55362-182">The item can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="55362-183">stringId</span><span class="sxs-lookup"><span data-stu-id="55362-183">stringId</span></span>       | <span data-ttu-id="55362-184">Nein</span><span class="sxs-lookup"><span data-stu-id="55362-184">No</span></span>        | <span data-ttu-id="55362-185">Der Zeichen folgen Bezeichner für das einzelne Ressourcen Element, das in die sprachspezifische Ressourcen Datei eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="55362-185">String identifier for individual resource item, to be placed in the language-specific resource file.</span></span> <span data-ttu-id="55362-186">Die Zeichenfolge kann als Bereich (z. b. "1-12") oder von einzelnen bezeichlern, getrennt durch Leerzeichen (z. b. "1 3 4"), angegeben werden. Dieses Attribut ermöglicht die Angabe von lokalisierbaren und nicht lokalisierbaren Zeichen folgen Tabellen Einträgen.</span><span class="sxs-lookup"><span data-stu-id="55362-186">The string can be specified as a range (for example, "1-12") or by individual identifiers separated by white spaces (for example, "1 3 4").This attribute allows the specification of both localizable and nonlocalizable string table entries.</span></span> <span data-ttu-id="55362-187">Er muss in Verbindung mit dem *tytzameid* -Wert "6" verwendet werden, der den Ressourcentyp "String Table Entry" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="55362-187">It must be used in conjunction with the *typeNameId* value of "6", denoting a string table entry resource type.</span></span><br/> <span data-ttu-id="55362-188">Zeichen folgen werden in Blöcken von 16 in einer Zeichen folgen Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="55362-188">Strings are stored in blocks of 16 in a string table.</span></span> <span data-ttu-id="55362-189">Die Zeichen folgen 0 bis 15 werden z. b. in einem einzelnen Ressourcen Element Block gespeichert, und in der Ressourcen Konfigurationsdatei kann als *ItemID* 1 oder als *stringID* "0-15" verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="55362-189">For example, strings 0 to 15 are stored in a single resource item block and can be referenced in the resource configuration file as *itemId* 1, or as *stringId* "0-15".</span></span> <span data-ttu-id="55362-190">Wenn beispielsweise fünf lokalisierbare Zeichen folgen und drei nicht lokalisierbare Zeichen folgen vorhanden sind, sollten Sie Zeichen folgen Bezeichner 0-4 für die lokalisierbaren Zeichen folgen und Zeichen folgen Bezeichner 16-18 für die nicht lokalisierbaren Zeichen folgen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="55362-190">For example, if there are five localizable strings and three nonlocalizable strings, you should assign string identifiers 0-4 for the localizable strings, and string identifiers 16-18 for the nonlocalizable strings.</span></span> <span data-ttu-id="55362-191">Wenn Sie Zeichen folgen nicht auf diese Weise organisieren, werden die betroffenen Zeichen folgen Blöcke sowohl in der LN-Datei als auch in der sprachspezifischen Ressourcen Datei platziert.</span><span class="sxs-lookup"><span data-stu-id="55362-191">If you do not organize strings this way, the affected blocks of strings are placed in both the LN file and the language-specific resource file.</span></span><br/> |



 

<span data-ttu-id="55362-192">Wenn Sie die Attribute *ItemName*, *ItemID* und/oder *stringID* für einen bestimmten Ressourcentyp unter dem localizedresource-Element angeben, werden nur die angegebenen Elemente bzw. Zeichen folgen für den angegebenen Ressourcentyp in die sprachspezifische Ressourcen Datei eingefügt.</span><span class="sxs-lookup"><span data-stu-id="55362-192">If you specify the *itemName*, *itemId*, and/or *stringId* attributes for a particular resource type under the localizedResource element, only these specified items or strings for the designated resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="55362-193">Wenn ein ResourceType-Element ohne einen expliziten Elementnamen, Element Bezeichner oder Zeichen folgen Bezeichner angegeben wird, werden alle Elemente des angegebenen Ressourcentyps in der sprachspezifischen Ressourcen Datei abgelegt.</span><span class="sxs-lookup"><span data-stu-id="55362-193">If a resourceType element is specified without any explicit item name, item identifier, or string identifier, all items of the specified resource type are placed in the language-specific resource file.</span></span> <span data-ttu-id="55362-194">Elemente oder Typen, die nicht in einem localizedresource-Element aufgelistet sind, werden in die LN-Datei eingefügt.</span><span class="sxs-lookup"><span data-stu-id="55362-194">Items or types not listed in any localizedResource element are placed in the LN file.</span></span>

<span data-ttu-id="55362-195">Im folgenden sind die Standard Ressourcentypen und deren numerische Bezeichner aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="55362-195">The following are the standard resource types and their numeric identifiers:</span></span>

-   <span data-ttu-id="55362-196">Cursor (1)</span><span class="sxs-lookup"><span data-stu-id="55362-196">CURSOR(1)</span></span>
-   <span data-ttu-id="55362-197">Bitmap (2)</span><span class="sxs-lookup"><span data-stu-id="55362-197">BITMAP(2)</span></span>
-   <span data-ttu-id="55362-198">Symbol (3)</span><span class="sxs-lookup"><span data-stu-id="55362-198">ICON(3)</span></span>
-   <span data-ttu-id="55362-199">Menü (4)</span><span class="sxs-lookup"><span data-stu-id="55362-199">MENU(4)</span></span>
-   <span data-ttu-id="55362-200">Dialog (5)</span><span class="sxs-lookup"><span data-stu-id="55362-200">DIALOG(5)</span></span>
-   <span data-ttu-id="55362-201">Zeichenfolge (6)</span><span class="sxs-lookup"><span data-stu-id="55362-201">STRING(6)</span></span>
-   <span data-ttu-id="55362-202">Fontdir (7)</span><span class="sxs-lookup"><span data-stu-id="55362-202">FONTDIR(7)</span></span>
-   <span data-ttu-id="55362-203">Schriftart (8)</span><span class="sxs-lookup"><span data-stu-id="55362-203">FONT(8)</span></span>
-   <span data-ttu-id="55362-204">Accelerators (9)</span><span class="sxs-lookup"><span data-stu-id="55362-204">ACCELERATORS(9)</span></span>
-   <span data-ttu-id="55362-205">RCDATA (10)</span><span class="sxs-lookup"><span data-stu-id="55362-205">RCDATA(10)</span></span>
-   <span data-ttu-id="55362-206">Messagetable (11)</span><span class="sxs-lookup"><span data-stu-id="55362-206">MESSAGETABLE(11)</span></span>
-   <span data-ttu-id="55362-207">Gruppen \_ Cursor (12)</span><span class="sxs-lookup"><span data-stu-id="55362-207">GROUP\_CURSOR(12)</span></span>
-   <span data-ttu-id="55362-208">Gruppen \_ Symbol (14)</span><span class="sxs-lookup"><span data-stu-id="55362-208">GROUP\_ICON(14)</span></span>
-   <span data-ttu-id="55362-209">Version (16)</span><span class="sxs-lookup"><span data-stu-id="55362-209">VERSION(16)</span></span>
-   <span data-ttu-id="55362-210">HTML (23)</span><span class="sxs-lookup"><span data-stu-id="55362-210">HTML(23)</span></span>

## <a name="example"></a><span data-ttu-id="55362-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="55362-211">Example</span></span>


```C++
<?xml version="1.0" encoding="utf-8"?> 
<localization>
  <resources>
    <win32Resources fileType="Application">
      <neutralResources>
        <resourceType
           typeNameId="#16"
        />
      </neutralResources>
      <localizedResources> 
         <resourceType
                typeNameId="#2"
                itemId="5 6 7 8 9 10 11 12"
                itemName="HTML PRI"
         />
         <resourceType
                typeNameId="#4"
         />
         <resourceType
                typeNameId="#5"
         />
         <resourceType
                typeNameId="#6"
         />
         <resourceType
                typeNameId="#9"
         />
         <resourceType
                typeNameId="#11"
         />
         <resourceType
                typeNameId="#16"
         />
         <resourceType
                typeNameId="HTML"
         />
         <resourceType
                typeNameId="#23"
         />
         <resourceType
                typeNameId="#240"
         />
         <resourceType
                typeNameId="#1024"
         />
         <resourceType
                typeNameId="MY_TYPE"
         />
      </localizedResources> 
    </win32Resources>
  </resources>
</localization>
```



## <a name="remarks"></a><span data-ttu-id="55362-212">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55362-212">Remarks</span></span>

<span data-ttu-id="55362-213">Wenn Sie ein beliebiges Symbol (3), einen Dialog (5), einen Zeichen folgen-(6) oder einen Versions (16) Ressourcentyp im neutralresources-Element enthalten, müssen Sie diesen Eintrag im localizedresources-Element duplizieren.</span><span class="sxs-lookup"><span data-stu-id="55362-213">If you include any ICON(3), DIALOG(5), STRING(6), or VERSION(16) resource type in the neutralResources element, then you have to duplicate that entry in the localizedResources element.</span></span> <span data-ttu-id="55362-214">Sie können dies im obigen Beispiel veranschaulichen, wobei der Ressourcentyp 16 sowohl in neutralen als auch in lokalisierten Ressourcen Abschnitten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="55362-214">You can see this illustrated in the example above, where resource type 16 appears in both neutral and localized resources sections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="55362-215">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="55362-215">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55362-216">Vorbereiten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="55362-216">Preparing Resources</span></span>](preparing-resources.md)
</dt> </dl>

 

 




