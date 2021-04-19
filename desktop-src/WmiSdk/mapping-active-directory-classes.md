---
description: Stellt Regeln zum Mapping von WMI-Klassen Active Directory bereit.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Zuordnung von Active Directory Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358584"
---
# <a name="mapping-active-directory-classes"></a>Zuordnung von Active Directory Klassen

Da Active Directory über eine Vielzahl möglicher Objekte verfügt, kann WMI keine direkte eins-zu-Eins-Zuordnung erstellen. Stattdessen verwendet der Verzeichnisdienst Anbieter Regeln, um Klassen zwischen den beiden Technologien zuzuordnen.

Die folgenden Abschnitte werden in diesem Thema behandelt:

-   [Mapping-Klassen](#mapping-classes)
-   [Mapping-Attribute](#mapping-attributes)
-   [Zuordnungs Klassen](#association-classes)

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).

 

## <a name="mapping-classes"></a>Mapping-Klassen

In der folgenden Liste werden die Richtlinien beschrieben, die der Verzeichnisdienst Anbieter zum Zuordnen von Active Directory Klassen zu WMI-Klassen verwendet:

-   Jede abstrakte Klasse im Active Directory Schema wird einer abstrakten Klasse im WMI-Schema zugeordnet.

    Im WMI-Schema wird jeder abstrakten Klasse das Präfix DS vorangestellt \_ . Beispielsweise wird die **Person** -Klasse aus dem Active Directory-Schema der **DS- \_ Person** -WMI-Klasse zugeordnet.

-   Jede nicht abstrakte Klasse aus dem Active Directory-Schema wird den folgenden zwei Klassen im WMI-Schema zugeordnet:

    -   Der ersten zugeordneten Klasse wird das Präfix ADS vorangestellt \_ . Dabei handelt es sich um abstrakte Klassen, die gemäß den folgenden Regeln zugeordnet werden.
    -   Die zweite zugeordnete Klasse ist eine nicht abstrakte Klasse mit dem DS- \_ namens Präfix. Diese Klasse wird von der ADS \_ abstract-Klasse abgeleitet, wobei der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) hinzugefügt wird.

    Beispielsweise wird die **Benutzer** Klasse aus dem Active Directory-Schema zwei Klassen zugeordnet. Die erste Klasse ist die **\_ Benutzer** abstrakte Klasse ADS, die gemäß den Regeln unten zugeordnet ist. Die zweite Klasse ist die nicht abstrakte Klasse " **DS- \_ Benutzer** ". Sie wird von **ADS \_ User** abgeleitet und verfügt über den hinzugefügten [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) .

-   Sofern nicht anders angegeben, ist der Name einer zugeordneten Klasse der gehat Wert der **LDAP-Display-Name-** Eigenschaft in der Active Directory-Klasse.
-   Wenn die **Unterklasse-of-** Eigenschaft in der Active Directory-Klasse vorhanden ist, wird die WMI-zugeordnete Klasse von der angegebenen Klasse abgeleitet.

    Wenn die **Unterklasse-of-** Eigenschaft nicht vorhanden ist, wird die WMI-zugeordnete Klasse von der **DS \_ LDAP \_ \_** -Stamm klassenklasse abgeleitet, wie in der MOF-Datei angegeben.

    > [!Note]  
    > Diese Klasse verfügt über die **adsipath** -Schlüsseleigenschaft mit dem Typ **VT \_ BSTR**. Dies ist der eindeutige ADSI-Pfad, der diese Instanz identifiziert. Active Directory unterstützt nur die einfache Vererbung, sodass dies funktioniert.

     

-   Für jede Klasse wird ein **dynamischer** Qualifizierer vom Typ **VT \_ bool** und `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` für jede Klasse der Wert auf **true** festgelegt. Dies ist ein standardmäßiger WMI-Qualifizierer, der angibt, dass Instanzen dieser Klasse dynamisch bereitgestellt werden.
-   Wenn die Klasse nicht abstrakt ist, erstellt der Anbieter einen [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) vom Typ **VT \_ BSTR bool** und die qualifiziererkonfiguration `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` , die für jede Klasse auf "DS-Instanzanbieter" festgelegt ist. Dies ist ein standardmäßiger WMI-Qualifizierer, der den Namen des Anbieters angibt, der Instanzen dieser Klasse dynamisch bereitstellt.

Die restlichen ADSI-Eigenschaften werden den Klassen Qualifizierern und Eigenschaften gemäß den folgenden Tabellen zugeordnet. Alle Qualifizierer werden mit einem qualifiziererflagwert von zugeordnet `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .

Im folgenden werden die Mapping-Informationen für die Active Directory-Klasse aufgelistet, die den WMI-Qualifizierer und den WMI-qualifizierungstyp für jede Active Directory

<dl> <dt>

**Gemeinsamer Name**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Wird direkt aus dem Zeichen folgen Wert zugeordnet.

</dd> <dt>

**Default-Object-Category**
</dt> <dd>

**Defaultobjectcategory** (**VT \_ BSTR**)

Wird direkt aus dem Zeichen folgen Wert zugeordnet.

</dd> <dt>

**Standard-Security-Descriptor**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Wird direkt aus dem Zeichen folgen Wert zugeordnet.

</dd> <dt>

**Regelt-ID**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Wird von der Zeichen folgen Darstellung der OID zugeordnet. Beispiel: "{1 3 3 6}".

</dd> <dt>

**Object-Klasse**
</dt> <dd>

–

Nicht zugeordnet.

</dd> <dt>

**Object-Class-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Wird direkt aus dem ganzzahligen Wert zugeordnet. Wenn der Wert abstrakt (2) ist, wird außerdem der standardmäßige **VT \_ bool** CIM-Qualifizierer, der als **"abstract"** -Qualifizierer bezeichnet wird, ebenfalls erstellt.

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**rDNAttID** (**VT \_ BSTR**)

Wird von der Zeichen folgen Darstellung des OID-Werts zugeordnet. Beispiel: "{1 3 3 6}". Außerdem wird die hier identifizierte Eigenschaft mit dem standardmäßigen **indizierten** CIM-Qualifizierer kommentiert, der auf **true** festgelegt ist.

</dd> <dt>

**Nur System**
</dt> <dd>

**Systemonly** (**VT \_ bool**)

Wird direkt aus dem booleschen Wert zugeordnet.

</dd> </dl>

 

Im folgenden werden die Eigenschaften der Active Directory-Klasse aufgelistet, die WMI-Klasseneigenschaften zugeordnet sind.

<dl> <dt>

**Kann enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.

</dd> <dt>

**Muss enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Der standardmäßige **Not \_ null** -CIM-Qualifizierer wird für jeden dieser Werte erstellt.

</dd> <dt>

**System-kann enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Außerdem wird jede Eigenschaft mit einem **System** Qualifizierer versehen und auf " **true**" festgelegt.

</dd> <dt>

**System-muss enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Der standardmäßige **Not \_ null** -CIM-Qualifizierer wird für jeden dieser Werte erstellt. Außerdem wird jede Eigenschaft mit einem **System** Qualifizierer versehen und auf " **true**" festgelegt.

</dd> </dl>

## <a name="mapping-attributes"></a>Mapping-Attribute

Der Verzeichnisdienst Anbieter ordnet jedes Attribut einer Active Directory-Klasse gemäß den Regeln in diesem Abschnitt genau einer Eigenschaft der entsprechenden WMI-Klasse zu. Im allgemeinen benennt der Verzeichnis Dienstanbieter die WMI-Eigenschaft als die geschützte Version des **LDAP-Display-Name-** Werts des Active Directory Attributs.

Wenn die Active Directory **-** Eigenschaft den Wert " **false**" hat, wird diese WMI-Eigenschaft mit dem or-Operator mit dem CIM- **Flag- \_ \_ Array** kombiniert. Beachten Sie, dass jede Eigenschaft mit dem **VT \_ BSTR** -Qualifizierer " **adsyntax**" gekennzeichnet ist. Sie stellt die zugrunde liegende Active Directory-Syntax dar.

In der folgenden Tabelle wird die Zuordnung der Active Directory-Syntax zum WMI-Eigenschafts Datentyp aufgelistet.



| Active Directory-Element                                      | WMI-Datentyp                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Zugriffspunkt**](/windows/desktop/ADSchema/s-object-access-point)            | **CIM- \_ Zeichenfolge**                                                         |
| [**Booleschen**](/windows/desktop/ADSchema/s-boolean)                             | **CIM- \_ boolescher Wert**                                                        |
| **Groß-/Kleinschreibung**                                   | **CIM- \_ Zeichenfolge**                                                         |
| [**Groß-/Kleinschreibung**](/windows/desktop/ADSchema/s-string-case-sensitive) | **CIM- \_ Zeichenfolge**                                                         |
| [**Definierter Name**](/windows/desktop/ADSchema/s-object-ds-dn)             | **CIM- \_ Zeichenfolge**                                                         |
| [**DN-Binär**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Eingebettetes Objekt der Klasse **DN \_ mit \_ binärer Binärdatei** .<br/> |
| [**DN-Zeichenfolge**](/windows/desktop/ADSchema/s-object-dn-string)                  | Eingebettetes Objekt der Klasse **DN \_ mit \_ Zeichenfolge** , die unten definiert ist.<br/> |
| [**Enumeration**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ SINT32**                                                         |
| [**Enumeration**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM- \_ Zeichenfolge**                                                         |
| [**Zah**](/windows/desktop/ADSchema/s-integer)                             | **CIM \_ SINT32**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **CIM- \_ Zeichenfolge**                                                         |
| Sicherheitsbeschreibung                                           | Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.<br/>       |
| Numerische Zeichenfolge                                                | **CIM- \_ Zeichenfolge**                                                         |
| ObjectID                                                     | **CIM- \_ Zeichenfolge**                                                         |
| Oktett-Zeichenfolge                                                  | Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.<br/>       |
| Oder Name                                                       | **CIM- \_ Zeichenfolge**                                                         |
| Presentation-Address                                          | Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.<br/>       |
| Print Case-Zeichenfolge                                             | **CIM- \_ Zeichenfolge**                                                         |
| Replikat Link                                                  | Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.<br/>       |
| [**Zeichenfolge (SID)**](/windows/desktop/ADSchema/s-string-sid)                      | Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.<br/>       |
| Time                                                          | **CIM- \_ DateTime**                                                       |
| UTC-codierte Zeit                                                | **CIM- \_ DateTime**                                                       |
| Unicode-Zeichenfolge                                                | **CIM- \_ Zeichenfolge**                                                         |



 

Die Oktett-Zeichen folgen Syntax, die auf ein Array von **Uint8** -Werten verweist, stellt bei der Zuordnung zu WMI ein Problem dar, da WMI Eigenschaften von Typen **Uint8** und Arrays von **Uint8** zulässt, während Active Directory Eigenschaften vom Typ Oktett String sowie Arrays von Oktett-Zeichen folgen zulässt.

Das folgende Beispiel zeigt die Verzeichnisdienst Anbieter-Klasse, die verwendet wird, um ein Array von Eigenschaften des Oktett-Zeichen folgen Typs zuzuordnen.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI ordnet alle Oktett-Zeichen folgen Active Directory-Eigenschafts Werten eingebetteten Instanzen von **Uint8Array** zu. Ebenso ordnet WMI Arrays von Oktett-Zeichen folgen Arrays von eingebetteten **Uint8Array** -Objekten zu.

Das folgende Beispiel zeigt die Klassen, die von WMI zugeordnet werden, um die Eigenschaften Werte DN-Binary und DN-String DS zu.

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

In der folgenden Tabelle ist aufgelistet, wie WMI die restlichen Eigenschaften der Active Directory-Attribut Schnittstelle den WMI-Eigenschafts Qualifizierern zuordnet.



| Active Directory Attribut-Eigenschaftsname | WMI Qualifizierer       | Datentyp    | Mapping-Informationen                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Attribut Syntax**                     | **AttributeSyntax** | **VT \_ BSTR** | Wird von der Zeichen folgen Darstellung der OID zugeordnet. |
| **Gemeinsamer Name**                          | **2.300**              | **VT \_ BSTR** | Wird vom Zeichen folgen Wert zugeordnet.                     |
| **Nur System**                          | **System**          | **VT \_ bool** | Wird vom booleschen Wert zugeordnet.                    |



 

> [!Note]  
> WMI ordnet alle Active Directory Qualifizierer den `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifizierervarianten zu.

 

## <a name="association-classes"></a>Zuordnungs Klassen

Der Verzeichnisdienst ist im Grunde ein hierarchischer Speicher von Objekten. Die Objekte, die auf einer nicht Blatt Ebene in der Hierarchie vorkommen können, werden als "Container" bezeichnet. Die Struktur dieser Hierarchie wird weiter von den Eigenschaften "Poss-Vorgesetzten" und "System-Poss-Vorgesetzten" einer Klasse im Schema gesteuert. Diese geben die Klassen an, deren Instanzen in einer Instanz einer Container Klasse enthalten sein können.

Im folgenden Beispiel wird eine CIM-Zuordnung als Instanzen der statischen Association-Klasse [**DS \_ LDAP \_ Class \_ Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)modelliert.

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

Der Association-Klassen Anbieter unterstützt die Methoden " [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) " und " [**feateclassenenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ".

 

