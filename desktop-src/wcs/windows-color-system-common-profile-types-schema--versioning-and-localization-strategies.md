---
title: 'Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien'
description: 'Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien'
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Farbsystem (WCS), allgemeine Profiltypen
- WCS (Windows Color System), allgemeine Profiltypen
- Bildfarbverwaltung,allgemeine Profiltypen
- Farbverwaltung,allgemeine Profiltypen
- Farben,allgemeine Profiltypen
- Windows Farbsystem (WCS), Profile
- WCS (Windows Color System), Profiles
- Bildfarbverwaltung,Profile
- Farbverwaltung,Profile
- Farben,Profile
- Windows Farbsystem (WCS), Versionierung
- WCS (Windows Color System), Versionierung
- Bildfarbverwaltung, Versionsverwaltung
- Farbverwaltung, Versionsverwaltung
- Farben, Versionierung
- Windows Farbsystem (WCS), Lokalisierung
- WCS (Windows Color System), Lokalisierung
- Bildfarbverwaltung,Lokalisierung
- Farbverwaltung, Lokalisierung
- Farben,Lokalisierung
- Allgemeine WCS-Profiltypen
- Profilverbraucher
- Allgemeine Profiltypen
- Schemas,allgemeine Profiltypen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c9df44fa7095d8cbcd3df6de00c92ba2d4ab2ddb7ef7d3565a820e925265ea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119442290"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien

-   [WCS Common Profile Types Schema V1](#wcs-common-profile-types-schema-v1)
-   [WCS Common Profile Types Schema V2 Additions](#wcs-common-profile-types-schema-v2-additions)
-   [WCS-Profilschemaversionierung](#wcs-profile-schema-versioning)
-   [WCS-Profillokalisierung](#wcs-profile-localization)
    -   [Ausdrücken von lokalisierbaren Elementen](#expressing-localizable-elements)
    -   [Schemaunterstützung](#schema-support)
    -   [Auswählen der Sprache](#selecting-the-language)
    -   [Integrierte Profile](#built-in-profiles)
-   [Zugehörige Themen](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>WCS Common Profile Types Schema V1

Im Folgenden finden Sie die v1.0-Schemadefinition für die allgemeinen WCS-Profiltypen.


```XML
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:import namespace="http://www.w3.org/XML/1998/namespace" />

  <xs:annotation>
    <xs:documentation xml:lang="en">
      Common types used in WCS profile schemas.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:simpleType name="NonNegativeFloatType">
    <xs:restriction base="xs:float">
      <xs:minInclusive value="0"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="NonNegativeCIEXYZType">
    <xs:attribute name="X" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Y" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Z" type="wcs:NonNegativeFloatType" use="required"/>
  </xs:complexType>

  <xs:simpleType name="GUIDType">
    <xs:restriction base="xs:string">
      <xs:pattern value="\{[a-fA-F0-9]{8}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{4}-[a-fA-F0-9]{12}\}"/>
    </xs:restriction>
  </xs:simpleType>

  <xs:complexType name="LocalizedTextType">
    <xs:simpleContent>
      <xs:extension base="xs:string">
        <xs:attribute ref="xml:lang" use="required"/>
      </xs:extension>
    </xs:simpleContent>
  </xs:complexType>

  <xs:complexType name="MultiLocalizedTextType">
    <xs:sequence>
      <xs:element name="Text" type="wcs:LocalizedTextType" minOccurs="1" />
    </xs:sequence>
  </xs:complexType>

</xs:schema>

```



Es werden nur UTF-8- oder UTF-16-Codierungen unterstützt. Von allen anderen XML-Codierungen wird dringend abgeraten, um eine optimale Interoperabilität zu gewährleisten.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>WCS Common Profile Types Schema V2 Additions

In Windows 7 wurde das SCHEMA für allgemeine WCS-Profiltypen aktualisiert, um Typen zur Unterstützung des [WCS-Kalibrierungsschemas zu enthalten.](wcs-calibration-schema.md)


```XML
  <xs:complexType name="ParameterizedCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="GreenTRC" type="wcs:ParameterizedCurveType"/>
      <xs:element name="BlueTRC" type="wcs:ParameterizedCurveType"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="ParameterizedCurveType">
    <xs:attribute name="Gamma" type="wcs:NonNegativeFloatType" use="required"/>
    <xs:attribute name="Offset1" type="xs:float" use="optional"/>
    <xs:attribute name="Gain" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset2" type="xs:float " use="optional"/>
    <xs:attribute name="TransitionPoint" type="wcs:NonNegativeFloatType" use="optional"/>
    <xs:attribute name="Offset3" type="xs:float" use="optional"/>
  </xs:complexType>

  <xs:simpleType name="FloatList">
    <xs:list itemType="xs:float"/>
  </xs:simpleType>

  <xs:complexType name="OneDimensionLutType">
    <xs:sequence>
      <xs:element name="Input" type="wcs:FloatList"/>
      <xs:element name="Output" type="wcs:FloatList"/>
    </xs:sequence>
  </xs:complexType>

  <xs:complexType name="HDRToneResponseCurvesType">
    <xs:sequence>
      <xs:element name="RedTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="GreenTRC" type="wcs:OneDimensionLutType"/>
      <xs:element name="BlueTRC" type="wcs:OneDimensionLutType"/>
    </xs:sequence>
    <xs:attribute name="TRCLength" use="required">
      <xs:simpleType>
        <xs:restriction base="xs:int">
          <xs:minInclusive value="2" />
        </xs:restriction>
      </xs:simpleType>
    </xs:attribute>
  </xs:complexType>
```



## <a name="wcs-profile-schema-versioning"></a>WCS-Profilschemaversionierung

In diesem Anhang bezieht sich der Begriff "Profilverbraucher" auf die WCS-Software oder auf eine Drittanbietersoftwarekomponente, die WCS-Profile verwendet.

Neuere Versionen von Profilverbrauchern können WCS-Profile nutzen, die gemäß älteren Versionen der Schemas geschrieben wurden. Um die in der neuesten Version der Schemas definierten Features voll zu nutzen, ist in der Regel die neueste Version eines Profilverbraucher erforderlich. Ältere Profilverbraucher können jedoch Profile nutzen, die gemäß neueren Versionen der Schemas geschrieben wurden. Der Profil-Consumer kann XML-Elemente und -Attribute ignorieren, die er nicht versteht. Die Ergebnisse sind korrekt, aber die Leistung oder Genauigkeit kann sich im Vergleich zu den Ergebnissen, die mit der neuesten Version des Profilverbraucher erzielt werden, beeinträchtigen.

Im Folgenden finden Sie Versionsrichtlinien für Profilverbraucher:

-   Eine bestimmte Version eines Profilverbraucher muss entweder alle Elemente und Attribute aus einem Versionsnamespace oder keines von ihnen erkennen.
-   Wenn ein Profil-Consumer auf ein Element oder Attribut aus einem Namespace trifft, das er nicht versteht, muss er dies als Fehlerbedingung behandeln, es sei denn, das Profil enthält explizite Anweisungen zur Fallbackverarbeitung.
-   Die [Open Packaging Specification definiert](https://www.microsoft.com/whdc/xps/xpspkg.mspx) einen zusätzlichen Namespace-URI, den Markupkompatibilitätsnamespace, der Elemente und Attribute definiert, die diese Anleitung zur Fallbackverarbeitung bereitstellen.
-   Alle Versionen aller Profilverbraucher müssen alle Elemente und Attribute im Markupkompatibilitätsnamespace erkennen und achten.
-   Profilverbraucher, die auf einer neuen Version der Profilschemas basieren, müssen alle zuvor definierten Versionsnamespaces unterstützen.

In Version 1.0 erkennt WCS Elemente und Attribute aus den folgenden Namespaces:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

Im Folgenden wird ein Beispiel für Markupkompatibilität veranschaulicht.


```XML
<?xml version="1.0" encoding="utf-8" ?>
<ColorAppearanceModel
  xmlns=http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
  xmlns:cam2=http://schemas.microsoft.com/windows/2007/08/color/ColorAppearanceModel
  xmlns:mc=http://schemas.microsoft.com/winfx/2005/02/markup-compatibility
  xs:schemaLocation="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel ColorAppearanceModel.xsd"
  xmlns:xs='http://www.w3.org/2001/XMLSchema-instance'
  mc:Ignorable="cam2">

  <ProfileName>Default profile for ICC viewing conditions</ProfileName>
  <mc:AlternateContent>
    <mc:Choice Requires="cam2">
      <cam2:AudioDescription source="ProfileExplanation.wav"/>
    </mc:Choice>
    <mc:Fallback>
      <Description>Appropriate for a print in a D50 viewing booth</Description>
        </mc:Fallback>
  </mc:AlternateContent>
  <Author>Microsoft</Author>

  <ViewingConditions>
    <WhitePointName>D50</WhitePointName>
    <Background X="19.3" Y="20.0" Z="16.5" />
    <Surround>Average</Surround>
    <LuminanceOfAdaptingField>31.8</LuminanceOfAdaptingField>
    <DegreeOfAdaptation>-1</DegreeOfAdaptation>
    <cam2:Humidity>30%</cam2:Humidity>
  </ViewingConditions>

</ColorAppearanceModel>
```



## <a name="wcs-profile-localization"></a>WCS-Profillokalisierung

**Requirements**

WCS-Profile enthalten bestimmte Elemente wie ProfileName und Description, die lesbaren Text enthalten. Dieser Text kann lokalisierbar sein.

Im Folgenden finden Sie Versionsrichtlinien für Profilersteller:

-   Für Profile, die von Dritten wie Druckerherstellern erstellt wurden, sollte der Autor des Profils beschreibenden Text in mehreren Sprachen enthalten.
-   Die folgenden Elemente sollten lokalisierbar sein: 

    | Element     | CDMP | GMMP | Camp |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | Beschreibung | x    | x    | x    |
    | Autor      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Ausdrücken von lokalisierbaren Elementen

Anstatt Text direkt zu enthalten, enthält jedes lokalisierbare Element mindestens ein wcs:Text-Unterelement, von denen jedes das xml:lang-Attribut angeben muss. Wie im [](http://www.w3.org/TR/REC-xml/) XML-Spezifikationsabschnitt 2.12 ("Sprachidentifikation") beschrieben, muss der Wert des xml:lang-Attributs ein IETF RFC 3066-Sprachbezeichner wie "en-US", "en" oder "fr-FR" sein. In WCS-Schemas darf der Wert des xml:lang-Attributs nicht die leere Zeichenfolge "" sein, obwohl XML dies im allgemeinen Fall zulässt. Beispiel:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Zwei wcs:Text-Elemente können nicht das gleiche xml:lang-Attribut haben. Jedes WCS-Profilschema muss diese Einschränkung für jedes lokalisierbare Element separat erzwingen. Nur UTF-8- und UTF-16-Codierungen werden unterstützt.

### <a name="schema-support"></a>Schemaunterstützung

Der Entwurf verwendet die XSD-Typen wcs:LocalizedText und wcs:MultiLocalizedType, die im WCS Common Profile Type-Schema definiert sind:


```XML
    <xs:complexType name="LocalizedText">
        <xs:simpleContent>
            <xs:extension base="xs:string">
                <xs:attribute name="xml:lang" type="xs:string" use="required"/>
            <xs:extension/>
        <xs:simpleContent/>
    </xs:complexType/>

    <xs:complexType name="MultiLocalizedType">
        <xs:element name="Text" type="cam:LocalizedText" minOccurs="1"/>
    </xs:complexType>
```



Jedes WCS-Profilschema deklariert jedes lokalisierbare Element als MultiLocalizedType-Typ, z. B.:


```XML
<xs:schema 
    xmlns:xs="http://www.w3.org/2001/XMLSchema"
    xmlns:cdm="http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
    targetNamespace=
        "http://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel"
    version="1.0">
    <xs:import namespace=
        "http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"/>

    <xs:element name="cdm:Description" type="wcs:MultiLocalizableType" minOccurs="0"/>

    <xs:unique name="uniqueDescriptionLanguage">
      <xs:selector xpath="cdm:ColorDeviceModel/cdm:Description/wcs:Text"/>
      <xs:field xpath="@xml:lang"/>
    </unique>

    ...
</xs:schema>
```



Das CDMP-Schema erzwingt die Einschränkung, dass jedes untergeordnete wcs:Text-Element des cdm:Description-Elements ein eindeutiges xml:lang-Attribut haben muss. Er erzwingt die gleiche Einschränkung für die anderen lokalisierbaren Elemente. Das gleiche gilt für die SCHEMAS FÜR DIE UND GMMP.

### <a name="selecting-the-language"></a>Auswählen der Sprache

Bei der Entscheidung, welche Sprachversion eines lokalisierbaren Elements angezeigt werden soll, sollte der Anwendungscode die "version" auswählen, die der "aktuellen Sprache" am nächsten ist. Was "nächste Version" und "aktuelle Sprache" tatsächlich bedeuten, ist plattformabhängig. siehe unten. Wenn das Profil keine Sprachversion enthält, die der aktuellen Sprache entspricht, sollte die Anwendung die erste Version im Profil auswählen (das erste untergeordnete wcs:Text-Element des lokalisierbaren Elements).

Unter Windows Vista erfolgt die Sprachauswahl wie folgt: Jedem Thread ist eine Liste mit "bevorzugten Benutzeroberflächensprachen" zugeordnet, die durch Aufrufen von [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages)ermittelt werden kann. Die Liste wird in der Reihenfolge der Benutzereinstellungen zurückgegeben. Auf einem Für US-Englisch eingerichteten System ist die von **GetThreadPreferredUILanguages** zurückgegebene Liste { "en-US", "en" } . Dies bedeutet: 1) US-Englisch, falls vorhanden. 2) Verwenden Sie andernfalls jede regionale Variante des Englischen, z. B. "en-GB" oder einfach "en".

Für jede Sprache in dieser Liste sucht der Benutzeroberflächencode in Listen reihenfolge nach einem wcs:Text-Element, dessen xml:lang-Attribut eine genaue Übereinstimmung ist. Die erste übereinstimmende Version wird verwendet. Wenn keine Version entspricht, wird das erste wcs:Text-Element verwendet.

### <a name="built-in-profiles"></a>Integrierte Profile

Die mit Windows Vista ausgelieferten STANDARD-WCS-Profile, z. B. sRGB.cdmp, verfügen über die gleichen lokalisierbaren Eigenschaften wie andere Profile.

Die standardmäßige Windows wäre, die lokalisierten Zeichenfolgen in eine DLL vom -Dll-Dateinamen (DLL) zu setzen und auf diese wie die folgenden zu verweisen:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



In einem Windows wird der Beschreibungstext aus der Ressourcen-ID 101 in der entsprechenden lokalisierten Version der RESOURCES-Ressourcen für mscms.dll. Nicht-Windows verwenden die wcs:Text-Unterelemente wie oben beschrieben.

Wir führen ein optionales, global eindeutiges ID-Attribut für das Stammelement jedes WCS-Profilschemas ein. Das Standardprofil wcsRGB.cdmp könnte wie hier aussehen:


```XML
<cdm:ColorDeviceModel
    ID=http://schemas.microsoft.com/2005/02/color/profiles/wcsRGB.cdmp
    ... >
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello.</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour.</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceModel>
```



Für die mit Fenstern ausgelieferten WCS-Farbprofile zeigt die Farb-CPL beschreibende Informationen aus den Ressourcen anstelle der wcs:Text-Elemente in den Profilen an. Dadurch können Windows lokalisierte Informationen für diese Profile in allen unterstützten Sprachen anzeigen, ohne dass die Profile themlselves beschreibende Informationen in allen Sprachen enthalten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 