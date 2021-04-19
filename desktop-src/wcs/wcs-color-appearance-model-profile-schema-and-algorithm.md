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
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>WCS-Farbdarstellungsmodell: Profilschema und Algorithmus

[Übersicht](#overview)

[Architektur des Farbdarstellung-Modell Profils (Camp)](#color-appearance-model-profile-architecture)

[Das Lager Schema](#the-camp-schema)

[Die Lager Schema Elemente](#the-camp-schema-elements)

[Der Camp-Algorithmus](#the-camp-algorithm)

### <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines Farbdarstellung-Modell Profils (Camp) anzugeben. Die zugehörigen baselinealgorithmen werden in den folgenden Abschnitten beschrieben.

Das Camp besteht aus XML-Tags, die parametrimetrische Werte für die Modell Variablen "CIECAM02 Baseline Color Appearance" bereitstellen. Ausführliche Informationen zu den Bereichen für Parameter finden Sie in den grundlegenden Farbdarstellung und der CIECAM02-Empfehlung.

### <a name="color-appearance-model-profile-architecture"></a>Architektur des Farbdarstellung-Modell Profils

![Diagramm, das die von X M L-Tags erstellte Architektur des Lager Profils anzeigt.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>Das Lager Schema


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



## <a name="the-camp-schema-elements"></a>Die Lager Schema Elemente

## <a name="colorappearancemodel"></a>Colorerscheinungs ancemodel

Dieses Element ist eine Sequenz von:

1.  Profilnamen Zeichenfolge,
2.  optionale Beschreibungs Zeichenfolge,
3.  optionale Autor Zeichenfolge,
4.  Viewingconditions-Element.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft. Zeichen folgen Längen sind auf 10.000 Zeichen beschränkt.

## <a name="namespace"></a>Namespace

xmlns: Cam = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Version

Version &gt; 0,1 oder &lt; = "1,0" mit der ersten Version von Windows Vista.

Überprüfungs **Bedingungen:** Jeder Versions Wert &lt; = 2,0 ist ebenfalls gültig, um nicht unterbrechende Änderungen im Format zu unterstützen.

## <a name="documentation"></a>Dokumentation

Profil Schema für Farbdarstellung des Modells.

Copyright (C) Microsoft. Alle Rechte vorbehalten.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

## <a name="surroundtype"></a>Surroundtype

Dieses Element ist entweder eine Enumeration von "Average", "Dim" oder "Dark" CIECAM02 Parametern oder die tatsächlichen quantitativen Parameter aus der CIECAM02-Empfehlung c, Auswirkung der umschließenden.

Überprüfungs **Bedingungen:** Der c-Parameter kann zwischen 0,525 und 0,69 liegen.

## <a name="viewingconditions"></a>Viewingconditions

Dieses Element besteht aus den folgenden untergeordneten Elementen:



| Element                    | type           |
|----------------------------|----------------|
| WhitePoint                 | Whitepointtype |
| Hintergrund                 | CIEXYZ         |
| Kur                   | Surroundtype   |
| "Luminanceofadaptingfield"   | float          |
| Degreeof-Anpassung         | float          |
| Normalizetomediawhitepoint | Boolean        |



 

Überprüfungs **Bedingungen:** CIEXYZ-unter Elemente werden von nonnegativexyztype überprüft. Der Wert für "luminanceofadaptingfield" ist maximal 10.000 CD/m ^ 2. Degreeofadaptions kann zwischen 0,0 und 1,0 liegen. Der normalizetomediawhitepoint-Wert kann entweder "true" oder "false" lauten. Wenn das Subelement normalizetomediawhitepoint nicht vorhanden ist, wird standardmäßig "true" verwendet. Weitere Informationen finden Sie im folgenden Abschnitt zu den lageralgorithmen.

## <a name="whitepointtype"></a>Whitepointtype

Dieses Element ist entweder eine Enumeration des Cie Light-Quell Werts ("D50", "D65", "a", "F2") oder ein "CIEXYZ"-Unterelement.

Überprüfungs **Bedingungen:** Jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

## <a name="ciexyztype"></a>Ciexyztype

Das ciexyztype-Element besteht aus drei nicht-negativefloattype-IEEE-Gleit Komma Elementen mit dem Namen "X", "Y" und "Z". Bei diesen Messungen kann es sich entweder um absolute (nicht relative) CIEXYZ 1931-reflektierte Werte oder absolute (nicht relative) CIEXYZ 1931 Direct-Werte (Transmissive) in den quadratischen Einheiten von Kerzen pro Meter handelt.

Überprüfungs **Bedingungen:** Dies bedeutet, dass nur reale Werte gültig sind, und negative CIEXYZ-Mess Werte sind ungültig. Da es sich hierbei um absolute Werte handelt, können Werte weit über 1,0 f hinaus reichen. Ein angemessener Grenzwert für jeden X-, Y-oder Z-Wert wird willkürlich auf 10000.0 f festgelegt.

 

### <a name="the-camp-algorithm"></a>Der Camp-Algorithmus

Das Farb Darstellungs Modell (Color Appearance Model, CAM) basiert auf den Modellen der Cie CIECAM02 Color-Darstellung.

Diese Klasse implementiert die Farbdarstellung von Modellen. Beachten Sie, dass die WCS-CAM *nicht* mithilfe eines Plug-ins ersetzt werden kann. Es ist ein Entwurfs Ziel, nur ein Farb Darstellungs Modell zu haben. Der Cam basiert auf CIECAM02-Empfehlungen.

CIECAM02 kann auf zwei Arten verwendet werden. In der Richtung "farbige Metrik-zu-Darstellung" wird eine Zuordnung zwischen dem Bereich "Cie XYZ" und dem Leerraum bereitstellt. In der Richtung "Darstellung bis farbige Metrik" erfolgt die Zuordnung aus dem Farb Darstellungs Raum zurück zu XYZ-Leerraum. Die Farbdarstellung korreliert Helligkeit, J, Chroma, C und Hue, h. Diese drei Werte bilden ein zylindrisches Koordinatensystem. Häufig ist es leichter, in einem rechteckigen Koordinatensystem zu arbeiten, also Compute a = c cos h und b = c Sin h, um CIECAM02 Jab zu geben.

Sie können die Werte der Cam-Helligkeit größer als 100 verwenden. Das Cie-Komitee, das CIECAM02 formuliert hat, entsprach nicht dem Verhalten der Helligkeit-Achse für Eingabewerte mit einer Leuchtkraft, die größer ist als der übergebene weiße Punkt; Das heißt, für Eingabe-y-Werte, die größer sind als der Wert des angenommenen y-Punkts. Das Experimentieren hat ergeben, dass sich die Leuchtkraft Gleichungen in CIECAM02 für solche Werte in angemessener Weise Verhalten. Die Helligkeit nimmt exponentiell zu und folgt dem gleichen Exponent (ungefähr 1/3).

Manchmal möchten Benutzer die Art und Weise ändern, in der der Grad der Anpassung (D) berechnet wird. Der WCS-Entwurf ermöglicht es Benutzern, diese Berechnung zu steuern, indem der Wert für degreeofadaption in den Parametern der Anzeige Bedingungen geändert wird.

Um den von den Benutzern, die von den Ansprüchen im Zusammenwirken von Benutzern eine konsistente Übereinstimmung bieten, zu gewährleisten, 1,0 ist die degreeofadaption in den Standard Camps Dies führt zu besseren Ergebnissen in allen Fällen als bei mincd absolute, bei denen WCS die degreeofadaption (über degreeofadaption =-1) berechnen könnte.

Anstatt einen umschließenden Wert "Average", "Dim" und "Dark" zu verwenden, wird ein kontinuierlicher Umschließungs Wert bereitgestellt, der aus dem Wert c berechnet wird. Der Wert von c muss ein float-Wert zwischen 0,525 und 0,69 sein.

Aus *c* können *NC* und *F* berechnet werden. dabei wird die schrittweise lineare interpolung zwischen den Werten verwendet, die bereits für "Average", "Dim" und "Dark" bereitgestellt wurden. Dies modelliert die Darstellung in Abbildung 1 von Cie 159:2004, der CIECAM02-Spezifikation.



| degreeof-Anpassung                     | Verhalten                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Zeigt eine Formel für das Standardverhalten c I E c a M 02 an.](images/camp-image006.png)Dies ist das Standardverhalten von CIECAM02.<br/> |
| 0,0 &lt; = degreeof-Anpassung &lt; = 1,0 | *D* = degreeof-Anpassung (der vom Benutzer bereitgestellte Wert)                      |



 

Eine bestimmte Menge an Fehlerüberprüfung wurde auch der-Implementierung hinzugefügt. Die folgenden Gleichung Zahlen werden in der Definition von Cie 159:2004 von CIECAM02 verwendet.

**Farbige metricin-ancecolors**

Die Eingabewerte werden auf eine nicht zurechtheit geprüft: Wenn X oder Z &lt; 0,0 oder Y &lt; -1,0, ist das HRESULT E \_ invalidArg. Wenn-1,0 &lt; = Y &lt; 0,0, werden J, C und h alle auf 0,0 festgelegt.

Es gibt bestimmte interne Bedingungen, die zu Fehlern führen können. Anstatt solche Ergebnisse zu erzeugen, werden die internen Ergebnisse abgeschnitten, um Werte im Gültigkeitsbereich zu erzeugen. Dies geschieht bei Spezifikationen von Farben, die dunkel und unverändersch sind: in Gleichung 7,23, wenn ein Wert von &lt; 0, a = 0. In Gleichung 7,26, wenn t &lt; 0, t = 0.

**Anzeige von "Erscheinungsbild"**

Die Eingabewerte werden auf eine nicht zurechtheit geprüft. Bei c &lt; 0, c &gt; 300 oder J &gt; 500 ist das HRESULT E \_ invalidArg.

*R '<sub>a;</sub>*, *G '<sub>a;</sub>* und *B '<sub>a;</sub>*, (Gleichungen 8,19-8,21) werden auf den Bereich 399,9 zugeschnitten.

Für alle Farbdarstellung-Modell profile (CAMPs) prüft die WCS-Engine den angenommenen weißen Punkt. Wenn y nicht 100,0 ist, wird der übergelagene weiße Punkt so skaliert, dass y gleich 100,0 ist. Die gleiche Skalierung wird auf den Hintergrund Wert angewendet. Der Skalierungsfaktor ist 100,0/adoptedwhitepoint. Y. Der Faktor für die Skalierung wird auf die einzelnen X-, Y-und Z-Dateien angewendet. Wenn das normalizetomediawhitepoint-Feld auf "true" festgelegt ist, oder wenn es nicht im Camp vorhanden ist, skaliert die Engine auch alle Eingabe Farben für Geräte Farben in devicetocolormetric, sodass der Y-Wert des Mediums mit dem Medien Medium 100,0 lautet. Geräte Farben von colormetrictodevice werden durch die multiplikative Umkehrung dieses Skalierungsfaktors skaliert. Wenn das normalizetomediawhitepoint-Flag auf "false" festgelegt ist, werden die farbige Metrikdaten nicht skaliert.

Bei einigen Aufgaben ist es sinnvoll, die farbmetrikwerte aus devicedecolormetric zu skalieren. Die hyperbolische Glanz Gleichungen in der CAM sind tatsächlich für eine weiße Punktbeleuchtung von 100,0 konzipiert. Die einzige Stelle, an der ein Unterschied in der absoluten Leuchtkraft (bzw. Beleuchtung) wiedergegeben wird, ist die Helligkeit des Anpassungs Felds. Daher muss der Cam mit einem weißen Punkt Y von 100,0 initialisiert werden. Wenn jedoch der mittlere weiße Punkt des Geräte Modells als gehostdeter weißer Punkt verwendet wird, müssen alle vom Gerät ausgehenden Farben entsprechend skaliert werden, oder das Gerät weiß nicht mit dem J-Wert 100,0. Daher müssen die Y-Werte in den Messungen skaliert werden. Die Maßwerte können vor dem Initialisieren des Geräte Modells skaliert werden. Die Ergebnisse befinden sich bereits im richtigen Bereich. Dies würde jedoch das Testen des Geräte Modells erschweren, da die ausgehenden Werte skaliert werden müssen. Bei Aufgaben, bei denen der Mittelpunkt des Mediums weiß, dass es sich um ein echtes weiß handelt, ist das normalisieren durch den Geräte Medien-weißen Punkt wünschenswert.

Der Cam wird direkt aus dem Camp initialisiert. Dies ermöglicht Entwicklern eine gewisse Flexibilität bei der Initialisierung der Cam, basierend auf der Aufgabe, die Sie ausführen möchten. In einigen Aufgaben ignorieren Beobachter alle Chroma in den Medien weißen Punkten, da Sie erkennen, dass die Quell-und Zielmedien "weiß" sind. In solchen Fällen möchten Entwickler die Forward-und inverse-Cams mit ihren jeweiligen Medien weißen Punkten initialisieren. In einigen Fällen können Beobachter die Farbe der Medien Hintergründe vergleichen. In diesen Fällen empfiehlt es sich, eine CAM für beide Geräte zu verwenden, und es kann wünschenswert sein, die farbmetrikwerte jedes Geräts nach dem mittleren weißen Punkt des Geräts zu skalieren. Dann führen die verschiedenen Werte für den Wert des Mediums in CIECAM02 zu unterschiedlichen Darstellungs Werten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





