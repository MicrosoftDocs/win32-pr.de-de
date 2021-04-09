---
description: Das Object-Type-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben. Der SNMP-Anbieter konvertiert ein MIB in die entsprechenden Teile des ObjektType-Makros.
ms.assetid: ad76a4fc-354e-4270-862c-062aa523bf7e
ms.tgt_platform: multiple
title: Object-Type-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c605a414c402f2cf2d18be2d966db6408f23cdc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128077"
---
# <a name="object-type-macro"></a><span data-ttu-id="d03bb-104">Object-Type-Makro</span><span class="sxs-lookup"><span data-stu-id="d03bb-104">OBJECT-TYPE Macro</span></span>

<span data-ttu-id="d03bb-105">Das Object-Type-Makro enthält obligatorische und optionale Klauseln, die die grundlegenden Merkmale eines MIB-Objekts beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d03bb-105">The OBJECT-TYPE macro contains mandatory and optional clauses that describe the basic characteristics of a MIB object.</span></span> <span data-ttu-id="d03bb-106">Der SNMP-Anbieter konvertiert ein MIB in die entsprechenden Teile des ObjektType-Makros.</span><span class="sxs-lookup"><span data-stu-id="d03bb-106">The SNMP Provider converts an MIB to the corresponding parts of the OBJECT-TYPE macro.</span></span>

> [!Note]  
> <span data-ttu-id="d03bb-107">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="d03bb-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

## <a name="components"></a><span data-ttu-id="d03bb-108">Komponenten</span><span class="sxs-lookup"><span data-stu-id="d03bb-108">Components</span></span>

<dl> <dt>

<span data-ttu-id="d03bb-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB-Objekt</span><span class="sxs-lookup"><span data-stu-id="d03bb-109"><span id="MIB_object"></span><span id="mib_object"></span><span id="MIB_OBJECT"></span>MIB object</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-110">Objekt, das den größten Teil der fraglichen Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="d03bb-110">Object that contains most of the data in question.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Objekt Deskriptor</span><span class="sxs-lookup"><span data-stu-id="d03bb-111"><span id="Object_descriptor"></span><span id="object_descriptor"></span><span id="OBJECT_DESCRIPTOR"></span>Object descriptor</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-112">Eindeutiger Name oder Objekt Deskriptor, der jedes MIB-Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d03bb-112">Unique name or object descriptor identifying each MIB object.</span></span> <span data-ttu-id="d03bb-113">Jeder MIB-Objekt Deskriptor ist exakt einem CIM-Eigenschaftsnamen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-113">Each MIB object descriptor maps exactly to a CIM property name.</span></span> <span data-ttu-id="d03bb-114">**Ifindex** beispielsweise wird in **ifindex** übersetzt.</span><span class="sxs-lookup"><span data-stu-id="d03bb-114">For example, **ifIndex** translates to **ifIndex**.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[Syntax Klausel](syntax-clause.md)</span><span class="sxs-lookup"><span data-stu-id="d03bb-115"><span id="SYNTAX_Clause"></span><span id="syntax_clause"></span><span id="SYNTAX_CLAUSE"></span>[SYNTAX Clause](syntax-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-116">Definiert die Daten und den Typ eines MIB-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d03bb-116">Defines the data and type of an MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[Index-Klausel](index-clause.md)</span><span class="sxs-lookup"><span data-stu-id="d03bb-117"><span id="INDEX_clause"></span><span id="index_clause"></span><span id="INDEX_CLAUSE"></span>[INDEX clause](index-clause.md)</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-118">Definiert einen Schlüssel zum Auswählen einer eindeutigen Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="d03bb-118">Defines a key for selecting a unique table row.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>Augments-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-119"><span id="AUGMENTS_clause"></span><span id="augments_clause"></span><span id="AUGMENTS_CLAUSE"></span>AUGMENTS clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-120">Gibt an, dass die von Ihnen festgelegten Tabellen Auflistung als Erweiterung einer anderen Tabellen Auflistung angesehen werden kann, und kann die Index Klausel in SNMPv2 ersetzen.</span><span class="sxs-lookup"><span data-stu-id="d03bb-120">Indicates that the table collection it specifies can be considered an extension of another table collection, and can replace the INDEX clause in SNMPv2.</span></span> <span data-ttu-id="d03bb-121">Die Auflistungen, auf die durch die Erweiterungs Klausel verwiesen wird, können mit der anderen Tabellen Auflistung kombiniert werden, um eine Sammlung zu bilden.</span><span class="sxs-lookup"><span data-stu-id="d03bb-121">The collections referred to by the AUGMENTS clause can be combined with the other table collection to form one collection.</span></span> <span data-ttu-id="d03bb-122">Die resultierende Auflistung gibt die in der letzten Tabellen Auflistung in der Kette angegebenen Primärschlüssel Eigenschaften frei.</span><span class="sxs-lookup"><span data-stu-id="d03bb-122">The resulting collection shares the primary key properties specified in the last table collection in the chain.</span></span>

<span data-ttu-id="d03bb-123">In diesem Fall werden die zuvor für die Index-Klausel angegebenen Zustellungs Regeln auf die letzte Tabellen Auflistung in der Kette angewendet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-123">In this case, the previous mapping rules specified for the INDEX clause are applied to the last table collection in the chain.</span></span> <span data-ttu-id="d03bb-124">Die Auflistung von-Objekten wird dann einer CIM-Klassendefinition zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-124">The collection of objects then maps to one CIM class definition.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>Object-Identifier-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-125"><span id="OBJECT-IDENTIFIER_clause"></span><span id="object-identifier_clause"></span><span id="OBJECT-IDENTIFIER_CLAUSE"></span>OBJECT-IDENTIFIER clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-126">Enthält einen eindeutigen Objekt Bezeichner für ein MIB-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d03bb-126">Contains a unique object identifier for an MIB object.</span></span> <span data-ttu-id="d03bb-127">Dieser Objekt Bezeichner wird dem **Objekt \_ Bezeichner** des CIM-Eigenschaften Qualifizierers zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-127">This object identifier maps to the CIM property qualifier **object\_identifier**.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[Access-und Max-Access-Klauseln](access-and-max-access-clauses.md)</span><span class="sxs-lookup"><span data-stu-id="d03bb-128"><span id="ACCESS_and_MAX-ACCESS_Clauses"></span><span id="access_and_max-access_clauses"></span><span id="ACCESS_AND_MAX-ACCESS_CLAUSES"></span>[ACCESS and MAX-ACCESS Clauses](access-and-max-access-clauses.md)</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-129">Definieren Sie die Zugriffsrechte für das MIB-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d03bb-129">Define the access rights to the MIB object.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>Description-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-130"><span id="DESCRIPTION_clause"></span><span id="description_clause"></span><span id="DESCRIPTION_CLAUSE"></span>DESCRIPTION clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-131">Stellt eine Textbeschreibung des-Objekts bereit, das der CIM-Eigenschaften **qualifiziererbeschreibung** zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d03bb-131">Provides a text description of the object, which maps to the CIM property qualifier **Description**.</span></span> <span data-ttu-id="d03bb-132">Diese Klausel ist möglicherweise leer.</span><span class="sxs-lookup"><span data-stu-id="d03bb-132">This clause may be empty.</span></span>

<span data-ttu-id="d03bb-133">Jede **Tabelle** und jedes **Eingabe** Objekt in einer SNMP-Tabellendefinition enthält auch eine Beschreibungs Klausel, die auch leer sein kann.</span><span class="sxs-lookup"><span data-stu-id="d03bb-133">Each **TABLE** and **ENTRY** object in an SNMP table definition also contains a DESCRIPTION clause, which also may be empty.</span></span> <span data-ttu-id="d03bb-134">Die Tabellen-und Eintrags Beschreibungs Klauseln werden verkettet, und das Ergebnis wird der **Beschreibung** der CIM-Klassen Qualifizierer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-134">The TABLE and ENTRY DESCRIPTION clauses are concatenated and the result maps to the CIM class qualifier **Description**.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>Status-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-135"><span id="STATUS_clause"></span><span id="status_clause"></span><span id="STATUS_CLAUSE"></span>STATUS clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-136">Gibt an, ob das Objekt unterstützt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d03bb-136">Indicates whether the object must be supported.</span></span> <span data-ttu-id="d03bb-137">Wenn der Wert der Status-Klausel **veraltet** ist, verwirft der Anbieter das MIB-Objekt aus der Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d03bb-137">When the value of the STATUS clause is **obsolete**, the provider discards the MIB object from the mapping.</span></span> <span data-ttu-id="d03bb-138">Andernfalls wird die Status-Klausel dem CIM-Eigenschaften **qualifiziererstatus** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-138">Otherwise, the STATUS clause maps to the CIM property qualifier **Status**.</span></span>

<span data-ttu-id="d03bb-139">Der bevorzugte **Wert für SNMPv1 ist entweder** **obligatorisch** oder **optional**, aber der Qualifizierer kann einen anderen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="d03bb-139">For SNMPv1, the preferred value of **Status** is either **mandatory** or **optional**, but the qualifier can contain some other value.</span></span> <span data-ttu-id="d03bb-140">Der bevorzugte **Wert für SNMPv2C ist entweder** **Current** oder **veraltet**, aber der Qualifizierer kann einen anderen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="d03bb-140">For SNMPv2C, the preferred value of **Status** is either **current** or **deprecated**, but the qualifier can contain some other value.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>Defval-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-141"><span id="DEFVAL_clause"></span><span id="defval_clause"></span><span id="DEFVAL_CLAUSE"></span>DEFVAL clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-142">Weist einer Variablen in einer logischen Tabellenzeile einen Standardwert zu und wird dem Zeichen folgen-CIM-Eigenschafts Qualifizierer **defval** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d03bb-142">Assigns a default value to a variable in a logical table row, and maps to the string CIM property qualifier **Defval**.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>Reference-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-143"><span id="REFERENCE_clause"></span><span id="reference_clause"></span><span id="REFERENCE_CLAUSE"></span>REFERENCE clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-144">Verweist auf ein anderes Dokument, das weitere Informationen zum-Objekt enthält.</span><span class="sxs-lookup"><span data-stu-id="d03bb-144">Refers to another document that contains more information about the object.</span></span> <span data-ttu-id="d03bb-145">Diese Klausel wird dem CIM-Eigenschafts **qualifiziererverweis** zugeordnet, der vom Typ "String" ist.</span><span class="sxs-lookup"><span data-stu-id="d03bb-145">This clause maps to the CIM property qualifier **Reference**, which is of type string.</span></span>

</dd> <dt>

<span data-ttu-id="d03bb-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>Units-Klausel</span><span class="sxs-lookup"><span data-stu-id="d03bb-146"><span id="UNITS_clause"></span><span id="units_clause"></span><span id="UNITS_CLAUSE"></span>UNITS clause</span></span>
</dt> <dd>

<span data-ttu-id="d03bb-147">Stellt eine genaue Definition der Darstellung des-Objekts bereit.</span><span class="sxs-lookup"><span data-stu-id="d03bb-147">Provides a precise definition of what the object represents.</span></span> <span data-ttu-id="d03bb-148">Diese Klausel ist den CIM-Eigenschaften **qualifizierereinheiten** zugeordnet, die den Typ "String" haben.</span><span class="sxs-lookup"><span data-stu-id="d03bb-148">This clause maps to the CIM property qualifier **Units**, which is of type string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d03bb-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d03bb-149">Remarks</span></span>

<span data-ttu-id="d03bb-150">Das Object-Type-Makro beschreibt die Grundmerkmale eines einzelnen MIB-Objekts.</span><span class="sxs-lookup"><span data-stu-id="d03bb-150">The OBJECT-TYPE macro describes the basic characteristics of an individual MIB object.</span></span> <span data-ttu-id="d03bb-151">Ein Satz von Objekttyp Makros kann als Gruppe verwandter Objekte betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="d03bb-151">A set of OBJECT-TYPE macros can be considered as a group of related objects.</span></span> <span data-ttu-id="d03bb-152">Verwenden Sie in SNMPv2C das Objektgruppen Makro, um Sätze verwandter Objekte formal in eine Auflistung zu gruppieren.</span><span class="sxs-lookup"><span data-stu-id="d03bb-152">In SNMPv2C, use the OBJECT-GROUP macro to formally group sets of related objects into a collection.</span></span> <span data-ttu-id="d03bb-153">Es ist jedoch kein formaler Mechanismus zum Erstellen von Sammlungen in SNMPv1 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d03bb-153">However, there is no formal mechanism for creating collections in SNMPv1.</span></span> <span data-ttu-id="d03bb-154">Für den SNMP-Anbieter wird das Objektgruppen Makro ignoriert, Sie können jedoch Gruppierungs Beziehungen und fabrizieren von Auflistungen erfinden.</span><span class="sxs-lookup"><span data-stu-id="d03bb-154">For the purposes of the SNMP Provider, the OBJECT-GROUP macro is ignored, but you can invent grouping relationships and fabricate collections.</span></span>

 

 



