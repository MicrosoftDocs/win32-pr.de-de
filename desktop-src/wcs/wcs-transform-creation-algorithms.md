---
title: WCS-Transformationserstellungsalgorithmen
description: WCS-Transformationserstellungsalgorithmen
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Farbsystem (WCS), Transformationserstellung
- WCS (Windows Color System), Transformieren der Erstellung
- Bildfarbverwaltung, Transformationserstellung
- Farbverwaltung, Transformationserstellung
- Farben, Transformationserstellung
- Transformationserstellung
- Erstellung der WCS-Transformation
- Algorithmen,Transformationserstellung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df199f0fa649e7ce545a7b371f1caba65686746766f5572bac8e43b47413eace
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118445559"
---
# <a name="wcs-transform-creation-algorithms"></a>WCS-Transformationserstellungsalgorithmen

[Erstellen von Transformationen](#creation-of-transforms)

 

[Sequenzielle Transformationsausführung](#sequential-transform-execution)

 

[Erstellen optimierter Transformationen](#creation-of-optimized-transforms)

 

[WCProfileFromWCSProfile](#iccprofilefromwcsprofile)

 

[Black Preservation und Black Generation](#black-preservation-and-black-generation)

 

[Gamut überprüfen](#checkgamut)

## <a name="creation-of-transforms"></a>Erstellen von Transformationen

Um die Funktionsweise von Farbtransformationen richtig zu erklären, ist es hilfreich, den vollständigen Verarbeitungspfad sowohl über ICM 2.0 als auch über die Internen des CTE zu erklären. Die ICM 2.0 [**CreateColorTransformW-Funktion**](/windows/win32/api/icm/nf-icm-createcolortransformw) erstellt eine Farbtransformation, die Anwendungen für die Farbverwaltung verwenden können. Diese Funktion erstellt einen Farbkontext aus den [**LOGCOLORSPACE-**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) und Intent-Eingaben. Die Absichten werden Baselinekorrelierungen des GAMUT-Zuordnungsalgorithmus von BASELINE zugeordnet. Die Funktion ruft dann ICM 2.0-Funktion [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/) für konsistente Farbverarbeitung auf. Die **CreateColorTransform-Funktion** kopiert daten in der Regel in die intern optimierte Transformationsstruktur.

Die ICM 2.0 CreateMultiProfileTransform-Funktion akzeptiert ein Array von Profilen und ein Array von Absichten oder ein einzelnes Geräteverknüpfungsprofil und erstellt eine Farbtransformation, die Anwendungen zum Durchführen der Farbzuordnung verwenden können. Diese Eingabeprofile und Absichten werden verarbeitet, um Gerätemodelle, Farbdarstellungsmodelle, Gamutbegrenzungsbeschreibungen und gamut-Zuordnungsmodelle zu erstellen. Dies geschieht wie hier:

-   Gerätemodelle werden direkt aus DM-Profilen initialisiert. Im Aufruf von [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)wird für jedes Profil ein Gerätemodell erstellt.
-   Farbdarstellungsmodelle werden direkt aus DEN PROFILEn initialisiert. Im Aufruf von [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)gibt es ein TAR-Profil für jedes Profil. Dasselbe PROFIL kann jedoch für mehrere Profile angegeben werden.
-   Gamut-Begrenzungsbeschreibungen werden aus einem Gerätemodellobjekt und einem WEBCAM-Objekt initialisiert. Im Aufruf von [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)gibt es eine Allgemeine Begrenzungsbeschreibung für jedes Profil.
-   Gamut-Zuordnungsmodelle werden von zwei gamut-Grenzen und einer Absicht initialisiert. Sie müssen ein gamut-Zuordnungsmodell zwischen jedem Gerätemodellpaar erstellen, das aus dem Aufruf von [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)erstellt wurde. Beachten Sie, dass Dies bedeutet, dass Sie ein gamut-Kartenmodell weniger als das Gerätemodell verwenden. Da die Anzahl der Absichten mit der Anzahl der Gerätemodelle übereinstimmt, gibt es auch eine Absicht mehr als erforderlich. Die erste Absicht in der Liste wird übersprungen. Sie durchlaufen die Liste der Gerätemodelle und Absichten und erstellen gamut-Zuordnungsmodelle. Wählen Sie das erste und zweite Gerätemodell und die zweite Absicht aus, und initialisieren Sie dann das erste Gamutzuordnungsmodell. Wählen Sie das zweite und dritte Gerätemodell und die dritte Absicht aus, und initialisieren Sie dann das zweite Gamutzuordnungsmodell. Fahren Sie auf diese Weise fort, bis Sie alle gamut-Zuordnungsmodelle erstellt haben.

Wenn die Profile ordnungsgemäß verarbeitet wurden und alle Zwischenobjekte erstellt und initialisiert wurden, können Sie die CITE-Transformation mit dem folgenden Aufruf erstellen. Die *pDestCAM* und *pDestDM* sind diejenigen, die dem letzten Profil im Aufruf von [**CreateMultiProfileTransform**](/windows/desktop/api/Wingdi/)zugeordnet sind.


```C++
HRESULT CreateCITEColorTransform(
 __inout     IDeviceModel          *pSourceDM,
 __inout     IColorAppearanceModel *pSourceCAM,
 __in        GamutMapArray         *pGamutMapArray,
 __inout     IColorAppearanceModel *pDestCAM,
 __inout     IDeviceModel          *pDestDM,
             EColorTransformMode    eTransformMode,
 __deref_out IColorTransform      **ppCTS
 );
```



## <a name="support-for-plug-ins"></a>Unterstützung für Plug-Ins

Ein Problem beim Einrichten der Transformationsliste besteht darin, zu überprüfen, ob ein erforderliches Plug-In verfügbar ist. Der folgende Modellschalter stellt diese Richtlinie bereit, um dieses Verhalten zu steuern. Die Verwaltung dieser Transformationsliste ist eine Methode in der intern optimierten Transformationsstruktur, aber jede Modellmethode stellt den Zeiger auf sich selbst und einen eigenen Satz von Parameterwerten bereit.

Der Modus muss einer der folgenden Sein.

-   TfmRobust: Wenn ein Messprofil ein bevorzugtes Plug-In angibt und das Plug-In nicht verfügbar ist, verwendet das neue CTE-System das Baseline-Plug-In. Wenn kein Plug-In verfügbar ist, meldet die Transformation einen Fehler.
-   TfmStrict: Wenn ColorContext ein bevorzugtes Plug-In angibt, muss das Plug-In verfügbar sein. Wenn kein bevorzugtes Plug-In gefunden wird, wird das Baseline-Plug-In verwendet. Wenn kein Plug-In verfügbar ist, meldet die Transformation einen Fehler.
-   TfmBaseline: In AddMeasurementStep können nur Baseline-Plug-Ins verwendet werden. Wenn ColorContext ein bevorzugtes Plug-In angibt, wird das Plug-In ignoriert. Wenn das Baseline-Plug-In nicht verfügbar ist, meldet die Transformation einen Fehler.

## <a name="transform-execution"></a>Transformieren der Ausführung

Die [**TranslateColors-Funktion**](/windows/win32/api/icm/nf-icm-translatecolors) ICM 2.0-API übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Zielfarbraum, wie durch eine Farbtransformation definiert. Diese Funktion überprüft intern ein Array zwischengespeicherter Farben, um den sofortigen Abgleich von häufig transformierten Farben zu ermöglichen. Diese Transformation unterstützt 8-Bit-Bytearrays pro Kanal und float-Arrays mit 32 Bit pro Kanal. Alle anderen Formate werden vor der Übergabe an den neuen CTE konvertiert.

Die ICM 2.0-API-Funktion [**TranslateBitmapBits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) übersetzt die Farben einer Bitmap mit einem definierten Format, um eine weitere Bitmap in einem angeforderten Format zu erzeugen. Diese Funktion überprüft intern ein Array zwischengespeicherter Farben, um den sofortigen Abgleich von häufig transformierten Farben zu ermöglichen. Um zu viele Codepfade, Unterstützung und Testkomplexität zu vermeiden, wird in der Transformations- und Interpolations-Engine nur eine begrenzte Anzahl von Bitmapformaten unterstützt. Diese Funktion muss die nicht nativen ein- und ausgehenden Bitmapformate zur Verarbeitung in nativ unterstützte Formate übersetzen. Diese Transformation unterstützt nur 8-Bit-Bytebitmaps pro Kanal und 32-Bit-Gleitkommabitmaps pro Kanal. Alle anderen Formate werden vor der Übergabe an den neuen CTE konvertiert.

 

### <a name="sequential-transform-execution"></a>Sequenzielle Transformationsausführung

Wenn für den *dwFlags-Parameter* das BIT SEQUENTIAL \_ TRANSFORM festgelegt ist, wenn die ICM Funktionen [**CreateColorTransformW**](/windows/win32/api/icm/nf-icm-createcolortransformw) oder **CreateMultiProfileTransform** aufgerufen werden, werden die Transformationsschritte sequenziell ausgeführt. Dies bedeutet, dass der Code die einzelnen Gerätemodelle, Farbdarstellungsmodelle und Gamutzuordnungsmodelle separat durchschneidet, wie durch den Aufruf von **CreateColorTransform** oder **CreateMultiProfileTransform** angegeben. Dies kann beim Debuggen von Plug-In-Modulen hilfreich sein, ist aber viel langsamer als die Ausführung durch eine optimierte Transformation. Die Ausführung im sequenziellen Modus wird daher für Produktionssoftware nicht empfohlen. Darüber hinaus kann es geringfügige Unterschiede in den Ergebnissen geben, die im sequenziellen Modus und im optimierten Modus ermittelt werden. Dies liegt an Variationen, die eingeführt werden, wenn die Funktionen miteinander verkettet werden.

### <a name="creation-of-optimized-transforms"></a>Erstellen optimierter Transformationen

Eine optimierte Transformation ist eine mehrdimensionale Nachschlagetabelle. Die Tabelle kann von einer mehrdimensionalen Interpolations-Engine verarbeitet werden, z. B. der interpolalen Interpolation, die die Eingabefarben auf die Transformation anwendet. Im folgenden Abschnitt wird beschrieben, wie die optimierten Nachschlagetabellen erstellt werden. Im folgenden Abschnitt wird beschrieben, wie sie innerhalb der optimierten Nachschlagetabellen interpoliert werden.

## <a name="sparse-lookup-tables"></a>Nachschlagetabellen mit geringer Dichte

Herkömmliche Drucker verfügen über CMYK-Farben. Um die allgemeine Skala zu erweitern, besteht ein Ansatz darin, dem System neue Farben hinzuzufügen. Bei den in der Regel hinzugefügten Farben handelt es sich um Farben, bei denen die Reproduktion von CMYK-Inks schwierig ist. Gängige Optionen sind Orange, Grün, Rot, Blau usw. Um die "sichtbare Auflösung" zu erhöhen, können Farben mit unterschiedlichen Tönungen verwendet werden, z. B. "Light Cyan", "Light Magenta" usw. Das Druckergerät verfügt über mehr als vier Kanäle.

Obwohl Drucker Ausgabegeräte sind, führen sie auch die Farbkonvertierung vom Gerätebereich in einen anderen Farbraum durch. Im Fall eines CMYK-Druckers wäre dies eine Transformation von CMYK zu XYZ oder das "Vorwärtsmodell" des Druckers. Durch Kombinieren des Vorwärtsmodells mit anderen Transformationen ist es möglich, einen CMYK-Druck auf einem anderen Gerät zu emulieren. Beispielsweise würde ein CMYK-Drucker für einen Monitor RGB einen Proofingmechanismus ermöglichen, der einen Druck dieses CMYK-Druckers auf einem Monitor emuliert. Gleiches gilt auch für Hi-Fi-Drucker. Eine KONVERTIERUNG VON CMYKOG in RGB ermöglicht den Nachweis des CMYKOG-Druckers auf einem Monitor.

Der herkömmliche Ansatz zum Implementieren einer solchen Farbkonvertierung ist die Verwendung eines einheitlichen UNIFORM. Beispielsweise ist in einem PRINTER-Profil für einen CMYKOG-Drucker die QUOTT-Spezifikation für ein A2B1-Tag festgelegt, das einen einheitlichen CMS speichert, der eine einheitliche Stichprobenentnahme im CMYKOG-Gerätebereich des Vorwärtsmodells darstellt, das von CMYKOG zum VERBINDUNGSraum des PROFILS (CIELAB oder CIEXYZ) wechselt. Das GERÄTELINK-Profil ermöglicht eine direkte Transformation vom CMYKOG-Gerätebereich in einen beliebigen Farbraum, einschließlich eines Gerätebereichs, auch in Form eines UNIFORM-Samplings im CMYKOG-Bereich. Die Stichprobenentnahme erfolgt aufgrund der großen RESULTIERENDEN ERGEBNISSE nie mit 256 Ebenen (Bittiefe 8), mit Ausnahme von monocoloren Geräten (1 Kanal). Stattdessen wird die Stichprobenentnahme mit niedrigerer Bittiefe verwendet. Einige typische Auswahlmöglichkeiten sind 9 (Bittiefe 3), 17 (Bittiefe 4), 33 (Bittiefe 5). Mit der Anzahl der Ebenen, die in jedem Kanal kleiner als 256 sind, wird der CSV in Verbindung mit einem Interpolationsalgorithmus verwendet, um das Ergebnis zu erzeugen, wenn eine Ebene zwischen zwei Stichprobenebenen liegt.

Während ein einheitliches UNIFORM-Objekt konzeptionell einfach zu implementieren ist und die Interpolation auf einem einheitlichen UNIFORM-Wert im Allgemeinen effizient ist, nimmt die GRÖßE von INTERPOL mit der Eingabedimension exponentiell zu. Wenn *d* die Anzahl von Schritten ist, die in der einheitlichen UNIFORM-Regel verwendet werden, und *n* die Anzahl der Kanäle im Quellfarbraum, dann ist die Anzahl der Knoten in der ![ CSV-Datei Zeigt die Variable für die Anzahl der Knoten in einem CAB ](images/transformcreation-image002.gif) an. Natürlich erfordert die Anzahl der Knoten schnell so viel Speicher im Arbeitsspeicher, dass selbst Top-of-the-Line-Computingsysteme Schwierigkeiten haben, den Bedarf zu verarbeiten. Für Geräte mit sechs oder acht Kanälen erfordert eine SIX-Implementierung des Geräteprofils die Verwendung einiger Schritte in der CSV-Datei, manchmal sogar bis zu fünf Schritte in der Tabelle A2B1, um das Profil innerhalb von Megabyte anstelle von Gigabytes beizubehalten. Die Verwendung einer kleineren Anzahl von Schritten erhöht eindeutig die Interpolationsfehler, da jetzt weniger Stichproben vorhanden sind. Da das -OBJEKT einheitlich sein muss, wird die Genauigkeit über den gesamten Farbraum sogar in den Bereichen des Raums beeinträchtigt, in denen ein signifikanter Farbunterschied durch kleine Änderungen des Gerätewerts verursacht werden kann.

Bei Geräten mit mehr als vier Farbelementen sind bestimmte Unterräume des gesamten Gerätebereichs wichtiger als andere. Im CMYKOG-Bereich werden z. B. Cyan- und grüne Farben selten zusammen verwendet, da sich ihre Farbtons größtenteils überlappen. Analog dazu überlappen sich gelbe und orangefarbene Farben größtenteils. Eine einheitliche Verringerung der Anzahl von Schritten kann als allgemeine Qualitätsminderung im gesamten Farbraum betrachtet werden. Dies ist etwas, das Sie sich für die unwahrscheinlichen Freihandkombinationen, aber nicht für die wahrscheinlichen oder wichtigen Kombinationen leisten können.

Während ein uniformiertes SAMPLING für interpolation einfach und effizient ist, stellt es mit zunehmender Dimension große Arbeitsspeicheranforderungen. In der Praxis kann ein Gerät sechs oder acht Kanäle aufweisen, sie werden jedoch selten gleichzeitig verwendet. In den meisten Fällen weist die Transformation für Die Eingabefarbe in Farbe nur wenige "aktive" Farbmittel auf und befindet sich daher in einem wenigerdimensionalen Farbraum. Dies bedeutet auch, dass die Interpolation in diesem niedrigeren dimensionalen Raum effizienter durchgeführt werden kann, da die Interpolation schneller ist, wenn die Dimension niedriger ist.

Daher besteht der Ansatz darin, den gesamten Gerätebereich in Unterräume verschiedener Dimensionen zu unterteilen. Und da niedrigere Dimensionen (die drei oder vier Farbmittel kombinieren) wichtiger sind, können Sie durch die Geschichteung des Raumes auch unterschiedliche Samplingraten anwenden. das heißt, eine andere Anzahl von Schritten als die einzelnen Schritte; Erhöhen der Samplingraten für niedrigere Dimensionen, verringern sie für höhere Dimensionen.

Um Notationen zu korrigieren, ist *n* die Anzahl der Kanäle im Quellfarbraum der Farbtransformation, die Sie abtasten möchten. Sie können auch auf *n* als Eingabedimension und ![ n größer oder gleich 5 verweisen.](images/transformcreation-image004.gif) , sofern nicht anders angegeben.

Die grundlegenden Bausteine sind LUTs verschiedener *Eingabedimensionen* und -größen, anstatt eines einheitlichen CSV mit eingabedimension *n*. Genauer gesagt ist ein *MATRI* ein rechteckiges Lattice, das auf einen Einheitencube gesetzt wird. das heißt, alle Gerätekoordinaten werden auf den Bereich \[ 0, 1 \] normalisiert. , wenn die Eingabedimension des Tes ist (beachten Sie, dass nicht gleich *n* sein muss, obwohl ![ V kleiner als oder gleich n anzeigt.](images/transformcreation-image006.gif) ist erforderlich), und besteht dann aus eindimensionalen Stichprobenraster:

Samp *i:* ![ Zeigt ein eindimensionales Samplingraster an.](images/transformcreation-image008.gif)

wobei alle *x <sub>j</sub>s* im Bereich \[ 0, 1 liegen \] müssen, zeigt einen ![ hochgestellten d(i) an.](images/transformcreation-image010.gif) ist die Anzahl der Schritte für die *i-ten* Kanalsampling, die mindestens 1 sein muss, und ![ Zeigt einen Spuperscript von X (Subscript) d(i) an.](images/transformcreation-image012.gif) muss 1 sein. Auf der anderen Seite ![ wird ein hochgestelltes X (Tiefgestellt 1) angezeigt.](images/transformcreation-image014.gif) muss nicht 0 sein.

Es werden nur die beiden folgenden Sonderfälle von CSV definiert.

*GeschlosseneSUNG:* Dies ist ein DASS mit der zusätzlichen Anforderung, dass für jeden Samp *<sub>i</sub>* ![ ein hochgestelltes X (Subscript 1) gleich 0 ist.](images/transformcreation-image016.gif) , und ![ Zeigt einen superscript d(i) größer als oder gleich 2 an.](images/transformcreation-image018.gif) . Ein einheitlicher geschlossener QUOTT ist ein geschlossener QUOT;, der über dasselbe ![ Verfügt Zeigt einen superscript d(i) an.](images/transformcreation-image010.gif) für jeden Kanal, und die Knoten liegen gleichmäßig zwischen 0 und 1.

*OpenTASTE:* Dies ist ein DASS mit der zusätzlichen Anforderung, dass für jedes Samp *i* ![ -SHows-A superscript X (subscript 1) größer als 0 ist.](images/transformcreation-image020.gif) . Es ist in Ordnung, wenn ![ ein superscript d(i) gleich 1 angezeigt wird.](images/transformcreation-image022.gif) .

Das Ziel besteht darin, den Einheitencube \[ 0, 1 \] *n* in eine Sammlung von geschlossenen LUTs und offenen LUTs zu geschichten, sodass die gesamte Sammlung den Einheitencube abdeckt. Es ist konzeptionell einfacher, diese "STRATA" nach ihren Dimensionen zu organisieren, sodass auf der obersten Ebene:

![Zeigt die oberste Ebene zum Organisieren von L U T-Schichten nach ihren Dimensionen an.](images/transformcreation-image024.png)

where ![ Shows sigma subscript k.](images/transformcreation-image026.gif) ist die *"k* -dimensional strata collection". Beachten Sie, dass die Strata-Dimension bei 3 anstelle von 0 beginnt. Das heißt, punktet, da die Interpolation von Kombinationen mit drei Farben ohne zu viel Arbeitsspeicherbedarf verarbeitet werden kann.

## <a name="description-of-the-lut-strata"></a>Beschreibung der STRATA

In dieser Implementierung:

1. ![Zeigt sigma subscript 3 an.](images/transformcreation-image028.gif) besteht aus geschlossenen LUTs mit drei Eingaben, eine aus jeder möglichen Kombination von drei Auswählfarben aus den *n* Farbanten.

2. ![Zeigt sigma subscript 4 an.](images/transformcreation-image030.gif) besteht aus einem geschlossenen CMS für die Kombination aus CMYK (oder den ersten vier Colorants) sowie ![Zeigt (n über 4) minus 1 an.](images/transformcreation-image032.png) Öffnen Sie LUTs für alle anderen Kombinationen mit vier Farben. Indem Sie die CMYK-Kombination aussingen, bestätigen Sie, dass es sich um eine wichtige Kombination handelt.

3. Für ![ Zeigt k gleich 5, ..., n an.](images/transformcreation-image034.gif) ![, zeigt sigma subscript k.](images/transformcreation-image026.gif) besteht aus ![ Shows (n über k).](images/transformcreation-image037.gif) öffnen Sie LUTs, eine für jede mögliche Kombination aus *k* Farbgebungsarten aus der Gesamtanzahl von *n* Farbanten.

Es bleibt, die Größen der LUTs anzugeben. Der Hauptunterschied zwischen offenen und geschlossenen LUTs besteht darin, dass sich offene LUTs nicht überlappen und dass sich geschlossene LUTs an den Begrenzungsflächen überlappen können. Die Tatsache, dass die eindimensionale Stichprobenentnahme in einem geöffneten DOMÄNENNAMEN nicht 0 (0) enthält, bedeutet im Wesentlichen, dass einem geöffneten MSI die Hälfte der Begrenzungsgesichter fehlt, daher der Name "open". Wenn sich zwei LUTs nicht überlappen, können Sie eine andere Anzahl von Schritten oder Knotenspeicherorten in jedem Kanal verwenden. Dasselbe gilt nicht, wenn sich zwei LUTs überlappen. Wenn sich die Anzahl der Schritte oder die Knotenpositionen in diesem Fall unterscheiden, erhält ein Punkt, der sich in der Schnittmenge der beiden LUTs befindet, einen anderen Interpolationswert, je nachdem, welcher INTERPOL-Wert in der Interpolation verwendet wird. Eine einfache Lösung für dieses Problem ist die Verwendung einer einheitlichen Stichprobenentnahme mit der gleichen Anzahl von Schritten, wenn sich zwei LUTs überlappen. Anders gesagt:

Alle geschlossenen LUTs (alle dreifarbigen LUTs und cmyk-LUTs in dieser Implementierung) müssen einheitlich sein und über die gleiche Anzahl von Schritten verfügen, die *als d* bezeichnet werden.

Die folgenden beiden Algorithmen können verwendet werden, um die Anzahl der Schritte *d* für geschlossene LUTs und die Anzahl der Schritte für geöffnete LUTs zu bestimmen.

## <a name="algorithm-1"></a>Algorithmus \# 1

Dieser Algorithmus erfordert keine externe Eingabe.

Alle geschlossenen LUTs sind mit *einer* Anzahl von Schritten gleich.

Alle offenen LUTs der Dimension *k* weisen dieselbe Anzahl von Schritten ![ auf. Zeigt d(k) an.](images/transformcreation-image039.gif) in jedem Eingabekanal, und die Knoten sind gleichmäßig voneinander getrennt. d. h., für jede ![ Show i equal to 1, 2, ..., k.](images/transformcreation-image041.gif) .

Samp *i:* ![ Zeigt den samp i-Algorithmus an.](images/transformcreation-image043.png)

Geben Sie abschließend *d* und *d* (*k* ) in der folgenden Tabelle 1 an. Die drei Modi "Proof", "normal" und "best" sind die ICM 2.0-Qualitätseinstellungen. In dieser Implementierung weist der Proof-Modus den kleinsten Speicherbedarf und der beste Modus den größten Speicherbedarf auf.

Um diesen Algorithmus zu implementieren, müssen Sie den folgenden Algorithmus \# 2 aufrufen. Benutzer können ihre eigenen Samplingspeicherorte angeben, indem sie die Tabellen als Leitfaden verwenden.

## <a name="algorithm-2"></a>Algorithmus \# 2

Dieser Algorithmus erfordert externe Eingaben in Form einer Liste von "wichtigen" Samplingspeicherorten, ist jedoch adaptiver und kann potenziell Speicherplatz sparen.

Die erforderliche Eingabe ist ein Array von Gerätewerten, die vom Benutzer bereitgestellt werden. Diese Gerätewerte geben an, welcher Bereich des Gerätefarbraums wichtig ist. Das heißt, welche Region mehr Stichproben entnommen werden soll.

Alle geschlossenen LUTs sind mit *einer* Anzahl von Schritten gleich, wie in Algorithmus \# 1 beschrieben. Werte für *d* werden in Tabelle 1 bereitgestellt.

*(a) Uniform Closed DASS*



|         | Proof-Modus | Normaler Modus | Optimaler Modus |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) Öffnen sie DEN*



| Eingabedimension | Proof-Modus | Normaler Modus | Optimaler Modus |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 oder mehr       | 2          | 2           | 2         |



 

**Tabelle 1:** IM Algorithmus verwendete GRÖßEN

Jede geöffnete BEIT kann in jedem Eingabekanal eine andere Anzahl von Schritten haben, und die Samplingspeicherorte müssen nicht gleichmäßig verteilt sein. Für ein bestimmtes offenesENDE-Stratum gibt es eine zugeordnete Farbkombination, z. B. ![ Zeigt den C-Subskript 1, ..., den C-Subskript k an.](images/transformcreation-image045.gif) , wobei der ![ C-Unterskript i zeigt.](images/transformcreation-image047.gif) s sind unterschiedliche ganze Zahlen zwischen 1 und *n.* Sie sind die Kanalindizes, die den "aktiven" Farbgebungsindizes in dieser Schicht entspricht.

SCHRITT 1: Filtern Sie das eingegebene Array von Gerätewerten heraus, die nicht in dieser Schicht enthalten sind. Ein Gerätewert ![ Zeigt X subscript 1, X subscript 2, ..., X subscript n an.](images/transformcreation-image049.gif) ist in der Strata enthalten, wenn und nur dann, wenn eine ![ Gruppe von Werten für einen Kanal zeigt.](images/transformcreation-image051.gif) und alle anderen Kanäle sind 0. Wenn die gefilterte Gruppe *N Einträge* auflistet, lassen Sie

![Zeigt eine Gleichung an, die verwendet werden soll, wenn die gefilterte Gruppe N Einträge enthält.](images/transformcreation-image053.png)

Für jede ![Zeigt i gleich 1, 2, ..., k an.](images/transformcreation-image041.gif) , führen Sie die folgenden Schritte 2-5 aus:

SCHRITT 2: Wenn ![ d als vorläufiges Inskript (k) gleich 1 zeigt.](images/transformcreation-image055.gif) , SAMP *i* hat nur 1 Punkt, was 1,0 sein muss. Wechseln Sie zum nächsten *i.* Fahren Sie andernfalls mit SCHRITT 3 fort.

SCHRITT 3: Sortieren der gefilterten Stichproben in aufsteigender Reihenfolge in der ![Zeigt den C-Unterskript i an.](images/transformcreation-image047.gif) channel.

SCHRITT 4: Definieren des "vorläufigen" Samplingrasters mithilfe der Knoten

![Zeigt die Knoten an, die zum Definieren des "vorläufigen" Samplingrasters verwendet werden.](images/transformcreation-image057.png)

where ![Zeigt j gleich 1, 2, ..., d vorläufiges Inskript (k) an.](images/transformcreation-image059.gif) .

SCHRITT 5: Regularisieren Sie das vorläufige Raster, um sicherzustellen, dass es der strengen Monotonie entspricht und mit 1.0 endet. Da das Array bereits sortiert ist, sind die Knoten im vorläufigen Raster bereits monoton und nicht dekrementierend. Angrenzende Knoten sind jedoch möglicherweise identisch. Sie können dies beheben, indem Sie bei Bedarf identische Knoten entfernen. Wenn der Endpunkt nach diesem Verfahren kleiner als 1.0 ist, ersetzen Sie ihn schließlich durch 1.0.

Beachten Sie, dass SCHRITT 5 der Grund dafür ist, dass die STRAT-Schicht in jedem Kanal eine andere Anzahl von Schritten haben kann. Nach der Regularisierung kann die Anzahl der Schritte in einem Kanal kleiner als sein. ![Zeigt d subscript vorläufiges (k) an.](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolation

Sie können die Schichtung des Unitcubes erstellen, indem Sie DIE Strata öffnen und die STRAT-Schicht schließen. Führen Sie die folgenden Schritte aus, um die Interpolation mithilfe dieser "SPARSE-STRUKTUR" durchzuführen. Angenommen, es wird ein angegebener Eingabegerätwert angenommen. ![Zeigt (X Subscript 1, X Subscript 2, ..., X subscript n).](images/transformcreation-image049.gif) .

SCHRITT 1: Bestimmen sie die Anzahl der "aktiven" Kanäle. Dies ist die Anzahl von Kanälen, die nicht 0 (null) sind. Dadurch wird die Stratadimension *k bestimmt,* die nach dem enthaltenden Stratum gesucht werden soll. Genauer gesagt ist die Stratadimension 3, wenn die Anzahl der aktiven Kanäle ![ Kleiner als oder gleich 3 ist.](images/transformcreation-image063.gif) , andernfalls ist die Stratadimension mit der Anzahl der aktiven Kanäle identisch.

SCHRITT 2: Innerhalb von ![Zeigt sigma subscript k an.](images/transformcreation-image026.gif) , suchen Sie nach dem enthaltenden Stratum. Ein Gerätewert ist in einem offenen Stratum enthalten, wenn alle dem Stratum entsprechenden Kanäle einen Wert von nicht 0 (null) haben und alle anderen Kanäle 0 (null) sind. Ein Gerätewert ist in einem geschlossenen Stratum enthalten, wenn jeder Kanal, der nicht durch das Stratum dargestellt wird, 0 (null) ist. Wenn kein enthaltenes Stratum gefunden wird, liegt eine Fehlerbedingung vor. Abbrechen und Melden eines Fehlers. Wenn ein enthaltenes Stratum gefunden wird, fahren Sie mit dem nächsten Schritt fort.

SCHRITT 3: Wenn das enthaltende Stratum geschlossen ist, kann die Interpolation innerhalb des Stratums von jedem bekannten Interpolationsalgorithmus durchgeführt werden. In dieser Implementierung ist die Wahl des Algorithmus die lineare Interpolation. Wenn das enthaltende Stratum offen ist und der Gerätewert ausschließlich innerhalb des Stratums liegt, d. h.

![Zeigt X-Unterskript i größer oder gleich... an. ](images/transformcreation-image065.gif) Erster Knoten  im i-th-Kanal

Wobei *i* ein Kanalindex für das Stratum ist, dann funktioniert der Standardinterpolationsalgorithmus, z. B. die interpolierte Interpolation.

Wenn X Subscript i less than... erster Knoten im i th-Kanal für einige i zeigt, fällt der Gerätewert in die "Lücke" zwischen dem Stratum und den unteren ![ ](images/transformcreation-image067.gif) dimensionalen Teilbereich.   Diese MOI betrifft keinen Interpolationsalgorithmus an sich, sodass jeder Interpolationsalgorithmus verwendet werden kann, um innerhalb dieser "Lücke" zu interpolieren, obwohl der bevorzugte Algorithmus die folgende transfinite Interpolation ist.

Die Architektur des Interpolationsmoduls wird in den beiden Teilen von Abbildung 1 veranschaulicht.

![Diagramm, das den ersten Teil der Architektur des Interpolationsmoduls zeigt.](images/transformcreation-image068.png)

![Diagramm, das den zweiten Teil der Architektur des Interpolationsmoduls zeigt.](images/transformcreation-image070.png)

**Abbildung 1:** Architektur des Intepolation-Moduls

Wie bereits erläutert, ist dieser Algorithmus in der Lage, eine relativ dichte Stichprobenentnahme in Regionen des Geräteraums zu erreichen, die eine wichtige Kombination von Farbmittel enthalten, während gleichzeitig die Gesamtgröße der benötigten LUTs minimiert wird. Die folgende Tabelle zeigt einen Vergleich der Anzahl von Knoten, die für die SPARSE-IMPLEMENTIERUNG (mit Algorithm 1 und dem normalen Modus) benötigt werden, und der entsprechenden \# einheitlichenFORMAT-Implementierung.



| **Anzahl der Eingabekanäle** | **Sparse-WIESE** | **UniformITÄT** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolation innerhalb eines Einheitencubes

Ein grundlegender Schritt im Fall eines rechteckigen Rasters ist die Interpolation innerhalb einer umschließenden Zelle. Für einen Eingabepunkt können Sie die umschließende Zelle leicht bestimmen. In einem rechteckigen Raster wird der Ausgabewert an jedem Scheitelpunkt (Eckpunkte) der umschließenden Zelle angegeben. Sie sind auch die einzigen Begrenzungsbedingungen (Boundary Conditions, BCs), die ein Interpolant erfüllen muss: Die Interpolant muss alle diese Punkte passieren. Beachten Sie, dass sich diese Begrenzungsbedingungen an "diskreten" Punkten befinden, in diesem Fall an den 2n Eckpunkten der Zelle, wobei n die Dimension des Farbraums ist.

Es ist hilfreich, das Konzept der Begrenzungsbedingungen zu formalisieren, bevor Sie mit diesem Verfahren fortfahren. Für jede Teilmenge S der Grenze der einschließenden Zelle (der Einheitencube in n Dimensionen) ist eine Begrenzungsbedingung für S eine Spezifikation einer Funktion BC: S → Rm, wobei m die Ausgabedimension ist. Anders ausgedrückt: Ein Interpolant, der als Interp: \[ 0,1 \] n→ Rm bezeichnet werden kann, muss erfüllen: Interp(x) = BC(x) für alle x in S.

Im Standardszenario der Interpolation für den Einheitencube ist S der Satz diskreter Punkte, die die 2n Scheitelpunkte des Cubes sind.

Sie können jetzt die Begrenzungsbedingungen generalisieren, um die zuvor beschriebenen Probleme zu beheben und einen neuen Interpolationsalgorithmus innerhalb des Komponentencubes bereitzustellen. Anstatt nur diskrete Begrenzungspunkte zuzulassen, können Begrenzungsbedingungen für eine gesamte Begrenzungsflächen des Cubes erzwungen werden. Die genauen Annahmen sind wie folgt:

(a) Der Punkt vn =(1,1,...,1) ist speziell und nur eine diskrete Begrenzungsbedingung ist zulässig. Anders ausgedrückt: Für die n Begrenzungsflächen xi=1 (i=1,...,n) können keine kontinuierlichen Begrenzungsbedingungen erzwungen werden.

(b) Für jedes der verbleibenden n Begrenzungsflächen xi=0 (i=1,...,n) kann die Begrenzungsbedingung für das gesamte Gesicht mit der Kompatibilitätsbedingung erzwungen werden, dass sich die Begrenzungsbedingungen auf den Gesichtern auf der Schnittmenge einigen sollten, wenn sich zwei Gesichter überschneiden.

(c) Alle Scheitelpunkte, die nicht in den Gesichtern mit Begrenzungsbedingung enthalten sind, verfügen über eine individuelle (diskrete) Begrenzungsbedingung.

Sie können eine diskrete Begrenzungsbedingung als endliche Daten und eine kontinuierliche Begrenzungsbedingung als transfinite Daten bezeichnen, wenn Sie interpolation für endliche und transfinite Daten erörtern.

Überprüfen Sie zunächst die standardmäßige interpolale Interpolation (z. B. die, die im Patent von Sakacca verwendet wird), um die Notationen für diese spezielle Formulierung des Problems festzulegen. Es ist bekannt, dass der Einheitencube \[ \] 0,1 n in n! unterteilt werden kann. libhedra, parametrisiert durch den Satz von Permutationen auf n Symbolen. Genauer gesagt wird jedes dieser Klammern durch Klammern definiert.

![Zeigt die Formel für die Inequalites der Leistenhedrons an.](images/transformcreation-image073.gif)

wobei σ:{1,2,..,n}→{1,2,...,n} eine Permutation von "Symbolen" 1, 2, ..., n, d. h. eine Bijektivzuordnung des n-Symbolsatzes ist. Wenn z.B. n = 3 und σ = (3, 2, 1) bedeutet, was σ(1)=3, σ(2)=2, σ(3)=1 bedeutet, wird das entsprechende edron durch z≥y≥x definiert, wobei die gemeinsame Notation x, y, z für x1, x2, x3 verwendet wird. Beachten Sie, dass diese Klammern nicht voneinander abgeknöpft sind. Zum Zweck der Interpolation haben Punkte, die auf einem gemeinsamen Gesicht von zwei unterschiedlichen Klammern stehen, den gleichen Interpolationswert, unabhängig davon, welches Klammerzeichen in der Interpolation verwendet wird. Im Standardszenario der Interpolation an endlichen Punkten für einen bestimmten Eingabepunkt (x1, ..., xn) müssen Sie jedoch zunächst bestimmen, in welchem Skalarhedron es sich befindet, oder entsprechend der entsprechenden Permutation σ, dann wird das interpolale Interpolant für die Vergrößerung als definiert.

![Zeigt die Gleichung an, die das interpolale Interpolant für die Klammer definiert.](images/transformcreation-image075.png)

where ![Zeigt die Gleichung für die Standardbasisvektoren an.](images/transformcreation-image077.png) für i=1, ..., n und e1, ..., en sind die Standardbasisvektoren. Bevor Sie mit der Generalisierung fortfahren, beachten Sie, dass v0, v1, ..., vn die Scheitelpunkte des Gittershedrons sind und ![Zeigt die baryzentrischen Koordinaten an.](images/transformcreation-image079.png) sind die "barycentric-Koordinaten".

Für den allgemeinen Fall von BCs auf Begrenzungsgesichtern können Sie das Konzept der baryzentrischen Projektion verwenden. Bestimmen Sie wie zuvor für einen bestimmten Eingabepunkt (x1, ..., xn) zuerst, in welchem Klammerhedron er sich befindet, oder bestimmen Sie entsprechend die entsprechende Permutation σ. Führen Sie dann wie folgt eine Reihe baryzentrischer Projektionen aus. Die erste Projektion ![Zeigt BProj-Tiefskript 1 (x) an.](images/transformcreation-image081.gif) sendet den Punkt an die Ebene. ![Zeigt das X-Tiefgestelltdelta (1) gleich 0 an.](images/transformcreation-image083.gif) Es sei denn ![Zeigt X gleich V subscript n an.](images/transformcreation-image085.gif) In diesem Fall wird sie nicht geändert. Die genaue Definition des Karten-BProj wird wie folgt definiert:

![Zeigt die Gleichung für die genaue Definition des Karten-BProj an.](images/transformcreation-image087.png)

durch ![Zeigt die Gleichung für P subscript k an.](images/transformcreation-image089.png) und k = 1, 2, ..., n.

In diesem Fall ![Zeigt an, dass X gleich V subscript n ist.](images/transformcreation-image085.gif) können Sie beenden, da BC bei vn durch Annahme (a) definiert wird. In diesem Fall ![Zeigt an, dass X ungleich V subscript n ist.](images/transformcreation-image091.gif) , ist klar, dass ![Zeigt BProj-Tiefskript 1 (X) an.](images/transformcreation-image081.gif) wird die σ(1)-Komponente gelöscht. Anders ausgedrückt: Es befindet sich auf einem der Begrenzungsflächen. Entweder befindet es sich auf einem Gesicht, auf dem BC definiert ist, in diesem Fall können Sie beenden, oder Sie führen eine andere baryzentrische Projektion aus. ![Zeigt BProj subscript 2 (X') an.](images/transformcreation-image093.gif) where ![Zeigt X' gleich BProj subscript 1 (X) an.](images/transformcreation-image095.gif) . Und wenn ![Zeigt X''= Bproj subscript 1 (X') an.](images/transformcreation-image097.gif) befindet sich auf einem Gesicht, auf dem BC definiert ist. Sie können anhalten. Führen Sie andernfalls eine weitere Projektion aus. ![Zeigt BProj-Tiefskript 3 (X'') an.](images/transformcreation-image099.gif) . Da jede Projektion eine Komponente auslöscht, verringert sich die effektive Dimension, sodass Sie wissen, dass der Prozess schließlich beendet werden muss. Im schlimmsten Fall führen Sie n Projektionen bis zu Dimension 0 aus, d. h. Scheitelpunkte für den Cube, für die gemäß Annahme (c) BC definiert wird.

Vorausgesetzt, dass K-Projektionen ausgeführt wurden, mit

![Zeigt eine zu verwendende Gleichung an, wenn die K-Projektion ausgeführt wurde.](images/transformcreation-image101.png)

x(0)= x, der Eingabepunkt und BC werden bei x(k) definiert. Entladen Sie dann die Projektionen, indem Sie eine Reihe von Ausgabevektoren definieren:

![Zeigt Gleichungen für eine Reihe von Ausgabevektoren an.](images/transformcreation-image103.png)

where ![Zeigt die Gleichung für Y superscript (K) an.](images/transformcreation-image105.gif) , und Sie erhalten schließlich die Antwort.

![Zeigt Interp(x) gleich y superscript (0) an.](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Arbeitsbeispiel

![Diagramm, das ein bearbeitetes Beispiel für die Interpolation mit einem Einheitencube zeigt.](images/transformcreation-image108.png)

**Abbildung 2:** Beispiel für "Funktioniert"

Betrachten Sie die in Abbildung 2 dargestellte Situation, in der n = 3, m = 1 und die folgenden BCs vorhanden sind:

(a) Vier diskrete BCs auf den Scheitelpunkten

(0, 0, 1): β001

(0, 1, 1): β011

(1, 0, 1): β101

(1, 1, 1): β111

(b) Ein fortlaufender BC im Gesicht x3=0: F(x1, x2)

Berechnung \# 1: Eingabepunkt x = (0,8, 0,5, 0,2). Das einschließende Barehedron ist der Permutation &lt; 1, 2, 3 &gt; zugeordnet.

1. Projektion: ![Zeigt die Gleichung für die erste Projektion an.](images/transformcreation-image110.png)

Dies befindet sich bereits im Gesicht x3=0, sodass Sie anhalten können. Die Rückwärtsersetzung gibt dann

![Zeigt die Antwort für die erste Projektion an.](images/transformcreation-image112.png) Dies ist die Antwort.

Berechnung \# 2: Eingabepunkt x = (0,2, 0,5, 0,8). Das einschließende Barehedron ist der Permutation &lt; 3, 2, 1 &gt; zugeordnet.

1. Projektion: ![Zeigt die Gleichung für die erste Projektion von Berechnung 2.](images/transformcreation-image113.png)

2. Projektion: ![Zeigt die Gleichung für die zweite Projektion von Berechnung 2.](images/transformcreation-image115.png)

Dritte Projektion: ![Zeigt die Gleichung für die dritte Projektion von Berechnung 2 an.](images/transformcreation-image117.png) , das sich im Gesicht x3=0 befindet. Die Rückwärtsersetzung gibt dann

![Zeigt die ersten beiden Gleichungen für die Rückwärtsersetzung an.](images/transformcreation-image119.png)

![Zeigt die dritte Gleichung für die Rückwärtsersetzung.](images/transformcreation-image123.png), was die endgültige Antwort ist.

## <a name="applications"></a>Anwendungen

*(a) Sequenzielle lineare Interpolation*

![Diagramm mit sequenzieller interpolierender Interpolation](images/transformcreation-image124.png)

**Abbildung 3:** Sequenzielle sequenzielle Interpolation

Weitere Informationen finden Sie in Abbildung 3. Um zwischen zwei Ebenen zu interpolieren, auf denen inkompatible Raster eingeführt wurden, betrachten Sie eine Zelle, die einen bestimmten Punkt P in der Abbildung umschließt. Die "oberen" Scheitelungen der Zelle stammen direkt aus dem Raster in der obersten Ebene. Die Scheitelzeichen im unteren Gesicht sind nicht mit dem Raster in der unteren Ebene kompatibel, sodass das gesamte Gesicht so behandelt wird, als ob es ein BC mit Werten gibt, die durch Interpolation im Raster in der unteren Ebene ermittelt wurden. Es ist dann klar, dass dieses Setup die obigen Annahmen (a), (b) und (c) erfüllt, und Sie können den Interpolationsalgorithmus anwenden.

Es ist auch klar, dass der Algorithmus die Dimension des Interpolationsproblems um 1 reduziert hat, da das Ergebnis eine lineare Kombination von Werten an den Scheitelwerten im oberen Raster und Interpolation in der unteren Ebene ist, die eine Dimension kleiner als 1 hat. Wenn eine ähnliche Sandwichingebenenkonfiguration in der unteren Ebene vorhanden ist, können Sie die Prozedur auf dieser Ebene anwenden, um die Dimension um 1 weiter zu reduzieren. Dieses Verfahren kann fortgesetzt werden, bis Dimension 0 erreicht ist. Diese Kaskadierung von Projektionen und Interpolationen kann als "Sequenzielle interpolation" bezeichnet werden.

*(b) Lückeninterpolation*

![Diagramm, das die Lückeninterpolation zeigt.](images/transformcreation-image126.jpg)

**Abbildung 4:** Lückeninterpolation

Dies ist ein Raster, das für einen Würfel gilt, der sich ausschließlich innerhalb des positiven Quadranten befindet. Der Cube selbst verfügt über ein Raster, und jede Koordinatenebene verfügt über Raster, die nicht unbedingt kompatibel sind. Die "Lücke" zwischen dem Cube und den Koordinatenebenen verfügt über einen "L-förmigen" Abschnitt, der für Standardtechniken nicht erreichbar ist. Mit der hier vorgestellten Technik können Sie jedoch problemlos Zellen einführen, die diese Lücke schließen. Abbildung 4 zeigt eine davon. Die Raster auf den Koordinatenebenen unterstützen die Interpolation, die die erforderlichen BCs für alle unteren Gesichter der Zelle mit einem verbleibenden Scheitelpunkt zur Verfügung stellt, dessen BC von der unteren Ecke des Cubes bereitgestellt wird.

## <a name="final-note-on-implementation"></a>Letzter Hinweis zur Implementierung

In der Praxis wird der "Einheitencube", der die grundlegende Einstellung des Algorithmus ist, aus größeren Lattices extrahiert, und die Werte an den Scheitelwerten erfordern möglicherweise eine teure Berechnung. Andererseits ist auch klar, dass die kubischhedrale Interpolation nur die Werte an den Scheitelwerten des Gerons erfordert, bei dem es sich um eine Teilmenge aller Scheitelsteine des Einheitencubes handelt. Daher ist es effizienter, das zu implementieren, was als "verzögerte Auswertung" bezeichnet werden kann. In einer Softwareimplementierung des vorangehenden Algorithmus ist es typisch, über eine Unterroutine zu verfügen, die den Einheitencube und die Werte an seinen Scheitelwerten als Eingabe akzeptiert. Verzögerte Auswertung bedeutet, dass anstelle der Übergabe der Werte an den Scheitelwerten die erforderlichen Informationen zum Auswerten der Werte der Scheitelungen übergeben werden, ohne die Auswertung tatsächlich durchführen zu müssen. Innerhalb der Unterroutine wird die tatsächliche Auswertung dieser Werte nur für die Scheitelpunkts durchgeführt, die zum umschließenden Gitterhedron gehören, nachdem das umschließende Allergedron bestimmt wurde.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Nachschlagetabelle für die Verwendung mit virtuellen RGB-Quellgeräten mit hohem dynamischen Bereich

Wenn eine Transformation mit einem Quellgerät erstellt wird, das als virtuelles RGB-Gerät modelliert ist, ist es möglich, dass die Farbwerte der Quelle negativ oder größer als Unity (1.0) sein können. In diesem Fall wird das Quellgerät als HDR (High Dynamic Range) bezeichnet. Für diesen Fall wird besonderer Aspekt berücksichtigt.

Bei HDR-Transformationen können die minimalen und maximalen Werte für jeden Farbkanal von der Gamutgrenze des Geräts bestimmt werden. Durch Die Verwendung dieser Werte wird eine einfache Skalierung für jeden Farbkanal angewendet, sodass Farbwerte, die dem minimalen Farbmittel entspricht, in 0,0 konvertiert werden und farbliche Werte, die dem maximalen Farbmittel entspricht, in 1,0 konvertiert werden, mit einer linearen Skalierung von Werten zwischen , um linear zwischen 0,0 und 1,0 zu ordnen.

### <a name="iccprofilefromwcsprofile"></a>CSProfileFromWCSProfile

Da der Hauptzweck dieses Features in der Unterstützung von Versionen vor Vista von Windows besteht, müssen Sie Version 2.2 DERTB-Profile generieren, wie in DER SPEZIFIKATION 1:1998-09 definiert. In bestimmten Fällen (siehe die folgende Tabelle "Baseline Device ToCS Profile Class Mapping") können Sie aus einem WCS-Profil ein Matrix- oder TRC-basiertes PROFIL erstellen. In anderen Fällen besteht dasTS-Profil aus LUTs. Im folgenden Prozess wird beschrieben, wie die AToB- und BToA-LUTs erstellt werden. NATÜRLICH verfügen DIE PROFILE auch über andere Felder. Einige der Daten können aus dem WCS-Profil abgeleitet werden. Für andere Daten müssen Sie intelligente Standardwerte entwickeln. Das Copyright wird Microsoft zugewiesen. da es sich um eine Microsoft-Technologie handelt, die zum Erstellen der LUTs verwendet wird.

Dieser Entwurf sollte für alle Arten von Gerätemodellen funktionieren, einschließlich Plug-Ins. Solange dem Plug-In ein Baselinegerätemodell zugeordnet ist, kann der zugrunde liegende Gerätetyp bestimmt werden.

Der schwierige Teil beim Erstellen eines PROFILS FÜR DIE ATOB- und BToA-Suche ist das Erstellen der AToB- und BToA-Nachschlagetabellen. Diese Tabellen werden zwischen dem Geräteraum, z. B. RGB oder C PCI, und dem Profilverbindungsraum (PCS) dargestellt, bei dem es sich um eine Variante von CIELAB handelt. Dies ist im Wesentlichen identisch mit dem Farbverwaltungsprozess, der in der ZUORDNUNGstransformation verwendet wird, um eine Zuordnung vom Gerätebereich zum Gerätebereich zu erstellen. Sie müssen jedoch über die folgenden Informationen verfügen, um die Transformation zu ermöglichen.

1) Referenzanzeigebedingungen für den PCS.

2) Referenz zur PCS-Gamut.

3) Gerätemodell, das zwischen PCS-Werten und Farbindimetrie konvertiert.

Das WCS-Profil und das zugeordnete WEBCAM werden als Parameter bereitgestellt. Es gibt zwei Baselinegerätemodelle, die zwischen Colorimetry und der PCS-Codierung konvertieren. Der Grund, warum Sie zwei benötigen, wird unten erläutert.

1) Sie können die Referenzanzeigebedingungen für den PCS aus der FORMATspezifikation des PROFILS DES PROFILS abrufen. Die informationen in der FORMATspezifikation des PROFILS FÜR DIES reichen aus, um alle Daten zu berechnen, die zum Initialisieren des vom CMS verwendeten CTIs erforderlich sind. Aus Konsistenz- und Flexibilitäts-Grund sind diese Informationen in einem WCS-Farbprofil gespeichert.

2) Sie können auch ein WCS-Profil verwenden, um Beispiele zu speichern, die die Referenz gamut des PCS definieren. Das Farbverwaltungssystem (Color Management System, CMS) von AUX verfügt über zwei Möglichkeiten zum Erstellen von Gamutgrenzen. Eine besteht in der Stichprobenentnahme des gesamten Gerätebereichs und der Verwendung des Gerätemodells zum Erstellen von Messwerten. Die zweite Methode besteht in der Verwendung von gemessenen Stichproben aus dem Profil, um eine Allgemeine Referenzgrenze zu erstellen. Da die Gamut der PCS des PCS zu groß ist, um einen nützlichen Referenz-Gamut zu machen, ist die erste Methode ungeeignet. Die zweite Methode ist jedoch ein flexibler, profilbasierter Ansatz. Sie können die Messdaten im PCS-Geräteprofil ändern, um den REFERENZ-PCS-Gamut neu zu definieren.

3) Der PCS DES PCS ist eine Modellierung eines idealen Geräts. Indem Sie ein Modell des PCS als echtes Gerät erstellen, können Sie den Farbverwaltungsprozess nutzen, der im Intelligenten CMM verwendet wird. Das Erstellen eines Gerätemodells von colorimetry bis zur PCS-Codierung ist einfach. Sie ordnen einfach die tatsächlichen Farbmetrikwerte und die PCS-codierten Werte zu. Da die CMS-Schnittstelle für Gerätemodelle nur XYZ-Werte unterstützt, müssen Sie möglicherweise auch zwischen XYZ und LAB zuordnen. Dies ist eine bekannte Transformation. Dieses Modell wird in Dokument 2.2.02 "Baselinegerätemodelle" in den Abschnitten 7.9 und 7.10 beschrieben.

Möglicherweise müssen Sie eine Gamutzuordnung durchführen, wenn die Gamut des Geräts größer als die Gamut des PCS ist. Die BASELINE-GMMs können zu diesem Zweck verwendet werden. Beachten Sie, dass ein ordnungsgemäß erstelltes NOTE-Profil Nachschlagetabellen für die Absichten Relative Colorimetric, Perceptual und Sättigung enthält, obwohl diese intern möglicherweise alle auf denselben NOTE zeigen.

![Diagramm, das die Erstellung einer A T o B L U T zeigt.](images/transformcreation-image128.png)

**Abbildung 5:** Erstellen einer AToB-1000-Datei

Dieser Prozess wird in Abbildung 5 veranschaulicht. Zunächst wird das Gerätemodell aus den Daten im DM-Profil initialisiert. Erstellen Sie dann wie folgt eine Geräte-Gamutgrenze. Eine Stichprobenentnahme von Daten aus dem Gerätemodell wird durch das Gerätemodell ausgeführt, um Farbmetrikdaten zu erhalten. Die farbmetrikmetrischen Daten werden durch dieCAM ausgeführt, um Darstellungsdaten zu erstellen. Die Darstellungsdaten werden verwendet, um die Geräte-Gamutgrenze zu erstellen.

Verwenden Sie als Nächstes Daten aus dem Referenzprofil für die PCS-Messung, um eine Gamutgrenze für die PCS zu erstellen.

Verwenden Sie die beiden gerade erstellten Gamutgrenzen, um eine GMM-Instanz zu initialisieren. Verwenden Sie dann das Gerätemodell, GMM und das PCS-Gerätemodell, um eine Transformation zu erstellen. Führen Sie eine Stichprobenentnahme des Gerätebereichs durch die Transformation aus, um ein AToB-Intervall zu erstellen.

![Diagramm, das die Erstellung einer A T o B L U T mithilfe einer Stichprobenentnahme des P C S-Raumes zeigt.](images/transformcreation-image130.png)

**Abbildung 6:** Erstellen eines BToA-15-000-Werts (BToA- UND

Abbildung 6 veranschaulicht die Erstellung des BToA-2016-2016-2016-2016-2016-BToA Dies ist fast identisch mit dem Erstellen einer AToB-DATEI mit ausgetauschten Quell- und Zielrollen. Außerdem müssen Sie den vollständigen PCS-Gamut als Beispiel verwenden, um dieÄNDer zu erstellen.

Beachten Sie, dass dietic-Anpassung zwischen dem Weißen Punkt der Medien und dem PCS-Weißpunkt (durch DIE CIECAM02 in WCS) transparent durch die WEBCAM erfolgt, da die CIECAM02 in WCS an dem Prozess beteiligt ist.

## <a name="hdr-virtual-rgb-devices"></a>Virtuelle HDR-RGB-Geräte

Beim Generieren von Profilen für virtuelle HDR-RGB-Geräte müssen sie besonders berücksichtigt werden. Das heißt, Geräte, für die die Farbwerte kleiner als 0,0 oder größer als 1,0 sein können. Bei der Generierung der ATOB-EINGANGS-LUTs wird ein größerer Satz von 1D-Eingabe-LUTs erstellt. Farbliche Werte werden skaliert und auf den Bereich 0 versetzt. 1 mit den minimalen und maximalen Farbwerten im WCS-Profil.

Da der Farbraum für HDR-Geräte wahrscheinlich nicht vollständig aufgefüllt ist, wird im 3D-FARBBEREICH auch für das Tag eine besondere Unterstützung bereitgestellt. Um Farben im mit geringer Dichte gefüllten Bereich zu verarbeiten, werden die Farbmittel neu codiert, sodass eine Extrapolation über 0,0 und 1,0 hinaus erreicht werden kann. Der verwendete Bereich ist -1. +4.

Aufgrund der für den 3D-HEX angewendeten Neuskalierung wird ein Satz von 1D-Ausgabe-LUTs erstellt, um das Ergebnis wieder dem Bereich 0 zuzuordnen. 1.

## <a name="more-than-one-pcs"></a>Mehr als ein PCS

Der WIES hat festgestellt, dass ein PCS nicht ausreichend flexibel ist, um alle vorgesehenen Verwendungszwecke eines CMS zu erfüllen. In Version 4 der Profilspezifikation hat der ZIP-Code verdeutlicht, dass es tatsächlich zwei PCS-Codierungen gibt. Eine wird für die farbmetrischen Absichten verwendet. ein anderer wird für die wahrnehmbare Absicht verwendet. (Für die Absicht Sättigung wird kein PCS angegeben. Der ABSCHNITT hat diesen Teil mehrdeutig lassen.) Für den farbmetrischen PCS ist eine minimale und maximale Helligkeit angegeben, aber die Werte für Dasin und Farbton liegen ungefähr ± 127. Dieses PCS sieht wie ein rechteckiges Prism aus. Wie bereits erwähnt, ähnelt das perzeptuelle PCS-Volume der Gamut eines Inkjetdruckers.

Die beiden CODEC-PCs verfügen auch über zwei unterschiedliche digitale Codierungen. Im perzeptuellen PCS stellt der Wert 0 (null) eine Helligkeit von 0 (null) dar. Im farbmetrischen PCS stellt der Wert 0 (null) die minimale Helligkeit des PCS dar, die größer als 0 (null) ist. Sie können dieses Problem lösen, indem Sie für jede PCS-Codierung ein anderes Gerätemodell verwenden.

## <a name="gamut-mapping"></a>Gamutzuordnung

Zum Erstellen der AToB-LUTs in einem MAPP-Profil ordnen Sie vom Gerätebereich zum entsprechenden PCS-Bereich zu. Um die BToA-LUTs zu erstellen, ordnen Sie die Zuordnung vom PCS-Bereich zum Gerätebereich zu. Die Zuordnung für die AToB-LUTs ähnelt der Zuordnung in einem maßbasierten CMS. Ordnen Sie für das perzeptuelle PCS die Geräte-Gamut der perzeptuellen PCS-Gamutgrenze zu, indem Sie clipping oder compression für alle Nicht-Gamutfarben verwenden. Für die farbmetrischen Absichten müssen Sie möglicherweise die Helligkeit abschneiden, aber die Werte für Die Färbung und Farbton passen alle in den farbmetrischen PCS-Gamut.

Die Zuordnung für die BToA-LUTs unterscheidet sich etwas. Die farbmetrischen Absichten sind immer noch einfach. Sie clipen einfach PCS-Werte auf die Geräte gamut. Allerdings erfordert das BED, dass alle möglichen PCS-Werte einem Gerätewert zugeordnet werden, nicht nur denen innerhalb der Referenz gamut des perzeptuellen PCS. Daher müssen Sie sicherstellen, dass die GMMs Quellfarben verarbeiten können, die sich außerhalb des Referenzumfangs befinden. Dies kann durch Ausschneiden dieser Farben an der Gamutgrenze des Geräts erfolgen.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Zuordnung von Baselinegerät zu PROFILE-Profilklasse



| Baselinegerätetyp              | PROFILE Profile-Klasse       | Anmerkung                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| RGB-Erfassungsgerät                | Eingabegerät ("scnr")   | PCS ist CIELAB. AToB0Tag ist Gerät zu PCS mit relativ farbmetrischer Absicht. |
| CRT, MONITOR-Monitor                  | Anzeigegerät ("mntr") | PCS ist CIEXYZ. Informationen zur Modellkonvertierung finden Sie im Folgenden.                      |
| RGB-Projektor                     | Farbraum ("Spac")    | PCS ist CIELAB.                                                              |
| RGB- und CMYK-Drucker              | Ausgabegerät ("prtr")  | PCS ist CIELAB.                                                              |
| Rgb Virtual Device (Nicht-HDR-Fall) | Anzeigegerät ("mntr") | PCS ist CIEXYZ.                                                              |
| RGB Virtual Device (HDR-Fall)     | Farbraum ("Spac")    | PCS ist CIELAB.                                                              |



 

Die Konvertierung von Überwachungsprofilen umfasst nicht das Erstellen von LUTs, sondern die Erstellung eines Matrix- oder TRC-Modells. Das in DER CRT verwendete Modell unterscheidet sich geringfügig von dem Modell, das in der WCS CRT- oder LCD-Modellierung verwendet wird, da der Begriff "schwarze Korrektur" fehlt. Sie haben folgende Möglichkeiten:

WCS-Modell: ![Zeigt ein W C S-Modell an.](images/transformcreation-image132.png)

MODELS-Modell: ![Zeigt ein I C C-Modell an.](images/transformcreation-image134.png)

Die Konvertierung vom WCS-Modell in das MODELL ERFOLGT wie folgt.

Definieren neuer Kurven:

![Zeigt eine Matrix zum Definieren neuer Kurven an.](images/transformcreation-image136.png)

Dies sind keine Tonwiedergabekurven, da sie nicht 1 zu 1 zugeordnet werden. Dies wird durch eine Normalisierung erreicht. Die endgültigen Definitionen des MODELLS SIND:

![Zeigt die endgültigen Definitionen des I C C-Modells an.](images/transformcreation-image138.png)

![Zeigt die endgültige Matrix für das I C C-Modell an.](images/transformcreation-image140.png)

Für nicht HDR RGB-virtuelle Geräte generieren Sie auch ein DISPLAY-PROFIL für die Speicherplatzeffizienz. In diesem Fall kann die Tristimulusmatrix *MWS* direkt aus den primären Dateien des WCS-Profils ohne die obige Modellkonvertierung abgerufen werden. Ein letzter, aber wichtiger Hinweis ist, dass diese tristimulus-Matrix mäßig an D50 angepasst werden muss, um der TRIM-Spezifikation des PCS zu entsprechen. Mit anderen Worten: Die Einträge in jeder Zeile der Matrix, die im CAB-Profil codiert werden soll, müssen jeweils mit 96,42, 100 und 82,49 summiert werden. In der aktuellen Implementierung erfolgt die umstellungstische Anpassung durch CAT02, bei der es sich auch um die in CAB02 verwendete transformationtische Anpassung handelt.

## <a name="black-preservation-and-black-generation"></a>Black Preservation und Black Generation

Die Implementierung der schwarzen Beibehaltung ist mit der Generierung des schwarzen Kanals in Geräten verknüpft, die einen schwarzen Kanal unterstützen. Um dies zu erreichen, werden Informationen zu jeder Quellfarbe gesammelt, damit Gerätemodelle, die einen schwarzen Kanal unterstützen, bestimmen können, wie der schwarze Kanal am besten für die Ausgabe festgelegt werden kann. Während die Beibehaltung von Schwarz für Farbtransformationen relevant ist, die zwischen einem Schwarzkanalgerät in ein anderes konvertiert werden, wird die schwarze Generierung für alle Transformationen implementiert, die ein Zielgerät mit schwarzem Kanal betreffen.

Informationen zu schwarzen Kanälen werden in einer Datenstruktur namens [**BlackInformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)aufgezeichnet. Die **BlackInformation-Struktur** enthält einen booleschen Wert, der angibt, ob die Farbe nur ein schwarzes Farbmittel enthält, und einen numerischen Wert, der den Grad der "Blackness" (Schwarzgewicht) angibt. Bei Quellgeräten, die einen schwarzen Kanal unterstützen, entspricht das schwarze Gewicht dem Prozentsatz des schwarzen Farbmittels in der Quellfarbe. Für Quellgeräte, die keinen schwarzen Kanal enthalten, wird die schwarze Gewichtung mithilfe der anderen Farbelemente und des Darstellungswerts berechnet. Ein Wert namens "Farbunterstärkung" wird berechnet, indem die Differenz zwischen dem maximalen Farbwert und dem minimalen Farbwert dividiert durch den maximalen Farbwert verwendet wird. Ein Wert namens "relative Helligkeit" wird berechnet, indem der Unterschied zwischen der Helligkeit der Farbe und der minimalen Helligkeit für das Zielgerät dividiert durch die Differenz zwischen der minimalen und maximalen Helligkeit für das Zielgerät ermittelt wird. Wenn es sich bei dem Quellgerät um ein additives Gerät (Monitor oder Projektor) handelt, wird das schwarze Gewicht als 1,0 abzüglich der Farbunterstärkung multipliziert mit der relativen Helligkeit bestimmt. Wenn das Quellgerät beispielsweise ein RGB-Monitor ist, werden der Höchstwert und der Mindestwert von R, G und B für jede Farbe berechnet, und die schwarze Gewichtung wird durch die Formel bestimmt:

BW = (1,0 – (max(R,G,B) – min(R,G,B)) / max(R, G, B)) \* relative Helligkeit

Wenn das Quellgerät die subtrahtive Farbgebung unterstützt, z. B. einen CMY-Drucker, müssen die einzelnen Farbmittel "ergänzt" (von 1.0 subtrahiert) sein, bevor sie in der obigen Formel verwendet werden. Daher ist für einen CMY-Drucker R = 1,0 – C, G = 1,0 – M und B = 1,0 – Y.

Die schwarzen Informationen für jede Farbe, die von der Farbtransformation verarbeitet wird, werden während des Farbübersetzungsprozesses bestimmt. Die Rein-Schwarz-Informationen werden nur bestimmt, wenn die schwarze Beibehaltung angegeben ist. Die schwarze Gewichtung wird immer bestimmt, wenn das Zielgerätemodell ein schwarzes Farbelement unterstützt. Die schwarzen Informationen werden über die [**ColorimetricToDeviceColorsWithBlack-Methode**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) an das Zielgerätemodell übergeben, die den resultierendenWERT verwendet.

Beachten Sie, dass der oben genannte Prozess aufgrund der Optimierung der Farbtransformation nur während der Erstellung der optimierten Transformierungs-MSI und nicht während der Ausführung der TranslateColors-Methode erfolgt.

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Optimierung für Transformationen mit mehr als drei Quellkanälen

Die Größe der optimierten Transformation wird durch mehrere Faktoren bestimmt: die Anzahl der Farbkanäle auf dem Quellgerät, die Anzahl der Schritte in der Tabelle für jeden Quellfarbkanal und die Anzahl der Farbkanäle auf dem Ausgabegerät. Die Formel zum Bestimmen der Größe der Transformationstabelle lautet wie folgt:

Größe = Anzahl der Schritte pro <sub>Kanalquelle\Gerät(Anzahl\ von\ Kanälen\ in\ Quelle\ Gerät)</sub> x Anzahl der Kanäle auf dem Ausgabegerät

Wie Sie sehen können, wächst die Größe der Tabelle exponentiell, abhängig von der Anzahl der Kanäle auf dem Quellgerät. Viele Quellgeräte unterstützen drei Farbkanäle, z.B. Rot, Grün und Blau. Wenn ein Quellgerät jedoch vier Kanäle unterstützt, z. B. CMYK, werden die Größe der Tabelle und die zum Erstellen der Tabelle erforderliche Zeit um den Faktor der Anzahl der Schritte vergrößert. In einem maßbasierten CMS, in dem Transformationen "im Laufenden" erstellt werden, ist dieses Mal möglicherweise nicht akzeptabel.

Um die Zeit zu reduzieren, die zum Erstellen der Farbkonvertierungstabelle erforderlich ist, ist es möglich, zwei Fakten zu nutzen. Erstens: Während das Quellgerät möglicherweise mehr als drei Farbkanäle unterstützt, verfügt der geräteunabhängige Zwischenfarbraum (CIECAM02 Ja <sub>C</sub> b <sub>C)</sub> nur über drei Farbkanäle. Zweitens ist der zeitaufwändige Teil der Verarbeitung nicht die Gerätemodellierung (Konvertierung von Gerätefarbkoordinaten in Tristimuluswerte), sondern die Gamutzuordnung. Anhand dieser Fakten können Sie eine vorläufige Farbkonvertierungstabelle erstellen, die Farben im geräteunabhängigen Farbraum über die Gamutzuordnungsschritte und schließlich über das Ausgabegerätefarbmodell konvertiert. Die Erstellung dieser Tabelle besteht aus Dimension 3. Anschließend erstellen wir die endgültige Farbkonvertierungstabelle der Dimension 4, indem wir die Quellfarbkombinationen in einen geräteunabhängigen Zwischenraum konvertieren und dann mithilfe der vorläufigen Tabelle für die Farbkonvertierung die Konvertierung in den Ausgabegerätefarbraum abschließen. Daher reduzieren Sie die Anzahl der Gamutzuordnungsberechnungen von <sub>Kanälen</sub> vom Computing (Anzahl der Schritte in der Nachschlagetabelle) auf die Anzahl der Schritte in der Zwischentabelle ₃ Gamutzuordnungsberechnungen. Obwohl Sie die Anzahl der Schritte in der (Nachschlagetabelle) <sub>Number\ of\channels-Berechnungen</sub> der Gerätemodellierung und der dreidimensionalen Tabellensuche ausführen müssen, ist dies immer noch viel schneller als die ursprüngliche Berechnung.

Der vorherige Prozess funktioniert gut, vorausgesetzt, dass keine Informationen zwischen dem Quellgerätemodell und einer anderen Komponente in der Farbtransformation übergeben werden müssen. Wenn das Ausgabegerät und das Quellgerät jedoch beide ein schwarzes Farbmittel unterstützen und das schwarze Quellfarbmittel zum Bestimmen des schwarzen Ausgabefarbmittels verwendet wird, kann der Prozess die Schwarz-Quellinformationen nicht ordnungsgemäß kommunizieren. Ein alternativer Prozess besteht darin, eine vorläufige Farbkonvertierungstabelle zu erstellen, die Farben im geräteunabhängigen Farbraum nur über die gamutbasierten Zuordnungsschritte konvertiert. Erstellen Sie dann die endgültige Farbkonvertierungstabelle der Dimension 4 mithilfe der folgenden Schritte: a) konvertieren Sie die Quellfarbkombinationen in einen geräteunabhängigen Zwischenbereich, b) führen Sie die Gamutzuordnungsschritte durch Interpolation in der vorläufigen Farbtabelle aus, anstatt die tatsächlichen Gamutzuordnungsprozesse anzuwenden, und c) verwenden Sie die resultierenden Werte aus den Gamutzuordnungsschritten und alle Informationen zum schwarzen Quellkanal, um die Farbelemente des Ausgabegeräts mithilfe des Ausgabegerätemodells zu berechnen. Dieser Prozess kann auch verwendet werden, wenn Informationen zwischen dem Quell- und dem Ausgabegerätemodell übertragen werden, auch wenn kein schwarzer Kanal vorhanden ist. Beispielsweise, wenn die beiden Module mit einer Plug-In-Architektur implementiert werden, die den Datenaustausch zwischen Modulen ermöglicht.

Die beiden vorhergehenden Prozesse können verwendet werden, um die Zeit effektiv zu verbessern, die zum Erstellen der vierdimensionalen Farbtransformationstabelle erforderlich ist.

### <a name="checkgamut"></a>CheckGamut

Die ICM aufruft CreateTransform und **CreateMultiProfileTransform** nehmen ein Wort mit Flagwerten an, von denen einer ENABLE \_ GAMUT \_ CHECKING ist. Wenn dieses Flag festgelegt ist, muss CITE die Transformation anders erstellen. Die ersten Schritte sind identisch: Die Quell- und Ziel-CAMs müssen initialisiert werden, dann müssen die Deskriptoren für die Allgemeine Quell- und Zielgrenze initialisiert werden. Unabhängig von der angegebenen Absicht muss CheckGamut GMM verwendet werden. CheckGamut GMM sollte mithilfe der Quell- und Zielgerätemodelle und gamut-Begrenzungsdeskriptoren initialisiert werden. Die Transformation sollte dann jedoch eine abgeschnittene Transformation erstellen, die das Quellgerätemodell, den Quell-CAB, alle dazwischen liegenden GMMs und checkGamut GMM umfasst. Dadurch wird sichergestellt, dass die vom CheckGamut CMM ausgegebenen Delta-J-, Delta C- und Delta h-Werte zu den endgültigen resultierenden Werten werden.

Die Bedeutung von CheckGamut ist klar, wenn nur zwei Geräteprofile in der Transformation vorhanden sind. Wenn mehr als zwei Geräteprofile und mehr als zwei GMMs vorhanden sind, meldet CheckGamut, ob die Farben, die durch das erste Gerätemodell transformiert wurden, und alle bis auf den letzten GMM innerhalb der Gamut des Zielgeräts liegen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende Farbverwaltungskonzepte](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




