---
description: Stellt Regeln zum Zuordnen von WMI-Klassen zu Active Directory zur
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Zuordnen von Active Directory-Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc38e91d52b59a206a0b64465d0f9710f6d515c9487853824477b7f4f6a126aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992900"
---
# <a name="mapping-active-directory-classes"></a>Zuordnen von Active Directory-Klassen

Da Active Directory über eine Vielzahl von möglichen Objekten verfügt, kann WMI keine direkte 1:1-Zuordnung erstellen. Stattdessen verwendet der Verzeichnisdiensteanbieter Regeln, um Klassen zwischen den beiden Technologien zu ordnen.

In diesem Thema werden die folgenden Abschnitte erläutert:

-   [Zuordnungsklassen](#mapping-classes)
-   [Zuordnungsattribute](#mapping-attributes)
-   [Zuordnungsklassen](#association-classes)

> [!Note]  
> Weitere Informationen zur Unterstützung und Installation dieser Komponente unter einem bestimmten Betriebssystem finden Sie unter [Betriebssystemverfügbarkeit von WMI-Komponenten.](operating-system-availability-of-wmi-components.md)

 

## <a name="mapping-classes"></a>Zuordnungsklassen

In der folgenden Liste werden die Richtlinien beschrieben, die der Verzeichnisdiensteanbieter zum Zuordnen von Active Directory-Klassen zu WMI-Klassen verwendet:

-   Jede abstrakte Klasse im Active Directory-Schema wird einer abstrakten Klasse im WMI-Schema entspricht.

    Im WMI-Schema wird jeder abstrakten Klasse DS \_ vorangestellt. Beispielsweise wird die **Person-Klasse** aus dem Active Directory-Schema der **WMI-Klasse der \_ DS-Person** angezeigt.

-   Jede nicht abstract-Klasse aus dem Active Directory-Schema wird den folgenden beiden Klassen im WMI-Schema zu ordnet:

    -   Der ersten zugeordneten Klasse wird ADS \_ vorangestellt. Hierbei handelt es sich um abstrakte Klassen, die gemäß den folgenden Regeln zugeordnet werden.
    -   Die zweite zugeordnete Klasse ist eine nicht abstract-Klasse mit dem \_ DS-Namenspräfix. Diese Klasse wird von der abstrakten \_ ADS-Klasse mit dem [**Anbieterqualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) abgeleitet.

    Beispielsweise wird die **Benutzerklasse** aus dem Active Directory-Schema zwei Klassen angezeigt. Die erste Klasse ist die **abstrakte \_ ADS-Benutzerklasse,** die gemäß den folgenden Regeln zugeordnet wird. Die zweite Klasse ist die nicht abstract-Klasse des **DS-Benutzers. \_** Sie wird vom **\_ ADS-Benutzer abgeleitet** und verfügt über den hinzugefügten Anbieterqualifizierer. [](/windows/desktop/api/Provider/nl-provider-provider)

-   Sofern nicht anders angegeben, ist der Name einer zugeordneten Klasse der verfappte Wert der **LDAP-Display-Name-Eigenschaft** in der Active Directory-Klasse.
-   Wenn die **Sub-Class-Of-Eigenschaft** in der Active Directory-Klasse vorhanden ist, wird die WMI-zugeordnete Klasse von der angegebenen Klasse abgeleitet.

    Wenn die **Sub-Class-Of-Eigenschaft** nicht vorhanden ist, wird die WMI-zugeordnete Klasse von der **DS \_ LDAP-Stammklassenklasse \_ \_** abgeleitet, wie in der MOF-Datei angegeben.

    > [!Note]  
    > Diese Klasse verfügt über die **ADSIPath-Schlüsseleigenschaft** mit dem **Typ VT \_ BSTR**. Dies ist der eindeutige ADSI-Pfad, der diese Instanz identifiziert. Active Directory unterstützt nur die einzelne Vererbung, sodass dies funktioniert.

     

-   Für **jede** Klasse wird ein dynamischer Qualifizierer vom Typ **VT \_ BOOL** erstellt, und die Variante wird `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` auf **TRUE** festgelegt. Dies ist ein WMI-Standardqualifizierer, der angibt, dass Instanzen dieser Klasse dynamisch bereitgestellt werden.
-   Wenn die Klasse nicht abstrakt [](/windows/desktop/api/Provider/nl-provider-provider) ist, erstellt der Anbieter einen Anbieterqualifizierer vom Typ **VT \_ BSTR BOOL,** und der Qualifizierertyp wird für jede Klasse auf `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` "DS-Instanzanbieter" festgelegt. Dies ist ein WMI-Standardqualifizierer, der den Namen des Anbieters angibt, der dynamisch Instanzen dieser Klasse angibt.

Die restlichen ADSI-Eigenschaften werden klassenqualifizierern und Eigenschaften wie in den folgenden Tabellen dargestellt. Alle Qualifizierer werden dem Qualifiziererflagwert () `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` zuordnen.

Im Folgenden werden Zuordnungsinformationen für die Active Directory-Klasse aufgeführt, die den WMI-Qualifizierer und den WMI-Qualifizierertyp für jede Active Directory-Eigenschaft anzeigen.

<dl> <dt>

**Common-Name**
</dt> <dd>

**CN** (**VT \_ BSTR**)

Wird direkt aus dem Zeichenfolgenwert zugeordnet.

</dd> <dt>

**Default-Object-Category**
</dt> <dd>

**DefaultObjectCategory** (**VT \_ BSTR**)

Wird direkt aus dem Zeichenfolgenwert zugeordnet.

</dd> <dt>

**Default-Security-Descriptor**
</dt> <dd>

**DefaultSecurityDescriptor** (**VT \_ BSTR**)

Wird direkt aus dem Zeichenfolgenwert zugeordnet.

</dd> <dt>

**Governs-Id**
</dt> <dd>

**GovernsId** (**VT \_ BSTR**)

Wird aus der Zeichenfolgendarstellung der OID zugeordnet. Beispiel: "{ 1 3 3 6 }".

</dd> <dt>

**Object-Class**
</dt> <dd>

Nicht zutreffend

Nicht zugeordnet.

</dd> <dt>

**Object-Class-Category**
</dt> <dd>

**ObjectClassCategory** (**VT \_ I4**)

Wird direkt aus dem ganzzahligen Wert zugeordnet. Wenn der Wert "Abstract(2)" ist, wird außerdem der STANDARDMÄßIGE CIM-Qualifizierer **\_ "VT BOOL"** erstellt, der **als "Abstract"-Qualifizierer** bezeichnet wird.

</dd> <dt>

**RDN-ATT-ID**
</dt> <dd>

**RDNATTID** (**VT \_ BSTR**)

Wird aus der Zeichenfolgendarstellung des OID-Werts zugeordnet. Beispiel: "{ 1 3 3 6 }". Darüber hinaus wird die hier identifizierte Eigenschaft mit dem standardmäßigen **indexierten** CIM-Qualifizierer kommentiert, der auf **TRUE festgelegt ist.**

</dd> <dt>

**Nur System**
</dt> <dd>

**SystemOnly** (**VT \_ BOOL**)

Wird direkt aus dem booleschen Wert zugeordnet.

</dd> </dl>

 

Im Folgenden werden die Eigenschaften der Active Directory-Klasse aufgeführt, die WMI-Klasseneigenschaften zugeordnet sind.

<dl> <dt>

**Kann enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.

</dd> <dt>

**Must-Contain**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Der **\_ CIM-Standardqualifizierer** Not Null wird für jede dieser Qualifizierer erstellt.

</dd> <dt>

**System kann enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Darüber hinaus wird jede Eigenschaft mit  einem Systemqualifizierer kommentiert, der auf **TRUE festgelegt ist.**

</dd> <dt>

**System muss enthalten**
</dt> <dd>

Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet. Der **\_ CIM-Standardqualifizierer** Not Null wird für jede dieser Qualifizierer erstellt. Darüber hinaus wird jede Eigenschaft mit  einem Systemqualifizierer kommentiert, der auf **TRUE festgelegt ist.**

</dd> </dl>

## <a name="mapping-attributes"></a>Zuordnungsattribute

Der Verzeichnisdiensteanbieter ordnet jedes Attribut einer Active Directory-Klasse genau einer Eigenschaft der entsprechenden WMI-Klasse gemäß den Regeln in diesem Abschnitt zu. Im Allgemeinen benennt der Verzeichnisdienstanbieter die WMI-Eigenschaft als die verfingte Version des **LDAP-Display-Name-Werts** des Active Directory-Attributs.

Wenn die Active **Directory-Eigenschaft Is-Single-Valued** **false** ist, wird diese WMI-Eigenschaft mit dem OR-Operator mit **CIM FLAG ARRAY \_ \_ kombiniert.** Beachten Sie, dass jede Eigenschaft mit dem **VT BSTR-Qualifizierer \_** **ADSyntax gekennzeichnet ist.** Sie stellt die zugrunde liegende Active Directory-Syntax dar.

In der folgenden Tabelle ist die Zuordnung der Active Directory-Syntax zum WMI-Eigenschaftsdatentyp aufgeführt.



| Active Directory-Element                                      | WMI-Datentyp                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [**Access-Point**](/windows/desktop/ADSchema/s-object-access-point)            | **\_CIM-ZEICHENFOLGE**                                                         |
| [**Boolean**](/windows/desktop/ADSchema/s-boolean)                             | **CIM \_ BOOLEAN**                                                        |
| **Zeichenfolge ohne Unterscheidung nach Groß-/Kleinschreibung**                                   | **\_CIM-ZEICHENFOLGE**                                                         |
| [**Zeichenfolge mit Zeichenfolge mit Sensitiver Schreibung**](/windows/desktop/ADSchema/s-string-case-sensitive) | **\_CIM-ZEICHENFOLGE**                                                         |
| [**Distinguished Name**](/windows/desktop/ADSchema/s-object-ds-dn)             | **\_CIM-ZEICHENFOLGE**                                                         |
| [**DN-Binary**](/windows/desktop/ADSchema/s-object-dn-binary)                  | Eingebettetes Objekt der **DN-Klasse \_ mit \_ unten definierter** Binärdatei.<br/> |
| [**DN-String**](/windows/desktop/ADSchema/s-object-dn-string)                  | Eingebettetes Objekt der **Klasse DN \_ mit unten \_ definierter** Zeichenfolge.<br/> |
| [**Enumeration**](/windows/desktop/ADSchema/s-enumeration)                     | **CIM \_ SINT32**                                                         |
| [**Enumeration**](/windows/desktop/ADSchema/s-enumeration)                     | **\_CIM-ZEICHENFOLGE**                                                         |
| [**Integer**](/windows/desktop/ADSchema/s-integer)                             | **CIM \_ SINT32**                                                         |
| [**LargeInteger**](/windows/desktop/ADSchema/s-largeinteger)                   | **\_CIM-ZEICHENFOLGE**                                                         |
| Sicherheitsbeschreibung                                           | Eingebettetes Objekt der **Klasse Uint8Array, unten** definiert.<br/>       |
| Numerische Zeichenfolge                                                | **\_CIM-ZEICHENFOLGE**                                                         |
| Objekt-ID                                                     | **\_CIM-ZEICHENFOLGE**                                                         |
| Oktettzeichenfolge                                                  | Eingebettetes Objekt der **Klasse Uint8Array, unten** definiert.<br/>       |
| OR-Name                                                       | **\_CIM-ZEICHENFOLGE**                                                         |
| Presentation-Address                                          | Eingebettetes Objekt der **Klasse Uint8Array, unten** definiert.<br/>       |
| Druckfallzeichenfolge                                             | **\_CIM-ZEICHENFOLGE**                                                         |
| Replikatlink                                                  | Eingebettetes Objekt der **Klasse Uint8Array, unten** definiert.<br/>       |
| [**String(Sid)**](/windows/desktop/ADSchema/s-string-sid)                      | Eingebettetes Objekt der **Klasse Uint8Array, unten** definiert.<br/>       |
| Time                                                          | **CIM \_ DATETIME**                                                       |
| UTC-Codierte Zeit                                                | **CIM \_ DATETIME**                                                       |
| Unicode-Zeichenfolge                                                | **\_CIM-ZEICHENFOLGE**                                                         |



 

Die Oktettzeichenfolgensyntax, die auf ein Array von **uint8-Werten** verweist, stellt bei der Zuordnung zu WMI ein Problem dar, da WMI Eigenschaften des Typs **uint8** und Arrays von **uint8** zulässt, während Active Directory Eigenschaften des Typs Oktettzeichenfolge sowie Arrays von Oktettzeichenfolgen zulässt.

Das folgende Beispiel zeigt die Directory Services Provider-Klasse, die zum Zuordnen eines Arrays von Octet String-Typeigenschaften verwendet wird.

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

WMI ordnet alle Active Directory-Eigenschaftswerte der Oktettzeichenfolge eingebetteten Instanzen von **Uint8Array zu.** Entsprechend ordnet WMI Arrays von Oktettzeichenfolgen Arrays von eingebetteten **Uint8Array-Objekten** zu.

Das folgende Beispiel zeigt die Klassen, die von WMI den DS-Eigenschaftswerten DN-Binary und DN-String zugeordnet werden.

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

In der folgenden Tabelle wird aufgeführt, wie WMI die restlichen Eigenschaften der Active Directory-Attributschnittstelle WMI-Eigenschaftenqualifizierern zuweist.



| Active Directory-Attributeigenschaftsname | WMI-Qualifizierer       | Datentyp    | Zuordnungsinformationen                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| **Attributsyntax**                     | **AttributeSyntax** | **VT \_ BSTR** | Wird aus der Zeichenfolgendarstellung der OID zugeordnet. |
| **Common-Name**                          | **CN**              | **VT \_ BSTR** | Wird aus dem Zeichenfolgenwert zugeordnet.                     |
| **Nur System**                          | **System**          | **VT \_ BOOL** | Wird aus dem booleschen Wert zugeordnet.                    |



 

> [!Note]  
> WMI ordnet alle Active Directory-Qualifizierer den `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` Qualifizierer-Varianten zu.

 

## <a name="association-classes"></a>Zuordnungsklassen

Der Verzeichnisdienst ist im Wesentlichen ein hierarchischer Objektspeicher. Die Objekte, die auf einer Nichtblattebene in der Hierarchie angezeigt werden können, werden als "Container" bezeichnet. Die Struktur dieser Hierarchie wird weiter durch die Eigenschaften "Poss-Superiors" und "System-Poss-Superiors" einer Klasse im Schema gesteuert. Diese geben zusammen den Satz von Klassen an, deren Instanzen in einer Instanz einer Containerklasse enthalten sein können.

Im folgenden Beispiel wird eine CIM-Zuordnung als Instanzen der statischen Zuordnungsklasse [**DS \_ LDAP Class \_ \_ Containment modelliert.**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)

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

Der Zuordnungsklassenanbieter unterstützt die [**Methoden GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) und [**CreateClassEnumAsync.**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync)

 

