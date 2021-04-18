---
title: 'Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien'
description: 'Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien'
ms.assetid: 295522c6-7c53-47f6-9b98-aeee2b0e34fc
keywords:
- Windows Color System (WCS), allgemeine Profiltypen
- WCS (Windows Color System), allgemeine Profiltypen
- Bild Farbverwaltung, allgemeine Profiltypen
- Farbverwaltung, allgemeine Profiltypen
- Farben, allgemeine Profiltypen
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Windows Color System (WCS), Versionierung
- WCS (Windows Color System), Versionsverwaltung
- Bild Farbverwaltung, Versionsverwaltung
- Farbverwaltung, Versionsverwaltung
- Farben, Versionsverwaltung
- Windows Color System (WCS), Lokalisierung
- WCS (Windows Color System), Lokalisierung
- Bild Farbverwaltung, Lokalisierung
- Farbverwaltung, Lokalisierung
- Farben, Lokalisierung
- Allgemeine WCS-Profiltypen
- Profil Consumer
- Allgemeine Profiltypen
- Schemas, allgemeine Profiltypen
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4814b652b654b6416b42a7a3484950273a93ea96
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106351864"
---
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a>Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien

-   [Allgemeine WCS-Profiltypen Schema v1](#wcs-common-profile-types-schema-v1)
-   [Allgemeine WCS-Profiltypen Schema v2-Ergänzungen](#wcs-common-profile-types-schema-v2-additions)
-   [WCS-Profil Schema-Versionsverwaltung](#wcs-profile-schema-versioning)
-   [Lokalisierung von WCS-Profilen](#wcs-profile-localization)
    -   [Ausdrücken Lokalisier barer Elemente](#expressing-localizable-elements)
    -   [Schema Unterstützung](#schema-support)
    -   [Auswählen der Sprache](#selecting-the-language)
    -   [Integrierte profile](#built-in-profiles)
-   [Zugehörige Themen](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a>Allgemeine WCS-Profiltypen Schema v1

Im folgenden finden Sie die v 1.0-Schema Definition für die allgemeinen WCS-Profiltypen.


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



Nur UTF-8-oder UTF-16-Codierungen werden unterstützt. Für alle anderen XML-Codierungen wird dringend abgeraten, um eine optimale Interoperabilität zu gewährleisten.

## <a name="wcs-common-profile-types-schema-v2-additions"></a>Allgemeine WCS-Profiltypen Schema v2-Ergänzungen

In Windows 7 wurde das Schema der allgemeinen WCS-Profiltypen so aktualisiert, dass es Typen zur Unterstützung des [WCS-Kalibrierungs Schemas](wcs-calibration-schema.md)enthält.


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



## <a name="wcs-profile-schema-versioning"></a>WCS-Profil Schema-Versionsverwaltung

In diesem Anhang bezieht sich der Begriff "profilconsumer" auf die WCS-Software oder auf eine Drittanbieter-Softwarekomponente, die WCS-Profile verwendet.

Neuere Versionen von Profil Verbrauchern können WCS-profile verarbeiten, die gemäß älteren Versionen der Schemas geschrieben wurden. Um die in der neuesten Version der Schemas definierten Features in vollem Umfang nutzen zu können, ist die neueste Version eines profilconsumers in der Regel erforderlich. Ältere Profil Consumer können jedoch Profile nutzen, die gemäß neueren Versionen der Schemas geschrieben wurden. Der profilconsumer kann XML-Elemente und-Attribute ignorieren, die er nicht versteht. Die Ergebnisse sind korrekt, aber die Leistung oder Genauigkeit kann im Vergleich zu den Ergebnissen, die mit der neuesten Version des profilconsumers erzielt werden, beeinträchtigt werden.

Im folgenden finden Sie Richtlinien für die Versionsverwaltung für profilconsumer:

-   Eine bestimmte Version eines profilconsumers muss entweder alle Elemente und Attribute aus einem versionsnamespace oder keines der Elemente erkennen.
-   Wenn ein profilconsumer ein Element oder Attribut aus einem Namespace erkennt, das nicht verstanden wird, muss dies als Fehlerbedingung behandelt werden, es sei denn, das Profil enthält eine explizite Anleitung zur Fall Back Verarbeitung.
-   Die [Open Packaging-Spezifikation](https://www.microsoft.com/whdc/xps/xpspkg.mspx) definiert einen zusätzlichen Namespace-URI, den Markup Kompatibilitäts Namespace, der Elemente und Attribute definiert, die diese Fall Back Verarbeitungsanleitung bereitstellen.
-   Alle-Versionen aller profilconsumer müssen alle Elemente und Attribute im Markup Compatibility-Namespace erkennen und berücksichtigen.
-   Profil Consumer, die auf einer neuen Version der Profil Schemas basieren, müssen alle zuvor definierten versionsnamespaces unterstützen.

In Version 1.0 erkennt WCS Elemente und Attribute aus den folgenden Namespaces:

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

Im folgenden wird ein Beispiel für die Markup Kompatibilität veranschaulicht.


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



## <a name="wcs-profile-localization"></a>Lokalisierung von WCS-Profilen

**Anforderungen**

WCS-Profile enthalten bestimmte Elemente wie "Profile Name" und "Description", die lesbaren Text enthalten. Dieser Text ist lokalisierbar.

Im folgenden finden Sie Richtlinien für die Versionsverwaltung für Profil Ersteller:

-   Für Profile, die von Drittanbietern, z. b. Druckerherstellern, erstellt wurden, sollte der Autor des Profils beschreibenden Text in mehrere Sprachen einschließen.
-   Die folgenden Elemente sollten lokalisierbar sein: 

    | Element     | CDMP | GMMP | Camping |
    |-------------|------|------|------|
    | ProfileName | x    | x    | x    |
    | BESCHREIBUNG | x    | x    | x    |
    | Autor      | x    | x    | x    |

    

     

### <a name="expressing-localizable-elements"></a>Ausdrücken Lokalisier barer Elemente

Anstatt direkt Text zu enthalten, enthält jedes lokalisierbare Element mindestens ein WCS: Text-Unterelement, von dem jedes das XML: lang-Attribut angeben muss. Wie im Abschnitt zur [XML-Spezifikation](http://www.w3.org/TR/REC-xml/) 2,12 ("sprach Identifikation") beschrieben, muss der Wert des Attributs "XML: lang" ein IETF RFC 3066-sprach Bezeichner wie "en-US", "en" oder "fr-FR" sein. In WCS-Schemas darf der Wert des XML: lang-Attributs nicht die leere Zeichenfolge "" sein, auch wenn XML dies im allgemeinen Fall zulässt. Beispiel:


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



Keine zwei WCs: Text Elemente können das gleiche XML: lang-Attribut aufweisen. Jedes WCS-Profil Schema muss diese Einschränkung für jedes lokalisierbare Element separat erzwingen. Nur UTF-8- und UTF-16-Codierungen werden unterstützt.

### <a name="schema-support"></a>Schema Unterstützung

Beim Entwurf werden die XSD-Typen WCS: LocalizedText und WCS: multilocalizedtype verwendet, die im allgemeinen WCS-Profiltyp Schema definiert sind:


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



Jedes WCS-Profil Schema deklariert jedes lokalisierbare Element vom Typ multilocalizedtype, z. b.:


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



Das CDMP-Schema erzwingt die Einschränkung, dass jedes WCS: Text-Element des CDM: Description-Elements über ein eindeutiges XML: lang-Attribut verfügen muss. Sie erzwingt die gleiche Einschränkung für die anderen lokalisierbaren Elemente. Das Camp und GMMP-Schemas sind identisch.

### <a name="selecting-the-language"></a>Auswählen der Sprache

Wenn Sie entscheiden, welche Sprachversion eines lokalisierbaren Elements angezeigt werden soll, muss der Anwendungscode die "nächstgelegene Version" der "aktuellen Sprache" auswählen. Was "nächstgelegene Version" und "aktuelle Sprache" bedeuten, ist plattformabhängig. siehe unten. Wenn das Profil keine Sprachversion enthält, die der aktuellen Sprache entspricht, sollte die Anwendung die erste Version im Profil auswählen (das erste untergeordnete WCS: Text-Element des lokalisierbaren Elements).

Unter Windows Vista erfolgt die Sprachauswahl wie folgt: jeder Thread verfügt über eine zugeordnete Liste von "bevorzugten Benutzeroberflächen Sprachen", die durch Aufrufen von " [**getthreadpreferreduilanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages)" abgerufen werden kann. Die Liste wird in der Reihenfolge der Benutzereinstellung zurückgegeben. Auf einem System, das für Englisch (USA) eingerichtet ist, lautet die von **getthreadpreferreduilanguages** zurückgegebene Liste beispielsweise {"en-US", "en"}. Dies bedeutet: 1) US-Englisch, falls vorhanden. 2) verwenden Sie andernfalls eine beliebige regionale Variante von Englisch, z. b. "en-GB" oder einfach "en".

Der UI-Code sucht für jede Sprache in dieser Liste in der Listen Reihenfolge nach einem WCS: Text-Element, dessen XML: lang-Attribut eine genaue Entsprechung ist. Die erste übereinstimmende Version wird verwendet. Wenn keine Version übereinstimmt, wird das erste WCS: Text-Element verwendet.

### <a name="built-in-profiles"></a>Integrierte profile

Die standardmäßigen WCS-Profile, die mit Windows Vista ausgeliefert werden, wie z. b. sRGB. CDMP, haben dieselben lokalisierbaren Eigenschaften wie andere Profile.

Die standardmäßige Windows-Lösung besteht darin, die lokalisierten Zeichen folgen in eine MUI-dll einzufügen und Sie wie folgt zu bezeichnen:


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



In einem Windows-System würde der Beschreibungstext aus der Ressourcen-ID 101 in der entsprechenden lokalisierten Version der MUI-Ressourcen für mscms.dll extrahiert werden. Nicht-Windows-Systeme verwenden die untergeordneten Elemente "WCS: Text", wie oben beschrieben.

Wir führen ein optionales, Global eindeutiges ID-Attribut für das Stamm Element jedes WCS-Profil Schemas ein. Das Standardprofil wcsrgb. CDMP könnte wie folgt aussehen:


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



Bei WCS-Farbprofilen, die mit Windows ausgeliefert werden, werden in der Farb-cpl beschreibende Informationen aus den Ressourcen anstelle von WCS: Text-Elementen in den Profilen angezeigt. Dadurch können Windows lokalisierte Informationen für diese Profile in allen unterstützten Sprachen anzeigen, ohne dass die Profile beschreibende Informationen in allen Sprachen enthalten müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 