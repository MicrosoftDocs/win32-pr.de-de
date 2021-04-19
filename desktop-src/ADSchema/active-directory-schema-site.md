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
# <a name="active-directory-schema-terminology"></a>Active Directory Schema-Terminologie

Die folgenden Begriffe werden häufig verwendet, um auf das Active Directory Schema zu verweisen.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Versehen
</dt> <dd>

Datenelemente, die verwendet werden, um die Objekte zu beschreiben, die von den im Schema definierten Klassen dargestellt werden. Attribute werden im Schema getrennt von den Klassen definiert. auf diese Weise kann eine einzelne Attribut Definition auf viele Klassen angewendet werden. Beispielsweise ist [**Description**](a-description.md) ein Attribut, das auf eine beliebige Klasse im Schema angewendet werden kann. Das **Description** -Attribut wird einmal im Schema definiert, um die Konsistenz zu gewährleisten, anstatt eine andere Definition für die **Beschreibung** eines Benutzers und die **Beschreibung** eines Druckers zu haben.

> [!Note]  
> Der Begriff " *Eigenschaft* " wird häufig mit dem Begriff " *Attribute*" austauschbar verwendet.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Attribut Instanz
</dt> <dd>

Ein Vorkommen eines Attributs, das im Schema definiert ist. Dieser Begriff wird verwendet, um zwischen der Definition eines Attributs und einem diskreten Vorkommen des Attributs zu unterscheiden. Beispielsweise wird beim Speichern eines Benutzer Objekts für "Jeff Smith" mit dem Attribut " [**Common-Name**](a-cn.md) ", das auf "Jeff Smith" festgelegt ist, eine Instanz von [**Common-Name**](a-cn.md)erstellt.

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Klassi
</dt> <dd>

Eine formale Beschreibung eines diskreten, identifizierbaren Objekt Typs, der im Verzeichnisdienst gespeichert ist. [**Benutzer**](c-user.md), [**Druck Warteschlange**](c-printqueue.md)und [**Gruppe**](c-group.md) sind z. b. alle Klassen. Außerdem gibt es drei verschiedene Kategorien von Klassen: [Struktur Klassen](classes-structural.md), [abstrakte Klassen](classes-abstract.md)und [Hilfsklassen](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Klasseninstanz
</dt> <dd>

Ein Vorkommen einer-Klasse, die im Schema definiert ist. Dieser Begriff wird verwendet, um zwischen der Definition einer Klasse und einem diskreten Vorkommen der-Klasse zu unterscheiden. Wenn Sie z. b. ein [**Benutzer**](c-user.md) Objekt für "Jeff Smith" im Verzeichnisdienst speichern, wird eine Instanz des [**Benutzers**](c-user.md)erstellt.

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Inhalts Regeln
</dt> <dd>

Die Definition der möglichen Inhalte der Klassen Instanzen, die im Verzeichnisdienst gespeichert werden. In NT-Verzeichnisdiensten (NTDS), auf denen Active Directory basiert, werden die Inhalts Regeln vollständig durch die Attribute " [**muss enthalten**](a-mustcontain.md) " und " [**May-**](a-maycontain.md) Attribute" der Schema Definitionen für jede Klasse ausgedrückt.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Ableitung
</dt> <dd>

Siehe *Vererbung*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Verzeichnis Informationsstruktur
</dt> <dd>

Das Verzeichnis selbst, das als Baumstruktur dargestellt wird, in der die Scheitel Punkte die Verzeichniseinträge (Klassen Instanzen) und die Verbindungslinien für die über-und untergeordneten Beziehungen zwischen den Einträgen darstellen.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>Scht
</dt> <dd>

Siehe *Verzeichnis Informations* Struktur.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Zugriffsrechte Steuern
</dt> <dd>

Eine Klasse, die ein Zugriffsrecht beschreibt, das nicht an eine Ressource gebunden ist, sondern eine Aktion ist. So kann z. b. einem Benutzer das Recht erteilt werden, relative ID Werte zu erstellen.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Vererbung
</dt> <dd>

Die Fähigkeit, neue Objektklassen aus vorhandenen Objektklassen zu erstellen. Das neue-Objekt ist als eine *Unterklasse* des übergeordneten Objekts definiert. Das übergeordnete Objekt wird zu einer über *geordneten Klasse* des neuen-Objekts. Eine Unterklasse erbt die Attribute des übergeordneten Elements, einschließlich Struktur Regeln und Inhalts Regeln.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>Standardi
</dt> <dd>

Siehe *Lightweight Directory Access Protocol*.

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Lightweight Directory Access-Protokoll
</dt> <dd>

Ein standardmäßiges Internet Kommunikationsprotokoll, das für die Kommunikation mit den NTDS verwendet wird. LDAP Version 2 und Version 3 werden unterstützt.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>NT-Sicherheits Beschreibung
</dt> <dd>

Weitere Informationen finden Sie unter *Sicherheits Beschreibung*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Objekt
</dt> <dd>

Eine Einheit der Datenspeicherung im Verzeichnisdienst. Verzeichnisdienst Objekte müssen nicht mit COM-Objekten oder anderen objektorientierten System Objekten verwechselt werden, die eine ausführbare Komponente und ein Laufzeitverhalten aufweisen. Verzeichnisdienst Objekte bestehen nur aus Daten. Ein Verzeichnisdienst Objekt wird durch ein [**Klassen Schema**](c-classschema.md) Objekt und eine Gruppe von [**Attribut Schema**](c-attributeschema.md) Objekten definiert, auf die vom [**Class-Schema-**](c-classschema.md) Objekt verwiesen wird.

[**Klassen-Schema-**](c-classschema.md) und [**Attribut Schema**](c-attributeschema.md) Objekte sind selbst Verzeichnisdienst Objekte und verfügen über Definitionen im Schema wie alle anderen Objekte. Siehe *Klasse*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Objekt Bezeichner
</dt> <dd>

Eindeutige numerische Werte, die von verschiedenen ausstellenden Behörden ausgegeben werden, um Datenelemente, Syntaxen und verschiedene andere Teile verteilter Anwendungen eindeutig zu identifizieren. Objekt-IDs (OIDs) finden Sie in OSI-Anwendungen, X. 500-Verzeichnissen, SNMP und anderen Anwendungen, in denen die Eindeutigkeit wichtig ist. OIDs basieren auf einer Baumstruktur, in der eine übergeordnete ausstellende Zertifizierungsstelle, z. b. das ISO, eine Verzweigung der Struktur einer untergeordneten Zertifizierungsstelle zuordnet, die wiederum untergeordnete branches zuordnen kann.

OIDs in den NTDS enthalten einige von der ISO-Ausgabe für X. 500-Klassen und-Attribute und einige von Microsoft ausgestellte. Die OID-Notation ist eine gepunktete Zeichenfolge mit Zahlen, z. b. "1.2.840.113556.1.5.4", die in der folgenden Liste aufgeführt wird. 

| Wert  | BESCHREIBUNG                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO: die "Stamm Zertifizierungsstelle" hat "1,2" an ANSI ausgegeben, was wiederum...                           |
| 2      | ANSI... "1.2.840" wurde für die USA ausgegeben.                                            |
| 840    | USA... "1.2.840.113556" wurde an Microsoft ausgegeben...                                               |
| 113556 | Microsoft... Dabei verwaltet Microsoft intern mehrere OID-branches unter "1.2.840.113556". |
| 1      | Microsoft DS                                                                                 |
| 5      | NTDS-Klassen                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Siehe *Objekt Bezeichner*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Chaos
</dt> <dd>

Eine formale Definition der Verzeichnisdienst Inhalte und-Struktur. Das Schema definiert alle Attribute und Klassen. Für jede Klasse werden die Attribute " [**Poss-**](a-posssuperiors.md)Tribute", " [**muss**](a-mustcontain.md)" und " [**Mai enthalten**](a-maycontain.md) " definiert. [**Poss-Vorgesetzten**](a-posssuperiors.md) definiert die möglichen Baumstrukturen für den Verzeichnisdienst, indem angegeben wird, welche Klassen als übergeordnete Klasse für eine bestimmte Klasse verwendet werden können. [**Muss**](a-mustcontain.md) die Attribute für eine Klasse enthalten, die vorhanden sein müssen, um die Klasse zu speichern [**, und welche**](a-maycontain.md) zusätzlichen Attribute optional vorhanden sein dürfen.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Sicherheits Beschreibung
</dt> <dd>

Informationen zum Besitz eines Objekts und zu den Berechtigungen, die andere Benutzer für dieses Objekt besitzen. Die [**NT-Security-Deskriptor**](a-ntsecuritydescriptor.md) -Eigenschaft eines Schema Eintrags enthält eine Zeichenfolge, die die Sicherheits Beschreibung des-Objekts darstellt. Weitere Informationen zum Format der Informationen in diesem Feld finden Sie unter Format der [Sicherheits Deskriptorzeichenfolge](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Struktur Regeln
</dt> <dd>

Die Definition der möglichen Baumstruktur oder Strukturen. In den NTDS werden die Struktur Regeln vollständig durch das Attribut "Poss-Vorgesetzten" ausgedrückt, das für jedes [**Klassen Schema**](c-classschema.md) Objekt vorhanden ist. Siehe *Schema*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Unterklasse
</dt> <dd>

Ein [**Klassen Schema**](c-classschema.md) Objekt, das von einem anderen [**Klassen Schema**](c-classschema.md) Objekt erbt. Siehe *Vererbung*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Übergeordneten Klasse
</dt> <dd>

Ein [**Klassen Schema**](c-classschema.md) Objekt, von dem ein oder mehrere andere [**Klassen Schema**](c-classschema.md) Objekte erben. Siehe *Vererbung*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Linde
</dt> <dd>

Siehe *Verzeichnis Informations* Struktur.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

Eine Reihe von Standards, die von der ISO-und der-Datei (ehemals CCITT) zusammen entwickelt wurden und die Benennungs-, Datendarstellung-und Kommunikationsprotokolle für einen Verzeichnisdienst angeben.

</dd> </dl>

 

 