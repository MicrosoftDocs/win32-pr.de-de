---
description: In der folgenden Tabelle werden alle HRESULT-Werte aufgelistet, die von den Methoden der XPS-Dokument-API zurückgegeben werden können.
ms.assetid: 9e6db1e3-7151-4538-8607-b7185ebc0110
title: XPS-Dokument Fehler (xpsobjectmodel. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a221858e177172a0062185cbe1bcc127ccc728fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215405"
---
# <a name="xps-document-errors"></a><span data-ttu-id="a982d-103">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="a982d-103">XPS Document Errors</span></span>

<span data-ttu-id="a982d-104">In der folgenden Tabelle werden alle **HRESULT** -Werte aufgelistet, die von den Methoden der XPS-Dokument-API zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="a982d-104">The following table lists all the **HRESULT** values that can be returned by the methods of the XPS Document API.</span></span> <span data-ttu-id="a982d-105">Beachten Sie, dass nicht jede Methode jeden in dieser Tabelle aufgelisteten Rückgabewert zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a982d-105">Note that not every method returns every return value that is listed in this table.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a982d-106">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="a982d-106">Return code/value</span></span></th>
<th><span data-ttu-id="a982d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a982d-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="XPS_E_ALREADY_OWNED"></span><span id="xps_e_already_owned"></span><dl> <span data-ttu-id="a982d-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-108"><dt><strong>XPS_E_ALREADY_OWNED</strong></dt> <dt>0x80520503</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-109">Die Schnittstelle verfügt bereits über einen Besitzer.</span><span class="sxs-lookup"><span data-stu-id="a982d-109">The interface already has an owner.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC"></span><span id="xps_e_bleed_box_page_dimensions_not_in_sync"></span><dl> <span data-ttu-id="a982d-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-110"><dt><strong>XPS_E_BLEED_BOX_PAGE_DIMENSIONS_NOT_IN_SYNC</strong></dt> <dt>0x80520509</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-111">Die ausgebfteten Feld Abmessungen sind nicht mit den Seiten Dimensionen kompatibel.</span><span class="sxs-lookup"><span data-stu-id="a982d-111">The bleed box dimensions are not compatible with the page dimensions.</span></span><br/> <span data-ttu-id="a982d-112">Der Wert der gebfteten Feldbreite muss größer als oder gleich der Seitenbreite plus dem absoluten Wert der x-Koordinate des Ursprungs der gebfteten Box sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-112">The bleed box width value must be greater than or equal to the page width plus the absolute value of the x-coordinate of the bleed box origin.</span></span> <span data-ttu-id="a982d-113">Der Wert für die Höhe der ausgeblendenden Box muss größer als oder gleich der Seitenhöhe plus dem absoluten Wert der y-Koordinate für den ursprünglichen Feld Ursprung sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-113">The bleed box height value must be greater than or equal to the page height plus the absolute value of the y-coordinate of the bleed box origin.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT"></span><span id="xps_e_both_pathfigure_and_abbr_syntax_present"></span><dl> <span data-ttu-id="a982d-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-114"><dt><strong>XPS_E_BOTH_PATHFIGURE_AND_ABBR_SYNTAX_PRESENT</strong></dt> <dt>0x80520507</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-115">Ein <strong>PathGeometry</strong> -Element enthält einen Satz von Pfad Abbildungen, die entweder mit dem <strong>Figures</strong> -Attribut oder mit einem untergeordneten <strong>PathFigure</strong> -Element angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-115">A <strong>PathGeometry</strong> element contains a set of path figures that are specified either with the <strong>Figures</strong> attribute or with a child <strong>PathFigure</strong> element.</span></span> <span data-ttu-id="a982d-116">Die Pfad Abbildungen einer Geometrie dürfen nicht sowohl das <strong>Figures</strong> -Attribut als auch ein untergeordnetes <strong>PathFigure</strong> -Element aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a982d-116">The path figures of a geometry cannot have both the <strong>Figures</strong> attribute and a child <strong>PathFigure</strong> element.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT"></span><span id="xps_e_both_resource_and_sourceattr_present"></span><dl> <span data-ttu-id="a982d-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-117"><dt><strong>XPS_E_BOTH_RESOURCE_AND_SOURCEATTR_PRESENT</strong></dt> <dt>0x80520508</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-118">Ein <strong>ResourceDictionary</strong> -Element, das ein Remote Ressourcen Wörterbuch in seinem <strong>Quell</strong> Attribut angibt, darf keine untergeordneten Ressourcen Definitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-118">A <strong>ResourceDictionary</strong> element that specifies a remote resource dictionary in its <strong>Source</strong> attribute MUST NOT contain any resource definition children.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_CARET_OUT_OF_ORDER"></span><span id="xps_e_caret_out_of_order"></span><dl> <span data-ttu-id="a982d-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-119"><dt><strong>XPS_E_CARET_OUT_OF_ORDER</strong></dt> <dt>0x80520306</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-120">Der Speicherort des Caretzeichen ist nicht in der richtigen Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a982d-120">A caret location value is out of order.</span></span> <span data-ttu-id="a982d-121">Die Location-Werte müssen in aufsteigender Reihenfolge sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-121">The location values must be sorted in ascending order.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_CARET_OUTSIDE_STRING"></span><span id="xps_e_caret_outside_string"></span><dl> <span data-ttu-id="a982d-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-122"><dt><strong>XPS_E_CARET_OUTSIDE_STRING</strong></dt> <dt>0x80520305</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-123">Caretzeichen wurden für eine leere Zeichenfolge angegeben. oder der Sprung Index des Caretzeichen hat die Länge der Unicode-Zeichenfolge überschritten.</span><span class="sxs-lookup"><span data-stu-id="a982d-123">Caret stops were specified for an empty string; or, the caret jump index has exceeded the length of the Unicode string.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_COLOR_COMPONENT_OUT_OF_RANGE"></span><span id="xps_e_color_component_out_of_range"></span><dl> <span data-ttu-id="a982d-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-124"><dt><strong>XPS_E_COLOR_COMPONENT_OUT_OF_RANGE</strong></dt> <dt>0x80520506</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-125">Ein Farbwert liegt außerhalb des zulässigen Bereichs.</span><span class="sxs-lookup"><span data-stu-id="a982d-125">A color value is out of range.</span></span><br/> <span data-ttu-id="a982d-126">Für <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> Farbtypen muss der Alphakanal Wert größer oder gleich 0,0 und kleiner oder gleich + 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-126">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_SCRGB</strong></a> color types, the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span><br/> <span data-ttu-id="a982d-127">Für <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> Farbtypen müssen die <strong>channelvalues [0]</strong> , die den Alphakanal Wert darstellen, größer oder gleich 0,0 und kleiner oder gleich + 1,0 sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-127">For <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a> color types, the <strong>channelValues[0]</strong> that represents the alpha channel value must be greater than or equal to 0.0 and less than or equal to +1.0.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DICTIONARY_ITEM_NAMED"></span><span id="xps_e_dictionary_item_named"></span><dl> <span data-ttu-id="a982d-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-128"><dt><strong>XPS_E_DICTIONARY_ITEM_NAMED</strong></dt> <dt>0x80520401</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-129">Ein visuelles Element in einem Ressourcen Wörterbuch verfügt über das <strong>Name</strong> -Attribut, das für keine untergeordneten Elemente eines <strong>ResourceDictionary</strong> -Elements angegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="a982d-129">A visual in a resource dictionary has the <strong>Name</strong> attribute, which may not be specified on any children of a <strong>ResourceDictionary</strong> element.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_DUPLICATE_NAMES"></span><span id="xps_e_duplicate_names"></span><dl> <span data-ttu-id="a982d-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-130"><dt><strong>XPS_E_DUPLICATE_NAMES</strong></dt> <dt>0x80520209</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-131">Ein Objekt mit diesem Namen ist bereits im Wörterbuch vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a982d-131">An object with this name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_DUPLICATE_RESOURCE_KEYS"></span><span id="xps_e_duplicate_resource_keys"></span><dl> <span data-ttu-id="a982d-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-132"><dt><strong>XPS_E_DUPLICATE_RESOURCE_KEYS</strong></dt> <dt>0x80520200</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-133">Ein Objekt mit diesem Schlüsselnamen ist bereits im Wörterbuch vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a982d-133">An object with this key name already exists in the dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INDEX_OUT_OF_RANGE"></span><span id="xps_e_index_out_of_range"></span><dl> <span data-ttu-id="a982d-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-134"><dt><strong>XPS_E_INDEX_OUT_OF_RANGE</strong></dt> <dt>0x80520500</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-135">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a982d-135">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_BLEED_BOX"></span><span id="xps_e_invalid_bleed_box"></span><dl> <span data-ttu-id="a982d-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-136"><dt><strong>XPS_E_INVALID_BLEED_BOX</strong></dt> <dt>0x80520004</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-137">Das Rechteck mit dem Feld mit dem gebfteten Feld enthält mindestens einen ungültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="a982d-137">The bleed box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="a982d-138">Die gültigen Werte finden Sie in der Parameter Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a982d-138">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_CONTENT_BOX"></span><span id="xps_e_invalid_content_box"></span><dl> <span data-ttu-id="a982d-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-139"><dt><strong>XPS_E_INVALID_CONTENT_BOX</strong></dt> <dt>0x8052000b</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-140">Das Inhaltsfeld Rechteck enthält mindestens einen ungültigen Wert.</span><span class="sxs-lookup"><span data-stu-id="a982d-140">The content box rectangle contains one or more values that are not valid.</span></span> <span data-ttu-id="a982d-141">Die gültigen Werte finden Sie in der Parameter Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="a982d-141">See the parameter description for the valid values.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_CONTENT_TYPE"></span><span id="xps_e_invalid_content_type"></span><dl> <span data-ttu-id="a982d-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000E</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-142"><dt><strong>XPS_E_INVALID_CONTENT_TYPE</strong></dt> <dt>0x8052000e</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-143">Die Inhaltstyp Zeichenfolge ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a982d-143">The content type string is not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_FLOAT"></span><span id="xps_e_invalid_float"></span><dl> <span data-ttu-id="a982d-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-144"><dt><strong>XPS_E_INVALID_FLOAT</strong></dt> <dt>0x80520007</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-145">Ein <strong>float</strong> -Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="a982d-145">A <strong>FLOAT</strong> value is not valid.</span></span> <span data-ttu-id="a982d-146">Dabei handelt es sich entweder um eine unbegrenzte oder nicht um eine Zahl (NaN).</span><span class="sxs-lookup"><span data-stu-id="a982d-146">It is either an infinite or not a number (NAN).</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_FONT_URI"></span><span id="xps_e_invalid_font_uri"></span><dl> <span data-ttu-id="a982d-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-147"><dt><strong>XPS_E_INVALID_FONT_URI</strong></dt> <dt>0x8052000a</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-148">Der Schriftart-URI ist ungültig, möglicherweise, weil er ein leeres Fragment oder ungültige Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="a982d-148">The font URI is not valid, possibly because it contains an empty fragment or characters that are not valid.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_LANGUAGE"></span><span id="xps_e_invalid_language"></span><dl> <span data-ttu-id="a982d-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-149"><dt><strong>XPS_E_INVALID_LANGUAGE</strong></dt> <dt>0x80520000</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-150">Die angegebene Sprache ist entweder ungültig oder nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="a982d-150">The specified language is either not valid or not correctly formatted.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_LOOKUP_TYPE"></span><span id="xps_e_invalid_lookup_type"></span><dl> <span data-ttu-id="a982d-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-151"><dt><strong>XPS_E_INVALID_LOOKUP_TYPE</strong></dt> <dt>0x80520006</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-152">Der Name des Suchschlüssels verweist auf ein Objekt, das nicht der richtige Typ für den-Befehl ist. Wenn die Methode z. b. einen Pinsel zurückgibt, aber der Name des Suchschlüssels auf ein Geometry-Objekt verweist.</span><span class="sxs-lookup"><span data-stu-id="a982d-152">The lookup key name references an object that is not the correct type for the call; for example, if the method returns a brush but the lookup key name refers to a geometry object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_MARKUP"></span><span id="xps_e_invalid_markup"></span><dl> <span data-ttu-id="a982d-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-153"><dt><strong>XPS_E_INVALID_MARKUP</strong></dt> <dt>0x8052000c</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-154">Das gelesene Markup enthält ein-Element oder ein-Attribut, das nicht mit der <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="a982d-154">The markup being read contains an element or an attribute that does not conform to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="a982d-155">Zum Darstellen von Gleit Komma Werten verwendet das XPS-om den <strong>float</strong> -Datentyp anstelle von <strong>Double</strong>.</span><span class="sxs-lookup"><span data-stu-id="a982d-155">To represent floating-point values, the XPS OM uses the <strong>FLOAT</strong> data type instead of <strong>DOUBLE</strong>.</span></span> <span data-ttu-id="a982d-156">Wenn ein XPS-Dokument ein Element mit Gleit Komma Daten aufweist, das nicht in einen <strong>float</strong> -Wert passt, wird dieser Fehler zurückgegeben, wenn dieser Wert während der Deserialisierung auftritt.</span><span class="sxs-lookup"><span data-stu-id="a982d-156">If an XPS document has an element with floating-point data that does not fit into a <strong>FLOAT</strong> value, this error will be returned when that value is encountered during deserialization.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_NAME"></span><span id="xps_e_invalid_name"></span><dl> <span data-ttu-id="a982d-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-157"><dt><strong>XPS_E_INVALID_NAME</strong></dt> <dt>0x80520001</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-158">Die über gegebene Zeichenfolge ist gemäß der XML Paper Specification kein gültiger Name.</span><span class="sxs-lookup"><span data-stu-id="a982d-158">The string that was passed is not a valid name, according to the XML Paper Specification.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_OBFUSCATED_FONT_URI"></span><span id="xps_e_invalid_obfuscated_font_uri"></span><dl> <span data-ttu-id="a982d-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-159"><dt><strong>XPS_E_INVALID_OBFUSCATED_FONT_URI</strong></dt> <dt>0x8052000f</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-160">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a982d-160">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_PAGE_SIZE"></span><span id="xps_e_invalid_page_size"></span><dl> <span data-ttu-id="a982d-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-161"><dt><strong>XPS_E_INVALID_PAGE_SIZE</strong></dt> <dt>0x80520003</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-162">Die Seiten Dimensionen enthalten einen ungültigen Seitengrößen Wert.</span><span class="sxs-lookup"><span data-stu-id="a982d-162">The page dimensions contain a page size value that is not valid.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_RESOURCE_KEY"></span><span id="xps_e_invalid_resource_key"></span><dl> <span data-ttu-id="a982d-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-163"><dt><strong>XPS_E_INVALID_RESOURCE_KEY</strong></dt> <dt>0x80520002</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-164">Gemäß der <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>ist die Zeichenfolge der Suchschlüssel ungültig.</span><span class="sxs-lookup"><span data-stu-id="a982d-164">According to the <a href="https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf">XML Paper Specification</a>, the lookup key string is not valid.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE"></span><span id="xps_e_invalid_thumbnail_image_type"></span><dl> <span data-ttu-id="a982d-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-165"><dt><strong>XPS_E_INVALID_THUMBNAIL_IMAGE_TYPE</strong></dt> <dt>0x80520005</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-166">Der Miniatur Bildtyp wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a982d-166">The thumbnail image type is not supported.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_INVALID_XML_ENCODING"></span><span id="xps_e_invalid_xml_encoding"></span><dl> <span data-ttu-id="a982d-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-167"><dt><strong>XPS_E_INVALID_XML_ENCODING</strong></dt> <dt>0x8052000d</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-168">Es wurde ein falsches oder falsch formatiertes XML-Markup gefunden</span><span class="sxs-lookup"><span data-stu-id="a982d-168">Found improper or incorrectly formatted XML markup.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUT_OF_ORDER"></span><span id="xps_e_mapping_out_of_order"></span><dl> <span data-ttu-id="a982d-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-169"><dt><strong>XPS_E_MAPPING_OUT_OF_ORDER</strong></dt> <dt>0x80520302</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-170">In mindestens einer <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> Struktur ist ein Element außerhalb der Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="a982d-170">In one or more <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_glyph_mapping"><strong>XPS_GLYPH_MAPPING</strong></a> structures, an element is out of sequence.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MAPPING_OUTSIDE_INDICES"></span><span id="xps_e_mapping_outside_indices"></span><dl> <span data-ttu-id="a982d-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-171"><dt><strong>XPS_E_MAPPING_OUTSIDE_INDICES</strong></dt> <dt>0x80520304</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-172">Die Symbol Zuordnungen überschreiten die Anzahl der Glyphe-Indizes.</span><span class="sxs-lookup"><span data-stu-id="a982d-172">The glyph mappings exceed the number of glyph indices.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MAPPING_OUTSIDE_STRING"></span><span id="xps_e_mapping_outside_string"></span><dl> <span data-ttu-id="a982d-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-173"><dt><strong>XPS_E_MAPPING_OUTSIDE_STRING</strong></dt> <dt>0x80520303</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-174">Fehler in den Symbol Mappings.</span><span class="sxs-lookup"><span data-stu-id="a982d-174">Error in the glyph mappings.</span></span><br/> <span data-ttu-id="a982d-175">Wenn die Unicode-Zeichenfolge leer ist, bedeutet dieser Fehler, dass auch eine Symbol Zuordnung definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a982d-175">If the Unicode string is empty, this error means that a glyph mapping was also defined.</span></span> <span data-ttu-id="a982d-176">Symbol Zuordnungen dürfen nicht definiert werden, wenn die Unicode-Zeichenfolge leer ist.</span><span class="sxs-lookup"><span data-stu-id="a982d-176">Glyph mappings must not be defined if the Unicode string is empty.</span></span><br/> <span data-ttu-id="a982d-177">Wenn die Unicode-Zeichenfolge nicht leer ist, bedeutet dieser Fehler, dass eine Symbol Zuordnung für Symbole außerhalb der Unicode-Zeichenfolge definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a982d-177">If the Unicode string is not empty, this error means that a glyph mapping was defined for glyphs outside of the Unicode string.</span></span> <span data-ttu-id="a982d-178">Symbol Zuordnungen können nicht für Symbole definiert werden, die außerhalb der Länge der Unicode-Zeichenfolge liegen.</span><span class="sxs-lookup"><span data-stu-id="a982d-178">Glyph mappings cannot be defined for glyphs that fall outside the length of the Unicode string.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_COLORPROFILE"></span><span id="xps_e_missing_colorprofile"></span><dl> <span data-ttu-id="a982d-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-179"><dt><strong>XPS_E_MISSING_COLORPROFILE</strong></dt> <dt>0x80520104</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-180">Der Farbprofil Parameter ist <strong>null</strong>, es wird jedoch ein Farbprofil erwartet.</span><span class="sxs-lookup"><span data-stu-id="a982d-180">The color profile parameter is <strong>NULL</strong>, but a color profile is expected.</span></span> <span data-ttu-id="a982d-181">Ein Farbprofil ist erforderlich, wenn der Farbtyp XPS_COLOR_TYPE_CONTEXT ist.</span><span class="sxs-lookup"><span data-stu-id="a982d-181">A color profile is required when the color type is XPS_COLOR_TYPE_CONTEXT.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DISCARDCONTROL"></span><span id="xps_e_missing_discardcontrol"></span><dl> <span data-ttu-id="a982d-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-182"><dt><strong>XPS_E_MISSING_DISCARDCONTROL</strong></dt> <dt>0x80520112</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-183">Eine Seite verweist auf verwerfbare Ressourcen, gibt jedoch keinen verwerfen-Elementnamen an.</span><span class="sxs-lookup"><span data-stu-id="a982d-183">A page refers to discardable resources but does not specify a DiscardControl part name.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_DOCUMENT"></span><span id="xps_e_missing_document"></span><dl> <span data-ttu-id="a982d-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-184"><dt><strong>XPS_E_MISSING_DOCUMENT</strong></dt> <dt>0x80520109</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>Ixpsompackagewriter:: addPage</strong></a> wurde vor <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>ixpsompackagewriter:: startnewdocument</strong></a>aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="a982d-185"><a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-addpage"><strong>IXpsOMPackageWriter::AddPage</strong></a> was called before <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP"></span><span id="xps_e_missing_documentsequence_relationship"></span><dl> <span data-ttu-id="a982d-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-186"><dt><strong>XPS_E_MISSING_DOCUMENTSEQUENCE_RELATIONSHIP</strong></dt> <dt>0x80520108</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-187">Das Paket enthält keine "FixedDocumentSequence".</span><span class="sxs-lookup"><span data-stu-id="a982d-187">The package does not contain a FixedDocumentSequence.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_FONTURI"></span><span id="xps_e_missing_fonturi"></span><dl> <span data-ttu-id="a982d-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-188"><dt><strong>XPS_E_MISSING_FONTURI</strong></dt> <dt>0x80520107</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-189">Die <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>ixpsomglyphs</strong></a> -Schnittstelle erfordert einen Schriftart-URI, aber eine ist nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-189">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface requires a font URI, but one is not specified.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_GLYPHS"></span><span id="xps_e_missing_glyphs"></span><dl> <span data-ttu-id="a982d-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-190"><dt><strong>XPS_E_MISSING_GLYPHS</strong></dt> <dt>0x80520102</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-191">Die <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>ixpsomglyphs</strong></a> -Schnittstelle ohne Unicode-Zeichenfolge gibt keine Glyphe-Indizes an.</span><span class="sxs-lookup"><span data-stu-id="a982d-191">The <a href="/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomglyphs"><strong>IXpsOMGlyphs</strong></a> interface without a Unicode string does not specify any glyph indices.</span></span> <span data-ttu-id="a982d-192">Eine <strong>ixpsomglyphs</strong> -Schnittstelle muss entweder eine Unicode-Zeichenfolge oder ein Array von Glyphe-Indizes angeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-192">An <strong>IXpsOMGlyphs</strong> interface must specify either a Unicode string or an array of glyph indices.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH"></span><span id="xps_e_missing_image_in_imagebrush"></span><dl> <span data-ttu-id="a982d-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010E</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-193"><dt><strong>XPS_E_MISSING_IMAGE_IN_IMAGEBRUSH</strong></dt> <dt>0x8052010e</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-194">Für den Bild Pinsel konnte keine Bildressource gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-194">An image resource could not be located for the image brush.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_LOOKUP"></span><span id="xps_e_missing_lookup"></span><dl> <span data-ttu-id="a982d-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-195"><dt><strong>XPS_E_MISSING_LOOKUP</strong></dt> <dt>0x80520101</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-196">Die Remote Ressource weist ein unerwartetes Objekt auf.</span><span class="sxs-lookup"><span data-stu-id="a982d-196">The remote resource has an unexpected object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_NAME"></span><span id="xps_e_missing_name"></span><dl> <span data-ttu-id="a982d-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-197"><dt><strong>XPS_E_MISSING_NAME</strong></dt> <dt>0x80520100</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-198">Die Seite wurde nicht benannt. der Status des Hyperlink-Ziels kann nur festgelegt werden, wenn die Seite einen Namen hat.</span><span class="sxs-lookup"><span data-stu-id="a982d-198">The page has not been named; the hyperlink target status can only be set if the page has a name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PAGE_IN_DOCUMENT"></span><span id="xps_e_missing_page_in_document"></span><dl> <span data-ttu-id="a982d-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-199"><dt><strong>XPS_E_MISSING_PAGE_IN_DOCUMENT</strong></dt> <dt>0x8052010c</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-200">Das FixedDocument enthält keine FixedPage-Teile.</span><span class="sxs-lookup"><span data-stu-id="a982d-200">The FixedDocument does not contain any FixedPage parts.</span></span> <span data-ttu-id="a982d-201">Ein XPS-Dokument muss mindestens einen FixedPage-Teil enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-201">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PAGE_IN_PAGEREFERENCE"></span><span id="xps_e_missing_page_in_pagereference"></span><dl> <span data-ttu-id="a982d-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-202"><dt><strong>XPS_E_MISSING_PAGE_IN_PAGEREFERENCE</strong></dt> <dt>0x8052010d</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-203">Der Seiten Verweis weist keine entsprechende Seite auf.</span><span class="sxs-lookup"><span data-stu-id="a982d-203">The page reference does not have a corresponding page.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_PART_REFERENCE"></span><span id="xps_e_missing_part_reference"></span><dl> <span data-ttu-id="a982d-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-204"><dt><strong>XPS_E_MISSING_PART_REFERENCE</strong></dt> <dt>0x80520110</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-205">Auf einen erforderlichen Zielteil wurde nicht verwiesen.</span><span class="sxs-lookup"><span data-stu-id="a982d-205">A required target part was not referenced.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_PART_STREAM"></span><span id="xps_e_missing_part_stream"></span><dl> <span data-ttu-id="a982d-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-206"><dt><strong>XPS_E_MISSING_PART_STREAM</strong></dt> <dt>0x80520113</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-207">Für die Ressource wurde kein Stream angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-207">A stream was not specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_REFERRED_DOCUMENT"></span><span id="xps_e_missing_referred_document"></span><dl> <span data-ttu-id="a982d-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-208"><dt><strong>XPS_E_MISSING_REFERRED_DOCUMENT</strong></dt> <dt>0x8052010a</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-209">Der FixedDocument-Teil, auf den von "FixedDocumentSequence" verwiesen wird, wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a982d-209">The FixedDocument part that is referenced by the FixedDocumentSequence could not be found.</span></span> <span data-ttu-id="a982d-210">Ein XPS-Dokument muss mindestens ein FixedDocument-Dokument enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-210">An XPS document must contain at least one FixedDocument.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_REFERRED_PAGE"></span><span id="xps_e_missing_referred_page"></span><dl> <span data-ttu-id="a982d-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-211"><dt><strong>XPS_E_MISSING_REFERRED_PAGE</strong></dt> <dt>0x8052010b</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-212">Der FixedPage-Teil, auf den vom FixedDocument verwiesen wird, wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="a982d-212">The FixedPage part that is referenced by the FixedDocument could not be found.</span></span> <span data-ttu-id="a982d-213">Ein XPS-Dokument muss mindestens einen FixedPage-Teil enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-213">An XPS document must contain at least one FixedPage part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RELATIONSHIP_TARGET"></span><span id="xps_e_missing_relationship_target"></span><dl> <span data-ttu-id="a982d-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-214"><dt><strong>XPS_E_MISSING_RELATIONSHIP_TARGET</strong></dt> <dt>0x80520105</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-215">Das Beziehungs Zielpart ist nicht in der Paket Beziehung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a982d-215">The relationship target part is not present in the package relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESOURCE_KEY"></span><span id="xps_e_missing_resource_key"></span><dl> <span data-ttu-id="a982d-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-216"><dt><strong>XPS_E_MISSING_RESOURCE_KEY</strong></dt> <dt>0x8052010f</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-217">Für die Ressource wurde kein <strong>x:Key</strong> -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-217">No <strong>x:Key</strong> attribute was specified for the resource.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_RESOURCE_RELATIONSHIP"></span><span id="xps_e_missing_resource_relationship"></span><dl> <span data-ttu-id="a982d-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-218"><dt><strong>XPS_E_MISSING_RESOURCE_RELATIONSHIP</strong></dt> <dt>0x80520106</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-219">Die Ressource, auf die der Inhalt der Seite oder des Remote Wörterbuchs verweist, ist nicht als Seiten Beziehung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a982d-219">The resource referred to by the page or remote dictionary content does not exist as a page relationship.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_missing_restricted_font_relationship"></span><dl> <span data-ttu-id="a982d-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-220"><dt><strong>XPS_E_MISSING_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520111</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-221">Die beschränkte Schriftart, auf die verwiesen wird, wurde im Aufrufen von <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>ixpsompackagewriter:: startnewdocument</strong></a>nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-221">The referenced restricted font was not specified in the call to <a href="/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompackagewriter-startnewdocument"><strong>IXpsOMPackageWriter::StartNewDocument</strong></a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MISSING_SEGMENT_DATA"></span><span id="xps_e_missing_segment_data"></span><dl> <span data-ttu-id="a982d-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-222"><dt><strong>XPS_E_MISSING_SEGMENT_DATA</strong></dt> <dt>0x80520103</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-223">Das Segment Daten Array weist weniger Einträge als das Array Segmenttypen auf.</span><span class="sxs-lookup"><span data-stu-id="a982d-223">The segment data array has fewer entries than the segment types array.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS"></span><span id="xps_e_multiple_documentsequence_relationships"></span><dl> <span data-ttu-id="a982d-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-224"><dt><strong>XPS_E_MULTIPLE_DOCUMENTSEQUENCE_RELATIONSHIPS</strong></dt> <dt>0x80520202</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-225">Es wurde versucht, einem Paket, das bereits ein Paket enthält, eine "FixedDocumentSequence" hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a982d-225">An attempt was made to add a FixedDocumentSequence to a package that already has one.</span></span> <span data-ttu-id="a982d-226">Ein XPS-Dokument muss nur einen FixedDocumentSequence-Teil enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-226">An XPS document must contain one and only one FixedDocumentSequence part.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT"></span><span id="xps_e_multiple_printtickets_on_document"></span><dl> <span data-ttu-id="a982d-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-227"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENT</strong></dt> <dt>0x80520206</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-228">Es wurde versucht, ein Druck Ticket auf Dokument Ebene zu einem FixedDocument hinzuzufügen, das bereits über eines verfügt.</span><span class="sxs-lookup"><span data-stu-id="a982d-228">An attempt was made to add a document-level print ticket to a FixedDocument that already has one.</span></span> <span data-ttu-id="a982d-229">Ein "FixedDocument" in einem XPS-Dokument kann nur ein Druck Ticket auf Dokument Ebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-229">A FixedDocument in an XPS document can contain only one document-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE"></span><span id="xps_e_multiple_printtickets_on_documentsequence"></span><dl> <span data-ttu-id="a982d-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-230"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_DOCUMENTSEQUENCE</strong></dt> <dt>0x80520207</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-231">Es wurde versucht, ein Druck Ticket auf Auftrags Ebene zu einer FixedDocumentSequence hinzuzufügen, die bereits über eine verfügt.</span><span class="sxs-lookup"><span data-stu-id="a982d-231">An attempt was made to add a job-level print ticket to a FixedDocumentSequence that already has one.</span></span> <span data-ttu-id="a982d-232">Die "FixedDocumentSequence" in einem XPS-Dokument kann nur ein Druck Ticket auf Auftrags Ebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-232">The FixedDocumentSequence in an XPS document can contain only one job-level print ticket.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE"></span><span id="xps_e_multiple_printtickets_on_page"></span><dl> <span data-ttu-id="a982d-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-233"><dt><strong>XPS_E_MULTIPLE_PRINTTICKETS_ON_PAGE</strong></dt> <dt>0x80520205</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-234">Es wurde versucht, ein Druck Ticket auf Seitenebene zu einer FixedPage hinzuzufügen, die bereits über eine verfügt.</span><span class="sxs-lookup"><span data-stu-id="a982d-234">An attempt was made to add a page-level print ticket to a FixedPage that already has one.</span></span> <span data-ttu-id="a982d-235">Eine FixedPage in einem XPS-Dokument kann nur ein Druck Ticket auf Seitenebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-235">A FixedPage in an XPS document can contain only one page-level print ticket.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_REFERENCES_TO_PART"></span><span id="xps_e_multiple_references_to_part"></span><dl> <span data-ttu-id="a982d-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-236"><dt><strong>XPS_E_MULTIPLE_REFERENCES_TO_PART</strong></dt> <dt>0x80520208</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-237">Die eingeschränkte Schriftart Auflistung enthielt einen eingeschränkten Schriftart Eintrag, der wiederholt wurde.</span><span class="sxs-lookup"><span data-stu-id="a982d-237">The restricted font collection contained a restricted font entry that was repeated.</span></span> <span data-ttu-id="a982d-238">Jeder Schriftart Eintrag kann in der Auflistung nur einmal vorkommen.</span><span class="sxs-lookup"><span data-stu-id="a982d-238">Each font entry can occur in the collection only once.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_RESOURCES"></span><span id="xps_e_multiple_resources"></span><dl> <span data-ttu-id="a982d-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-239"><dt><strong>XPS_E_MULTIPLE_RESOURCES</strong></dt> <dt>0x80520201</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-240">Eine Ressource mit diesem Teilnamen ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a982d-240">A resource by that part name already exists.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE"></span><span id="xps_e_multiple_thumbnails_on_package"></span><dl> <span data-ttu-id="a982d-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-241"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PACKAGE</strong></dt> <dt>0x80520204</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-242">Es wurde versucht, einem Paket, das bereits über eine Miniaturansicht verfügt, ein Miniaturbild hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a982d-242">An attempt was made to add a thumbnail image to a package that already has one.</span></span> <span data-ttu-id="a982d-243">Ein XPS-Dokument kann nur ein Miniaturbild auf Paketebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-243">An XPS document can contain only one package-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE"></span><span id="xps_e_multiple_thumbnails_on_page"></span><dl> <span data-ttu-id="a982d-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-244"><dt><strong>XPS_E_MULTIPLE_THUMBNAILS_ON_PAGE</strong></dt> <dt>0x80520203</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-245">Es wurde versucht, ein Miniaturbild auf Seitenebene zu einer FixedPage hinzuzufügen, die bereits über ein Bild verfügt.</span><span class="sxs-lookup"><span data-stu-id="a982d-245">An attempt was made to add a page-level thumbnail image to a FixedPage that already has one.</span></span> <span data-ttu-id="a982d-246">Eine FixedPage in einem XPS-Dokument kann nur ein Miniaturbild der Seitenebene enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-246">A FixedPage in an XPS document can contain only one page-level thumbnail image.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NEGATIVE_FLOAT"></span><span id="xps_e_negative_float"></span><dl> <span data-ttu-id="a982d-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-247"><dt><strong>XPS_E_NEGATIVE_FLOAT</strong></dt> <dt>0x8052030a</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-248">Ein Eintrag enthält einen negativen Wert, er muss jedoch einen nicht negativen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="a982d-248">An entry contains a negative value, but it must contain a non-negative value.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NESTED_REMOTE_DICTIONARY"></span><span id="xps_e_nested_remote_dictionary"></span><dl> <span data-ttu-id="a982d-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-249"><dt><strong>XPS_E_NESTED_REMOTE_DICTIONARY</strong></dt> <dt>0x80520402</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-250">Es wurde versucht, einen Remote-Wörterbuch Verweis zu einem Remote Wörterbuch hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a982d-250">An attempt was made to add a remote dictionary reference to a remote dictionary.</span></span> <span data-ttu-id="a982d-251">Ein Remote Wörterbuch kann nicht auf ein anderes Remote Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="a982d-251">A remote dictionary cannot reference another remote dictionary.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_NO_CUSTOM_OBJECTS"></span><span id="xps_e_no_custom_objects"></span><dl> <span data-ttu-id="a982d-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-252"><dt><strong>XPS_E_NO_CUSTOM_OBJECTS</strong></dt> <dt>0x80520502</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-253">Ein Schnittstellen Zeiger verweist nicht auf eine erkannte Schnittstellen Implementierung.</span><span class="sxs-lookup"><span data-stu-id="a982d-253">An interface pointer does not point to a recognized interface implementation.</span></span> <span data-ttu-id="a982d-254">Benutzerdefinierte Implementierungen von XPS-Dokument-API-Schnittstellen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a982d-254">Custom implementation of XPS Document API interfaces is not supported.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_NOT_ENOUGH_GRADIENT_STOPS"></span><span id="xps_e_not_enough_gradient_stops"></span><dl> <span data-ttu-id="a982d-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-255"><dt><strong>XPS_E_NOT_ENOUGH_GRADIENT_STOPS</strong></dt> <dt>0x8052050b</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-256">Die Auflistung der Farbverlaufs Stopps weist weniger als zwei Stopps auf.</span><span class="sxs-lookup"><span data-stu-id="a982d-256">The gradient stop collection has fewer than two stops.</span></span> <span data-ttu-id="a982d-257">Eine Auflistung von Farbverlaufs Stopps muss über mindestens zwei Farbverlaufs Stopps verfügen.</span><span class="sxs-lookup"><span data-stu-id="a982d-257">A gradient stop collection must have at least two gradient stops.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_ODD_BIDILEVEL"></span><span id="xps_e_odd_bidilevel"></span><dl> <span data-ttu-id="a982d-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-258"><dt><strong>XPS_E_ODD_BIDILEVEL</strong></dt> <dt>0x80520307</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-259">Die Text Zeichenfolge wurde als ausgerichtete Seite und von rechts nach Links angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-259">The text string was specified as being oriented sideways and right-to-left.</span></span> <span data-ttu-id="a982d-260">Wenn der Text seitwärts ausgerichtet ist, kann er nicht über eine Bidi-Ebene verfügen, bei der es sich um einen ungeraden Wert handelt (von rechts nach links).</span><span class="sxs-lookup"><span data-stu-id="a982d-260">If the text is oriented sideways, it cannot have a bidi level that is an odd value (right-to-left).</span></span> <span data-ttu-id="a982d-261">Ebenso kann, wenn die Bidi-Ebene ein ungerader Wert ist, der Text nicht seitwärts ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-261">Likewise, if the bidi level is an odd value, the text cannot be oriented sideways.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_ONE_TO_ONE_MAPPING_EXPECTED"></span><span id="xps_e_one_to_one_mapping_expected"></span><dl> <span data-ttu-id="a982d-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-262"><dt><strong>XPS_E_ONE_TO_ONE_MAPPING_EXPECTED</strong></dt> <dt>0x80520308</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-263">Die Symbol Zuordnungen stimmen nicht mit dem Inhalt der Unicode-Zeichenfolge identisch.</span><span class="sxs-lookup"><span data-stu-id="a982d-263">The glyph mappings do not match the Unicode string contents.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_PACKAGE_WRITER_NOT_CLOSED"></span><span id="xps_e_package_writer_not_closed"></span><dl> <span data-ttu-id="a982d-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-264"><dt><strong>XPS_E_PACKAGE_WRITER_NOT_CLOSED</strong></dt> <dt>0x8052050c</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-265">Der paketwriter wurde vor der Freigabe nicht geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a982d-265">The package writer was not closed before it was released.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RELATIONSHIP_EXTERNAL"></span><span id="xps_e_relationship_external"></span><dl> <span data-ttu-id="a982d-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-266"><dt><strong>XPS_E_RELATIONSHIP_EXTERNAL</strong></dt> <dt>0x8052050a</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-267">Eine Beziehung verweist auf einen Teil außerhalb des XPS-Dokuments.</span><span class="sxs-lookup"><span data-stu-id="a982d-267">A relationship refers to a part that is outside of the XPS document.</span></span> <span data-ttu-id="a982d-268">Alle Inhalte, die in einem XPS-Dokument gerendert werden sollen, müssen im XPS-Dokument enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-268">All content to be rendered in an XPS document must be contained in the XPS document.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_RESOURCE_NOT_OWNED"></span><span id="xps_e_resource_not_owned"></span><dl> <span data-ttu-id="a982d-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-269"><dt><strong>XPS_E_RESOURCE_NOT_OWNED</strong></dt> <dt>0x80520504</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-270">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a982d-270">Reserved.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED"></span><span id="xps_e_restricted_font_not_obfuscated"></span><dl> <span data-ttu-id="a982d-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-271"><dt><strong>XPS_E_RESTRICTED_FONT_NOT_OBFUSCATED</strong></dt> <dt>0x80520309</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-272"><em>Reserviert</em>.</span><span class="sxs-lookup"><span data-stu-id="a982d-272"><em>Reserved</em>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_STRING_TOO_LONG"></span><span id="xps_e_string_too_long"></span><dl> <span data-ttu-id="a982d-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-273"><dt><strong>XPS_E_STRING_TOO_LONG</strong></dt> <dt>0x80520300</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-274">Bei dem Versuch, eine Zeichenfolge in einen neuen Puffer zu kopieren, ist ein <strong>size_t</strong> Überlauf aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a982d-274">A <strong>size_t</strong> overflow occurred during an attempt to copy a string into a new buffer.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_TOO_MANY_INDICES"></span><span id="xps_e_too_many_indices"></span><dl> <span data-ttu-id="a982d-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-275"><dt><strong>XPS_E_TOO_MANY_INDICES</strong></dt> <dt>0x80520301</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-276">Es gab mehr Symbol Indizes als Unicode-Code Punkte.</span><span class="sxs-lookup"><span data-stu-id="a982d-276">There were more glyph indices than Unicode code points.</span></span> <span data-ttu-id="a982d-277">Wenn keine Symbol Zuordnungen vorhanden sind, muss die Anzahl von Glyphe-Indizes kleiner oder gleich der Anzahl von Unicode-Code Punkten sein.</span><span class="sxs-lookup"><span data-stu-id="a982d-277">If there are no glyph mappings, the number of glyph indices must be less than or equal to the number of Unicode code points.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNAVAILABLE_PACKAGE"></span><span id="xps_e_unavailable_package"></span><dl> <span data-ttu-id="a982d-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-278"><dt><strong>XPS_E_UNAVAILABLE_PACKAGE</strong></dt> <dt>0x80520114</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-279">Ein schwerwiegender Fehler ist aufgetreten, und der Inhalt des XPS OM kann nicht wieder hergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="a982d-279">A severe error occurred and the contents of the XPS OM might be unrecoverable.</span></span> <span data-ttu-id="a982d-280">Einige Komponenten des XPS OM sind möglicherweise weiterhin verwendbar, müssen jedoch vor der weiteren Verwendung überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-280">Some components of the XPS OM might still be usable, but they will need to be verified before being used further.</span></span> <span data-ttu-id="a982d-281">Da der Zustand des XPS-OMS nach dem zurückgeben dieses Fehlers nicht vorhergesagt werden kann, sollten alle Komponenten des XPS-OM freigegeben und verworfen werden.</span><span class="sxs-lookup"><span data-stu-id="a982d-281">Because the state of the XPS OM cannot be predicted after this error is returned, all components of the XPS OM should be released and discarded.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_COLORPROFILE"></span><span id="xps_e_unexpected_colorprofile"></span><dl> <span data-ttu-id="a982d-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-282"><dt><strong>XPS_E_UNEXPECTED_COLORPROFILE</strong></dt> <dt>0x80520505</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-283">Ein Farbprofil war vorhanden, als es nicht erwartet wurde.</span><span class="sxs-lookup"><span data-stu-id="a982d-283">A color profile was present when one was not expected.</span></span> <span data-ttu-id="a982d-284">Ein Farbprofil ist nur zulässig, wenn der Farbtyp <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>ist.</span><span class="sxs-lookup"><span data-stu-id="a982d-284">A color profile is only allowed when the color type is <a href="/windows/win32/api/xpsobjectmodel/ns-xpsobjectmodel-xps_color"><strong>XPS_COLOR_TYPE_CONTEXT</strong></a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_CONTENT_TYPE"></span><span id="xps_e_unexpected_content_type"></span><dl> <span data-ttu-id="a982d-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-285"><dt><strong>XPS_E_UNEXPECTED_CONTENT_TYPE</strong></dt> <dt>0x80520008</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-286">Das Ziel einer Beziehung ist nicht der Typ, der vom Kontext der Beziehung erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="a982d-286">The target of a relationship is not the type expected by the context of the relationship.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_UNEXPECTED_RELATIONSHIP_TYPE"></span><span id="xps_e_unexpected_relationship_type"></span><dl> <span data-ttu-id="a982d-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-287"><dt><strong>XPS_E_UNEXPECTED_RELATIONSHIP_TYPE</strong></dt> <dt>0x80520010</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-288">Der Beziehungstyp wurde nicht erkannt.</span><span class="sxs-lookup"><span data-stu-id="a982d-288">The relationship type was not recognized.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP"></span><span id="xps_e_unexpected_restricted_font_relationship"></span><dl> <span data-ttu-id="a982d-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-289"><dt><strong>XPS_E_UNEXPECTED_RESTRICTED_FONT_RELATIONSHIP</strong></dt> <dt>0x80520011</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-290">Die eingeschränkte Schriftart Auflistung enthält eine uneingeschränkte Schriftart.</span><span class="sxs-lookup"><span data-stu-id="a982d-290">The restricted font collection contains an unrestricted font.</span></span><br/></td>
</tr>
<tr class="even">
<td><span id="XPS_E_VISUAL_CIRCULAR_REF"></span><span id="xps_e_visual_circular_ref"></span><dl> <span data-ttu-id="a982d-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-291"><dt><strong>XPS_E_VISUAL_CIRCULAR_REF</strong></dt> <dt>0x80520501</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-292">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="a982d-292">Reserved.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span id="XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT"></span><span id="xps_e_xkey_attr_present_outside_res_dict"></span><dl> <span data-ttu-id="a982d-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span><span class="sxs-lookup"><span data-stu-id="a982d-293"><dt><strong>XPS_E_XKEY_ATTR_PRESENT_OUTSIDE_RES_DICT</strong></dt> <dt>0x80520400</dt> </span></span></dl></td>
<td><span data-ttu-id="a982d-294">Für eine Pfad Geometrie, die nicht in einem Ressourcen Wörterbuch enthalten ist, ist ein <strong>x:Key</strong> -Attribut angegeben.</span><span class="sxs-lookup"><span data-stu-id="a982d-294">A path geometry that is not in a resource dictionary has an <strong>x:Key</strong> attribute specified.</span></span> <span data-ttu-id="a982d-295">Pfadgeometrien, die nicht in einem Ressourcen Wörterbuch enthalten sind, dürfen kein <strong>x:Key</strong> -Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a982d-295">Path geometries that are not in a resource dictionary cannot have an <strong>x:Key</strong> attribute.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a982d-296">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a982d-296">Remarks</span></span>

<span data-ttu-id="a982d-297">Einige XPS-Dokument-API-Methoden führen Aufrufe an die [Paketierungs](/previous-versions/windows/desktop/opc/packaging) -API aus.</span><span class="sxs-lookup"><span data-stu-id="a982d-297">Some XPS document API methods make calls to the [Packaging](/previous-versions/windows/desktop/opc/packaging) API.</span></span> <span data-ttu-id="a982d-298">Informationen zu den Rückgabe Werten der Packungs-API finden Sie unter [Packen von Fehlern](/previous-versions/windows/desktop/opc/packaging-errors).</span><span class="sxs-lookup"><span data-stu-id="a982d-298">For information about the Packaging API return values, see [Packaging Errors](/previous-versions/windows/desktop/opc/packaging-errors).</span></span>

## <a name="requirements"></a><span data-ttu-id="a982d-299">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a982d-299">Requirements</span></span>



| <span data-ttu-id="a982d-300">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a982d-300">Requirement</span></span> | <span data-ttu-id="a982d-301">Wert</span><span class="sxs-lookup"><span data-stu-id="a982d-301">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a982d-302">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a982d-302">Minimum supported client</span></span><br/> | <span data-ttu-id="a982d-303">Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a982d-303">Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a982d-304">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a982d-304">Minimum supported server</span></span><br/> | <span data-ttu-id="a982d-305">Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a982d-305">Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a982d-306">Header</span><span class="sxs-lookup"><span data-stu-id="a982d-306">Header</span></span><br/>                   | <dl> <span data-ttu-id="a982d-307"><dt>Xpsobjectmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="a982d-307"><dt>Xpsobjectmodel.h</dt></span></span> </dl>                                       |
| <span data-ttu-id="a982d-308">IDL</span><span class="sxs-lookup"><span data-stu-id="a982d-308">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a982d-309"><dt>Xpsobjectmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a982d-309"><dt>XpsObjectModel.idl</dt></span></span> </dl>                                     |



## <a name="see-also"></a><span data-ttu-id="a982d-310">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a982d-310">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a982d-311">Fehlerbehandlung in com</span><span class="sxs-lookup"><span data-stu-id="a982d-311">Error Handling in COM</span></span>](../com/error-handling-in-com.md)
</dt> </dl>

 

