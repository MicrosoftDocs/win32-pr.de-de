---
title: 'WCS-Farbauswahlpalette: Profilschema und Algorithmen'
description: 'WCS-Farbauswahlpalette: Profilschema und Algorithmen'
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Color System (WCS), Gamut Map Model Profile (GMMP)
- WCS (Windows Color System), Gamut Map Model Profile (GMMP)
- Bild Farbverwaltung, Gamut Map Model Profile (GMMP)
- Farbverwaltung, Gamut Map Model Profile (GMMP)
- Farben, Gamut Map Model Profile (GMMP)
- Windows Color System (WCS), profile
- WCS (Windows Color System), profile
- Bildfarben Verwaltung, profile
- Farbverwaltung, profile
- Farben, profile
- Farbskala Map Model Profile (GMMP)
- GMMP (Gamut Map Model Profile)
- WCS-Modell Profil für gamingkarten
- Schemas, Gamut Map Model Profile (GMMP)
- Algorithmen, Gamut Map Model Profile (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3714e5d7592cb1fbbbfa98e238642a2fcb38bafd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104566894"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>WCS-Farbauswahlpalette: Profilschema und Algorithmen

-   [Übersicht](#overview)
-   [Architektur des Gamut-Karten Modell Profils](#gamut-map-model-profile-architecture)
-   [Generierung der Gamut-Grenze](#generation-of-the-gamut-boundary)
-   [Das GMMP-Schema](#the-gmmp-schema)
-   [Die GMMP-Schema Elemente](#the-gmmp-schema-elements)
-   [Gamutmapmodel](#defaultbaselinegamutmapmodel-type)
    -   [Namespace](#namespace)
    -   [Version](#version)
    -   [Dokumentation](#documentation)
    -   [Defaultbaselinegamutmapmodel-Typ](#defaultbaselinegamutmapmodel-type)
    -   [Plugingamutmaptype](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Die GMMP-baselinealgorithmen](#the-gmmp-baseline-algorithms)
-   [Ausrichten der neutralen Achsen](#aligning-the-neutral-axes)
    -   [Minimale Farbunterschiede (mincd)](#minimum-color-difference-mincd)
    -   [Basicphoto](#basicphoto)
    -   [Übersicht](#overview)
    -   [Die Groß-/Kleinschreibung einer einzelnen Farbskala-Shell](#the-case-of-single-gamut-shell)
    -   [Schwarze Erweiterung](#black-enhancement)
    -   [Die Groß-/Kleinschreibung von dualer Farbskala Shells](#the-case-of-dual-gamut-shells)
    -   [Gründe für Änderungen von den Cie TC8-03-Empfehlungen](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Hue-Zuordnung](#hue-mapping)
-   [Beschreibung von Gamut-Grenzen und Gamut-shellalgorithmen](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Die Untergrenze der spielbegrenzung.](#triangulation-of-the-gamut-boundary)
    -   [Begrenzungs Linien Elemente](#boundary-line-elements)
    -   [Gamut-Vorgang: Prüfpunkt](#gamut-operation-checkgamut)
    -   [Vollton-Ebene: Intersect](#full-hue-plane-intersect)
    -   [Gamut-Vorgang: checkgamut (fortgesetzt)](#gamut-operation-checkgamut-continued)
    -   [Minimale Farbunterschiede-Diagramm Zuordnung](#minimum-color-difference-gamut-mapping)
    -   [Farbton Glättung](#hue-smoothing)
    -   [Festlegen von primären und sekundären Replikaten in der Beschreibung der changesehe](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Festlegen der neutralen Achse in der Beschreibung der Gamut-Grenze](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines Farbskala Map Model-Profils (GMMP) anzugeben. Die zugehörigen baselinealgorithmen werden im folgenden Thema beschrieben.

Das grundlegende GMMP-Schema besteht aus allgemeinen Header Informationen, einem optionalen Verweis auf ein bevorzugtes Gamut-Karten Modell-Plug-in und Erweiterungs Tags.

Darüber hinaus stellt das GMMP explizite Informationen über das Zielmodell für die Gamut-Zuordnung bereit und stellt eine Richtlinie für das Modell der baselinefallbackgamingzuordnung bereit, das verwendet werden soll, wenn das Zielmodell nicht verfügbar ist. Das Schema kann private Erweiterungsinformationen enthalten, enthält jedoch keine weiteren überflüssigen Informationen.

## <a name="gamut-map-model-profile-architecture"></a>Architektur des Gamut-Karten Modell Profils

![Diagramm, das das Modell Profil für die Profilerstellung anzeigt.](images/gmmp-image002.png)

Die Stichprobenentnahme des Colorant-Raums der Ausgabegeräte erfolgt durch Durchlaufen der Colorants von 0,0 bis 1,0 mit einem Bruchteil, kumulieren Sie bei jedem Schritt alle Kombinationen der einzelnen coloranten, und wandeln Sie diese dann mithilfe der Methode DM::D evicetocolormetriccolors, gefolgt von der Methode CAM:: colormetrictoappearance-Methode, aus dem Colorant-Raum des Geräts in den Farb Darstellungs Bereich um. Im folgenden finden Sie ein Beispiel dafür, wie dies für RGB erfolgt.


```C++
For (red= 0.0; red <= 1.0; red += redStep) {

     For (green = 0.0; green <= 1.0; green += greenStep) {

          For (blue = 0.0; blue <= 1.0; blue += blueStep) {

               Colorants[0] = red; colorants[1] = green; colorants[2] = blue;

               pRGBDM->DeviceToColorimetricColors(1, colorants, &amp;XYZ);

               pCAM->ColorimetricToAppearanceColors(1, &amp;XYZ, &amp;JCh);

          }

     }

}

```



## <a name="generation-of-the-gamut-boundary"></a>Generierung der Gamut-Grenze

Es gibt drei Komponenten der Grenze für das Spiel: die primäre Replikate, die neutralen Beispiele und die Shells. Die primären Replikate werden generiert, indem die Geräte primäre Replikate übernommen und die devicetocolormetric/colormetrictoappearance-Transformation angewendet wird. Die neutralen Beispiele werden generiert, indem der Colorant-Bereich des Geräts im neutralen Bereich Abtast und dieselbe Transformation angewendet wird. Für drei Colorant-Geräte (RGB oder CMY) werden die neutralen Beispiele so definiert, dass alle Colorants gleich sind, z. b. R = = G = = B. Für CMYK sind die neutralen Beispiele so definiert, dass Sie C = = M = = Y = = 0 aufweisen.

Die Faktoren, die die Daten beeinflussen, die zum Erstellen der Farbskala-Grenze verwendet werden, sind die Daten Stichproben (nur baselinegeräte) und die Anzeige Bedingungen. Die Schrittgröße, die für die vollständige Stichprobenentnahme des Colorant-Raums (für Monitore und für eine plausible Shell) verwendet wird, ist eine interne Konstante und ist nicht für die externe Bearbeitung verfügbar. Durch Ändern der Anzeige Bedingungen wird das Verhalten des Farb Darstellungs Modells (Color Appearance Model, CAM) geändert, und die Form der spielbegrenzung wird geändert, sodass Sie eine an das Profil der Anzeige Bedingungen gebundene Farbskala-Grenze generieren müssen. Wenn Beispiel Daten verwendet werden, wie im Fall von baselinedruckern und Erfassungs Geräten, haben die Beispiele eine große Auswirkung auf die Form des Verweis Schachtes und wirken sich auf das Verhalten des Modells selbst aus.

Für Eingabegeräte, z. b. Kameras und Scanner, werden unterschiedliche Samplings verwendet, um die verweisshell und die plausible Shell zu generieren. Die verweisshell wird aus den Messungen generiert, die zum Initialisieren des Geräte Modells verwendet werden. Die plausible Shell wird ähnlich wie in der vorherigen Abbildung für Ausgabegeräte generiert. Der Unterschied besteht darin, dass Sie beim Eingeben eines typischen Ziels nicht vollständig satte Werte erhalten (R, G oder B = 255). Sie müssen die Werte mithilfe des Geräte Modells extrapolieren.

## <a name="the-gmmp-schema"></a>Das GMMP-Schema


```C++
<?xml version="1.0" encoding="UTF-8"?>
<xs:schema 
  xmlns:gmm="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:wcs="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes"
  targetNamespace="http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel"
  xmlns:xs="http://www.w3.org/2001/XMLSchema"
  elementFormDefault="qualified"
  attributeFormDefault="unqualified"
  blockDefault="#all"
  version="1.0">

  <xs:annotation>
    <xs:documentation>
      Gamut Map Model profile schema.
      Copyright (C) Microsoft. All rights reserved.
    </xs:documentation>
  </xs:annotation>

  <xs:import namespace="http://schemas.microsoft.com/windows/2005/02/color/WcsCommonProfileTypes" />

  <xs:element name="GamutMapModel">
    <xs:complexType>
      <xs:sequence>
        <xs:element name="ProfileName" type="wcs:MultiLocalizedTextType"/>
        <xs:element name="Description" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="Author" type="wcs:MultiLocalizedTextType" minOccurs="0"/>
        <xs:element name="DefaultBaselineGamutMapModel">
          <xs:simpleType>
            <xs:restriction base="xs:string">
              <xs:enumeration value="HPMinCD_Absolute"/>
              <xs:enumeration value="HPMinCD_Relative"/>
              <xs:enumeration value="SGCK"/>
              <xs:enumeration value="HueMap"/>
            </xs:restriction>
          </xs:simpleType>
        </xs:element>
        <xs:element name="PlugInGamutMapModel" minOccurs="0">
          <xs:complexType>
            <xs:sequence>
              <xs:any namespace="##other" processContents="skip"
                minOccurs="0" maxOccurs="unbounded" />
            </xs:sequence>
            <xs:attribute name="GUID" type="wcs:GUIDType" use="required"/>
          </xs:complexType>
        </xs:element>
      </xs:sequence>
      <xs:attribute name="ID" type="xs:string" use="optional" />
    </xs:complexType>
  </xs:element>
</xs:schema>
```



## <a name="the-gmmp-schema-elements"></a>Die GMMP-Schema Elemente

## <a name="gamutmapmodel"></a>Gamutmapmodel

Dieses Element ist eine Sequenz der folgenden unter Elemente:

1.  Profilnamen Zeichenfolge,
2.  Defaultbaselinegamutmapmodel,
3.  Optionale Beschreibungs Zeichenfolge,
4.  Optionale Autor Zeichenfolge,
5.  Optionale plugingamutmap und
6.  Optionaler ExtensionType.

**Validierungs Bedingungen** : jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="namespace"></a>Namespace

xmlns: GMM = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace = " http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Version

Version "1,0" mit der ersten Version von Windows Vista.

Überprüfungs **Bedingungen** : 1,0 in Windows Vista. &lt;Die Versionen 2,0 sind ebenfalls gültig, um nicht unterbrechende Änderungen im Format zu unterstützen.

### <a name="documentation"></a>Dokumentation

Profil Schema für Gamut-Karten Modell.

Copyright (C) Microsoft. Alle Rechte vorbehalten.

**Validierungs Bedingungen** : jedes untergeordnete Element wird anhand seines eigenen Typs überprüft.

### <a name="defaultbaselinegamutmapmodel-type"></a>Defaultbaselinegamutmapmodel-Typ

Uint-Typ

Enumerationswerte:

<dl> "Mincd \_ absolute"  
"Mincd \_ relative"  
"SIG- \_ Knie"  
"Huemap"  
</dl>

**Validierungs Bedingungen** : die Werte müssen mit einer der oben aufgeführten Enumerationen identisch sein.

### <a name="plugingamutmaptype"></a>Plugingamutmaptype

Bei diesem Element handelt es sich um eine Sequenz eines GUID-guidtype und aller untergeordneten Elemente.

Überprüfungs **Bedingungen** : die GUID wird verwendet, um die GUID der GMM-Plug-in-dll abzugleichen. Es sind maximal 100.000 benutzerdefinierte unter Elemente vorhanden.

### <a name="extensiontype"></a>ExtensionType

Dieses Element ist eine optionale Sequenz von untergeordneten Elementen.

**Validierungs Bedingungen** : Es können maximal 100.000 unter Elemente vorhanden sein.

## <a name="the-gmmp-baseline-algorithms"></a>Die GMMP-baselinealgorithmen

## <a name="aligning-the-neutral-axes"></a>Ausrichten der neutralen Achsen

Die meisten Farbskala-Zuordnungsalgorithmen haben das Ziel, die neutrale Achse des Quell Geräts der neutralen Achse des Zielgeräts zu ordnen, d. h. weiß, weiß, schwarz zu schwarz und grau nach grau. Dies wird teilweise behandelt, indem die Helligkeit der Quell Farben an die Helligkeit des Zielgeräts angepasst wird. Das Problem wird dabei jedoch nicht vollständig behandelt.

Es handelt sich um eine physische Eigenschaft der meisten Bildverarbeitungsgeräte, die die Chromatizität des Geräts weiß nicht genau mit der Chromaticity des Geräts schwarz übereinstimmt. Beispielsweise hängt der Monitor weiß von der Summe der chromatitäten und der relativen Leuchtkraft der drei primären Replikate ab, während Monitor Black von der Reflektion der Anzeige Oberfläche abhängt. Der Drucker weiß ist von der papierstadt des Papiers abhängig, während der Drucker schwarz von der verwendeten Handschrift oder dem verwendeten Toner abhängig ist. Ein Darstellungs Modell, das das Gerät weiß exakt der neutralen Achse des Darstellungs Raums zuordnet (Chroma genau gleich null), wird das Gerät schwarz nicht der neutralen Achse zugeordnet. Da der Blick auf Chroma-Unterschiede sensibler ist, wenn die Helligkeit zunimmt, werden Mid-Grays als noch mehr als ein Gerät schwarz dargestellt. (In Abbildung 1 wird die Krümmung der neutralen Achsen in zwei Dimensionen veranschaulicht. Tatsächlich bilden die neutralen Achsen eine komplexere Kurve in drei Dimensionen.)

Obwohl die Cam vorhersagt, dass diese Geräte neutralen Farben als chromatisch angezeigt werden, scheinen die eigentlichen Beobachter dies zu kompensieren. Die meisten Benutzer sehen diese Geräte neutralen Werte nicht als "Chromatisch" an. Für die meisten gamingzuordnungs Modelle sollten Sie daher weiterhin Quell-und Geräte-Neutrals zuordnen.

Passen Sie die Quell-und Ziel-spielgrenzen und die einzelnen Pixel an, wenn Sie den Farbskala-Zuordnungs Algorithmus anwenden, um Quell-neutrale zu Geräte neutralen zuzuordnen. Passen Sie zuerst jeden Wert in der Quellfarbe an, sodass die neutrale Achse des Quell Geräts an der Helligkeit der Quellfarbe direkt auf der neutralen Achse des Darstellungs Raums liegt. (Weitere Informationen finden Sie auf der linken Seite von Abbildung 1.) Passen Sie dann die Beschreibung für die Beschreibung des Zielgeräts an, sodass jede Farbe auf der neutralen Achse des Zielgeräts an der Obergrenze der Begrenzungs Farbe des Zielgeräts direkt auf der neutralen Achse des Darstellungs Raums liegt. (Weitere Informationen finden Sie auf der rechten Seite von Abbildung 1.)

![Diagramm, das das Quell-Gamut-Begrenzungs Diagramm auf der linken Seite und die Ziel-spielbegrenzung auf der rechten Seite anzeigt.](images/gmmp-image004.png)

**Abbildung 1** : Ausrichtung der neutralen Achsen wird veranschaulicht. Left: Anpassen der Quellpunkte in Bezug auf die neutrale Quell Geräte Achse. Right: passen Sie die Beschreibung der Ziel-changesehe in Bezug auf die Beschreibung der Ziel-changesehe an.

Beachten Sie, dass Sie jeden quellpixelwert relativ zur neutralen Achse mit diesem Wert anpassen. Dadurch wird sichergestellt, dass Quell Geräte neutrale auf die neutrale Achse des Darstellungs Modells fallen. Außerdem verschieben Sie alle anderen Farben mit dieser Helligkeit um denselben Betrag, sodass keine Diskontinuitäten in der Darstellung des Quell-Gamut vorhanden sind. Sie müssen sich auf unterschiedlichen Ebenen um unterschiedliche Beträge bewegen, da die neutralen Quell Geräte nicht auf den unterschiedlichen Helligkeit-Ebenen als gleichzeitig auf den einzelnen Ebenen dargestellt werden. Dabei handelt es sich natürlich nicht um eine triviale Transformation.

Die Verarbeitung der Zielgeräte Werte ist ein wenig komplizierter. Zunächst passen Sie die gesamte Ziel-Spiel Grenze auf ähnliche Weise an, aber relativ zur neutralen Zielgeräte Achse. Dies wird in Abbildung 1 auf der rechten Seite veranschaulicht. Diese Anpassung stellt sicher, dass graue Quell Werte den grauen Zielwerten zugeordnet werden. Dies ist der Speicherplatz, in dem die Farbskala-Mapping-Algorithmen funktionieren.

Dieser Speicherplatz beschreibt jedoch nicht genau das tatsächliche Verhalten des Zielgeräts. Sie müssen die Zuordnung umkehren, bevor die zugeordneten Farben des Farbskala an das Darstellungs Modell und das Zielgeräte Modell übergeben werden. Alle zugeordneten Werte werden um das Gegenteil des Offsets versetzt, das zuvor auf die neutrale Zielgeräte Achse angewendet wurde. Dadurch wird die Ziel neutrale Achse wieder dem Wert zugeordnet, der ursprünglich von der Cam dargestellt wurde. Das gleiche gilt für die Spiel Grenze und alle Zwischenwerte.

![Diagramm, das ein Diagramm zum abmachen der Ausrichtung der neutralen Zielgeräte Achse anzeigt.](images/gmmp-image008.png)

**Abbildung 2** : Deaktivieren der Ausrichtung der neutralen Zielgeräte Achse

### <a name="minimum-color-difference-mincd"></a>Minimale Farbunterschiede (mincd)

Minimale Farbunterschiede (mincd) relative und absolute Versionen-Äquivalent zum Zweck des "ICC Color Metric".

> [!Note]  
> Der mincd-GMM eignet sich für die Zuordnung von Grafiken und Liniengrafiken mit "Logo"-Farben (Spotfarben), Farbverläufen für Logos mit einigen Farben und für die letzte Phase der Korrektur von Transformationen. Obwohl mincd GMM für Foto Bilder verwendet werden kann, die sich vollständig innerhalb des Ziel gamels befinden, wird das allgemeine Rendering von Fotobildern nicht empfohlen. Die Zuordnung von Farben, die sich nicht im Spiel befinden, zu Farben auf der Ziel-Farbskala-Oberfläche kann zu unerwünschten Artefakten führen, wie z. b. Tone-oder Chroma-Unregelmäßigkeiten in Smooth-Farbverläufen, die die Grenze überschreiten. Basicphoto wird für Foto Bilder empfohlen. Wenn für ein Foto-oder Contone-Image eine andere Farbskala-Zuordnung als basicphoto erforderlich ist, sollte die Alternative zum Erstellen eines Plug-in-GMM, das diese Zuordnung implementiert, anstelle von mincd verwendet werden.

 

Farben im Spiel bleiben unverändert. Für Out-of-Farbskala-Farben werden Helligkeit und Chroma angepasst, indem der Punkt im Ziel-Farbskala gefunden wird, der den minimalen Farb Abstand von nicht-in-Farbskala-Eingabe Punkten aufweist. Der Farb Abstand wird im Jch-Bereich berechnet. Allerdings wird der Abstand in den Helligkeit (J) und der Abstand in Chroma (C) oder Hue (h) anders gewichtet. Eine Chroma-abhängige Gewichtungsfunktion wird für den Abstand in der Helligkeit verwendet, sodass die Gewichtung für kleine Chroma kleiner ist und für große Chroma größer ist, bis ein Schwellenwert (Chroma) erreicht wird, bei dem die Gewichtung um 1 bleibt, d. h. die gleiche Gewichtung wie die Entfernung in Chroma oder Hue. Dies folgt der empfohlenen Verwendung für CMC und CIEDE2000. Es gibt zwei Varianten: relative farbige Metrik und absolute farbige Metrik.

**Relative farbige Metrik:** Richten Sie zunächst die Quell-und Ziel neutralen Achsen wie zuvor beschrieben aus. Wählen Sie dann die angepasste Quellfarbe an die angepasste Ziel-Spiel Grenze aus. (Siehe Abbildung 4. Chroma-Zuordnung entlang konstanter Helligkeit.) Lesen Sie die Zielgeräte Werte wie zuvor beschrieben. Im Fall einer Schnittstelle für das monochrome Ziel bedeutet das Chroma-Clipping, dass der Chroma-Wert (C) auf 0 (null) festgelegt ist (0,0).

**Absolute farbige Metrik:** Dies ähnelt der relativen farbige Metrik, aber ohne die Ausrichtung der Quell-und Ziel neutralen Achse. Der Quellwert wird direkt an die Ziel neutrale Achse abgeschnitten. Beachten Sie, dass das Verhalten identisch mit der relativen farbige Metrik ist, wenn sowohl die Quell-als auch die Ziel-spielgrenzen monochrome sind. Das heißt, die Ausrichtung der neutralen Achse wird ausgeführt, und dann wird der Chroma-Wert auf 0 (null) gekürzt. Dadurch wird sichergestellt, dass eine sinnvolle Ausgabe erreicht wird, auch wenn sich die Medien und Colorants erheblich unterscheiden.

![Diagramm, das ein Diagramm für das mincd-Clipping an die angepasste Spiel Palette zeigt.](images/gmmp-image010.png)

**Abbildung 3** : mincd-Clipping in den angepassten Farbskala

### <a name="basicphoto"></a>Basicphoto

### <a name="overview"></a>Übersicht

Basicphoto: entspricht der bevorzugten, malerischen oder perzeptive Absicht von ICC.

Dieser Algorithmus ist eine Variante der Chroma-abhängigen sigmoidal-Helligkeit-Zuordnung und der Cusp-Knie Skalierung (sgck), die von Cie TC8-03 in CIE156:2004 beschrieben wird. Dieser Variant-Algorithmus unterstützt Farbskala-Begrenzungs Deskriptoren (gbds) mit Dual-Farbskala-Shells. Das heißt, gbds mit einer verweisshell und eine plausible Shell. Der sgck-Algorithmus, der ursprünglich nur eine Farbskala-Shell in der Gbd annimmt, basiert auf dem SIG \_ -elgorithmus (braun 1999), der die sigmoidal-Helligkeit und die von Braun und Fairchild (1999) vorgeschlagene Skalierungs Funktion für die untergeordnete Funktion enthält, kombiniert mit der Chroma-Abhängigkeit von gcusp (Morovic, 1998) Sie behält die wahrgenommene Farbton Konstante bei, z. b. Hue Angle in Hue korrigiert und verwendet eine generische (Bild unabhängige) sigmoidal-Helligkeit-Skalierung, die auf eine vom Chroma abhängige Weise und eine 90-Prozent-Knie-Funktion Chroma angewendet wird. Die Variante wird entlang konstanter Helligkeit skaliert.

### <a name="the-case-of-single-gamut-shell"></a>Die Groß-/Kleinschreibung einer einzelnen Farbskala-Shell

Es ist hilfreich, den Algorithmus zu überprüfen, wenn sowohl die Quell-als auch die Ziel-gbds nur eine Farbskala-Shell haben. In diesem Fall besteht der Algorithmus aus den folgenden Berechnungen.

Führen Sie zuerst mit der folgenden Formel eine anfängliche Helligkeit-Zuordnung durch:

![Zeigt die Formel für die anfängliche Helligkeit-Zuordnung an.](images/gmmp-image012.png) (1)

Dabei ist *j ₒ* die ursprüngliche Helligkeit, und *j <sub>R</sub>* ist die Helligkeit der Reproduktion.

![Zeigt die zweite Helligkeit für die Helligkeit-Zuordnung an.](images/gmmp-image014.png) (2)

Wenn die Quell Spiel Grenze monochrom ist, wird der Chroma-Wert für die monochrome-Grenze aufgrund der neutralen Achsen Ausrichtung auf 0 (null) gesetzt. Dies führt zu einem degenerierten Fall, bei dem C gleich 0 (null) ist. In diesem Fall wird *p <sub>C</sub>* auf 1 festgelegt.

*p <sub>C</sub>* ist ein Chroma-abhängiger Gewichtungsfaktor (Morovic, 1998), der vom Chroma der ursprünglichen Farbe abhängt, C und *J <sub>S</sub>* sind das Ergebnis der ursprünglichen Helligkeit, die mithilfe einer sigmoidal-Funktion zugeordnet wird.

 

Zum Berechnen von *J <sub>S</sub>* (braun und Fairchild, 1999) wird zunächst eine eindimensionale Nachschlage Tabelle (LUT) zwischen ursprünglicher und Reproduktions Werten für die Reproduktion festgelegt.

![Zeigt eine Formel zur Berechnung von J s an.](images/gmmp-image016.png) (3)

Dabei sind x ₀ und S der Mittelwert und die Standardabweichung der normalen Verteilung und *i* = 0, 1, 2... *m*,*m* ist die Anzahl von Punkten, die im LUT verwendet werden. *S <sub>i</sub>* ist der Wert der kumulativen normalen Funktion für *i*  / *m* Prozent. Die Parameter hängen von der Leichtigkeit des schwarzen Punkts der Reproduktion ab und können aus Tabelle 1 interpoliert werden. Ausführliche Informationen zum Berechnen dieser Parameter finden Sie unter braun und Fairchild (1999, p). 391).

:::row:::
    :::column:::
        J <sub>minout</sub>
    :::column-end:::
    :::column:::
       5.0
    :::column-end:::
    :::column:::
        10.0
    :::column-end:::
    :::column:::
        15.0
    :::column-end:::
    :::column:::
        20.0
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        x ₀
    :::column-end:::
    :::column:::
       53,7
    :::column-end:::
    :::column:::
        56,8
    :::column-end:::
    :::column:::
        58,2
    :::column-end:::
    :::column:::
        60,6
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        E
    :::column-end:::
    :::column:::
       43.0
    :::column-end:::
    :::column:::
        40.0
    :::column-end:::
    :::column:::
        35.0
    :::column-end:::
    :::column:::
        34,5
    :::column-end:::
:::row-end:::


**Tabelle 1** : Berechnung der Berechnung von basicphoto-Helligkeit-Parametern

Um s als eine Helligkeit-Zuordnung (s, <sub>LUT) zu</sub> verwenden, muss Sie zunächst in den Bereich für die Helligkeit von 0100 normalisiert werden \[ \] . Die normalisierten Daten werden dann in den dynamischen Bereich des Zielgeräts skaliert, wie in Gleichung 4 dargestellt, wobei *j*<sub>Min \ *out*</sub> und *j*<sub>Max \ *out*</sub> die Werte der Helligkeit des schwarzen und des weißen Punkts des Reproduktions Mediums sind.

![Zeigt die Formel für S als eine Helligkeit-Zuordnung an.](images/gmmp-image018.png) (4)

An diesem Punkt können die *J s* -Werte aus dem S- <sub>LUT</sub> abgerufen werden, indem zwischen den *m* Punkten der entsprechenden *j O* -und *j S* -Werte interpolieren und die folgende Gleichung als Eingabe verwendet wird.

![Zeigt die Formel zum Abrufen der J S-Werte.](images/gmmp-image020.png) (5)

J <sub>Minin</sub> ist der Wert für die Helligkeit des schwarzen Punkts des ursprünglichen Mediums, j <sub>Maxin</sub> ist der Helligkeit-Wert des weißen Punkts des ursprünglichen Mediums, und j <sub>O</sub> ist die ursprüngliche Helligkeit. Zum späteren Zeitpunkt können Sie angeben, dass die sigmoidal-Funktion *in der eben* beschriebenen Weise definiert ist, wie in der folgenden Abbildung 4 dargestellt.

![Diagramm, das das Diagramm für die Chroma-Zuordnung entlang konstanter Helligkeit anzeigt.](images/gmmp-image024.png)

**Abbildung 4** : Chroma-Zuordnung entlang konstanter Helligkeit

Zweitens: Wenn die Ziel-Spiel Grenze "Chromatisch" ist, komprimieren Sie Chroma entlang der Linien der Konstanten Helligkeit (l), und führen Sie die Komprimierung wie folgt aus.

![Zeigt die Formel zum Durchführen der Chroma-Komprimierung.](images/gmmp-image026.png)  (6)

wobei *d* den Abstand von *E* in *l* darstellt. *g* stellt die Grenze für das mittlere Spiel dar. *r* stellt die Reproduktion dar. und *o* die ursprüngliche Abbildung 5.

![Diagramm, das das Diagramm für die Chroma-und die Helligkeit-Komprimierung in basicphoto anzeigt.](images/gmmp-image028.png)

**Abbildung 5** : Chroma-und Helligkeit-Komprimierung in basicphoto

Wenn die Ziel-Farbskala-Grenze monochrom ist, wird der Chroma-Wert auf 0 (null) gekürzt.

Verwenden Sie als drittes einen mincd-Clip (weiter oben beschrieben), um einen beliebigen Restfehler auszuschließen.

### <a name="black-enhancement"></a>Schwarze Erweiterung

Der vorherige Algorithmus kann geändert werden, um die schwarze zu verbessern, wenn das Ziel ein Druckergerät ist. Das Problem ist mit der Wahl von *J <sub>minout</sub>* zu tun, was in der Regel nicht der dunkelsten Farbe entspricht, die ein Drucker verursachen kann.

Genauer gesagt, ist die Farbe mit der höchsten Dichte, die durch das Platzieren von 100-Prozent-Inks (oder der maximalen möglichen Abdeckung, wenn die GCR-/Freihand-Begrenzung aktiviert ist), in der Regel nicht "neutral" im Farbdarstellung-Raum. Siehe Abbildung 6. Anders ausgedrückt: Wenn eine neutrale minimale Helligkeit für das Zielgerät verwendet wird, wird die erstellte Helligkeit Scaler einer minimalen Helligkeit zugeordnet, die nicht die höchste Dichte ist, die durch den Drucker erreicht werden kann. Beachten Sie den weiteren Anwendungsfall von Monitor auf Drucker. Der Monitor schwarz, R = G = B = 0, wird dann als nicht die höchste Dichte ausgegeben. Die Auswirkung auf die Bildqualität ist, dass es eine fehlende tiefe und einen Kontrast gibt.

![Diagramm, das zeigt, wie der schwarze Punkt des Geräts dunkler als die neutrale minimale Helligkeit sein könnte.](images/gmmp-seqfigure01.png)

**Abbildung 6** : der schwarze Punkt des Geräts ist möglicherweise dunkler als die neutrale minimale Helligkeit.

Angenommen, das Ziel "Schwarzes Gerät" des Geräts ist jkakbk/jkckh k. Wenn C k nicht 0 (null) ist, ist der schwarze Punkt des Geräts relativ zu CAM02 nicht neutral. Wenn Sie J k für das Ziel "neutrale minimale Helligkeit" in der Konstruktion der Helligkeit Scaler verwenden, Das heißt, es wird festgelegt

*J <sub>minout</sub> = JK*

und Sie auf die quellcodeshell anwenden, rufen Sie die in Abbildung 7 dargestellte Konfiguration ab. In der Abbildung entspricht die Hue-Ebene h k.

![Diagramm, das die geänderte Helligkeit Scaler mit dem Ziel Gerät Black Point anzeigt.](images/gmmp-seqfigure02.png)

**Abbildung 7** : Geometrie mit der geänderten Helligkeit Scaler mit dem Ziel Gerät Black Point

Damit der nachfolgende Chroma-Komprimierungs Algorithmus fortgesetzt werden kann, sollten Sie die maximalen und minimalen lightlichkeiten in den Quell-und Ziel Shells ausrichten. Dies kann erreicht werden, indem Sie die zielshell zwischen J <sub>neutralmin</sub> und j k anpassen, indem Sie die Punkte nach links verschieben. Außerdem muss diese Transformation auf den gesamten Speicherplatz des Speicherplatzes angewendet werden, nicht nur auf die Hue-Ebene, die h k entspricht.

Die Transformation ist

![Zeigt die Formel für die Transformation an.](images/gmmp-seqfigure03.png)

Abbildung 8 zeigt die Auswirkung der Transformation.

![Diagramm, das die Auswirkung der geänderten Helligkeit Scaler mit dem Ziel Gerät Black Point anzeigt.](images/gmmp-seqfigure04.png)

**Abbildung 8** : Geometrie mit der geänderten Helligkeit Scaler mit dem Ziel Gerät Black Point

Nachdem Sie den üblichen Chroma-Komprimierungs Algorithmus angewendet haben, muss der Punkt "zurück verschoben" werden, d. h., die umgekehrte Transformation muss angewendet werden, um die endgültige zugeordnete Farbe zu erhalten.

![Zeigt die Formel für die umgekehrte Transformation zum Abrufen der endgültigen zugeordneten Farbe an.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>Die Groß-/Kleinschreibung von dualer Farbskala Shells

Ziel ist es, SIG- \_ Knie für eine einzelne Farbskala-Shell zu generalisieren, wenn das Quellgerät Gbd oder das Ziel Gerät Gbd eine zwei-Shellstruktur aufweist. Die innere Shell wird als verweisshell bezeichnet, während die äußere Shell als plausible Shell bezeichnet wird. Sie sollten die folgenden Fälle in Erwägung gezogen werden.

(a) sowohl die Quell-als auch die Ziel-Gbd haben eine zwei-Shellstruktur.

(b) der Quell-Gbd hat eine zwei-Shellstruktur. die Ziel-Gbd verfügt nur über eine Shell.

(c) der Quell-Gbd hat nur eine Shell. die Ziel-Gbd verfügt über eine zwei-Shellstruktur.

(d) sowohl die Quell-als auch die Ziel-Gbd verfügen nur über eine Shell.

Case (d) ist die Groß-/Kleinschreibung der einzelnen Farbskala-Shell, die bereits erläutert wurde. In Fällen (a), (b) und (c) können Sie das Neuskalieren der Helligkeit verallgemeinern, um die zusätzlichen Informationen aus der Dual Shell-Struktur zu verwenden. In Fällen (b) und (c), in denen entweder die Quelle oder das Ziel nur eine Shell aufweist, führen Sie eine "induzierte verweisshell" ein, die im nachfolgenden Abschnitt "induzierte verweisshell" erläutert wird. Der allgemeine Algorithmus für zwei Shells wird für Case (a) beschrieben. Nachdem die Erstellung der induzierten Verweis Shell erläutert wurde, kann der Algorithmus auch auf Case (b) und (c) angewendet werden. Wie bei der Chroma-Komprimierung wird das Komprimierungs Verhältnis durch die größten verfügbaren Shells bestimmt. Anders ausgedrückt: Wenn sowohl die plausible Shell als auch die verweisshell verfügbar sind, wird die plausible Shell verwendet. Andernfalls wird die verweisshell verwendet.

*Allgemeine Helligkeit-Neuskalierung*

Das vorhanden sein von zwei Shells für Quell-und Ziel-Gbd bedeutet, dass Sie einen Satz von vier Punkten aus dem Quell-Gbd einem entsprechenden Satz in der Ziel-Gbd zuordnen müssen.

![Zeigt, wie ein Satz von vier Punkten einem entsprechenden Satz zugeordnet wird.](images/gmmp-image030.png)

Die Indizes haben die folgenden Bedeutungen.

o oder r: "Original" (Quelle) oder "Reproduktion" (Ziel)

min oder Max: minimale neutrale Helligkeit oder maximale neutrale Helligkeit

Pla oder Ref: plausible Shell oder verweisshell

Die Reihenfolge in jedem Viereck ist auch die erwartete relative Größe dieser Punkte.

Das Bild für die Helligkeit-Neuzuordnung verwendet die gleichen ersten beiden Gleichungen wie die einzige Shell, aber *J S* wird wie folgt auf eine Weise definiert.

![Zeigt die Formel für J S in einer schrittweisen Weise an.](images/gmmp-image032.png) (7)

Dies bedeutet, dass es sich um eine Signatur in der verweisshell handelt und lineare außerhalb von. Weitere Informationen in Abbildung 9.

![Diagramm, das ein Diagramm für die Funktion für die Helligkeit-Neuskalierung für zwei-Shell-gbds anzeigt.](images/gmmp-image033.png)

**Abbildung 9** : Funktion zum Neuskalieren für zwei-Shell-gbds

**induzierte verweisshell**

Wenn ein Gbd über eine Shell verfügt und die andere Gbd über zwei Shells verfügt, müssen Sie eine "verweisshell" für die Gbd mit nur einer Shell erstellen. Die vorhandene Shell, die als verweisshell bezeichnet wird, wird in die "plausible Shell" geändert. Tatsächlich müssen Sie keine Shell im vollständigen Speicherplatz erstellen. Da die Helligkeit nur *j Max* und *j min* verwendet, müssen Sie diese Werte nur für die induzierte verweisshell erstellen. Es gibt zwei Fälle, je nachdem, welcher Gbd über zwei Shells verfügt.

Fall 1: Quell-Gbd hat zwei Shells. Ziel-Gbd verfügt über eine Shell.

Ermitteln der durch das Ziel verursachten verweisshell auf der neutralen Achse Das heißt, j <sub>r, \ min, \ Ref</sub> und j <sub>r, \ Max, \ Ref</sub> der Shell. Dies erfolgt mithilfe des folgenden Algorithmus.

![Zeigt den Algorithmus zum Ermitteln der durch das Ziel veranlassten verweisshell.](images/gmmp-induced01.png)

Die Faktoren? <sub>niedrig</sub> und? <sub>hohe</sub> Kontrolle der Trennung zwischen der plausibler Shell und der verweisshell. Der Wert 1 bedeutet, dass die Werte für j <sub>Min</sub> -Werte oder j m ₐ ₓ übereinstimmen. Ihre Werte werden aus der quellverweisshell und der Quell-Quellcode-Shell "induziert".

![Zeigt die Formel für die Werte der quellverweisshell und die plausible Quell-Shell.](images/gmmp-induced02.png)

Die "Fudge Factors" f <sub>Low</sub> und f <sub>High</sub> sind *anpassbare Parameter* , die zwischen 0 und 1 liegen müssen. Wenn der Wert 0 ist, werden die j <sub>Min</sub> -oder j m ₐ ₓ direkt aus den Quell Shells abgeleitet. Wählen Sie in diesem Fall f <sub>Low</sub> = 0,95 und f <sub>High</sub> = 0,1 aus.

Fall 2: Quell-Gbd hat eine Shell. Ziel-Gbd verfügt über zwei Shells.

Ermitteln der durch Quelle verursachten verweisshell auf der neutralen Achse; Das heißt, j <sub>o, \ min, \ Ref</sub> und j <sub>o, \ Max, \ Ref</sub> der Shell. Dies erfolgt mithilfe des folgenden Algorithmus.

![Zeigt den Algorithmus zum Ermitteln der durch das Ziel veranlassten verweisshell auf der neutralen Achse.](images/gmmp-induced03.png)

Die Faktoren? <sub>niedrig</sub> und? <sub>hohe</sub> Kontrolle der Trennung zwischen der plausibler Shell und der verweisshell. Der Wert 1 bedeutet, dass die Werte für j <sub>Min</sub> -Werte oder j m ₐ ₓ übereinstimmen. Ihre Werte werden aus der quellverweisshell und der Quell-Quellcode-Shell "induziert":

![Zeigt den Algorithmus zum Steuern der Trennung zwischen der referenzshell und der kryptografiequellshell.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Gründe für Änderungen von den Cie TC8-03-Empfehlungen

Basicphoto unterscheidet sich in den folgenden Punkten von den Cie TC8-03-Empfehlungen.

1.  Chroma wird nicht in Bezug auf den Cusp komprimiert, sondern entlang konstanter Helligkeit.
2.  Der Bereich Helligkeit verwendet die Helligkeit der dunkelsten Farbe im Spielbereich anstelle des Punkts, an dem die Spiel Grenze die neutrale Achse überschreitet.
3.  Basicphoto unterstützt sowohl eine Referenz-Farbskala-Shell als auch eine plausible Farbskala-Shell, wenn eine der beiden beiden Shells über zwei Shells verfügt.
4.  Basicphoto verwendet CIECAM02; anstatt CIECAM97s zu verwenden, um 400 cd/m2 in D65 zu konvertieren, und verwenden Sie dann den "rit IPT"-Farbraum.

Die erste Änderung wurde vorgenommen, um Probleme bei der inversierung von Tone zu vermeiden, die bei der Verwendung der Komprimierung für eine Cusp auftreten Wie in Abbildung 10 dargestellt, kann die Cusp-Komprimierung zu Ton Versionen führen. Dies kann vorkommen, wenn Farben von hohem Chroma heller sind als Farben von niedrigerem Chroma. Da sgck jedes Pixel unabhängig in Helligkeit und Chroma komprimiert, ist es nicht garantiert, dass die Helligkeit-Beziehung zwischen den Pixelwerten nach der Komprimierung erhalten bleibt. Der Nachteil dieser Entscheidung für die Komprimierung in Linien konstanter Helligkeit besteht darin, dass Sie Verluste von Chroma erleiden können, insbesondere in Bereichen, in denen die Ziel Spiel Grenze sehr flach ist, was bei hellen gelbwerten der Fall ist.

![Diagramm, das die von sgck verursachte toninversion anzeigt.](images/gmmp-toneinversion.png)

**Abbildung 10** : durch sgck verursachte toninversion

![Zeigt ein ursprüngliches Bild von einer "Teapot" an.](images/originalteapot.jpg)![Zeigt das sgck-Ergebnis des Teekanne-Bilds an.](images/badteapot.jpg)![Zeigt das basicphoto-Ergebnis des "Teekanne"-Bilds an.](images/betterteapot.jpg)

**Abbildung 11** : Ursprüngliches Bild, sgck-Ergebnis und basicphoto-Ergebnis

In Abbildung 11 wird diese toninversion veranschaulicht. Auf der linken Seite befindet sich ein ursprüngliches Bild, das von einer digitalen Kamera erfasst wurde. in der Mitte ist das Bild wie von sgck reproduziert. und auf der rechten Seite das Bild wie von basicphoto reproduziert. Das Bild auf der linken Seite befindet sich im Farbraum der digitalen Kamera, das Mittelpunkt und das rechte Bild befinden sich im Farbraum einer LCD-Videoanzeige. In der ursprünglichen Abbildung ist der obere Teil der "Teekanne" dunkler als der untere Teil, da der untere Teil das tableklo reflektiert, auf dem es sich befindet. Im sgck-Bild ist der obere Teil aufgrund der toninversion tatsächlich heller als der untere Teil. Außerdem ist es schwierig, die Elemente im unteren Teil von "Teapot" anzuzeigen. Auf der rechten Seite hat basicphoto den Ton Inversion korrigiert, und die reflektierten Artikel sind deutlicher zu unterscheiden.

Die zweite Änderung wurde vorgenommen, um die Reproduktion von nahezu schwarzen Farben auf Druckern zu verbessern, bei denen der schwärzeste schwarze nicht direkt auf die CIECAM02 neutrale Achse fällt. Die folgende Abbildung 12 zeigt ein Bild, das in sRGB konvertiert wurde. für einen RGB-Inkjet-Drucker mit sgck reproduziert und mit basicphoto für denselben Drucker reproduziert. Das Bild in der Mitte verwendet nicht das vollständige schwarze Gerät, und daher fehlt der Kontrast in der ursprünglichen. Der Kontrast wird mit basicphoto wieder hergestellt.

![Zeigt das ursprüngliche Bild eines Playsets an.](images/playstructure.jpg)![Zeigt das Bild des Playsets, das für einen R G B-Inkjet-Drucker mithilfe von sgck reproduziert wurde.](images/playstructurebad.jpg)![Zeigt das Bild des für einen R G B-Inkjet-Drucker mithilfe von basicphoto neu gegebenen Playsets an.](images/betterplaystructure.jpg)

**Abbildung 12** : Verbessertes Schwarzes

Die dritte Änderung wurde vorgenommen, um die Farb Reproduktion für digitale Kameras zu verbessern. Insbesondere in Fällen, in denen die Profilerstellung für die digitale Kamera mithilfe eines Verweis Ziels durchgeführt wurde, enthält eine in den gemessenen Farben aufgebaute Beschreibung der Beschreibung des Farb verlauforts möglicherweise nicht alle Farben, die in einer realen Szene aufgezeichnet werden könnten. Anstatt alle Farben auf die Größe des gemessenen farbziels zu kürzen, können Sie mit der extrapolierungs Grenze eine plausible Spiel Grenze schaffen. Der basicphoto-Algorithmus ist so konzipiert, dass er eine derart extrapolierte Spiel Grenze unterstützt.

Die vierte Änderung wurde vorgenommen, da CIECAM02 gut für die Zuordnung von Farbskala funktioniert. Der Prozess, der von TC8-03 zum Umrechnen von Geräte Farben in D65 bei 400 cd/m2 und anschließende Verwendung des "rit IPT"-Farbraum empfohlen wird, ist Rechen intensiv und zeitaufwändig.

### <a name="hue-mapping"></a>Hue-Zuordnung

Huemap entspricht der Absicht der IStGH-Sättigung.

Wenn die Quell-oder Ziel-Farbskala-Grenze keine primär Punkte enthält, wird dieses Modell auf das mincd (relative)-Modell zurückgesetzt, das in einem vorherigen Abschnitt beschrieben wurde. beispielsweise Geräte, für die die primären Replikate nicht bestimmt werden können ("ICC-Profile mit mehr als vier Kanälen") oder Chrome-ICC-Profile.

Dieser Algorithmus passt zuerst den Farbton des Eingabe Farbwerts an. Anschließend werden die Helligkeit und der Chroma mithilfe einer Scheren Zuordnung gleichzeitig angepasst. Schließlich wird der Farbwert durch Clips, um sicherzustellen, dass er sich innerhalb von Gamut befindet.

Der erste Schritt besteht darin, die "Hue Wheels" zu bestimmen. Suchen Sie nach den Jch-Werten für die primäre und die sekundäre Farbe für das Quell-und Zielgerät. Sie berücksichtigen nur die Hue-Komponenten. Dies führt zu einem primären oder sekundären Farbton mit sechs Farbpunkten für jedes Gerät. (Siehe Abbildung 13.)

![Diagramm, in dem die Hue-Räder mit sechs Farbpunkten angezeigt werden.](images/gmmp-figure12.png)

**Abbildung 13** : Hue Wheels

Bessere Ergebnisse können erzielt werden, wenn das blaue Quell primäre Replikat nicht auf das blaue Ziel Ziel gedreht wird. Stattdessen wird der primäre Hue-Farbton als Ziel verwendet.

Führen Sie als nächstes die Farbton Farben für jede Eingabe Farbe aus dem Quell Abbild aus.

a) Wenn Sie den Hue-Winkel der Eingabe Farbe verwenden, bestimmen Sie den Speicherort der Farbe auf dem quellfarbton in Bezug auf die beiden angrenzenden primär-oder Sekundärfarben. Der Speicherort kann als Prozentsatz der Entfernung zwischen den primären Replikaten betrachtet werden. Beispielsweise ist der Eingabe farbfarbton 40 Prozent der Methode vom Farbton-Wert von Magenta bis zum Farbton-Wert rot.

b) suchen Sie auf dem Zielfarbton den entsprechenden Hue-Winkel, z. b. 40 Prozent von Magenta bis rot. Dieser Wert ist der Zielfarbton.

Im allgemeinen befinden sich die Quell Primär-und sekundären Replikate nicht in den gleichen Farbton wie die primären Primär-und sekundären Replikate. Das heißt, der Zielfarbton unterscheidet sich in der Regel vom Quell Farbton Winkel.

Nehmen wir beispielsweise an, dass die Hue-Räder die folgenden Werte ergeben:

Quelle M = 295 Grad, Quelle R = 355 Grad.

Ziel M = 290 Grad, Ziel-R = 346 Grad.

Wenn der Hue-Winkel der Eingabe Farbe 319 Grad beträgt, beträgt er 40 Prozent des Winkels (24 Grad) von der Quelle M bis zur Quelle R. Der Winkel zwischen m und R ist 60 Grad, und der Winkel zwischen m und Eingabe Farbton beträgt 24 Grad. Berechnen Sie den Winkel auf dem Ziel, der 40 Prozent vom Ziel M bis zum Ziel R (22 Grad) ist, sodass der Hue-Winkel der Zielfarbe 312 Grad beträgt.

Berechnen Sie als nächstes die Hue-Bezugspunkte für den quellfarbton und den Zielfarbton. Wenn Sie den Hue-Bezugspunkt für einen bestimmten h-Wert (Hue) berechnen möchten, finden Sie den Wert J (Helligkeit) und C (Chroma).

-   Suchen Sie den j-Wert des Hue-Bezugspunkts durch Interpolation zwischen den j-Werten für die angrenzenden primären oder sekundären Punkte, und verwenden Sie dabei die relative Position von Hue. Beispiel: 40 Prozent in diesem Beispiel.
-   Suchen Sie den maximalen C-Wert mit diesem J-Wert und dem Wert h. Sie verfügen nun über den Jch-Wert des Hue-Bezugspunkts für diesen Farbton.

![Diagramm, das ein Farbton Blatt zeigt.](images/gmmp-figure13.png)

**Abbildung 14** : ein Hue-Blatt (Visualisierung eines Slice-Begrenzungs Slice in einem bestimmten Farbton)

Der nächste Schritt ist die Berechnung der Scheren Zuordnung für jedes Pixel. Visualisieren Sie zunächst ein Farbton Blatt aus dem Quell Spiel für den Farbton der Quellfarbe und ein Farbton Blatt aus dem Ziel-Farbskala für den Zielfarbton, der während der Farbton Drehung berechnet wird. Die Hue-Blätter werden erstellt, indem ein "Slice" von der Jch-Oberfläche für die Obergrenze in einem bestimmten Farbton erstellt wird (siehe Abbildung 14).

Hinweis: aus Gründen der Leistungsoptimierung werden Hue-Blätter nicht erstellt. Sie werden hier nur zu Visualisierungs Zwecken beschrieben und angezeigt. Die Vorgänge werden direkt auf der Oberfläche für die Farbskala-Begrenzung am angegebenen Farbton ausgeführt. Anschließend berechnen Sie die Hue-Verweis Punkte, um die scherungs Zuordnung zu bestimmen.

-   Führen Sie eine Durchführung einer Helligkeit aus, um die schwarzen und weißen Punkte des Quell Blatts dem Ziel Blatt zuzuordnen (siehe Abbildung 15). Die schwarzen und weißen Punkte des Quell Blatt Blatts werden linear zu den schwarzen und weißen Punkten des Ziel-Hue-Blatts zugeordnet, indem alle J-Koordinaten der Quell Grenze skaliert werden. Der Farbton zugeordnete Eingabe Farbwert wird auf die gleiche Weise skaliert.

![Diagramm, das die Helligkeit-Zuordnung anzeigt.](images/gmmp-figure14.png)

**Abbildung 15** : Helligkeit-Zuordnung

-   Bestimmen Sie die Hue-Bezugspunkte für die einzelnen Hue-Blätter. Wenden Sie eine Scheren Zuordnung auf das Quell Blatt an, sodass die Quell-und Ziel Verweis Punkte übereinstimmen (siehe Abbildung 16). Der Bezugspunkt für ein Spiel in einem bestimmten Farbton ist der interpoliert Hue-Referenzpunkt zwischen den angrenzenden primären Replikaten. Der Bezugspunkt des Quell Farbton Blatts wird linear dem Bezugspunkt des Ziel-Hue-Blatts zugeordnet. dabei wird ein "Scheren"-Vorgang verwendet, der die J-Achse sperrt, wobei die schwarzen und die weißen Punkte stationär bleiben. Die schwarzen Punkte, weißen Punkte und Bezugspunkte der Quell-und zielhue sollten übereinstimmen.
-   Wenden Sie die Schere-Zuordnung auf den Wert für die Helligkeit-angepasste Eingabe Farbe an. Die J-und C-Koordinaten des Quell Farbwerts werden proportional zur Entfernung von der j-Achse proportional skaliert.
-   Im nächsten Schritt wird eine feine, von Chroma abhängige Helligkeit-Komprimierung für den J-Wert des Hue-Referenz Punkts auf dem durch Scheren zugeordneten Farbpunkt ausgeführt. Die Komprimierung in Bezug auf Hue Reference j erfolgt in einer Gamma ähnlichen Weise, bei der weiß, schwarz, Grays und Punkte auf der Hue-Referenz j nicht betroffen sind. Alle anderen Punkte neigen in gewisser Weise den Farbton Verweis j, was sich in der Nähe des Hue-Verweises j, mit der verbleibenden Chroma-Konstante, geringfügig nach oben bewegt. Die Chroma-Abhängigkeit gewährleistet, dass neutrale Farben nicht betroffen sind, und der Effekt erhöht sich bei Farben mit höherem Chroma.

Im folgenden finden Sie eine mathematische Beschreibung der Helligkeit-Komprimierung in Bezug auf den Hue-Verweis J oder die Anpassung des J-Werts des Ziel Punkts. Sie wird als Zielpunkt bezeichnet, da Sie im Ziel-Gamut eine Schere zugeordnet wurde.

Berechnen Sie zuerst "factorc" (Chroma-Abhängigkeits Faktor) für den Zielpunkt, der bestimmt, wie viele Auswirkungen die Helligkeit-Komprimierung hat. Punkte in der Nähe von oder auf der J-Achse haben nur wenig oder keine Komprimierung. für Punkte, die weiter Weg von der J-Achse (High-Chroma) liegen, wird eine höhere Komprimierung angewendet. Multiplizieren Sie um 0,5, um sicherzustellen, dass factoric kleiner als 1 ist, da es möglich ist, dass sourcec etwas größer als referencec ist, aber nicht doppelt so groß ist.

facktorc = (destinationc/referencec)? 0.5

Dabei gilt:

destinationc ist der C-Wert des Ziel Punkts.

referencec ist der C-Wert des Hue-Referenz Punkts.

Legen Sie als nächstes fest, ob sich der Zielpunkt j oberhalb oder unterhalb des Hue-Verweises j befindet. Wenn dies der Fall ist, gehen Sie wie folgt vor:

1.  Compute "Factor" für den Zielpunkt relativ zum referencej. Dieser Factor-Wert liegt zwischen 0 und 1 (0 bei referencej; 1, wenn bei maxj).
2.  factorij = (destinationj-referencej)/(maxj-referencej)

    Dabei gilt:

    destinationj ist der J-Wert des Ziel Punkts.

    referencej ist der J-Wert des Hue-Referenz Punkts.

    maxj ist der maximale J-Wert des Gamut.

3.  Wenden Sie eine Gamma ähnliche Power-Funktion auf factorj an, wodurch factorj um eine bestimmte Menge reduziert wird. In diesem Beispiel wird die Potenz von 2 (dem Quadrat) verwendet. Subtrahieren Sie den reduzierten Faktor vom ursprünglichen Faktor, und multiplizieren Sie das Ergebnis mit dem gesamten J-Bereich oberhalb der primären referencej, um nach der "Delta-" zu suchen, die die Änderung in j nach der Helligkeit-Komprimierung, jedoch nicht mit der Chroma-Abhängigkeit darstellt.
4.  Delta = (Factor j-(Factor) facktorj))? (maxj-referencej)

5.  Wenden Sie Factor auf das Delta (je höher das Chroma, je größer die Auswirkung) an, und berechnen Sie den neuen J-Wert für den Zielpunkt.
6.  destinationj = destinationj-(Delta? facktorc)

Wenn der Wert für "j-Value" für den Zielpunkt unterhalb von "referencej" liegt, wird eine ähnliche Berechnung der vorangehenden Schritte a-C durchgeführt, wobei minj anstelle von maxj verwendet wird, um den Bereich in J zu ermitteln, in dem die facrenj berechnet werden soll, und die Polarität der Vorgänge "unterhalb" der referencej zu berücksichtigen.

factorij = (referencej-destinationj)/(referencej-minj)

Delta = (Factor j-(Factor) facktorj))? (referencej-minj)

destinationj = destinationj + (Delta? facktorc)

Dabei gilt:

minj ist der minimale J-Wert des Gamut.

Die Chroma für Eingabe Farbpunkte wird linear (sofern möglich) entlang konstanter Helligkeit erweitert, proportional zum maximalen Chroma-Wert der Quell-und Ziel-Gamuts an diesem Farbton und der Helligkeit. In Kombination mit der vorangehenden Chroma-abhängigen Helligkeit-Komprimierung wird dadurch die Sättigung bewahrt, da bei der Scheren Zuordnung mit den Verweis Punkten mitunter der Quellpunkt in Chroma überkomprimiert wird (siehe Abbildung 16).

![Diagramm, das die zu Übereinstimmungs ung von Hue-Verweis Punkten vor der Schecke auf der rechten Seite anzeigt.](images/gmmp-shearmapping.png)

**Abbildung 16** : Scheren Zuordnung, Helligkeit-Komprimierung in Richtung Hue Reference J und Chroma-Erweiterung

Im folgenden finden Sie eine mathematische Beschreibung des Chroma-Erweiterungsprozesses, oder Sie passen den C-Wert des Ziel Punkts an. Es wird als Zielpunkt bezeichnet, da es eine Schere zugeordnet wurde und die Helligkeit in den Ziel Gamut komprimiert wurde.

1.  Stellen Sie vor der Scheren Zuordnung sourceextentc (den Block "Chroma" bei Helligkeit und Farbton des Quell Punkts).
2.  Nachdem die schof-und die Helligkeit-Komprimierung den Quellpunkt in den Zielpunkt transformiert haben, bestimmen Sie den Wert für "destextentc" (der Chroma-Wertebereich mit Helligkeit und Farbton des Ziel Punkts).
3.  Wenn die sourceextentc-Datei größer ist als der destextentc, ist keine Chroma-Anpassung am Zielpunkt erforderlich, und Sie können den nächsten Schritt überspringen.
4.  Passen Sie destinationc (der Chroma des Ziel Punkts) so an, dass er mit dieser Helligkeit und dem Farbton in den Zielbereich für den Bereich passt.
5.  destinationc = destinationc? (destextentc/sourceextentc)

    Dabei gilt:

    destinationc ist der Ziel Punkt C-Wert.

    sourceextentc ist der maximale C-Wert des Quellcodes bei Helligkeit und Farbton des Quell Punkts.

    destextentc ist der maximale C-Wert des Ziel gamels mit Helligkeit und Farbton des Ziel Punkts.

Führen Sie schließlich das imimumentfernungs Clipping aus. Wenn die Eingedrehte, von Helligkeit angepasste und mit der Stift zugeordnete Eingabe Farbe weiterhin etwas außerhalb des Ziel gamels liegt, schneiden Sie Sie (verschieben) an den nächstgelegenen Punkt an der Ziel-Spiel Grenze aus (siehe Abbildung 17).

![Diagramm, das das minimale Entfernungs Clipping anzeigt.](images/gmmp-figure15.png)

**Abbildung 17** : minimaler Entfernungs Clipping

## <a name="gamut-boundary-description-and-gamut-shell-algorithms&quot;></a>Beschreibung von Gamut-Grenzen und Gamut-shellalgorithmen

Die Funktion &quot;Geräte-Farbskala-Begrenzung&quot; verwendet die Gerätemodell-Engine und die analytischen Parameter, um eine Farb Geräte-Spiel Grenze abzuleiten, die als indizierte vertexliste der Hülle des Geräte gamzes beschrieben wird. Die Hülle wird unterschiedlich berechnet, je nachdem, ob Sie mit Additiven Geräten arbeiten, wie z. b. Monitoren, Projektoren oder subtraktive Geräte. Die indizierte Vertex-Liste wird in ciejab gespeichert. Die Struktur der indizierten Vertex-Liste ist für die Hardwarebeschleunigung durch DirectX optimiert.

Dieser Ansatz verfügt über viele bekannte Lösungen. Wenn Sie im Web nach &quot;anvexen Hülle DirectX&quot; suchen, erhalten Sie mehr als 100 Treffer. Beispielsweise gibt es in diesem speziellen Thema einen Verweis von 1983 (Computer Grafik Theorie und-Anwendung, &quot;shiphulls, b-Spline-Oberflächen und CADCAM&quot;, &quot;PP. 34-49") mit Verweisen von 1970 bis 1982 im Thema.

Die Sammlung der Punkte kann aus extern verfügbaren Informationen wie folgt ermittelt werden:

-   Punkte für die verweisshell für Monitore werden mithilfe einer Stichprobe des farbcubes im Colorant-Raum des Geräts generiert.
-   Punkte für die Referenz-Shell für Drucker und Erfassungsgeräte werden aus den Beispiel Daten abgerufen, die zum Initialisieren des Modells verwendet werden.
-   Punkte für die Referenz-Shell für ScRGB und sRGB werden mithilfe einer Stichprobe des farbcubes für sRGB generiert.
-   Punkte für die plausible Shell für Erfassungsgeräte werden mithilfe einer Stichprobe des farbcubes im Colorant-Raum des Geräts generiert.
-   Punkte für die verweisshell für Projektoren werden mithilfe einer Stichprobe eines Polyhedron im farbcube im Colorant-Raum des Geräts generiert.
-   Punkte für die mögliche Shell für Breite dynamische Bereichs Farbraum werden mithilfe einer Stichprobe des farbcubes im eigentlichen Bereich generiert.

Sie können eine Scheitelpunkt Liste erstellen, in der das Farb Geräte Spiel mit einem Geräte Profil und System Supportdiensten effizient beschrieben wird.

Für Ausgabegeräte beschreibt die Roaminggrenze den Bereich von Farben, die vom Gerät angezeigt werden können. Eine Spiel Grenze wird aus denselben Daten generiert, die zum Modellieren des Verhaltens des Geräts verwendet werden. Konzeptionell geben Sie eine Stichprobe des Bereichs von Farben aus, die das Gerät erzeugen kann, messen die Farben, konvertieren die Messungen in Darstellungs Raum und verwenden dann die Ergebnisse zum Erstellen der spielbegrenzung.

Eingabegeräte sind kniffliger. Jedes Pixel in einem Eingabebild muss über einen Wert verfügen. Jedes Pixel muss in der Praxis eine beliebige Farbe darstellen können, die in der realen Welt gefunden wurde. In diesem Sinne sind keine Farben für ein Eingabegerät "nicht im Spiel", da Sie immer dargestellt werden können.

Alle digitalen Bildformate haben einen dynamischen Bereich mit fester Größe. Aufgrund dieser Einschränkung sind immer einige unterschiedliche Reize vorhanden, die dem gleichen digitalen Wert zugeordnet werden. Daher ist es nicht möglich, eine eins-zu-Eins-Zuordnung zwischen realen Farben und digitalen Kamera Werten herzustellen. Stattdessen wird die Spiel Grenze gebildet, indem eine Reihe von echten Farben geschätzt wird, die die digitalen Reaktionen der Kamera liefern können. Sie verwenden diesen geschätzten Bereich als Farbskala für das Eingabegerät.

Primäre Replikate sind enthalten, um die Zuordnung von Geschäftsgrafiken zu ermöglichen.

In der objektorientierten Art "true" abstrahieren Sie die zugrunde liegende Darstellung der Farbskala-Grenze. Dies ermöglicht Ihnen die Flexibilität, die Darstellung in Zukunft zu ändern. Um die im neuen allgemeinen Tabellen Ausdruck verwendete-Gbd (Farbskala Boundary Deskriptor) zu verstehen, müssen Sie zunächst verstehen, wie Farbskala-Mapping-Algorithmen (gmas) funktionieren. Bisher wurden die gmas so entworfen, dass Sie die Anforderungen der Grafik Grafik-Community erfüllen. Das heißt, um Bilder zu reproduzieren, die bereits ordnungsgemäß für das Gerät gerendert wurden, auf dem das Eingabe Image erstellt wurde. Das Ziel der Graphic Arts-gmas besteht darin, die bestmögliche Reproduktion des Eingabe Abbilds auf dem Ausgabegerät zu ermöglichen. Der neue CTE-Gbd ist so konzipiert, dass vier wichtige Probleme gelöst werden.

Da das Eingabebild für das Eingabegerät gerendert wird, passen alle Farben in den Bereich zwischen den weißen und schwarzen Punkten des Mediums. Angenommen, das Bild ist ein Foto einer Szene, in der es ein diffuses weiß ist, z. b. eine Person in einem weißen Tee-Shirt und eine Glanz Markierung, z. b. ein Licht, das ein Fenster oder eine Chrome-Stoßstange reflektiert. Die Szene wird auf dem Eingabe Medium gerendert, sodass die Glanz Markierung dem weißen Punkt des Mediums zugeordnet ist, und das diffuse weiß wird einer neutralen Farbe zugeordnet, die dunkler ist als der weiße Punkt des Mediums. Die Auswahl der Kartenfarben von der Szene zum Eingabe Medium ist sowohl eine Szenen abhängige Entscheidung als auch eine ästhetische Entscheidung. Wenn die Glanz Markierung in der ursprünglichen Szene fehlt, wird das diffuse weiß wahrscheinlich dem weißen Punkt des Mediums zugeordnet. In einer Szene mit vielen Hervorhebungs Details wird zwischen dem Glanz weißen und dem diffusen weißen Bereich mehr Bereich verbleiben. In einer Szene, in der die Hervorhebung nicht signifikant ist, kann nur sehr wenig Bereich verbleiben.

Bei vorab gerenderten Images ist die Zuordnung von Farbskala relativ unkompliziert. Im Grunde ist der weiße Punkt des ursprünglichen Mediums dem weißen Punkt des Reproduktions Mediums zugeordnet, der schwarze Quellpunkt wird dem Ziel-Schwarzpunkt zugeordnet, und der größte Teil der Zuordnung ist fertiggestellt. Die verschiedenen gmas in der Existenz bieten Variationen für das Mapping anderer Punkte auf der Tonskala des Quell Mediums und verschiedene Möglichkeiten zur Behandlung von Out-of-Gamut-Chroma-Werten. Die Zuordnung von weiß zu weiß und schwarz zu schwarz ist in diesen Variationen jedoch einheitlich. Diese Implementierung erfordert, dass weiß oberhalb von j \* von 50 und schwarz unterhalb von j \* von 50 liegen muss.

Nicht alle Farb Codierungen schränken Farbbereiche für Eingabe Bilder ein. Die IEC-Standard Farbcodierung ScRGB (IEC 61966-2-2) stellt 16 Bits für jeden der drei Farbkanäle rot, grün und blau (RGB) bereit. In dieser Codierung wird der Verweis schwarz nicht als RGB-Triple (0,0) codiert, sondern als (4096, 4096, 4096). Der Verweis weiß wird als (12288, 12288, 12288) codiert. Mithilfe der ScRGB-Codierung können Glanzlichter und Schattendetails dargestellt werden. Sie enthält RGB-Tripel, die nicht physisch möglich sind, da Sie negative Mengen an Licht und Codierungen außerhalb des Cie-Spektral Lokus erfordern. Natürlich kann kein Gerät möglicherweise alle Farben im ScRGB-Gamut liefern. Tatsächlich kann kein Gerät alle Farben liefern, die ein Menschen sehen kann. Die Geräte können also den ScRGB-Farbskala nicht ausfüllen, und es wäre hilfreich, den Teil des gamches darzustellen, den Sie ausfüllen. Jedes Gerät verfügt über einen Bereich von Werten im ScRGB-Speicherplatz, den es verursachen kann. Dies sind die "erwarteten" Farben für das Gerät. Es wäre überraschend, dass das Gerät außerhalb dieses Gamut Farben erzeugt. Es gibt eine definierte Transformation zwischen ScRGB-Speicherplatz und Darstellungs Raum, sodass jedes Gerät auch über einen Bereich von Darstellungs Werten verfügt, die er reproduzieren soll.

Sowohl in ScRGB als auch in der Eingabe von Erfassungs Geräten, die mit einem festgelegten Ziel gekennzeichnet sind, ist es möglich, einen Wert außerhalb des Bereichs der erwarteten Werte zu erhalten. Wenn jemand eine Kamera an ein Testziel kalibriert, und dann eine Szene mit Glanzlichtern aufzeichnet, gibt es möglicherweise Pixel, die heller als der weiße Punkt des Ziels sind. Das gleiche kann passieren, wenn ein auf natürliche Weise auftretendes rot mehr als das rote Ziel ist. Wenn ein Benutzer ein ScRGB-Image von einem Gerät annimmt und dann die Farben im Bild manuell bearbeitet, ist es möglich, Pixel zu erstellen, die außerhalb des erwarteten Bereichs des Geräte gamts liegen, auch wenn Sie sich innerhalb des gesamten ScRGB-Gamut befinden.

Ein zweites Problem ist möglicherweise zunächst mit diesem Problem verknüpft. Dies ist der Fall, wenn Sie ein farbziel verwenden, um ein Eingabegerät zu charakterisieren, z. b. eine Kamera oder einen Scanner. Reflektierenden Ziele werden in der Regel auf Papier erstellt und enthalten eine Reihe farbiger Patches. Manufaturer stellt Datendateien mit Farbmessungen bereit, die unter einer festgelegten Anzeige Bedingung für jeden farbpatch erstellt wurden. Farbprofilerstellungs-Tools erstellen eine Zuordnung zwischen diesen gemessenen Werten und den Werten, die von den Farbsensoren in den Geräten zurückgegeben werden. Das Problem ist, dass diese farbziele häufig nicht den vollständigen Bereich der Geräte Werte abdecken. Beispielsweise gibt der Scanner oder die Kamera möglicherweise den Wert (253, 253, 253) für den Verweis-weißen Punkt zurück, und ein Verweis rotes Patch hat möglicherweise den RGB-Wert (254, 12, 4). Diese stellen den Bereich der erwarteten Werte für das Eingabegerät dar, basierend auf den Zielwerten. Wenn Sie das Eingabegerät basierend auf den Antworten auf das Ziel bezeichnen, werden nur Farben in diesem schmalen Bereich erwartet. Dieser Bereich ist nicht nur kleiner als der Bereich von Farben, den Menschen sehen können, sondern kleiner als der Bereich von Farben, den das Gerät liefern kann.

In beiden Fällen ist es schwierig, die Größe des Eingabe Geräts oder-Bilds zu schätzen, trotz des Vorhandenseins eines Verweises oder von Messungen. Beim ersten Problem ist der plausible Spiel Aufwand für das Eingabegerät niedriger als der gesamte ScRGB-Wert. Beim zweiten Problem ist der Verweis Bereich des Ziels kleiner als der gesamte mögliche Bereich des Eingabe Geräts.

Das dritte Problem betrifft die Tonzuordnung. Viele Modelle von spielgrenzen, die die in der Grafikkunst verwendeten vorgerenderten Bilder adäquat darstellen können, wurden vorgeschlagen, z. b. der braun-und Fairchild Mountain Range Gbd (braun \[ 97 \] ), und der Abschnitt Maxima-Begrenzungs Deskriptor (Morovic 98) von Morovic \[ \] . Diese Modelle enthalten jedoch nur Informationen zu den extremen des Geräts. Ihnen fehlen Informationen zu anderen Punkten in der klanglichen Zuordnung. Ohne diese Informationen können gmas nur grobe Schätzungen der optimalen Ton Zuordnung erstellen. Schlimmer noch: diese Modelle bieten keine Hilfe für den erweiterten dynamischen Bereich in ScRGB und in digitalen Kamerabildern.

Wie wird dieses Problem in der Fotobranche gelöst? Die Kamera erfasst ein Bild. Experten könnten erörtern, wie viel Rendering im Erfassungsgerät auftritt. Sie stimmen jedoch zu, dass es sich nicht um einen signifikanten Betrag handelt. Beide Technologien ordnen kein diffuses weiß in einer erfassten Szene dem weißen Punkt des Mediums zu. Ebenso wird der schwarze Punkt nicht aus der Szene dem schwarzen Punkt des Mediums zugeordnet. Das Verhalten von Fotofilmen wird unter Dichte Raum mithilfe einer charakteristivenkurve beschrieben, die oft als Hurter und Driffield bezeichnet wird, oder H&D-Kurve. Die Kurve zeigt die Dichte der ursprünglichen Szene und die resultierende Dichte für den Film an. Abbildung 18 zeigt eine typische H-&D-Kurve. Die x-Achse stellt eine erhöhte Protokoll Präsenz dar. Die y-Achse stellt die Dichte auf der Folie dar. Fünf Verweis Punkte werden in der Kurve markiert: schwarz ohne Detail, das die minimale Dichte im negativen darstellt. schwarz mit Detail; Verweis Mid-graue Karte; weiß mit Detail; und weiß ohne Detail. Beachten Sie, dass Leerzeichen zwischen schwarz ohne Detail (das schwarz dargestellt werden) und schwarz mit Detail (Schatten schwarz) vorhanden ist. Ebenso gibt es Leerraum zwischen weiß mit Detail (diffuses weiß) und weiß ohne Detail (steht für das weiß des Geräts).

![Diagramm, das die H-und D-Kurve für FolienFolie anzeigt.](images/gmmp-image079.png)

**Abbildung 18** : H&D-Kurve für FolienFolie

Die Videobranche liefert "Headroom&quot; und &quot;fooorial&quot; in Bildern. In der ITU 709-Spezifikation wird die Leuchtkraft (&quot;Y") in 8 Bits mit einem Bereich von 0 bis 255 codiert. Allerdings wird der Verweis schwarz bei 15 codiert und der Verweis weiß als 235 codiert. Dadurch bleibt der Codierungs Bereich zwischen 236 und 255, um Glanzlichter darzustellen.

Die Videobranche stellt ein im wesentlichen geschlossenes Schleifen System dar. Obwohl es viele verschiedene Gerätehersteller gibt, basieren Videosysteme auf Referenz Geräten. Es gibt eine Standard Codierung für Videobilder. Es ist nicht erforderlich, eine Spiel Grenze mit Videobildern zu kommunizieren, da alle Bilder für die Reproduktion auf demselben Referenzgerät codiert sind. Der Film ist auch eine geschlossene Schleife, da zwischen den verschiedenen Komponenten keine zwischen Daten vermittelt werden müssen. Sie benötigen eine Lösung, die Bilder von Geräten mit unterschiedlichen Gamuts ermöglicht und sowohl vorab gerenderte als auch ungerenderte Szenen darstellt, die bei der Ausgabe mit unterschiedlichen Gamuts reproduziert werden.

Ein viertes Problem, das durch den neuen allgemeinen Tabellen Ausdruck gelöst werden muss, besteht darin, dass die von einem Gerät erzeugten visuellen Farben, z. b. wenn rot = grün = blau, bei einem Monitor häufig nicht auf die neutrale Achse der CAM (bei Chroma = 0,0) fallen. Dies verursacht große Schwierigkeiten für gmas. Damit gmas ordnungsgemäß funktioniert, müssen Sie die Beschreibung der Art des Geräts und der Eingabepunkte anpassen, damit die neutrale Achse des Geräts auf der neutralen Achse des Erscheinungs Bilds liegt. Sie müssen Punkte an der neutralen Achse um eine ähnliche Menge anpassen. Andernfalls können Sie keine Glättung durch das Bild durchführen. Auf dem Weg aus dem GMA wird diese Zuordnung relativ zur neutralen Achse des Ausgabegeräts rückgängig gemacht. Dies wird als "Chiropractic"-Korrektur der Achse bezeichnet. Wie bei einem chirovorgang wird das Gerüst (neutrale Achse) nicht nur auf das Gerüst ausgerichtet, sondern auch auf den Rest des Texts, um zusammen mit dem Gerüst zu wechseln. Wie bei einem Chiropractor passen Sie das Gerüst nicht um denselben Betrag durch den gesamten Raum an. Stattdessen werden verschiedene Abschnitte anders angepasst.

![Diagramm, das die Krümmung der Geräte neutralen Achse relativ zur neutralen ciecam-Achse anzeigt.](images/gmmp-image081.png)

**Abbildung 19:** Krümmung der Geräte neutralen Achse relativ zur ciecam-neutralen Achse

Der neue CTE erfordert ein Modell einer spielbegrenzung, das sowohl gerenderte als auch nicht gerenderte Quellbilder darstellen, Informationen zur Darstellung von Geräte neutralen bereitstellen und Informationen für Ton Zuordnungs Bilder mit einem breiten Glanz Bereich bereitstellen kann.

![Diagramm, das die drei Farbskala Shells anzeigt.](images/gmmp-image083.png)

**Abbildung 20** : drei Farbskala Shells

Die Spiel Grenze besteht aus drei Shells, die drei Bereiche definieren.

Im neuen allgemeinen Tabellen Ausdruck wird die äußere Shell des Farbskala mit einer konvexen Hülle gebildet, die aus Beispiel Punkten im Geräte Spiel erstellt wurde. Eine Hülle wird gebildet, indem eine Reihe von Beispiel Punkten erstellt und durch eine Oberfläche umgeben wird. Eine anvexen Hülle verfügt über die zusätzliche Eigenschaft, die überall gleich ist. Daher ist dies nicht die kleinste mögliche Hülle, die an die Daten angepasst werden kann. Doch das Experimentieren hat gezeigt, dass das Anpassen der Beispiel Punkte zu unansprech enden Artefakten in Bildern, wie z. b. fehlende Glättung, nicht geeignet ist. Diese Probleme lassen sich durch die konforme Hülle lösen.

Im Algorithmus werden farbdarstellungs Werte für einen Satz von Punkten abgerufen, die vom Gerät abgetastet werden. Bei Monitoren und Druckern werden die farbdarstellungs Werte durch Ausgabe von Beispielen abgerufen und anschließend gemessen. Sie können auch ein Gerätemodell erstellen und dann mithilfe des Geräte Modells synthetische Daten ausführen, um gemessene Werte vorherzusagen. Die gemessenen Werte werden dann von dem Wert "farbige Metrik" (XYZ) in den Darstellungs Raum (Jab) konvertiert, und die Hülle wird um die Punkte umschlossen.

Der wichtigste Punkt für diesen Algorithmus besteht darin, dass der bei der Konvertierung von farbmetriken in Darstellungs Raum verwendete weiße Punkt nicht den weißen Punkt des Mediums enthalten muss. Stattdessen können Sie einen Punkt weiter unten im Spielbereich und am (oder in der Nähe) der neutralen Achse auswählen. Dieser Punkt hat dann einen J-Wert von 100. Beispiele mit einem gemessenen Y-Wert, der höher als der angenommene weiße Punkt ist, erhalten einen J-Wert größer als 100.

Wenn Sie den diffusen weißen Punkt der Szene als den angenommenen weißen Punkt für die Farb Raum Konvertierung platzieren, werden Glanzlichter in der Szene leicht erkannt, wenn ein J-Wert größer als 100 ist.

Da das CIECAM02-Farbmodell auf dem visuellen System des visuellen Elements basiert, wird nach dem Auswählen eines gefolgten weißen weiß, dass die Beleuchtungs Ebene des schwarzen Punkts (J = 0) automatisch durch das Modell bestimmt wird. Wenn das Eingabebild über einen breiten dynamischen Bereich verfügt, ist es möglich, dass Werte, die J-Werten zugeordnet sind, kleiner als 0 (null) sind.

In der folgenden Abbildung 21 sind die Geräte neutrale aufgeführt, die im Mittelpunkt der Programmier-und Verweis-Gamuts ausgeführt werden.

![Diagramm, das die Geräte neutrale Achse anzeigt, die der Grenze für das Spiel hinzugefügt wurde.](images/gmmp-image085.png)

**Abbildung 21** : Geräte neutrale Achse zur Farbskala-Begrenzung hinzugefügt

Alle Farbskala-Zuordnungen umfassen entweder das Abschneiden eines Eingabe Bereichs in ein Ausgabe Spiel oder das Komprimieren des Eingabe-gamels, damit er in den Ausgabebereich passt. Komplexere Algorithmen werden durch Komprimieren und Abschneiden in verschiedene Richtungen oder durch Aufteilen des gamens in verschiedene Bereiche und anschließende durchführen von Clipping oder Komprimierung in den verschiedenen Regionen gebildet.

Der neue CTE erweitert dieses Konzept, um die Bereiche eines möglichen Gamut, ein plausibles Spiel und einen Verweis Bereich zu unterstützen, und ermöglicht gmas, Sie auf unterschiedliche Weise zuzuordnen. Darüber hinaus enthalten die gmas Informationen zur Geräte neutralen Achse. Im folgenden wird erläutert, wie Situationen behandelt werden, in denen die plausiblen Gamuts und Verweis-Gamuts aufeinander reduziert wurden.

![Diagramm, das das G M A mit zwei nicht reduzierten Spiel Deskriptoren anzeigt.](images/gmmp-image091.png)

**Abbildung 22** : GMA mit zwei nicht reduzierten Farbskala-Deskriptoren

Dieses Beispiel kann angezeigt werden, wenn Sie von einem Eingabegerät (z. b. einer Kamera oder einem Scanner, der mit einem reflektierenden Ziel gekennzeichnet ist) den ScRGB-Speicherplatz zuordnen. Hier sind die plausibler Farben, die heller als der Verweis weiß sind, Glanzlichter. In der Praxis generiert das Kennzeichnen einer Kamera mit einem Ziel möglicherweise nicht den vollständigen Bereich der in der Kamera möglichen Werte. Glanzlichter und sehr in der Natur gefundene Farben sind jedoch. (Bei Transaktions Zielen gibt es in der Regel einen Patch, der der auf dem Medium möglichen minimalen Dichte entspricht. Mit einem solchen Ziel würden Glanzlichter im Zielbereich liegen.) Der Verweis schwarz für ein reflektierendes Ziel wäre der Anfang des Schatten-schwarzen Bereichs. Das heißt, es gibt wahrscheinlich Farben in den Schatten, die dunkler als die schwarze auf dem Ziel sind. Wenn das Image viele interessante Inhalte in dieser Region enthält, kann es sinnvoll sein, diese klangliche Abweichung beizubehalten.

![Diagramm, das das G M a mit einem reduzierten Ziel Gamut anzeigt.](images/gmmp-image095.png)

**Abbildung 23** : GMA mit reduziertem Ziel Farbskala

Abbildung 23 zeigt einen möglichen Farbskala-Mapping-Algorithmus, wenn der Ziel Farbskala nur den Bereich von Gerät weiß bis schwarz bereitstellt und keine Farben außerhalb dieses gamels vorhanden sind. Dies geschieht wahrscheinlich für typische Ausgabegeräte, z. b. Drucker. Die möglichen Farben werden dem Rand des Ziel Gamut zugeordnet. Es fehlt jedoch eine Tonkurve für das Ausgabegerät. Das GMA muss einen neutralen Punkt der unteren Leuchtkraft auswählen, der als das Ziel der Referenz weiß verwendet werden soll. Ein ausgereifteter Algorithmus kann dies durch das histommen der lightpaces im Quell Bild erreichen und sehen, wie viele in den Bereich des erwarteten, aber heller als der Verweis weiß fallen. Umso komplexer ist, desto mehr Speicherplatz ist auf dem Zielgerät zwischen den zugeordneten Punkten für die Glanzlichter und den Verweis weiß erforderlich. Ein einfacherer Algorithmus könnte eine beliebige Entfernung der horizontalen Skalierung von Geräte weiß, z. b. 5 Prozent, auswählen. Ein ähnlicher Ansatz gilt für die Zuordnung der maximalen Schwarz-und Schatten-schwarz.

Nachdem Sie die Ziel Tonkurve generiert haben, können Sie eine Zuordnung in einer Methode durchführen, die der in der obigen Abbildung 23 verwendeten ähnelt. Alle Punkte in der Ziel Tonkurve liegen innerhalb des Geräte gamels, und alle Punkte in der Zuordnung müssen in den Geräte Gamut fallen.

Wenn Sie die linken und rechten Abbildungen und die Richtungen der Pfeile in Abbildung 23 umkehren, können Sie die Groß-/Kleinschreibung beschreiben, in der das Quell Abbild nur über einen Verweis Bereich verfügt und die drei Gamuts des Ausgabegeräts nicht ineinander reduziert sind. Ein Beispiel hierfür ist die Zuordnung von einem Monitor zu ScRGB. Auch hier muss das GMA die Steuerungs Punkte für die fünf Punkte in der Tonkurve des Quell Bilds synthetisieren. Bei manchen Zuordnungen werden möglicherweise alle Punkte der Tonkurve innerhalb des ScRGB-Geräte Diagramms eingefügt, während andere Zuordnungen einen größeren Teil des ScRGB-Diagramms verwenden können, indem diffuses weiß dem Verweis weiß zugeordnet wird und das Glanzlicht einem leichteren Wert zugeordnet werden kann.

Schließlich haben beide Geräte nur den Verweis Farbskala, d. h., wie die meisten Farbskala-Mapping-Algorithmen funktionieren. Dies können Sie beheben, indem Sie nur auf aktuelle Algorithmen zurückgreifen. Wenn Sie die fünf Bezugspunkte für die Quell-und Zielgeräte auf sinnvolle Weise ermitteln können, können Sie die Zuordnung der Referenzpunkte anordnen.

Geräte-Gamuts enthalten mehr als die fünf Referenzpunkte auf der neutralen Achse. Diese stellen lediglich die Grenzen zwischen potenziellen Regionen im Image dar. Zwischen den einzelnen Referenzpunkten können Sie eine beliebige der vorhandenen Techniken zur Spielkarten Zuordnung verwenden. Sie können also den Bereich unerwarteter Farben abschneiden und alle Farben zwischen den erwarteten weißen und schwarzen Farben komprimieren, oder Sie können alle Farben außerhalb des Bezugsbereichs Ausschneiden und innerhalb dieses Bereichs komprimieren. Es gibt zahlreiche Möglichkeiten, die in verschiedenen gmas implementiert werden können. Außerdem können die gmas auf unterschiedliche Weise komprimiert und ausgeschaltet werden. Alle diese Kombinationen werden innerhalb dieser Erfindung behandelt.

Bisher wurde in diesem Thema der Farbskala so behandelt, als wäre er nur eine Funktion des Geräts, auf dem das Image erstellt, aufgezeichnet oder angezeigt wurde. Es gibt jedoch keinen Grund, warum alle Images für ein Gerät denselben Gamut aufweisen müssen. Die gmas sind abhängig von den Daten in der Gbd. Wenn der Deskriptor zwischen Bildern geändert wird, gibt es keine Möglichkeit, die gmas zu kennen. Insbesondere wenn Bilder keine Glanzlichter aufweisen, erzielen gmas eine bessere Leistung, wenn der Farbskala-Deskriptor nicht anzeigt, dass Farben heller als diffuses weiß sind.

In der neuen CTE-Architektur ist es möglich, mehr als ein GMA zu verwenden. Die Verwendung mehrerer gmas ist von Natur aus falsch definiert. Wenn z. b. ein Aufzeichnungsgerät seine "Erscheinungsbild" mit dem "Aussehen und fühlen" verknüpft, wird dies in der Regel mit einem Ziel Gamut (Ziel) durchzuführen. Das gleiche gilt für Ausgabegeräte und Ziel Quell Gamuts. Der sRGB-Farbskala ist ein üblicherweise implizites Spiel. Daher wird dringend empfohlen, dass Sie ein einzelnes GMA verwenden, wenn Vorhersagbarkeit eine Priorität darstellt. Ein einzelner GMA-Workflow sollte der Standardwert für alle Workflows sein, insbesondere für Consumer-und Prosumer-Workflows. Während die Farbskala-Zuordnung für die bevorzugte Reproduktion einmalig erfolgen soll, gibt es Instanzen, in denen mehrere zuder Zuordnungsprozesse eingeschlossen werden. Als erstes machen Sie für die Absicherung eine bevorzugte Zuordnung zum Farbskala des endgültigen Zielgeräts und dann ein farmetriedaten-Rendering zum Spiel des Messgeräts. Zweitens werden einige Typen von Zuordnungen verwendet, um die Merkmale des Bilds zu ändern, aber nicht für die Zuordnung zu einem Geräte Spiel, z. b. zum Anpassen der Tonkurve oder der Chromatizität. Wenn mehrere gmas verwendet werden, nimmt die Transformations Schnittstelle ein Array von gebundenen gamingzuordnungen, d. h. Farbskala-Zuordnungen, die mit einem Paar von Farb Begrenzungs Beschreibungen initialisiert wurden. Wenn mehrere gamingzuordnungen vorhanden sind, muss die eingabegamut-Grenze für eine nachfolgende gamingzuordnung mit der Ausgabe Spiel Grenze des Vorgängers identisch sein.

Die Geräte-Farbskala-Begrenzungs Funktion nimmt die Gerätemodell-Engine und die analytischen Parameter an und leitet eine Farb Geräte-geclustergrenze ab, die als geordnete Vertex-Liste der einander zusammengestellten Hülle des Geräte gamzes beschrieben wird. Die geordnete Vertex-Liste wird in ciejab gespeichert. Die Struktur der geordneten Vertex-Liste ist für die Hardwarebeschleunigung durch DirectX optimiert. Bei diesem Ansatz gibt es viele bekannte Lösungen (suchen 100 Sie im Web nach "" mit "" der ""-"" "," "," "," "," " In diesem Thema finden Sie auch einen Verweis von 1983 (Computer Grafik Theorie und-Anwendung, "shiphulls, b-Spline-Oberflächen und CADCAM" PP. 34-49) mit Verweisen von 1970 bis 1982 im Thema.

Zum Berechnen der Dreiecke in der Farbskala-Shell können zwei verschiedene Verfahren verwendet werden. Bei anderen Geräten als Additiven RGB-Geräten berechnen Sie eine konvexe Hülle. Wenn Sie direkten Zugriff auf solche Geräte haben, können Sie die Unterstützung der nicht-unterstützten Hülle für andere Geräte in Erwägung gezogen, um die Stabilität, Leistung und Genauigkeit der Algorithmen zu überprüfen. Dies ist ein bekannter Prozess, für den keine weitere Beschreibung erforderlich ist. Das Verfahren, das für Additive RGB-Geräte verwendet wird, wird wie folgt beschrieben.

Unterschiedliche gbds haben vor-und Nachteile. Die Darstellung der Darstellung der Darstellung gewährleistet eine gute geometrische Eigenschaft, wie z. b. konforme Hue-Slices, die einen eindeutigen Schnittstellen Punkt mit einem Strahl darstellen, der von einem Punkt auf der neutralen Achse ausgeht. Der Nachteil der Darstellung der einander-Darstellung ist ebenfalls "". Es ist bekannt, dass viele Geräte, speziell Geräte anzeigen, über Gamuts verfügen, die weit von der Verwendung von "konform" sind. Wenn der tatsächliche Farbskala stark von der anvexity Annahme abweicht, wäre die Darstellung der Kontur Darstellung ungenau, möglicherweise in dem Ausmaß, in dem Sie die Realität nicht repräsentiert.

Nachdem Sie eine Gbd übernommen haben, die eine ziemlich genaue Darstellung des tatsächlichen Gamut liefert, treten andere Probleme auf, was aufgrund des sehr großen Konzepts von Hue Slice der Grund ist. Es sind mindestens zwei pathologische Situationen vorhanden. In der folgenden Abbildung 24 gibt es mit einem CRT-Farbskala eine Zunahme von Hue Slices mit "Inseln". In Abbildung 25 wird ein Drucker Spiel in einem Hue-Slice angezeigt, dessen Teil der neutralen Achse fehlt. Die pathologischen Farbton werden in diesen Fällen nicht durch besonders pathologische spielgrenzen verursacht. Sie werden durch das Konzept von Hue Slice verursacht, da (a) es sich um einen konstanten Farbton handelt, und (b) es nimmt nur eine Hälfte der Ebene, die dem Hue-Winkel entspricht.

![Diagramm, das eine obere Ansicht und eine neben Ansicht der "Cursor in" in den blauen Schattierungen anzeigt.](images/gmmp-image097.jpg)

**Abbildung 24** : ein typischer CRT-Monitor verfügt über eine Reihe von Farben, die sich in den blauen Farben als "Cursor" in den blauen Farben anzeigen. Wenn Hue Slices innerhalb dieses Farbton Bereichs entnommen werden, können isolierte Inseln in den Hue-Slices angezeigt werden.

![Diagramm eines Farbskala mit einer "Lücke" in der neutralen Achse.](images/gmmp-image099.jpg)

**Abbildung 25** : ein Drucker kann über eine "Lücke" in seiner neutralen Achse verfügen. Wenn ein Hue-Slice (also nur eine Hälfte der Ebene) erstellt wird, gibt es einen "Dent" für den Teil der Grenze, bei dem es sich um die neutrale Achse handelt. Dies kann nur schwer algorithmisch aufgelöst werden.

Um diese Pathologien aufzulösen, wird ein neues Framework vorgeschlagen, das das Konzept von Hue Slice abbricht, das als Ausgangspunkt verwendet wird. Stattdessen verwendet das Framework den Satz von "Begrenzungs Linienelementen" oder Zeilen, die sich auf der Spiel Grenze befinden. Sie bieten nicht notwendigerweise eine kohärente geometrische Visualisierung wie Hue Slices, Sie unterstützen jedoch alle gängigen Spiel Vorgänge. Zusätzlich zu den oben erwähnten Problemen deutet dieser Ansatz auch darauf hin, dass die Erstellung von Hue-Slices, auch wenn möglich, Rechen bedingt verschwendet wird.

### <a name="triangulation-of-the-gamut-boundary"></a>Die Untergrenze der spielbegrenzung.

Der Ausgangspunkt ist ein Gbd, das aus einer drei-und dreieckigen Begrenzung besteht. Bekannte Methoden zum Erstellen von gbds stellen in der Regel die drei Möglichkeiten zur Verfügung. Aus Gründen der Konkretheit wird hier eine Methode zum Erstellen von gbds für Additive Geräte beschrieben. Zu diesen Geräten gehören Monitore (sowohl CRT-als auch LCD-basiert) und Projektoren. Die einfache Geometrie des Cubes ermöglicht es Ihnen, ein reguläres Gitter auf dem Cube einzuführen. Die Begrenzungs Gesichter des Cubes können in einer Reihe von Fashions (z. b. in Abbildung 26) als Dreieck dargestellt werden. Die Architektur stellt entweder ein Gerätemodell für das Gerät bereit, sodass farbige Metrikwerte der Gitter Punkte algorithmisch abgerufen werden können oder dass für diese Punkte direkt Messungen durchgeführt wurden. Die Architektur bietet auch CIECAM02, sodass Sie annehmen können, dass die Anfangsdaten bereits im CIECAM02 Jab-Speicherplatz zugeordnet wurden. Dann hat jeder Gitterpunkt an den Begrenzungs Flächen des RGB-Cubes einen entsprechenden Punkt im Speicherplatz. Die Verbindungen von Punkten, die den Satz von Dreiecken in RGB-Raum bilden, verursachen auch eine Reihe von Dreiecken im Speicherplatz. Diese Gruppe von Dreiecken bildet eine sinnvolle Dreiecke der Farbskala-Begrenzung, wenn (a) das Gitter auf dem RGB-Cube ausreichend ist, und (b) die Transformation vom Gerätebereich zum einheitlichen farbliche farbliche Wert ist. Das heißt, Sie ordnet die Grenze der Grenze zu und schaltet den Bereich nicht in den Bereich ein, sodass die inneren Punkte zu Begrenzungs Punkten werden.

![Diagramm, das eine einfache Methode zeigt, um die Spiel Grenze eines Geräts mit R G B als Geräteraum zu überwiegen.](images/gmmp-image100.png)

**Abbildung 26** : eine einfache Methode, um die Spiel Grenze eines Geräts mit RGB als Geräte Speicherplatz zu ermitteln

### <a name="boundary-line-elements"></a>Begrenzungs Linien Elemente

Die zentrale für dieses Framework ist das Konzept von Begrenzungs Linienelementen. eine Reihe von Liniensegmenten (a), die sich auf der Spiel Grenze befinden, und (b) auf einer Ebene. In diesem Fall ist die Ebene eine Farbton Ebene. Jedes Zeilen Segment ist das Ergebnis der Schnittmenge der Ebene mit einem Farbskala-Begrenzungs Dreieck. Obwohl viele Forscher die Konstruktion der Schnittmenge einer Ebene mit Begrenzungs Dreiecken verwendet haben, analysieren Sie im Allgemeinen die Beziehung zwischen diesen Liniensegmenten und versuchen, ein kohärentes geometrisches Objekt aus den Liniensegmenten zu konstruieren. Es wurden verschiedene Algorithmen entworfen, um die folgenden Liniensegmente nacheinander zu befolgen, bis ein ganzer Farbton abgerufen wird, und es wurden viele Versuche unternommen, den Suchvorgang zu beschleunigen.

Diese Vorgehensweise ist unterschiedlich. Sie schneiden die Ebene mit den Dreiecken ab, um die Liniensegmente zu erhalten. Diese Liniensegmente werden dann als *grundlegende* konzeptionelle Objekte betrachtet. Die Beziehung zwischen den Liniensegmenten muss analysiert werden. Sie müssen nicht wissen, wie Sie miteinander verbunden sind. In dieser Sicht wird das Problem von Hue Slice mit Inseln gelöst. Die bekannten Ansätze, die versuchen, Hue Slice zu erstellen, nehmen an, dass, wenn eine Zeile mit einem Zeilen Segment beginnt und auf das nächste Zeilen Segment folgt, und so weiter. Schließlich führt Sie zurück zum Ausgangspunkt. an diesem Punkt würde ein ganzer Farbton erstellt werden. Leider würde diese Vorgehensweise die Insel übersehen (und im schlimmsten Szenario, auf dem Kontinent). Wenn Sie nicht darauf beharren, ein kohärentes geometrisches Bild zu erhalten, Das heißt, Sie können das inselproblem mühelos lösen. Ein weiterer wichtiger Unterschied bei diesem Ansatz besteht darin, dass zum beschleunigen der Konstruktion von Liniensegmenten ein "Dreiecks Filter" verwendet wird. Der Dreieck Filter löst bestimmte Dreiecke aus, die definitiv keine Liniensegmente erzeugt, die für den aktuellen gamingvorgang nützlich sind. Da das überschneiden eines Dreiecks mit der Ebene sehr teuer ist, wird dadurch die Geschwindigkeit erhöht. Ein Nebeneffekt ist, dass Sie Hue Slice nicht erstellen können, da einige Liniensegmente aufgrund der Dreiecks Filterung fehlen würden.

### <a name="gamut-operation-checkgamut"></a>Gamut-Vorgang: Prüfpunkt

Im folgenden Beispiel wird erläutert, wie das Framework funktioniert und wie checkgamut durchgeführt wird, d. h. der Vorgang der Überprüfung, ob eine Farbe im Spiel ist.

Das allgemeine Framework wird in der folgenden Abbildung 27 veranschaulicht. Es gibt verschiedene Komponenten. Bei den in kursiv gekennzeichneten Komponenten handelt es sich um Komponenten, die je nach dem fraglichen gamingvorgang in der Implementierung unterschiedlich sein können. Die anderen Komponenten sind in allen gamingvorgängen invariante. Zunächst ist die ***Eingabe*** ein Satz von Farb Attributen. Im Fall von checkgamut ist dies die Abfrage Farbe. In Abbildung 27 und der folgenden Erläuterung wird davon ausgegangen, dass der Hue-Winkel entweder aus den Eingabe Farb Attributen besteht oder von Ihnen abgerufen werden kann. Dies ist eindeutig der Fall, wenn es sich bei der Eingabe um den gesamten Farbpunkt handelt (entweder in Jab oder Jch), von dem aus Sie den Farbton berechnen können. Beachten Sie, dass der Hue-Winkel nur benötigt wird, da Hue-Flächen verwendet werden. Je nach dem fraglichen gamingvorgang ist es möglicherweise nicht erforderlich, die Hue-Ebene zu verwenden. Beispielsweise können Sie bei der Erstellung der Routine checkgamut die Ebenen der Konstanten J verwenden. Dies ist eine Generalität, die nicht weiter verwendet oder diskutiert wird. Es kann jedoch hilfreich sein, sich diese Flexibilität der Methodik zu merken, um andere Spiel Vorgänge zu unterstützen, wenn die Hue-Ebene möglicherweise nicht die beste Wahl ist.

![Diagramm, das den Flow zum unterstützen von Farbskala-Vorgängen anzeigt.](images/gmmp-image112.jpg)

**Abbildung 27** : das Framework zur Unterstützung von Farbskala-Vorgängen

Der Hue-Winkel, der direkt aus den Eingaben abgerufen oder aus den Eingaben berechnet wird, wird verwendet, um die Hue-Ebene mit der Bezeichnung **Full Hue Plane** in der Abbildung zu initialisieren. "Full" wird hervorgehoben, da es sich hierbei um die vollständige Ebene handelt, nicht nur die Hälfte der Ebene, die den Farbton enthält. Die vollständige Ebene enthält sowohl den Eingabe Farbton Winkel als auch den Winkel von 180 Grad. Die Hauptfunktionalität der Hue-Ebene ist die Intersect-Funktion, die im folgenden unter Abschnitt "Full Hue Plane: Intersect" erläutert wird. Nehmen Sie an, dass die Gbd bereits erstellt wurde, und dass die Menge der **Gamut-Begrenzungs Dreiecke** verfügbar ist. Schneiden Sie die Dreiecke ab, die den **_Dreiecks Filter_* _ mit der Hue-Ebene mit Intersect noch nicht verwendet haben. Die _Komponente "Dreieck Filter *" ist kursiv gekennzeichnet, was bedeutet, dass die Komponente in der Implementierung für verschiedene Spiel Vorgänge variiert. Der *Dreieck Filter* für checkgamut wird im Abschnitt "Gamut-Vorgang: checkgamut (fortgesetzt)" erläutert. Das Ergebnis der Schnittmenge eines Dreiecks mit der Hue-Ebene ist entweder leer oder ein **Begrenzungs Linien Element** , d. h. ein paar von unterschiedlichen Punkten. Wenn das Ergebnis nicht leer ist, wird es an den *-*_Zeilen Element Prozessor_* weitergegeben_ , der wiederum unterschiedliche Aktionen in Abhängigkeit vom Spiel Vorgang durchführt. Der _Line-Element-Prozessor * aktualisiert die interne Datenstruktur (***interne verarbeitete Daten**_ ), deren Inhalt oder Layout auch vom Spiel Vorgang abhängig ist. Im allgemeinen _enthält die intern verarbeiteten Daten * die "Antwort" für das Problem, das ständig aktualisiert wird, wenn jedes neue Begrenzungs Linien Element gefunden wurde. Wenn alle Begrenzungs Linien Elemente verarbeitet wurden, wurde die Antwort gefunden. Über den *-**Ausgabe Adapter**_ kann darauf zugegriffen werden. Da es sich bei der _Internal verarbeiteten Daten * um einen speziellen Arbeits Aufgabentyp handelt, ist der *Ausgabe Adapter* ebenfalls für das Spiel.

### <a name="full-hue-plane-intersect"></a>Vollton-Ebene: Intersect

Die Intersect-Funktion berechnet die Schnittmenge der Hue-Ebene und eines Dreiecks. So einfach, wie es klingt, ist diese Funktion aus zwei Gründen wichtig.

Zuerst kann die überschneidende Schnittstelle des Dreiecks mit der Ebene drei Schnittstellen Punkte ergeben, eine nicht allzu mögliche Situation. Der Grund, warum dies in der Berechnung auftreten könnte, besteht darin, dass bei Berechnungen in Gleit Komma Zahlen (z. b. IEEE-Format) oder "numerischer Rauschen" in jedem Schritt, der sich auf den Schluss der überschneidet, ob ein Rand die Ebene überschneidet. Wenn die Ebene die Ränder in einer fast-Miss-Situation schneidet, sind die Schnittpunkte nah beieinander und die Bestimmung, ob ein Schnittpunkt innerhalb des Edge liegt, zufällig. Obwohl das Rauschen in den numerischen Werten der Punkte gering ist, ist der qualitative Schluss, dass es mehr als zwei Schnittstellen Punkte gibt, geometrisch unmöglich und schwierig, die ordnungsgemäße Behandlung im Algorithmus durchzuführen.

Zweitens: Diese Funktion befindet sich in der kritischen Schleife für jeden Rand jedes gefilterten Dreiecks, daher ist es wichtig, dass Sie die Effizienz so weit wie möglich optimieren.

Um das erste Problem des numerischen Rauschens zu beheben, führen Sie die Berechnungen in ganzen Zahlen aus. Um das zweite Problem bei der Optimierung der Effizienz zu beheben, müssen Sie das am häufigsten verwendete Attribut jedes Scheitel Punkts oder das "Punktprodukt" Zwischenspeichern, das jedem Scheitelpunkt zugeordnet ist. Das übergeben in ganze Zahlen ist eine typische Methode, um geometrische Konsistenz zu gewährleisten. Die grundlegende Idee ist, dass Sie, wenn Sie quantifisieren müssen, dies am Anfang tun müssen. Anschließend können nachfolgende Berechnungen in ganzen Zahlen durchgeführt werden, und wenn die ganzen Zahlen breit genug sind, sodass keine Überlauf Gefahr besteht, können die Berechnungen mit unbegrenzter Genauigkeit durchgeführt werden. Die folgende quantisierungsfunktion ist für diesen Zweck nützlich.

Scaleandtruncate (x) = ganzzahliger Teil von x \* 10000

Der Skalierungsfaktor 10000 bedeutet, dass die Eingabe Gleit Komma Zahl vier Dezimalstellen aufweist, die für diese Anwendung genau genug ist. Abhängig von dem Wertebereich des Farb Darstellungs Bereichs möchten Sie einen ganzzahligen Typ mit Bits für die Zwischenberechnungen auswählen. In den meisten Farbdarstellung liegt der Bereich der einzelnen Koordinaten im Bereich von-1.000 bis 1.000. Die quantifizierte Koordinate hat einen maximalen möglichen absoluten Wert von 1.000 \* 10.000 = 10 Millionen. Wie Sie sehen werden, ist die zwischen Menge ein Punktprodukt, bei dem es sich um eine Summe von zwei Koordinaten Werten handelt, sodass es einen maximalen möglichen absoluten Wert von 2 \* (10 Millionen) 2 () = 2? 10 ₁ ₄ hat. Die erforderliche Anzahl von Bits ist log CO2 (2? 10 ₁ ₄) = 47,51. Eine bequeme Wahl für den ganzzahligen Typ ist daher 64-Bit-Ganzzahlen.

Um sicherzustellen, dass die Schnittmenge einer Ebene mit einem Dreieck immer entweder eine leere Menge oder einen Satz von zwei Punkten ergibt, müssen Sie das Dreieck als Ganzes betrachten, nicht als einzelne Ränder des Dreiecks getrennt. Zum besseren Verständnis der geometrischen Situation sollten Sie die "signierten Entfernungen" der Scheitel Punkte des Dreiecks von der Hue-Ebene in Erwägung gezogen haben. Diese signierten Entfernungen nicht direkt berechnen; Berechnen Sie stattdessen die Punkt Produkte der Positions Vektoren der Vertices mit dem quantifizierten normalen Vektor auf der Ebene. Genauer gesagt wird der quantifisierte normale Vektor während der Initialisierung der Hue-Ebene wie folgt berechnet.

Normalvector = (scaleandtruncate (-Sin (Hue)), scaleandtruncate (COS (Hue)))

Beachten Sie, dass es sich bei diesem Vektor um einen zweidimensionalen Vektor handelt. Sie können einen zweidimensionalen Vektor verwenden, da die Hue-Ebene vertikal ist, sodass die dritte Komponente des normalen Vektors immer 0 (null) ist. Darüber hinaus wird eine Nachschlage Tabelle mit Punkt Produkten initialisiert, um einen Eintrag für jeden Scheitelpunkt von der Gamut-Begrenzungs Dreiecke und das entsprechende Punktprodukt auf einen ungültigen Wert festzulegen.

Bei einem Vorgang, der die Hue-Ebene mit einem Dreieck schneidet, wird das Punktprodukt der einzelnen Scheitel Punkte des Dreiecks gesucht. Wenn der Wert in der Nachschlage Tabelle der ungültige Wert ist, wird das Punktprodukt mit dem folgenden Ausdruck berechnet.

Normvector. a \* scaleandtruncate (Vertex. a) + normalvector. b \* scaleandtruncate (Vertex. b)

Auch hier wird die J-Komponente des Scheitel Punkts niemals verwendet, da der normale Vektor horizontal ist. Dieses Punktprodukt wird dann in der Nachschlage Tabelle gespeichert, damit es nicht erneut berechnet werden muss, wenn das Punktprodukt des Scheitel Punkts später abgefragt wird.

Mithilfe der Zwischenspeicherung können Sie schnell feststellen, ob sich der Rand der Ebene überschneidet, nachdem die Punkt Produkte in der Nachschlage Tabelle in der Tabelle angezeigt werden, die bei der Verarbeitung der Scheitel Punkte progressiv erstellt wird.

![Diagramm, das die Schnittmenge der Hue-Ebene mit einem Dreieck anzeigt.](images/gmmp-image114.jpg)

**Abbildung 28** : überschneidende Hue-Ebene mit einem Dreieck

Damit das Dreieck in Abbildung 28 die Hue-Ebene in einem nicht degenerierten Liniensegment schneidet, müssen sich die Punkt Produkte der Scheitel Punkte in einem der folgenden Muster befinden, wenn Sie in aufsteigender Reihenfolge sortiert werden.

0, 0, +; -, 0, 0; -, 0, +; -,-,+; -,+,+

Ein Endpunkt des Linien Segments wird angezeigt, wenn die Ebene von einem Rand mit Scheitel Punkten geschnitten wird, die im Punktprodukt verschiedene Vorzeichen aufweisen. Wenn das Vorzeichen NULL ist, befindet sich der Scheitelpunkt rechts auf der Ebene, und die Schnittmenge des Randes mit der Ebene ist der Scheitelpunkt selbst. Beachten Sie auch, dass die Fälle 0, 0, 0; -,-, 0; 0, +, + werden nicht gemeldet. Der erste Fall (0,0) bedeutet, dass das gesamte Dreieck auf der Ebene liegt. Dies wird nicht berichtet, weil jeder Rand des Dreiecks zu einem benachbarten Dreieck gehört, das nicht auch vollständig auf der Ebene liegt. Der Edge wird gemeldet, wenn das Dreieck berücksichtigt wird. Die anderen beiden Fälle (-,-, 0 und 0, +, +) entsprechen der geometrischen Konfiguration, dass das Dreieck die Ebene in einem Scheitelpunkt berührt. Diese Fälle werden nicht gemeldet, da Sie nicht auf ein nicht degeneriertes Liniensegment steigen.

Der vorherige Algorithmus bestimmt, wann eine Schnittmenge zwischen einem Rand des Dreiecks und der Hue-Ebene berechnet werden soll. Nachdem eine Kante festgelegt wurde, wird die Schnittmenge mithilfe von parametrischen Gleichungen berechnet. Wenn eines der Punkt Produkte 0 (null) ist, ist die Schnittmenge der Scheitelpunkt selbst, sodass keine Berechnung notwendig ist. Wenn beide Punkt Produkte der Scheitel Punkte des edgeknotens ungleich NULL sind, ist vertex1 der Scheitelpunkt mit *negativem* Punkt Product dotProduct1; und vertex2 ist der Scheitelpunkt mit einem *positiven* Punkt Product dotProduct2. Diese Reihenfolge ist wichtig, um sicherzustellen, dass der berechnete Schnittstellen Punkt nicht davon abhängt, wie die Reihenfolge der Scheitel Punkte in der Darstellung des Edge erscheint. Das geometrische Konzept des Edge ist in Bezug auf seine Scheitel Punkte symmetrisch. Der Berechnungs Aspekt der Verwendung von parametrischen Gleichungen der Edge führt zu asymmetrischen Gleichungen (Auswahl des ersten Scheitel Punkts), die aufgrund des numerischen Rauschens und der Durchsetzung der zu lösenden linearen Gleichungen etwas unterschiedliche Schnittstellen aufweisen können. In diesem Beispiel wird der Schnittstellen Punkt (Schnittmenge) durch Folgendes angegeben.

t = dotProduct1/(dotProduct1-dotProduct2)

Kreuz. J = vertex1. J + t \* (vertex2. J-vertex1. IStGH

Schnittmenge. a = vertex1. a + t \* (vertex2. a-vertex1. a)

Schnittmenge. b = vertex1. b + t \* (vertex2. b-vertex1. b)

### <a name="gamut-operation-checkgamut-continued"></a>Gamut-Vorgang: checkgamut (fortgesetzt)

Der grundlegende geometrische Algorithmus, der für die Überprüfung der Überprüfung verwendet wird, ist das zählen der Anzahl von Strahl Übergängen Bei einem bestimmten Abfrage Punkt sollten Sie einen Strahl in Erwägung nehmen, der mit dem Abfrage Punkt beginnt und nach oben (J-Direction) zeigt. Zählt, wie oft dieser Strahl die Spiel Grenze überschreitet. Wenn diese Zahl gerade ist, dann ist der Abfrage Punkt nicht mehr im Spiel. Wenn diese Zahl ungerade ist, befindet sich der Punkt innerhalb von. Im Prinzip kann dieser Algorithmus in 3D implementiert werden. er wird in der Regel durch degenerierte Situationen, z. b. das strahlende (teilweise) auf einem Begrenzungs Dreieck, oder eine niedrigere dimensionale degenerität, wie z. b. das strahlende (teilweise) an einem Rand eines Begrenzungs Dreiecks, geplagt. Auch in 2D müssen Sie sich mit diesen degenerierten Situationen befassen. das Problem ist jedoch einfacher und wurde auf zufriedenstellende Weise gelöst. Weitere Informationen finden Sie unter "" \[ \] .

Legen Sie für einen bestimmten Eingabe Punkt Jab wie folgt den Farbton Wert h fest.

h = Atan (b/a),

Initialisieren Sie die Hue-Ebene, und bestimmen Sie dann die Begrenzungs Linien Elemente, die dieser Farbton Ebene entsprechen. Da die Begrenzungs Linien Elemente nur relevant sind, wenn Sie den aufwärts Strahl überschneiden, richten Sie einen Dreiecks Filter ein, um Dreiecke zu entfernen, die Linien Elemente, die definitiv den Pfeil nach oben nicht überschneiden. Beachten Sie in diesem Fall das umgebende Feld des Dreiecks. Der aufwärts Strahl überschneidet das Dreieck nicht, wenn sich der Abfrage Punkt außerhalb des "Schattens" befindet, der durch das umgebende Feld umgewandelt wird, wenn eine Lichtquelle direkt oberhalb von ist. Erhöhen Sie dies leicht mit einer Toleranz vor dem festgelegten Toleranz, damit Sie ein numerisches Rauschen zulassen, damit Sie nicht versehentlich Dreiecke auslassen, die möglicherweise nützliche Linien Elemente ergeben. Das Ergebnis ist der semiunendliche rechteckige Zylinder, der in Abbildung 29 dargestellt wird. Die Überprüfung, ob sich der Abfrage Punkt innerhalb oder außerhalb dieses Zylinders befindet, kann mithilfe einfacher Ungleichheiten effizient implementiert werden.

![Zeigt den Dreiecks Filter für checkgamut an.](images/gmmp-image116.jpg)

**Abbildung 29** : Dreieck Filter für checkgamut

Checkgamut umfasst drei Komponenten für den gamingvorgang: *interne verarbeitete Daten*,*Zeilen Element Prozessor* und *Ausgabe Adapter*. Bei den *intern verarbeiteten Daten* handelt es sich um eine Liste der Zeilen Elemente, die vom *Zeilen Element Prozessor* verarbeitet wurden. In diesem Fall fügt der *Zeilen Element Prozessor* der Liste einfach ein Line-Element hinzu. Die interne Datenstruktur für die *intern verarbeiteten Daten* kann entweder eine verknüpfte Liste oder ein Array sein, das die Größe vergrößern kann.

Der *Ausgabe Adapter* ist ein Modul, das auf die Liste der Zeilen Elemente zugreift, bestimmt, ob ein Line-Element den aufwärts Strahl (count 1) oder nicht (count 0) überschreitet. Durch addieren all dieser Zahlen ergibt sich eine Gesamtzahl. Der *Ausgabe Adapter* gibt letztendlich eine Antwort mit dem Wert "yes" (in-Gamut) oder "No" (außerhalb des Gamut) aus, je nachdem, ob die Gesamtanzahl ungerade oder gerade ist. Der Schritt, in dem Sie bestimmen, ob ein Line-Element den aufwärts gerichteten Strahl überschreitet, verdient eine gewisse Aufmerksamkeit, da hier das Problem der herab Stellung auftritt und auch das Problem der überzähligen Zählung auftritt. Nach der Verwendung \[ von "o \] ..." für ein Line-Element, um das Strahl zu überschreiten, muss sich der Rechte Endpunkt (der Endpunkt mit größerem Chroma) strikt auf der rechten Seite des Strahls befinden. Dadurch wird sichergestellt, dass, wenn ein Endpunkt jemals genau auf dem Strahl liegt, nur einmal gezählt wird. Dieselbe Regel löst auch die degenerierte Situation, in der das Line-Element genau auf dem Strahl liegt. Sie erhöhen die Anzahl für dieses Zeilen Element nicht.

Abbildung 30 zeigt die resultierenden Linien Elemente eines Beispiel-Farbskala mit dem Abfrage Punkt an verschiedenen Positionen.

![Diagramm, das die sich ergebenden Linien Elemente eines Beispiel Diagramms mit dem Abfrage Punkt an verschiedenen Positionen anzeigt.](images/gmmp-image118.jpg)

**Abbildung 30** : Funktionsweise von checkgamut

### <a name="minimum-color-difference-gamut-mapping"></a>Minimale Farbunterschiede-Diagramm Zuordnung

Die minimale Farbunterschiede-Zuordnungs Zuordnung, "mindemap", weist eine einfache Spezifikation auf: Wenn eine Farbe im Spiel ist, sollten Sie nichts tun. Wenn eine Farbe außerhalb des Farbskala ist, projizieren Sie Sie an den "nächstgelegenen" Punkt an der Spiel Grenze. Das Schlüsselwort "Next" ist nicht klar definiert, bis Sie angeben, welche Farbunterschied-Gleichung verwendet werden soll. In der Praxis wird zur Vereinfachung und schnelleren Berechnung der euklidischen Entfernung des ausgewählten Farb Darstellungs Raums oder eine Variante davon als Farbunterschied verwendet. Der Vorteil der euklidischen Metrik besteht darin, dass Sie mit dem Punktprodukt des Raums kompatibel ist, wodurch es möglich ist, lineare Algebra zu verwenden. Wenn im Raum ein "Punktprodukt" definiert ist, kann eine Distanz als Quadratwurzel des Punkt Produkts des Differenz Vektors mit sich selbst definiert werden. Ein Punktprodukt kann im Allgemeinen durch eine positive, definitive 3X3-Matrix a definiert werden.

u? v = u <sub>T</sub> AV

Dabei ist die Rechte Seite die übliche Matrix Multiplikation. Wenn eine Identitätsmatrix ist, wird das Standard-Punktprodukt wieder hergestellt. Wenn Jab der Farbraum ist, sollten Sie die Komponenten in der Praxis nicht vermischen, sodass eine andere Diagonale Matrix als die Identitätsmatrix verwendet werden kann. Außerdem empfiehlt es sich, die Skalierung von a und b unverändert zu lassen, damit das Maß von Hue beibehalten wird. Eine nützliche Variante des standardmäßigen euklidischen Punkt Produkts ist die folgende.

w <sub>j</sub> (j-Komponente von Ihnen) (j-Komponente von v) + (eine Komponente von Ihnen) (eine Komponente von v) + (b-Komponente von Ihnen) (b-Komponente von v)

wobei w <sub>J</sub> eine positive Zahl ist. Eine weitere Variante besteht darin, w <sub>J</sub> mit dem Eingabe Abfrage Punkt zu unterscheiden:

w <sub>j \ =</sub> w <sub>(</sub> querypoint)

Das Endergebnis ist ein Measure der Entfernung, das in Bezug auf die beiden Punkte asymmetrisch ist, und mit unterschiedlichen relativen Gewichtungen bei Helligkeit und Chroma oder Hue, wenn der Eingabe Abfrage Punkt variiert. Dies entspricht einigen Beobachtungen hinsichtlich der menschlichen Farbwahrnehmung, dass Farbunterschiede nicht gleichmäßig in allen Dimensionen gewichtet werden. Es wurde festgestellt, dass Personen weniger sensibel sind als Unterschiede in Hue und Chroma.

Die folgende Gewichtungsfunktion ist hilfreich.

w <sub>J</sub> = k-k ₁ (c-C m ₐ ₓ) n

Where k. = 1, k ₁ = 0,75/(C m ₐ ₓ) n, C m ₐ ₓ = 100, n = 2 und c ist der kleinere von Chroma des Abfrage Punkts und c m ₐ ₓ.

eine Gewichtung von 0,25 wird also auf den J-Begriff gesetzt, wenn Chroma NULL ist, und eine Gewichtung von 1, wenn Chroma 100 ist. Der Trend der Bedeutung von j, wenn Chroma gering ist, und der Bedeutung von j, wenn Chroma groß ist, folgt der empfohlenen Verwendung für CMC und CIEDE2000.

![Diagramm, das die Gewichtungsfunktion in der J-Komponente der Metrik anzeigt.](images/gmmp-image119.png)

**Abbildung 31** : die Gewichtungsfunktion für die J-Komponente der Metrik

Verwenden Sie den Speicherplatz für das folgende Beispiel. Es ist rechnerisch anspruchsvoll, alle Begrenzungs Dreiecke zu durchsuchen, um den nächstgelegenen Punkt der euklidischen Metrik zu ermitteln. Im folgenden finden Sie eine einfache Vorgehensweise, um diesen Prozess so effizient wie möglich zu gestalten, ohne dass zusätzliche Annahmen eingeführt werden, die den Prozess beschleunigen können, aber auch nur eine ungefähre Antwort erhalten. Zunächst ist es erforderlich, das geometrische Verfahren zum Projizieren eines Punkts auf das angegebene Dreieck zu verstehen. Hier wird eine Beschreibung angegeben.

Eine orthogonale Projektion auf die unendliche Ebene, die das Dreieck enthält, wird zuerst ausgeführt. Die kürzeste Entfernung des Abfrage Punkts von der Ebene kann in zwei Schritten festgelegt werden.

**(a)** berechnen Sie den Einheiten normalen Vektor für das Dreieck.

**(b)** berechnen Sie das Punktprodukt des Einheits normalen Vektors und einen Vektor, der sich aus dem Abfrage Punkt und einem Punkt auf dem Dreieck gebildet hat. Das heißt, einer seiner Scheitel Punkte. Da der normale Vektor über eine Einheitslänge verfügt, ist der absolute Wert dieses Punkt Produkts der Abstand des Abfrage Punkts von der Ebene.

Der projizierte Punkt ist möglicherweise nicht die Antwort, da er sich außerhalb des Dreiecks befinden könnte. Daher müssen Sie zuerst eine Überprüfung durchführen. Die Berechnung entspricht der Berechnung der barzentrischen Koordinaten des projizierten Punkts relativ zum Dreieck. Wenn der projizierte Punkt als innerhalb des Dreiecks festgelegt wird, ist dies die Antwort. Wenn dies nicht der Wert ist, wird der nächste Punkt an einem der Ränder des Dreiecks abgerufen. Führen Sie für jeden der drei Kanten eine Suche durch. Das Ermitteln der Projektion des Abfrage Punkts auf einen Edge ist ein Prozess, der der Projektion auf das Dreieck ähnelt, aber eine Dimension kleiner ist. Eine orthogonale Projektion wird zuerst berechnet. Wenn sich der projizierte Punkt auf dem Rand befindet, ist dies die Antwort. Wenn dies nicht der Wert ist, wird der nächste Punkt an einem der beiden Endpunkte abgerufen. Führt eine Suche an den beiden Endpunkten aus. Das heißt, Sie berechnen den Abstand eines Abfrage Punkts von jedem einzelnen und vergleichen, welcher kleiner ist.

Die sorgfältige Untersuchung zeigt, dass es viele Wiederholungs Vorgänge gibt, wenn Sie alle Dreiecke durchlaufen, da eine Kante immer durch zwei Dreiecke und ein Scheitelpunkt von mindestens drei Kanten gemeinsam genutzt wird. Außerdem ist es nicht sehr interessant, den nächstgelegenen Punkt zu einem bestimmten Dreieck zu finden. Stattdessen sind Sie daran interessiert, den nächstgelegenen Punkt der gesamten Spiel Grenze zu finden. Dabei handelt es sich jedoch um ein bestimmtes Dreieck, in dem dies erreicht wird. Es gibt zwei Strategien, die Sie verwenden können, um die Suche zu beschleunigen.

**Strategie I**. Jeder Scheitelpunkt wird höchstens einmal verarbeitet. Jeder Edge wird höchstens einmal verarbeitet.

**Strategie II**. An jedem Punkt der Suche haben Sie einen besten Kandidaten mit der entsprechenden optimalen Entfernung. Wenn Sie durch eine schnell Überprüfung feststellen können, dass ein Dreieck nicht in der Lage ist, eine bessere Entfernung zu erzielen, muss die Berechnung nicht weiter fortgesetzt werden. Sie benötigen nicht den nächstgelegenen Punkt und die Entfernung für dieses Dreieck.

![Diagramm, das den Fluss der minimalen Zuordnung von "de" anzeigt.](images/gmmp-image120.png)

**Abbildung 32** : minimale Zuordnung der de-Zuordnung

In Abbildung 32 wird der allgemeine Logik Fluss für die Registerkarte "Code Map" gezeigt. Bei einem Abfrage Punkt wird zuerst die checkgamut-Funktion aufgerufen. Wenn der Punkt im Spiel ist, ist die Zuordnung ein No-op. Wenn der Punkt außerhalb des Gamut ist, nennen Sie projectpointumboundary. Wechseln Sie nun zu Abbildung 33. An diesem Punkt wird davon ausgegangen, dass die folgenden Werte berechnet wurden.

**(a)** Einheiten normaler Vektor für jedes Gamut-Begrenzungs Dreieck in Bezug auf das Standard-Punktprodukt.

**(b)** Vertex-Liste und Rand Liste zusätzlich zur Dreiecks Liste.

![Diagramm, das die "projectpointchanboundary"-Routine anzeigt.](images/gmmp-image122.jpg)

**Abbildung 33** : die "projectpointchanboundary"-Routine

All dies ist ein konstanter Aufwand, der zu einer Verringerung der Kosten führt, wenn genügend Abfragen für diese Farbskala-Grenze vorgenommen werden. Dies ist normalerweise der Fall, wenn Sie eine Transformations-LUT von einem Gerät zu einem anderen erstellen, bei dem es nur zwei fixierte Gamuts gibt und der Transform-LUT durch Punkte im einheitlich erfassten Raster verläuft. Sie berechnen die normalen Vektoren in Bezug auf das Standard-Punktprodukt, auch wenn das Konzept der kalkularität auf dem gewichteten Punktprodukt basiert, das von dem Abfrage Punkt abhängig ist, wie bereits erläutert. Der Grund hierfür ist, dass ein normaler Vektor in Bezug auf das gewichtete Punktprodukt auf einfache Weise vom normalen Vektor in Bezug auf das Standard-Punktprodukt abgerufen werden kann. Wenn n ₀ ein normaler Vektor in Bezug auf das Standard-Punktprodukt ist, dann

n = (J-Component von n ₀/w <sub>J</sub>, a-component of n ₀, b-Component of n ₀)

ist für das Dreieck in Bezug auf das gewichtete Punktprodukt normal. Aufgrund dieser Beziehung ist es immer noch vorteilhaft, eine vorabberechnung von n ₀ durchzuführen, auch wenn es auf der Grundlage des Abfrage Punkts angepasst werden muss.

Die "projectpointchanboundary"-Routine beginnt mit dem Zurücksetzen des verarbeitetes Verlaufs der Scheitel Punkte und Kanten. Dabei handelt es sich um Tabellen mit booleschen Flags, mit denen nachverfolgt wird, ob ein Scheitelpunkt oder Edge bereits besucht wurde. Außerdem setzt Sie die Variable "shortestdistance" auf "unendlich" zurück. Dies ist der maximale codierte Wert im verwendeten Gleit Komma Zahlensystem. Anschließend wird Sie durch eine Schleife ausgeführt, die mithilfe des processtriangle-Aufrufs den nächstgelegenen Punkt von jedem Dreieck aus sucht. Processtriangle ist die Routine zum Aktualisieren der shortestdistance-Variablen und ist in der Critical-Schleife eindeutig. Eine Optimierung besteht darin, zu beenden, wenn das Ergebnis ausreichend ist. Nach jedem Aufrufen von processtriangle wird die Variable "shortestdistance" untersucht. Wenn ein vordefinierter Schwellenwert erfüllt ist, können Sie den Vorgang abbrechen. Der vordefinierte Schwellenwert hängt von dem verwendeten Farbraum und der erforderlichen Genauigkeit des Farb Abbild Systems ab. Bei einer typischen Anwendung ist es nicht sinnvoll, unnötige Arbeiten durchzuführen, wenn der Farbunterschied kleiner ist, als von der menschlichen Vision erkannt werden kann. Für CIECAM02 ist dieser Farbunterschied 1. Verwenden Sie den Schwellenwert 0,005 in der Implementierung jedoch, um die Genauigkeit von Berechnungen beizubehalten, da dies nur ein Zwischenschritt in einer Kette von Transformationen sein kann.

Processtriangle implementiert die vorangehende Strategie II. Beim Abrufen eines normalen Vektors vom Standardvektor der vorab berechneten Einheit bis zum Dreieck in Bezug auf das Standard-Punktprodukt wird der Abstand des Abfrage Punkts auf die unendliche Ebene mit dem Dreieck berechnet, indem das Punktprodukt des Einheiten normalen Vektors und der queryvector, der Vektor von einer der Scheitel Punkte des Dreiecks, vertex1, zum Abfrage Punkt gebildet werden. , querypoint.

queryvector = querypoint-vertex1

Distance = \| normvector \* queryvector- \| / \| \| Normal Vektor\|\|

Dies ist eine relativ kostengünstige Berechnung, und die Entfernung ist erforderlich, um weitere Berechnungen auszuführen. Wenn diese Distanz nicht kleiner ist als die aktuelle beste Entfernung, shortestdistance, erzeugt dieses Dreieck keine bessere Distanz, da es nicht zu einer besseren Distanz als die Ebene mit der Ebene führt. In diesem Fall wird die Steuerung an die Dreiecks Schleife zurückgegeben. Wenn der Abstand kleiner als shortestdistance ist, haben Sie möglicherweise einen genaueren Punkt, wenn dieser Punkt innerhalb des Dreiecks liegt. Sie müssen einige "harte" Berechnungen durchführen, um dies zu bestimmen (allerdings ohne lineare Algebra). Wenn die beiden anderen Scheitel Punkte des Dreiecks vertex2 und vertex3 sind, bilden Sie die Basis Vektoren firstbasisvector und secondbasisvector.

firstbasisvector = vertex2-vertex1

secondbasisvector = vertex3-vertex1

Verwenden Sie das folgende lineare System von Gleichungen, um Sie und v zu lösen.

firstbasisvector \* queryvector = (firstbasisvector \* firstbasisvector) u + (firstbasisvector \* secondbasisvector) v

secondbasisvector \* queryvector = (secondbasisvector \* firstbasisvector) u + (secondbasisvector \* secondbasisvector) v

und die Bedingungen für den projizierten Punkt, der innerhalb des Dreiecks liegen soll, sind:

0, u. 1, 0. v. 1, und Sie + v, 1

Wenn nach dieser Berechnung festgestellt wird, dass der projizierte Punkt innerhalb des Dreiecks liegt, haben Sie einen neuen nächsten Punkt gefunden. der Abstand, den Sie am Anfang berechnet haben, ist die neue kürzeste Entfernung. Aktualisieren Sie in diesem Fall die Variablen shortestdistance und closestpoint. Wenn der projizierte Punkt außerhalb des Dreiecks liegt, finden Sie möglicherweise einen genaueren Punkt an einem seiner Ränder. Daher können Sie die processdge-Routine für jeden der drei Kanten aufrufen.

![Diagramm, das den Fluss der processdge-und processvertex-Routinen anzeigt.](images/gmmp-image124.jpg)

**Abbildung 34** : procesendge-und processvertex-Routinen

Die processdge-Routine implementiert Strategie I, wie in Abbildung 34 dargestellt. Procesmendge prüft zunächst, ob der Edge bereits verarbeitet wurde. Wenn dies der Fall ist, wird keine weitere Aktion durchgeführt. Wenn dies nicht der Fall ist, wird die orthogonale Projektion des Abfrage Punkts auf die unendliche Linie mit dem Rand berechnet. Die an der Berechnung beteiligte lineare Algebra ähnelt den vorherigen Dreiecks Gleichungen. Die Berechnung ist jedoch einfacher, Sie wird hier nicht beschrieben. Wenn der projizierte Punkt innerhalb des Edge liegt, finden Sie den Abstand des projizierten Punkts vom Abfrage Punkt aus. Wenn diese Entfernung kleiner als shortestdistance ist, haben Sie einen neuen nächsten Punkt gefunden. Aktualisieren Sie sowohl shortestdistance als auch closestpoint. Wenn der projizierte Punkt außerhalb des Edge liegt, wird processvertex für die beiden Endpunkte aufgerufen. Aktualisieren Sie vor dem Zurückgeben der Steuerung den Kanten Verlauf, sodass dieser Edge als "verarbeitet" gekennzeichnet ist.

Abschließend wird eine Beschreibung von processvertex angezeigt. Die "projectvertex"-Routine implementiert auch Strategie "I" und unterhält eine Vertex-Vertex Wie in Abbildung 34 dargestellt, wird zuerst überprüft, ob der Scheitelpunkt bereits verarbeitet wurde. Wenn dies der Fall ist, wird keine weitere Aktion durchgeführt. Wenn dies nicht der Fall ist, wird der Abstand des Scheitel Punkts vom Abfrage Punkt aus berechnet. Wenn die Entfernung kleiner als shortestdistance ist, aktualisieren Sie sowohl shortestdistance als auch closestpoint. Am Ende aktualisiert Sie den vertexverlauf, sodass dieser Scheitelpunkt als "verarbeitet" gekennzeichnet ist.

Wenn die äußere Steuerungs Schleife entweder alle Dreiecke erschöpft oder vor dem Erreichen des Farbunterschied-Schwellenwerts beendet wurde, wird auf die Variable closestpoint zugegriffen. Dies ist das Ergebnis von "mindemap". Der Aufrufer kann auch shortestdistance abrufen, wenn Sie interessiert sind, wie weit die zugeordnete Farbe von der Abfrage Farbe abgeleitet ist.

### <a name="hue-smoothing"></a>Farbton Glättung

![Diagramm, das zwei obere Ansichten von Hue Glättung anzeigt, das Original oben und den Farbton im unteren Bereich.](images/gmmp-image125.png)

**Abbildung 35** : Hue Glättung

Ein Problem tritt bei Vorgängen auf, die mit Hue eingeschränkt sind. Das heißt, der Vorgang berücksichtigt nur Variablen innerhalb einer Hue-Ebene. In Abbildung 35 wird ein Beispiel für einen "nicht kontinuierlichen" Farbton in den blauen Farben dargestellt. Innerhalb dieses Farbton Bereichs ist für bestimmte Hue-Winkel der Farbverlauf tangential. Dies bewirkt, dass die topologische Struktur der Hue Slices geändert wird. Im gezeigten Beispiel wird, wenn die Hue-Ebene über diesen Hue-Bereich hinausgeht, eine "Insel" und Teil Zusammenführungen. Diese Änderung in der Topologie führt dazu, dass Hue-spezifische Vorgänge nicht kontinuierlich sind. Beispielsweise ändert sich der Cusp bei festem Farbton abrupt, wenn sich der Hue-Winkel in diesem Bereich ändert.

Es gibt einen Color Science-Grund, warum es wünschenswert ist, Hue in bestimmten Vorgängen beizubehalten. Um das vorherige Problem zu beheben, müssen die ursprünglichen Gamut-Begrenzungs Dreiecke "Hue gläoniert" lauten. Im Allgemeinen ist eine Farbton Glättung eines Satzes von Farbskala-Begrenzungs Dreiecken eine Menge von Dreiecken, sodass (a) die Begrenzung eines neuen "Farbskala" bildet, die möglicherweise nicht dem tatsächlichen Geräte Spiel entspricht, und das durch den ursprünglichen Satz von Dreiecken definierte Farbskala enthält. und (b) die Dreiecke in der neuen Menge sind von der parallelen zu den Hue-Ebenen begrenzt.

Eine praktische Möglichkeit zum Abrufen eines aus dem Farbton geglättenen Dreiecke besteht darin, die konforme Hülle der ursprünglichen Scheitel Punkte zu verwenden. Wie in Abbildung 35 dargestellt, unterscheiden sich die Hue-Slices der-Kontur im problematischen Farbton ohne plötzliche Änderung der Topologie nahtlos.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Festlegen von primären und sekundären Replikaten in der Beschreibung der changesehe

Bestimmte gamingzuordnungs Methoden, wie z. b. huemap, hängen vom Speicherort der Geräte Primär-und sekundären Replikate ab. Bei Additiven Geräten sind die primären Replikate rot, grün und blau (R, G und B); und die sekundären Datenbanken sind Cyan, Magenta und gelb (C, M und Y). Bei subtraktiven Geräten sind die primären Replikate C, M und Y. und die sekundären Datenbanken sind R, G und B. Mit dem Gbd werden alle sechs Werte sowie weiß und schwarz (W und K) in einem Array von JAB-Farbwerten nachverfolgt. Diese Werte werden bei der Erstellung in die Beschreibung der changesetengrenze festgelegt. Für Ausgabegeräte können die primären Replikate durch das Ausführen von Kombinationen von Geräte Steuerungs Werten durch das Gerätemodell ermittelt werden. Bei Erfassungs Geräten eignet sich dieser Ansatz nicht für die Erstellung des Referenz-Gbd, da es nahezu unmöglich ist, ein Abbild zu erfassen, das einen vollständig übersättigten reinen Geräte Wert ergibt, z. b. (0,0, 0,0, 1,0). WCS-Geräteprofile enthalten die Indizes der primären Replikate im Erfassungs Ziel. Da diese Werte nicht in einem "ICC"-Profil enthalten sind, verwenden Sie nach der Umstellung auf den "Jab"-Wert in Bezug auf die Bedingungen der ICC-Anzeige die Werte, die nach der

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Festlegen der neutralen Achse in der Beschreibung der Gamut-Grenze

Die huemap und die relativen mincd-Farbskala-Zuordnungs Methoden verwenden die Geräte neutrale Achse für die Nachrichten. Bei den baselineausgabegeräten kann die neutrale Achse durch das Ausführen von Geräte neutralen Werten (R = G = B oder C = M = Y) durch die devicedecolormetric-Methode und dann durch die Farbgebung-Methode des CIECAM02-Objekts ermittelt werden. Erfassungsgeräte geben jedoch nicht immer einen Geräte neutralen Wert zurück, wenn ein neutrales Beispiel angezeigt wird. Dies trifft vor allem dann zu, wenn die Umgebungsbeleuchtung nicht vollständig neutral ist. WCS-Geräteprofile enthalten die Indizes der neutralen Beispiele im Ziel. Verwenden Sie diese Beispiele, um die neutrale Achse festzulegen. Da diese Informationen für die ICC-Profile nicht verfügbar sind, müssen Sie dieselbe Methode verwenden, die auch für Ausgabegeräte verwendet wird. Führen Sie Geräte neutrale Beispiele durch die devicedecolormetric-Methode aus, und verknüpfen Sie dann die Eingabewerte und die Farb Metrikergebnisse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




