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
# <a name="windows-color-system-common-profile-types-schema-versioning-and-localization-strategies"></a><span data-ttu-id="74100-127">Windows Color System: Schema gemeinsamer Profiltypen, Versionierung und Lokalisierungsstrategien</span><span class="sxs-lookup"><span data-stu-id="74100-127">Windows Color System Common Profile Types schema, Versioning and Localization Strategies</span></span>

-   [<span data-ttu-id="74100-128">Allgemeine WCS-Profiltypen Schema v1</span><span class="sxs-lookup"><span data-stu-id="74100-128">WCS Common Profile Types Schema V1</span></span>](#wcs-common-profile-types-schema-v1)
-   [<span data-ttu-id="74100-129">Allgemeine WCS-Profiltypen Schema v2-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="74100-129">WCS Common Profile Types Schema V2 Additions</span></span>](#wcs-common-profile-types-schema-v2-additions)
-   [<span data-ttu-id="74100-130">WCS-Profil Schema-Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="74100-130">WCS Profile Schema Versioning</span></span>](#wcs-profile-schema-versioning)
-   [<span data-ttu-id="74100-131">Lokalisierung von WCS-Profilen</span><span class="sxs-lookup"><span data-stu-id="74100-131">WCS Profile Localization</span></span>](#wcs-profile-localization)
    -   [<span data-ttu-id="74100-132">Ausdrücken Lokalisier barer Elemente</span><span class="sxs-lookup"><span data-stu-id="74100-132">Expressing localizable elements</span></span>](#expressing-localizable-elements)
    -   [<span data-ttu-id="74100-133">Schema Unterstützung</span><span class="sxs-lookup"><span data-stu-id="74100-133">Schema Support</span></span>](#schema-support)
    -   [<span data-ttu-id="74100-134">Auswählen der Sprache</span><span class="sxs-lookup"><span data-stu-id="74100-134">Selecting the Language</span></span>](#selecting-the-language)
    -   [<span data-ttu-id="74100-135">Integrierte profile</span><span class="sxs-lookup"><span data-stu-id="74100-135">Built-in profiles</span></span>](#built-in-profiles)
-   [<span data-ttu-id="74100-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74100-136">Related topics</span></span>](#related-topics)

## <a name="wcs-common-profile-types-schema-v1"></a><span data-ttu-id="74100-137">Allgemeine WCS-Profiltypen Schema v1</span><span class="sxs-lookup"><span data-stu-id="74100-137">WCS Common Profile Types Schema V1</span></span>

<span data-ttu-id="74100-138">Im folgenden finden Sie die v 1.0-Schema Definition für die allgemeinen WCS-Profiltypen.</span><span class="sxs-lookup"><span data-stu-id="74100-138">The following provides the v1.0 schema definition for the WCS Common Profile Types.</span></span>


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



<span data-ttu-id="74100-139">Nur UTF-8-oder UTF-16-Codierungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74100-139">Only UTF-8 or UTF-16 encodings are supported.</span></span> <span data-ttu-id="74100-140">Für alle anderen XML-Codierungen wird dringend abgeraten, um eine optimale Interoperabilität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="74100-140">All other XML encodings are strongly discouraged in order to preserve optimum interoperability.</span></span>

## <a name="wcs-common-profile-types-schema-v2-additions"></a><span data-ttu-id="74100-141">Allgemeine WCS-Profiltypen Schema v2-Ergänzungen</span><span class="sxs-lookup"><span data-stu-id="74100-141">WCS Common Profile Types Schema V2 Additions</span></span>

<span data-ttu-id="74100-142">In Windows 7 wurde das Schema der allgemeinen WCS-Profiltypen so aktualisiert, dass es Typen zur Unterstützung des [WCS-Kalibrierungs Schemas](wcs-calibration-schema.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="74100-142">In Windows 7, the WCS Common Profile Types schema has been updated to include types to support the [WCS Calibration schema](wcs-calibration-schema.md).</span></span>


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



## <a name="wcs-profile-schema-versioning"></a><span data-ttu-id="74100-143">WCS-Profil Schema-Versionsverwaltung</span><span class="sxs-lookup"><span data-stu-id="74100-143">WCS Profile Schema Versioning</span></span>

<span data-ttu-id="74100-144">In diesem Anhang bezieht sich der Begriff "profilconsumer" auf die WCS-Software oder auf eine Drittanbieter-Softwarekomponente, die WCS-Profile verwendet.</span><span class="sxs-lookup"><span data-stu-id="74100-144">In this Appendix, the term "profile consumer" refers to the WCS software, or to a third-party software component that consumes WCS profiles.</span></span>

<span data-ttu-id="74100-145">Neuere Versionen von Profil Verbrauchern können WCS-profile verarbeiten, die gemäß älteren Versionen der Schemas geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="74100-145">Newer versions of profile consumers will be able to consume WCS profiles written according to older versions of the schemas.</span></span> <span data-ttu-id="74100-146">Um die in der neuesten Version der Schemas definierten Features in vollem Umfang nutzen zu können, ist die neueste Version eines profilconsumers in der Regel erforderlich.</span><span class="sxs-lookup"><span data-stu-id="74100-146">To take full advantage of features defined in the newest version of the schemas, the newest version of a profile consumer will generally be required.</span></span> <span data-ttu-id="74100-147">Ältere Profil Consumer können jedoch Profile nutzen, die gemäß neueren Versionen der Schemas geschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="74100-147">However, older profile consumers can consume profiles written according to newer versions of the schemas.</span></span> <span data-ttu-id="74100-148">Der profilconsumer kann XML-Elemente und-Attribute ignorieren, die er nicht versteht.</span><span class="sxs-lookup"><span data-stu-id="74100-148">The profile consumer can ignore XML elements and attributes that it does not understand.</span></span> <span data-ttu-id="74100-149">Die Ergebnisse sind korrekt, aber die Leistung oder Genauigkeit kann im Vergleich zu den Ergebnissen, die mit der neuesten Version des profilconsumers erzielt werden, beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="74100-149">The results will be correct, but performance or fidelity may degraded as compared to the results achieved with the newest version of the profile consumer.</span></span>

<span data-ttu-id="74100-150">Im folgenden finden Sie Richtlinien für die Versionsverwaltung für profilconsumer:</span><span class="sxs-lookup"><span data-stu-id="74100-150">The following are versioning guidelines for profile consumers:</span></span>

-   <span data-ttu-id="74100-151">Eine bestimmte Version eines profilconsumers muss entweder alle Elemente und Attribute aus einem versionsnamespace oder keines der Elemente erkennen.</span><span class="sxs-lookup"><span data-stu-id="74100-151">A given version of a profile consumer must recognize either all of the elements and attributes from a version namespace, or none of them.</span></span>
-   <span data-ttu-id="74100-152">Wenn ein profilconsumer ein Element oder Attribut aus einem Namespace erkennt, das nicht verstanden wird, muss dies als Fehlerbedingung behandelt werden, es sei denn, das Profil enthält eine explizite Anleitung zur Fall Back Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="74100-152">If a profile consumer encounters an element or attribute from a namespace that it does not understand, it must treat this as an error condition, unless the profile contains explicit guidance on fallback processing.</span></span>
-   <span data-ttu-id="74100-153">Die [Open Packaging-Spezifikation](https://www.microsoft.com/whdc/xps/xpspkg.mspx) definiert einen zusätzlichen Namespace-URI, den Markup Kompatibilitäts Namespace, der Elemente und Attribute definiert, die diese Fall Back Verarbeitungsanleitung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="74100-153">The [Open Packaging Specification](https://www.microsoft.com/whdc/xps/xpspkg.mspx) defines an additional namespace URI, the markup compatibility namespace, which defines elements and attributes that provide this fallback processing guidance.</span></span>
-   <span data-ttu-id="74100-154">Alle-Versionen aller profilconsumer müssen alle Elemente und Attribute im Markup Compatibility-Namespace erkennen und berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="74100-154">All versions of all profile consumers must recognize and respect all the elements and attributes in the markup compatibility namespace.</span></span>
-   <span data-ttu-id="74100-155">Profil Consumer, die auf einer neuen Version der Profil Schemas basieren, müssen alle zuvor definierten versionsnamespaces unterstützen.</span><span class="sxs-lookup"><span data-stu-id="74100-155">Profile consumers based on a new version of the profile schemas must support all previously defined version namespaces.</span></span>

<span data-ttu-id="74100-156">In Version 1.0 erkennt WCS Elemente und Attribute aus den folgenden Namespaces:</span><span class="sxs-lookup"><span data-stu-id="74100-156">In the v1.0 release, WCS recognizes elements and attributes from the following namespaces:</span></span>

-   https://schemas.microsoft.com/windows/2005/02/color/ColorDeviceModel
-   https://schemas.microsoft.com/windows/2005/02/color/GamutMapModel
-   https://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel
-   https://schemas.microsoft.com/winfx/2005/06/markup-compatibility

<span data-ttu-id="74100-157">Im folgenden wird ein Beispiel für die Markup Kompatibilität veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="74100-157">The following demonstrates an example of markup compatibility.</span></span>


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



## <a name="wcs-profile-localization"></a><span data-ttu-id="74100-158">Lokalisierung von WCS-Profilen</span><span class="sxs-lookup"><span data-stu-id="74100-158">WCS Profile Localization</span></span>

<span data-ttu-id="74100-159">**Anforderungen**</span><span class="sxs-lookup"><span data-stu-id="74100-159">**Requirements**</span></span>

<span data-ttu-id="74100-160">WCS-Profile enthalten bestimmte Elemente wie "Profile Name" und "Description", die lesbaren Text enthalten.</span><span class="sxs-lookup"><span data-stu-id="74100-160">WCS profiles contain certain elements such as ProfileName and Description which contain human-readable text.</span></span> <span data-ttu-id="74100-161">Dieser Text ist lokalisierbar.</span><span class="sxs-lookup"><span data-stu-id="74100-161">This text is localizable.</span></span>

<span data-ttu-id="74100-162">Im folgenden finden Sie Richtlinien für die Versionsverwaltung für Profil Ersteller:</span><span class="sxs-lookup"><span data-stu-id="74100-162">The following are versioning guidelines for profile creators:</span></span>

-   <span data-ttu-id="74100-163">Für Profile, die von Drittanbietern, z. b. Druckerherstellern, erstellt wurden, sollte der Autor des Profils beschreibenden Text in mehrere Sprachen einschließen.</span><span class="sxs-lookup"><span data-stu-id="74100-163">For profiles created by 3rd parties such as printer manufacturers, the profile author should incorporate descriptive text in multiple languages.</span></span>
-   <span data-ttu-id="74100-164">Die folgenden Elemente sollten lokalisierbar sein:</span><span class="sxs-lookup"><span data-stu-id="74100-164">The following elements should be localizable:</span></span> 

    | <span data-ttu-id="74100-165">Element</span><span class="sxs-lookup"><span data-stu-id="74100-165">Element</span></span>     | <span data-ttu-id="74100-166">CDMP</span><span class="sxs-lookup"><span data-stu-id="74100-166">CDMP</span></span> | <span data-ttu-id="74100-167">GMMP</span><span class="sxs-lookup"><span data-stu-id="74100-167">GMMP</span></span> | <span data-ttu-id="74100-168">Camping</span><span class="sxs-lookup"><span data-stu-id="74100-168">CAMP</span></span> |
    |-------------|------|------|------|
    | <span data-ttu-id="74100-169">ProfileName</span><span class="sxs-lookup"><span data-stu-id="74100-169">ProfileName</span></span> | <span data-ttu-id="74100-170">x</span><span class="sxs-lookup"><span data-stu-id="74100-170">x</span></span>    | <span data-ttu-id="74100-171">x</span><span class="sxs-lookup"><span data-stu-id="74100-171">x</span></span>    | <span data-ttu-id="74100-172">x</span><span class="sxs-lookup"><span data-stu-id="74100-172">x</span></span>    |
    | <span data-ttu-id="74100-173">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="74100-173">Description</span></span> | <span data-ttu-id="74100-174">x</span><span class="sxs-lookup"><span data-stu-id="74100-174">x</span></span>    | <span data-ttu-id="74100-175">x</span><span class="sxs-lookup"><span data-stu-id="74100-175">x</span></span>    | <span data-ttu-id="74100-176">x</span><span class="sxs-lookup"><span data-stu-id="74100-176">x</span></span>    |
    | <span data-ttu-id="74100-177">Autor</span><span class="sxs-lookup"><span data-stu-id="74100-177">Author</span></span>      | <span data-ttu-id="74100-178">x</span><span class="sxs-lookup"><span data-stu-id="74100-178">x</span></span>    | <span data-ttu-id="74100-179">x</span><span class="sxs-lookup"><span data-stu-id="74100-179">x</span></span>    | <span data-ttu-id="74100-180">x</span><span class="sxs-lookup"><span data-stu-id="74100-180">x</span></span>    |

    

     

### <a name="expressing-localizable-elements"></a><span data-ttu-id="74100-181">Ausdrücken Lokalisier barer Elemente</span><span class="sxs-lookup"><span data-stu-id="74100-181">Expressing localizable elements</span></span>

<span data-ttu-id="74100-182">Anstatt direkt Text zu enthalten, enthält jedes lokalisierbare Element mindestens ein WCS: Text-Unterelement, von dem jedes das XML: lang-Attribut angeben muss.</span><span class="sxs-lookup"><span data-stu-id="74100-182">Instead of directly containing text, each localizable element contains one or more wcs:Text sub-elements, each of which must specify the xml:lang attribute.</span></span> <span data-ttu-id="74100-183">Wie im Abschnitt zur [XML-Spezifikation](http://www.w3.org/TR/REC-xml/) 2,12 ("sprach Identifikation") beschrieben, muss der Wert des Attributs "XML: lang" ein IETF RFC 3066-sprach Bezeichner wie "en-US", "en" oder "fr-FR" sein.</span><span class="sxs-lookup"><span data-stu-id="74100-183">As described in the [XML specification](http://www.w3.org/TR/REC-xml/) Section 2.12 ("Language Identification"), the value of the xml:lang attribute must be an IETF RFC 3066 language identifier such as "en-US", "en", or "fr-FR".</span></span> <span data-ttu-id="74100-184">In WCS-Schemas darf der Wert des XML: lang-Attributs nicht die leere Zeichenfolge "" sein, auch wenn XML dies im allgemeinen Fall zulässt.</span><span class="sxs-lookup"><span data-stu-id="74100-184">In WCS schemas, the value of the xml:lang attribute must not be the empty string "", even though XML allows this in the general case.</span></span> <span data-ttu-id="74100-185">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="74100-185">For example:</span></span>


```XML
<cdm:ColorDeviceModel ... />
    <cdm:Description>
        <wcs:Text xml:lang="en-US">Hello</wcs:Text>
        <wcs:Text xml:lang="fr-FR">Bonjour</wcs:Text>
    </cdm:Description>
    ...
</cdm:ColorDeviceeModel>
```



<span data-ttu-id="74100-186">Keine zwei WCs: Text Elemente können das gleiche XML: lang-Attribut aufweisen.</span><span class="sxs-lookup"><span data-stu-id="74100-186">No two wcs:Text elements can have the same xml:lang attribute.</span></span> <span data-ttu-id="74100-187">Jedes WCS-Profil Schema muss diese Einschränkung für jedes lokalisierbare Element separat erzwingen.</span><span class="sxs-lookup"><span data-stu-id="74100-187">Each WCS profile schema must enforce this constraint separately for each localizable element.</span></span> <span data-ttu-id="74100-188">Nur UTF-8- und UTF-16-Codierungen werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74100-188">Only UTF-8 and UTF-16 encodings are supported.</span></span>

### <a name="schema-support"></a><span data-ttu-id="74100-189">Schema Unterstützung</span><span class="sxs-lookup"><span data-stu-id="74100-189">Schema Support</span></span>

<span data-ttu-id="74100-190">Beim Entwurf werden die XSD-Typen WCS: LocalizedText und WCS: multilocalizedtype verwendet, die im allgemeinen WCS-Profiltyp Schema definiert sind:</span><span class="sxs-lookup"><span data-stu-id="74100-190">The design makes use of the XSD types wcs:LocalizedText and wcs:MultiLocalizedType defined in the WCS Common Profile Type schema:</span></span>


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



<span data-ttu-id="74100-191">Jedes WCS-Profil Schema deklariert jedes lokalisierbare Element vom Typ multilocalizedtype, z. b.:</span><span class="sxs-lookup"><span data-stu-id="74100-191">Each WCS profile schema declares each localizable element to be of type MultiLocalizedType, for example:</span></span>


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



<span data-ttu-id="74100-192">Das CDMP-Schema erzwingt die Einschränkung, dass jedes WCS: Text-Element des CDM: Description-Elements über ein eindeutiges XML: lang-Attribut verfügen muss.</span><span class="sxs-lookup"><span data-stu-id="74100-192">The CDMP schema enforces the constraint that each wcs:Text child of the cdm:Description element must have a unique xml:lang attribute.</span></span> <span data-ttu-id="74100-193">Sie erzwingt die gleiche Einschränkung für die anderen lokalisierbaren Elemente.</span><span class="sxs-lookup"><span data-stu-id="74100-193">It enforces the same constraint for the other localizable elements.</span></span> <span data-ttu-id="74100-194">Das Camp und GMMP-Schemas sind identisch.</span><span class="sxs-lookup"><span data-stu-id="74100-194">The CAMP and GMMP schemas do the same.</span></span>

### <a name="selecting-the-language"></a><span data-ttu-id="74100-195">Auswählen der Sprache</span><span class="sxs-lookup"><span data-stu-id="74100-195">Selecting the Language</span></span>

<span data-ttu-id="74100-196">Wenn Sie entscheiden, welche Sprachversion eines lokalisierbaren Elements angezeigt werden soll, muss der Anwendungscode die "nächstgelegene Version" der "aktuellen Sprache" auswählen.</span><span class="sxs-lookup"><span data-stu-id="74100-196">When deciding which language version of a localizable element to display, application code should select the "closest version" to the "current language".</span></span> <span data-ttu-id="74100-197">Was "nächstgelegene Version" und "aktuelle Sprache" bedeuten, ist plattformabhängig. siehe unten.</span><span class="sxs-lookup"><span data-stu-id="74100-197">What "closest version" and "current language" actually mean is platform-dependent; see below.</span></span> <span data-ttu-id="74100-198">Wenn das Profil keine Sprachversion enthält, die der aktuellen Sprache entspricht, sollte die Anwendung die erste Version im Profil auswählen (das erste untergeordnete WCS: Text-Element des lokalisierbaren Elements).</span><span class="sxs-lookup"><span data-stu-id="74100-198">If the profile does not contain a language version that matches the current language, the application should select the first version in the profile (the first wcs:Text child element of the localizable element).</span></span>

<span data-ttu-id="74100-199">Unter Windows Vista erfolgt die Sprachauswahl wie folgt: jeder Thread verfügt über eine zugeordnete Liste von "bevorzugten Benutzeroberflächen Sprachen", die durch Aufrufen von " [**getthreadpreferreduilanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages)" abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="74100-199">On Windows Vista, the language selection is done as follows: Each thread has an associated list of "preferred UI languages", which can be obtained by calling [**GetThreadPreferredUILanguages**](/windows/win32/api/winnls/nf-winnls-getthreadpreferreduilanguages).</span></span> <span data-ttu-id="74100-200">Die Liste wird in der Reihenfolge der Benutzereinstellung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="74100-200">The list is returned in order of user preference.</span></span> <span data-ttu-id="74100-201">Auf einem System, das für Englisch (USA) eingerichtet ist, lautet die von **getthreadpreferreduilanguages** zurückgegebene Liste beispielsweise {"en-US", "en"}.</span><span class="sxs-lookup"><span data-stu-id="74100-201">For instance, on a system set up for US English, the list returned by **GetThreadPreferredUILanguages** is { "en-US", "en" }.</span></span> <span data-ttu-id="74100-202">Dies bedeutet: 1) US-Englisch, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="74100-202">This means: 1) US English if present.</span></span> <span data-ttu-id="74100-203">2) verwenden Sie andernfalls eine beliebige regionale Variante von Englisch, z. b. "en-GB" oder einfach "en".</span><span class="sxs-lookup"><span data-stu-id="74100-203">2) Otherwise, use any regional variant of English, such as "en-GB" or just plain "en".</span></span>

<span data-ttu-id="74100-204">Der UI-Code sucht für jede Sprache in dieser Liste in der Listen Reihenfolge nach einem WCS: Text-Element, dessen XML: lang-Attribut eine genaue Entsprechung ist.</span><span class="sxs-lookup"><span data-stu-id="74100-204">For each language in that list, in list order, the UI code looks for a wcs:Text element whose xml:lang attribute is an exact match.</span></span> <span data-ttu-id="74100-205">Die erste übereinstimmende Version wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="74100-205">The first matching version is used.</span></span> <span data-ttu-id="74100-206">Wenn keine Version übereinstimmt, wird das erste WCS: Text-Element verwendet.</span><span class="sxs-lookup"><span data-stu-id="74100-206">If no version matches, the first wcs:Text element is used.</span></span>

### <a name="built-in-profiles"></a><span data-ttu-id="74100-207">Integrierte profile</span><span class="sxs-lookup"><span data-stu-id="74100-207">Built-in profiles</span></span>

<span data-ttu-id="74100-208">Die standardmäßigen WCS-Profile, die mit Windows Vista ausgeliefert werden, wie z. b. sRGB. CDMP, haben dieselben lokalisierbaren Eigenschaften wie andere Profile.</span><span class="sxs-lookup"><span data-stu-id="74100-208">The standard WCS profiles shipped with Windows Vista, such as sRGB.cdmp, have the same localizable properties as other profiles.</span></span>

<span data-ttu-id="74100-209">Die standardmäßige Windows-Lösung besteht darin, die lokalisierten Zeichen folgen in eine MUI-dll einzufügen und Sie wie folgt zu bezeichnen:</span><span class="sxs-lookup"><span data-stu-id="74100-209">The standard Windows solution would be to put the localized strings in a MUI DLL, and refer to them like this:</span></span>


```XML
<cdm:Description resourceId="mscms.dll,-101">
    <wcs:Text xml:lang="en-US">Hello, world!</wcs:Text>
<cdm:Description>
```



<span data-ttu-id="74100-210">In einem Windows-System würde der Beschreibungstext aus der Ressourcen-ID 101 in der entsprechenden lokalisierten Version der MUI-Ressourcen für mscms.dll extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="74100-210">On a Windows system, the description text would be extracted from resource ID 101 in the appropriate localized version of the MUI resources for mscms.dll.</span></span> <span data-ttu-id="74100-211">Nicht-Windows-Systeme verwenden die untergeordneten Elemente "WCS: Text", wie oben beschrieben.</span><span class="sxs-lookup"><span data-stu-id="74100-211">Non-Windows systems would use the wcs:Text sub-elements as described above.</span></span>

<span data-ttu-id="74100-212">Wir führen ein optionales, Global eindeutiges ID-Attribut für das Stamm Element jedes WCS-Profil Schemas ein.</span><span class="sxs-lookup"><span data-stu-id="74100-212">We introduce an optional, globally unique ID attribute on the root element of each WCS profile schema.</span></span> <span data-ttu-id="74100-213">Das Standardprofil wcsrgb. CDMP könnte wie folgt aussehen:</span><span class="sxs-lookup"><span data-stu-id="74100-213">The standard profile wcsRGB.cdmp might look like this:</span></span>


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



<span data-ttu-id="74100-214">Bei WCS-Farbprofilen, die mit Windows ausgeliefert werden, werden in der Farb-cpl beschreibende Informationen aus den Ressourcen anstelle von WCS: Text-Elementen in den Profilen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="74100-214">For the WCS color profiles shipped with windows, the Color CPL displays descriptive information from the resources, rather than from the wcs:Text elements in the profiles.</span></span> <span data-ttu-id="74100-215">Dadurch können Windows lokalisierte Informationen für diese Profile in allen unterstützten Sprachen anzeigen, ohne dass die Profile beschreibende Informationen in allen Sprachen enthalten müssen.</span><span class="sxs-lookup"><span data-stu-id="74100-215">This allows Windows to display localized information for these profiles in all supported languages, without requiring the profiles themlselves to contain descriptive information in all languages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="74100-216">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="74100-216">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74100-217">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="74100-217">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="74100-218">Windows Color System: Schemas und Algorithmen</span><span class="sxs-lookup"><span data-stu-id="74100-218">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 