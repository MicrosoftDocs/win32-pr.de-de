---
title: 'WCS-Farbauswahlpalette: Profilschema und Algorithmen'
description: 'WCS-Farbauswahlpalette: Profilschema und Algorithmen'
ms.assetid: 64b9871a-1b4f-4e9a-be4d-4c25b3198b91
keywords:
- Windows Color System (WCS), Gamut Map Model Profile (GMMP)
- WCS (Windows Color System), gamut map model profile (GMMP)
- Bildfarbverwaltung, Gamut-Kartenmodellprofil (GMMP)
- Farbverwaltung, Gamut-Kartenmodellprofil (GMMP)
- Colors, gamut map model profile (GMMP) (Farben,Gamut-Kartenmodellprofil (GMMP))
- Windows Color System (WCS), Profile
- WCS (Windows Color System), Profile
- Bildfarbverwaltung, Profile
- Farbverwaltung, Profile
- Farben, Profile
- gamut map model profile (GMMP)
- GMMP (Gamut-Kartenmodellprofil)
- GAMUT-Kartenmodellprofil für WCS
- schemas,gamut map model profile (GMMP)
- algorithms,gamut map model profile (GMMP)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7db5b7a26fe5832fe33095c5785e90ad0a6938649878ff279e101a7e5817cc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118037290"
---
# <a name="wcs-gamut-map-model-profile-schema-and-algorithms"></a>WCS-Farbauswahlpalette: Profilschema und Algorithmen

-   [Übersicht](#overview)
-   [Architektur des Gamut-Kartenmodellprofils](#gamut-map-model-profile-architecture)
-   [Generierung der Gamutgrenze](#generation-of-the-gamut-boundary)
-   [Das GMMP-Schema](#the-gmmp-schema)
-   [Die GMMP-Schemaelemente](#the-gmmp-schema-elements)
-   [GamutMapModel](#defaultbaselinegamutmapmodel-type)
    -   [Namespace](#namespace)
    -   [Version](#version)
    -   [Dokumentation](#documentation)
    -   [DefaultBaselineGamutMapModel-Typ](#defaultbaselinegamutmapmodel-type)
    -   [PlugInGamutMapType](#plugingamutmaptype)
    -   [ExtensionType](#extensiontype)
-   [Die GMMP-Baselinealgorithmen](#the-gmmp-baseline-algorithms)
-   [Ausrichten der neutralen Achsen](#aligning-the-neutral-axes)
    -   [Minimaler Farbunterschied (MinCD)](#minimum-color-difference-mincd)
    -   [BasicPhoto](#basicphoto)
    -   [Übersicht](#overview)
    -   [Fall einer einzelnen gamut-Shell](#the-case-of-single-gamut-shell)
    -   [Black-Erweiterung](#black-enhancement)
    -   [Fall von dualen gamut-Shells](#the-case-of-dual-gamut-shells)
    -   [Gründe für Änderungen an den CIE TC8-03-Empfehlungen](#reasons-for-changes-from-the-cie-tc8-03-recommendations)
    -   [Hue-Zuordnung](#hue-mapping)
-   [Gamut Boundary Description and Gamut Shell Algorithms](#gamut-boundary-description-and-gamut-shell-algorithms)
    -   [Triangulation der Gamutgrenze](#triangulation-of-the-gamut-boundary)
    -   [Begrenzungslinienelemente](#boundary-line-elements)
    -   [Gamut-Vorgang: CheckGamut](#gamut-operation-checkgamut)
    -   [Vollständige Hue-Ebene: Überschneiden](#full-hue-plane-intersect)
    -   [Gamut-Vorgang: CheckGamut (fortsetzung)](#gamut-operation-checkgamut-continued)
    -   [Minimale Farbunterschiede – Gamutzuordnung](#minimum-color-difference-gamut-mapping)
    -   [Farbtonglättung](#hue-smoothing)
    -   [Festlegen von primären und zweiten Binärdateien in der Gamut-Begrenzungsbeschreibung](#setting-primaries-and-secondaries-in-the-gamut-boundary-description)
    -   [Festlegen der neutralen Achse in der Gamut-Begrenzungsbeschreibung](#setting-the-neutral-axis-in-the-gamut-boundary-description)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Dieses Schema wird verwendet, um den Inhalt eines gamutmap-Modellprofils (GMMP) anzugeben. Die zugehörigen Baselinealgorithmen werden im folgenden Thema beschrieben.

Das grundlegende GMMP-Schema besteht aus allgemeinen Headerinformationen, einem optionalen Verweis auf ein bevorzugtes Gamut Map Model-Plug-In und Erweiterungstags.

Darüber hinaus stellt GMMP explizite Informationen zum gamut-Zielzuordnungsmodell bereit und stellt eine Richtlinie für das Gamut Map-Basismodell bereit, das verwendet werden soll, wenn das Zielmodell nicht verfügbar ist. Das Schema kann private Erweiterungsinformationen enthalten, enthält jedoch keine weiteren überflüssigen Informationen.

## <a name="gamut-map-model-profile-architecture"></a>Architektur des Gamut-Kartenmodellprofils

![Diagramm, das das Gamut-Kartenmodellprofil zeigt.](images/gmmp-image002.png)

Die Stichprobenentnahme des Farbraums des Ausgabegeräts erfolgt, indem die Farbmittel von 0,0 bis 1,0 mit einem Bruchteilschritt durchlaufen werden, wobei alle Kombinationen jedes Farbelements bei jedem Schritt akkumuliert werden. Anschließend werden sie mithilfe der DM::D eviceToColorimetricColors-Methode, gefolgt von der METHODE DER::ColorimetricToAppearanceColors, vom Farbraum des Geräts in den Farbdarstellungsbereich konvertiert. Im Folgenden wird ein Beispiel dafür veranschaulicht, wie dies für RGB erfolgt.


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



## <a name="generation-of-the-gamut-boundary"></a>Generierung der Gamutgrenze

Die Gamutgrenze besteht aus drei Komponenten: den primären, den neutralen Stichproben und den Shells. Die primären Primären werden generiert, indem die primären Geräteanwendungen verwendet und die Transformation DeviceToColorimetric/ColorimetricToAppearance angewendet wird. Die neutralen Stichproben werden generiert, indem der Farbraum des Geräts im neutralen Bereich entnommen und die gleiche Transformation angewendet wird. Bei drei farbigen Geräten (RGB oder CMY) werden die neutralen Stichproben so definiert, dass alle Farbelemente gleich sind, z. B. R == G == B. Für CMYK werden die neutralen Stichproben als C == M == Y == 0 definiert.

Die Faktoren, die die Daten beeinflussen, die zum Erstellen der Gamutgrenze verwendet werden, sind die Datenbeispiele (nur Baselinegeräte) und die Anzeigebedingungen. Die Schrittgröße, die zum Durchführen der vollständigen Stichprobenentnahme des Farbraums (für Monitore und für die shell-Shell) verwendet wird, ist eine interne Konstante und steht nicht für externe Bearbeitungen zur Verfügung. Das Ändern der Anzeigebedingungen ändert das Verhalten des Farbdarstellungsmodells (COLOR) und ändert die Form der Gamutgrenze, sodass Sie eine gamut-Begrenzung generieren müssen, die an das Anzeigebedingungenprofil gebunden ist. Wenn Beispieldaten verwendet werden, wie bei Baselinedruckern und Erfassungsgeräten, haben die Beispiele große Auswirkungen auf die Form des Referenz-Gamuts und wirken sich auf das Verhalten des Modells selbst aus.

Für Eingabegeräte, z. B. Kameras und Scanner, werden verschiedene Stichproben verwendet, um die Referenzshell und die Shell shell zu generieren. Die Verweisshell wird aus den Messungen generiert, die zum Initialisieren des Gerätemodells verwendet werden. Die shell-Shell wird ähnlich wie in der vorherigen Abbildung für Ausgabegeräte generiert. Der Unterschied besteht darin, dass Sie bei der Eingabe eines typischen Ziels keine vollständigen Werte erhalten (wobei R, G oder B = 255 ist). Sie müssen mithilfe des Gerätemodells extrapolieren, um diese Werte zu schätzen.

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



## <a name="the-gmmp-schema-elements"></a>Die GMMP-Schemaelemente

## <a name="gamutmapmodel"></a>GamutMapModel

Dieses Element ist eine Sequenz der folgenden Unterelemente:

1.  ProfileName-Zeichenfolge,
2.  DefaultBaselineGamutMapModel,
3.  Optionale Beschreibungszeichenfolge,
4.  Optionale Erstellungszeichenfolge,
5.  Optionale PlugInGamutMap und
6.  Optionaler ExtensionType.

**Validierungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="namespace"></a>Namespace

xmlns:gmm=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

targetNamespace=" http://schemas.microsoft.com/windows/2005/02/color/GamutMapModel "

### <a name="version"></a>Version

Version "1.0" mit der ersten Version von Windows Vista.

**Überprüfungsbedingungen:** 1.0 in Windows Vista. Versionen &lt; 2.0 sind auch gültig, um nicht breaking changes am Format zu unterstützen.

### <a name="documentation"></a>Dokumentation

Gamut Map Model Profile-Schema.

Copyright (C) Microsoft. All rights reserved.

**Validierungsbedingungen:** Jedes Unterelement wird durch seinen eigenen Typ überprüft.

### <a name="defaultbaselinegamutmapmodel-type"></a>DefaultBaselineGamutMapModel-Typ

UINT-Typ

Enumerationswerte:

<dl> "MinCD \_ Absolute"  
"MinCD \_ Relative"  
\_"SIGSELECT"  
"HueMap"  
</dl>

**Überprüfungsbedingungen:** Die Werte müssen mit einer der oben genannten Enumerationen übereinstimmen.

### <a name="plugingamutmaptype"></a>PlugInGamutMapType

Dieses Element ist eine Sequenz eines GUID GUIDType und aller Untergeordneten Elemente.

**Überprüfungsbedingungen:** Die GUID wird verwendet, um der GMM PlugIn DLL-GUID zu entsprechen. Es gibt maximal 100.000 benutzerdefinierte Unterelemente.

### <a name="extensiontype"></a>ExtensionType

Dieses Element ist eine optionale Sequenz beliebiger Unterelemente.

**Überprüfungsbedingungen:** Es können maximal 100.000 Unterelemente vorhanden sein.

## <a name="the-gmmp-baseline-algorithms"></a>Die GMMP-Baselinealgorithmen

## <a name="aligning-the-neutral-axes"></a>Ausrichten der neutralen Achsen

Die meisten gamut-Zuordnungsalgorithmen haben das Ziel, die neutrale Achse des Quellgeräts der neutralen Achse des Zielgeräts zuzuordnen: Weiß wechselt also zu Weiß, Schwarz zu Schwarz und Grau zu Grau. Dies wird teilweise behoben, indem die Helligkeit der Quellfarben so skaliert wird, dass sie dem Helligkeitsbereich des Zielgeräts entspricht. Damit wird das Problem jedoch nicht vollständig behoben.

Es ist eine physische Eigenschaft der meisten bildgebenden Geräte, dass die Empfindlichkeit des Geräts weiß nicht genau mit der Aggregatität des Geräts schwarz übereinstimmt. Monitor White hängt z. B. von der Summe der Zierlichkeiten und relativen Leuchtdichten der drei primären Primären ab, während monitor black von der Reflektion der Anzeigeoberfläche abhängt. Druckerwittchen hängt von der Sättigung des Papiers ab, während Druckerschwarz von der verwendeten Farbe oder dem verwendeten Toner abhängt. Ein Darstellungsmodell, das Das Gerät weiß genau der neutralen Achse des Darstellungsbereichs zuzuordnen (das Erscheinungsbild entspricht genau 0), ordnet das Gerät schwarz nicht der neutralen Achse zu. Da das Auge anfälliger für Farbunterschiede ist, wenn die Helligkeit zunimmt, werden Mittelgraue noch stärker als Geräteschwarz dargestellt. (Abbildung 1 veranschaulicht die Krümmung der neutralen Achsen in zwei Dimensionen. Tatsächlich bilden die neutralen Achsen eine komplexere Kurve in drei Dimensionen.)

Während die REGEL vorhersagt, dass diese geräteneutralen Farben farbig erscheinen, scheinen tatsächliche Beobachter dies zu kompensieren. Die meisten Personen betrachten diese geräteneutralen Werte nicht als schädlich. Für die meisten gamut-Zuordnungsmodelle sollten Sie daher weiterhin Quellneutrale den Geräteneutralen zuordnen.

Zum Zuordnen von Quellneutralen zu Geräteneutralen passen Sie die Gamutgrenzen für Quelle und Ziel und jedes Pixel an, wenn Sie den Gamutzuordnungsalgorithmus anwenden. Passen Sie zunächst jeden Wert in der Quellfarbe so an, dass die neutrale Achse des Quellgeräts bei der Helligkeit der Quellfarbe direkt auf die neutrale Achse des Darstellungsbereichs fällt. (Siehe linke Seite von Abbildung 1.) Passen Sie dann die Gamutbegrenzungsbeschreibung des Zielgeräts so an, dass jede Farbe auf der neutralen Achse des Zielgeräts an der Gamutbegrenzungsfarbe des Zielgeräts direkt auf die neutrale Achse des Darstellungsbereichs fällt. (Siehe die rechte Seite von Abbildung 1.)

![Diagramm, das das Diagramm Source Gamut Boundary (Gamut-Quellgrenze) auf der linken Seite und die Destination Gamut Boundary (Ziel gamut-Grenze) auf der rechten Seite zeigt.](images/gmmp-image004.png)

**Abbildung 1:** Ausrichtung der neutralen Achsen veranschaulicht. Links: Anpassen von Quellpunkten relativ zur neutralen Achse des Quellgeräts. Rechts: Passen Sie die Beschreibung der Ziel-Gamutgrenze relativ zur Beschreibung der Ziel-Gamutgrenze an.

Beachten Sie, dass Sie jeden Quellpixelwert relativ zur neutralen Achse bei diesem Helligkeitswert anpassen. Dadurch wird sichergestellt, dass Quellgeräteneutrale auf die neutrale Achse des Darstellungsmodells fallen. Sie verschieben auch alle anderen Farben bei dieser Helligkeit um die gleiche Menge, sodass es keine Diskontinuitäten in der Darstellung der Quellpalette gibt. Sie müssen sich um unterschiedliche Mengen bei unterschiedlichen Helligkeitsstufen verschieben, da die Quellgeräteneutrale auf den unterschiedlichen Helligkeitsstufen nicht als gleich heiter dargestellt werden. Dies ist natürlich keine triviale Transformation.

Die Verarbeitung der Zielgerätewerte ist etwas komplizierter. Zunächst passen Sie die gesamte Gamutgrenze des Ziels auf ähnliche Weise an, jedoch relativ zur neutralen Achse des Zielgeräts. Dies ist in Abbildung 1 auf der rechten Seite dargestellt. Durch diese Anpassung wird sichergestellt, dass graue Quellwerte den grauen Zielwerten zugeordnet werden. Dies ist der Bereich, in dem die Gamutzuordnungsalgorithmen ausgeführt werden.

In diesem Bereich wird das tatsächliche Verhalten des Zielgeräts jedoch nicht genau beschrieben. Sie müssen die Zuordnung umkehren, bevor gamut-zugeordnete Farben an das Darstellungsmodell und das Zielgerätemodell übergeben werden. Sie versetzen alle zugeordneten Werte um das Gegenteil des Offsets, der zuvor auf die neutrale Achse des Zielgeräts angewendet wurde. Dadurch wird die neutrale Zielachse wieder dem Wert zugeordnet, der ursprünglich von DER ZIP-Datei dargestellt wurde. Dies gilt für die Gamutgrenze und alle Zwischenwerte.

![Diagramm, das ein Diagramm zum Rückgängig machen der Ausrichtung der neutralen Achse des Zielgeräts zeigt.](images/gmmp-image008.png)

**Abbildung 2:** Rückgängig machen der Ausrichtung der neutralen Achse des Zielgeräts

### <a name="minimum-color-difference-mincd"></a>Minimaler Farbunterschied (MinCD)

Minimum Color Difference(MinCD) Relative and Absolute versions ( Minimum Color Difference(MinCD) Relative and Absolute versions – equivalent to the COLORimetric intent.

> [!Note]  
> MinCD GMM eignet sich für die Zuordnung von Grafiken und Liniengrafiken mit Logofarben (Spotfarben), Logofarbverläufen mit einigen out-of-gamut-Farben und für die letzte Phase der Korrekturtransformationen. MinCD GMM kann zwar für Bilder verwendet werden, die sich vollständig innerhalb des Zielformats befinden, es wird jedoch nicht für das allgemeine Rendern von Fotobildern empfohlen. Die Zuordnung von Nicht-Gamutfarben zu Farben auf der Gamutoberfläche des Ziels kann zu unerwünschten Artefakten führen, z. B. Ton- oder Farbverläufen in gleichmäßigen Farbverläufen, die die Gamutgrenze überschreiten. BasicPhoto wird für Bildbilder empfohlen. Wenn ein Foto- oder Contonebild eine andere Gamutzuordnung als BasicPhoto erfordert, sollte die Alternative darin sein, ein Plug-In zu erstellen, das diese Zuordnung implementiert, anstatt MinCD zu verwenden.

 

Unveränderliche Farben bleiben unverändert. Für Farben außerhalb des gamutigen Farbverlaufs werden Helligkeit und Glanz angepasst, indem der Punkt in der Ziel-Gamut ermittelt wird, der den minimalen Farbabstand von out-of-gamut-Eingabepunkten aufzuweisen hat. Der Farbabstand wird im JCh-Raum berechnet. Sie gewichten jedoch den Abstand in Helligkeit (J) und den Abstand in Kästchen (C) oder Farbton (h) anders. Für den Abstand in der Helligkeit wird eine von Eineme abhängige Gewichtungsfunktion verwendet, sodass das Gewicht für kleine Vergrößerungen kleiner und größer für großes Leinen ist, bis ein Schwellenwert erreicht wird, nach dem das Gewicht bei 1 bleibt, d. h. das gleiche Gewicht wie die Entfernung in Farbe oder Farbton. Dies entspricht der empfohlenen Verwendung für CMC und CIEDE2000. Es gibt zwei Varianten: relative farbmetrische und absolute farbmetrische.

**Relativ colorimetric:** Richten Sie zunächst die quell- und zielneutrale Achse wie zuvor beschrieben aus. Beschneiden Sie dann die angepasste Quellfarbe auf die angepasste Zielbereichsgrenze. (Siehe Abbildung 4. Zuordnung von Farben entlang konstanter Helligkeit.) Ändern Sie die Zielgerätewerte wie zuvor beschrieben neu. Bei einer monocoloren Ziel-Gamutgrenze bedeutet der Clipping von "clipping", dass der Farbwert (C) auf 0 (0,0) festgelegt ist.

**Absolute farbgebungsmetrik:** Dies ähnelt der relativen farbmetrischen, jedoch ohne die Ausrichtung der quell- und zielneutralen Achse. Der Quellwert wird direkt auf die neutrale Zielachse abgeschnitten. Beachten Sie, dass das Verhalten mit der relativen farbmetrischen Variante identisch ist, wenn sowohl die Quell- als auch die Ziel-Gamutgrenze monocolore sind. Das heißt, die Ausrichtung der neutralen Achsen wird ausgeführt, und dann wird die Folie auf 0 (null) abgeschnitten. Dadurch wird sichergestellt, dass eine angemessene Ausgabe erzielt wird, auch wenn sich die Medien und Farbmittel erheblich unterscheiden.

![Diagramm, das ein Diagramm für minCD-Clipping auf die angepasste Gamut zeigt.](images/gmmp-image010.png)

**Abbildung 3:** MinCD-Clipping zum angepassten Gamut

### <a name="basicphoto"></a>BasicPhoto

### <a name="overview"></a>Übersicht

BasicPhoto: entspricht der bevorzugten, bildlichen oder perzeptiven ABSICHT VON NAV.

Dieser Algorithmus ist eine Variante der vom CIE TC8-03 in CIE156:2004 beschriebenen Variante der sigmoidalen Sigmoidal lightness mapping und cusp scaling (SGCK). Dieser Variant-Algorithmus unterstützt GAMUT-Begrenzungsdeskriptoren (GBDs) mit dualen Gamut-Shells. Das heißt, GBDs mit einer Verweisshell und einer Shell für Shells. Der SGCK-Algorithmus, der ursprünglich nur eine gamutbasierte Shell in der GBD annimmt, basiert auf dem SIG \_ ALGORITHM-Algorithmus (Stumm 1999), der die sigmoidale Lightness-Zuordnung und die skalierungsbasierte Funktionsskalierung umfasst, die von Robin und Fairchild (1999) vorgeschlagen wurde, kombiniert mit der Abhängigkeit von GCUSP (Morweis, 1998). Sie behält die wahrgenommene Farbtonkonstante bei, z. B. den Farbtonwinkel in einem durch Farbton korrigierten Jab, und verwendet eine generische (bildunabhängige) sigmoidale Helligkeitsskalierung, die auf eine vom Farbton abhängige Weise angewendet wird, und ein 90-prozentiges Farbtonfunktionsskalieren. Die Variante skaliert entlang der Linien konstanter Helligkeit.

### <a name="the-case-of-single-gamut-shell"></a>Fall einer einzelnen gamut-Shell

Es ist hilfreich, den Algorithmus für den Fall zu überprüfen, dass sowohl Quell- als auch Ziel-GBDs nur eine gamut-Shell haben. In diesem Fall besteht der Algorithmus aus den folgenden Berechnungen.

Führen Sie zunächst die anfängliche Lightness-Zuordnung mithilfe der folgenden Formel aus:

![Zeigt die Formel für die anfängliche Helligkeitszuordnung an.](images/gmmp-image012.png) (1)

wobei *Jₒ* die ursprüngliche Helligkeit und *J <sub>R</sub>* die helligkeits lightness ist.

![Zeigt die zweite Formel für die Lightness-Zuordnung an.](images/gmmp-image014.png) (2)

Wenn die Gamutgrenze der Quelle monocolore ist, ist der Wert 0 (null) für die monocolore Grenze aufgrund einer neutralen Achsenausrichtung. Dies führt zu dem degenerieren Fall, in dem C gleich 0 (null) ist. In diesem Fall ist *p <sub>C</sub>* auf 1 festgelegt.

*p <sub>C</sub>* ist ein von einem Element abhängiger Gewichtungsfaktor (Mormil, 1998), der von der Ursprünglichen Farbe abhängt. C und *J <sub>S</sub>* sind das Ergebnis der ursprünglichen Helligkeit, die mit einer sigmoidalen Funktion zugeordnet wird.

 

Zum Berechnen von *J <sub>S</sub>* (Neu und Fairchild, 1999) wird zunächst eine eindimensionale Lookuptabelle (ONE-Dimensional Lookup Table, JIT) zwischen ursprünglichen und reproduzierenden Helligkeitswerten auf der Grundlage einer diskreten kumulativen Normalfunktion (S) eingerichtet.

![Zeigt eine Formel zum Berechnen von J s an.](images/gmmp-image016.png) (3)

wobei x ₀ und S die mittlere und Standardabweichung der Normalverteilung bzw. *i* = 0,1,2... *m*,*m* ist die Anzahl von Punkten, die in der BEZEICHNUNG verwendet werden. *S <sub>i</sub>* ist der Wert der kumulativen normal-Funktion für *i*  / *m* Prozent. Die Parameter hängen von der Helligkeit des schwarzen Punkts des Reproduktionsumfangs ab und können aus Tabelle 1 interpoliert werden. Ausführliche Informationen zum Berechnen dieser Parameter finden Sie unter Braun und Fairchild (1999, p. 391).

:::row:::
    :::column:::
        J <sub>minOut</sub>
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
       53.7
    :::column-end:::
    :::column:::
        56.8
    :::column-end:::
    :::column:::
        58.2
    :::column-end:::
    :::column:::
        60.6
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


**Tabelle 1:** Berechnung der Komprimierungsparameter "BasicPhoto Lightness"

Um S als Helligkeitszuordnungsmapping (S <sub>SOLL)</sub> zu verwenden, muss es zunächst in den Helligkeitsbereich von \[ 0.100 normalisiert \] werden. Die normalisierten Daten werden dann in den dynamischen Bereich des Zielgeräts skaliert, wie in Gleichung 4 gezeigt, wobei *J*<sub>min\ *Out*</sub> und *J*<sub>max\ *Out*</sub> die Werte der Helligkeit des schwarzen Punkts bzw. des weißen Punkts des Wiedergabemediums sind.

![Zeigt die Formel für S als Helligkeitszuordnungs-CSV an.](images/gmmp-image018.png) (4)

An diesem Punkt können die *J S-Werte* aus dem <sub>S-WERT</sub> abgerufen werden, indem zwischen den *m-Punkten* der entsprechenden *enthaltenen J O-* und *J S-Werte* interpoliert und die folgende Gleichung als Eingabe verwendet wird.

![Zeigt die Formel zum Abrufen der J S-Werte an.](images/gmmp-image020.png) (5)

J <sub>minIn</sub> ist der Helligkeitswert des schwarzen Punkts des ursprünglichen Mediums, J <sub>maxIn</sub> der Helligkeitswert des weißen Punkts des ursprünglichen Mediums und J <sub>O</sub> die ursprüngliche Helligkeit. Zur späteren Referenz können Sie durch *S* die sigmoidale Funktion bezeichnen, die wie in der folgenden Abbildung 4 dargestellt in der soeben beschriebenen Weise definiert ist.

![Diagramm, das das Diagramm für die Zuordnung von Karten entlang konstanter Helligkeit zeigt.](images/gmmp-image024.png)

**Abbildung 4:** Zuordnung von Farben mit konstanter Helligkeit

Wenn die Gamutgrenze des Ziels 1:0 ist, komprimieren Sie die Komprimierung entlang von Linien mit konstanter Helligkeit (l), und führen Sie die Komprimierung wie folgt aus.

![Zeigt die Formel zum Ausführen der Komprimierung an.](images/gmmp-image026.png)  (6)

wobei *d* den Abstand von *E* auf *l* darstellt; *g* stellt die mittlere Gamutgrenze dar. *r* stellt die Reproduktion dar; und *o* die ursprüngliche Abbildung 5.

![Diagramm, das das Diagramm für die Komprimierung von Farben und Helligkeit in BasicPhoto zeigt.](images/gmmp-image028.png)

**Abbildung 5:** Farb- und Helligkeitskomprimierung in BasicPhoto

Wenn die Gamutgrenze des Ziels monocolore ist, wird der Wert für die Klammer auf 0 (null) abgeschnitten.

Verwenden Sie drittens einen MinCD-Clip (weiter oben beschrieben), um Restfehler zu vermeiden.

### <a name="black-enhancement"></a>Black-Erweiterung

Der vorherige Algorithmus kann geändert werden, um schwarz zu verbessern, wenn das Ziel ein Druckergerät ist. Das Problem hat mit der Auswahl von *J <sub>minOut</sub>* zu tun, die in der Regel nicht der dunkelsten Farbe entspricht, die ein Drucker erzeugen kann.

Genauer gesagt ist die Farbe mit der höchsten Dichte, die durch Das Setzen von 100 Prozent Farben (oder der maximal möglichen Abdeckung, wenn die GCR-/Freihandbegrenzung wirksam ist) erhalten wird, in der Regel nicht "neutral" im Farbdarstellungsbereich. Siehe Abbildung 6. Anders ausgedrückt: Wenn für das Zielgerät eine neutrale minimale Helligkeit verwendet wird, wird der erstellte Lightness Scaler einer minimalen Helligkeit zugeordnet, die nicht der höchsten Dichte entspricht, die vom Drucker erzielt werden kann. Berücksichtigen Sie den weiteren Anwendungsfall von Monitor zu Drucker. Der Monitor black, R=G=B=0, wird dann als nicht die höchste Dichte gedruckt. Der Einfluss auf die Imagequalität besteht darin, dass es an Tiefe und Kontrast fehlt.

![Diagramm, das zeigt, wie der schwarze Punkt des Geräts dunkler als die neutrale minimale Helligkeit sein kann.](images/gmmp-seqfigure01.png)

**Abbildung 6:** Der schwarze Punkt des Geräts ist möglicherweise dunkler als die neutrale minimale Helligkeit.

Angenommen, das Ziel "Device Black Point" ist Jkakbk/JkCkh k. Wenn C k nicht 0 (null) ist, ist der schwarze Punkt des Geräts relativ zu CAB02 nicht neutral. Wenn Sie J k für das Ziel "neutrale minimale Helligkeit" bei der Erstellung des Lightness Scalers verwenden, d. b. festlegen

*J <sub>minOut</sub> = Jₖ*

und wenden Sie sie auf die allgemeine Quellshell an. Sie erhalten die in Abbildung 7 dargestellte Konfiguration. In der Abbildung entspricht die Farbtonebene h k.

![Diagramm, das den geänderten Lightness Scaler mit dem schwarzen Punkt des Zielgeräts zeigt.](images/gmmp-seqfigure02.png)

**Abbildung 7:** Geometrie mit dem geänderten Lightness Scaler mit schwarzem Punkt des Zielgeräts

Damit der nachfolgende Komprimierungsalgorithmus fortgesetzt werden kann, möchten Sie die maximale und minimale Helligkeit auf den Quell- und Zielshells ausrichten. Dies kann erreicht werden, indem die Zielshell zwischen J <sub>neutralMin</sub> und J k durch Verschieben von Punkten nach links angepasst wird. Darüber hinaus muss diese Transformation auf den gesamten Jab-Raum angewendet werden, nicht nur auf die Farbtonebene, die h k entspricht.

Die Transformation ist

![Zeigt die Formel für die Transformation an.](images/gmmp-seqfigure03.png)

Abbildung 8 zeigt die Auswirkungen der Transformation.

![Diagramm, das die Auswirkung des geänderten Lightness Scalers mit dem schwarzen Punkt des Zielgeräts zeigt.](images/gmmp-seqfigure04.png)

**Abbildung 8:** Geometrie mit dem geänderten Lightness Scaler mit schwarzem Punkt des Zielgeräts

Nach dem Anwenden des üblichen Algorithmus für die Komprimierung muss der Punkt "zurückversetzt" werden, d. h., die umgekehrte Transformation muss angewendet werden, um die endgültige zugeordnete Farbe zu erhalten.

![Zeigt die Formel für die inverse Transformation an, um die endgültige zugeordnete Farbe abzurufen.](images/gmmp-seqfigure05.png)

### <a name="the-case-of-dual-gamut-shells"></a>Fall von dualen gamut-Shells

Das Ziel besteht darin, SIG \_ GIGABIT für eine einzelne gamut-Shell für den Fall zu generalisieren, dass entweder die Quellgeräte-GBD oder die Zielgeräte-GBD eine Zwei-Shell-Struktur aufweist. Die innere Shell wird als Verweisshell bezeichnet, während die äußere Shell als Shell shell bezeichnet wird. Berücksichtigen Sie die folgenden Fälle.

(a) Sowohl die Quell-GBD als auch die Ziel-GBD verfügen über eine Zwei-Shell-Struktur.

(b) Die Quell-GBD verfügt über eine Zwei-Shell-Struktur. Die Ziel-GBD verfügt nur über eine Shell.

(c) Die Quell-GBD verfügt nur über eine Shell. Die Ziel-GBD verfügt über eine Zwei-Shell-Struktur.

(d) Sowohl die Quell-GBD als auch die Ziel-GBD verfügen nur über eine Shell.

Fall (d) ist der Fall einer einzelnen gamut-Shell, die zuvor erläutert wurde. In den Fällen (a), (b) und (c) können Sie die Helligkeitsskalierung generalisieren, um die zusätzlichen Informationen aus der Dual Shell-Struktur zu verwenden. In Fällen (b) und (c), in denen entweder die Quelle oder das Ziel nur über eine Shell verfügt, führen Sie eine "abgeleitete Verweisshell" ein, die in einem nachfolgenden Abschnitt erläutert wird: "Induced Reference Shell". Der allgemeine Algorithmus für zwei Shells wird für den Fall (a) beschrieben. Nachdem die Induced Reference Shell-Konstruktion erläutert wurde, kann der Algorithmus auch auf fall (b) und (c) angewendet werden. Wie bei der Komprimierung wird das Komprimierungsverhältnis durch die größten verfügbaren Shells bestimmt. Anders ausgedrückt: Wenn sowohl die Shell Shell als auch die Verweisshell verfügbar sind, wird die Shell Shell verwendet. Andernfalls wird die Verweisshell verwendet.

*Generalisierte Helligkeitsskalierung*

Das Vorhandensein von zwei Shells für Quell- und Ziel-GBD bedeutet, dass Sie einen Satz von vier Punkten aus der Quell-GBD einer entsprechenden Gruppe in der Ziel-GBD zuordnen müssen.

![Zeigt, wie eine Gruppe von vier Punkten einer entsprechenden Menge zugeordnet wird.](images/gmmp-image030.png)

Die Tiefgestellten haben die folgende Bedeutung.

o oder r: "original" (Quelle) oder "reproduktion" (Ziel)

min oder max: minimale neutrale Helligkeit oder maximale neutrale Helligkeit

pla oder ref: Shell oder Verweisshell

Die Reihenfolge in jedem Vierfachen entspricht auch der erwarteten relativen Größe dieser Punkte.

Die Lightness Rescaling Map verwendet die gleichen ersten beiden Gleichungen wie die einzelne Shell, *J S* wird jedoch wie folgt stückweise definiert.

![Zeigt die Formel für J S stückweise an.](images/gmmp-image032.png) (7)

Anders ausgedrückt: Sie ist innerhalb der Verweisshell sigmoidal und außerhalb linear. Weitere Informationen in Abbildung 9.

![Diagramm, das ein Diagramm für die Lightness Rescaling-Funktion für ZWEI-Shell-GBDs zeigt.](images/gmmp-image033.png)

**Abbildung 9:** Funktion zur Neuskalierung der Lichtheit für GBDs mit zwei Shells

**INDUZIERTE VERWEISSHELL**

Wenn eine GBD eine Shell und die andere GBD über zwei Shells verfügt, müssen Sie eine "Verweisshell" für die GBD mit nur einer Shell erstellen. Die vorhandene Shell, die als Verweisshell bezeichnet wird, wird in "Shell Shell" geändert. Tatsächlich müssen Sie keine Shell im vollständigen Jab-Bereich erstellen. Da bei der Neuskalierung der Lichtheit nur *J max* und *J min* verwendet werden, müssen Sie diese Werte nur für die ausgelöste Verweisshell auswerten. Es gibt zwei Fälle, je nachdem, welche GBD über zwei Shells verfügt.

Fall 1: Quell-GBD verfügt über zwei Shells; Die Ziel-GBD verfügt über eine Shell.

Bestimmen Sie die zielinduzierte Verweisshell auf der neutralen Achse. das heißt, der J <sub>r,\ min,\ ref</sub> und J <sub>r,\ max,\ ref</sub> der Shell. Dies erfolgt mit dem folgenden Algorithmus.

![Zeigt den Algorithmus an, um die zielinduzierte Verweisshell zu bestimmen.](images/gmmp-induced01.png)

Die Faktoren ? <sub>niedrig</sub> und ? <sub>hohe</sub> Kontrolle über die Trennung zwischen der Shell Shell shell und der Reference Shell. Der Wert 1 bedeutet, dass die Werte J <sub>min</sub> oder J mₐₓ übereinstimmen. Ihre Werte werden von der Quellverweisshell und der Quellshell "abgeleitet".

![Zeigt die Formel für die Werte der Quellverweisshell und der Quell-Shell an.](images/gmmp-induced02.png)

Die "Fudgefaktoren" F <sub>niedrig</sub> und F <sub>hoch</sub> sind *abstimmbare* Parameter, die zwischen 0 und 1 liegen müssen. Wenn der Wert 0 ist, werden die J <sub>min-</sub> oder J-mₐₓ direkt von den Quellshells abgeleitet. Wählen Sie in diesem Fall F <sub>low</sub> = 0,95 und F <sub>high</sub> = 0,1 aus.

Fall 2: Quell-GBD verfügt über eine Shell; Die Ziel-GBD verfügt über zwei Shells.

Bestimmen Sie die quellinduzierte Verweisshell auf der neutralen Achse. das heißt, der J <sub>o,\ min,\ ref</sub> und J <sub>o,\ max,\ ref</sub> der Shell. Dies erfolgt mit dem folgenden Algorithmus.

![Zeigt den Algorithmus an, um die zielinduzierte Verweisshell auf der neutralen Achse zu bestimmen.](images/gmmp-induced03.png)

Auch hier sind die Faktoren ? <sub>niedrig</sub> und ? <sub>hohe</sub> Kontrolle über die Trennung zwischen shell und reference shell. Der Wert 1 bedeutet, dass die Werte für J <sub>min</sub> oder J mₐₓ übereinstimmen. Ihre Werte werden von der Quellverweisshell und der Quellshell "abgeleitet":

![Zeigt den Algorithmus zum Steuern der Trennung zwischen der Verweisshell und der Quell-Shell an.](images/gmmp-induced04.png)

### <a name="reasons-for-changes-from-the-cie-tc8-03-recommendations"></a>Gründe für Änderungen aus den CIE TC8-03-Empfehlungen

BasicPhoto unterscheidet sich wie folgt von den CIE TC8-03-Empfehlungen.

1.  "List" wird nicht in Richtung des Cusp komprimiert, sondern entlang von Linien konstanter Lichtheit.
2.  Der Lichtbereich verwendet die Lichtheit der dunkelsten Farbe im Gamut und nicht den Punkt, an dem die Gamutgrenze die neutrale Achse überkreuzt.
3.  BasicPhoto unterstützt sowohl eine Gamut-Referenzshell als auch eine gamut-Shell, wenn eine der Gamutgrenzen in der Transformation über zwei Shells verfügt.
4.  BasicPhoto verwendet CIECAM02; anstelle von CIECAM97s zum Konvertieren in D65 bei 400 cd/m2 und anschließendes Verwenden des RIT IPT-Farbraums.

Die erste Änderung wurde vorgenommen, um Tonumkehrprobleme zu verhindern, die auftreten können, wenn die Komprimierung in Richtung einer Cusp verwendet wird. Wie in Abbildung 10 dargestellt, kann die Cusp-Komprimierung zu Tonumkehrungen führen. Dies kann passieren, wenn Farben von hohen Brillen heller sind als Farben von unteren Brillen. Da SGCK jedes Pixel unabhängig sowohl in der Lichtheit als auch in der Komprimierung komprimiert, ist es nicht garantiert, dass die Lichtheitsbeziehung zwischen den Pixelwerten nach der Komprimierung erhalten bleibt. Der bekannte Nachteil dieser Entscheidung, auf Linien konstanter Lichtheit zu komprimieren, ist, dass Sie Verluste von Glühbirnen einbußen können, insbesondere in Bereichen, in denen die Ziel-Gamutgrenze sehr flach ist, wie dies bei hell gelben Farben der Fall ist.

![Diagramm, das die Tonumkehr zeigt, die durch SGCK verursacht wird.](images/gmmp-toneinversion.png)

**Abbildung 10:** Tonumkehr durch SGCK

![Zeigt ein originales Bild einer Teekanne.](images/originalteapot.jpg)![Zeigt das SGCK-Ergebnis des Teekannenbilds an.](images/badteapot.jpg)![Zeigt das BasicPhoto-Ergebnis des Teekannenbilds an.](images/betterteapot.jpg)

**Abbildung 11:** Originalbild, SGCK-Ergebnis und BasicPhoto-Ergebnis

Abbildung 11 veranschaulicht diese Tonumkehr. Auf der linken Seite befindet sich ein Originalbild, das von einer Digitalkamera aufgenommen wurde. in der Mitte das Von SGCK reproduzierte Bild; und auf der rechten Seite das Bild, wie von BasicPhoto reproduziert. Das Bild auf der linken Seite befindet sich im Farbraum der Digitalkamera, die Bilder in der Mitte und rechts befinden sich im Farbraum einer DISPLAY-Videoanzeige. In der ursprünglichen Abbildung ist der obere Teil der Teekanne dunkler als der untere, da der untere Teil die Tischdecken wiederspiegelt, auf denen sie sich befindet. Im SGCK-Bild ist der obere Teil aufgrund der Tonumkehr tatsächlich leichter als der untere Teil. Außerdem ist es schwierig, die Elemente im unteren Teil der Teekanne widergespiegelt zu sehen. Auf der rechten Seite hat BasicPhoto die Tonumkehr korrigiert, und die reflektierten Artikel sind eindeutiger zu unterscheiden.

Die zweite Änderung wurde vorgenommen, um die Wiedergabe von fast schwarzen Farben auf Druckern zu verbessern, bei denen das schwarzste Schwarz nicht direkt auf die neutrale CIECAM02-Achse fällt. Die folgende Abbildung 12 zeigt ein in sRGB konvertiertes Bild. reproduziert für einen RGB-Drucker mit SGCK; und für denselben Drucker mit BasicPhoto reproduziert. Das Bild in der Mitte verwendet nicht das vollständige Schwarzgerät, sodass der im Original angezeigte Kontrast fehlt. Der Kontrast wird mit BasicPhoto wiederhergestellt.

![Zeigt das originale Bild eines Playsets an.](images/playstructure.jpg)![Zeigt das Bild des Playsets, das für einen R G B-Drucker mit SGCK reproduziert wurde.](images/playstructurebad.jpg)![Zeigt das Bild des Playsets, das mit BasicPhoto für einen R G B-Drucker reproduziert wurde.](images/betterplaystructure.jpg)

**Abbildung 12:** Erweitertes Schwarz

Die dritte Änderung wurde vorgenommen, um die Farbwiedergabe für Digitalkameras zu verbessern. Insbesondere in Fällen, in denen die Digitalkamera mithilfe eines Referenzziels profiliert wurde, enthält eine gamut boundary description, die aus gemessenen Farben erstellt wurde, möglicherweise nicht alle Farben, die in einer realen Szene erfasst werden können. Anstatt alle Farben auf den Gamut des gemessenen Farbziels zu beschneiden, lassen Sie die Extrapolierung zu, um eine randlose Gamutgrenze zu erzeugen. Der BasicPhoto-Algorithmus ist so konzipiert, dass er eine solche extrapolierte Gamutgrenze unterstützt.

Die vierte Änderung wurde vorgenommen, da CIECAM02 gut für die Gamutzuordnung funktioniert. Der von TC8-03 empfohlene Prozess der Konvertierung von Gerätefarben in D65 bei 400 cd/m2 und der anschließenden Verwendung des RIT-IPT-Farbraums ist rechenintensiv und zeitaufwändig.

### <a name="hue-mapping"></a>Hue-Zuordnung

HueMap ist das Äquivalent zur ABSICHT FÜR DIE Sättigung durch DIE FARBMAP.

Wenn entweder die Quell-Gamutgrenze oder die Ziel-Gamutgrenze keine primären Elemente enthält, wird dieses Modell auf das (relative) MinCD-Modell zurückverwendet, das in einem vorherigen Abschnitt beschrieben wurde. Beispielsweise Geräte, für die die primären Profile nicht bestimmt werden können (STELLUNGsprofile mit mehr als vier Kanälen) oder monotoneSTS-Profile.

Dieser Algorithmus passt zunächst den Farbton des Eingabefarbwerts an. Anschließend wird die Helligkeit und das Glühbirnen mithilfe einer Strichzuordnung gleichzeitig angepasst. Schließlich wird der Farbwert per Cliping sichergestellt, um sicherzustellen, dass er sich innerhalb des Gamut-Werts befindet.

Der erste Schritt besteht in der Bestimmung der "Hue-Scheiben". Suchen Sie die JCh-Werte für primäre und sekundäre Farben für quell- und zielgerät. Sie berücksichtigen nur die Hue-Komponenten. Dies führt zu einem primären oder sekundären Farbrad mit sechs Farbpunkten für jedes Gerät. (Siehe Abbildung 13.)

![Diagramm, das die Farbpaletten mit sechs Farbpunkten zeigt.](images/gmmp-figure12.png)

**Abbildung 13:** Hue-Rad

Bessere Ergebnisse können erzielt werden, wenn die quellblaue primäre Quelle nicht zum blauen primären Ziel rotiert wird. Stattdessen wird der quellblaue primäre Farbtonwinkel als zielblauer primärer Farbtonwinkel verwendet.

Führen Sie als Nächstes die Farbtonrotation für jede Eingabefarbe aus dem Quellbild aus.

a)Bestimmen Sie mithilfe des Farbtonwinkels der Eingabefarbe die Position der Farbe auf dem Quellfarbrad relativ zur zwei angrenzenden primären oder sekundären Farbe. Der Standort kann als Prozentsatz der Entfernung zwischen den primärerEntitäten bezeichnet werden. Beispielsweise beträgt der Farbton der Eingabefarbe 40 Prozent des Wegs vom Farbtonwert von Magenta bis zum Farbtonwert Rot.

b) Suchen Sie auf dem Ziel-Farbrad den zugeordneten Farbtonwinkel, z. B. 40 Prozent von Magenta zu Rot. Dieser Wert ist der Zieltonwinkel.

Im Allgemeinen sind die Quellprimär- und -zweiten Quellen nicht mit den gleichen Farbtonwinkeln wie die Zielprimär- und -nachwahlen identisch. Das heißt, der Zieltonwinkel ist in der Regel anders als der Quelltonwinkel.

Angenommen, die Hue-Rade erzeugen die folgenden Werte:

Quelle M = 295 Grad, Quelle R = 355 Grad.

Ziel M = 290 Grad, Ziel R = 346 Grad.

Wenn der Farbtonwinkel der Eingabefarbe 319 Grad beträgt, beträgt er 40 Prozent des Winkels (24 Grad) von Quelle M zu Quelle R. Der Winkel von M bis R beträgt 60 Grad, und der Winkel von M zum Eingabeton beträgt 24 Grad. Berechnen Sie den Winkel am Ziel, der 40 Prozent von Ziel M bis Ziel R (22 Grad) beträgt, sodass der Farbtonwinkel der Zielfarbe 312 Grad beträgt.

Berechnen Sie als Nächstes die Hue-Referenzpunkte für den Quellton und den Zielton. Um den Farbton-Referenzpunkt für einen bestimmten h-Wert (Hue) zu berechnen, möchten Sie den J-Wert (Lichtheit) und den C-Wert (Hue) ermitteln.

-   Suchen Sie den J-Wert des Hue-Referenzpunkts, indem Sie zwischen den J-Werten für die angrenzenden primären oder sekundären Punkte interpolieren, indem Sie die relative Position des Farbtons verwenden. Beispiel: 40 Prozent in diesem Beispiel.
-   Suchen Sie den maximalen C-Wert an diesem J-Wert und h-Wert. Sie verfügen nun über den JCh des Hue-Referenzpunkts für diesen Farbton.

![Diagramm, das ein Farbtonblatt zeigt.](images/gmmp-figure13.png)

**Abbildung 14:** Ein Farbtonblatt (Visualisierung einer Gamutbegrenzungsslice bei einem bestimmten Farbton)

Der nächste Schritt besteht darin, die Schubzuordnung für jedes Pixel zu berechnen. Visualisieren Sie zunächst ein Farbtonblatt aus der Quellfarbskala für den Farbtonwinkel der Quellfarbe und ein Farbtonblatt aus der Zielfarbskala für den Zielfarbwinkel, der während der Farbtonrotation berechnet wird. Die Farbtonblätter werden erstellt, indem ein "Slice" von der JCh-Gamutbegrenzungsoberfläche in einem bestimmten Farbtonwinkel entnommen wird (siehe Abbildung 14).

HINWEIS: Aus Leistungsoptimierungsgründen werden Farbtonblätter nicht tatsächlich erstellt. sie werden hier nur zu Visualisierungszwecken beschrieben und angezeigt. Die Vorgänge werden direkt auf der gamut-Begrenzungsoberfläche im angegebenen Farbton ausgeführt. Anschließend berechnen Sie die Farbtonverweispunkte, um die Schubzuordnung zu bestimmen.

-   Führen Sie eine Neuskalierung der Helligkeit durch, um die schwarz-weißen Punkte des Quellblatts dem Zielblatt zuzuordnen (siehe Abbildung 15). Die schwarz-weißen Punkte des Quelltonblatts werden linear den schwarzen und weißen Punkten des Zieltonblatts zugeordnet, indem alle J-Koordinaten der Quellgrenze skaliert werden. Der Farbton-zugeordnete Eingabefarbwert wird auf die gleiche Weise skaliert.

![Diagramm, das die Helligkeitszuordnung zeigt.](images/gmmp-figure14.png)

**Abbildung 15:** Helligkeitszuordnung

-   Bestimmen Sie die Farbtonverweispunkte für jedes Farbtonblatt. Wenden Sie eine Schubzuordnung auf das Quellblatt an, damit die Quell- und Zielverweispunkte übereinstimmen (siehe Abbildung 16). Der Bezugspunkt für eine Gamut bei einem bestimmten Farbton ist der interpolierte Farbtonverweispunkt zwischen den benachbarten primären Farbarten. Der Bezugspunkt des Quelltonblatts wird linear dem Bezugspunkt des Zieltonblatts zugeordnet. Dabei wird ein "Schubvorgang" verwendet, der die J-Achse sperrt, wobei die schwarzen Punkte und die weißen Punkte stationär bleiben. Die schwarzen Punkte, weißen Punkte und Bezugspunkte der Quell- und Zieltonblätter sollten übereinstimmen.
-   Wenden Sie die Schubzuordnung auf den Lichtheits-angepassten Eingabefarbwert an. Die J- und C-Koordinaten des Quellfarbwerts werden proportional skaliert, relativ zum Abstand von der J-Achse.
-   Als Nächstes wird eine dezente, von der Helligkeit abhängige Komprimierung in Richtung des J-Werts des Farbtonverweispunkts auf dem scharren zugeordneten Farbpunkt durchgeführt. Die Komprimierung für den Farbtonverweis J erfolgt gammaähnlicher Weise, wobei Weiß, Schwarz, Grau und Punkte auf dem Farbtonverweis J nicht betroffen sind. Alle anderen Punkte tendieren zu dem Farbtonverweis J in einer reibungslosen Weise, die sich leicht in der Nähe des Farbtonverweises J annähert, wobei der Farbton konstant bleibt. Die Abhängigkeit von der Färbung stellt sicher, dass neutrale Farben nicht betroffen sind, und die Auswirkung auf Farben mit höherem Farbton wird erhöht.

Im Folgenden finden Sie eine mathematische Beschreibung der Helligkeitskomprimierung für den Farbtonverweis J oder das Anpassen des J-Werts des Zielpunkts. Er wird als Zielpunkt bezeichnet, da er dem Ziel gamut zugeordnet wurde.

Berechnen Sie zunächst "factorC" (Abhängigkeitsfaktor für Denkfaktor) für den Zielpunkt, der bestimmt, wie viel Auswirkung die Helligkeitskomprimierung haben wird. Punkte in der Nähe oder auf der J-Achse weisen nur wenige oder gar keine Komprimierung auf. An Punkten, die weiter von der J-Achse entfernt sind (hohe Färbung), wird mehr Komprimierung angewendet. Multiplizieren Sie mit 0,5, um sicherzustellen, dass factorC kleiner als 1 ist, da sourceC möglicherweise etwas größer als referenceC, aber nicht doppelt so groß sein kann.

factorC = (destinationC/referenceC) ? 0,5

Dabei gilt:

destinationC ist der C-Wert des Zielpunkts.

referenceC ist der C-Wert des Hue-Referenzpunkts.

Bestimmen Sie als Nächstes, ob der Zielpunkt J oberhalb oder unterhalb des Farbtonverweises J liegt. Gehen Sie im obigen Beispiel wie folgt vor:

1.  Berechnen Sie "factorJ" für den Zielpunkt relativ zum referenceJ. Dieser FactorJ-Wert liegt zwischen 0 und 1 (0, wenn für referenceJ; 1 bei maxJ).
2.  factorJ = (destinationJ - referenceJ) / (maxJ - referenceJ)

    Dabei gilt:

    destinationJ ist der J-Wert des Zielpunkts.

    referenceJ ist der J-Wert des Hue-Bezugspunkts.

    maxJ ist der maximale J-Wert des Gamuts.

3.  Wenden Sie eine gammaähnliche Potenzfunktion auf factorJ an, wodurch FactorJ um einen bestimmten Betrag reduziert wird. In diesem Beispiel wird die Potenz von 2 (das Quadrat) verwendet. Subtrahieren Sie den reduzierten FactorJ vom ursprünglichen FactorJ, und multiplizieren Sie das Ergebnis mit dem gesamten J-Bereich über dem primären ReferenceJ, um das "deltaJ" zu finden, das die Änderung in J nach der Helligkeitskomprimierung darstellt, aber nicht die Abhängigkeit der Potenz enthält.
4.  deltaJ = (factorJ - (factorJ ? factorJ)) ? (maxJ – referenceJ)

5.  Wenden Sie factorC auf das DeltaJ an (je höher der Füllungsfaktor, desto größer der Effekt), und berechnen Sie den neuen J-Wert für den Zielpunkt.
6.  destinationJ = destinationJ – (deltaJ ? factorC)

Wenn der J-Wert für den Zielpunkt unter referenceJ liegt, wird eine ähnliche Berechnung wie in den vorherigen Schritten A-C ausgeführt. Dabei wird minJ anstelle von maxJ verwendet, um den Bereich in J zu ermitteln, um den FactorJ zu berechnen, und die Polarität der Vorgänge "unterhalb" des referenceJ zu berücksichtigen.

factorJ = (referenceJ - destinationJ) / (referenceJ - minJ)

deltaJ = (factorJ - (factorJ ? factorJ)) ? (referenceJ – minJ)

destinationJ = destinationJ + (deltaJ ? factorC)

Dabei gilt:

minJ ist der J-Mindestwert des Gamuts.

Der Farbpunkt für Eingabefarbpunkte wird linear (wenn möglich) entlang konstanter Helligkeit proportional zum maximalen Farbwert der Quell- und Zielfarbwerte bei diesem Farbton und dieser Helligkeit erweitert. In Kombination mit der vorherigen, von der Helligkeit abhängigen Komprimierung trägt dies dazu bei, die Sättigung beizubehalten, da die Schubzuordnung mithilfe der Verweispunkte manchmal dazu führt, dass der Quellpunkt in der Färbung überkomprimiert wird (siehe Abbildung 16).

![Diagramm, das die Schubarzuordnung zeigt, die den Farbtonverweispunkten entspricht, vor dem Schub auf der linken Seite, nach dem Schub auf der rechten Seite.](images/gmmp-shearmapping.png)

**Abbildung 16:** Shearzuordnung, Helligkeitskomprimierung in Richtung Farbtonverweis J und Glanzerweiterung

Im Folgenden finden Sie eine mathematische Beschreibung des Vorgangs für die Erweiterung der Vergrößerung oder das Anpassen des C-Werts des Zielpunkts. Er wird als Zielpunkt bezeichnet, da er schubschnell zugeordnet und die Helligkeit in der Ziel-Gamut komprimiert wurde.

1.  Bestimmen Sie vor der Schubzuordnung sourceExtentC (das Füllzeichen bei der Helligkeit und dem Farbton des Quellpunkts).
2.  Bestimmen Sie nach der Schubzuordnungs- und Helligkeitskomprimierung, die den Quellpunkt in den Zielpunkt transformiert, den destExtentC (den Füllbereich bei der Helligkeit und dem Farbton des Zielpunkts).
3.  Wenn sourceExtentC größer als der destExtentC ist, ist keine Anpassung des Zielpunkts erforderlich, und Sie können den nächsten Schritt überspringen.
4.  Passen Sie destinationC (das Farbchen des Zielpunkts) so an, dass es bei dieser Helligkeit und diesem Farbton in den Ziel-Sgrad passt.
5.  destinationC = destinationC ? (destExtentC/sourceExtentC)

    Dabei gilt:

    destinationC ist der C-Wert des Zielpunkts.

    sourceExtentC ist der maximale C-Wert der Quell gamut bei der Helligkeit und dem Farbton des Quellpunkts.

    destExtentC ist der maximale C-Wert der Ziel gamut bei der Helligkeit und dem Farbton des Zielpunkts.

Führen Sie abschließend den Mimimum-Abstandsclipping aus. Wenn sich die Farbtonrotierung, die Helligkeitseinstellung und die Schubarzuordnungseingabefarbe noch etwas außerhalb der Ziel gamut befindet, clippen Sie sie (verschieben Sie sie) an den nächstgelegenen Punkt an der Gamutgrenze des Ziels (siehe Abbildung 17).

![Diagramm, das die Minimale Entfernungsabschneidung zeigt.](images/gmmp-figure15.png)

**Abbildung 17:** Abschneiden des Mindestabstands

## <a name="gamut-boundary-description-and-gamut-shell-algorithms"></a>Gamut Boundary Description and Gamut Shell Algorithms

Die Gamutbegrenzungsfunktion des Geräts verwendet die Gerätemodell-Engine und analytische Parameter, um eine farbliche Gamutgrenze des Geräts abzuleiten, die als indizierte Scheitelpunktliste der Hülle der Geräte gamutbeschrieben wird. Die Hülle wird unterschiedlich berechnet, je nachdem, ob Sie mit additiven Geräten wie Monitoren und Projektoren oder subtrahierten Geräten arbeiten. Die indizierte Scheitelpunktliste wird in CIEJab gespeichert. Die Struktur der indizierten Scheitelpunktliste ist für die Hardwarebeschleunigung durch DirectX optimiert.

Dieser Ansatz verfügt über viele bekannte Lösungen. Wenn Sie im Web nach "convex hull DirectX" suchen, erhalten Sie mehr als 100 Treffer. Es gibt z. B. einen Verweis aus 1983 zu diesem speziellen Thema (Computergrafiktheorie und -anwendung, "Ship untereinander, b-spline oberflächen, and cadcam", S. 34-49) mit Verweisen von 1970 bis 1982 zu diesem Thema.

Die Sammlung von Punkten kann anhand extern verfügbarer Informationen wie folgt bestimmt werden:

-   Punkte für die Referenzshell für Monitore werden mithilfe einer Stichprobenentnahme des Farbcubes im Farbraum des Geräts generiert.
-   Punkte für die Referenzshell für Drucker und Erfassungsgeräte werden aus den Beispieldaten abgerufen, die zum Initialisieren des Modells verwendet werden.
-   Punkte für die Verweisshell für scRGB und sRGB werden mithilfe einer Stichprobenentnahme des Farbcubes für sRGB generiert.
-   Punkte für die shell-Shell für Erfassungsgeräte werden mithilfe einer Stichprobenentnahme des Farbcubes im Farbraum des Geräts generiert.
-   Punkte für die Referenzshell für Projektoren werden mithilfe einer Stichprobenentnahme eines Polyeders im Farbcube im Farbraum des Geräts generiert.
-   Punkte für die mögliche Shell für breite Dynamische Bereichsfarbräume werden mithilfe einer Stichprobenentnahme des Farbcubes im Raum selbst generiert.

Sie können eine Scheitelpunktliste erstellen, die die Farbgeräte-Gamut effizient beschreibt, wenn Sie ein Geräteprofil und Systemunterstützungsdienste verwenden.

Bei Ausgabegeräten beschreibt die Gamutgrenze den Farbbereich, der vom Gerät angezeigt werden kann. Eine gamut-Grenze wird aus den gleichen Daten generiert, die zum Modellieren des Verhaltens des Geräts verwendet werden. Konzeptionell können Sie eine Stichprobenentnahme des Farbbereichs ausgeben, den das Gerät erzeugen kann, die Farben messen, die Messungen in den Darstellungsbereich konvertieren und dann die Ergebnisse verwenden, um die Gamutgrenze zu erstellen.

Eingabegeräte sind schwieriger. Jedes Pixel in einem Eingabebild muss einen Wert aufweisen. Jedes Pixel muss in der Lage sein, jede Farbe in der realen Welt in irgendeiner Weise darzustellen. In diesem Sinn sind keine Farben für ein Eingabegerät "out of gamut", da sie immer dargestellt werden können.

Alle digitalen Bildformate weisen einen festen dynamischen Bereich auf. Aufgrund dieser Einschränkung gibt es immer einige unterschiedliche Unterschiedliche, die dem gleichen digitalen Wert zugeordnet sind. Daher können Sie keine 1:1-Zuordnung zwischen realen Farben und Digitalkamerawerten einrichten. Stattdessen wird die Gamutgrenze gebildet, indem ein Bereich von realen Farben abschätzet wird, die die digitalen Antworten der Kamera erzeugen können. Sie verwenden diesen geschätzten Bereich als Gamut für das Eingabegerät.

Primäre Typen sind enthalten, um eine Gamutzuordnung vom Typ "Absichtstyp" für Geschäftsgrafiken bereitzustellen.

Im echten objektorientierten Stil abstrahieren Sie die zugrunde liegende Darstellung der Gamutgrenze. Dadurch können Sie die Darstellung in Zukunft flexibel ändern. Um den gamut-Begrenzungsdeskriptor (GBD) zu verstehen, der im neuen allgemeinen Tabellenauswertungsmodul verwendet wird, müssen Sie zunächst verstehen, wie gamut-Zuordnungsalgorithmen (GAAs) funktionieren. Bisher wurden GMAs entwickelt, um die Anforderungen der Grafikcommunity zu erfüllen. das heißt, Bilder zu reproduzieren, die bereits ordnungsgemäß für das Gerät gerendert wurden, auf dem das Eingabebild erstellt wurde. Das Ziel grafischer GmAs besteht darin, die bestmögliche Wiedergabe des Eingabebilds auf dem Ausgabegerät zu ermöglichen. Die neue CTE-GBD wurde entwickelt, um vier wichtige Probleme zu lösen.

Da das Eingabebild für das Eingabegerät gerendert wird, passen alle Farben in den Bereich zwischen dem weißen Punkt des Mediums und dem schwarzen Punkt. Angenommen, das Bild ist ein Foto einer Szene, in der ein diffuses Weiß vorliegt, z. B. eine Person in einem weißen T-Shirt, und ein Glanzlicht, z. B. Licht, das von einem Fenster oder einem Chrome-Bumper reflektiert wird. Die Szene wird auf dem Eingabemedium gerendert, sodass die Glanzlichter dem weißen Punkt des Mediums zugeordnet und das diffuse Weiß einer neutralen Farbe zugeordnet wird, die dunkler als der weißer Punkt des Mediums ist. Die Wahl, wie Farben aus der Szene dem Eingabemedium zugeordnet werden, ist sowohl eine szenenabhängige als auch eine optische Entscheidung. Wenn das Glanzlicht in der ursprünglichen Szene fehlt, wird das diffuse Weiß wahrscheinlich dem weißen Punkt des Mediums zugeordnet. In einer Szene mit vielen Hervorhebungsdetails würde mehr Bereich zwischen dem Glanzlicht und dem diffusen Weiß übrig bleiben. In einer Szene, in der die Hervorhebung nicht signifikant ist, kann nur ein sehr kleiner Bereich übrig bleiben.

Bei vorab gerenderten Bildern ist die Gamutzuordnung relativ einfach. Im Grunde wird der weißer Punkt des ursprünglichen Mediums dem weißen Punkt des Reproduktionsmediums zugeordnet, der schwarze Quellpunkt wird dem schwarzen Zielpunkt zugeordnet, und der großteil der Zuordnung ist abgeschlossen. Die verschiedenen vorhanden GMAs bieten Variationen für die Zuordnung anderer Punkte auf der Tonskala des Quellmediums und verschiedene Möglichkeiten, out-of-gamut-Werte zu verarbeiten. Die Zuordnung von Weiß zu Weiß und Schwarz zu Schwarz ist jedoch in diesen Variationen konsistent. Diese Implementierung erfordert, dass weiß über einem J \* von 50 und schwarz unter einem J \* von 50 liegt.

Nicht alle Farbcodierungen beschränken Farbbereiche für Eingabebilder. Der IEC-Standardfarbcodierungs-scRGB (IEC 61966-2-2) bietet 16 Bits für jeden der drei Farbkanäle Rot, Grün und Blau (RGB). In dieser Codierung wird der Verweis schwarz nicht als RGB-Triple (0, 0, 0), sondern als (4096, 4096, 4096) codiert. Verweis weiß ist als codiert (12288, 12288, 12288). Die scRGB-Codierung kann verwendet werden, um Glanzlichter und Schattendetails darzustellen. Sie enthält RGB-Triples, die physisch nicht möglich sind, da sie negative Lichtmengen erfordern, sowie Codierungen, die sich außerhalb des CIE-Locus befinden. Natürlich kann kein Gerät möglicherweise alle Farben im scRGB-Gamut erzeugen. Tatsächlich kann kein Gerät alle Farben erzeugen, die ein Mensch sehen kann. Daher können Geräte den scRGB-Gamut nicht ausfüllen, und es wäre hilfreich, den Teil des Gamuts darstellen zu können, den sie füllen. Jedes Gerät verfügt über einen Bereich von Werten im scRGB-Bereich, den es erzeugen kann. Dies sind die "erwarteten" Farben für das Gerät. Es wäre überraschend, dass das Gerät Farben außerhalb dieses Gamuts erzeugt. Es gibt eine definierte Transformation vom scRGB-Raum zum Darstellungsbereich, sodass jedes Gerät auch über einen Bereich von Darstellungswerten verfügt, die es voraussichtlich reproduzieren wird.

Sowohl bei scRGB als auch bei Eingaben von Erfassungsgeräten, die mit einem festen Ziel gekennzeichnet sind, ist es möglich, einen Wert außerhalb des erwarteten Wertebereichs abzurufen. Wenn jemand eine Kamera an ein Testziel kalibriert, und erfasst dann eine Szene mit Glanzlichtern. Es gibt möglicherweise Pixel, die hell als der weiße Punkt des Ziels sind. Dasselbe kann passieren, wenn ein natürlich auftretendes Rot freundlicher als das Zielrot ist. Wenn ein Benutzer ein scRGB-Bild von einem Gerät übernimmt und dann die Farben im Bild manuell bearbeitet, ist es möglich, Pixel zu erstellen, die außerhalb des erwarteten Bereichs des Gerätebereichs liegen, obwohl sie sich innerhalb des vollständigen scRGB-Gamuts befinden.

Ein zweites Problem scheint zunächst nicht damit in Zusammenhang zu stehen. Sie tritt auf, wenn Sie ein Farbziel verwenden, um ein Eingabegerät wie eine Kamera oder einen Scanner zu charakterisieren. Reflektierende Ziele werden in der Regel auf Papier erzeugt und enthalten eine Reihe farbiger Patches. Manufaturer stellen Datendateien mit Farbmessungen bereit, die unter einer festen Anzeigebedingung für jeden Farbpatch durchgeführt werden. Farbprofilerstellungstools erstellen eine Zuordnung zwischen diesen gemessenen Werten und den Werten, die von den Farbsensoren auf den Geräten zurückgegeben werden. Das Problem besteht darin, dass diese Farbziele häufig nicht den gesamten Bereich der Gerätewerte abdecken. Beispielsweise kann der Scanner oder die Kamera den Wert (253, 253, 253) für den weißen Verweispunkt zurückgeben, und ein roter Verweispatch kann den RGB-Wert (254, 12, 4) aufweisen. Diese stellen den Bereich der erwarteten Werte für das Eingabegerät dar, basierend auf den Zielwerten. Wenn Sie das Eingabegerät basierend auf den Antworten auf das Ziel charakterisieren, erwarten Sie nur Farben innerhalb dieses schmalen Bereichs. Dieser Bereich ist nicht nur kleiner als der Farbbereich, den Menschen sehen können, sondern auch kleiner als der Farbbereich, den das Gerät erzeugen kann.

In beiden Fällen ist es schwierig, die Gamut des Eingabegeräts oder -bilds zu schätzen, obwohl eine Verweis-Gamut oder Messungen vorhanden sind. Im ersten Problem ist die skala Gamut des Eingabegeräts kleiner als die vollständige Gamut von scRGB. Im zweiten Problem ist die Verweis-Gamut des Ziels kleiner als die vollständige mögliche Gamut des Eingabegeräts.

Das dritte Problem umfasst die Tonzuordnung. Es wurden viele Modelle von Gamutgrenzen vorgeschlagen, die vorab gerenderte Bilder, die in der Grafischen Grafik verwendet werden, angemessen darstellen können, z. B. die GBD der Stumm- und Fairchild Mountain Range (Stumm \[ 97) \] und Mordos Segment Maxima-Begrenzungsdeskriptor (Mor gigabyte \[ 98 \] ). Diese Modelle bieten jedoch nur Informationen über die Extreme der Gamut des Geräts. Es fehlen Informationen zu anderen Punkten in der Tonalitätszuordnung. Ohne solche Informationen können GMAs nur grobe Schätzungen der optimalen Tonzuordnung vornehmen. Schlechter noch: Diese Modelle bieten keine Hilfe für den erweiterten dynamischen Bereich in scRGB und in Digitalkamerabildern.

Wie wird dieses Problem in der Foto- und Videographik behoben? Die Kamera erfasst ein Bild. Experten könnten darüber nachdenken, wie viel Rendering auf dem Erfassungsgerät erfolgt. sie stimmen jedoch zu, dass es sich nicht um einen signifikanten Betrag handelt. Beide Technologien ordnen dem weißen Punkt des Mediums kein diffuses Weiß in einer erfassten Szene zu. Ebenso ordnen sie den schwarzen Punkt aus der Szene nicht dem schwarzen Punkt des Mediums zu. Das Verhalten von Fotofolien wird im Dichteraum mithilfe einer Merkkurve beschrieben, die häufig als "Hurter" und "Driffield" oder "H&D"-Kurve bezeichnet wird. Die Kurve zeigt die Dichte der ursprünglichen Szene und die resultierende Dichte für den Film. Abbildung 18 zeigt eine typische H&D-Kurve. Die x-Achse stellt eine zunehmende Protokollbelichtung dar. Die y-Achse stellt die Dichte auf der Folie dar. Fünf Verweispunkte sind in der Kurve markiert: Schwarz ohne Detail, das die minimale Dichte auf dem Negativen darstellt; schwarz mit Details; Verweis auf mittelgraue Karte; weiß mit Details; und weiß ohne Details. Beachten Sie, dass zwischen Schwarz ohne Detail (das Geräteschwarz darstellt) und Schwarz mit Details (Schattenschwarz) Platz vorhanden ist. Auf ähnliche Weise gibt es Leerzeichen zwischen Weiß mit Details (diffuses Weiß) und Weiß ohne Detail (was Gerätewittchen darstellt).

![Diagramm, das die H- und D-Kurve für Denkfolien zeigt.](images/gmmp-image079.png)

**Abbildung 18:** H&D-Kurve für Folien

Die Videobranche bietet "Headroom" und "Footroom" in Bildern. In der ITU 709-Spezifikation wird die Leuchtdichte (Y) in 8 Bits mit einem Bereich von 0 bis 255 codiert. Der Verweis black wird jedoch bei 15 codiert, und verweis white wird als 235 codiert. Dadurch bleibt der Codierungsbereich zwischen 236 und 255, um Glanzlichter darzustellen.

Die Videobranche stellt ein im Wesentlichen geschlossenes Schleifensystem dar. Obwohl es viele verschiedene Gerätehersteller gibt, basieren Videosysteme auf Referenzgeräten. Es gibt eine Standardcodierung für Videobilder. Es ist nicht erforderlich, eine gamut-Grenze mit Videobildern zu kommunizieren, da alle Bilder für die Reproduktion auf demselben Referenzgerät codiert sind. Film ist auch eine geschlossene Schleife, da zwischen verschiedenen Komponenten keine Zwischendaten vermittelt werden müssen. Sie möchten eine Lösung, mit der Bilder von Geräten mit unterschiedlichen Gamuts und darstellungen vorab gerenderter und nicht gerenderter Szenen bei der Ausgabe mit unterschiedlichen Gamuts reproduziert werden können.

Ein viertes Problem, das der neue CTE lösen muss, besteht darin, dass die visuell grauen Farben, die von einem Gerät erzeugt werden, z. B. wenn red=green=blue auf einem Monitor angezeigt wird, häufig nicht auf die neutrale Achse des GERÄTs fallen (wenn die Farbe = 0,0 ist). Dies führt zu großen Schwierigkeiten bei GMAs. Damit GMAs gut funktionieren, müssen Sie die Beschreibung des Gamuts des Geräts und der Eingabepunkte so anpassen, dass die neutrale Achse des Geräts auf die neutrale Achse des Darstellungsbereichs fällt. Sie müssen Punkte von der neutralen Achse um einen ähnlichen Betrag anpassen. Andernfalls können Sie keine reibungslosen Abstufungen über das Bild vornehmen. Auf dem Weg aus dem GMA wird diese Zuordnung relativ zur neutralen Achse des Ausgabegeräts rückgängig machen. Dies wird als "chiropractische" Geradeung der Achse bezeichnet. Wie bei einem Chiropraktor richten Sie nicht nur das Gerüst (neutrale Achse) aus, sondern passen den Rest des Textkörpers so an, dass er zusammen mit dem Gerüst bewegt wird. Wie bei einem Chiropraktor passen Sie das Gerüst nicht um dieselbe Menge im gesamten Raum an. Stattdessen passen Sie verschiedene Abschnitte unterschiedlich an.

![Diagramm, das die Krümmung der geräteneutralen Achse relativ zur neutralen CIECAM-Achse zeigt.](images/gmmp-image081.png)

**Abbildung 19:** Krümmung der geräteneutralen Achse relativ zur neutralen CIECAM-Achse

Der neue allgemeine Domänenauszug erfordert ein Modell einer Gamutgrenze, mit dem sowohl gerenderte als auch nicht gerenderte Quellbilder dargestellt werden können, Informationen über die Darstellung von Geräteneutralen und Informationen für Tonzuordnungsbilder mit einem breiten Leuchtbereich zur Verfügung stehen.

![Diagramm, das die drei gamut-Shells zeigt.](images/gmmp-image083.png)

**Abbildung 20:** Drei gamut-Shells

Die Gamutgrenze besteht aus drei Shells, die drei Regionen definieren.

Im neuen Allgemeinen Allgemeinen wird die äußere Shell des Gamuts mit einer konvexen Hülle gebildet, die aus Beispielpunkten in der Gamut des Geräts besteht. Eine Hülle wird gebildet, indem eine Reihe von Beispielpunkten genommen und von einer Oberfläche um sie umgeben wird. Eine konvexe Hülle hat die zusätzliche Eigenschaft, überall konvex zu sein. Daher ist dies nicht die kleinstmögliche Hülle, die an die Daten angepasst werden kann. Experimente haben jedoch gezeigt, dass die zu enge Anpassung der Beispielpunkte dazu führt, dass Artefakte in Bildern nicht verwendet werden, z. B. eine fehlende reibungslose Schattierung. Die konvexe Hülle scheint diese Probleme zu lösen.

Im Algorithmus werden Farbdarstellungswerte für eine Reihe von Punkten abgerufen, die vom Gerät entnommen werden. Für Monitore und Drucker werden die Farbdarstellungswerte abgerufen, indem Stichproben ausgegeben und anschließend gemessen werden. Sie können auch ein Gerätemodell erstellen und dann synthetische Daten über das Gerätemodell ausführen, um gemessene Werte vorherzusagen. Die gemessenen Werte werden dann vom farbmetrischen Raum (XYZ) in den Darstellungsbereich (Jab) konvertiert, und die Hülle wird um die Punkte umschlossen.

Der wichtigste Punkt für diesen Algorithmus ist, dass der verwendete Weißpunkt, der bei der Konvertierung von colorimetric in darstellungsraum verwendet wird, nicht der Weißpunkt des Mediums sein muss. Stattdessen können Sie einen Punkt weiter im Gamut und auf (oder in der Nähe) der neutralen Achse auswählen. Dieser Punkt hat dann den J-Wert 100. Stichproben mit einem gemessenen Y-Wert, der höher als der angenommene weiß punkt ist, erhalten einen J-Wert größer als 100.

Wenn Sie den diffusen weißen Punkt der Szene als übernommenen weißen Punkt für die Farbraumkonvertierung platzieren, werden Glanzlichter in der Szene leicht erkannt, wenn ein J-Wert größer als 100 ist.

Da das CIECAM02-Farbmodell auf dem visuellen System des Menschen basiert, wird die Leuchtdichte des schwarzen Punkts (J = 0) automatisch vom Modell bestimmt, nachdem ein übernommenes Weiß ausgewählt wurde. Wenn das Eingabebild über einen breiten dynamischen Bereich verfügt, kann es vorkommen, dass J-Werten Werte zugeordnet sind, die kleiner als 0 (null) sind.

Die folgende Abbildung 21 zeigt die Geräteneutralen, die durch die Mitte der Skalar- und Referenz gamuts laufen.

![Diagramm, das die geräteneutrale Achse zeigt, die der Gamutgrenze hinzugefügt wurde.](images/gmmp-image085.png)

**Abbildung 21:** Geräteneutrale Achse zur Gamutgrenze hinzugefügt

Alle Gamutzuordnungen umfassen entweder das Ausschneiden eines Eingabebereichs auf eine Ausgabe gamut oder das Komprimieren der Eingabe gamut, damit sie in die Ausgabe gamut passt. Komplexere Algorithmen werden durch Komprimieren und Clipping in unterschiedliche Richtungen, durch Unterteilen der Gamut in verschiedene Regionen und anschließendes Ausführen von Clipping oder Komprimierung in den verschiedenen Regionen gebildet.

Der neue allgemeine Allgemeine Allgemeine Ansatz erweitert dieses Konzept, um die Regionen eines möglichen Gamuts, eines fähigen Gamuts und einer Referenz-Gamut zu unterstützen, und ermöglicht GMAs, sie auf unterschiedliche Weise zuzuordnen. Darüber hinaus verfügen die GMAs über Informationen zur geräteneutralen Achse. Die folgende Diskussion behandelt den Umgang mit Situationen, in denen die skalaren Gamuts und Verweis gamuts aufeinander reduziert wurden.

![Diagramm, das das G M A mit zwei nicht reduzierten Gamutdeskriptoren zeigt.](images/gmmp-image091.png)

**Abbildung 22:** GMA mit zwei nicht reduzierten Gamutdeskriptoren

Dieses Beispiel wird möglicherweise angezeigt, wenn Sie von einem Eingabegerät, z. B. einer Kamera oder einem Scanner, die mit einem reflektierenden Ziel gekennzeichnet ist, scRGB-Raum zuordnen. Hier sind die glanzlichteren Farben, die leichter sind als Referenzfarben, Glanzlichter. In der Praxis generiert das Kennzeichnen einer Kamera mit einem Ziel möglicherweise nicht den vollständigen Wertebereich, der in der Kamera möglich ist. Glanzlichter und sehr heiterische Farben würden jedoch in der Natur gefunden werden. (Transmissive Ziele verfügen in der Regel über einen Patch, der die auf dem Medium mögliche Mindestdichte ist. Bei einem solchen Ziel würden Glanzlichter innerhalb des Zielbereichs liegen.) Der Verweis black für ein reflektierendes Ziel wäre der Anfang des schattenschwarzen Bereichs. Das heißt, es gibt wahrscheinlich Farben in den Schatten, die dunkler sind als schwarz auf dem Ziel. Wenn das Bild viele interessante Inhalte in dieser Region enthält, kann es sinnvoll sein, diese tonale Variation zu erhalten.

![Diagramm, das die G M A mit reduzierter Ziel gamut zeigt.](images/gmmp-image095.png)

**Abbildung 23:** GMA mit reduzierter Ziel gamut

Abbildung 23 zeigt einen möglichen Gamutzuordnungsalgorithmus, wenn die Ziel gamut nur den Bereich von Geräte weiß bis Schwarz bereitstellt und es keine möglichen Farben außerhalb dieser Gamut gibt. Dies ist wahrscheinlich bei typischen Ausgabegeräten wie Druckern der Fall. Die möglichen Farben werden dem Rand des Zielbereichs zugeordnet. Es fehlt jedoch eine Tonkurve für das Ausgabegerät. Das GMA muss einen neutralen Punkt mit geringerer Leuchtdichte auswählen, der als Zuordnungsziel für das Verweiswittchen verwendet werden soll. Ein ausgereifter Algorithmus kann dies erreichen, indem er die Helligkeiten im Quellbild histogrammiert und erkennt, wie viele in den Bereich der erwarteten, aber leichter als das Verweiswittchen fallen. Je mehr Helligkeiten erforderlich sind, desto mehr Platz ist auf dem Zielgerät zwischen den zugeordneten Punkten für die Glanzlichter und verweis white erforderlich. Ein einfacherer Algorithmus kann einen willkürlichen Abstand von der Helligkeitsskala von Geräte weiß auswählen, z. B. 5 Prozent. Ein ähnlicher Ansatz gilt für die Zuordnung der maximalen Schwarz- und Schattenschwarze.

Nachdem Sie die Zieltonkurve generiert haben, können Sie sie in einer Methode zuordnen, die der in der vorherigen Abbildung 23 verwendeten Methode ähnelt. Alle Punkte in der Zieltonkurve fallen innerhalb der Geräte-Gamut, und alle Punkte in der Zuordnung müssen innerhalb der Geräte-Gamut liegen.

Wenn Sie die linken und rechten Abbildungen und die Richtungen der Pfeile in Abbildung 23 umkehren, können Sie den Fall beschreiben, in dem das Quellbild nur über einen Verweis gamut verfügt und die drei Gamuts des Ausgabegeräts nicht aufeinander reduziert wurden. Ein Beispiel hierfür ist die Zuordnung von einem Monitor zu scRGB. Auch hier muss das GMA die Kontrollpunkte für die fünf Punkte in der Tonkurve für das Quellbild synthetisieren. Einige Zuordnungen können alle Punkte der Tonkurve innerhalb des scRGB-Geräte-Gamuts setzen, während andere Zuordnungen möglicherweise mehr scRGB-Gamut verwenden, indem sie diffuses Weiß dem Verweis white zuordnen und es specular white ermöglichen, einem leichteren Wert zuzuordnen.

Schließlich haben Sie den Fall, dass beide Geräte nur über die Referenz-Gamut verfügen. Dies ist die Funktionsweise der meisten Gamutzuordnungsalgorithmen. Sie können dies beheben, indem Sie einfach auf aktuelle Algorithmen zurückgreifen. Wenn Sie alternativ eine sinnvolle Möglichkeit haben, die fünf Verweispunkte für die Quell- und Zielgeräte zu bestimmen, können Sie die Zuordnung der Verweispunkte anordnen.

Geräte gamuts enthalten mehr als die fünf Verweispunkte auf der neutralen Achse. Diese stellen lediglich die Grenzen zwischen potenziellen Regionen im Bild dar. Zwischen den einzelnen Referenzpunkten können Sie alle vorhandenen Gamutzuordnungstechniken verwenden. Sie können also den Bereich unerwarteter Farben beschneiden und alle Farben zwischen dem erwarteten Weiß und Schwarz komprimieren, oder Sie können alle Farben außerhalb des Bezugsbereichs beschneiden und innerhalb dieses Bereichs komprimieren. Es gibt viele Möglichkeiten, die in verschiedenen GMAs implementiert werden können. Darüber hinaus können die GMAs auf unterschiedliche Weise komprimiert und abgeschnitten werden. Alle diese Kombinationen werden in dieser Erfindung behandelt.

Bisher wurde die Gamut in dieser Diskussion so behandelt, als wäre sie nur eine Funktion des Geräts, auf dem das Bild erstellt, erfasst oder angezeigt wurde. Es gibt jedoch keinen Grund, warum alle Images für ein Gerät dieselbe Gamut aufweisen müssen. Die GMAs hängen von den Daten in der GBD ab. Wenn der Deskriptor zwischen Bildern geändert wird, gibt es für die GMAs keine Möglichkeit, dies zu wissen. Insbesondere dann, wenn Bilder keine Glanzlichter aufweisen, sind GMAs besser, wenn der Gamutdeskriptor nicht zeigt, dass Farben leichter sind als diffuses Weiß.

In der neuen CTE-Architektur ist es möglich, mehr als ein GMA zu verwenden. Die Verwendung mehrerer GMAs ist grundsätzlich falsch definiert. Wenn z. B. ein Erfassungsgerät ein GMA mit seinem "Aussehen und Gefühl" verknüpft, tendiert es dazu, dies mit einer "Zielziel-Gamut" zu tun. Dasselbe gilt für Ausgabegeräte und "zielorientierte" Quell-Gamuts. Der sRGB-Gamut ist ein allgemein implizierter Gamut. Daher wird dringend empfohlen, ein einzelnes GMA zu verwenden, wenn vorhersagbar ist. Ein einzelner GMA-Workflow sollte die Standardeinstellung für alle Workflows sein, insbesondere für Consumer- und Prosumerworkflows. Die Gamutzuordnung für die bevorzugte Reproduktion sollte zwar einmal durchgeführt werden, es gibt jedoch Instanzen, in denen mehrere Zuordnungsprozesse enthalten sind. Zum Nachweis erstellen Sie zunächst eine bevorzugte Zuordnung zur Gamut des endgültigen Zielgeräts und dann ein farbmetrisches Rendering zur Gamut des Nachweisgeräts. Zweitens werden einige Arten von Zuordnungen verwendet, um die Merkmale des Bilds zu ändern, aber nicht enthalten, um einer Geräte gamut zuzuordnen, z. B. zum Anpassen der Tonkurve oder der Farblichkeit. Wenn mehrere GMAs verwendet werden, verwendet die Transformationsschnittstelle ein Array von gebundenen Gamutzuordnungen, d. h. Gamutkarten, die mit einem Paar von Gamutbegrenzungsbeschreibungen initialisiert wurden. Wenn mehrere Gamutzuordnungen vorhanden sind, muss die Eingabe-Gamutgrenze für eine erfolgreiche Gamutzuordnung mit der Ausgabe-Gamutgrenze ihres Vorgängers identisch sein.

Die Gamut-Begrenzungsfunktion des Geräts verwendet die Gerätemodell-Engine und analytische Parameter und leitet eine Farbgeräte-Gamutgrenze ab, die als sortierte Scheitelpunktliste der konvexen Hülle der Geräte gamutbeschrieben wird. Die Sortierte Scheitelpunktliste wird in CIEJab gespeichert. Die Struktur der geordneten Scheitelpunktliste ist für die Hardwarebeschleunigung durch DirectX optimiert. Dieser Ansatz verfügt über viele bekannte Lösungen (suchen Sie im Web nach "convex hull DirectX", und Sie erhalten weit über 100 Treffer). Es gibt auch einen Verweis aus 1983 zu diesem Thema (Computer graphics theory and application, "Ship datesls, b-spline surfaces and cadcam" pp. 34-49), mit Verweisen von 1970 bis 1982 zu diesem Thema.

Zwei verschiedene Techniken können verwendet werden, um die Dreiecke in der gamut-Shell zu berechnen. Für andere Geräte als additive RGB-Geräte berechnen Sie eine konvexe Hülle. Sie können erwägen, die Unterstützung nicht konvexer Hüllen für andere Geräte zu untersuchen, wenn Sie direkten Zugriff auf solche Geräte haben, um die Stabilität, Leistung und Genauigkeit der Algorithmen zu überprüfen. Dies ist ein bekannter Prozess, der keine weitere Beschreibung erfordert. Die für additive RGB-Geräte verwendete Technik wird wie folgt beschrieben.

Verschiedene GBDs haben Vor- und Nachteile. Die konvexe Hüllendarstellung garantiert ansprechende geometrische Eigenschaften, z. B. konvexe Farbtonslices, die einen eindeutigen Schnittpunkt mit einem Strahl bereitstellen, der von einem Punkt auf der neutralen Achse aus strahlt. Der Nachteil der konvexen Hüllendarstellung ist auch die Konvexität. Es ist bekannt, dass viele Geräte, insbesondere Anzeigegeräte, gamuts aufweisen, die weit davon entfernt sind, konvex zu sein. Wenn die tatsächliche Gamut erheblich von der Konvexitätsannahme abweicht, wäre die konvexe Hüllendarstellung ungenau, möglicherweise in dem Maße, in dem sie nicht die Realität darstellt.

Nachdem Sie eine GBD verwendet haben, die eine relativ genaue Darstellung des tatsächlichen Gamuts bietet, treten andere Probleme auf, einige aufgrund des Konzepts des Farbtonslices. Es gibt mindestens zwei Situationen. In der folgenden Abbildung 24 führt eine CRT-Gamut zu Farbtonslices mit "Islands". In Abbildung 25 führt ein Drucker gamut zu einem Farbtonslice, bei dem ein Teil der neutralen Achse fehlt. Die Schattierungsslices werden in diesen Fällen nicht durch besonders stark veränderliche Gamutgrenzen verursacht. Sie werden durch das Konzept des Farbtonslices verursacht, da (a) es mit konstantem Farbton aufgenommen wird und (b) es nur die Hälfte der Ebene nimmt, die dem Farbtonwinkel entspricht.

![Diagramm, das eine obere Ansicht und Eine-Seite-Ansicht des "curving in" in den blauen Farbtons zeigt.](images/gmmp-image097.jpg)

**Abbildung 24:** Ein typischer CRT-Monitor weist einen Gamut auf, der eine typische "Einkrümmung" in den blauen Farbtons zeigt. Wenn Hue-Slices innerhalb dieses Farbtonbereichs aufgenommen werden, können isolierte Inseln in den Farbtonslices angezeigt werden.

![Diagramm eines Gamuts mit einer "Lücke" auf der neutralen Achse.](images/gmmp-image099.jpg)

**Abbildung 25:** Ein Drucker verfügt möglicherweise über einen Gamut mit "Lücke" auf seiner neutralen Achse. Wenn ein Hue-Slice (der nur die Hälfte der Ebene ist) verwendet wird, gibt es einen "Dent" auf dem Teil der Grenze, der die neutrale Achse ist. Dies kann schwierig sein, algorithmisch aufzulösen.

Um diese Probleme zu beheben, wird ein neues Framework vorgeschlagen, das das Konzept des Hue-Slices abhebt, das als Ausgangspunkt verwendet wurde. Stattdessen verwendet das Framework den Satz von "Begrenzungslinienelementen" oder Linien, die sich an der Gamutgrenze befinden. Sie bieten nicht notwendigerweise eine konsistente geometrische Visualisierung wie Hue-Slices, unterstützen aber alle gängigen Gamutvorgänge. Neben der Lösung der zuvor erwähnten Probleme deutet dieser Ansatz auch darauf hin, dass die Konstruktion von Hue-Slices, selbst wenn dies möglich ist, rechenintensiv ist.

### <a name="triangulation-of-the-gamut-boundary"></a>Triangulation der Gamut-Grenze

Der Ausgangspunkt ist eine GBD, die aus einer Triangulation der Gamutgrenze besteht. Bekannte Methoden zum Erstellen von GBDs bieten in der Regel diese Triangulation. Aus Konkreten geht es hier um eine Methode zum Erstellen von GBDs für additive Geräte. Zu diesen Geräten gehören Monitore (sowohl CRT-basiert als auch WIES-basiert) und Projektoren. Mit der einfachen Geometrie des Cubes können Sie ein reguläres Lattice für den Cube einführen. Die Begrenzungsgesichter des Cubes können auf verschiedene Weise trianguliert werden, z. B. die in Abbildung 26 dargestellte. Die Architektur bietet entweder ein Gerätemodell für das Gerät, sodass farbmetrische Werte der Latticepunkte algorithmisch oder direkt für diese Punkte gemessen werden können. Die Architektur bietet auch CIECAM02, sodass Sie davon ausgehen können, dass die Startdaten bereits dem CIECAM02 Jab-Raum zugeordnet wurden. Anschließend hat jeder Latticepunkt auf den Begrenzungsflächen des RGB-Cubes einen entsprechenden Punkt im Jab-Raum. Die Verbindungen von Punkten, die die Reihe von Dreiecken im RGB-Raum bilden, lösen auch eine Reihe von Dreiecken im Jab-Raum aus. Diese Gruppe von Dreiecken bildet eine sinnvolle Triangulation der Gamutgrenze, wenn (a) das Lattice im RGB-Cube ausreichend groß genug ist und (b) die Transformation vom Geräteraum zum einheitlichen Farbraum topologisch gut ist; Das heißt, es ordnet Begrenzungen Begrenzungen zu, und der Gamut wird nicht innerhalb der Grenze heraus gewendet, sodass innere Punkte zu Begrenzungspunkten werden.

![Diagramm, das eine einfache Methode zum Triangluieren der Gamutgrenze eines Geräts mit R G B als Gerätebereich zeigt.](images/gmmp-image100.png)

**Abbildung 26:** Eine einfache Methode zum Triangulieren der Gamutgrenze eines Geräts mit RGB als Geräteraum

### <a name="boundary-line-elements"></a>Begrenzungslinienelemente

Im Mittelpunkt dieses Frameworks steht das Konzept von Begrenzungslinienelementen. ein Satz von Liniensegmenten, die (a) an der Gamutgrenze liegen, und (b) auf einer Ebene liegen. In diesem Fall ist die Ebene eine Farbtonebene. Jedes Liniensegment ist das Ergebnis der Überschneidung der Ebene mit einem gamut-Begrenzungsdreieck. Obwohl viele Forscher die Konstruktion der Überschneidung einer Ebene mit Begrenzungsdreiecken verwendet haben, analysieren sie im Allgemeinen die Beziehung zwischen diesen Liniensegmenten und versuchen, ein zusammenhängendes geometrisches Objekt aus den Liniensegmenten zu erstellen. Es wurden verschiedene Algorithmen entwickelt, um diesen Liniensegmenten nacheinander zu folgen, bis ein ganzer Farbtonslice ermittelt wurde und viele Versuche unternommen wurden, den Suchvorgang zu beschleunigen.

Dieser Ansatz ist anders. Sie überschneiden die Ebene mit den Dreiecken, um die Liniensegmente zu erhalten. Anschließend betrachten Sie diese Liniensegmente als grundlegende *konzeptionelle* Objekte. Es ist erforderlich, die Beziehung zwischen den Liniensegmenten zu analysieren. Sie müssen nicht wissen, wie sie miteinander verbunden sind. Dieser Standpunkt löst das Problem der Farbtonslice mit Inseln. Bei den bekannten Ansätzen, die versuchen, einen Farbtonslice zu erstellen, wird davon ausgegangen, dass, wenn ein Segment mit einem Liniensegment beginnt und ihm das nächste Liniensegment folgt, und so weiter; Sie führt schließlich zurück zum Ausgangspunkt, an dem ein ganzer Farbtonslice erstellt wird. Leider würde dieser Ansatz die Insel (und im schlechtesten Szenario den Kontinent) übersehen. Indem sie sich nicht um die Beschaffung eines zusammenhängenden geometrischen Bilds zu verkningen; Das heißt, hue slice, Sie können das Problem der Insel mühelos behandeln. Ein weiterer wichtiger Unterschied bei diesem Ansatz besteht in der Verwendung eines "Dreiecksfilters", um die Konstruktion von Liniensegmenten zu beschleunigen. Der Dreiecksfilter löst bestimmte Dreiecke aus, die definitiv keine Liniensegmente erzeugen, die für den aktuellen Gamut-Vorgang nützlich wären. Da das Überschneiden eines Dreiecks mit der Ebene rechenintensiv ist, verbessert dies die Geschwindigkeit. Ein Nebeneffekt ist, dass Sie keinen Farbtonslice erstellen können, da einige Liniensegmente aufgrund der Dreiecksfilterung fehlen würden.

### <a name="gamut-operation-checkgamut"></a>Gamut-Vorgang: CheckGamut

Im folgenden Beispiel wird erläutert, wie das Framework funktioniert und wie CheckGamut ausgeführt wird, d.&a0;b. der Vorgang der Überprüfung, ob eine Farbe in Gamut ist.

Das allgemeine Framework ist in der folgenden Abbildung 27 dargestellt. Es gibt verschiedene Komponenten. Bei den italisch bezeichneten Komponenten handelt es sich um Komponenten, die sich je nach dem in Frage gestellten Gamutvorgang in der Implementierung unterscheiden können. Die anderen Komponenten sind für alle gamut-Vorgänge invariant. Zunächst handelt es sich ***bei der Eingabe*** um einen Satz von Farbattributen. Im Fall von CheckGamut ist dies die Abfragefarbe. In Abbildung 27 und der folgenden Diskussion wird davon ausgegangen, dass der Farbtonwinkel entweder zu den Eingabefarbattributen gehört oder daraus ermittelt werden kann. Dies ist eindeutig der Fall, wenn die Eingabe der gesamte Farbpunkt ist, entweder in Jab oder JCh, aus dem Sie dann den Farbtonwinkel berechnen können. Beachten Sie, dass der Farbtonwinkel nur erforderlich ist, da Farbtonebenen verwendet werden. Je nach dem in Frage gestellten Gamut-Vorgang ist es möglicherweise nicht erforderlich, die Farbtonebene zu verwenden. Bei der Konstruktion der Routine CheckGamut können Sie z. B. Ebenen der Konstante J verwenden. Dies ist eine Allgemeinheit, die nicht weiter verwendet oder erläutert wird. Aber es kann hilfreich sein, sich diese Flexibilität der Methodik zur Unterstützung anderer Gamutvorgänge zu merken, wenn die Farbtonebene möglicherweise nicht die beste Wahl ist.

![Diagramm, das den Ablauf zur Unterstützung von Gamutvorgängen zeigt.](images/gmmp-image112.jpg)

**Abbildung 27:** Das Framework zur Unterstützung von gamut-Vorgängen

Der Farbtonwinkel, der direkt aus den Eingaben ermittelt oder aus den Eingaben berechnet wird, wird verwendet, um die Farbtonebene mit der Bezeichnung Full Hue Plane (Vollständige **Hue-Ebene)** in der Abbildung zu initialisieren. "Full" wird hervorgehoben, da dies die vollständige Ebene ist, nicht nur die halbe Ebene, die den Farbton enthält. Die vollständige Ebene enthält sowohl den Eingabetonwinkel als auch den 180 Grad umgekehrten Winkel. Die Hauptfunktionalität der Farbtonebene ist die Intersect-Funktion, die im folgenden Unterabschnitt, Full Hue Plane: Intersect, erläutert wird. Angenommen, die GBD wurde bereits erstellt, und der Satz von **Gamut-Begrenzungsdreiecken** ist verfügbar. Überschneiden Sie die Dreiecke, die den **_Dreiecksfilter_* _ überdauert haben, mit der Farbtonebene, indem Sie Intersect verwenden. The _Triangle Filter* component is labeled in italics, which means that the component varies in implementation for different gamut operations. The *Triangle Filter* for CheckGamut is explained in the section, Gamut Operation: CheckGamut (continued). The result of intersecting a triangle with the hue plane is either empty or a **Boundary Line Element** , that is, a pair of distinct points. If the result is non-empty, it is passed into the **_Line Element Processor_*_ , which again does different things depending on the gamut operation. Der _Line Element Processor* aktualisiert die_ interne Datenstruktur * Interne verarbeitete Daten , deren Inhalt oder Layout ebenfalls vom Gamut-Vorgang abhängt. Im Allgemeinen enthält die intern verarbeiteten Daten* die "Antwort" auf das Problem, das ständig mit jedem gefundenen neuen _Boundary Line-Element aktualisiert wird. Nachdem alle Begrenzungslinienelemente verarbeitet wurden, wurde die Antwort gefunden. Es bleibt bestehen, um über den ***Ausgabeadapter darauf zu zugreifen.**_ Da der _Internal Verarbeitete Daten* gamut-vorgangsspezifisch ist, ist der *Ausgabeadapter* auch gamut-vorgangsspezifisch.

### <a name="full-hue-plane-intersect"></a>Vollständige Hue-Ebene: Überschneiden

Die Intersect-Funktion berechnet die Schnittmenge der Farbtonebene und eines Dreiecks. Diese Funktion ist aus zwei Gründen wichtig, so einfach sie klingt.

Erstens kann das Überschneiden der einzelnen Ränder des Dreiecks mit der Ebene drei Schnittpunkte ergeben, eine geometrisch unmögliche Situation. Dies kann bei der Berechnung der Grund dafür sein, dass bei Berechnungen im Gleitkommaformat, z. B. im IEEE-Format, in jedem Schritt Rauschen oder "numerisches Rauschen" vorliegen, die sich auf die Schlussfolgerung auswirken, ob eine Kante die Ebene überschneidet. Wenn die Ebene die Ränder in einer Situation überschneidet, in der sich die Schnittpunkte nahezu aus dem Nichts befinden, sind die Schnittpunkte nah beieinander, und die Bestimmung, ob ein Schnittpunkt innerhalb des Edge liegt, ist zufällig. Obwohl das Rauschen in den numerischen Werten der Punkte klein ist, ist die qualitative Schlussfolgerung, dass es mehr als zwei Schnittpunkte gibt, geometrisch unmöglich und schwierig, im Algorithmus richtig zu behandeln.

Zweitens befindet sich diese Funktion in der kritischen Schleife für jeden Rand jedes gefilterten Dreiecks. Daher ist es wichtig, dass Sie die Effizienz so weit wie möglich optimieren.

Um das erste Problem des numerischen Rauschens zu beheben, führen Sie die Berechnungen in ganzen Zahlen aus. Um das zweite Problem der Optimierung der Effizienz zu beheben, speichern Sie das am häufigsten verwendete Attribut jedes Scheitelpunkts oder das jedem Scheitelpunkt zugeordnete "Punktprodukt" zwischen. Die Übergabe in ganze Zahlen ist eine typische Möglichkeit, geometrische Konsistenz zu gewährleisten. Die Grundidee ist, dass Sie dies am Anfang tun müssen, wenn Sie Quantisieren müssen. Anschließend können nachfolgende Berechnungen in ganzen Zahlen ausgeführt werden, und wenn die ganzen Zahlen breit genug sind, sodass keine Überlaufgefährdung besteht, können die Berechnungen mit unendlicher Genauigkeit durchgeführt werden. Die folgende Quantisierungsfunktion ist für diesen Zweck nützlich.

ScaleAndTruncate(x) = Ganzzahliger Teil von x \* 10000

Der Skalierungsfaktor 10000 bedeutet, dass die Eingabe-Gleitkommazahl vier Dezimalstellen hat, was für diese Anwendung genau genug ist. Abhängig vom Bereich der Werte des Farbbildraums möchten Sie einen ganzzahligen Typ mit Bits auswählen, die breit genug sind, um die Zwischenberechnungen zu speichern. In den meisten Farbflächen liegt der Bereich jeder Koordinate im Bereich von -1.000 bis 1.000. Die quantisierte Koordinate hat einen maximal möglichen absoluten Wert von 1.000 \* 10.000 = 10.000.000. Wie Sie sehen werden, ist die Zwischenmenge ein Punktprodukt, bei dem es sich um eine Summe von zwei Produkten von Koordinaten handelt, sodass sie einen maximal möglichen absoluten Wert von 2 \* (10.000.000) ₂ = 2?10 ₁₄. Die Erforderliche Anzahl von Bits ist log ₂ (2?10 ₁₄ ) = 47,51. Eine praktische Wahl für den Ganzzahltyp sind daher 64-Bit-Ganzzahlen.

Um zu gewährleisten, dass das Überschneiden einer Ebene mit einem Dreieck immer entweder eine leere Menge oder eine Gruppe von zwei Punkten ergibt, müssen Sie das Dreieck als Ganzes betrachten, nicht als einzelne Ränder des Dreiecks separat. Um die geometrische Situation zu verstehen, berücksichtigen Sie die "signierten Abstände" der Scheitelstellen des Dreiecks von der Farbtonebene. Berechnen Sie diese vorsignierte Entfernungen nicht direkt. berechnen Sie stattdessen die Punktprodukte der Positionsvektoren der Scheitelpunkte mit dem quantisierten Normalvektor zur Ebene. Genauer gesagt wird der quantisierte Normalvektor während der Initialisierung der Farbtonebene wie folgt berechnet.

NormalVector = (ScaleAndTruncate(-sin(hue)), ScaleAndTruncate(cos(hue)))

Beachten Sie, dass dieser Vektor ein zweidimensionaler Vektor ist. Sie können einen zweidimensionalen Vektor verwenden, da die Farbtonebene vertikal ist, sodass die dritte Komponente des normalen Vektors immer 0 (null) ist. Darüber hinaus wird eine Nachschlagetabelle mit Punktprodukten initialisiert, um einen Eintrag für jeden Scheitelpunkt aus den Gamut-Begrenzungsdreiecken zu erhalten, und das entsprechende Punktprodukt wird auf einen ungültigen Wert festgelegt.

Während eines Vorgangs zum Überschneiden der Farbtonebene mit einem Dreieck wird das Punktprodukt jedes Scheitelpunkts des Dreiecks nachge sucht. Wenn der Wert in der Nachschlagetabelle der ungültige Wert ist, wird das Punktprodukt mit dem folgenden Ausdruck berechnet.

NormalVector.a \* ScaleAndTruncate(vertex.a) + NormalVector.b \* ScaleAndTruncate(vertex.b)

Auch hier wird die J-Komponente des Scheitelpunkts nie verwendet, da der normale Vektor horizontal ist. Dieses Punktprodukt wird dann in der Nachschlagetabelle gespeichert, sodass es nicht erneut berechnet werden muss, wenn das Punktprodukt des Scheitelpunkts später abgefragt wird.

Das Zwischenspeichern ermöglicht eine schnelle Ermittlung, ob ein Rand die Ebene überschneidet, nachdem die Punktprodukte in der Nachschlagetabelle tabellarisch sind, die progressiv erstellt wird, wenn die Scheitelpunkte verarbeitet werden.

![Diagramm, das die Schnittmenge der Farbtonebene mit einem Dreieck zeigt.](images/gmmp-image114.jpg)

**Abbildung 28:** Überschneiden der Farbtonebene mit einem Dreieck

Damit das Dreieck in Abbildung 28 die Farbtonebene in einem nicht degenerierten Liniensegment überschneidet, müssen sich die Punktprodukte der Scheitelpunkte in einem der folgenden Muster befinden, wenn sie in aufsteigender Reihenfolge sortiert werden.

0,0,+; -,0,0; -,0,+; -,-,+; -,+,+

Ein Endpunkt des Liniensegments tritt auf, wenn die Ebene von einem Rand mit Scheitelpunkten überschneidet wird, die unterschiedliche Zeichen im Punktprodukt aufweisen. Wenn das Vorzeichen 0 (null) ist, liegt der Scheitelpunkt direkt auf der Ebene, und die Schnittmenge des Rands mit der Ebene ist der Scheitelpunkt selbst. Beachten Sie auch, dass die Fälle 0,0,0; -,-,0; 0,+,+ werden nicht gemeldet. Der erste Fall (0,0,0) bedeutet, dass das gesamte Dreieck auf der Ebene liegt. Dies wird nicht gemeldet, da jeder Rand des Dreiecks zu einem benachbarten Dreieck gehören sollte, das nicht auch vollständig auf der Ebene liegt. Der Rand wird gemeldet, wenn dieses Dreieck berücksichtigt wird. Die anderen beiden Fälle (-,-,0 und 0,+,+) entsprechen der geometrischen Konfiguration, dass das Dreieck die Ebene in einem Scheitelpunkt berührt. Diese Fälle werden nicht gemeldet, da sie nicht zu einem nicht degenerieren Liniensegment führen.

Der vorangehende Algorithmus bestimmt, wann eine Schnittmenge zwischen einem Rand des Dreiecks und der Farbtonebene berechnet werden soll. Nachdem ein Rand bestimmt wurde, wird die Schnittmenge mit parametrischen Gleichungen berechnet. Wenn eines der Punktprodukte 0 (null) ist, ist die Schnittmenge der Scheitelpunkt selbst, sodass keine Berechnung erforderlich ist. Vorausgesetzt, dass beide Punktprodukte der Scheitelpunkte des Edges ungleich 0 (null) sind, ist vertex1 der Scheitelpunkt mit dem *negativen* Punktprodukt dotProduct1; und vertex2 ist der Scheitelpunkt mit *positivem* Punktprodukt dotProduct2. Diese Reihenfolge ist wichtig, um sicherzustellen, dass der berechnete Schnittpunkt nicht davon abhängt, wie die Reihenfolge der Scheitelpunkte in der Darstellung des Rands angezeigt wird. Das geometrische Konzept des Edges ist in Bezug auf seine Scheitelpunkte symmetrisch. Der Berechnungsaspekt bei der Verwendung parametrischer Gleichungen des Rands führt zu einer Asymmetrie (Auswahl des Startpunkts), die aufgrund von numerischem Rauschen und der Konditionierung der zu lösenden linearen Gleichungen einen etwas anderen Schnittpunkt ergeben kann. In diesem Beispiel wird der Schnittpunkt (Schnittmenge) wie folgt angegeben.

t = dotProduct1/(dotProduct1 - dotProduct2)

Schnittpunkt. J = vertex1. J + t \* (vertex2. J – vertex1. J)

intersection.a = vertex1.a + t \* (vertex2.a - vertex1.a)

intersection.b = vertex1.b + t \* (vertex2.b - vertex1.b)

### <a name="gamut-operation-checkgamut-continued"></a>Gamut-Vorgang: CheckGamut (fortsetzung)

Der grundlegende geometrische Algorithmus, der für die Gamutüberprüfung verwendet wird, ist die Zählung der Anzahl von Strahlübergängen. Betrachten Sie für einen bestimmten Abfragepunkt einen Strahl, der mit dem Abfragepunkt beginnt und nach oben zeigt (J-Richtung). Zählen Sie, wie oft dieser Strahl die Gamutgrenze überschreitet. Wenn diese Zahl gerade ist, ist der Abfragepunkt out-of-gamut. Wenn diese Zahl ungerade ist, befindet sich der Punkt darin. Im Prinzip kann dieser Algorithmus in 3D implementiert werden. Er wird in der Regel durch Schwierigkeiten ersetzt, die durch degenerierte Situationen verursacht werden, wie z. B. die Strahlgeschädigung (teilweise) auf einem Begrenzungsdreieck oder eine niedrigerdimensionale Degeneranz, z. B. die Strahlstrahlgeschädigung (teilweise) an einem Rand eines Begrenzungdreiecks. Selbst in 2D müssen Sie sich mit diesen degenerieren Situationen befassen. aber das Problem ist einfacher und wurde auf zufriedenstellende Weise behoben. Weitere Informationen finden Sie \[ unter O'Rourke \] .

Bestimmen Sie für einen bestimmten Eingabepunkt Jab den Farbtonwinkel h wie folgt.

h = atan(b/a),

Initialisieren Sie die Farbtonebene, und bestimmen Sie dann die Begrenzungslinienelemente, die dieser Farbtonebene entsprechen. Da die Begrenzungslinienelemente nur relevant sind, wenn sie den Aufwärtsstrahl überschneiden, richten Sie einen Dreiecksfilter ein, um Dreiecke zu entfernen, die Linienelemente enthalten, die den Aufwärtsstrahl definitiv nicht überschneiden. Betrachten Sie in diesem Fall das umgebende Feld des Dreiecks. Der Aufwärtsstrahl überschneidet sich nicht mit dem Dreieck, wenn sich der Abfragepunkt außerhalb des "Schattens" befindet, der vom begrenzungsfeld geworfen wird, wenn sich eine Lichtquelle direkt darüber befand. Erweitern Sie dies geringfügig mit einer vordefinierten Toleranz, um numerisches Rauschen zu ermöglichen, sodass Sie versehentlich keine Dreiecke wegwerfen, die nützliche Linienelemente liefern können. Das Ergebnis ist der halb unendliche rechteckige Zylinder in Abbildung 29. Die Überprüfung, ob sich der Abfragepunkt innerhalb oder außerhalb dieses Zylinders befindet, kann mithilfe einfacher Gleichung effizient implementiert werden.

![Zeigt den Dreiecksfilter für CheckGamut an.](images/gmmp-image116.jpg)

**Abbildung 29:** Dreiecksfilter für CheckGamut

CheckGamut verfügt über drei allgemeine Vorgangskomponenten: *Interne verarbeitete Daten,**Zeilenelementprozessor* und *Ausgabeadapter*. Die *intern verarbeiteten Daten* sind eine Liste von Zeilenelementen, die vom *Zeilenelementprozessor* verarbeitet wurden. In diesem Fall fügt der *Zeilenelementprozessor* der Liste einfach ein Linienelement hinzu. Die interne Datenstruktur für *intern verarbeitete Daten* kann entweder eine verknüpfte Liste oder ein Array sein, das größer werden kann.

Der *Ausgabeadapter* ist ein Modul, das auf die Liste der Zeilenelemente zugreift und bestimmt, ob ein Linienelement den Aufwärtsstrahl (Anzahl 1) überschreitet (Anzahl 0). Das Summieren all dieser Anzahlen ergibt eine Gesamtanzahl. Der *Ausgabeadapter* gibt letztendlich eine Antwort mit "ja" (in-gamut) oder "nein" (out-of-gamut) aus, je nachdem, ob die Gesamtanzahl ungerade oder gerade ist. Der Schritt, in dem Sie bestimmen, ob ein Linienelement den Aufwärtsstrahl überschreitet, ist ein gewisses Maß an Aufmerksamkeit, da hier das Problem der Degeneranz auftritt und auch das Problem der Überzählung auftritt. Nach \[ O'Rourke muss sich \] der rechte Endpunkt (der Endpunkt mit größerem Strahl) genau auf der rechten Seite des Strahls halten, damit ein Linienelement den Strahl kreuzt. Dadurch wird sichergestellt, dass ein Endpunkt nur einmal gezählt wird, wenn er jemals genau auf dem Strahl liegt. Dieselbe Regel löst auch die degenerate Situation, in der sich das Linienelement genau auf dem Strahl befindet. Sie erhöhen die Anzahl für dieses Zeilenelement nicht.

Abbildung 30 zeigt die resultierenden Linienelemente eines Beispiel-Gamuts mit dem Abfragepunkt an verschiedenen Positionen.

![Diagramm, das die resultierenden Linienelemente eines Beispiel-Gamuts mit dem Abfragepunkt an verschiedenen Positionen zeigt.](images/gmmp-image118.jpg)

**Abbildung 30:** Funktionsweise von CheckGamut

### <a name="minimum-color-difference-gamut-mapping"></a>Minimale Farbunterschiede – Gamutzuordnung

MinDEMap , Minimum Color Difference Gamut Mapping, verfügt über eine einfache Spezifikation: Wenn eine Farbe in gamut ist, tun Sie nichts. Wenn eine Farbe nicht gamutig ist, pro projectieren Sie sie auf den "nächstgelegenen" Punkt an der Gamutgrenze. Das Schlüsselwort "nearest" ist erst dann klar definiert, wenn Sie die zu verwendende Farbunterschiedsgleichung angeben. In der Praxis wird der euklidische Abstand des ausgewählten Farbdarstellungsbereichs oder eine Variante davon als Farbunterschiedsmetrik verwendet, um die Berechnung zu vereinfachen und zu beschleunigen. Der Vorteil der euklidischen Metrik besteht darin, dass sie mit dem Punktprodukt des Raumes kompatibel ist, wodurch es möglich ist, lineare Algebra zu verwenden. Wenn im Raum ein "Punktprodukt" definiert ist, kann ein Abstand als Quadratwurzel des Punktprodukts des Differenzvektors mit sich selbst definiert werden. Ein Punktprodukt kann im Allgemeinen durch eine positive eindeutige 3x3-Matrix A definiert werden.

u?v = u <sub>T</sub> Av

dabei ist die rechte Seite die übliche Matrixmultiplikation. Wenn A die Identitätsmatrix ist, wird das Standardpunktprodukt wiederhergestellt. In der Praxis möchten Sie, wenn Jab der Farbraum ist, die Komponenten nicht mischen, sodass eine andere diagonale Matrix als die Identitätsmatrix verwendet werden kann. Darüber hinaus sollten Sie die Skala auf a und b unverändert lassen, damit das Maß für den Farbton beibehalten wird. Daher ist eine nützliche Variante des euklidischen Standardpunktprodukts die folgende.

w <sub>J</sub> (J-Komponente von Ihnen)(J-Komponente von v) + (eine Komponente von Ihnen)(eine Komponente von v) + (b Komponente von Ihnen)(b Komponente von v)

wobei w <sub>J</sub> eine positive Zahl ist. Eine weitere Variante besteht darin, w <sub>J</sub> mit dem Eingabeabfragepunkt variieren zu lassen:

w <sub>J\ =</sub> w <sub>J</sub> (queryPoint)

Das Endergebnis ist ein Maß für die Entfernung, das in Bezug auf die beiden Punkte asymmetrisch ist, und mit unterschiedlichen relativen Gewichtungen für Helligkeit und Farbton oder Farbton, da der Eingabeabfragepunkt variiert. Dies entspricht einigen Beobachtungen zur menschlichen Farberkennung, dass Farbunterschiede nicht gleichmäßig in allen Dimensionen gewichtet werden. Es wurde festgestellt, dass Die Menschen weniger empfindlich auf Unterschiede bei der Helligkeit reagieren als auf Unterschiede in Farbton und Farbe.

Die folgende Gewichtungsfunktion ist nützlich.

w <sub>J</sub> = k ₂ – k ₁ (C – C mₐₓ ) n

wobei k ₂ = 1, k ₁ = 0,75/(C mₐₓ ) n, C mₐₓ = 100, n = 2 und C der kleinere Teil des Abfragepunkts und C mₐₓ ist.

, sodass eine Gewichtung von 0,25 auf den J-Begriff gesetzt wird, wenn Dasin null ist, und ein Gewicht von 1, wenn Dasin 100 beträgt. Der Trend, J bei geringem Gewichtungsgewicht weniger gewichtend zu verwenden, und mehr Gewichtung für J, wenn Dasin groß ist, entspricht der empfohlenen Verwendung für CMC und CIEDE2000.

![Graph, der die Gewichtungsfunktion für die J-Komponente der Metrik anzeigt.](images/gmmp-image119.png)

**Abbildung 31:** Gewichtungsfunktion für die J-Komponente der Metrik

Verwenden Sie jab space für das folgende Beispiel. Es ist rechenintensiv, alle Begrenzungsdreiecke zu durchsuchen, um den nächstgelegenen Punkt in der euklidischen Metrik zu ermitteln. Im Folgenden finden Sie einen einfachen Ansatz, um diesen Prozess so effizient wie möglich zu gestalten, ohne zusätzliche Annahmen einzuführen, die den Prozess beschleunigen, aber auch nur eine ungefähre Antwort ergeben. Zunächst müssen Sie die geometrische Prozedur verstehen, mit der ein Punkt auf das angegebene Dreieck projiziert wird. Eine Beschreibung finden Sie hier.

Zuerst wird eine orthogonale Projektion auf die unendliche Ebene durchgeführt, die das Dreieck enthält. Die kürzeste Entfernung des Abfragepunkts von der Ebene kann in zwei Schritten ermittelt werden.

**(a)** Berechnen Sie den Normalenvektor der Einheit auf das Dreieck.

**(b)** Berechnen Sie das Punktprodukt des Normalvektors der Einheit und einen Vektor, der aus dem Abfragepunkt und einem Punkt auf dem Dreieck gebildet wird. das heißt, einer seiner Scheitelpunkte. Da der normale Vektor eine Einheitenlänge hat, ist der absolute Wert dieses Punktprodukts der Abstand des Abfragepunkts von der Ebene.

Der projizierte Punkt ist möglicherweise nicht die Antwort, da er sich außerhalb des Dreiecks befindet. Daher müssen Sie zuerst eine Überprüfung durchführen. Die Berechnung entspricht der Berechnung der baryzentrischen Koordinaten des projizierten Punkts relativ zum Dreieck. Wenn der projizierte Punkt bestimmt wird, dass er sich innerhalb des Dreiecks befindet, ist dies die Antwort. Falls nicht, wird der nächstgelegene Punkt an einem der Ränder des Dreiecks bezogen. Führen Sie eine Suche an jedem der drei Ränder durch. Das Bestimmen der Projektion des Abfragepunkts auf einen Rand ist ein Prozess, der der Projektion auf das Dreieck ähnelt, jedoch eine Dimension weniger. Zuerst wird eine orthogonale Projektion berechnet. Wenn der projizierte Punkt am Rand liegt, ist dies die Antwort. Falls nicht, wird der nächstgelegene Punkt an einem der beiden Endpunkte bezogen. Führen Sie eine Suche an den beiden Endpunkten aus. Das heißt, berechnen Sie den Abstand des Abfragepunkts zu jedem Abfragepunkt, und vergleichen Sie, welcher kleiner ist.

Eine sorgfältige Untersuchung zeigt, dass es viele wiederholte Suchvorgänge gibt, wenn Sie alle Dreiecke durchlaufen, da ein Rand immer von zwei Dreiecken gemeinsam genutzt wird und ein Scheitelpunkt von mindestens drei Kanten gemeinsam genutzt wird. Darüber hinaus sind Sie nicht sehr daran interessiert, den nächstgelegenen Punkt zu einem bestimmten Dreieck zu finden. Stattdessen möchten Sie den nächstgelegenen Punkt der gesamten Gamutgrenze ermitteln. Ein bestimmtes Dreieck wäre jedoch das Dreieck, in dem dies erreicht wird. Es gibt zwei Strategien, mit denen Sie die Suche beschleunigen können.

**Strategie I**. Jeder Scheitelpunkt wird höchstens einmal verarbeitet. Jeder Edge wird höchstens einmal verarbeitet.

**Strategie II**. Zu jedem Zeitpunkt der Suche haben Sie einen besten Kandidaten mit der entsprechenden besten Entfernung. Wenn Sie durch eine schnelle Überprüfung feststellen können, dass ein Dreieck keine bessere Entfernung bieten kann, ist es nicht erforderlich, die Berechnung fortzusetzen. Sie benötigen nicht den nächstgelegenen Punkt und Abstand für dieses Dreieck.

![Diagramm, das den Ablauf der Minimal-DE-Zuordnung zeigt.](images/gmmp-image120.png)

**Abbildung 32:** Minimale DE-Zuordnungsschemata

Abbildung 32 zeigt den allgemeinen Logikfluss für die Gamutkarte MinDEMap. Für einen Abfragepunkt wird zuerst die CheckGamut-Funktion aufgerufen. Wenn der Punkt in gamut ist, ist die Karte kein Op. Wenn der Punkt out-of-gamut ist, rufen Sie ProjectPointToBoundary auf. Fahren Sie nun mit Abbildung 33 fort. An diesem Punkt wird davon ausgegangen, dass die folgenden Werte berechnet wurden.

**(a)** Unit normal vector to each Gamut Boundary Triangle in Bezug auf das Standardpunktprodukt.

**(b)** Scheitelpunktliste und Kantenliste zusätzlich zur Dreiecksliste.

![Diagramm, das die Routine "ProjectPointToBoundary" zeigt.](images/gmmp-image122.jpg)

**Abbildung 33:** Die ProjectPointToBoundary-Routine

All dies ist ein konstanter Mehraufwand und würde die Kosten verringern, wenn genügend Abfragen an diese allgemeine Grenze durchgeführt werden. In der Regel ist dies der Fall, wenn Sie eine Transformations-CSV-Datei von einem Gerät zu einem anderen erstellen, bei der nur zwei feste Gamuts vorhanden sind, und die Transformations-MSI durch Punkte im einheitlichen Raster mit Stichproben ausgeführt wird. Sie berechnen die normalen Vektoren im Hinblick auf das Standardpunktprodukt vorab, obwohl das Konzept der Perpendity auf dem gewichteten Punktprodukt basiert, das vom Abfragepunkt abhängt, wie zuvor erläutert. Der Grund dafür ist, dass ein normaler Vektor in Bezug auf das gewichtete Punktprodukt leicht aus dem normalen Vektor in Bezug auf das Standardpunktprodukt abgerufen werden kann. Wenn n ₀ ein normaler Vektor in Bezug auf das Standardpunktprodukt ist, dann

n = (J-Komponente von n ₀ /w <sub>J</sub>, A-Komponente von n ₀, B-Komponente von n ₀ )

ist für das Dreieck in Bezug auf das gewichtete Punktprodukt normal. Aufgrund dieser Beziehung ist es immer noch vorteilhaft, n ₀ vorab zu berechnen, obwohl sie basierend auf dem Abfragepunkt angepasst werden muss.

Die ProjectPointToBoundary-Routine beginnt mit dem Zurücksetzen des "verarbeiteten Verlaufs" der Scheitelpunkte und Kanten. Dies sind Tabellen mit BOOLESCHEN Flags, die nachverfolgen, ob zuvor ein Scheitelpunkt oder eine Kante besucht wurde. Außerdem wird die Variable ShortestDistance auf "INFINITY" zurückgesetzt. Dies ist der maximale codierte Wert im verwendeten Gleitkommazahlensystem. Anschließend wird eine Schleife durchlaufen, wobei mithilfe des ProcessTringle-Aufrufs von jedem Dreieck nach dem nächstgelegenen Punkt gesucht wird. ProcessTriangle ist die Routine zum Aktualisieren der ShortestDistance-Variablen und befindet sich eindeutig in der kritischen Schleife. Eine Optimierung besteht darin, zu beenden, wenn das Ergebnis gut genug ist. Nach jedem Aufruf von ProcessTringle wird die Variable ShortestDistance untersucht. Wenn sie einen vordefinierten Schwellenwert erfüllt, können Sie beenden. Der vordefinierte Schwellenwert hängt vom verwendeten Farbraum und von der erforderlichen Genauigkeit des Farbbildsystems ab. Bei einer typischen Anwendung möchten Sie keine unnötigen Arbeiten durchführen, wenn der Farbunterschied kleiner ist als das, was durch menschliches Sehen erkannt werden kann. Bei CIECAM02 beträgt dieser Farbunterschied 1. Verwenden Sie in der Implementierung jedoch einen Schwellenwert von 0,005, um die Genauigkeit von Berechnungen beizubehalten, da dies möglicherweise nur ein Zwischenschritt in einer Kette von Transformationen ist.

ProcessTriangle implementiert die vorherige Strategie II. Beim Abrufen eines normalen Vektors vom vorberechnten Einheitennormalen Vektor zum Dreieck in Bezug auf das Standardpunktprodukt berechnet er den Abstand des Abfragepunkts zur Unendlichkeitsebene, die das Dreieck enthält, indem das Punktprodukt des Normalvektors der Einheit und der queryVector, der Vektor aus einem der Scheitelpunkte des Dreiecks, gebildet werden.  vertex1, bis zum Abfragepunkt queryPoint.

queryVector = queryPoint – vertex1

distance = \| normalVector \* queryVector \| / \| \| normalVector\|\|

Dies ist eine relativ kostengünstige Berechnung, und die Entfernung ist erforderlich, um weitere Berechnungen durchzuführen. Wenn dieser Abstand nicht kleiner als die aktuelle beste Entfernung (ShortestDistance) ist, erzeugt dieses Dreieck keinen besseren Abstand, da es keinen besseren Abstand als die Ebene ergibt, die ihn enthält. In diesem Fall geben Sie die Steuerung an die Dreiecksschleife zurück. Wenn der Abstand kleiner als ShortestDistance ist, haben Sie möglicherweise einen näheren Punkt, wenn dieser Punkt im Dreieck liegt. Sie müssen einige "harte" Berechnungen durchführen (obwohl nichts über lineare Algebra hinausgeht), um dies zu bestimmen. Wenn die anderen beiden Scheitelpunkte des Dreiecks vertex2 und vertex3 sind, bilden Sie die Basisvektoren firstBasisVector und secondBasisVector.

firstBasisVector = vertex2 – vertex1

secondBasisVector = vertex3 – vertex1

Verwenden Sie das folgende lineare System von Gleichungen, um für Unbekannte sie und v zu lösen.

firstBasisVector \* queryVector = (firstBasisVector \* firstBasisVector)u + (firstBasisVector \* secondBasisVector)v

secondBasisVector \* queryVector = (secondBasisVector \* firstBasisVector)u + (secondBasisVector \* secondBasisVector)v

und die Bedingungen für den projizierten Punkt, der innerhalb des Dreiecks liegen soll, sind:

0 ≤ u ≤ 1, 0 ≤ v ≤ 1 und Sie + v ≤ 1

Wenn nach dieser Berechnung ermittelt wird, dass der projizierte Punkt innerhalb des Dreiecks liegt, haben Sie einen neuen nächstgelegenen Punkt gefunden. Der Abstand, den Sie am Anfang berechnet haben, ist die neue kürzeste Entfernung. Aktualisieren Sie in diesem Fall die Variablen ShortestDistance und ClosestPoint. Wenn der projizierte Punkt außerhalb des Dreiecks liegt, finden Sie möglicherweise einen näheren Punkt an einem seiner Ränder. Sie können also die ProcessEdge-Routine an jedem der drei Ränder aufrufen.

![Diagramm, das den Ablauf der ProcessEdge- und ProcessVertex-Routinen zeigt.](images/gmmp-image124.jpg)

**Abbildung 34:** ProcessEdge- und ProcessVertex-Routinen

Die ProcessEdge-Routine implementiert Strategie I, wie in Abbildung 34 dargestellt. ProcessEdge beginnt mit der Überprüfung, ob der Edge zuvor verarbeitet wurde. In diesem Falle wird keine weitere Aktion ausgeführt. Falls nicht, wird die orthogonale Projektion des Abfragepunkts auf die unendliche Linie mit dem Rand berechnet. Die lineare Algebra, die an der Berechnung beteiligt ist, ähnelt den vorherigen Dreiecksgleichungen. Die Berechnung ist jedoch einfacher, sie wird hier nicht beschrieben. Wenn der projizierte Punkt innerhalb des Rands liegt, finden Sie den Abstand des projizierten Punkts vom Abfragepunkt. Wenn dieser Abstand kleiner als ShortestDistance ist, haben Sie einen neuen nächstgelegenen Punkt gefunden. Aktualisieren Sie ShortestDistance und ClosestPoint. Wenn der projizierte Punkt außerhalb des Rands liegt, rufen Sie ProcessVertex an den beiden Endpunkten auf. Bevor Sie das Steuerelement zurückgeben, aktualisieren Sie den Edgeverlauf, sodass dieser Edge als "PROCESSED" markiert ist.

Abschließend geben Sie eine Beschreibung von ProcessVertex an. Die ProjectVertex-Routine implementiert auch Strategy I und verwaltet eine Scheitelpunktverlaufstabelle. Wie in Abbildung 34 dargestellt, wird zunächst überprüft, ob der Scheitelpunkt zuvor verarbeitet wurde. In diesem Falle wird keine weitere Aktion ausgeführt. Falls nicht, wird der Abstand des Scheitelpunkts vom Abfragepunkt berechnet. Wenn der Abstand kleiner als ShortestDistance ist, aktualisieren Sie ShortestDistance und ClosestPoint. Am Ende wird der Scheitelpunktverlauf aktualisiert, sodass dieser Scheitelpunkt als "PROCESSED" markiert ist.

Wenn die äußere Steuerelementschleife entweder alle Dreiecke erschöpft oder beendet wurde, bevor der Schwellenwert für farbliche Unterschiede erreicht wurde, wird auf die Variable ClosestPoint zugegriffen. Dies ist das Ergebnis von MinDEMap. Der Aufrufer kann auch ShortestDistance abrufen, wenn er daran interessiert ist, wie weit die zugeordnete Farbe von der Abfragefarbe entfernt ist.

### <a name="hue-smoothing"></a>Farbtonglättung

![Diagramm, das zwei obere Ansichten der Farbtonglättung zeigt: den ursprünglichen oben und den farblich geglätteten Farbton am unteren Rand.](images/gmmp-image125.png)

**Abbildung 35:** Farbtonglättung

Ein Problem tritt bei Vorgängen auf, bei denen der Farbton eingeschränkt ist. Das heißt, der Vorgang berücksichtigt nur Variablen innerhalb einer Farbtonebene. Abbildung 35 zeigt ein Beispiel für eine Gamut mit "diskontinuen" Farbtonslices in den blauen Farbtons. Innerhalb dieses Farbtonbereichs ist die Gamutgrenze für bestimmte Farbtonwinkel tangential zur Farbtonebene. Dies führt tatsächlich zu einer Änderung der topologien Struktur der Farbtonslices. Im gezeigten Beispiel, während die Farbtonebene über diesen Farbtonbereich hinweg stürzt, entsteht eine "Insel" und wird untergemergt. Diese Änderung in der Topologie hat zur Diskontinuität bei hue-spezifischen Vorgängen führen. Beispielsweise ändert sich die Cusp bei festem Farbton plötzlich, wenn sich der Farbtonwinkel in diesem Bereich ändert.

Es gibt einen Grund für die Farbforschung, warum es wünschenswert ist, den Farbton in bestimmten Vorgängen zu erhalten. Um das vorherige Problem zu beheben, müssen die ursprünglichen Gamut Boundary Triangles "hue smoothed" sein. Im Allgemeinen ist eine Farbtonglättung einer Reihe von Gamut-Begrenzungsdreiecken eine Reihe von Dreiecken, die (a) die Grenze einer neuen "Gamut" bilden, die möglicherweise nicht der tatsächlichen Geräte gamut entspricht und die gamut enthält, die durch den ursprünglichen Satz von Dreiecken definiert ist; und (b) die Dreiecke in der neuen Menge sind von der Parallelität mit den Farbtonebenen entfernt.

Eine praktische Möglichkeit, einen geglätteten Satz von Dreiecken mit Farbton zu erhalten, besteht in der Konvexen Hülle der ursprünglichen Scheitelungen. Wie in Abbildung 35 dargestellt, variieren die Farbtonslices der konvexen Hülle im problematischen Farbtonbereich reibungslos, ohne dass sich die Topologie plötzlich ändert.

### <a name="setting-primaries-and-secondaries-in-the-gamut-boundary-description"></a>Festlegen von Primär- und Sekunden in der Gamut-Begrenzungsbeschreibung

Bestimmte Gamut-Zuordnungsmethoden, z. B. HueMap, hängen vom Standort der Primärgeräte und der zweiten Geräte ab. Bei additiven Geräten sind die Primärelemente rot, grün und blau (R, G und B). und die zweiten Sind Cyan, Magenta und Gelb (C, M und Y). Bei subtraktiven Geräten sind die Primärelemente C, M und Y. und die zweiten Sind R, G und B. Die GBD verfolgt alle sechs werte plus weiß und schwarz (W und K) in einem Array von Jab-Farbwerten nach. Diese Werte werden in der Gamut-Begrenzungsbeschreibung festgelegt, wenn sie erstellt werden. Für Ausgabegeräte können die Primärelemente bestimmt werden, indem Kombinationen von Gerätesteuerungswerten über das Gerätemodell ausgeführt werden. Bei Erfassungsgeräten eignet sich dieser Ansatz nicht gut für die Erstellung der Referenz-GBD, da es fast unmöglich ist, ein Bild zu erfassen, das einen vollständig verwertbare reinen Gerätewert ergibt, z. B. (0,0, 0,0, 1,0). WCS-Geräteprofile enthalten die Indizes der primärer Elemente im Erfassungsziel. Da diese Werte nicht in einemTASTE-Profil enthalten sind, verwenden Sie werte, die von einem typischen Scannerziel gemessen werden, nachdem sie in Jab konvertiert wurden, relativ zu den BEDINGUNGEN der ANZEIGE VONTB.

### <a name="setting-the-neutral-axis-in-the-gamut-boundary-description"></a>Festlegen der neutralen Achse in der Gamut-Begrenzungsbeschreibung

Die Gamutzuordnungsmethoden HueMap und Relative MinCD verwenden die geräteneutrale Achse zum Begradigen. Für die Baselineausgabegeräte kann die neutrale Achse bestimmt werden, indem geräteneutrale Werte (R=G=B oder C=M=Y) über die DeviceToColorimetric-Methode und dann über die ColorimetricToAppearance-Methode des CIECAM02-Objekts ausgeführt werden. Erfassungsgeräte geben jedoch nicht immer einen geräteneutralen Wert zurück, wenn eine neutrale Stichprobe angezeigt wird. Dies gilt insbesondere, wenn die Umgebungsbeleuchtung nicht vollkommen neutral ist. WCS-Geräteprofile enthalten die Indizes der neutralen Stichproben im Ziel. Verwenden Sie diese Beispiele, um die neutrale Achse zu setzen. Da diese Informationen für DIE-Profile nicht verfügbar sind, müssen Sie dieselbe Methode verwenden, die auch für Ausgabegeräte verwendet wird. Führen Sie geräteneutrale Stichproben über die DeviceToColorimetric-Methode aus, und paaren Sie dann die Eingabewerte und die Farbmetrikergebnisse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Konzepte der Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




