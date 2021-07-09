---
description: Erfahren Sie mehr über XML-Attribute im Druckschemaframework. Dieses Thema ist nicht aktuell. Die aktuellen Informationen finden Sie unter Spezifikation des Druckschemas.
ms.assetid: 41bc10fe-6c00-44c5-ba9a-10414b31cbdf
title: XML-Attribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d410dcb1476d90568bee10c7c1e41ee7a9bee2e7
ms.sourcegitcommit: 998d50f6def8a25850fc113fc8a2df903c829c5e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/09/2021
ms.locfileid: "113548818"
---
# <a name="xml-attributes"></a><span data-ttu-id="1fa4e-105">XML-Attribute</span><span class="sxs-lookup"><span data-stu-id="1fa4e-105">XML Attributes</span></span>

<span data-ttu-id="1fa4e-106">Dieses Thema ist nicht aktuell.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-106">This topic is not current.</span></span> <span data-ttu-id="1fa4e-107">Die aktuellen Informationen finden Sie unter [Print Schema Specification (Spezifikation des Druckschemas).](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)</span><span class="sxs-lookup"><span data-stu-id="1fa4e-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="1fa4e-108">Es gibt eine Reihe von XML-Attributen, die in mehreren Elementtypen angezeigt werden, die im Druckschemaframework definiert sind.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-108">There are a number of XML attributes that appear in several element types defined in the Print Schema Framework.</span></span> <span data-ttu-id="1fa4e-109">XML-Attribute mit demselben Namen haben in der Regel dieselbe Bedeutung und befolgen die gleichen Regeln, unabhängig vom Elementtyp, in dem sie sich befinden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-109">XML attributes with the same name generally have the same meaning and obey the same rules regardless of the element type they reside in.</span></span> <span data-ttu-id="1fa4e-110">Daher werden die XML-Attribute hier nach Name und nicht nach ihrem Hostelementtyp aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-110">Therefore, the XML attributes are listed here by name and not by their host element type.</span></span> <span data-ttu-id="1fa4e-111">Privat definierte XML-Attribute sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-111">Privately-defined XML attributes are not permitted.</span></span> <span data-ttu-id="1fa4e-112">Nur die hier definierten XML-Attribute können in einem PrintCapabilities-Dokument oder einem PrintTicket und dann nur im definierten Kontext verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-112">Only the XML attributes defined here may be used in a PrintCapabilities document or a PrintTicket, and then only in the defined context.</span></span>

<span data-ttu-id="1fa4e-113">Private Parteien dürfen zwar keine neuen Definitionen in den Namespace einer anderen Partei einführen, sie dürfen jedoch vorhandene Namen aus einem anderen privaten Namespace verwenden, solange ihre Verwendung mit der von der anderen Partei festgelegten Verwendung konsistent ist.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-113">Although private parties are not permitted to introduce new definitions into another party's namespace, they are permitted utilize existing names from another private namespace as long as its use is consistent with the usage established by the other party.</span></span> <span data-ttu-id="1fa4e-114">Daher kann eine Option ScoredProperty-Elemente enthalten, die von mehreren verschiedenen Parteien definiert wurden, die sich jeweils in unterschiedlichen Namespaces befinden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-114">Thus an Option may contain ScoredProperty elements defined by several different parties, each residing in different namespaces.</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1fa4e-115">Attributname</span><span class="sxs-lookup"><span data-stu-id="1fa4e-115">Attribute Name</span></span></th>
<th><span data-ttu-id="1fa4e-116">Datentypen und Werte</span><span class="sxs-lookup"><span data-stu-id="1fa4e-116">Data Types and Values</span></span></th>
<th><span data-ttu-id="1fa4e-117">Zweck</span><span class="sxs-lookup"><span data-stu-id="1fa4e-117">Purpose</span></span></th>
<th><span data-ttu-id="1fa4e-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fa4e-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1fa4e-119">name</span><span class="sxs-lookup"><span data-stu-id="1fa4e-119">name</span></span> <br/></td>
<td><span data-ttu-id="1fa4e-120">XML QName</span><span class="sxs-lookup"><span data-stu-id="1fa4e-120">XML QName</span></span><br/></td>
<td><span data-ttu-id="1fa4e-121">Dieses XML-Attribut identifiziert die Elementinstanz.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-121">This XML attribute identifies the element instance.</span></span> <span data-ttu-id="1fa4e-122">Es unterscheidet ein Element von einem anderen Element desselben Elementtyps.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-122">It distinguishes one element from another of the same element type.</span></span> <span data-ttu-id="1fa4e-123">Dieses XML-Attribut wird so häufig verwendet, dass es als Namensattribut bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-123">This XML attribute is so widely used it is referred to as the name attribute.</span></span><br/></td>
<td><span data-ttu-id="1fa4e-124">Die folgenden Einschränkungen gelten für das Name-Attribut.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-124">The following restrictions pertain to the name attribute.</span></span><br/>
<ul>
<li><span data-ttu-id="1fa4e-125">Das Name-Attribut muss in Form eines gültigen XML-definierten QName-Werts sein.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-125">The name attribute must be in the form of a valid XML-defined QName.</span></span> <span data-ttu-id="1fa4e-126">Das heißt, sie muss durch einen gültigen XML-Namespace qualifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-126">That is, it must be qualified by a valid XML namespace.</span></span> <span data-ttu-id="1fa4e-127">Die QNames, die als Werte von Namensattributen angezeigt werden, müssen explizit namespacequalifiziert sein, auch wenn ein Standardnamespace definiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-127">The QNames appearing as values of name attributes must be explicitly namespace-qualified even if a default namespace is defined.</span></span> <br/></li>
<li><span data-ttu-id="1fa4e-128">Der Zeicheninhalt muss der eines gültigen XML-definierten QName sein.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-128">Character content must be that of a valid XML-defined QName.</span></span> <br/></li>
<li><span data-ttu-id="1fa4e-129">Privat definierte Namen müssen mit einem Namespace qualifiziert werden, der eindeutig der Partei zugeordnet ist, die das Namensattribut eingeführt hat.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-129">Privately-defined names must be qualified with a namespace that is uniquely associated with the party that introduced the name attribute.</span></span><br/></li>
<li><span data-ttu-id="1fa4e-130">Anforderung an die gleichgeordnete Eindeutigkeit: Zwei gleichgeordnete Elemente, die zum gleichen Elementtyp gehören, dürfen nicht das gleiche Namensattribut haben.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-130">Sibling Uniqueness requirement: No two sibling elements belonging to the same element type may have the same name attribute.</span></span> <span data-ttu-id="1fa4e-131">Die einzige Ausnahme sind Option-Elemente, bei denen das Name-Attribut verwendet werden kann, um eine Option zu definieren.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-131">The only exception is Option elements, where the name attribute can be used to define an Option.</span></span> <span data-ttu-id="1fa4e-132">Daher können mehrere gleichgeordnete Option-Elemente das gleiche Namensattribut haben.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-132">Thus multiple-sibling Option elements may have the same name attribute.</span></span><br/></li>
<li><span data-ttu-id="1fa4e-133">Die folgenden Elementtypen können Namensattribute enthalten: Property, ScoredProperty, ParameterDef, Option und Feature.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-133">The following element types may contain name attributes: Property, ScoredProperty, ParameterDef, Option, and Feature.</span></span><br/></li>
<li><span data-ttu-id="1fa4e-134">Name-Attribute müssen in jedem element-Typ angezeigt werden, der sie enthält, mit Ausnahme einiger zuvor definierter öffentlicher Elemente der Druckschemaoption, z. B. DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-134">name attributes are required to appear in each of the element types that contain them, except in the case of some previously defined public Print Schema Option elements, such as DocumentNUp.</span></span><br/></li>
</ul>
<span data-ttu-id="1fa4e-135">Das folgende Beispiel zeigt, wie Sie eine Option-Instanz mithilfe eines "name"-Attributs identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-135">The following example shows how to identify an Option instance using a 'name' attribute.</span></span> <span data-ttu-id="1fa4e-136">Dies ist die richtige Methode zum Definieren von Option-Elementen.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-136">This is the correct way to define Option elements.</span></span> <span data-ttu-id="1fa4e-137">Ein Anbieter sollte keine unbenannten Optionen haben, es sei denn, sie sind öffentlich im Druckschema definiert, z. B. DocumentNUp.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-137">A provider should not have unnamed Options, unless they are publicly defined in the Print Schema, such as DocumentNUp.</span></span><br/>
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
<td><span data-ttu-id="1fa4e-138">Weitergegeben</span><span class="sxs-lookup"><span data-stu-id="1fa4e-138">propagate</span></span> <br/></td>
<td><span data-ttu-id="1fa4e-139">Enumeration</span><span class="sxs-lookup"><span data-stu-id="1fa4e-139">Enumeration</span></span><br/> <span data-ttu-id="1fa4e-140">Derzeit sind keine Werte definiert.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-140">No values are currently defined.</span></span><br/></td>
<td><span data-ttu-id="1fa4e-141">Das Attribut "propagate" wird in der ursprünglichen Version des Druckschemaframeworks nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-141">The propagate attribute is not used in the initial version of the Print Schema Framework.</span></span> <span data-ttu-id="1fa4e-142">Dies ist hier dokumentiert, damit printCapabilities- oder PrintTicket-Validierungscode, der für die erste Version des Druckschemaframework implementiert wurde, alle nachfolgenden Schemaversionen ohne Fehler verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-142">It is documented here so that PrintCapabilities or PrintTicket validation code implemented for the initial version of the Print Schema Framework can process any subsequent schema versions without error.</span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="1fa4e-143">Eingeschränkt</span><span class="sxs-lookup"><span data-stu-id="1fa4e-143">constrained</span></span> <br/></td>
<td><span data-ttu-id="1fa4e-144">Enumeration</span><span class="sxs-lookup"><span data-stu-id="1fa4e-144">Enumeration</span></span><br/> <span data-ttu-id="1fa4e-145">Zulässige Werte:</span><span class="sxs-lookup"><span data-stu-id="1fa4e-145">Allowed values:</span></span><br/>
<ul>
<li><span data-ttu-id="1fa4e-146">Keine</span><span class="sxs-lookup"><span data-stu-id="1fa4e-146">None</span></span> <br/></li>
<li><span data-ttu-id="1fa4e-147">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-147">PrintTicketSettings</span></span> <br/></li>
<li><span data-ttu-id="1fa4e-148">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-148">AdminSettings</span></span> <br/></li>
<li><span data-ttu-id="1fa4e-149">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-149">DeviceSettings</span></span> <br/></li>
</ul></td>
<td><span data-ttu-id="1fa4e-150">Gibt an, ob die Option zur Auswahl oder zur Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-150">Indicates whether the Option is available for selection or for use.</span></span> <br/></td>
<td><span data-ttu-id="1fa4e-151">Die zulässigen Werte des eingeschränkten Attributs haben die folgende Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-151">The allowed values of the constrained attribute have the following meanings.</span></span> <span data-ttu-id="1fa4e-152">Beachten Sie, dass diese Werte in der Reihenfolge aufgeführt sind, von der am wenigsten restriktiven (Keine) bis zur restriktivsten (DeviceSettings).</span><span class="sxs-lookup"><span data-stu-id="1fa4e-152">Note that these values are listed in order, from least restrictive (None) to most restrictive (DeviceSettings).</span></span><br/> <span data-ttu-id="1fa4e-153">Keine</span><span class="sxs-lookup"><span data-stu-id="1fa4e-153">None</span></span> <br/>
<ul>
<li><span data-ttu-id="1fa4e-154">Die Option ist nicht eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-154">The Option is not constrained.</span></span> <br/></li>
</ul>
<span data-ttu-id="1fa4e-155">PrintTicketSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-155">PrintTicketSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="1fa4e-156">Die Option wird durch die PrintTicket-Einstellungen eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-156">The Option is constrained by the PrintTicket settings.</span></span> <span data-ttu-id="1fa4e-157">Dies bedeutet, dass das Ändern der Konfiguration die Einschränkung entfernen kann.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-157">This implies that changing the configuration can remove the constraint.</span></span> <br/></li>
</ul>
<span data-ttu-id="1fa4e-158">AdminSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-158">AdminSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="1fa4e-159">Die Option wird durch die Einstellungen des Administrators eingeschränkt. Die Option kann vom Benutzer nicht aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-159">The Option is constrained by the administrator's settings; the Option cannot be enabled by the user.</span></span><br/></li>
</ul>
<span data-ttu-id="1fa4e-160">DeviceSettings</span><span class="sxs-lookup"><span data-stu-id="1fa4e-160">DeviceSettings</span></span> <br/>
<ul>
<li><span data-ttu-id="1fa4e-161">Die Option wird durch die Geräteeinstellungen oder die optionen für physisch installierte Geräte eingeschränkt. Die Option kann weder vom Benutzer noch vom Administrator aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-161">The Option is constrained by the device settings or the physically installed device options; the Option cannot be enabled by either the user or the administrator.</span></span><br/></li>
</ul>
<span data-ttu-id="1fa4e-162">Wenn der PrintCapabilities-Anbieter Werte des eingeschränkten Attributs meldet, sollte die restriktivste gefundene Einschränkung gemeldet werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-162">When the PrintCapabilities provider reports values of the constrained attribute, the most restrictive constraint found should be reported.</span></span> <span data-ttu-id="1fa4e-163">Wenn beispielsweise eine Option sowohl durch eine Administratoreinstellung als auch durch eine Geräteeinstellung eingeschränkt wird, sollte der PrintCapabilities-Anbieter DeviceSettings melden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-163">For example, if an Option is constrained by both an administrator setting and a device setting, the PrintCapabilities provider should report DeviceSettings.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1fa4e-164">xmlns</span><span class="sxs-lookup"><span data-stu-id="1fa4e-164">xmlns</span></span> <br/></td>
<td><span data-ttu-id="1fa4e-165">URI</span><span class="sxs-lookup"><span data-stu-id="1fa4e-165">URI</span></span><br/></td>
<td><span data-ttu-id="1fa4e-166">Dieses XML-Attribut erstellt eine Verknüpfung zwischen einem Namespace-URI (Uniform Resource Identifier) und dem Namespacepräfix, das im XML QName angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-166">This XML attribute establishes a link between a namespace uniform resource identifier (URI) and the namespace prefix that appears in the XML QName.</span></span> <span data-ttu-id="1fa4e-167">Sie müssen einen solchen Link zu dem Namespace-URI einrichten, der für das Druckschemaframework definiert ist, bevor Sie eines der Framework-definierten Elementtags, Attribute, Namensattribute und so weiter verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-167">You must establish such a link to the namespace URI defined for the Print Schema Framework before you can use any of the Framework-defined element tags, Attributes, name attributes, and so on.</span></span> <span data-ttu-id="1fa4e-168">Sie können diesen Namespace als Standardnamespace deklarieren, um zu vermeiden, dass die Elementtags tatsächlich mit einem Namespacepräfix qualifiziert werden, obwohl alle anderen QNames explizit qualifiziert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-168">You may declare this namespace to be the default to avoid actually qualifying the element tags with a namespace prefix, although all other QNames must be explicitly qualified.</span></span> <span data-ttu-id="1fa4e-169">Der Standardnamespace muss im entsprechenden Stammelement definiert werden.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-169">The standard namespace must be defined in the appropriate root element.</span></span> <span data-ttu-id="1fa4e-170">Beachten Sie alle XML-Regeln und -Konventionen in Bezug auf die Verwendung des xmlns-Attributs.</span><span class="sxs-lookup"><span data-stu-id="1fa4e-170">Observe all XML rules and conventions regarding use of the xmlns attribute.</span></span><br/> <span data-ttu-id="1fa4e-171">Der URI für das Druckschemaframework ist http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework .</span><span class="sxs-lookup"><span data-stu-id="1fa4e-171">The URI for the Print Schema Framework is http://schemas.microsoft.com/windows/2003/08/printing/printschemaframework.</span></span><br/> <span data-ttu-id="1fa4e-172">Der URI für die Druckschemaschlüsselwörter ist https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords .</span><span class="sxs-lookup"><span data-stu-id="1fa4e-172">The URI for the Print Schema Keywords is https://schemas.microsoft.com/windows/2003/08/printing/printschemakeywords.</span></span><br/></td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="1fa4e-173">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1fa4e-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1fa4e-174">Spezifikation des Druckschemas</span><span class="sxs-lookup"><span data-stu-id="1fa4e-174">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




