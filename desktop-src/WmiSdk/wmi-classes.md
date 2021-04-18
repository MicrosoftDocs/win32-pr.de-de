---
description: Dieser Abschnitt enthält Informationen zur WMI-Klassen-und-Referenzseite.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: WMI-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa764d39c1fb048e125898a1f7e6d5cadf7f127d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368235"
---
# <a name="wmi-classes"></a><span data-ttu-id="78834-103">WMI-Klassen</span><span class="sxs-lookup"><span data-stu-id="78834-103">WMI Classes</span></span>

<span data-ttu-id="78834-104">Dieser Abschnitt enthält Informationen zur WMI-Klassen-und-Referenzseite.</span><span class="sxs-lookup"><span data-stu-id="78834-104">This section provides WMI class and reference page information.</span></span> <span data-ttu-id="78834-105">Weitere Informationen zum Abrufen von Klassen-oder Instanzdaten finden Sie unter Bearbeiten von [Klassen-und Instanzinformationen](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="78834-105">For more information about how to retrieve class or instance data, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span> <span data-ttu-id="78834-106">In der folgenden Liste sind Links zu bestimmten WMI-Klassen Informationen aufgelistet, beschrieben und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="78834-106">The following list lists, describes, and provides links to specific WMI class information.</span></span> <span data-ttu-id="78834-107">Weitere Informationen und Skriptcode Beispiele für die Verwendung von WMI-Klassen zum Abrufen einer Vielzahl von Betriebssystem-und Hardware Daten finden Sie unter [WMI-Tasks für Skripts und Anwendungen](wmi-tasks-for-scripts-and-applications.md).</span><span class="sxs-lookup"><span data-stu-id="78834-107">For more information and script code examples of using WMI classes to obtain a variety of operating system and hardware data, see [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="78834-108">Beispiele in C++ finden Sie unter [WMI C++ Application examples](wmi-c---application-examples.md).</span><span class="sxs-lookup"><span data-stu-id="78834-108">For examples in C++, see [WMI C++ Application Examples](wmi-c---application-examples.md).</span></span> <span data-ttu-id="78834-109">[Beim Herstellen einer Verbindung mit WMI auf einem Remote Computer](connecting-to-wmi-on-a-remote-computer.md) wird das Abrufen von Remote Daten gezeigt.</span><span class="sxs-lookup"><span data-stu-id="78834-109">[Connecting to WMI on a Remote Computer](connecting-to-wmi-on-a-remote-computer.md) shows how to obtain remote data.</span></span> <span data-ttu-id="78834-110">Sie können auch PowerShell-Zugriff auf WMI-Objekte verwenden; eine Liste der WMI-Klassen, die PowerShell-Codebeispiele enthalten, finden Sie [hier](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).</span><span class="sxs-lookup"><span data-stu-id="78834-110">You can also use PowerShell do access WMI objects; for a list of WMI classes that include PowerShell code samples, see [here](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).</span></span>



| <span data-ttu-id="78834-111">`Section`</span><span class="sxs-lookup"><span data-stu-id="78834-111">Section</span></span>                                                    | <span data-ttu-id="78834-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78834-112">Description</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78834-113">WMI-System Klassen</span><span class="sxs-lookup"><span data-stu-id="78834-113">WMI System Classes</span></span>](wmi-system-classes.md)               | <span data-ttu-id="78834-114">Vordefinierte Klassen, die in jedem Namespace im WMI-Kern (Windows-Verwaltungsinstrumentation) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="78834-114">Predefined classes that are included in every namespace in the Windows Management Instrumentation (WMI) core.</span></span> <span data-ttu-id="78834-115">Sie können eine WMI-System Klasse erkennen, da der Name mit einem doppelten Unterstrich ( \_ \_ ) beginnt.</span><span class="sxs-lookup"><span data-stu-id="78834-115">You can recognize a WMI system class because the name begins with a double underscore (\_\_).</span></span> <span data-ttu-id="78834-116">Diese Klassen stellen einen großen Teil der grundlegenden Funktionen für WMI bereit.</span><span class="sxs-lookup"><span data-stu-id="78834-116">These classes provide much of the basic functionality for WMI.</span></span> <span data-ttu-id="78834-117">Die WMI-System Klassen sind den Systemtabellen in SQL Server ähnlich.</span><span class="sxs-lookup"><span data-stu-id="78834-117">The WMI system classes are similar in purpose to the system tables in SQL server.</span></span> |
| [<span data-ttu-id="78834-118">MSFT-Klassen</span><span class="sxs-lookup"><span data-stu-id="78834-118">MSFT Classes</span></span>](msft-classes.md)                           | <span data-ttu-id="78834-119">Andere Microsoft-Klassen, die die Möglichkeit bieten, mehrere Betriebssystemfunktionen zu bearbeiten, wie z. b. Remote Ereignisse und Richtlinien Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="78834-119">Other Microsoft classes that offer the means to manipulate several operating system features, such as remote events and policy extensions.</span></span> <span data-ttu-id="78834-120">Die [WMI-Problem](wmi-troubleshooting.md) Behandlungs Klassen sind MSFT-Klassen, die Daten zu WMI-Vorgängen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="78834-120">The [WMI Troubleshooting](wmi-troubleshooting.md) classes are MSFT classes that provide data about WMI operations.</span></span>                                                                                               |
| [<span data-ttu-id="78834-121">CIM-Klassen</span><span class="sxs-lookup"><span data-stu-id="78834-121">CIM Classes</span></span>](cimclas.md)                                 | <span data-ttu-id="78834-122">[*Common Information Model (CIM)*](gloss-c.md) -Schema Klassen.</span><span class="sxs-lookup"><span data-stu-id="78834-122">[*Common Information Model (CIM)*](gloss-c.md) schema classes.</span></span> <span data-ttu-id="78834-123">Wenn Sie eigene WMI-Klassen schreiben möchten, können Sie von einer oder mehreren dieser Klassen erben.</span><span class="sxs-lookup"><span data-stu-id="78834-123">If you want to write your own WMI classes then you can inherit from one or more of these classes.</span></span> <span data-ttu-id="78834-124">Die WMI- [Win32-Klassen](/windows/desktop/CIMWin32Prov/win32-provider) erben von den CIM-Klassen.</span><span class="sxs-lookup"><span data-stu-id="78834-124">The WMI [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider) inherit from the CIM classes.</span></span>                                                                          |
| [<span data-ttu-id="78834-125">Standard Consumer-Klassen</span><span class="sxs-lookup"><span data-stu-id="78834-125">Standard Consumer Classes</span></span>](standard-consumer-classes.md) | <span data-ttu-id="78834-126">Ein Satz von WMI-Ereignisconsumern, die eine Aktion nach dem Empfang eines beliebigen Ereignisses auslöst.</span><span class="sxs-lookup"><span data-stu-id="78834-126">A set of WMI event consumers which trigger an action upon receipt of an arbitrary event.</span></span> <span data-ttu-id="78834-127">Weitere Informationen finden Sie unter über [Wachen von Ereignissen](monitoring-events.md).</span><span class="sxs-lookup"><span data-stu-id="78834-127">For more information, see [Monitoring Events](monitoring-events.md).</span></span>                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a><span data-ttu-id="78834-128">Code Beispiele für WMI-Klassen-Skript Center</span><span class="sxs-lookup"><span data-stu-id="78834-128">WMI Class Scripting Center Code Examples</span></span>

<span data-ttu-id="78834-129">Die folgenden Codebeispiele für das Skript Center wirken sich auf mehrere WMI-Klassen über mehrere Namespaces aus.</span><span class="sxs-lookup"><span data-stu-id="78834-129">The following Scripting Center code samples affect multiple WMI classes across multiple namespaces.</span></span>



| <span data-ttu-id="78834-130">Link</span><span class="sxs-lookup"><span data-stu-id="78834-130">Link</span></span>                                                                                                                                      | <span data-ttu-id="78834-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78834-131">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78834-132">GUI-WMI-Explorer und Hilfe-Generator der WMI-Methode</span><span class="sxs-lookup"><span data-stu-id="78834-132">GUI WMI Explorer and WMI Method Help Generator</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | <span data-ttu-id="78834-133">Beispielskript, das einen GUI-WMI-Explorer und Hilfe-Generator für WMI-Methoden bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="78834-133">Sample script that provides a GUI WMI Explorer and WMI Method Help Generator.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="78834-134">WMI-Explorer-durchsuchen von WMI-Namespaces</span><span class="sxs-lookup"><span data-stu-id="78834-134">WMI Explorer Search WMI NameSpaces</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | <span data-ttu-id="78834-135">Ermöglicht es Benutzern, in allen verfügbaren Namespaces auf den angegebenen Computern nach Klassen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="78834-135">Allows users to search for classes in all of the available namespaces on the specified computers.</span></span> <span data-ttu-id="78834-136">Bei diesem Beispiel handelt es sich um die Befehlszeilen übersaison des GUI-WMI-Explorer-Beispiels, die als Erweiterung von Get-WmiObject-List angesehen werden können.</span><span class="sxs-lookup"><span data-stu-id="78834-136">This sample is the command-line verison of the GUI WMI Explorer sample, and may be considered an extension of Get-WmiObject -List.</span></span> |
| [<span data-ttu-id="78834-137">Arposh Windows-System Verwaltungs Tool</span><span class="sxs-lookup"><span data-stu-id="78834-137">Arposh Windows System Administration tool</span></span>](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | <span data-ttu-id="78834-138">Awsa wurde mit dem System Administrator erstellt.</span><span class="sxs-lookup"><span data-stu-id="78834-138">AWSA was built with the System Administrator in mind.</span></span> <span data-ttu-id="78834-139">Die Problembehandlung für Windows-Probleme erfordert ein breites Spektrum an Tools und wissen.</span><span class="sxs-lookup"><span data-stu-id="78834-139">Troubleshooting Windows issues requires a vast array of tools and knowledge.</span></span> <span data-ttu-id="78834-140">Awsa vereint diese Tools an einem zentralen Ort und bietet zusätzliche Funktionen.</span><span class="sxs-lookup"><span data-stu-id="78834-140">AWSA brings those tools together in one central location and adds additional functionality.</span></span>       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a><span data-ttu-id="78834-141">Benennungs Konventionen für WMI-Klassen und-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78834-141">Naming Conventions for WMI Classes and Properties</span></span>

<span data-ttu-id="78834-142">Eigenschaftsnamen müssen der von der verteilten Verwaltungs Task Force (DTMF) definierten Managed Object Format (MOF)-Syntax entsprechen.</span><span class="sxs-lookup"><span data-stu-id="78834-142">Property names must conform to the Managed Object Format (MOF) syntax defined by the Distributed Management Task Force (DTMF).</span></span> <span data-ttu-id="78834-143">Die anfänglichen Bezeichnerzeichen müssen aus den Buchstaben a bis z und dem Unterstrich ( \_ ) bestehen.</span><span class="sxs-lookup"><span data-stu-id="78834-143">The initial identifier characters must be from the letters a through z and the underscore character (\_).</span></span> <span data-ttu-id="78834-144">Alle weiteren Zeichen müssen aus den Buchstaben a bis z, dem Unterstrich und den Ziffern 0 bis 9 liegen.</span><span class="sxs-lookup"><span data-stu-id="78834-144">All additional characters must be from the letters a through z, the underscore character, and the numerals 0 through 9.</span></span> <span data-ttu-id="78834-145">Weitere Informationen finden Sie im Abschnitt zur Unicode-Verwendung in der [CIM-Spezifikation, Version 2,2](https://www.dmtf.org/standards/cim).</span><span class="sxs-lookup"><span data-stu-id="78834-145">For more information, see the Unicode Usage section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

<span data-ttu-id="78834-146">SQL-Reserve Wörter sollten nicht in Klassen-und Eigenschaftsnamen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78834-146">SQL reserve words should not be used in class and property names.</span></span> <span data-ttu-id="78834-147">Eine vollständige Liste der SQL-Reserve Wörter und weitere Informationen finden Sie im Abschnitt "Richtlinien" in der [CIM-Spezifikation, Version 2,2](https://www.dmtf.org/standards/cim).</span><span class="sxs-lookup"><span data-stu-id="78834-147">For a complete list of the SQL reserve words and for more information, see the Guidelines section of the [CIM Specification Version 2.2](https://www.dmtf.org/standards/cim).</span></span>

## <a name="document-conventions-for-a-wmi-class-reference-page"></a><span data-ttu-id="78834-148">Dokument Konventionen für eine WMI-Klassenreferenz Seite</span><span class="sxs-lookup"><span data-stu-id="78834-148">Document Conventions for a WMI Class Reference Page</span></span>

<span data-ttu-id="78834-149">In diesem Abschnitt werden die Dokument Konventionen für eine WMI-Klassen Verweisseite identifiziert und beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78834-149">This section identifies and describes the document conventions for a WMI class reference page.</span></span>

<span data-ttu-id="78834-150">Eine typische Referenzseite enthält einen Syntax Block, eine Methoden Tabelle und eine Eigenschaften Liste.</span><span class="sxs-lookup"><span data-stu-id="78834-150">A typical reference page contains a syntax block, methods table, and a properties list.</span></span>

-   <span data-ttu-id="78834-151">Syntaxblock</span><span class="sxs-lookup"><span data-stu-id="78834-151">Syntax block</span></span>

    <span data-ttu-id="78834-152">Eine vereinfachte Version von MOF-Code, die den Klassennamen, die übergeordnete Klasse (sofern vorhanden) und die Klasseneigenschaften in alphabetischer Reihenfolge mit Datentypen enthält.</span><span class="sxs-lookup"><span data-stu-id="78834-152">A simplified version of MOF code that includes the class name, parent class (if any), and class properties, in alphabetical order, with data types.</span></span>

-   <span data-ttu-id="78834-153">Tabelle "Methoden"</span><span class="sxs-lookup"><span data-stu-id="78834-153">Methods table</span></span>

    <span data-ttu-id="78834-154">Wenn eine Klasse über Methoden verfügt, werden die Methoden in der Tabelle unmittelbar nach dem Syntax Block aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="78834-154">If a class has methods, the methods are listed in the table immediately following the syntax block.</span></span> <span data-ttu-id="78834-155">Jede implementierte Methode ist mit einer Referenzseite verknüpft.</span><span class="sxs-lookup"><span data-stu-id="78834-155">Each implemented method is linked to a reference page.</span></span>

-   <span data-ttu-id="78834-156">Liste Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78834-156">Properties list</span></span>

    <span data-ttu-id="78834-157">Jede Klassen Eigenschaft wird mit einem Datentyp, einem Zugriffstyp (schreibgeschützt oder Lese-/Schreibzugriff), Qualifizierern und einer Beschreibung der Eigenschaft aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="78834-157">Each class property is listed with a data type, access type (read-only or read/write), qualifiers, and a description of the property.</span></span>

## <a name="syntax-block"></a><span data-ttu-id="78834-158">Syntaxblock</span><span class="sxs-lookup"><span data-stu-id="78834-158">Syntax block</span></span>

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a><span data-ttu-id="78834-159">Tabelle "Methoden"</span><span class="sxs-lookup"><span data-stu-id="78834-159">Methods table</span></span>



| <span data-ttu-id="78834-160">Win32 \_ XYZ-Methoden</span><span class="sxs-lookup"><span data-stu-id="78834-160">Win32\_xyz methods</span></span> | <span data-ttu-id="78834-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78834-161">Description</span></span>                                |
|--------------------|--------------------------------------------|
| <span data-ttu-id="78834-162">*SomeMethod*</span><span class="sxs-lookup"><span data-stu-id="78834-162">*SomeMethod*</span></span>       | <span data-ttu-id="78834-163">Kurze Beschreibung der Funktionsweise der Methode.</span><span class="sxs-lookup"><span data-stu-id="78834-163">Brief description of what the method does.</span></span> |



 

## <a name="properties-list"></a><span data-ttu-id="78834-164">Liste Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="78834-164">Properties list</span></span>

<dl> <dt>

<span data-ttu-id="78834-165"><span id="abc"></span><span id="ABC"></span>Sender</span><span class="sxs-lookup"><span data-stu-id="78834-165"><span id="abc"></span><span id="ABC"></span>abc</span></span>
</dt> <dd>

<span data-ttu-id="78834-166">Datentyp: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="78834-166">Data type: **uint16**</span></span>

<span data-ttu-id="78834-167">Zugriffstyp: zeigt an, ob Sie Lese-/Schreibzugriff oder schreibgeschützten Zugriff auf diese Eigenschaft haben.</span><span class="sxs-lookup"><span data-stu-id="78834-167">Access type: Shows whether you have read/write or read-only access to this property.</span></span>

<span data-ttu-id="78834-168">Qualifizierer: zeigt die Qualifizierer für die Eigenschaft an, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="78834-168">Qualifiers: If present, shows the qualifiers for the property.</span></span> <span data-ttu-id="78834-169">Beispiel: **Key**, **override**.</span><span class="sxs-lookup"><span data-stu-id="78834-169">For example, **Key**, **Override**.</span></span>

<span data-ttu-id="78834-170">Beschreibt die-Eigenschaft und stellt Vererbungs Informationen für die-Eigenschaft bereit.</span><span class="sxs-lookup"><span data-stu-id="78834-170">Describes the property and provides inheritance information for the property.</span></span> <span data-ttu-id="78834-171">Diese Eigenschaft wird z. b. von \**CIM \_* XYZ \* \* \* geerbt.</span><span class="sxs-lookup"><span data-stu-id="78834-171">For example, this property is inherited from \**CIM\_* xyz\*\*\*.</span></span> <span data-ttu-id="78834-172">Es gibt einen Link zur übergeordneten-Klasse, wenn Microsoft eine Implementierung dieser Klasse bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="78834-172">There is a link to the parent class if Microsoft provides an implementation of that class.</span></span> <span data-ttu-id="78834-173">Die CIM-Klassen sind jedoch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="78834-173">However, the CIM classes are not available.</span></span>

</dd> <dt>

<span data-ttu-id="78834-174"><span id="def"></span><span id="DEF"></span>auflösenden</span><span class="sxs-lookup"><span data-stu-id="78834-174"><span id="def"></span><span id="DEF"></span>def</span></span>
</dt> <dd>

<span data-ttu-id="78834-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="78834-175">Data type: **string**</span></span>

<span data-ttu-id="78834-176">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="78834-176">Access type: Read-only</span></span>

<span data-ttu-id="78834-177">Die Beschreibung der Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="78834-177">Description of the property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78834-178">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78834-178">Remarks</span></span>

<span data-ttu-id="78834-179">Gibt ggf. Weitere Informationen zur-Klasse.</span><span class="sxs-lookup"><span data-stu-id="78834-179">Gives more information about the class, if applicable.</span></span> <span data-ttu-id="78834-180">Bietet auch abderivationsinformationen, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="78834-180">Also provides derivation information, if applicable.</span></span>

## <a name="related-topics"></a><span data-ttu-id="78834-181">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="78834-181">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="78834-182">WMI-Referenz</span><span class="sxs-lookup"><span data-stu-id="78834-182">WMI Reference</span></span>](wmi-reference.md)
</dt> </dl>

 

 
