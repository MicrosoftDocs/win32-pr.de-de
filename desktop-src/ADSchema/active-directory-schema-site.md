---
title: Active Directory-Schematerminologie
description: Die folgenden Begriffe werden häufig verwendet, um auf das Active Directory-Schema zu verweisen.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836436"
---
# <a name="active-directory-schema-terminology"></a>Active Directory-Schematerminologie

Die folgenden Begriffe werden häufig verwendet, um auf das Active Directory-Schema zu verweisen.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Datenelemente, die verwendet werden, um die Objekte zu beschreiben, die durch die klassen dargestellt werden, die im Schema definiert sind. Attribute werden im Schema getrennt von den Klassen definiert. Dadurch kann eine einzelne Attributdefinition auf viele Klassen angewendet werden. Beispielsweise ist [**Description**](a-description.md) ein Attribut, das auf jede Klasse im Schema angewendet werden kann. Das **Description-Attribut** wird einmal im Schema definiert, um Konsistenz sicherzustellen, anstatt eine andere Definition für Beschreibung eines Benutzers und **Beschreibung eines** Druckers zu haben. 

> [!Note]  
> Die *Begriffseigenschaft* wird häufig synonym mit dem Begriffsattribut *verwendet.*

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attributinstanz
</dt> <dd>

Ein Vorkommen eines Attributs, das im Schema definiert ist. Dieser Begriff wird verwendet, um zwischen der Definition eines Attributs und einem diskreten Vorkommen des Attributs zu unterscheiden. Wenn Sie beispielsweise ein User-Objekt für "Jeff Smith" speichern, bei dem [**das Common-Name-Attribut**](a-cn.md) auf "Jeff Smith" festgelegt ist, wird eine Instanz von [**Common-Name erstellt.**](a-cn.md)

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Klasse
</dt> <dd>

Eine formale Beschreibung eines diskreten, identifizierbaren Objekttyps, der im Verzeichnisdienst gespeichert ist. Beispielsweise sind [**User,**](c-user.md) [**Print-Queue**](c-printqueue.md)und [**Group**](c-group.md) alle Klassen. Darüber hinaus gibt es drei verschiedene Klassenkategorien: [Strukturelle Klassen,](classes-structural.md) [abstrakte Klassen](classes-abstract.md)und [Hilfsklassen](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Klasseninstanz
</dt> <dd>

Ein Vorkommen einer Klasse, die im Schema definiert ist. Dieser Begriff wird verwendet, um zwischen der Definition einer Klasse und einem diskreten Vorkommen der -Klasse zu unterscheiden. Wenn Sie beispielsweise ein [**User-Objekt**](c-user.md) für "Jeff Smith" im Verzeichnisdienst speichern, wird eine Instanz von [**User erstellt.**](c-user.md)

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Inhaltsregeln
</dt> <dd>

Die Definition des möglichen Inhalts der Klasseninstanzen, die im Verzeichnisdienst gespeichert sind. In NT Directory Services (NTDS), auf denen Active Directory basiert, werden die Inhaltsregeln vollständig durch die [**Must-Contain-**](a-mustcontain.md) und [**May-Contain-Attribute**](a-maycontain.md) der Schemadefinitionen für jede Klasse ausgedrückt.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Ableitung
</dt> <dd>

Siehe *Vererbung*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Verzeichnisinformationsstruktur
</dt> <dd>

Das Verzeichnis selbst, dargestellt als Strukturstruktur, in der die Scheitelelemente die Verzeichniseinträge (Klasseninstanzen) sind und die verbindenden Zeilen die Über-/Unter-/Unterstellungsbeziehungen zwischen den Einträgen herstellen.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>Dit
</dt> <dd>

Weitere Informationen *finden Sie unter Verzeichnisinformationsstruktur.*

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Steuern von Zugriffsrechten
</dt> <dd>

Eine Klasse, die ein Zugriffsrecht beschreibt, das nicht an eine Ressource, sondern an eine Aktion gebunden ist. Beispielsweise kann einem Benutzer das Recht erteilt werden, relative ID zu erstellen.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Vererbung
</dt> <dd>

Die Fähigkeit, neue Objektklassen aus vorhandenen Objektklassen zu erstellen. Das neue -Objekt wird als *Unterklasse des* übergeordneten Objekts definiert. Das übergeordnete Objekt wird zu *einer Übergeordneten Klasse* des neuen Objekts. Eine Unterklasse erbt die Attribute des übergeordneten Elements, einschließlich Strukturregeln und Inhaltsregeln.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>Ldap
</dt> <dd>

Weitere Informationen finden *Sie unter Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access Protocol
</dt> <dd>

Ein Standard-Internetkommunikationsprotokoll, das für die Kommunikation mit ntds verwendet wird. LDAP-Version 2 und Version 3 werden unterstützt.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT-Sicherheitsbeschreibung
</dt> <dd>

Weitere Informationen *finden Sie unter Sicherheitsdeskriptor.*

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objekt
</dt> <dd>

Eine Einheit des Datenspeichers im Verzeichnisdienst. Verzeichnisdienstobjekte dürfen nicht mit COM-Objekten oder anderen objektorientierten Systemobjekten verwechselt werden, die eine ausführbare Komponente und ein Laufzeitverhalten haben. Verzeichnisdienstobjekte bestehen nur aus Daten. Ein Verzeichnisdienstobjekt wird durch ein [**Class-Schema-Objekt**](c-classschema.md) und eine Gruppe von [**Attribute-Schema-Objekten**](c-attributeschema.md) definiert, auf die vom [**Class-Schema-Objekt verwiesen**](c-classschema.md) wird.

[**Klassenschema-**](c-classschema.md) und [**Attributschemaobjekte**](c-attributeschema.md) sind selbst Verzeichnisdienstobjekte und verfügen wie alle anderen Objekte über Definitionen im Schema. Weitere Informationen *finden Sie unter Klasse*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Objektbezeichner
</dt> <dd>

Eindeutige numerische Werte, die von verschiedenen ausstellenden Stellen ausgegeben werden, um Datenelemente, Syntaxen und verschiedene andere Teile verteilter Anwendungen eindeutig zu identifizieren. Objektbezeichner (Object Identifiers, OIDs) befinden sich in OSI-Anwendungen, X.500-Verzeichnissen, SNMP und anderen Anwendungen, in denen Eindeutigkeit wichtig ist. OIDs basieren auf einer Struktur, in der eine übergeordnete Ausstellende Stelle, z. B. die ISO, einer Untergeordneten Autorität einen Zweig der Struktur zuteilen kann, die wiederum Untergeordnete Verzweigungen zuordnen kann.

OIDs im NTDS enthalten einige, die von der ISO für X.500-Klassen und -Attribute ausgestellt wurden, und einige von Microsoft. Die OID-Notation ist eine gepunktete Zeichenfolge mit Zahlen, z.B. "1.2.840.113556.1.5.4", die wie in der folgenden Liste aufgeführt übersetzt wird. 

| Wert  | Beschreibung                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: Die "Stammzertifizierungsstelle", die "1.2" an ANSI ausgegeben hat, die wiederum...                           |
| 2      | Ansi... hat "1.2.840" für die USA ausgegeben, die wiederum...                                            |
| 840    | Usa... ausgestellt "1.2.840.113556" an Microsoft...                                               |
| 113556 | Microsoft... Wobei Microsoft intern mehrere OID-Branches unter "1.2.840.113556" verwaltet. |
| 1      | Microsoft DS                                                                                 |
| 5      | NTDS-Klassen                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>Oid
</dt> <dd>

Siehe *Objektbezeichner*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schema
</dt> <dd>

Eine formale Definition des Inhalts und der Struktur des Verzeichnisdiensts. Das Schema definiert alle Attribute und Klassen. Für jede Klasse werden die [**Attribute Poss-Superiors**](a-posssuperiors.md), [**Must-Contain**](a-mustcontain.md)und [**May-Contain**](a-maycontain.md) definiert. [**Poss-Superiors definiert**](a-posssuperiors.md) die möglichen Strukturstrukturen für den Verzeichnisdienst, indem angegeben wird, welche Klassen das übergeordnete Element für eine bestimmte Klasse sein können. [**Must-Contain**](a-mustcontain.md) und [**May-Contain**](a-maycontain.md) listen die Attribute für eine Klasse auf, die vorhanden sein müssen, um die Klasse zu speichern, und welche zusätzlichen Attribute optional vorhanden sein können.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Sicherheitsbeschreibung
</dt> <dd>

Informationen zum Besitz eines Objekts und zu den Berechtigungen, die andere Benutzer für dieses Objekt besitzen. Die [**NT-Security-Descriptor-Eigenschaft**](a-ntsecuritydescriptor.md) eines Schemaeintrags enthält eine Zeichenfolge, die den Sicherheitsdeskriptor des Objekts darstellt. Weitere Informationen zum Format der Informationen in diesem Feld finden Sie unter [Security Descriptor String Format](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Strukturregeln
</dt> <dd>

Die Definition der möglichen Struktur oder Strukturen. Im NTDS werden die Strukturregeln vollständig durch das Poss-superiors-Attribut ausgedrückt, das für jedes [**Class-Schema-Objekt vorhanden**](c-classschema.md) ist. Weitere Informationen *finden Sie unter Schema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Unterklasse
</dt> <dd>

Ein [**Class-Schema-Objekt,**](c-classschema.md) das von einem anderen [**Class-Schema-Objekt erbt.**](c-classschema.md) Siehe *Vererbung*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Oberklasse
</dt> <dd>

Ein [**Class-Schema-Objekt,**](c-classschema.md) von dem ein oder mehrere andere [**Class-Schema-Objekte**](c-classschema.md) erben. Siehe *Vererbung*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Baum
</dt> <dd>

Weitere Informationen *finden Sie unter Verzeichnisinformationsstruktur.*

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X.500
</dt> <dd>

Eine Familie von Standards, die gemeinsam von ISO und ITU entwickelt wurden, früher als CCITT bezeichnet, die die Benennungs-, Datendarstellungs- und Kommunikationsprotokolle für einen Verzeichnisdienst angeben.

</dd> </dl>

 

 