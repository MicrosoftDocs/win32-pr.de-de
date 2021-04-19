---
title: 'WCS-Farbdarstellungsmodell: Profilschema und Algorithmus'
description: 'WCS-Farbdarstellungsmodell: Profilschema und Algorithmus'
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Windows Color System (WCS), Color Appearance Model Profile (Camp)
- WCS (Windows Color System), Color Appearance Model Profile (Camp)
- Bild Farbverwaltung, Farbdarstellung-Modell Profil (Camp)
- Farbverwaltung, Farbdarstellung-Modell Profil (Camp)
- Farben, Farbdarstellung-Modell Profil (Camp)
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Farbdarstellung-Modell Profil (Camp)
- Camp (Farbdarstellung-Modell Profil)
- Schemas, Color Appearance Model Profile (Camp)
- Algorithmen, Farbdarstellung-Modell Profil (Camp)
- Modell Profil für WCS-Farbdarstellung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a928aebcfe02f1db39de2452a0b49e5c888bccc
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "106354250"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a><span data-ttu-id="82a7c-118">WCS-Farbdarstellungsmodell: Profilschema und Algorithmus</span><span class="sxs-lookup"><span data-stu-id="82a7c-118">WCS Color Appearance Model Profile Schema and Algorithm</span></span>

[<span data-ttu-id="82a7c-119">Übersicht</span><span class="sxs-lookup"><span data-stu-id="82a7c-119">Overview</span></span>](#overview)

[<span data-ttu-id="82a7c-120">Architektur des Farbdarstellung-Modell Profils (Camp)</span><span class="sxs-lookup"><span data-stu-id="82a7c-120">Color Appearance Model Profile (CAMP) Architecture</span></span>](#color-appearance-model-profile-architecture)

[<span data-ttu-id="82a7c-121">Das Lager Schema</span><span class="sxs-lookup"><span data-stu-id="82a7c-121">The CAMP Schema</span></span>](#the-camp-schema)

[<span data-ttu-id="82a7c-122">Die Lager Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="82a7c-122">The CAMP Schema Elements</span></span>](#the-camp-schema-elements)

[<span data-ttu-id="82a7c-123">Der Camp-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="82a7c-123">The CAMP Algorithm</span></span>](#the-camp-algorithm)

### <a name="overview"></a><span data-ttu-id="82a7c-124">Übersicht</span><span class="sxs-lookup"><span data-stu-id="82a7c-124">Overview</span></span>

<span data-ttu-id="82a7c-125">Dieses Schema wird verwendet, um den Inhalt eines Farbdarstellung-Modell Profils (Camp) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="82a7c-125">This schema is used to specify the content of a color appearance model profile (CAMP).</span></span> <span data-ttu-id="82a7c-126">Die zugehörigen baselinealgorithmen werden in den folgenden Abschnitten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="82a7c-126">The associated baseline algorithms are described in the following sections.</span></span>

<span data-ttu-id="82a7c-127">Das Camp besteht aus XML-Tags, die parametrimetrische Werte für die Modell Variablen "CIECAM02 Baseline Color Appearance" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-127">The CAMP is composed of XML tags that provide parametric values to the CIECAM02 baseline color appearance model variables.</span></span> <span data-ttu-id="82a7c-128">Ausführliche Informationen zu den Bereichen für Parameter finden Sie in den grundlegenden Farbdarstellung und der CIECAM02-Empfehlung.</span><span class="sxs-lookup"><span data-stu-id="82a7c-128">Details on the ranges for parameters are provided in the baseline color appearance model specification and CIECAM02 recommendation.</span></span>

### <a name="color-appearance-model-profile-architecture"></a><span data-ttu-id="82a7c-129">Architektur des Farbdarstellung-Modell Profils</span><span class="sxs-lookup"><span data-stu-id="82a7c-129">Color Appearance Model Profile Architecture</span></span>

![Diagramm, das die von X M L-Tags erstellte Architektur des Lager Profils anzeigt.](images/camp-image002new.png)

### <a name="the-camp-schema"></a><span data-ttu-id="82a7c-131">Das Lager Schema</span><span class="sxs-lookup"><span data-stu-id="82a7c-131">The CAMP Schema</span></span>


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema
  xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Color Appearance Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:annotation>
    <xs:documentation>
      ColorAppearanceModel element contains viewing conditions
      parameters based on CIECAM02.
    </xs:documentation>
  </xs:annotation>
  <xs:element name="ColorAppearanceModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="ViewingConditions">
          <xs:complexType>
            <xs:sequence>
              <xs:choice>
                <xs:element name="WhitePoint" type="wcs:NonNegativeCIEXYZType"/>
                <xs:element name="WhitePointName">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="D50"/>
                      <xs:enumeration value="D65"/>
                      <xs:enumeration value="A"/>
                      <xs:enumeration value="F2"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="Background" type="wcs:NonNegativeCIEXYZType"/>
              <xs:choice>
                <xs:element name="ImpactOfSurround" type="xs:float"/>
                <xs:element name="Surround">
                  <xs:simpleType>
                    <xs:restriction base="xs:string">
                      <xs:enumeration value="Average"/>
                      <xs:enumeration value="Dim"/>
                      <xs:enumeration value="Dark"/>
                    </xs:restriction>
                  </xs:simpleType>
                </xs:element>
              </xs:choice>
              <xs:element name="LuminanceOfAdaptingField" type="xs:float"/>
              <xs:element name="DegreeOfAdaptation" type="xs:float"/>
            </xs:sequence>
          </xs:complexType>
        </xs:element>
        <xs:element name="NormalizeToMediaWhitePoint" minOccurs="0">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="True"/>
              <xs:enumeration value="False"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-camp-schema-elements"></a><span data-ttu-id="82a7c-132">Die Lager Schema Elemente</span><span class="sxs-lookup"><span data-stu-id="82a7c-132">The CAMP Schema Elements</span></span>

## <a name="colorappearancemodel"></a><span data-ttu-id="82a7c-133">Colorerscheinungs ancemodel</span><span class="sxs-lookup"><span data-stu-id="82a7c-133">ColorAppearanceModel</span></span>

<span data-ttu-id="82a7c-134">Dieses Element ist eine Sequenz von:</span><span class="sxs-lookup"><span data-stu-id="82a7c-134">This element is a sequence of:</span></span>

1.  <span data-ttu-id="82a7c-135">Profilnamen Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="82a7c-135">ProfileName string,</span></span>
2.  <span data-ttu-id="82a7c-136">optionale Beschreibungs Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="82a7c-136">optional Description string,</span></span>
3.  <span data-ttu-id="82a7c-137">optionale Autor Zeichenfolge,</span><span class="sxs-lookup"><span data-stu-id="82a7c-137">optional Author string,</span></span>
4.  <span data-ttu-id="82a7c-138">Viewingconditions-Element.</span><span class="sxs-lookup"><span data-stu-id="82a7c-138">ViewingConditions element.</span></span>

<span data-ttu-id="82a7c-139">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-139">**Validation conditions:** Each sub-element is validated by its own type.</span></span> <span data-ttu-id="82a7c-140">Zeichen folgen Längen sind auf 10.000 Zeichen beschränkt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-140">String lengths are limited to 10,000 characters.</span></span>

## <a name="namespace"></a><span data-ttu-id="82a7c-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="82a7c-141">Namespace</span></span>

<span data-ttu-id="82a7c-142">xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="82a7c-142">xmlns:cam="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

<span data-ttu-id="82a7c-143">targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "</span><span class="sxs-lookup"><span data-stu-id="82a7c-143">targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel"</span></span>

## <a name="version"></a><span data-ttu-id="82a7c-144">Version</span><span class="sxs-lookup"><span data-stu-id="82a7c-144">Version</span></span>

<span data-ttu-id="82a7c-145">Version &gt; 0,1 oder &lt; = "1,0" mit der ersten Version von Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="82a7c-145">Version &gt;0.1 or &lt;= "1.0" with the first release of Windows Vista.</span></span>

<span data-ttu-id="82a7c-146">Überprüfungs **Bedingungen:** Jeder Versions Wert &lt; = 2,0 ist ebenfalls gültig, um nicht unterbrechende Änderungen im Format zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-146">**Validation conditions:** Any version value &lt;=2.0 is also valid to support non-breaking changes to the format.</span></span>

## <a name="documentation"></a><span data-ttu-id="82a7c-147">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="82a7c-147">Documentation</span></span>

<span data-ttu-id="82a7c-148">Profil Schema für Farbdarstellung des Modells.</span><span class="sxs-lookup"><span data-stu-id="82a7c-148">Color Appearance Model Profile Schema.</span></span>

<span data-ttu-id="82a7c-149">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-149">Copyright (C) Microsoft.</span></span> <span data-ttu-id="82a7c-150">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-150">All rights reserved.</span></span>

<span data-ttu-id="82a7c-151">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-151">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="surroundtype"></a><span data-ttu-id="82a7c-152">Surroundtype</span><span class="sxs-lookup"><span data-stu-id="82a7c-152">SurroundType</span></span>

<span data-ttu-id="82a7c-153">Dieses Element ist entweder eine Enumeration von "Average", "Dim" oder "Dark" CIECAM02 Parametern oder die tatsächlichen quantitativen Parameter aus der CIECAM02-Empfehlung c, Auswirkung der umschließenden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-153">This element is a either an enumeration of "Average," "Dim," or "Dark" CIECAM02 parameters or the actual quantitative parameters from the CIECAM02 recommendation c, impact of the surround.</span></span>

<span data-ttu-id="82a7c-154">Überprüfungs **Bedingungen:** Der c-Parameter kann zwischen 0,525 und 0,69 liegen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-154">**Validation conditions:** The c parameter can range from 0.525 to 0.69.</span></span>

## <a name="viewingconditions"></a><span data-ttu-id="82a7c-155">Viewingconditions</span><span class="sxs-lookup"><span data-stu-id="82a7c-155">ViewingConditions</span></span>

<span data-ttu-id="82a7c-156">Dieses Element besteht aus den folgenden untergeordneten Elementen:</span><span class="sxs-lookup"><span data-stu-id="82a7c-156">This element consists of the following sub-elements:</span></span>



| <span data-ttu-id="82a7c-157">Element</span><span class="sxs-lookup"><span data-stu-id="82a7c-157">Element</span></span>                    | <span data-ttu-id="82a7c-158">type</span><span class="sxs-lookup"><span data-stu-id="82a7c-158">Type</span></span>           |
|----------------------------|----------------|
| <span data-ttu-id="82a7c-159">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="82a7c-159">WhitePoint</span></span>                 | <span data-ttu-id="82a7c-160">Whitepointtype</span><span class="sxs-lookup"><span data-stu-id="82a7c-160">WhitePointType</span></span> |
| <span data-ttu-id="82a7c-161">Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82a7c-161">Background</span></span>                 | <span data-ttu-id="82a7c-162">CIEXYZ</span><span class="sxs-lookup"><span data-stu-id="82a7c-162">CIEXYZ</span></span>         |
| <span data-ttu-id="82a7c-163">Kur</span><span class="sxs-lookup"><span data-stu-id="82a7c-163">Surround</span></span>                   | <span data-ttu-id="82a7c-164">Surroundtype</span><span class="sxs-lookup"><span data-stu-id="82a7c-164">SurroundType</span></span>   |
| <span data-ttu-id="82a7c-165">"Luminanceofadaptingfield"</span><span class="sxs-lookup"><span data-stu-id="82a7c-165">LuminanceOfAdaptingField</span></span>   | <span data-ttu-id="82a7c-166">float</span><span class="sxs-lookup"><span data-stu-id="82a7c-166">float</span></span>          |
| <span data-ttu-id="82a7c-167">Degreeof-Anpassung</span><span class="sxs-lookup"><span data-stu-id="82a7c-167">DegreeOfAdaptation</span></span>         | <span data-ttu-id="82a7c-168">float</span><span class="sxs-lookup"><span data-stu-id="82a7c-168">float</span></span>          |
| <span data-ttu-id="82a7c-169">Normalizetomediawhitepoint</span><span class="sxs-lookup"><span data-stu-id="82a7c-169">NormalizeToMediaWhitePoint</span></span> | <span data-ttu-id="82a7c-170">Boolean</span><span class="sxs-lookup"><span data-stu-id="82a7c-170">Boolean</span></span>        |



 

<span data-ttu-id="82a7c-171">Überprüfungs **Bedingungen:** CIEXYZ-unter Elemente werden von nonnegativexyztype überprüft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-171">**Validation conditions:** CIEXYZ sub-elements are validated by NonNegativeXYZType.</span></span> <span data-ttu-id="82a7c-172">Der Wert für "luminanceofadaptingfield" ist maximal 10.000 CD/m ^ 2.</span><span class="sxs-lookup"><span data-stu-id="82a7c-172">The LuminanceOfAdaptingField is a maximum of 10,000cd/m^2.</span></span> <span data-ttu-id="82a7c-173">Degreeofadaptions kann zwischen 0,0 und 1,0 liegen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-173">The DegreeOfAdaptation can range from 0.0 to 1.0.</span></span> <span data-ttu-id="82a7c-174">Der normalizetomediawhitepoint-Wert kann entweder "true" oder "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-174">The NormalizeToMediaWhitePoint value can be either "true" or "false."</span></span> <span data-ttu-id="82a7c-175">Wenn das Subelement normalizetomediawhitepoint nicht vorhanden ist, wird standardmäßig "true" verwendet.</span><span class="sxs-lookup"><span data-stu-id="82a7c-175">If the NormalizeToMediaWhitePoint sub-element is absent, it effectively defaults to "true."</span></span> <span data-ttu-id="82a7c-176">Weitere Informationen finden Sie im folgenden Abschnitt zu den lageralgorithmen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-176">See the following CAMP algorithm section.</span></span>

## <a name="whitepointtype"></a><span data-ttu-id="82a7c-177">Whitepointtype</span><span class="sxs-lookup"><span data-stu-id="82a7c-177">WhitePointType</span></span>

<span data-ttu-id="82a7c-178">Dieses Element ist entweder eine Enumeration des Cie Light-Quell Werts ("D50", "D65", "a", "F2") oder ein "CIEXYZ"-Unterelement.</span><span class="sxs-lookup"><span data-stu-id="82a7c-178">This element is a either an enumeration of CIE light source value ("D50," "D65," "A," or "F2") or a CIEXYZ sub-element.</span></span>

<span data-ttu-id="82a7c-179">Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-179">**Validation conditions:** Each sub-element is validated by its own type.</span></span>

## <a name="ciexyztype"></a><span data-ttu-id="82a7c-180">Ciexyztype</span><span class="sxs-lookup"><span data-stu-id="82a7c-180">CIEXYZType</span></span>

<span data-ttu-id="82a7c-181">Das ciexyztype-Element besteht aus drei nicht-negativefloattype-IEEE-Gleit Komma Elementen mit dem Namen "X", "Y" und "Z".</span><span class="sxs-lookup"><span data-stu-id="82a7c-181">The CIEXYZType element is composed of three NonNegativeFloatType single-precision IEEE floating-point elements, named "X," "Y," and "Z."</span></span> <span data-ttu-id="82a7c-182">Bei diesen Messungen kann es sich entweder um absolute (nicht relative) CIEXYZ 1931-reflektierte Werte oder absolute (nicht relative) CIEXYZ 1931 Direct-Werte (Transmissive) in den quadratischen Einheiten von Kerzen pro Meter handelt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-182">These measurements can be either absolute (not relative) CIEXYZ 1931 reflective values or absolute (not relative) CIEXYZ 1931 direct (transmissive) values in candelas per meter squared units.</span></span>

<span data-ttu-id="82a7c-183">Überprüfungs **Bedingungen:** Dies bedeutet, dass nur reale Werte gültig sind, und negative CIEXYZ-Mess Werte sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="82a7c-183">**Validation conditions:** This means that only real-world values are valid, and negative CIEXYZ measurement values are invalid.</span></span> <span data-ttu-id="82a7c-184">Da es sich hierbei um absolute Werte handelt, können Werte weit über 1,0 f hinaus reichen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-184">Since these are absolute values, values can range well beyond 1.0f.</span></span> <span data-ttu-id="82a7c-185">Ein angemessener Grenzwert für jeden X-, Y-oder Z-Wert wird willkürlich auf 10000.0 f festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-185">A reasonable limit for any X, Y, or Z value will be arbitrarily set to 10000.0f.</span></span>

 

### <a name="the-camp-algorithm"></a><span data-ttu-id="82a7c-186">Der Camp-Algorithmus</span><span class="sxs-lookup"><span data-stu-id="82a7c-186">The CAMP Algorithm</span></span>

<span data-ttu-id="82a7c-187">Das Farb Darstellungs Modell (Color Appearance Model, CAM) basiert auf den Modellen der Cie CIECAM02 Color-Darstellung.</span><span class="sxs-lookup"><span data-stu-id="82a7c-187">The color appearance model (CAM) is based on the CIE CIECAM02 color appearance model equations.</span></span>

<span data-ttu-id="82a7c-188">Diese Klasse implementiert die Farbdarstellung von Modellen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-188">This class implements the color appearance modeling.</span></span> <span data-ttu-id="82a7c-189">Beachten Sie, dass die WCS-CAM *nicht* mithilfe eines Plug-ins ersetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="82a7c-189">Note that the WCS CAM is *not* replaceable, for example, using a plug-in.</span></span> <span data-ttu-id="82a7c-190">Es ist ein Entwurfs Ziel, nur ein Farb Darstellungs Modell zu haben.</span><span class="sxs-lookup"><span data-stu-id="82a7c-190">It is a design goal to have only one color appearance model.</span></span> <span data-ttu-id="82a7c-191">Der Cam basiert auf CIECAM02-Empfehlungen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-191">The CAM is based on CIECAM02 recommendations.</span></span>

<span data-ttu-id="82a7c-192">CIECAM02 kann auf zwei Arten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-192">CIECAM02 can be used in two ways.</span></span> <span data-ttu-id="82a7c-193">In der Richtung "farbige Metrik-zu-Darstellung" wird eine Zuordnung zwischen dem Bereich "Cie XYZ" und dem Leerraum bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-193">In the colorimetric-to-appearance direction, it provides a mapping from CIE XYZ space to color appearance space.</span></span> <span data-ttu-id="82a7c-194">In der Richtung "Darstellung bis farbige Metrik" erfolgt die Zuordnung aus dem Farb Darstellungs Raum zurück zu XYZ-Leerraum.</span><span class="sxs-lookup"><span data-stu-id="82a7c-194">In the appearance-to-colorimetric direction, it maps from color appearance space back to XYZ space.</span></span> <span data-ttu-id="82a7c-195">Die Farbdarstellung korreliert Helligkeit, J, Chroma, C und Hue, h.</span><span class="sxs-lookup"><span data-stu-id="82a7c-195">The color appearance correlates lightness, J, chroma, C, and hue, h.</span></span> <span data-ttu-id="82a7c-196">Diese drei Werte bilden ein zylindrisches Koordinatensystem.</span><span class="sxs-lookup"><span data-stu-id="82a7c-196">These three values form a cylindrical coordinate system.</span></span> <span data-ttu-id="82a7c-197">Häufig ist es leichter, in einem rechteckigen Koordinatensystem zu arbeiten, also Compute a = c cos h und b = c Sin h, um CIECAM02 Jab zu geben.</span><span class="sxs-lookup"><span data-stu-id="82a7c-197">Frequently, it turns out to be more convenient to work in a rectangular coordinate system, so compute a = C cos h and b = C sin h, to give CIECAM02 Jab.</span></span>

<span data-ttu-id="82a7c-198">Sie können die Werte der Cam-Helligkeit größer als 100 verwenden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-198">You can use CAM lightness values greater than 100.</span></span> <span data-ttu-id="82a7c-199">Das Cie-Komitee, das CIECAM02 formuliert hat, entsprach nicht dem Verhalten der Helligkeit-Achse für Eingabewerte mit einer Leuchtkraft, die größer ist als der übergebene weiße Punkt; Das heißt, für Eingabe-y-Werte, die größer sind als der Wert des angenommenen y-Punkts.</span><span class="sxs-lookup"><span data-stu-id="82a7c-199">The CIE committee that formulated CIECAM02 did not address the behavior of the lightness axis for input values with a luminance greater than the adopted white point; that is, for input Y values greater than the adopted white point Y value.</span></span> <span data-ttu-id="82a7c-200">Das Experimentieren hat ergeben, dass sich die Leuchtkraft Gleichungen in CIECAM02 für solche Werte in angemessener Weise Verhalten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-200">Experimentation has shown that the luminance equations in CIECAM02 behave reasonably for such values.</span></span> <span data-ttu-id="82a7c-201">Die Helligkeit nimmt exponentiell zu und folgt dem gleichen Exponent (ungefähr 1/3).</span><span class="sxs-lookup"><span data-stu-id="82a7c-201">The lightness increases exponentially and follows the same exponent (roughly 1/3).</span></span>

<span data-ttu-id="82a7c-202">Manchmal möchten Benutzer die Art und Weise ändern, in der der Grad der Anpassung (D) berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="82a7c-202">Users sometimes want to change the way that the degree of adaptation (D) is calculated.</span></span> <span data-ttu-id="82a7c-203">Der WCS-Entwurf ermöglicht es Benutzern, diese Berechnung zu steuern, indem der Wert für degreeofadaption in den Parametern der Anzeige Bedingungen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="82a7c-203">The WCS design enables users to control this calculation by changing the degreeOfadaptation value in the viewing conditions parameters.</span></span>

<span data-ttu-id="82a7c-204">Um den von den Benutzern, die von den Ansprüchen im Zusammenwirken von Benutzern eine konsistente Übereinstimmung bieten, zu gewährleisten, 1,0 ist die degreeofadaption in den Standard Camps</span><span class="sxs-lookup"><span data-stu-id="82a7c-204">To provide a more consistent match to users' ICC-influenced expectations, the degreeOfAdaptation in the default CAMPS is 1.0.</span></span> <span data-ttu-id="82a7c-205">Dies führt zu besseren Ergebnissen in allen Fällen als bei mincd absolute, bei denen WCS die degreeofadaption (über degreeofadaption =-1) berechnen könnte.</span><span class="sxs-lookup"><span data-stu-id="82a7c-205">This produces better results in all cases other than MinCD Absolute, where one might want to let WCS compute the degreeOfAdaptation (via degreeOfAdaptation = -1).</span></span>

<span data-ttu-id="82a7c-206">Anstatt einen umschließenden Wert "Average", "Dim" und "Dark" zu verwenden, wird ein kontinuierlicher Umschließungs Wert bereitgestellt, der aus dem Wert c berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="82a7c-206">Instead of using a surround value of "Average," "Dim," and "Dark," a continuous surround value, computed from the value c, is provided.</span></span> <span data-ttu-id="82a7c-207">Der Wert von c muss ein float-Wert zwischen 0,525 und 0,69 sein.</span><span class="sxs-lookup"><span data-stu-id="82a7c-207">The value of c must be a float between 0.525 and 0.69.</span></span>

<span data-ttu-id="82a7c-208">Aus *c* können *NC* und *F* berechnet werden. dabei wird die schrittweise lineare interpolung zwischen den Werten verwendet, die bereits für "Average", "Dim" und "Dark" bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-208">From *c*, *Nc* and *F* can be computed, using piecewise linear interpolation between the values already provided for "Average," "Dim," and "Dark."</span></span> <span data-ttu-id="82a7c-209">Dies modelliert die Darstellung in Abbildung 1 von Cie 159:2004, der CIECAM02-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="82a7c-209">This models what is shown in Figure 1 of CIE 159:2004, the CIECAM02 specification.</span></span>



| <span data-ttu-id="82a7c-210">degreeof-Anpassung</span><span class="sxs-lookup"><span data-stu-id="82a7c-210">degreeOfAdaption</span></span>                     | <span data-ttu-id="82a7c-211">Verhalten</span><span class="sxs-lookup"><span data-stu-id="82a7c-211">Behavior</span></span>                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="82a7c-212">-1.0</span><span class="sxs-lookup"><span data-stu-id="82a7c-212">-1.0</span></span>                                 | ![Zeigt eine Formel für das Standardverhalten c I E c a M 02 an.](images/camp-image006.png)<span data-ttu-id="82a7c-214">Dies ist das Standardverhalten von CIECAM02.</span><span class="sxs-lookup"><span data-stu-id="82a7c-214">This is the default CIECAM02 behavior.</span></span><br/> |
| <span data-ttu-id="82a7c-215">0,0 &lt; = degreeof-Anpassung &lt; = 1,0</span><span class="sxs-lookup"><span data-stu-id="82a7c-215">0.0 &lt;= degreeOfAdaption &lt;= 1.0</span></span> | <span data-ttu-id="82a7c-216">*D* = degreeof-Anpassung (der vom Benutzer bereitgestellte Wert)</span><span class="sxs-lookup"><span data-stu-id="82a7c-216">*D* = degreeOfAdaptation (the value supplied by the user)</span></span>                      |



 

<span data-ttu-id="82a7c-217">Eine bestimmte Menge an Fehlerüberprüfung wurde auch der-Implementierung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-217">A certain amount of error checking has also been added to the implementation.</span></span> <span data-ttu-id="82a7c-218">Die folgenden Gleichung Zahlen werden in der Definition von Cie 159:2004 von CIECAM02 verwendet.</span><span class="sxs-lookup"><span data-stu-id="82a7c-218">The following equation numbers are those used in the CIE 159:2004 definition of CIECAM02.</span></span>

<span data-ttu-id="82a7c-219">**Farbige metricin-ancecolors**</span><span class="sxs-lookup"><span data-stu-id="82a7c-219">**ColorimetricToAppearanceColors**</span></span>

<span data-ttu-id="82a7c-220">Die Eingabewerte werden auf eine nicht zurechtheit geprüft: Wenn X oder Z &lt; 0,0 oder Y &lt; -1,0, ist das HRESULT E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="82a7c-220">The input values are checked for reasonableness: If X or Z &lt; 0.0, or if Y &lt; -1.0, then the HRESULT is E\_INVALIDARG.</span></span> <span data-ttu-id="82a7c-221">Wenn-1,0 &lt; = Y &lt; 0,0, werden J, C und h alle auf 0,0 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-221">If -1.0 &lt;= Y &lt; 0.0, then J, C, and h are all set to 0.0.</span></span>

<span data-ttu-id="82a7c-222">Es gibt bestimmte interne Bedingungen, die zu Fehlern führen können.</span><span class="sxs-lookup"><span data-stu-id="82a7c-222">There are certain internal conditions that can produce error results.</span></span> <span data-ttu-id="82a7c-223">Anstatt solche Ergebnisse zu erzeugen, werden die internen Ergebnisse abgeschnitten, um Werte im Gültigkeitsbereich zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-223">Instead of producing such results, the internal results are clipped to produce in-range values.</span></span> <span data-ttu-id="82a7c-224">Dies geschieht bei Spezifikationen von Farben, die dunkel und unverändersch sind: in Gleichung 7,23, wenn ein Wert von &lt; 0, a = 0.</span><span class="sxs-lookup"><span data-stu-id="82a7c-224">This happens for specifications of colors that would be dark and impossibly chromatic: In equation 7.23, if A &lt; 0, A = 0.</span></span> <span data-ttu-id="82a7c-225">In Gleichung 7,26, wenn t &lt; 0, t = 0.</span><span class="sxs-lookup"><span data-stu-id="82a7c-225">In equation 7.26, if t &lt; 0, t = 0.</span></span>

<span data-ttu-id="82a7c-226">**Anzeige von "Erscheinungsbild"**</span><span class="sxs-lookup"><span data-stu-id="82a7c-226">**AppearanceToColorimetricColors**</span></span>

<span data-ttu-id="82a7c-227">Die Eingabewerte werden auf eine nicht zurechtheit geprüft.</span><span class="sxs-lookup"><span data-stu-id="82a7c-227">The input values are checked for reasonableness.</span></span> <span data-ttu-id="82a7c-228">Bei c &lt; 0, c &gt; 300 oder J &gt; 500 ist das HRESULT E \_ invalidArg.</span><span class="sxs-lookup"><span data-stu-id="82a7c-228">If C &lt; 0 , C &gt; 300, or J &gt; 500, then the HRESULT is E\_INVALIDARG.</span></span>

<span data-ttu-id="82a7c-229">*R '<sub>a;</sub>*, *G '<sub>a;</sub>* und *B '<sub>a;</sub>*, (Gleichungen 8,19-8,21) werden auf den Bereich 399,9 zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-229">*R'<sub>a;</sub>*, *G'<sub>a;</sub>*, and *B'<sub>a;</sub>*, (equations 8.19 - 8.21) are clipped to the range   399.9 .</span></span>

<span data-ttu-id="82a7c-230">Für alle Farbdarstellung-Modell profile (CAMPs) prüft die WCS-Engine den angenommenen weißen Punkt.</span><span class="sxs-lookup"><span data-stu-id="82a7c-230">For all Color Appearance Model Profiles (CAMPs), the WCS engine will examine the adopted white point.</span></span> <span data-ttu-id="82a7c-231">Wenn y nicht 100,0 ist, wird der übergelagene weiße Punkt so skaliert, dass y gleich 100,0 ist.</span><span class="sxs-lookup"><span data-stu-id="82a7c-231">If Y is not 100.0, then the adopted white point will be scaled so that Y does equal 100.0.</span></span> <span data-ttu-id="82a7c-232">Die gleiche Skalierung wird auf den Hintergrund Wert angewendet.</span><span class="sxs-lookup"><span data-stu-id="82a7c-232">The same scaling will be applied to the background value.</span></span> <span data-ttu-id="82a7c-233">Der Skalierungsfaktor ist 100,0/adoptedwhitepoint. Y.</span><span class="sxs-lookup"><span data-stu-id="82a7c-233">The scaling factor is 100.0/adoptedWhitePoint.Y.</span></span> <span data-ttu-id="82a7c-234">Der Faktor für die Skalierung wird auf die einzelnen X-, Y-und Z-Dateien angewendet. Wenn das normalizetomediawhitepoint-Feld auf "true" festgelegt ist, oder wenn es nicht im Camp vorhanden ist, skaliert die Engine auch alle Eingabe Farben für Geräte Farben in devicetocolormetric, sodass der Y-Wert des Mediums mit dem Medien Medium 100,0 lautet.</span><span class="sxs-lookup"><span data-stu-id="82a7c-234">The same scaling factor is applied to each of X, Y, and Z. If the NormalizeToMediaWhitePoint field is set to "True," or if it is absent from the CAMP, the engine also scales all device colors input to DeviceToColorimetric so that the Y value of the device media white point equals 100.0.</span></span> <span data-ttu-id="82a7c-235">Geräte Farben von colormetrictodevice werden durch die multiplikative Umkehrung dieses Skalierungsfaktors skaliert.</span><span class="sxs-lookup"><span data-stu-id="82a7c-235">Device colors coming from ColorimetricToDevice will be scaled by the multiplicative inverse of that scaling factor.</span></span> <span data-ttu-id="82a7c-236">Wenn das normalizetomediawhitepoint-Flag auf "false" festgelegt ist, werden die farbige Metrikdaten nicht skaliert.</span><span class="sxs-lookup"><span data-stu-id="82a7c-236">If the NormalizeToMediaWhitePoint flag is set to "False," then the colorimetric data is not scaled.</span></span>

<span data-ttu-id="82a7c-237">Bei einigen Aufgaben ist es sinnvoll, die farbmetrikwerte aus devicedecolormetric zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="82a7c-237">For some tasks, it makes sense to scale the colorimetric values coming from DeviceToColorimetric.</span></span> <span data-ttu-id="82a7c-238">Die hyperbolische Glanz Gleichungen in der CAM sind tatsächlich für eine weiße Punktbeleuchtung von 100,0 konzipiert.</span><span class="sxs-lookup"><span data-stu-id="82a7c-238">The hyperbolic lightness equations in the CAM are really designed for a white point luminance of 100.0.</span></span> <span data-ttu-id="82a7c-239">Die einzige Stelle, an der ein Unterschied in der absoluten Leuchtkraft (bzw. Beleuchtung) wiedergegeben wird, ist die Helligkeit des Anpassungs Felds.</span><span class="sxs-lookup"><span data-stu-id="82a7c-239">The only place where a difference in the absolute luminance (or illuminance) comes into play is in the luminance of the adapting field.</span></span> <span data-ttu-id="82a7c-240">Daher muss der Cam mit einem weißen Punkt Y von 100,0 initialisiert werden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-240">So the CAM must be initialized with a white point Y of 100.0.</span></span> <span data-ttu-id="82a7c-241">Wenn jedoch der mittlere weiße Punkt des Geräte Modells als gehostdeter weißer Punkt verwendet wird, müssen alle vom Gerät ausgehenden Farben entsprechend skaliert werden, oder das Gerät weiß nicht mit dem J-Wert 100,0.</span><span class="sxs-lookup"><span data-stu-id="82a7c-241">But if the device model's medium white point is being used as the adopted white point, then all colors coming from the device must be scaled accordingly, or device white will not come out with a J value of 100.0.</span></span> <span data-ttu-id="82a7c-242">Daher müssen die Y-Werte in den Messungen skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-242">So the Y values have to be scaled in the measurements.</span></span> <span data-ttu-id="82a7c-243">Die Maßwerte können vor dem Initialisieren des Geräte Modells skaliert werden.</span><span class="sxs-lookup"><span data-stu-id="82a7c-243">The measurement values could be scaled before initializing the device model.</span></span> <span data-ttu-id="82a7c-244">Die Ergebnisse befinden sich bereits im richtigen Bereich.</span><span class="sxs-lookup"><span data-stu-id="82a7c-244">Then results would already be in the proper range.</span></span> <span data-ttu-id="82a7c-245">Dies würde jedoch das Testen des Geräte Modells erschweren, da die ausgehenden Werte skaliert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-245">But that would make testing the device model more difficult, because the values coming out would require scaling.</span></span> <span data-ttu-id="82a7c-246">Bei Aufgaben, bei denen der Mittelpunkt des Mediums weiß, dass es sich um ein echtes weiß handelt, ist das normalisieren durch den Geräte Medien-weißen Punkt wünschenswert.</span><span class="sxs-lookup"><span data-stu-id="82a7c-246">For tasks in which the device medium white point is perceived to be a true white, normalizing by the device media white point is desirable.</span></span>

<span data-ttu-id="82a7c-247">Der Cam wird direkt aus dem Camp initialisiert.</span><span class="sxs-lookup"><span data-stu-id="82a7c-247">The CAM is initialized directly from the CAMP.</span></span> <span data-ttu-id="82a7c-248">Dies ermöglicht Entwicklern eine gewisse Flexibilität bei der Initialisierung der Cam, basierend auf der Aufgabe, die Sie ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-248">This allows developers some flexibility in initializing the CAM, based upon the task they want to perform.</span></span> <span data-ttu-id="82a7c-249">In einigen Aufgaben ignorieren Beobachter alle Chroma in den Medien weißen Punkten, da Sie erkennen, dass die Quell-und Zielmedien "weiß" sind.</span><span class="sxs-lookup"><span data-stu-id="82a7c-249">In some tasks, observers will ignore any chroma in the media white points, because they cognitively "know" that the source and destination media are "white."</span></span> <span data-ttu-id="82a7c-250">In solchen Fällen möchten Entwickler die Forward-und inverse-Cams mit ihren jeweiligen Medien weißen Punkten initialisieren.</span><span class="sxs-lookup"><span data-stu-id="82a7c-250">In such cases, developers will want to initialize the forward and inverse CAMs with their respective media white points.</span></span> <span data-ttu-id="82a7c-251">In einigen Fällen können Beobachter die Farbe der Medien Hintergründe vergleichen.</span><span class="sxs-lookup"><span data-stu-id="82a7c-251">In some cases, observers may be comparing the color of the media backgrounds.</span></span> <span data-ttu-id="82a7c-252">In diesen Fällen empfiehlt es sich, eine CAM für beide Geräte zu verwenden, und es kann wünschenswert sein, die farbmetrikwerte jedes Geräts nach dem mittleren weißen Punkt des Geräts zu skalieren.</span><span class="sxs-lookup"><span data-stu-id="82a7c-252">In these cases, it is advisable to use one CAM for both devices, and it may be desirable not to scale each device's colorimetric values by that device's medium white point.</span></span> <span data-ttu-id="82a7c-253">Dann führen die verschiedenen Werte für den Wert des Mediums in CIECAM02 zu unterschiedlichen Darstellungs Werten.</span><span class="sxs-lookup"><span data-stu-id="82a7c-253">Then the different tristimulus values of the media will lead to different appearance values in CIECAM02.</span></span>

## <a name="related-topics"></a><span data-ttu-id="82a7c-254">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="82a7c-254">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82a7c-255">Konzepte der grundlegenden Farbverwaltung</span><span class="sxs-lookup"><span data-stu-id="82a7c-255">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="82a7c-256">Windows Color System: Schemas und Algorithmen</span><span class="sxs-lookup"><span data-stu-id="82a7c-256">Windows Color System Schemas and Algorithms</span></span>](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





