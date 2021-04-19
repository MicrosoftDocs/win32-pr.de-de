---
description: Dieses Thema ist nicht aktuell. Die aktuellsten Informationen finden Sie in der PrintSchema-Spezifikation.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70dd05effe6f3ea79afd0972867cb2734ace1a71
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106366573"
---
# <a name="xml-attributes"></a><span data-ttu-id="16471-104">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="16471-104">XML Attributes</span></span>

<span data-ttu-id="16471-105">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="16471-105">This topic is not current.</span></span> <span data-ttu-id="16471-106">Die aktuellsten Informationen finden Sie in der [PrintSchema-Spezifikation](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="16471-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="16471-107">Es gibt eine Reihe von XML-Attributen, die in mehreren Elementtypen angezeigt werden, die im Druck Schema Framework definiert sind.</span><span class="sxs-lookup"><span data-stu-id="16471-107">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="16471-108">XML-Attribute mit demselben Namen haben in der Regel dieselbe Bedeutung und befolgen dieselben Regeln, unabhängig von dem Elementtyp, in dem Sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="16471-108">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="16471-109">Daher werden die XML-Attribute hier nach Namen und nicht nach Ihrem Host Elementtyp aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="16471-109">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="16471-110">Privat definierte XML-Attribute sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="16471-110">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="16471-111">Nur die hier definierten XML-Attribute können in einem printfunktionen-Dokument oder einem PrintTicket verwendet werden, und dann nur im definierten Kontext.</span><span class="sxs-lookup"><span data-stu-id="16471-111">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="16471-112">Obwohl Privatparteien keine neuen Definitionen in den Namespace einer anderen Partei einführen dürfen, ist es zulässig, vorhandene Namen aus einem anderen privaten Namespace zu verwenden, solange die Verwendung mit der von der anderen Partei eingerichteten Nutzung konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="16471-112">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="16471-113">Daher kann eine Option ScoredProperty-Elemente enthalten, die von mehreren verschiedenen Parteien definiert werden, die sich jeweils in unterschiedlichen Namespaces befinden.</span><span class="sxs-lookup"><span data-stu-id="16471-113">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16471-114">Attributname</span><span class="sxs-lookup"><span data-stu-id="16471-114">Attribute Name</span></span></th>
<th><span data-ttu-id="16471-115">Datentypen und Werte</span><span class="sxs-lookup"><span data-stu-id="16471-115">Data Types and Values</span></span></th>
<th><span data-ttu-id="16471-116">Zweck</span><span class="sxs-lookup"><span data-stu-id="16471-116">Purpose</span></span></th>
<th><span data-ttu-id="16471-117">Notizen</span><span class="sxs-lookup"><span data-stu-id="16471-117">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16471-118">name</span><span class="sxs-lookup"><span data-stu-id="16471-118">name</span></span> <br/></td>
<td><span data-ttu-id="16471-119">XML-QName</span><span class="sxs-lookup"><span data-stu-id="16471-119">XML QName</span></span><br/></td>
<td><span data-ttu-id="16471-120">Dieses XML-Attribut identifiziert die-Element Instanz.</span><span class="sxs-lookup"><span data-stu-id="16471-120">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="16471-121">Es unterscheidet ein Element von einem anderen desselben Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="16471-121">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="16471-122">Dieses XML-Attribut wird so weit verbreitet verwendet, dass es als Name-Attribut bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="16471-122">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="16471-123">Die folgenden Einschränkungen beziehen sich auf das Name-Attribut.</span><span class="sxs-lookup"><span data-stu-id="16471-123">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="16471-124">Das Name-Attribut muss in der Form eines gültigen XML-definierten QName vorliegen.</span><span class="sxs-lookup"><span data-stu-id="16471-124">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="16471-125">Das heißt, er muss durch einen gültigen XML-Namespace qualifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="16471-125">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="16471-126">Die QNames, die als Werte von namens Attributen angezeigt werden, müssen explizit Namespace qualifiziert werden, auch wenn ein Standard Namespace definiert ist.</span><span class="sxs-lookup"><span data-stu-id="16471-126">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="16471-127">Der Zeichen Inhalt muss ein gültiger XML-definierter QName sein.</span><span class="sxs-lookup"><span data-stu-id="16471-127">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="16471-128">Privat definierte Namen müssen mit einem Namespace qualifiziert werden, der eindeutig mit der Partei verknüpft ist, die das Name-Attribut eingeführt hat.</span><span class="sxs-lookup"><span data-stu-id="16471-128">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="16471-129">Gleich geordnete Eindeutigkeits Anforderung: keine zwei gleich geordneten Elemente, die zum selben Elementtyp gehören, haben möglicherweise dasselbe Name-Attribut.</span><span class="sxs-lookup"><span data-stu-id="16471-129">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="16471-130">Die einzige Ausnahme sind Options Elemente, bei denen das Name-Attribut verwendet werden kann, um eine Option zu definieren.</span><span class="sxs-lookup"><span data-stu-id="16471-130">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="16471-131">Daher können mehrere gleich geordnete Options Elemente dasselbe Name-Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="16471-131">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="16471-132">Die folgenden Elementtypen können namens Attribute enthalten: Eigenschaft, ScoredProperty, ParameterDef, Option und Feature.</span><span class="sxs-lookup"><span data-stu-id="16471-132">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="16471-133">namens Attribute müssen in jedem der Elementtypen angezeigt werden, die Sie enthalten, es sei denn, es gibt einige zuvor definierte Elemente der öffentlichen Druck Schema Option (z. b. DocumentNUp).</span><span class="sxs-lookup"><span data-stu-id="16471-133">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="16471-134">Im folgenden Beispiel wird gezeigt, wie eine Options Instanz mit einem ' Name '-Attribut identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="16471-134">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="16471-135">Dies ist die korrekte Methode zum Definieren von Options Elementen.</span><span class="sxs-lookup"><span data-stu-id="16471-135">This is the correct way to define Option elements.</span></span> <span data-ttu-id="16471-136">Ein Anbieter sollte keine unbenannten Optionen haben, es sei denn, Sie sind öffentlich im Druck Schema definiert, z. b. in DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="16471-136">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
<pre class="syntax" data-space="preserve"><code>  <psf:Option name=&quot;psk:StapleBottomRight&quot;>
    <psf:ScoredProperty name=&quot;psk:Angle&quot;>
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name=&quot;psk:SheetCapacity&quot; >
      <psf:Value xsi:type=&quot;xs:integer&quot;>_Undefined_</psf:Value>
    </psf:ScoredProperty>
  </psf:Option></code></pre></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16471-137">Pixeln</span><span class="sxs-lookup"><span data-stu-id="16471-137">propagate</span></span> <br/></td>
<td><span data-ttu-id="16471-138">Enumeration</span><span class="sxs-lookup"><span data-stu-id="16471-138">Enumeration</span></span><br/> <span data-ttu-id="16471-139">Zurzeit sind keine Werte definiert.</span><span class="sxs-lookup"><span data-stu-id="16471-139">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="16471-140">Das propagierte Attribut wird in der ersten Version des Print Schema-Frameworks nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="16471-140">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="16471-141">Es ist hier dokumentiert, damit printfunktionalitäten oder PrintTicket-Validierungscode, der für die ursprüngliche Version des Print Schema-Frameworks implementiert wurde, alle nachfolgenden Schema Versionen ohne Fehler verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="16471-141">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="16471-142">schwierige</span><span class="sxs-lookup"><span data-stu-id="16471-142">constrained</span></span> <br/></td>
<td><span data-ttu-id="16471-143">Enumeration</span><span class="sxs-lookup"><span data-stu-id="16471-143">Enumeration</span></span><br/> <span data-ttu-id="16471-144">Zulässige Werte:</span><span class="sxs-lookup"><span data-stu-id="16471-144">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="16471-145">Keine</span><span class="sxs-lookup"><span data-stu-id="16471-145">None</span></span> <br/></li>
<li><span data-ttu-id="16471-146">Printticketsettings</span><span class="sxs-lookup"><span data-stu-id="16471-146">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="16471-147">Adminsettings</span><span class="sxs-lookup"><span data-stu-id="16471-147">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="16471-148">Geräte-Manager</span><span class="sxs-lookup"><span data-stu-id="16471-148">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="16471-149">Gibt an, ob die Option für die Auswahl oder zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="16471-149">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="16471-150">Die zulässigen Werte des eingeschränkten Attributs haben folgende Bedeutungen.</span><span class="sxs-lookup"><span data-stu-id="16471-150">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="16471-151">Beachten Sie, dass diese Werte in der Reihenfolge aufgelistet werden, von der geringsten Einschränkung (keine) bis zu den meisten restriktiveren (Geräte-Manager).</span><span class="sxs-lookup"><span data-stu-id="16471-151">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="16471-152">Keine</span><span class="sxs-lookup"><span data-stu-id="16471-152">None</span></span> <br/>
<ul>
<li><span data-ttu-id="16471-153">Die Option ist nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="16471-153">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="16471-154">Printticketsettings</span><span class="sxs-lookup"><span data-stu-id="16471-154">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="16471-155">Die Option wird durch die PrintTicket-Einstellungen eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="16471-155">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="16471-156">Dies bedeutet, dass das Ändern der Konfiguration die Einschränkung entfernen kann.</span><span class="sxs-lookup"><span data-stu-id="16471-156">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="16471-157">Adminsettings</span><span class="sxs-lookup"><span data-stu-id="16471-157">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="16471-158">Die Option wird durch die Einstellungen des Administrators eingeschränkt. die Option kann vom Benutzer nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="16471-158">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="16471-159">Geräte-Manager</span><span class="sxs-lookup"><span data-stu-id="16471-159">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="16471-160">Die Option wird durch die Geräteeinstellungen oder die physisch installierten Geräteoptionen eingeschränkt. die Option kann weder vom Benutzer noch vom Administrator aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="16471-160">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="16471-161">Wenn der PrintValues-Anbieter Werte des eingeschränkten Attributs meldet, sollte die restriktivste Einschränkung gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="16471-161">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="16471-162">Wenn eine Option beispielsweise durch eine Administrator Einstellung und eine Geräteeinstellung eingeschränkt ist, sollte der printSettings-Anbieter devicesettings melden.</span><span class="sxs-lookup"><span data-stu-id="16471-162">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16471-163">xmlns</span><span class="sxs-lookup"><span data-stu-id="16471-163">xmlns</span></span> <br/></td>
<td><span data-ttu-id="16471-164">URI</span><span class="sxs-lookup"><span data-stu-id="16471-164">URI</span></span><br/></td>
<td><span data-ttu-id="16471-165">Dieses XML-Attribut stellt eine Verknüpfung zwischen einem Namespace-URI (Uniform Resource Identifier) und dem Namespace Präfix her, der im XML-QName angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="16471-165">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="16471-166">Sie müssen einen solchen Link zum Namespace-URI einrichten, der für das Druck Schema Framework definiert ist, bevor Sie eines der Framework-definierten Element Tags, Attribute, namens Attribute usw. verwenden können.</span><span class="sxs-lookup"><span data-stu-id="16471-166">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="16471-167">Sie können diesen Namespace als Standard deklarieren, um zu vermeiden, dass die Element Tags tatsächlich mit einem Namespace Präfix qualifiziert werden, obwohl alle anderen QNames explizit qualifiziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="16471-167">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="16471-168">Der Standard Namespace muss im entsprechenden Root-Element definiert werden.</span><span class="sxs-lookup"><span data-stu-id="16471-168">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="16471-169">Beachten Sie alle XML-Regeln und-Konventionen hinsichtlich der Verwendung des xmlns-Attributs.</span><span class="sxs-lookup"><span data-stu-id="16471-169">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="16471-170">Der URI für das Druck Schema-Framework ist http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="16471-170">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="16471-171">Der URI für die Schlüsselwörter des Druck Schemas ist https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="16471-171">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="16471-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="16471-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16471-173">Druck Schema Spezifikation</span><span class="sxs-lookup"><span data-stu-id="16471-173">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




