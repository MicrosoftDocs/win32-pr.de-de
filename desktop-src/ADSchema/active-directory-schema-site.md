---
title: Active Directory Schema-Terminologie
description: Die folgenden Begriffe werden häufig verwendet, um auf das Active Directory Schema zu verweisen.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efca7057a79d87c45cc3e3da4b604e842143fedd
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "106342388"
---
# <a name="active-directory-schema-terminology"></a><span data-ttu-id="df867-103">Active Directory Schema-Terminologie</span><span class="sxs-lookup"><span data-stu-id="df867-103">Active Directory Schema Terminology</span></span>

<span data-ttu-id="df867-104">Die folgenden Begriffe werden häufig verwendet, um auf das Active Directory Schema zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="df867-104">The following terms are commonly used to refer to the Active Directory schema.</span></span>


<dl> <dt>

<span data-ttu-id="df867-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen</span><span class="sxs-lookup"><span data-stu-id="df867-105"><span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribute</span></span>
</dt> <dd>

<span data-ttu-id="df867-106">Datenelemente, die verwendet werden, um die Objekte zu beschreiben, die von den im Schema definierten Klassen dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="df867-106">Data items used to describe the objects that are represented by the classes that are defined in the schema.</span></span> <span data-ttu-id="df867-107">Attribute werden im Schema getrennt von den Klassen definiert. auf diese Weise kann eine einzelne Attribut Definition auf viele Klassen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="df867-107">Attributes are defined in the schema separately from the classes; this allows a single attribute definition to be applied to many classes.</span></span> <span data-ttu-id="df867-108">Beispielsweise ist [**Description**](a-description.md) ein Attribut, das auf eine beliebige Klasse im Schema angewendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="df867-108">For example, [**Description**](a-description.md) is an attribute that can be applied to any class in the schema.</span></span> <span data-ttu-id="df867-109">Das **Description** -Attribut wird einmal im Schema definiert, um die Konsistenz zu gewährleisten, anstatt eine andere Definition für die **Beschreibung** eines Benutzers und die **Beschreibung** eines Druckers zu haben.</span><span class="sxs-lookup"><span data-stu-id="df867-109">The **Description** attribute is defined once in the schema, assuring consistency, rather than having a different definition for **Description** of a user and **Description** of a printer.</span></span>

> [!Note]  
> <span data-ttu-id="df867-110">Der Begriff " *Eigenschaft* " wird häufig mit dem Begriff " *Attribute*" austauschbar verwendet.</span><span class="sxs-lookup"><span data-stu-id="df867-110">The term *property* is frequently used interchangeably with the term *attribute*.</span></span>

 

</dd> <dt>

<span data-ttu-id="df867-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribut Instanz</span><span class="sxs-lookup"><span data-stu-id="df867-111"><span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribute Instance</span></span>
</dt> <dd>

<span data-ttu-id="df867-112">Ein Vorkommen eines Attributs, das im Schema definiert ist.</span><span class="sxs-lookup"><span data-stu-id="df867-112">An occurrence of an attribute that is defined in the schema.</span></span> <span data-ttu-id="df867-113">Dieser Begriff wird verwendet, um zwischen der Definition eines Attributs und einem diskreten Vorkommen des Attributs zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="df867-113">This term is used to distinguish between the definition of an attribute and a discrete occurrence of the attribute.</span></span> <span data-ttu-id="df867-114">Beispielsweise wird beim Speichern eines Benutzer Objekts für "Jeff Smith" mit dem Attribut " [**Common-Name**](a-cn.md) ", das auf "Jeff Smith" festgelegt ist, eine Instanz von [**Common-Name**](a-cn.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="df867-114">For example, storing a User object for "Jeff Smith" with the [**Common-Name**](a-cn.md) attribute set to "Jeff Smith" creates an instance of [**Common-Name**](a-cn.md).</span></span>

</dd> <dt>

<span data-ttu-id="df867-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Klassi</span><span class="sxs-lookup"><span data-stu-id="df867-115"><span id="Class"></span><span id="class"></span><span id="CLASS"></span>Class</span></span>
</dt> <dd>

<span data-ttu-id="df867-116">Eine formale Beschreibung eines diskreten, identifizierbaren Objekt Typs, der im Verzeichnisdienst gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="df867-116">A formal description of a discrete, identifiable type of object stored in the directory service.</span></span> <span data-ttu-id="df867-117">[**Benutzer**](c-user.md), [**Druck Warteschlange**](c-printqueue.md)und [**Gruppe**](c-group.md) sind z. b. alle Klassen.</span><span class="sxs-lookup"><span data-stu-id="df867-117">For example, [**User**](c-user.md), [**Print-Queue**](c-printqueue.md), and [**Group**](c-group.md) are all classes.</span></span> <span data-ttu-id="df867-118">Außerdem gibt es drei verschiedene Kategorien von Klassen: [Struktur Klassen](classes-structural.md), [abstrakte Klassen](classes-abstract.md)und [Hilfsklassen](classes-auxiliary.md).</span><span class="sxs-lookup"><span data-stu-id="df867-118">Furthermore, there are 3 distinct categories of classes: [Structural Classes](classes-structural.md), [Abstract Classes](classes-abstract.md), and [Auxiliary Classes](classes-auxiliary.md).</span></span>

</dd> <dt>

<span data-ttu-id="df867-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Klasseninstanz</span><span class="sxs-lookup"><span data-stu-id="df867-119"><span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Class Instance</span></span>
</dt> <dd>

<span data-ttu-id="df867-120">Ein Vorkommen einer-Klasse, die im Schema definiert ist.</span><span class="sxs-lookup"><span data-stu-id="df867-120">An occurrence of a class that is defined in the schema.</span></span> <span data-ttu-id="df867-121">Dieser Begriff wird verwendet, um zwischen der Definition einer Klasse und einem diskreten Vorkommen der-Klasse zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="df867-121">This term is used to distinguish between the definition of a class and a discrete occurrence of the class.</span></span> <span data-ttu-id="df867-122">Wenn Sie z. b. ein [**Benutzer**](c-user.md) Objekt für "Jeff Smith" im Verzeichnisdienst speichern, wird eine Instanz des [**Benutzers**](c-user.md)erstellt.</span><span class="sxs-lookup"><span data-stu-id="df867-122">For example, storing a [**User**](c-user.md) object for "Jeff Smith" in the directory service creates an instance of [**User**](c-user.md).</span></span>

</dd> <dt>

<span data-ttu-id="df867-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Inhalts Regeln</span><span class="sxs-lookup"><span data-stu-id="df867-123"><span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Content Rules</span></span>
</dt> <dd>

<span data-ttu-id="df867-124">Die Definition der möglichen Inhalte der Klassen Instanzen, die im Verzeichnisdienst gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="df867-124">The definition of the possible contents of the class instances that are stored in the directory service.</span></span> <span data-ttu-id="df867-125">In NT-Verzeichnisdiensten (NTDS), auf denen Active Directory basiert, werden die Inhalts Regeln vollständig durch die Attribute " [**muss enthalten**](a-mustcontain.md) " und " [**May-**](a-maycontain.md) Attribute" der Schema Definitionen für jede Klasse ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="df867-125">In NT Directory Services (NTDS), upon which Active Directory is based, the content rules are completely expressed by the [**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) attributes of the schema definitions for each class.</span></span>

</dd> <dt>

<span data-ttu-id="df867-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Ableitung</span><span class="sxs-lookup"><span data-stu-id="df867-126"><span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Derivation</span></span>
</dt> <dd>

<span data-ttu-id="df867-127">Siehe *Vererbung*.</span><span class="sxs-lookup"><span data-stu-id="df867-127">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Verzeichnis Informationsstruktur</span><span class="sxs-lookup"><span data-stu-id="df867-128"><span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Directory Information Tree</span></span>
</dt> <dd>

<span data-ttu-id="df867-129">Das Verzeichnis selbst, das als Baumstruktur dargestellt wird, in der die Scheitel Punkte die Verzeichniseinträge (Klassen Instanzen) und die Verbindungslinien für die über-und untergeordneten Beziehungen zwischen den Einträgen darstellen.</span><span class="sxs-lookup"><span data-stu-id="df867-129">The directory itself, represented as a tree structure in which the vertices are the directory entries (class instances) and the connecting lines the parent-child relationships between the entries.</span></span>

</dd> <dt>

<span data-ttu-id="df867-130"><span id="DIT"></span><span id="dit"></span>Scht</span><span class="sxs-lookup"><span data-stu-id="df867-130"><span id="DIT"></span><span id="dit"></span>DIT</span></span>
</dt> <dd>

<span data-ttu-id="df867-131">Siehe *Verzeichnis Informations* Struktur.</span><span class="sxs-lookup"><span data-stu-id="df867-131">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Zugriffsrechte Steuern</span><span class="sxs-lookup"><span data-stu-id="df867-132"><span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Control Access Rights</span></span>
</dt> <dd>

<span data-ttu-id="df867-133">Eine Klasse, die ein Zugriffsrecht beschreibt, das nicht an eine Ressource gebunden ist, sondern eine Aktion ist.</span><span class="sxs-lookup"><span data-stu-id="df867-133">A class that describes an access right not tied to a resource, but an action.</span></span> <span data-ttu-id="df867-134">So kann z. b. einem Benutzer das Recht erteilt werden, relative ID Werte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df867-134">For example, a user can be granted the right to create relative ID values.</span></span>

</dd> <dt>

<span data-ttu-id="df867-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Vererbung</span><span class="sxs-lookup"><span data-stu-id="df867-135"><span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance</span></span>
</dt> <dd>

<span data-ttu-id="df867-136">Die Fähigkeit, neue Objektklassen aus vorhandenen Objektklassen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="df867-136">The ability to build new object classes from existing object classes.</span></span> <span data-ttu-id="df867-137">Das neue-Objekt ist als eine *Unterklasse* des übergeordneten Objekts definiert.</span><span class="sxs-lookup"><span data-stu-id="df867-137">The new object is defined as a *subclass* of the parent object.</span></span> <span data-ttu-id="df867-138">Das übergeordnete Objekt wird zu einer über *geordneten Klasse* des neuen-Objekts.</span><span class="sxs-lookup"><span data-stu-id="df867-138">The parent object becomes a *superclass* of the new object.</span></span> <span data-ttu-id="df867-139">Eine Unterklasse erbt die Attribute des übergeordneten Elements, einschließlich Struktur Regeln und Inhalts Regeln.</span><span class="sxs-lookup"><span data-stu-id="df867-139">A subclass inherits the attributes of the parent, including structure rules and content rules.</span></span>

</dd> <dt>

<span data-ttu-id="df867-140"><span id="LDAP"></span><span id="ldap"></span>Standardi</span><span class="sxs-lookup"><span data-stu-id="df867-140"><span id="LDAP"></span><span id="ldap"></span>LDAP</span></span>
</dt> <dd>

<span data-ttu-id="df867-141">Siehe *Lightweight Directory Access Protocol*.</span><span class="sxs-lookup"><span data-stu-id="df867-141">See *Lightweight Directory Access Protocol*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access-Protokoll</span><span class="sxs-lookup"><span data-stu-id="df867-142"><span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol</span></span>
</dt> <dd>

<span data-ttu-id="df867-143">Ein standardmäßiges Internet Kommunikationsprotokoll, das für die Kommunikation mit den NTDS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="df867-143">A standard Internet communications protocol used to communicate with the NTDS.</span></span> <span data-ttu-id="df867-144">LDAP Version 2 und Version 3 werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="df867-144">LDAP version 2 and version 3 are supported.</span></span>

</dd> <dt>

<span data-ttu-id="df867-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT-Sicherheits Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df867-145"><span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="df867-146">Weitere Informationen finden Sie unter *Sicherheits Beschreibung*.</span><span class="sxs-lookup"><span data-stu-id="df867-146">See *Security Descriptor*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objekt</span><span class="sxs-lookup"><span data-stu-id="df867-147"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Object</span></span>
</dt> <dd>

<span data-ttu-id="df867-148">Eine Einheit der Datenspeicherung im Verzeichnisdienst.</span><span class="sxs-lookup"><span data-stu-id="df867-148">A unit of data storage in the directory service.</span></span> <span data-ttu-id="df867-149">Verzeichnisdienst Objekte müssen nicht mit COM-Objekten oder anderen objektorientierten System Objekten verwechselt werden, die eine ausführbare Komponente und ein Laufzeitverhalten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="df867-149">Directory service objects are not to be confused with COM objects or other object-oriented system objects, which have an executable component and run-time behavior.</span></span> <span data-ttu-id="df867-150">Verzeichnisdienst Objekte bestehen nur aus Daten.</span><span class="sxs-lookup"><span data-stu-id="df867-150">Directory service objects consist only of data.</span></span> <span data-ttu-id="df867-151">Ein Verzeichnisdienst Objekt wird durch ein [**Klassen Schema**](c-classschema.md) Objekt und eine Gruppe von [**Attribut Schema**](c-attributeschema.md) Objekten definiert, auf die vom [**Class-Schema-**](c-classschema.md) Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="df867-151">A directory service object is defined by a [**Class-Schema**](c-classschema.md) object and a group of [**Attribute-Schema**](c-attributeschema.md) objects referenced by the [**Class-Schema**](c-classschema.md) object.</span></span>

<span data-ttu-id="df867-152">[**Klassen-Schema-**](c-classschema.md) und [**Attribut Schema**](c-attributeschema.md) Objekte sind selbst Verzeichnisdienst Objekte und verfügen über Definitionen im Schema wie alle anderen Objekte.</span><span class="sxs-lookup"><span data-stu-id="df867-152">[**Class-Schema**](c-classschema.md) and [**Attribute-Schema**](c-attributeschema.md) objects are themselves directory service objects, and have definitions in the schema like any other objects.</span></span> <span data-ttu-id="df867-153">Siehe *Klasse*.</span><span class="sxs-lookup"><span data-stu-id="df867-153">See *Class*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="df867-154"><span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Object Identifier</span></span>
</dt> <dd>

<span data-ttu-id="df867-155">Eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und verschiedene andere Teile verteilter Anwendungen eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="df867-155">Unique numeric values, issued by various issuing authorities, to uniquely identify data elements, syntaxes, and various other parts of distributed applications.</span></span> <span data-ttu-id="df867-156">Objekt-IDs (OIDs) finden Sie in OSI-Anwendungen, X. 500-Verzeichnissen, SNMP und anderen Anwendungen, in denen die Eindeutigkeit wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="df867-156">Object Identifiers (OIDs) are found in OSI applications, X.500 Directories, SNMP, and other applications where uniqueness is important.</span></span> <span data-ttu-id="df867-157">OIDs basieren auf einer Baumstruktur, in der eine übergeordnete ausstellende Zertifizierungsstelle, z. b. das ISO, eine Verzweigung der Struktur einer untergeordneten Zertifizierungsstelle zuordnet, die wiederum untergeordnete branches zuordnen kann.</span><span class="sxs-lookup"><span data-stu-id="df867-157">OIDs are based on a tree structure, in which a superior issuing authority, such as the ISO, allocates a branch of the tree to a sub-authority, which in turn can allocate sub-branches.</span></span>

<span data-ttu-id="df867-158">OIDs in den NTDS enthalten einige von der ISO-Ausgabe für X. 500-Klassen und-Attribute und einige von Microsoft ausgestellte.</span><span class="sxs-lookup"><span data-stu-id="df867-158">OIDs in the NTDS include some issued by the ISO for X.500 classes and attributes, and some issued by Microsoft.</span></span> <span data-ttu-id="df867-159">Die OID-Notation ist eine gepunktete Zeichenfolge mit Zahlen, z. b. "1.2.840.113556.1.5.4", die in der folgenden Liste aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df867-159">OID notation is a dotted string of numbers, for example "1.2.840.113556.1.5.4", which translates as listed in the following list.</span></span> 

| <span data-ttu-id="df867-160">Wert</span><span class="sxs-lookup"><span data-stu-id="df867-160">Value</span></span>  | <span data-ttu-id="df867-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df867-161">Description</span></span>                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="df867-162">1</span><span class="sxs-lookup"><span data-stu-id="df867-162">1</span></span>      | <span data-ttu-id="df867-163">ISO: die "Stamm Zertifizierungsstelle" hat "1,2" an ANSI ausgegeben, was wiederum...</span><span class="sxs-lookup"><span data-stu-id="df867-163">ISO - the "root authority", issued "1.2" to ANSI, which in turn...</span></span>                           |
| <span data-ttu-id="df867-164">2</span><span class="sxs-lookup"><span data-stu-id="df867-164">2</span></span>      | <span data-ttu-id="df867-165">ANSI... "1.2.840" wurde für die USA ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="df867-165">ANSI ...issued "1.2.840" to USA, which in turn...</span></span>                                            |
| <span data-ttu-id="df867-166">840</span><span class="sxs-lookup"><span data-stu-id="df867-166">840</span></span>    | <span data-ttu-id="df867-167">USA... "1.2.840.113556" wurde an Microsoft ausgegeben...</span><span class="sxs-lookup"><span data-stu-id="df867-167">USA ...issued "1.2.840.113556" to Microsoft...</span></span>                                               |
| <span data-ttu-id="df867-168">113556</span><span class="sxs-lookup"><span data-stu-id="df867-168">113556</span></span> | <span data-ttu-id="df867-169">Microsoft... Dabei verwaltet Microsoft intern mehrere OID-branches unter "1.2.840.113556".</span><span class="sxs-lookup"><span data-stu-id="df867-169">Microsoft ...where Microsoft internally manages several OID branches under "1.2.840.113556".</span></span> |
| <span data-ttu-id="df867-170">1</span><span class="sxs-lookup"><span data-stu-id="df867-170">1</span></span>      | <span data-ttu-id="df867-171">Microsoft DS</span><span class="sxs-lookup"><span data-stu-id="df867-171">Microsoft DS</span></span>                                                                                 |
| <span data-ttu-id="df867-172">5</span><span class="sxs-lookup"><span data-stu-id="df867-172">5</span></span>      | <span data-ttu-id="df867-173">NTDS-Klassen</span><span class="sxs-lookup"><span data-stu-id="df867-173">NTDS Classes</span></span>                                                                                 |
| <span data-ttu-id="df867-174">4</span><span class="sxs-lookup"><span data-stu-id="df867-174">4</span></span>      | <span data-ttu-id="df867-175">Builtin-Domain</span><span class="sxs-lookup"><span data-stu-id="df867-175">Builtin-Domain</span></span>                                                                               |



 

</dd> <dt>

<span data-ttu-id="df867-176"><span id="OID"></span><span id="oid"></span>OID</span><span class="sxs-lookup"><span data-stu-id="df867-176"><span id="OID"></span><span id="oid"></span>OID</span></span>
</dt> <dd>

<span data-ttu-id="df867-177">Siehe *Objekt Bezeichner*.</span><span class="sxs-lookup"><span data-stu-id="df867-177">See *Object Identifier*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Chaos</span><span class="sxs-lookup"><span data-stu-id="df867-178"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema</span></span>
</dt> <dd>

<span data-ttu-id="df867-179">Eine formale Definition der Verzeichnisdienst Inhalte und-Struktur.</span><span class="sxs-lookup"><span data-stu-id="df867-179">A formal definition of the directory service contents and structure.</span></span> <span data-ttu-id="df867-180">Das Schema definiert alle Attribute und Klassen.</span><span class="sxs-lookup"><span data-stu-id="df867-180">The schema defines all attributes and classes.</span></span> <span data-ttu-id="df867-181">Für jede Klasse werden die Attribute " [**Poss-**](a-posssuperiors.md)Tribute", " [**muss**](a-mustcontain.md)" und " [**Mai enthalten**](a-maycontain.md) " definiert.</span><span class="sxs-lookup"><span data-stu-id="df867-181">For each class, the [**Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md), and [**May-Contain**](a-maycontain.md) attributes are defined.</span></span> <span data-ttu-id="df867-182">[**Poss-Vorgesetzten**](a-posssuperiors.md) definiert die möglichen Baumstrukturen für den Verzeichnisdienst, indem angegeben wird, welche Klassen als übergeordnete Klasse für eine bestimmte Klasse verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="df867-182">[**Poss-Superiors**](a-posssuperiors.md) defines the possible tree structures for the directory service by specifying what classes can be the parent for any given class.</span></span> <span data-ttu-id="df867-183">[**Muss**](a-mustcontain.md) die Attribute für eine Klasse enthalten, die vorhanden sein müssen, um die Klasse zu speichern [**, und welche**](a-maycontain.md) zusätzlichen Attribute optional vorhanden sein dürfen.</span><span class="sxs-lookup"><span data-stu-id="df867-183">[**Must-Contain**](a-mustcontain.md) and [**May-Contain**](a-maycontain.md) list the attributes for a class that must be present to store the class and what additional attributes may optionally be present.</span></span>

</dd> <dt>

<span data-ttu-id="df867-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Sicherheits Beschreibung</span><span class="sxs-lookup"><span data-stu-id="df867-184"><span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Security Descriptor</span></span>
</dt> <dd>

<span data-ttu-id="df867-185">Informationen zum Besitz eines Objekts und zu den Berechtigungen, die andere Benutzer für dieses Objekt besitzen.</span><span class="sxs-lookup"><span data-stu-id="df867-185">Information about the ownership of an object and the permissions that other users have on that object.</span></span> <span data-ttu-id="df867-186">Die [**NT-Security-Deskriptor**](a-ntsecuritydescriptor.md) -Eigenschaft eines Schema Eintrags enthält eine Zeichenfolge, die die Sicherheits Beschreibung des-Objekts darstellt.</span><span class="sxs-lookup"><span data-stu-id="df867-186">The [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) property of a schema entry contains a string that represents the security descriptor of the object.</span></span> <span data-ttu-id="df867-187">Weitere Informationen zum Format der Informationen in diesem Feld finden Sie unter Format der [Sicherheits Deskriptorzeichenfolge](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span><span class="sxs-lookup"><span data-stu-id="df867-187">For more information about the format of the information in this field, see [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).</span></span>

</dd> <dt>

<span data-ttu-id="df867-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Struktur Regeln</span><span class="sxs-lookup"><span data-stu-id="df867-188"><span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Structure Rules</span></span>
</dt> <dd>

<span data-ttu-id="df867-189">Die Definition der möglichen Baumstruktur oder Strukturen.</span><span class="sxs-lookup"><span data-stu-id="df867-189">The definition of the possible tree structure or structures.</span></span> <span data-ttu-id="df867-190">In den NTDS werden die Struktur Regeln vollständig durch das Attribut "Poss-Vorgesetzten" ausgedrückt, das für jedes [**Klassen Schema**](c-classschema.md) Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="df867-190">In the NTDS, the structure rules are completely expressed by the Poss-superiors attribute present on each [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="df867-191">Siehe *Schema*.</span><span class="sxs-lookup"><span data-stu-id="df867-191">See *Schema*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Unterklasse</span><span class="sxs-lookup"><span data-stu-id="df867-192"><span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Subclass</span></span>
</dt> <dd>

<span data-ttu-id="df867-193">Ein [**Klassen Schema**](c-classschema.md) Objekt, das von einem anderen [**Klassen Schema**](c-classschema.md) Objekt erbt.</span><span class="sxs-lookup"><span data-stu-id="df867-193">A [**Class-Schema**](c-classschema.md) object that inherits from another [**Class-Schema**](c-classschema.md) object.</span></span> <span data-ttu-id="df867-194">Siehe *Vererbung*.</span><span class="sxs-lookup"><span data-stu-id="df867-194">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Übergeordneten Klasse</span><span class="sxs-lookup"><span data-stu-id="df867-195"><span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclass</span></span>
</dt> <dd>

<span data-ttu-id="df867-196">Ein [**Klassen Schema**](c-classschema.md) Objekt, von dem ein oder mehrere andere [**Klassen Schema**](c-classschema.md) Objekte erben.</span><span class="sxs-lookup"><span data-stu-id="df867-196">A [**Class-Schema**](c-classschema.md) object from which one or more other [**Class-Schema**](c-classschema.md) objects inherit.</span></span> <span data-ttu-id="df867-197">Siehe *Vererbung*.</span><span class="sxs-lookup"><span data-stu-id="df867-197">See *Inheritance*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Linde</span><span class="sxs-lookup"><span data-stu-id="df867-198"><span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Tree</span></span>
</dt> <dd>

<span data-ttu-id="df867-199">Siehe *Verzeichnis Informations* Struktur.</span><span class="sxs-lookup"><span data-stu-id="df867-199">See *Directory Information Tree*.</span></span>

</dd> <dt>

<span data-ttu-id="df867-200"><span id="X.500"></span><span id="x.500"></span>X. 500</span><span class="sxs-lookup"><span data-stu-id="df867-200"><span id="X.500"></span><span id="x.500"></span>X.500</span></span>
</dt> <dd>

<span data-ttu-id="df867-201">Eine Reihe von Standards, die von der ISO-und der-Datei (ehemals CCITT) zusammen entwickelt wurden und die Benennungs-, Datendarstellung-und Kommunikationsprotokolle für einen Verzeichnisdienst angeben.</span><span class="sxs-lookup"><span data-stu-id="df867-201">A family of standards developed jointly by the ISO and ITU, formerly known as the CCITT, that specify the naming, data representation, and communications protocols for a directory service.</span></span>

</dd> </dl>

 

 