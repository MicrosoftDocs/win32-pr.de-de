---
title: Ebene der Schema Unterstützung
description: In diesem Abschnitt werden die Details zur Ebene der Schema Unterstützung behandelt.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Schema Unterstützungs Ebene-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aa50eef8835f643abb668b439160ea733bf5160
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104554501"
---
# <a name="schema-support-level"></a><span data-ttu-id="a01a8-106">Ebene der Schema Unterstützung</span><span class="sxs-lookup"><span data-stu-id="a01a8-106">Schema support level</span></span>

<span data-ttu-id="a01a8-107">In diesem Abschnitt werden die Details zur Ebene der Schema Unterstützung behandelt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-107">This section covers the details around the level of schema support.</span></span>


<span data-ttu-id="a01a8-108">Das Schema unterstützt direkt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a01a8-108">The schema directly supports the following:</span></span>

-   <span data-ttu-id="a01a8-109">Sequenzen von Elementen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-109">Sequences of elements.</span></span>
-   <span data-ttu-id="a01a8-110">Ableitung von Elementtypen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-110">Derivation of element types.</span></span>
-   <span data-ttu-id="a01a8-111">Einfache Auswahl von Elementen (solche, die einer markierten Union zugeordnet sind).</span><span class="sxs-lookup"><span data-stu-id="a01a8-111">Simple choices of elements (those that map to a tagged union).</span></span>
-   <span data-ttu-id="a01a8-112">Grundlegende Typen, die durch das XSD/.net-Binärformat definiert sind, einschließlich Bereiche (min/max).</span><span class="sxs-lookup"><span data-stu-id="a01a8-112">Basic types defined by XSD / .NET binary format including ranges (min/max).</span></span>
-   <span data-ttu-id="a01a8-113">Einfache Unterstützung für ein beliebiges Element (keine Einschränkungen für den Elementtyp).</span><span class="sxs-lookup"><span data-stu-id="a01a8-113">Simple support for any element (no restrictions on type of element).</span></span>
-   <span data-ttu-id="a01a8-114">Optionale Elemente und Attribute mit Standardwerten.</span><span class="sxs-lookup"><span data-stu-id="a01a8-114">Optional elements and attributes with default values.</span></span>
-   <span data-ttu-id="a01a8-115">Wiederholen von Elementen mit Bereichen (min/max).</span><span class="sxs-lookup"><span data-stu-id="a01a8-115">Repeating elements with ranges (min/max).</span></span>
-   <span data-ttu-id="a01a8-116">Nillable-Elemente.</span><span class="sxs-lookup"><span data-stu-id="a01a8-116">Nillable elements.</span></span>

<span data-ttu-id="a01a8-117">Das Schema unterstützt Folgendes nicht direkt (was das "Fallback"-Verhalten impliziert):</span><span class="sxs-lookup"><span data-stu-id="a01a8-117">The schema does not support the following directly (which imply the "fallback" behavior):</span></span>

-   <span data-ttu-id="a01a8-118">Benutzerdefinierte Basis Typen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-118">User defined basic types.</span></span>
-   <span data-ttu-id="a01a8-119">Kompliziertere Auswahlmöglichkeiten.</span><span class="sxs-lookup"><span data-stu-id="a01a8-119">More complicated choices.</span></span>
-   <span data-ttu-id="a01a8-120">Unbekannte Attribute werden abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-120">Rejecting unknown attributes.</span></span>
-   <span data-ttu-id="a01a8-121">Roundtrip für unbekannte Attribute.</span><span class="sxs-lookup"><span data-stu-id="a01a8-121">Round tripping unknown attributes.</span></span>
-   <span data-ttu-id="a01a8-122">Kompliziertere Unterstützung für jedes Element.</span><span class="sxs-lookup"><span data-stu-id="a01a8-122">More complicated support for any element.</span></span>
-   <span data-ttu-id="a01a8-123">Das All-Konstrukt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-123">The all construct.</span></span>
-   <span data-ttu-id="a01a8-124">Key/keyref.</span><span class="sxs-lookup"><span data-stu-id="a01a8-124">Key/keyref.</span></span>

<span data-ttu-id="a01a8-125">Im folgenden finden Sie eine ausführliche Aufschlüsselung der Unterstützung unterschiedlicher Schema Komponenten.</span><span class="sxs-lookup"><span data-stu-id="a01a8-125">Following is a detailed breakdown of different schema component support.</span></span> <span data-ttu-id="a01a8-126">Sie wird mit einem Datenvertrag in WCF verglichen, weil die Funktions Ähnlichkeit besteht.</span><span class="sxs-lookup"><span data-stu-id="a01a8-126">It is compared with data contract in WCF because the similarity in functionality.</span></span> <span data-ttu-id="a01a8-127">Der Unterschied wird beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a01a8-127">The difference will be described.</span></span>

<span data-ttu-id="a01a8-128">Im Allgemeinen gilt für Fall Back Verhalten:</span><span class="sxs-lookup"><span data-stu-id="a01a8-128">Generally, for fallback behaviors:</span></span>

-   <span data-ttu-id="a01a8-129">Attribute werden auf die WS- \_ Zeichenfolge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-129">attributes are fall backed to WS\_STRING;</span></span>
-   <span data-ttu-id="a01a8-130">der Inhalt des Elements wird auf den WS-XML-Puffer unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a01a8-130">element content are fall backed to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-131">complexType wird auf eine Struktur unterstützt, die ein Feld mit dem WS- \_ XML- \_ Puffer enthält.</span><span class="sxs-lookup"><span data-stu-id="a01a8-131">complexType are fall backed to structure containing a field of WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-132">Einfache Typen werden auf die WS- \_ Zeichenfolge unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-132">Simple types are fall backed to WS\_STRING.</span></span>

<span data-ttu-id="a01a8-133">wsutil generiert Warnungen für Schema Komponenten, die derzeit nicht vollständig unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-133">wsutil generates warnings for schema components that are not currently fully supported.</span></span> <span data-ttu-id="a01a8-134">Die Anwendung muss möglicherweise eine zusätzliche Überprüfung durchführen, damit diese Komponenten benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-134">Application might need to do additional verification for those components are needed.</span></span> <span data-ttu-id="a01a8-135">Die Überstunden "wsutil" kann verbessert werden, um einige der Funktionen zu verarbeiten, die derzeit in der Laufzeit unterstützt werden, z. b. Standardwert</span><span class="sxs-lookup"><span data-stu-id="a01a8-135">Overtime wsutil can be improved to handle some of the features that are currently supported in runtime, like default value support.</span></span> <span data-ttu-id="a01a8-136">wsutil kann auch zusammen mit der Serialisierung verbessert werden, um andere Features wie Abstract zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-136">wsutil can also be improved together with serialization to support other features like abstract.</span></span> <span data-ttu-id="a01a8-137">Die Anzahl der nicht unterstützten Schema Komponenten kann im Laufe der Zeit reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-137">The number of unsupported schema components can be reduced over time.</span></span>

## <a name="the-overall-schema-document"></a><span data-ttu-id="a01a8-138">Das Gesamt Schema Dokument</span><span class="sxs-lookup"><span data-stu-id="a01a8-138">The Overall Schema Document</span></span>

<span data-ttu-id="a01a8-139">Eine globale Definition, die sich möglicherweise auf eingebettete Definitionen im Schema auswirkt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-139">Global definition that might affect embedded definitions in the schema.</span></span> <span data-ttu-id="a01a8-140">Dabei handelt es sich um globale Attribute, die auf alle Definitionen im Schema anwendbar sind.</span><span class="sxs-lookup"><span data-stu-id="a01a8-140">These are global attributes that are applicable to all definitions in the schema.</span></span>

<span data-ttu-id="a01a8-141"><xs: Schema> Attribute</span><span class="sxs-lookup"><span data-stu-id="a01a8-141"><xs:schema> attributes</span></span>

-   <span data-ttu-id="a01a8-142">attributefromdefault wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-142">attributeFromDefault Ignored.</span></span>
-   <span data-ttu-id="a01a8-143">blockDefault wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-143">blockDefault Ignored.</span></span>
-   <span data-ttu-id="a01a8-144">Element Form Default wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-144">elementFormDefault Ignored.</span></span> <span data-ttu-id="a01a8-145">Dies unterscheidet sich von DataContract, da nicht qualifizierte Elemente in der Laufzeit unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-145">This is different from dataContract as unqualified elements are supported in runtime.</span></span>
-   <span data-ttu-id="a01a8-146">finalDefault wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-146">finalDefault Ignored.</span></span> <span data-ttu-id="a01a8-147">Es gibt keine Unterstützung für die C-Sprache für das Konzept von "Final".</span><span class="sxs-lookup"><span data-stu-id="a01a8-147">There is no C language support for the concept of final.</span></span>
-   <span data-ttu-id="a01a8-148">ID wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-148">id Ignored.</span></span>
-   <span data-ttu-id="a01a8-149">targetNamespace wird unterstützt und dem Dienst Namespace zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-149">targetNamespace Supported and mapped to the service namespace.</span></span>
-   <span data-ttu-id="a01a8-150">die Version wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-150">version Ignored.</span></span>

<span data-ttu-id="a01a8-151"><xs: Schema> Inhalt</span><span class="sxs-lookup"><span data-stu-id="a01a8-151"><xs:schema> contents</span></span>

-   <span data-ttu-id="a01a8-152">Unterstützte einschließen; wsutil erfordert, dass alle erforderlichen Definitionen während der Kompilierungszeit als Eingabedateien verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a01a8-152">include Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="a01a8-153">neu definieren wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-153">redefine Ignored.</span></span> <span data-ttu-id="a01a8-154">Dies wird von wsutil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-154">wsutil does not support this.</span></span>
-   <span data-ttu-id="a01a8-155">Import wird unterstützt. wsutil erfordert, dass alle erforderlichen Definitionen während der Kompilierungszeit als Eingabedateien verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a01a8-155">import Supported; wsutil requires all necessary definition be available as input files during compilation time.</span></span>
-   <span data-ttu-id="a01a8-156">simpleType unterstützt: siehe Abschnitt "einfacher Typ" weiter unten.</span><span class="sxs-lookup"><span data-stu-id="a01a8-156">simpleType Supported- see simple type section below.</span></span>
-   <span data-ttu-id="a01a8-157">ComplexType unterstützt-siehe Abschnitt ' complexType '</span><span class="sxs-lookup"><span data-stu-id="a01a8-157">complexType Supported- see 'complexType' section</span></span>
-   <span data-ttu-id="a01a8-158">die Gruppe wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-158">group Ignored.</span></span>
-   <span data-ttu-id="a01a8-159">attributeGroup wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-159">attributeGroup Ignored.</span></span>
-   <span data-ttu-id="a01a8-160">unterstütztes Element; wird globalen Element Definitionen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-160">element Supported; maps to global element definitions.</span></span>
-   <span data-ttu-id="a01a8-161">unterstützte Attribute wird globalen Attribut Definitionen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-161">attribute Supported; maps to global attribute definitions.</span></span>
-   <span data-ttu-id="a01a8-162">Notation ignoriert</span><span class="sxs-lookup"><span data-stu-id="a01a8-162">notation Ignored</span></span>

## <a name="complex-type"></a><span data-ttu-id="a01a8-163">Komplexer Typ</span><span class="sxs-lookup"><span data-stu-id="a01a8-163">Complex Type</span></span>

<span data-ttu-id="a01a8-164">Ein komplexer Typ, der durch <xs: complexType-> dargestellt wird, kann eine Einschränkung des einfachen Typs oder komplexen Typs, der Erweiterung von einfachem Typ, Arrays oder Strukturen sein.</span><span class="sxs-lookup"><span data-stu-id="a01a8-164">Complex type, represented by <xs:complexType>, could be restriction of simple type or complex type, extension of simple type, arrays or structure.</span></span> <span data-ttu-id="a01a8-165">Beachten Sie, dass in der Erweiterung von einfachen Typen keine Vererbung und keine xsi: Type-Unterstützung vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a01a8-165">Noticed that in extension of simple types, there is no inheritance and no xsi:type support.</span></span>

<span data-ttu-id="a01a8-166"><xs: complexType-> Attribute</span><span class="sxs-lookup"><span data-stu-id="a01a8-166"><xs:complexType> attributes</span></span>

-   <span data-ttu-id="a01a8-167">Abstract generieren Sie eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-167">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-168">Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-168">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-169">abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-169">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-170">ID wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-170">id Ignored.</span></span>
-   <span data-ttu-id="a01a8-171">gemischt generiert eine Warnung über nicht unterstützte Funktion, Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer, wenn true.</span><span class="sxs-lookup"><span data-stu-id="a01a8-171">mixed Generate warning about unsupported feature, fallback to structure with WS\_XML\_BUFFER if true.</span></span>
-   <span data-ttu-id="a01a8-172">der Name wird unterstützt und dem Strukturtyp Namen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-172">name Supported and mapped to structure type name.</span></span>

<span data-ttu-id="a01a8-173"><xs: complexType> Inhalt</span><span class="sxs-lookup"><span data-stu-id="a01a8-173"><xs:complexType> contents</span></span>

<span data-ttu-id="a01a8-174">Dies ist eine Typdefinition für die-Struktur.</span><span class="sxs-lookup"><span data-stu-id="a01a8-174">This is type definition for structure.</span></span> <span data-ttu-id="a01a8-175">die complexContent-Einschränkung wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-175">complexContent restriction is not supported.</span></span>

-   <span data-ttu-id="a01a8-176">complexContent unterstützt komplexe Inhalts Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-176">complexContent Support complex content extension.</span></span> <span data-ttu-id="a01a8-177">Wird der Struktur Vererbung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-177">Maps to structure inheritance.</span></span>
-   <span data-ttu-id="a01a8-178">Gruppieren Sie derzeit ein Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer Feld.</span><span class="sxs-lookup"><span data-stu-id="a01a8-178">group Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="a01a8-179">Kann gemäß dem untergeordneten Partikel unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-179">Can be supported according to the underneath particle.</span></span>
-   <span data-ttu-id="a01a8-180">Auswahl wird als Union unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-180">choice supported as union.</span></span> <span data-ttu-id="a01a8-181">Dies wird im Datenvertrag nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-181">This is not supported in data contract.</span></span>
-   <span data-ttu-id="a01a8-182">Sequence supported-Zuordnungen zu Feldern einer Struktur</span><span class="sxs-lookup"><span data-stu-id="a01a8-182">sequence Supported - maps to fields of a structure</span></span>
-   <span data-ttu-id="a01a8-183">das Attribut wird mit einer Ausnahme von "verboten" unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-183">attribute supported with one exception of 'prohibited'.</span></span> <span data-ttu-id="a01a8-184">Fall Back auf die Struktur mit dem WS- \_ XML- \_ Puffer, wenn ' unzulässig ' ist.</span><span class="sxs-lookup"><span data-stu-id="a01a8-184">fallback to structure with WS\_XML\_BUFFER if 'prohibited'.</span></span>
-   <span data-ttu-id="a01a8-185">attributeGroup unterstützt-Zuordnungs Sequenz von Attributen</span><span class="sxs-lookup"><span data-stu-id="a01a8-185">attributeGroup supported - maps to sequence of attributes</span></span>
-   <span data-ttu-id="a01a8-186">anyAttribute wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-186">anyAttribute Ignored</span></span>
-   <span data-ttu-id="a01a8-187">Attributegroupref unterstützt: entspricht der Sequenz von Attributen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-187">AttributeGroupRef Supported - maps to sequence of attributes.</span></span>
-   <span data-ttu-id="a01a8-188">Groupref führt zurzeit ein Fall Back auf die Struktur mit dem WS \_ XML- \_ Puffer Feld aus</span><span class="sxs-lookup"><span data-stu-id="a01a8-188">GroupRef Currently fallback to structure with WS\_XML\_BUFFER field.</span></span> <span data-ttu-id="a01a8-189">Kann entsprechend der darunter liegenden Gruppe unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-189">Can be supported according to the underneath group.</span></span>
-   <span data-ttu-id="a01a8-190">Alle unterstützten, dem XML-Puffer Zuordnungen \_</span><span class="sxs-lookup"><span data-stu-id="a01a8-190">Any Supported, maps to XML\_BUFFER</span></span>
-   <span data-ttu-id="a01a8-191">(leer) unterstützte Zuordnung zu leerer Struktur Beschreibung ohne generierte Struktur.</span><span class="sxs-lookup"><span data-stu-id="a01a8-191">(blank) supported map to empty struct description with no struct generated.</span></span>

<span data-ttu-id="a01a8-192"><xs:sequence> in einem komplexen Typ: Inhalt</span><span class="sxs-lookup"><span data-stu-id="a01a8-192"><xs:sequence> in a complex type: contents</span></span>

<span data-ttu-id="a01a8-193">die Sequenz von minvorkommen = 1 und maxvorkommen = 1 wird von wsutil nur vollständig unterstützt. Andernfalls wird der komplexe Typ zurzeit auf den WS-XML-Puffer unterstützt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a01a8-193">wsutil only fully support sequence of minOccurs = 1 and maxOccurs = 1; otherwise the complex type is currently fall backed to WS\_XML\_BUFFER.</span></span> <span data-ttu-id="a01a8-194">Sie kann als Array von Strukturen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-194">It can be supported as array of structures.</span></span>

-   <span data-ttu-id="a01a8-195">unterstütztes Element; jede Instanz wird einem Feld in der Struktur zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-195">element Supported; each instance maps to a field in the structure.</span></span>
-   <span data-ttu-id="a01a8-196">Gruppen Fallback; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="a01a8-196">Group fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-197">Alle Fallbacks; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="a01a8-197">All fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-198">Auswahl wird unterstützt. Ordnen Sie dem Union-Feld zu.</span><span class="sxs-lookup"><span data-stu-id="a01a8-198">choice supported; map to union field.</span></span>
-   <span data-ttu-id="a01a8-199">Sequenz Fall Back; der complexType ist ein Fall Back auf den WS- \_ XML- \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="a01a8-199">sequence fallback; the complexType is fallback to WS\_XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-200">Alle unterstützten; dem XML- \_ Puffer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-200">any Supported; mapped to XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-201">(leer) unterstützt; ComplexType kann eine leere Struktur sein, wenn keine Attribute vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a01a8-201">(blank) supported; complexType can be an empty structure if there is no attributes.</span></span>

## <a name="elements"></a><span data-ttu-id="a01a8-202">Elemente</span><span class="sxs-lookup"><span data-stu-id="a01a8-202">Elements</span></span>

<span data-ttu-id="a01a8-203"><xs: Element>kann in drei Kontexten vorkommen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-203"><xs:element>may occur in three contexts.</span></span>

-   <span data-ttu-id="a01a8-204">Er kann in einem <xs: Sequence-> auftreten, der ein Feld einer regulären Struktur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-204">It may occur within an <xs:sequence>, describing a field of a regular struct.</span></span> <span data-ttu-id="a01a8-205">In diesem Fall muss das maxvorkommen-Attribut 1 sein.</span><span class="sxs-lookup"><span data-stu-id="a01a8-205">In this case, the maxOccurs attribute must be 1.</span></span> <span data-ttu-id="a01a8-206">Das-Feld ist optional, wenn minvorkommen den Wert 0 hat.</span><span class="sxs-lookup"><span data-stu-id="a01a8-206">The field is optional if minOccurs is 0.</span></span>
-   <span data-ttu-id="a01a8-207">Er kann in einem <xs: Sequence-> auftreten, der ein Feld eines Arrays beschreibt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-207">It may occur within an <xs:sequence>, describing a field of an array.</span></span> <span data-ttu-id="a01a8-208">In diesem Fall muss das maxvorkommen-Attribut größer als 1 oder unbegrenzt sein.</span><span class="sxs-lookup"><span data-stu-id="a01a8-208">In this case, the maxOccurs attribute must be greater than 1 or 'unbounded'.</span></span>
-   <span data-ttu-id="a01a8-209">Sie kann in einem <xs: Schema-> als eine globale Element Beschreibung auftreten.</span><span class="sxs-lookup"><span data-stu-id="a01a8-209">It may occur within an <xs:schema> as a global element description.</span></span>

<span data-ttu-id="a01a8-210"><xs: Element> in einer <xs: Sequence> oder <xs: Choice-> als Feld in einer Struktur</span><span class="sxs-lookup"><span data-stu-id="a01a8-210"><xs:element> within an <xs:sequence> or <xs:choice> as a field in a structure</span></span>

-   <span data-ttu-id="a01a8-211">Verweis wird unterstützt. aufgelöst, um auf das globale Element zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-211">ref Supported; resolved to reference to global element.</span></span>
-   <span data-ttu-id="a01a8-212">Name unterstützt, wird dem Feldnamen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-212">name Supported, maps to field name.</span></span>
-   <span data-ttu-id="a01a8-213">der Typ wird unterstützt, der Feldtyp zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-213">type Supported, maps to field type.</span></span> <span data-ttu-id="a01a8-214">Weitere Informationen finden Sie unter "Typzuordnung".</span><span class="sxs-lookup"><span data-stu-id="a01a8-214">For more information, see 'Type Mapping'.</span></span> <span data-ttu-id="a01a8-215">Wenn nicht angegeben (und das Element keinen anonymen Typ enthält), wird xs: anyType angenommen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-215">If not specified (and the element does not contain an anonymous type), xs:anyType is assumed.</span></span>
-   <span data-ttu-id="a01a8-216">Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-216">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-217">standardmäßige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-217">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-218">korrigiert: Warnung zu nicht unterstütztem Feature generieren, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-218">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-219">das Formular wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-219">form Ignored.</span></span> <span data-ttu-id="a01a8-220">Unsere Serialisierungsebene unterstützt sowohl qualifizierte als auch nicht qualifizierte Formulare.</span><span class="sxs-lookup"><span data-stu-id="a01a8-220">Our serialization layer supports both qualified and unqualified forms.</span></span>
-   <span data-ttu-id="a01a8-221">ID wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-221">id Ignored.</span></span>
-   <span data-ttu-id="a01a8-222">maxvorkommen ist einem einzelnen Datenfeld zugeordnet, wenn 1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="a01a8-222">maxOccurs maps to a single data field if equals 1.</span></span> <span data-ttu-id="a01a8-223">Sie wird einem Array Feld (sich wiederholendes Element) zugeordnet, wenn maxvorkommen größer als 1 ist.</span><span class="sxs-lookup"><span data-stu-id="a01a8-223">it is mapped to an array field (repeating element) if maxOccurs is larger than 1.</span></span>
-   <span data-ttu-id="a01a8-224">minvorkommen wenn 0, werden die Feld Optionen auf Feld optional festgelegt \_ , wenn nillable nicht festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a01a8-224">minOccurs if 0, the field options is set to FIELD\_OPTIONAL, if nillable is not set.</span></span>
-   <span data-ttu-id="a01a8-225">nillable: das Feld ist nillable.</span><span class="sxs-lookup"><span data-stu-id="a01a8-225">nillable The field is nillable.</span></span> <span data-ttu-id="a01a8-226">Ausführlichere Informationen finden Sie unter [Serialisierung](serialization.md) .</span><span class="sxs-lookup"><span data-stu-id="a01a8-226">See [Serialization](serialization.md) for more detail.</span></span>

<span data-ttu-id="a01a8-227"><xs: Element> als globales Element: Attribute</span><span class="sxs-lookup"><span data-stu-id="a01a8-227"><xs:element> as global element: attributes</span></span>

<span data-ttu-id="a01a8-228">die Attribute minvorkommen und maxvorkommen sind als globale Element Beschreibung ungültig.</span><span class="sxs-lookup"><span data-stu-id="a01a8-228">minOccurs and maxOccurs attributes are invalid as global element description.</span></span> <span data-ttu-id="a01a8-229">Die Anwendung kann die generierte Element Beschreibung in der Serialisierungsebene oder auf Kanal Ebenen direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-229">Application can use generated element description in serialization layer or channel layers directly.</span></span>

-   <span data-ttu-id="a01a8-230">Abstract generieren Sie eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-230">abstract Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-231">Block Generieren von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-231">block Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-232">standardmäßige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-232">default Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-233">abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-233">final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-234">korrigiert: Warnung zu nicht unterstütztem Feature generieren, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-234">fixed Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-235">ID wurde ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-235">id Ignored.</span></span>
-   <span data-ttu-id="a01a8-236">Name unterstützt: Ordnen Sie den Namen der globalen Element Beschreibung zu und ist die Basis für den anonymen Typ, wenn angegeben.</span><span class="sxs-lookup"><span data-stu-id="a01a8-236">name Supported- map to name of the global element description, and it is the base for the anonymous type when specified.</span></span>
-   <span data-ttu-id="a01a8-237">nillable ignoriert: die Anwendung muss mit dem richtigen Flag aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-237">nillable Ignored-application needs to call with right flag.</span></span>
-   <span data-ttu-id="a01a8-238">substitutionGroup Fall Back auf Struktur mit WS- \_ XML- \_ Puffer, sofern festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-238">substitutionGroup fallback to structure with WS\_XML\_BUFFER if set.</span></span> <span data-ttu-id="a01a8-239">"substitutionGroup" wird von wsutil nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-239">wsutil does not support substitutionGroup.</span></span>
-   <span data-ttu-id="a01a8-240">der Typ wird unterstützt und dem Typ des Elements zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-240">type Supported and map to the type of the element.</span></span>

<span data-ttu-id="a01a8-241"><xs: Element> als globales Element: Content</span><span class="sxs-lookup"><span data-stu-id="a01a8-241"><xs:element> as global element: contents</span></span>

-   <span data-ttu-id="a01a8-242">simpleType wird unterstützt. wird der Typdefinition zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-242">simpleType Supported; maps to type definition.</span></span>
-   <span data-ttu-id="a01a8-243">complexType wird unterstützt. wird einem komplexen Typ zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-243">complexType supported; maps to a complex type.</span></span>
-   <span data-ttu-id="a01a8-244">eindeutige Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-244">unique Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="a01a8-245">"wsutil" unterstützt keine Element Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-245">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="a01a8-246">Schlüssel generiert Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-246">key Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="a01a8-247">"wsutil" unterstützt keine Element Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-247">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="a01a8-248">keyref generiert eine Warnung über eine nicht unterstützte Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-248">keyref Generate warning about unsupported feature, no change to code generation.</span></span> <span data-ttu-id="a01a8-249">"wsutil" unterstützt keine Element Einschränkungen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-249">wsutil does not support element constraints.</span></span>
-   <span data-ttu-id="a01a8-250">Blitz Unterstützt ein Element ohne Typangabe wird als xs: anyType behandelt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-250">(blank) Supported; element with no type specification is treated as xs:anyType.</span></span>

## <a name="simple-types"></a><span data-ttu-id="a01a8-251">Einfache Typen</span><span class="sxs-lookup"><span data-stu-id="a01a8-251">Simple Types</span></span>

<span data-ttu-id="a01a8-252"><xs: simpleType-> Attribute</span><span class="sxs-lookup"><span data-stu-id="a01a8-252"><xs:simpleType> attributes</span></span>

-   <span data-ttu-id="a01a8-253">Abschließende Generierung von Warnungen zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-253">Final Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-254">ID ignoriert</span><span class="sxs-lookup"><span data-stu-id="a01a8-254">Id Ignored</span></span>
-   <span data-ttu-id="a01a8-255">Name unterstützt, wird dem Typnamen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-255">Name Supported, maps to type name.</span></span>

<span data-ttu-id="a01a8-256"><xs: simpleType-> Inhalt</span><span class="sxs-lookup"><span data-stu-id="a01a8-256"><xs:simpleType> contents</span></span>

-   <span data-ttu-id="a01a8-257">Unterstützte Einschränkung, wird dem Enumerationstyp oder dem Bereich zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a01a8-257">Restriction Supported, maps to enum type or range.</span></span> <span data-ttu-id="a01a8-258">Weitere Informationen finden Sie im Abschnitt "xs: simpleType-Einschränkungen".</span><span class="sxs-lookup"><span data-stu-id="a01a8-258">See "xs:simpleType restrictions" section.</span></span>
-   <span data-ttu-id="a01a8-259">Liste generiert Warnung zu nicht unterstützter Funktion, Fall Back auf XML- \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="a01a8-259">List Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>
-   <span data-ttu-id="a01a8-260">Union generiert Warnung über nicht unterstützte Funktion, Fall Back auf XML- \_ Puffer.</span><span class="sxs-lookup"><span data-stu-id="a01a8-260">Union Generate warning about unsupported feature, fallback to XML\_BUFFER.</span></span>

## <a name="simple-type-restriction"></a><span data-ttu-id="a01a8-261">Einschränkung für einfache Typen</span><span class="sxs-lookup"><span data-stu-id="a01a8-261">Simple Type restriction</span></span>

<span data-ttu-id="a01a8-262">Bestimmte Facetten sind in ganzzahligen Typen und Zeichen folgen Typen zulässig, um Unterstützung für Bereiche und Enumerationen zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-262">Certain facets are allowed in integral types and strings type to allow range and enum support.</span></span>

<span data-ttu-id="a01a8-263">enumerationsunterstützung</span><span class="sxs-lookup"><span data-stu-id="a01a8-263">enumeration support</span></span>

<span data-ttu-id="a01a8-264"><xs: Enumeration> einfache Typeinschränkung für den Basistyp der Zeichenfolge als Enumerationstyp behandelt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-264"><xs:enumeration> simple type restriction for base type of string is treated as enum type.</span></span> <span data-ttu-id="a01a8-265">In diesem Fall muss das Basis Attribut vom Typ "String" sein.</span><span class="sxs-lookup"><span data-stu-id="a01a8-265">In this case, the Base attribute MUST be string type.</span></span> <span data-ttu-id="a01a8-266">In Aufzählungs Fällen werden alle anderen Facetten ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-266">In enumeration case, all other facets are ignored.</span></span>

<span data-ttu-id="a01a8-267">Bereich bei einfacher Typunterstützung</span><span class="sxs-lookup"><span data-stu-id="a01a8-267">range on simple type support</span></span>

<span data-ttu-id="a01a8-268">Einige Facetten sind Unterstützung für einfache Typen Unterstützung für den Typ.</span><span class="sxs-lookup"><span data-stu-id="a01a8-268">Some facets are support in simple types support effectively range allowed on the type.</span></span> <span data-ttu-id="a01a8-269">Die folgenden Einschränkungen gelten für ganzzahlige Typen und float/double-Typen.</span><span class="sxs-lookup"><span data-stu-id="a01a8-269">Following are restriction for integral types and float/double types.</span></span> <span data-ttu-id="a01a8-270">Einfache Typen mit anderen Facetten werden auf den WS- \_ Zeichen Folgentyp unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-270">Simple types with other facets are fall backed to WS\_STRING type</span></span>

-   <span data-ttu-id="a01a8-271">minExclusive unterstützt</span><span class="sxs-lookup"><span data-stu-id="a01a8-271">minExclusive Supported</span></span>
-   <span data-ttu-id="a01a8-272">unterstützt minInclusive</span><span class="sxs-lookup"><span data-stu-id="a01a8-272">minInclusive Supported</span></span>
-   <span data-ttu-id="a01a8-273">maxExclusive unterstützt</span><span class="sxs-lookup"><span data-stu-id="a01a8-273">maxExclusive Supported</span></span>
-   <span data-ttu-id="a01a8-274">unterstützt maxInclusive</span><span class="sxs-lookup"><span data-stu-id="a01a8-274">maxInclusive Supported</span></span>
-   <span data-ttu-id="a01a8-275">totalDigits generiert eine Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-275">totalDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-276">"fractionDigits" generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-276">fractionDigits Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-277">Länge generiert Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-277">length Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-278">MinLength generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-278">minLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-279">MaxLength generiert eine Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-279">maxLength Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-280">die Enumeration generiert eine Warnung zu einer nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-280">enumeration Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-281">Leerraum generiert Warnung zur nicht unterstützten Funktion, ohne Änderungen an der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-281">whiteSpace Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-282">Muster generieren Warnung zu nicht unterstützter Funktion, keine Änderung der Codegenerierung.</span><span class="sxs-lookup"><span data-stu-id="a01a8-282">pattern Generate warning about unsupported feature, no change to code generation.</span></span>
-   <span data-ttu-id="a01a8-283">Blitz Unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-283">(blank) Supported.</span></span>

<span data-ttu-id="a01a8-284">MinLength und MaxLength in der Zeichenfolge werden zurzeit nicht unterstützt, ist aber ein wünschenswert, der unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a01a8-284">minLength and maxLength on string is not supported currently but is a desirable feature to support.</span></span>

## <a name="inheritance"></a><span data-ttu-id="a01a8-285">Vererbung</span><span class="sxs-lookup"><span data-stu-id="a01a8-285">Inheritance</span></span>

<span data-ttu-id="a01a8-286">Wsutil unterstützt die Vererbung komplexer Typen, d. h., eine Struktur kann von einer anderen Struktur erben, ähnlich der Schnittstellen Vererbung in C++.</span><span class="sxs-lookup"><span data-stu-id="a01a8-286">Wsutil supports inheritance of complex types, that is, a structure can inherit from another structure, similar to interface inheritance in C++.</span></span> <span data-ttu-id="a01a8-287">Dies erfolgt über <xs: complexcontentextension>.</span><span class="sxs-lookup"><span data-stu-id="a01a8-287">This is done through <xs:complexContentExtension>.</span></span> <span data-ttu-id="a01a8-288"><xs: simplecontentextension> wird unterstützt, aber als einfache Struktur mit dem Basistyp als erstes Feld anstelle der Typvererbung generiert.</span><span class="sxs-lookup"><span data-stu-id="a01a8-288"><xs:simpleContentExtension> is supported but is generated as plain structure with base type as first field instead of type inheritance.</span></span>

## <a name="typeprimitive-mapping"></a><span data-ttu-id="a01a8-289">Zuordnung von Typen zu primitivem Typen</span><span class="sxs-lookup"><span data-stu-id="a01a8-289">Type/primitive mapping</span></span>

<span data-ttu-id="a01a8-290">Bezeichner müssen bei der Übersetzung von NCNames in XML normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a01a8-290">Identifiers needs to be normalized when translating from NCNames in XML.</span></span> <span data-ttu-id="a01a8-291">Zeichen folgen sind nillable. Zeiger Typen sind nillable. ganzzahlige Typen und float/double sind nillable, und DefaultValue ist auf 0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a01a8-291">Strings are nillable; pointer types are nillable; integral types and float/double are nillable and defaultValue is set to 0.</span></span>

![Tabelle, die die Zuordnung zwischen XSD-Typen und sapplidatentypen anzeigt.](images/schematypemap.png)

 

 




