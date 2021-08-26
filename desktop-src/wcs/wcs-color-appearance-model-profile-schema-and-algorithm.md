---
title: 'WCS-Farbdarstellungsmodell: Profilschema und Algorithmus'
description: 'WCS-Farbdarstellungsmodell: Profilschema und Algorithmus'
ms.assetid: 017588fe-cec9-4178-a912-7950cefc036c
keywords:
- Windows Color System (WCS), Farbdarstellungsmodellprofil (COLOR)
- WCS (Windows Color System), Farbdarstellungsmodellprofil (COLOR)
- Bildfarbverwaltung, Farbdarstellungsmodellprofil (COLOR)
- Farbverwaltung, Farbdarstellungsmodellprofil (COLOR)
- Farben, Farbdarstellungsmodellprofil (COLOR)
- Windows Color System (WCS), Profile
- WCS (Windows Color System), Profile
- Bildfarbverwaltung, Profile
- Farbverwaltung, Profile
- Farben, Profile
- Farbdarstellungsmodellprofil (COLOR)
- COLOR (Farbdarstellungsmodellprofil)
- Schemas, Farbdarstellungsmodellprofil (COLOR)
- Algorithmen, Farbdarstellungsmodellprofil (COLOR)
- WCS-Farbdarstellungsmodellprofil
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042cf74d264a7b5d40fdc30fec44784680a67b95363b579d0c7bebc7ececcedb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090098"
---
# <a name="wcs-color-appearance-model-profile-schema-and-algorithm"></a>WCS-Farbdarstellungsmodell: Profilschema und Algorithmus

[Übersicht](#overview)

[COLOR-Architektur (Color Appearance Model Profile)](#color-appearance-model-profile-architecture)

[DAS SCHEMA DES SCHEMAS](#the-camp-schema)

[DIE SCHEMAELEMENTE DES SCHEMAS](#the-camp-schema-elements)

[Der ALGORITHM-Algorithmus](#the-camp-algorithm)

### <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines Farbdarstellungsmodellprofils (COLOR) anzugeben. Die zugeordneten Baselinealgorithmen werden in den folgenden Abschnitten beschrieben.

Die COLOR besteht aus XML-Tags, die parametrische Werte für die Variablen des CIECAM02-Baselinefarbdarstellungsmodells bereitstellen. Details zu den Bereichen für Parameter finden Sie in der Spezifikation des Basisfarbdarstellungsmodells und der CIECAM02-Empfehlung.

### <a name="color-appearance-model-profile-architecture"></a>Architektur des Farbdarstellungsmodellprofils

![Diagramm, das die PROFILarchitektur VON X M L-Tags zeigt.](images/camp-image002new.png)

### <a name="the-camp-schema"></a>DAS SCHEMA DES SCHEMAS


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



## <a name="the-camp-schema-elements"></a>DIE SCHEMAELEMENTE DES SCHEMAS

## <a name="colorappearancemodel"></a>ColorAppearanceModel

Dieses Element ist eine Sequenz von:

1.  ProfileName-Zeichenfolge,
2.  optionale Beschreibungszeichenfolge,
3.  optionale Erstellungszeichenfolge,
4.  ViewingConditions-Element.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft. Zeichenfolgenlängen sind auf 10.000 Zeichen beschränkt.

## <a name="namespace"></a>Namespace

xmlns:cam=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/ColorAppearanceModel "

## <a name="version"></a>Version

Version &gt; 0.1 oder &lt; = "1.0" mit der ersten Version von Windows Vista.

**Überprüfungsbedingungen:** Jeder Versionswert &lt; =2.0 ist auch gültig, um nicht breaking changes am Format zu unterstützen.

## <a name="documentation"></a>Dokumentation

Profilschema des Farbdarstellungsmodells.

Copyright (C) Microsoft. All rights reserved.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

## <a name="surroundtype"></a>SurroundType

Dieses Element ist entweder eine Enumeration der CIECAM02-Parameter "Average", "Dim" oder "Dark" oder die tatsächlichen quantitativen Parameter aus der CIECAM02-Empfehlung c, Auswirkung der Umgebung.

**Überprüfungsbedingungen:** Der c-Parameter kann zwischen 0,525 und 0,69 liegen.

## <a name="viewingconditions"></a>ViewingConditions

Dieses Element besteht aus den folgenden Unterelementen:



| Element                    | Typ           |
|----------------------------|----------------|
| Weißtons                 | WhitePointType |
| Hintergrund                 | CIEXYZ         |
| Surround                   | SurroundType   |
| LuminanceOfAdaptingField   | float          |
| DegreeOfAdaptation         | float          |
| NormalizeToMediaWhitePoint | Boolesch        |



 

**Überprüfungsbedingungen:** CIEXYZ-Unterelemente werden durch NonNegativeXYZType überprüft. LuminanceOfAdaptingField ist maximal 10.000cd/m^2. DegreeOfAdaptation kann zwischen 0,0 und 1,0 liegen. Der NormalizeToMediaWhitePoint-Wert kann entweder "true" oder "false" sein. Wenn das Unterelement NormalizeToMediaWhitePoint nicht vorhanden ist, wird standardmäßig "true" verwendet. Weitere Informationen finden Sie im folgenden ABSCHNITT ZUM ALGORITHMUS.

## <a name="whitepointtype"></a>WhitePointType

Dieses Element ist entweder eine Enumeration des CIE-Lichtquellenwerts ("D50", "D65", "A" oder "F2") oder ein CIEXYZ-Unterelement.

**Überprüfungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

## <a name="ciexyztype"></a>CIEXYZType

Das CIEXYZType-Element besteht aus drei NonNegativeFloatType IEEE-Gleitkommaelementen mit einfacher Genauigkeit mit den Namen "X", "Y" und "Z". Diese Messungen können entweder absolute (nicht relative) CIEXYZ 1931 reflektierende Werte oder absolute (nicht relative) CIEXYZ 1931 direkte (transmissive) Werte in Candelas pro Quadrateinheiten pro Meter sein.

**Überprüfungsbedingungen:** Dies bedeutet, dass nur reale Werte gültig sind und negative CIEXYZ-Messwerte ungültig sind. Da es sich hierbei um absolute Werte handelt, können Werte weit über 1,0f liegen. Ein angemessener Grenzwert für jeden X-, Y- oder Z-Wert wird willkürlich auf 10000,0f festgelegt.

 

### <a name="the-camp-algorithm"></a>Der ALGORITHM-Algorithmus

Das Farbdarstellungsmodell (COLOR) basiert auf den Formeln des CIE CIE CIECAM02-Farbdarstellungsmodells.

Diese Klasse implementiert die Farbdarstellungsmodellierung. Beachten Sie, dass das WCS-PLUG-IN *nicht* ersetzt werden kann, z. B. mithilfe eines Plug-Ins. Es ist ein Entwurfsziel, nur ein Farbdarstellungsmodell zu verwenden. Der FOKUS basiert auf CIECAM02-Empfehlungen.

CIECAM02 kann auf zwei Arten verwendet werden. In der Colorimetric-to-Appearance-Richtung wird eine Zuordnung vom CIE XYZ-Raum zum Farbdarstellungsbereich ermöglicht. In der Farbgebungsrichtung wird der Farbdarstellungsbereich wieder dem XYZ-Raum zugeordnet. Die Farbdarstellung korreliert Helligkeit, J, Glanz, C und Farbton, h. Diese drei Werte bilden ein koordinatenförmiges Koordinatensystem. Häufig ist es praktischer, in einem rechteckigen Koordinatensystem zu arbeiten. Berechnen Sie also a = C cos h und b = C sin h, um CIECAM02 Jab zu erhalten.

Sie können DIE LIGHTNESS-Werte größer als 100 verwenden. Der CIE-Ausschuss, der CIECAM02 formuliert hat, hat sich nicht mit dem Verhalten der Helligkeitsachse für Eingabewerte befasst, deren Leuchtdichte größer als der angenommene Weißpunkt ist. Das heißt, für Eingabewerte von Y, die größer als der übernommene weißer Punkt Y-Wert sind. Experimente haben gezeigt, dass sich die Leuchtdichtegleichungen in CIECAM02 für solche Werte angemessen verhalten. Die Lichtheit nimmt exponentiell zu und folgt demselben Exponenten (ungefähr 1/3).

Benutzer möchten manchmal ändern, wie der Grad der Anpassung (D) berechnet wird. Mit dem WCS-Entwurf können Benutzer diese Berechnung steuern, indem sie den DegreeOfadaptation-Wert in den Parametern der Anzeigebedingungen ändern.

Um eine konsistentere Übereinstimmung mit den VOM BENUTZER beeinflussten Erwartungen zu bieten, ist degreeOfAdaptation in der Standardeinstellung 1.0. Dies führt in allen Anderen Fällen als MinCD Absolute zu besseren Ergebnissen, in denen WCS möglicherweise den DegreeOfAdaptation (über degreeOfAdaptation = -1) berechnen soll.

Anstatt den Umschließwert "Average", "Dim" und "Dark" zu verwenden, wird ein kontinuierlicher Umschließungswert bereitgestellt, der aus dem Wert c berechnet wird. Der Wert von c muss ein Gleitkommawert zwischen 0,525 und 0,69 sein.

Von *c* aus können *Nc* und *F* mithilfe einer stückweise linearen Interpolation zwischen den Werten berechnet werden, die bereits für "Average", "Dim" und "Dark" bereitgestellt wurden. Hier wird das modelliert, was in Abbildung 1 von CIE 159:2004, der CIECAM02-Spezifikation, dargestellt ist.



| degreeOfAdaption                     | Verhalten                                                                       |
|--------------------------------------|--------------------------------------------------------------------------------|
| -1.0                                 | ![Zeigt eine Formel für das Standardverhalten von C I E C A M 02 an.](images/camp-image006.png)Dies ist das Standardverhalten von CIECAM02.<br/> |
| 0,0 &lt; = degreeOfAdaption &lt; = 1,0 | *D* = degreeOfAdaptation (der vom Benutzer angegebene Wert)                      |



 

Der Implementierung wurde auch eine bestimmte Anzahl von Fehlerüberprüfungen hinzugefügt. Die folgenden Gleichungszahlen werden in der CIE 159:2004-Definition von CIECAM02 verwendet.

**ColorimetricToAppearanceColors**

Die Eingabewerte werden auf Angemessenes überprüft: Wenn X oder Z &lt; 0,0 oder Y &lt; -1,0, dann ist das HRESULT E \_ INVALIDARG. Wenn -1.0 &lt; = Y &lt; 0.0 ist, werden J, C und h alle auf 0,0 festgelegt.

Es gibt bestimmte interne Bedingungen, die zu Fehlerergebnissen führen können. Anstatt solche Ergebnisse zu erzeugen, werden die internen Ergebnisse abgeschnitten, um Werte innerhalb des Bereichs zu erzeugen. Dies geschieht bei Spezifikationen von Farben, die dunkel und unergründlich versunken sind: In Gleichung 7.23, wenn A &lt; 0, A = 0. In Gleichung 7.26, wenn t &lt; 0, t = 0.

**AppearanceToColorimetricColors**

Die Eingabewerte werden auf Sinnvolles überprüft. Wenn C &lt; 0, C &gt; 300 oder J &gt; 500, dann ist das HRESULT E \_ INVALIDARG.

*R'<sub>a;</sub>*, *G'<sub>a;</sub>* und *B'<sub>a;</sub>*, (Gleichungen 8.19 - 8.21) werden auf den Bereich 399.9 abgeschnitten.

Für alle COLOR Appearance Model Profiles (NAPPs) untersucht die WCS-Engine den übernommenen Weißpunkt. Wenn Y nicht 100,0 ist, wird der übernommene Weißpunkt skaliert, sodass Y gleich 100,0 ist. Die gleiche Skalierung wird auf den Hintergrundwert angewendet. Der Skalierungsfaktor ist 100.0/adoptWhitePoint.Y. Der gleiche Skalierungsfaktor wird auf alle X-, Y- und Z-Skalierungsfaktor angewendet. Wenn das Feld NormalizeToMediaWhitePoint auf "True" festgelegt ist, oder wenn es nicht im FELD vorhanden ist, skaliert die Engine auch alle Gerätefarbeneingaben auf DeviceToColorimetric, sodass der Y-Wert des Gerätemedien-Weißpunkts gleich 100,0 ist. Gerätefarben, die von ColorimetricToDevice kommen, werden durch die multiplikative Umkehrung dieses Skalierungsfaktors skaliert. Wenn das NormalizeToMediaWhitePoint-Flag auf "False" festgelegt ist, werden die Farbmetrikdaten nicht skaliert.

Bei einigen Aufgaben ist es sinnvoll, die colorimetric-Werte aus DeviceToColorimetric zu skalieren. Die hyperbolischen Lichtheitsgleichungen in der WEBCAM sind wirklich für eine Weißpunkt-Leuchtdichte von 100,0 konzipiert. Der einzige Ort, an dem ein Unterschied in der absoluten Luminanz (oder Derstanz) ins Spiel kommt, ist die Leuchtdichte des anpassenden Felds. Daher muss dieCAM mit einem weißen Punkt Y von 100.0 initialisiert werden. Wenn jedoch der mittlere Weißpunkt des Gerätemodells als übernommener weißer Punkt verwendet wird, müssen alle Farben, die vom Gerät stammen, entsprechend skaliert werden, oder das Gerät weiß wird nicht mit dem J-Wert 100,0 angezeigt. Daher müssen die Y-Werte in den Messungen skaliert werden. Die Messwerte könnten vor der Initialisierung des Gerätemodells skaliert werden. Die Ergebnisse liegen dann bereits im richtigen Bereich. Dies würde jedoch das Testen des Gerätemodells erschweren, da die auskommenden Werte eine Skalierung erfordern würden. Für Aufgaben, bei denen der mittlere Weißpunkt des Geräts als richtig weiß wahrgenommen wird, ist eine Normalisierung durch den Gerätemedien-Weißpunkt wünschenswert.

DieCAM wird direkt aus der DABEI-Instanz initialisiert. Dies ermöglicht Entwicklern ein gewisses Maß an Flexibilität bei der Initialisierung der TASK basierend auf der Aufgabe, die sie ausführen möchten. In einigen Aufgaben ignorieren Beobachter alle White Points in den Medien, da sie kognitiv "wissen", dass die Quell- und Zielmedien "weiß" sind. In solchen Fällen möchten Entwickler die Vorwärts- und umgekehrten CAMs mit ihren jeweiligen Medien-White points initialisieren. In einigen Fällen vergleichen Beobachter möglicherweise die Farbe der Medienhintergrund. In diesen Fällen empfiehlt es sich, für beide Geräte ein EINZIGES ZU VERWENDEN, und es kann wünschenswert sein, die Farbmetrikwerte der einzelnen Geräte nicht nach dem mittleren Weißpunkt des Geräts zu skalieren. Dann führen die verschiedenen Tristimuluswerte des Mediums zu unterschiedlichen Darstellungswerten in CIECAM02.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 





