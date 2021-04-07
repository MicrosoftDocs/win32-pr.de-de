---
title: Eigenschaften von Objektklassen
description: Jede Objektklasse in Active Directory Domain Services wird von einem classSchema-Objekt im Schema Container definiert.
ms.assetid: 88a2b2a3-e8e2-4be1-9784-9709cbea08d6
ms.tgt_platform: multiple
keywords:
- Merkmale von Objektklassen AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00c7e750d53597d1532d48c3c463315f8a48bd6d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724632"
---
# <a name="characteristics-of-object-classes"></a>Eigenschaften von Objektklassen

Jede Objektklasse in Active Directory Domain Services wird von einem **classSchema** -Objekt im Schema Container definiert. Die Attribute eines **classSchema** -Objekts geben die Eigenschaften der Klasse an, z. b.:

-   Klassen Bezeichner: Klassen verfügen über mehrere Bezeichner, einschließlich **ldapDisplayName**, die von LDAP-Clients verwendet werden, um die Klasse in Suchfiltern zu identifizieren, und **schemaIdGUID**, die in Sicherheits Deskriptoren zum Steuern des Zugriffs auf die Klasse verwendet werden.
-   Mögliche Attribute: eine Objektklassen Definition enthält Listen mit den obligatorischen und optionalen Attributen, die für eine Instanz der-Klasse festgelegt werden können.
-   Mögliche übergeordnete Elemente: Jede Objektinstanz, mit Ausnahme des Stamms der Verzeichnishierarchie, verfügt über genau ein übergeordnetes Element. Eine Objektklassen Definition enthält Listen möglicher übergeordneter Elemente, d. h. der Objektklassen, die eine Instanz der Klasse enthalten können.
-   Super Classes und Hilfsklassen: jede Objektklasse (außer [*Top*](/previous-versions/windows/desktop/legacy/ms681941(v=vs.85))) wird von einer anderen Klasse abgeleitet. Eine Klasse erbt mögliche Attribute und mögliche übergeordnete Elemente aus den übergeordneten Klassen in der Klassenhierarchie. Eine Klasse kann auch über eine beliebige Anzahl von Hilfsklassen verfügen, von denen Sie Listen möglicher Attribute erbt. Weitere Informationen finden Sie unter [Klassen Vererbung im Active Directory Schema](class-inheritance-in-the-active-directory-schema.md).

In der folgenden Tabelle sind der **ldapDisplayName** und die Beschreibung der Schlüssel Attribute eines **classSchema** -Objekts aufgelistet. Weitere Informationen und eine komplette Liste der obligatorischen und optionalen Attribute eines **classSchema** -Objekts finden Sie unter [**classSchema**](/windows/desktop/ADSchema/c-classschema).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>lDAPDisplayName</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>2.300</strong></td>
<td>Jedes Objekt in Active Directory Domain Services verfügt über ein Naming-Attribut, von dem der Relative Distinguished Name (RDN) gebildet wird. Das Benennungs Attribut für <strong>classSchema</strong> -Objekte lautet <strong>CN</strong> (Common-Name). Der dem <strong>CN</strong> zugewiesene Wert ist der Wert, der von der Objektklasse als RDN zugewiesen wird. Beispielsweise ist der <strong>CN</strong> der <strong>OrganizationalUnit</strong> -Objektklasse Organisationseinheit, die in einem Distinguished Name als CN = Organisationseinheit angezeigt wird. Der <strong>CN</strong> muss im Schema Container eindeutig sein.</td>
</tr>
<tr class="even">
<td><strong>lDAPDisplayName</strong></td>
<td>Der Name, der von LDAP-Clients verwendet wird, z. b. der ADSI LDAP-Anbieter, um auf die Klasse zu verweisen, z. b. um die Klasse in einem Suchfilter anzugeben. Der <strong>ldapDisplayName</strong> einer Klasse muss im Schema Container eindeutig sein, was bedeutet, dass Sie für alle <strong>classSchema</strong> -und <strong>attributeSchema</strong> -Objekte eindeutig sein muss. Weitere Informationen zum Erstellen einer <strong>CN</strong> und eines <strong>ldapDisplayName</strong> für eine neue Klasse finden Sie unter <a href="naming-attributes-and-classes.md">Benennen von Attributen und Klassen</a>.</td>
</tr>
<tr class="odd">
<td><strong>schemaIDGUID</strong></td>
<td>Eine GUID, die als Oktett-Zeichenfolge gespeichert ist. Mit dieser GUID wird die-Klasse eindeutig identifiziert. Diese GUID kann in Zugriffs Steuerungs Einträgen verwendet werden, um den Zugriff auf Objekte dieser Klasse zu steuern. Weitere Informationen finden Sie unter <a href="setting-permissions-on-child-object-operations.md">Festlegen von Berechtigungen für untergeordnete Objekt Vorgänge</a>. Beim Erstellen des <strong>classSchema</strong> -Objekts generiert der Active Directory Server diesen Wert, wenn er nicht angegeben ist. Wenn Sie eine neue Klasse erstellen, generieren Sie eine eigene GUID für jede Klasse, damit alle Installationen der Erweiterung die gleiche <strong>schemaIdGUID</strong> verwenden, um auf die Klasse zu verweisen.<br/></td>
</tr>
<tr class="even">
<td><strong>adminDisplayName</strong></td>
<td>Ein Anzeige Name der Klasse, die in Verwaltungs Tools verwendet werden soll. Wenn <strong>adminDisplayName</strong> beim Erstellen einer Klasse nicht angegeben wird, verwendet das System den Common-Name Wert als anzeigen Amen. Dieser Anzeige Name wird nur verwendet, wenn in der <strong>classdisplayname</strong> -Eigenschaft des Anzeige Spezifizierers für die-Klasse keine Zuordnung vorhanden ist. Weitere Informationen finden Sie unter <a href="display-specifiers.md">Anzeige Spezifizierer</a> und <a href="class-and-attribute-display-names.md">Klassen-und Attribut anzeigen Amen</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>governsID</strong></td>
<td>Die OID der-Klasse. Dieser Wert muss für die <strong>governsids</strong> aller <strong>classSchema</strong> -Objekte und die <strong>attributeids</strong> aller <strong>attributeSchema</strong> -Objekte eindeutig sein. Weitere Informationen finden Sie unter <a href="object-identifiers.md">Objekt</a>Bezeichner.</td>
</tr>
<tr class="even">
<td><strong>rDNAttID</strong></td>
<td>Gibt das Benennungs Attribut an. Hierbei handelt es sich um das Attribut, das den RDN für diese Klasse bereitstellt, wenn dies vom Standard (<strong>CN</strong>) abweicht. Die Verwendung eines anderen Namens Attributs als <strong>CN</strong> ist nicht empfehlenswert. Benennungs Attribute sollten aus dem bekannten Satz (OE, CN, O, L und DC) gezeichnet werden, der von allen LDAP Version 3-Clients verstanden wird. Weitere Informationen finden Sie unter <a href="object-names-and-identities.md">Objektnamen und-Identitäten</a> und <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">Syntaxen für Attribute in Active Directory Domain Services</a>. Ein Benennungs Attribut muss die Syntax der Verzeichnis Zeichenfolge aufweisen. Weitere Informationen finden Sie unter <a href="syntaxes-for-attributes-in-active-directory-domain-services.md">Syntax für Attribute in Active Directory Domain Services</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>mustare</strong>, <strong>systemmust-enthalten</strong></td>
<td>Ein paar von mehrwertigen Eigenschaften, die die Attribute angeben, die in Instanzen dieser Klasse vorhanden sein müssen. Dabei handelt es sich um obligatorische Attribute, die während der Erstellung vorhanden sein müssen und nach der Erstellung nicht gelöscht werden können. Nach der Erstellung der-Klasse können diese Eigenschaften nicht mehr geändert werden. Der vollständige Satz erforderlicher Attribute für eine Klasse ist die Kombination der <strong>systemmust-</strong> und <strong>must-</strong> Werte für diese Klasse und alle geerbten Klassen.<br/></td>
</tr>
<tr class="even">
<td><strong>mayare</strong>, <strong>systemmayenth;</strong></td>
<td>Ein paar von mehrwertigen Eigenschaften, die die Attribute angeben, die möglicherweise in Instanzen dieser Klasse vorhanden sind. Dabei handelt es sich um optionale Attribute, die nicht obligatorisch sind und daher in einer Instanz dieser Klasse vorhanden sein können. Sie können die Werte von " <strong>mayare</strong> " aus einem vorhandenen "Category 1"-oder "Category 2 <strong>classSchema</strong> "-Objekt hinzufügen Vor dem Entfernen eines <strong>mayare</strong> -Werts aus einem <strong>classSchema</strong> -Objekt sollten Sie nach Instanzen der Objektklasse suchen und alle Werte für das Attribut löschen, das Sie entfernen. Nach der Erstellung der-Klasse kann die <strong>systemmayare</strong> -Eigenschaft nicht mehr geändert werden. der vollständige Satz optionaler Attribute für eine Klasse ist die Vereinigung der <strong>systemmayare</strong> -und <strong>May-</strong> Werte für diese Klasse und alle geerbten Klassen.<br/></td>
</tr>
<tr class="odd">
<td><strong>Besitzer</strong>, <strong>systempossvorgesetzten</strong></td>
<td>Ein paar von mehrwertigen Eigenschaften, die die strukturellen Klassen angeben, die juristische übergeordnete Elemente von Instanzen dieser Klasse sein können. Der vollständige Satz der möglichen Vorgesetzten ist die Vereinigung der <strong>systempossvorgesetzten</strong> -und- <strong>Besitzer</strong> Werte für diese Klasse und aller geerbten strukturellen oder abstrakten Klassen. <strong>systemposs-</strong> und- <strong>Besitzer</strong> Werte werden nicht von Hilfsklassen geerbt. Sie können <strong>Besitzer</strong> Werte aus einem vorhandenen Category 1-oder Category 2 <strong>classSchema</strong> -Objekt hinzufügen oder daraus entfernen. Nach der Erstellung der-Klasse kann die <strong>systempossvorgesetzten</strong> -Eigenschaft nicht mehr geändert werden.<br/></td>
</tr>
<tr class="even">
<td><strong>objectClassCategory</strong></td>
<td>Ein ganzzahliger Wert, der die Kategorie der Klasse angibt, die einen der folgenden Werte aufweisen kann:
<ul>
<li>Strukturelle, d. h., Sie kann im Verzeichnis instanziiert werden.</li>
<li>Abstract bedeutet, dass die-Klasse eine grundlegende Definition einer Klasse bereitstellt, die zum bilden von Struktur Klassen verwendet werden kann.</li>
<li>Dies bedeutet, dass eine Klasse, die verwendet werden kann, um die Definition einer Klasse zu erweitern, die von ihr erbt, aber nicht verwendet werden kann, um allein eine Klasse zu bilden.</li>
</ul>
Weitere Informationen finden Sie unter <a href="structural-abstract-and-auxiliary-classes.md">Struktur-, abstrakte und Hilfsklassen</a>.<br/></td>
</tr>
<tr class="odd">
<td><strong>subClassOf</strong></td>
<td>Eine OID für die unmittelbare übergeordnete Klasse dieser Klasse, d. h. die Klasse, von der diese Klasse abgeleitet wird. Bei Struktur Klassen kann <strong>subClassOf</strong> eine strukturelle oder abstrakte Klasse sein.<br/> Bei abstrakten Klassen kann <strong>subClassOf</strong> nur eine abstrakte Klasse sein.<br/> Bei Erweiterungs Klassen kann <strong>subClassOf</strong> eine abstrakte oder eine zusätzliche Klasse sein.<br/> Wenn Sie eine neue Klasse definieren, stellen Sie sicher, dass die Klasse <strong>subClassOf</strong> vorhanden ist oder vorhanden ist, wenn die neue Klasse in das Verzeichnis geschrieben wird. Wenn die Klasse nicht vorhanden ist, wird das <strong>classSchema</strong> -Objekt nicht dem Verzeichnis hinzugefügt.<br/></td>
</tr>
<tr class="even">
<td><strong>auxiliaryClass</strong>, <strong>systemAuxiliaryClass</strong></td>
<td>Ein paar von mehrwertigen Eigenschaften, die die Erweiterungs Klassen angeben, von denen diese Klasse erbt. Der vollständige Satz von Hilfsklassen ist die Vereinigung der <strong>systemAuxiliaryClass</strong> -und <strong>auxiliaryClass</strong> -Werte für diese Klasse und alle geerbten Klassen. Für ein vorhandenes <strong>classSchema</strong> -Objekt können Werte der <strong>auxiliaryClass</strong> -Eigenschaft hinzugefügt, aber nicht entfernt werden. Nach der Erstellung der-Klasse kann die <strong>systemAuxiliaryClass</strong> -Eigenschaft nicht mehr geändert werden.<br/></td>
</tr>
<tr class="odd">
<td><strong>defaultObjectCategory</strong></td>
<td>Der Distinguished Name dieser Objektklasse oder einer ihrer übergeordneten Klassen. Wenn eine Instanz dieser Objektklasse erstellt wird, legt das System die <strong>objectCategory</strong> -Eigenschaft der neuen Instanz auf den Wert fest, der in der <strong>defaultobjectcategory</strong> -Eigenschaft der Objektklasse angegeben ist. Die <strong>objectCategory</strong> -Eigenschaft ist eine indizierte Eigenschaft, die verwendet wird, um die Effizienz von Objektklassen suchen zu erhöhen. Wenn <strong>defaultobjectcategory</strong> beim Erstellen einer Klasse nicht angegeben wird, legt das System es auf den Distinguished Name (DN) des <strong>classSchema</strong> -Objekts für diese Klasse fest. Wenn dieses Objekt häufig durch den Wert einer übergeordneten Klasse und nicht durch die Klasse des Objekts abgefragt wird, können Sie <strong>defaultobjectcategory</strong> auf den DN der übergeordneten Klasse festlegen. Wenn Sie z. b. eine vordefinierte Klasse (Category 1) Unterklassen, empfiehlt es sich, <strong>defaultobjectcategory</strong> auf denselben Wert wie die übergeordnete Klasse festzulegen. Dadurch kann die Standardbenutzer Oberfläche &quot; nach &quot; ihrer Unterklasse suchen.<br/> Weitere Informationen finden Sie unter <a href="object-class-and-object-category.md">Objektklasse und Objekt Kategorie</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>defaultHidingValue</strong></td>
<td>Ein boolescher Wert, der die Standardeinstellung der <strong>showInAdvancedViewOnly</strong> -Eigenschaft der neuen Instanzen dieser Klasse angibt. Viele Verzeichnisobjekte sind für Endbenutzer nicht interessant. Um zu verhindern, dass diese Objekte die Benutzeroberfläche gruppieren, verfügt jedes Objekt über ein boolesches Attribut namens <strong>showInAdvancedViewOnly</strong>. Wenn <strong>defaultHidingValue</strong> auf <strong>true</strong>festgelegt ist, werden neue Objektinstanzen in den administrativen Snap-Ins und in der Windows-Shell ausgeblendet. Ein Menü Element für die Objektklasse wird nicht im <strong>neuen</strong> Kontextmenü der administrativen Snap-Ins angezeigt, auch wenn die entsprechenden Eigenschaften des Erstellungs-Assistenten für das <strong>Display specifier</strong> -Objekt der Objektklasse festgelegt sind.<br/> Wenn <strong>defaultHidingValue</strong> auf <strong>false</strong>festgelegt ist, werden neue Instanzen des Objekts in den administrativen Snap-Ins und in der Windows-Shell angezeigt. Legen Sie diese Eigenschaft auf " <strong>false</strong> " fest, um Instanzen der Klasse in den administrativen Snap-Ins und der Shell anzuzeigen und einen Erstellungs-Assistenten und dessen Menü Element im Menü " <strong>neu</strong> " der administrativen Snap-Ins zu aktivieren.<br/> Wenn der <strong>defaultHidingValue</strong> -Wert nicht festgelegt ist, ist der Standardwert <strong>true</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>systemFlags</strong></td>
<td>Ein ganzzahliger Wert, der Flags enthält, die zusätzliche Eigenschaften der-Klasse definieren. Das 0x10-Bit identifiziert eine Klasse der Kategorie 1 (eine Klasse, die Teil des im System enthaltenen Basis Schemas ist). Dieses Bit kann nicht festgelegt werden, was bedeutet, dass das Bit nicht in Klassen der Kategorie 2 festgelegt ist (die Erweiterungen des Schemas sind).</td>
</tr>
<tr class="even">
<td><strong>systemOnly</strong></td>
<td>Ein boolescher Wert, der angibt, ob die Klasse nur vom Active Directory Server geändert werden kann. Reine System Klassen können nur vom Verzeichnis System-Agent (DSA) erstellt oder gelöscht werden. Systemeigene Klassen sind die Klassen, von denen das System für den normalen Betrieb abhängig ist.</td>
</tr>
<tr class="odd">
<td><strong>defaultSecurityDescriptor</strong></td>
<td>Gibt die Standard Sicherheits Beschreibung für neue Objekte dieser Klasse an. Weitere Informationen finden Sie unter <a href="default-security-descriptor.md">Standard Sicherheits Beschreibung</a> und <a href="how-security-descriptors-are-set-on-new-directory-objects.md">wie Sicherheits Deskriptoren für neue Verzeichnisobjekte festgelegt werden</a>.</td>
</tr>
<tr class="even">
<td><strong>isDefunct</strong></td>
<td>Ein boolescher Wert, der angibt, ob die Klasse veraltet ist. Weitere Informationen finden Sie unter <a href="disabling-existing-classes-and-attributes.md">Deaktivieren vorhandener Klassen und Attribute</a>.</td>
</tr>
<tr class="odd">
<td><strong>Beschreibung</strong></td>
<td>Eine Textbeschreibung der-Klasse, die von administrativen Anwendungen verwendet werden soll.</td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifiziert die Objektklasse, für die dieses-Objekt eine Instanz ist, die die <strong>Klassen Schema</strong> -Objektklasse für alle Klassendefinitionen und die <strong>attributeSchema</strong> -Objektklasse für alle Attribut Definitionen ist.</td>
</tr>
</tbody>
</table>



 

 

