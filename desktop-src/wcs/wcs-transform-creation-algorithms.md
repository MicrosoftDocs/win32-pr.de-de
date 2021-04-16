---
title: WCS-Transformationserstellungsalgorithmen
description: WCS-Transformationserstellungsalgorithmen
ms.assetid: 526bbbfc-fb60-415d-b4f0-6a44a5d11a55
keywords:
- Windows Color System (WCS), Transformations Erstellung
- WCS (Windows Color System), Transformations Erstellung
- Bild Farbverwaltung, Transformations Erstellung
- Farbverwaltung, Transformations Erstellung
- Farben, Transformations Erstellung
- Transformations Erstellung
- WCS-Transformations Erstellung
- Algorithmen, Transformations Erstellung
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418596c0e57571f3e504727d4606921d36ff9461
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104569356"
---
# <a name="wcs-transform-creation-algorithms"></a>WCS-Transformationserstellungsalgorithmen

[Erstellung von Transformationen](#creation-of-transforms)

 

[Sequenzielle Transformations Ausführung](#sequential-transform-execution)

 

[Erstellung optimierter Transformationen](#creation-of-optimized-transforms)

 

[Iccprofilefromwcsprofile](#iccprofilefromwcsprofile)

 

[Schwarze Beibehaltung und schwarze Generierung](#black-preservation-and-black-generation)

 

[Überprüfen des Gamut](#checkgamut)

## <a name="creation-of-transforms"></a>Erstellung von Transformationen

Um ordnungsgemäß zu erklären, wie Farb Transformationen funktionieren, ist es hilfreich, den gesamten Verarbeitungs Pfad sowohl über ICM 2,0 als auch über die internale des CTE zu erläutern. Die ICM 2,0-Funktion " [**fiatecolortransformw**](/windows/win32/api/icm/nf-icm-createcolortransformw) " erstellt eine Farb Transformation, die Anwendungen zum Durchführen der Farbverwaltung verwenden können. Diese Funktion erstellt einen Farb Kontext aus den [**logcolorspace**](/windows/desktop/api/Wingdi/ns-wingdi-taglogcolorspacea) -und Intent-Eingaben. Die Intents werden dem Baseline-Farbskala-Zuordnungsalgorithmus zugeordnet, der korreliert. Die-Funktion ruft dann die ICM 2,0-Funktion für die konsistente Farbverarbeitung mit " [**fiatemultiprofiletransform**](/windows/desktop/api/Wingdi/) " auf. Die Funktion " **kreatecolortransform** " kopiert Daten in der Regel in die interne optimierte Transformations Struktur.

Die ICM 2,0-Funktion "fiatemultiprofiletransform" akzeptiert ein Array von Profilen und ein Array von Intents oder ein einzelnes Geräte Verknüpfungs Profil und erstellt eine Farb Transformation, mit der Anwendungen eine Farbzuordnung durchführen können. Diese Eingabe Profile und Intents werden verarbeitet, um Gerätemodelle, Farb Darstellungsmodelle, Beschreibungen der Farbdarstellung und gamingzuordnungsmodelle zu erstellen. Dies geschieht wie folgt:

-   Gerätemodelle werden direkt von DM-Profilen initialisiert. Es wird ein Gerätemodell für jedes Profil im Aufrufen von " [**foratemultiprofiletransform**](/windows/desktop/api/Wingdi/)" erstellt.
-   Farb Darstellungsmodelle werden direkt aus den CAM-Profilen initialisiert. Es gibt ein CAM-Profil für jedes Profil im Aufrufen von " [**foratemultiprofiletransform**](/windows/desktop/api/Wingdi/)". Das gleiche CAM-Profil kann jedoch für mehr als ein Profil angegeben werden.
-   Die Beschreibungen der spielgrenzen werden von einem Gerätemodell Objekt und einem CAM-Objekt initialisiert. Es gibt eine Beschreibung der Beschreibung der einzelnen Profile im Aufrufen von " [**foratemultiprofiletransform**](/windows/desktop/api/Wingdi/)".
-   Farbskala-Mapping-Modelle werden von zwei spielgrenzen und einer Absicht initialisiert. Sie müssen zwischen jedem Paar von Geräte Modellen, die aus dem Aufrufen von " [**foratemultiprofiletransform**](/windows/desktop/api/Wingdi/)" erstellt wurden, ein gamingmodellmapping-Modell erstellen. Dies bedeutet, dass Sie ein weniger gamingzuordnungs Modell als das Gerätemodell verwenden. Da die Anzahl der Intents mit der Anzahl der Gerätemodelle übereinstimmt, gibt es auch eine höhere Absicht als erforderlich. Die erste Absicht in der Liste wird übersprungen. Sie durchlaufen die Liste der Gerätemodelle und Intents und erstellen gamingzuordnungsmodelle. Übernehmen Sie das erste und zweite Gerätemodell und die zweite Absicht, und initialisieren Sie dann das erste Modell für die Farbskala-Zuordnung. Wählen Sie das zweite und dritte Gerätemodell und die dritte Absicht aus, und initialisieren Sie dann das zweite Modell für die Modell Zuordnung. Fahren Sie auf diese Weise fort, bis Sie alle gamingmapping-Modelle erstellt haben.

Wenn die Profile ordnungsgemäß verarbeitet wurden und alle zwischen Objekte erstellt und initialisiert wurden, können Sie die "Zitat Transformation" mit dem folgenden-Befehl erstellen. *Pdestcam* und *pdestdm* sind [**solche, die**](/windows/desktop/api/Wingdi/)mit dem letzten Profil im Aufrufen von "" für "" von "" in "" von "" von ""


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



## <a name="support-for-plug-ins"></a>Unterstützung für Plug-ins

Ein Problem beim Einrichten der Transformations Liste besteht darin, zu überprüfen, ob ein erforderliches Plug-in verfügbar ist. Der folgende Modellwechsel bietet diese Richtlinie, um dieses Verhalten zu steuern. Die Verwaltung dieser Transformations Liste ist eine Methode in der internen optimierten Transformations Struktur, aber jede Modell Methode stellt den Zeiger auf sich selbst und einen eigenen Satz von Parameterwerten bereit.

Der Modus muss einer der folgenden sein.

-   Tfmrobust: Wenn ein Mess Profil ein bevorzugtes Plug-in angibt und das Plug-in nicht verfügbar ist, verwendet das neue CTE-System das Baseline-Plug-in. Wenn keines der Plug-Ins verfügbar ist, meldet die Transformation einen Fehler.
-   Tfmstrict: Wenn ColorContext ein bevorzugtes Plug-in angibt, muss das Plug-in verfügbar sein. Wenn kein bevorzugtes Plug-in gefunden wird, wird das Baseline-Plug-in verwendet. Wenn keines der Plug-Ins verfügbar ist, meldet die Transformation einen Fehler.
-   Tfmbaseline: in addmessrementstep können nur Baseline-Plug-ins verwendet werden. Wenn ColorContext ein bevorzugtes Plug-in angibt, wird das Plug-in ignoriert. Wenn das Baseline-Plug-in nicht verfügbar ist, meldet die Transformation einen Fehler.

## <a name="transform-execution"></a>Transformations Ausführung

Die ICM 2,0 API [**translatecolors**](/windows/win32/api/icm/nf-icm-translatecolors) -Funktion übersetzt ein Array von Farben aus dem [Quellfarbraum](c.md) in den Ziel Farbraum, wie durch eine Farb Transformation definiert. Diese Funktion überprüft intern eine Reihe von zwischengespeicherten Farben, um eine sofortige Übereinstimmung der häufig transformierten Farben zu ermöglichen. Diese Transformation unterstützt 8-Bit-pro-Kanal-Byte Arrays und 32-Bit-pro-Kanal-float-Arrays. Alle anderen Formate werden vor der Übergabe an den neuen CTE konvertiert.

Die ICM 2,0 API [**translatebitmapbits**](/windows/win32/api/icm/nf-icm-translatebitmapbits) -Funktion übersetzt die Farben einer Bitmap mit einem definierten Format, um eine andere Bitmap in einem angeforderten Format zu entwickeln. Diese Funktion überprüft intern eine Reihe von zwischengespeicherten Farben, um eine sofortige Übereinstimmung der häufig transformierten Farben zu ermöglichen. Um zu viele Codepfade, Unterstützung und testkomplexität zu vermeiden, wird nur eine begrenzte Anzahl von Bitmapformaten in der Transformations-und Interpolations-Engine unterstützt. Diese Funktion muss die nicht systemeigenen, eingehenden und ausgehenden Bitmapformate in nativ unterstützte Formate für die Verarbeitung übersetzen. Diese Transformation unterstützt nur 8-Bit-pro-Kanal-Byte-Bitmaps und 32-Bit pro Kanal Gleit Komma-Bitmaps. Alle anderen Formate werden vor der Übergabe an den neuen CTE konvertiert.

 

### <a name="sequential-transform-execution"></a>Sequenzielle Transformations Ausführung

Wenn für den *dwFlags* -Parameter das sequentielle \_ Transform-Bit festgelegt ist, wenn die ICM-Funktionen " [**samatecolortransformw**](/windows/win32/api/icm/nf-icm-createcolortransformw) " oder " **featemultiprofiletransform** " aufgerufen werden, werden die Transformationsschritte nacheinander ausgeführt. Dies bedeutet, dass der Code die einzelnen Gerätemodelle, das Farb Darstellungs Modell und das gamingzuordnungsmodell separat durchläuft, wie durch den Befehl " **foratecolortransform** " oder " **foratemultiprofiletransform** " angegeben. Dies ist möglicherweise hilfreich beim Debuggen von Plug-in-Modulen, aber es ist viel langsamer als die Ausführung durch eine optimierte Transformation. Die Ausführung im sequenziellen Modus ist daher für Produktionssoftware nicht empfehlenswert. Außerdem gibt es möglicherweise geringfügige Unterschiede in den Ergebnissen, die im sequenziellen Modus und im optimierten Modus erzielt werden. Dies ist auf Variationen zurückzuführen, die bei der Verkettung der Funktionen eingeführt werden.

### <a name="creation-of-optimized-transforms"></a>Erstellung optimierter Transformationen

Eine optimierte Transformation ist eine mehrdimensionale Such Tabelle. Die Tabelle kann von einer mehrdimensionalen Interpolations-Engine verarbeitet werden, z. b. von der "tetrahedral"-Interpolations-Engine, die die Eingabe Farben auf die Transformation anwendet. Im folgenden Abschnitt wird beschrieben, wie die optimierten Nachschlage Tabellen erstellt werden. Der Abschnitt after, der beschreibt, wie in den optimierten Nachschlage Tabellen interpolieren wird.

## <a name="sparse-lookup-tables"></a>Lookuptabellen mit geringer Dichte

Herkömmliche Drucker verfügen über CMYK-Farben. Um das Spiel zu erweitern, besteht ein Ansatz darin, dem System neue Farben hinzuzufügen. Die Farben, die in der Regel hinzugefügt werden, sind Farben, die von CMYK-Inks Gängige Optionen sind orange, grün, rot, blau usw. Um die "offensichtliche Auflösung" zu erhöhen, können Farben mit unterschiedlichen tints verwendet werden, z. b. Light Cyan, Light Magenta usw. Tatsächlich weist das Druckergerät mehr als vier Kanäle auf.

Obwohl es sich bei Druckern um Ausgabegeräte handelt, wird auch die Farbkonvertierung des geräteraums in einen anderen Farbraum durchgeführt. Bei einem CMYK-Drucker wäre dies eine Transformation von CMYK zu XYZ oder das "Forward-Modell" des Druckers. Durch die Kombination des vorwärts Modells mit anderen Transformationen ist es möglich, einen CMYK-Druck auf einem anderen Gerät zu emulieren. Beispielsweise würde ein Drucker CMYK auf einen Monitor RGB einen Nachweis Mechanismus ermöglichen, der einen Abdruck dieses CMYK-Druckers auf einem Monitor emuliert. Ebenso gilt das gleiche auch für Hi-Fi-Drucker. Eine Konvertierung von CMYKOG zu RGB ermöglicht das Nachweis des CMYKOG-Druckers auf einem Monitor.

Der konventionelle Ansatz für die Implementierung einer solchen Farbkonvertierung ist die Verwendung eines einheitlichen LUT. Beispielsweise ist in einem-ICC-Profil für einen CMYKOG-Drucker die Bezeichnung "ICC" ein A2B1-Tag, das eine einheitliche schstich Probe im CMYKOG-Gerätebereich des Forward-Modells darstellt, das aus CMYKOG in den Verbindungsbereich des ICC-Profils (CIELAB oder CIEXYZ) übergeht. Das agentgeräterink-Profil ermöglicht eine direkte Transformation vom CMYKOG-Geräte Speicherplatz in einen beliebigen Farbraum, einschließlich eines geräteraums, auch in Form eines in der CMYKOG-Speicherplatz Stichproben gleichmäßig. Die Stichprobenentnahme erfolgt nie mit 256 Ebenen (Bit-Tiefe 8) aufgrund der großen Schachtelungs Ergebnisse, außer im Fall von Mono-Geräten (1 Kanal). Stattdessen wird die Stichprobenentnahme mit niedrigerer Bittiefe verwendet. Einige typische Optionen sind 9 (Bittiefe 3), 17 (Bittiefe 4), 33 (Bittiefe 5). Wenn die Anzahl der Ebenen kleiner als 256 in jedem Kanal ist, wird der LUT in Verbindung mit einem Interpolations Algorithmus verwendet, um das Ergebnis zu schaffen, wenn eine Ebene zwischen zwei samplingebenen liegt.

Obwohl ein einheitlicher LUT konzeptionell einfach zu implementieren ist und Interpolationen auf einem einheitlichen LUT in der Regel effizient sind, erhöht sich die LUT-Größe exponentiell mit der Eingabe Dimension. Tatsächlich zeigt die Anzahl  von Knoten im Kanal die  ![ Variable für die Anzahl von Knoten in einem LUT an, wenn d die Anzahl der in der Uniform LUT verwendeten Schritte und n die Anzahl der Kanäle im Quell Farbraum ist. ](images/transformcreation-image002.gif) Die Anzahl der Knoten erfordert in der Zwischenzeit schnell so viel Speicherplatz im Arbeitsspeicher, dass auch bei der Verarbeitung der Anforderung durch die neuesten Computersysteme Schwierigkeiten auftreten. Bei Geräten mit sechs oder acht Kanälen erfordert die Implementierung des Geräte Profils in der Anwendung einige Schritte in der LUT, manchmal sogar bis zu fünf Schritte in der A2B1-Tabelle, um das Profil innerhalb von Megabyte anstelle von Gigabyte beizubehalten. Die Verwendung einer kleineren Anzahl von Schritten erhöht den Interpolations Fehler, da jetzt weniger Beispiele vorhanden sind. Da der Kanal einheitlich sein muss, wird die Genauigkeit für den gesamten Farbraum auch in den Bereichen des Raums beeinträchtigt, in denen ein signifikanter Farbunterschied durch eine kleine Änderung des Geräte Werts verursacht werden kann.

Bei Geräten mit mehr als vier Colorants sind bestimmte Teilbereiche des gesamten geräteraums wichtiger als andere. Beispielsweise werden im Bereich "CMYKOG" Zyan-und grüne Farben selten verwendet, da sich ihre Schattierungen größtenteils einander überlappen. Ebenso überlappend sich gelbe und orangefarbene Farben größtenteils einander. Eine einheitliche Reduzierung der Anzahl von Schritten kann als allgemeine Herabstufung der Qualität im gesamten Farbraum angezeigt werden. Dies ist etwas, das Sie für die unwahrscheinlichen Freihand-Kombinationen, aber nicht für die wahrscheinlichen oder wichtigen Kombinationen leisten können.

Während ein einheitlich erfasste LUT einfach und effizient für Interpolationen ist, erzwingt er bei zunehmender Dimensions Steigerung sehr hohe Speicheranforderungen. Während ein Gerät in der Praxis über sechs oder acht Kanäle verfügen kann, werden Sie selten gleichzeitig verwendet. In den meisten Fällen enthält die Transformation für die Eingabe Farben zu Farben nur einige "aktive" Colorants und befindet sich daher in einem unteren dimensionalen Farbraum. Dies bedeutet auch, dass Interpolationen effizienter in diesem unteren dimensionalen Bereich durchgeführt werden können, da die interpolung schneller ist, wenn die Dimension niedriger ist.

Daher besteht der Ansatz darin, den gesamten Gerätebereich in Teilbereiche verschiedener Dimensionen zu überarbeiten. Und da niedrigere Dimensionen (solche, die drei oder vier Colorants kombinieren) wichtiger sind, können Sie durch das Durchlaufen des Raums auch andere Stichproben Raten anwenden. Das heißt, es gibt eine andere Anzahl von Schritten für die Teile. Erhöhen der Stichproben Raten für niedrigere Dimensionen, wodurch Sie für höhere Dimensionen reduziert werden.

Zum Beheben von Notationen ist *n* die Anzahl der Kanäle im Quell Farbraum der Farb Transformation, die Sie testen möchten. Sie können auch auf *n* als Eingabe Dimension verweisen und ![ zeigt n größer oder gleich 5 an.](images/transformcreation-image004.gif) , sofern nicht anders angegeben.

Die Grundbausteine sind LUTs verschiedener Eingabe *Dimensionen* und-Größen, anstelle eines einheitlichen LUT mit der Eingabe Dimension *n*. Um präziser zu sein, ist ein *LUT* ein rechteckiges Gitter, das für einen Einheiten Cube vorgeschrieben ist. Das heißt, alle Geräte Koordinaten werden in den Bereich \[ 0, 1) normalisiert \] . Wenn die Eingabe Dimension des LUT ist (Beachten Sie, dass nicht gleich *n* sein muss, obwohl ![ V kleiner oder gleich n zeigt.](images/transformcreation-image006.gif) ist erforderlich), dann besteht eine eindimensionale eindimensionale Stichprobenentnahme:

SAMP *i*: ![ zeigt ein eindimensionales Stichproben Raster an.](images/transformcreation-image008.gif)

Wenn alle *x-<sub>j</sub>s* im Bereich von \[ 0, 1 liegen müssen \] , wird ![ ein hoch gestellt d (i) angezeigt.](images/transformcreation-image010.gif) Gibt die Anzahl der Schritte für die Stichprobenentnahme des *i* -Kanals an, die mindestens 1 betragen muss, und ![ zeigt ein spuperscript von X (Index) d (i) an.](images/transformcreation-image012.gif) muss 1 sein. Dagegen ![ zeigt ein hoch gestellt X (Index 1) an.](images/transformcreation-image014.gif) muss nicht 0 sein.

Es werden nur die folgenden beiden speziellen Fälle von LUT definiert.

*Closed LUT*: Dies ist eine Meldung mit der zusätzlichen Anforderung, dass für jedes SAMP *<sub>i</sub>* ![ ein hoch gestellt X (Index 1) mit dem Wert "0" angezeigt wird.](images/transformcreation-image016.gif) , und ![ zeigt ein hoch gestellt d (i) größer oder gleich 2 an.](images/transformcreation-image018.gif) . Bei einem einheitlichen, geschlossenen LUT handelt es sich um einen geschlossenen LUT, der das gleiche ![ zeigt wie ein hoch gestellt d (i).](images/transformcreation-image010.gif) für jeden Kanal sind und die Knoten gleichmäßig zwischen 0 und 1.

*Öffnen von LUT*: Dies ist ein LUT mit der zusätzlichen Anforderung, dass für jedes SAMP *i* ![ ein hoch gestellt X (Index 1) größer als 0 (null) anzeigt.](images/transformcreation-image020.gif) . Es ist in Ordnung, ![ ein hoch gestellt d (i) gleich 1 zu sehen.](images/transformcreation-image022.gif) .

Ziel ist es, den Unit-Cube \[ 0, 1 \] *n* in eine Auflistung von geschlossenen LUTs und geöffneten LUTs zu stratifizieren, sodass die gesamte Sammlung den Einheiten Cube abdeckt. Es ist konzeptionell einfacher, diese "LUT-Schichten" nach ihren Dimensionen zu organisieren, damit auf der obersten Ebene:

![Zeigt die oberste Ebene zum Organisieren von L U T-Schichten anhand ihrer Dimensionen an.](images/transformcreation-image024.png)

dabei ![ zeigt Sigma den abonniert k.](images/transformcreation-image026.gif) ist die "*k* -dimensionale Schichten Auflistung". Beachten Sie, dass die Schichten Dimension von 3 anstelle von 0 beginnt. Das heißt, Punkte, da die interpolung von drei farbigen Kombinationen ohne zu viel Arbeitsspeicher Anforderung verarbeitet werden kann.

## <a name="description-of-the-lut-strata"></a>Beschreibung der LUT-Schichten

In dieser Implementierung:

1. ![Zeigt Sigma-Index 3 an.](images/transformcreation-image028.gif) besteht aus geschlossenen LUTs mit drei Eingaben, eine aus jeder möglichen Kombination aus drei Colorants, die aus den *n* Colorants ausgewählt wurden.

2. ![Zeigt Sigma-Index 4.](images/transformcreation-image030.gif) besteht aus einem geschlossenen LUT für die Kombination aus CMYK (oder die ersten vier Colorants), zusammen mit ![Zeigt (n über 4) minus 1 an.](images/transformcreation-image032.png) Öffnen Sie LUTs für alle anderen vierfarbigen Kombinationen. Wenn Sie die Kombination aus CMYK auslagern, bestätigen Sie, dass es sich um eine wichtige Kombination handelt.

3. Für ![ zeigt k gleich 5,..., n an.](images/transformcreation-image034.gif) , ![ Zeigt Sigma (abonniert k).](images/transformcreation-image026.gif) besteht aus ![ anzeigen (n over k).](images/transformcreation-image037.gif) Öffnen Sie LUTs, eine für jede mögliche Kombination aus der Auswahl von *k* Colorants aus der Gesamtzahl von *n* Colorants.

Es bleibt bestehen, die Größen der LUTs anzugeben. Der Hauptunterschied zwischen offenen und geschlossenen LUTs besteht darin, dass sich öffnende LUTs nicht überlappen und dass sich geschlossene LUTs an den Begrenzungs Flächen überlappen können. Die Tatsache, dass die eindimensionale Stichprobe in einem geöffneten LUT nicht 0 (null) enthält, bedeutet im Wesentlichen, dass in einem geöffneten LUT die Hälfte der Begrenzungs Flächen fehlt, sodass der Name "Open" lautet. Wenn sich zwei LUTs nicht überlappen, können Sie eine andere Anzahl von Schritten oder Knoten Positionen in jedem Kanal verwenden. Dies trifft nicht zu, wenn sich zwei LUTs überschneiden. Wenn in diesem Fall die Anzahl der Schritte oder die Knoten Speicherorte unterschiedlich sind, erhält ein Punkt, der in der Schnittmenge der beiden LUTs liegt, einen anderen Interpolations Wert, je nachdem, welcher LUT in der Interpolations Zeit verwendet wird. Eine einfache Lösung für dieses Problem besteht darin, eine einheitliche Stichprobe mit der gleichen Anzahl von Schritten zu verwenden, wenn sich zwei LUTs überschneiden. Anders gesagt:

Alle geschlossenen LUTs (alle drei farbigen LUTs und der CMYK-LUT in dieser Implementierung) müssen einheitlich sein und über die gleiche Anzahl von Schritten verfügen, die als *d* bezeichnet werden.

Die folgenden beiden Algorithmen können verwendet werden, um die Anzahl der Schritte *d* für geschlossene LUTs und die Anzahl von Schritten für geöffnete LUTs zu bestimmen.

## <a name="algorithm-1"></a>Algorithmus \# 1

Dieser Algorithmus erfordert keine externe Eingabe.

Alle geschlossenen LUTs sind gleichmäßig mit der *d-* Anzahl von Schritten.

Alle geöffneten LUTs der Dimension *k* haben die gleiche Anzahl von Schritten, ![ d (k).](images/transformcreation-image039.gif) in jedem Eingabe Kanal und die Knoten sind gleichmäßig verteilt. Das heißt, für jede ![ zeigt, dass ich gleich 1, 2,..., k ist.](images/transformcreation-image041.gif) .

SAMP *i*: ![ zeigt den SAMP i-Algorithmus an.](images/transformcreation-image043.png)

Geben Sie schließlich *d* und *d* (*k* ) in der folgenden Tabelle 1 an. Die drei Modi "Nachweis", "Normal" und "am besten" sind die ICM 2,0 Quality-Einstellungen. In dieser Implementierung hat der Nachweis Modus den kleinsten Speicherbedarf, und der beste Modus hat den größten Speicherbedarf.

Zum Implementieren dieses Algorithmus muss der folgende Algorithmus 2 aufgerufen werden \# . Benutzer können Ihre eigenen Stichproben Speicherorte angeben, indem Sie die Tabellen als Leitfaden verwenden.

## <a name="algorithm-2"></a>Algorithmus \# 2

Dieser Algorithmus erfordert eine externe Eingabe in Form einer Liste von "wichtigen" Sampling-Speicherorten, aber er ist adaptiver und kann möglicherweise Speicherplatz einsparen.

Die erforderliche Eingabe ist ein Array von Geräte Werten, die vom Benutzer angegeben werden. Diese Geräte Werte geben an, welche Region des Geräte Farbraum wichtig ist. Das heißt, für welchen Bereich sollten mehr Stichproben erstellt werden.

Alle geschlossenen LUTs sind mit der *d-* Anzahl von Schritten einheitlich, wie in Algorithmus \# 1 beschrieben. Die Werte für *d* sind in Tabelle 1 angegeben.

*(a) Uniform Closed-LUT*



|         | Nachweis Modus | Normaler Modus | Bester Modus |
|---------|------------|-------------|-----------|
| ***d*** | 9          | 17          | 33        |



 

*(b) Öffnen von LUT*



| Eingabe Dimension | Nachweis Modus | Normaler Modus | Bester Modus |
|-----------------|------------|-------------|-----------|
| 4               | 5          | 7           | 9         |
| 5               | 2          | 3           | 3         |
| 6               | 2          | 3           | 3         |
| 7               | 2          | 2           | 2         |
| 8 oder mehr       | 2          | 2           | 2         |



 

**Tabelle 1:** Im Algorithmus verwendete LUT-Größen

Jeder geöffnete LUT kann eine andere Anzahl von Schritten in jedem Eingabe Kanal aufweisen, und die Stichproben Speicherorte müssen nicht gleichmäßig verteilt werden. Für einen angegebenen geöffneten LUT-Stratum gibt es eine zugehörige Colorant-Kombination, z ![ . b. zeigt c-Index 1,..., c-Index-k.](images/transformcreation-image045.gif) , wobei das ![ C-Index i anzeigt.](images/transformcreation-image047.gif) s sind unterschiedliche ganze Zahlen zwischen 1 und *n*. Dabei handelt es sich um die Kanal Indizes, die den "aktiven" Colorants in dieser Schicht entsprechen.

Schritt 1: Filtern Sie das in dieser Schicht enthaltene Array mit den Geräte Werten heraus. Ein Geräte Wert zeigt den x-Index Index ![ 1, x, Index 2,..., x-Index.](images/transformcreation-image049.gif) ist in den Schichten enthalten, und zwar nur, wenn ![ eine Gruppe von Werten für einen Kanal anzeigt.](images/transformcreation-image051.gif) und alle anderen Kanäle sind 0. Wenn der gefilterte Satz *N* Einträge enthält, lassen Sie

![Zeigt eine Gleichung an, die verwendet werden soll, wenn der gefilterte Satz N Einträge aufweist.](images/transformcreation-image053.png)

Für jede ![Zeigt an, dass ich gleich 1, 2,..., k ist.](images/transformcreation-image041.gif) iterieren Sie die folgenden Schritte 2-5:

Schritt 2: gibt ![ an, dass d Index (k) gleich 1 zeigt.](images/transformcreation-image055.gif) , SAMP *i* hat nur einen Punkt, der 1,0 sein muss. Fahren Sie mit dem nächsten *i* fort. Andernfalls fahren Sie mit Schritt 3 fort.

Schritt 3: Sortieren der gefilterten Beispiele in aufsteigender Reihenfolge im ![Zeigt C-Index i an.](images/transformcreation-image047.gif) channel.

Schritt 4: Definieren des "vorläufigen" Stichproben Rasters mithilfe der Knoten

![Zeigt die Knoten an, die zum Definieren des "vorläufigen" Stichproben Rasters verwendet werden.](images/transformcreation-image057.png)

where ![Zeigt j gleich 1, 2,..., d abonniert vorläufig (k).](images/transformcreation-image059.gif) .

Schritt 5: regularisieren Sie das vorläufige Raster, um sicherzustellen, dass es mit Strict Monotonie konform ist und dass es mit 1,0 endet. Da das Array bereits sortiert ist, sind die Knoten im vorläufigen Raster bereits monoton und nicht absteigend. Angrenzende Knoten sind jedoch möglicherweise identisch. Sie können dieses Problem beheben, indem Sie bei Bedarf identische Knoten entfernen. Ersetzen Sie schließlich nach diesem Verfahren, wenn der Endpunkt kleiner als 1,0 ist, ihn durch 1,0.

Beachten Sie, dass Schritt 5 der Grund dafür ist, dass die LUT-Schichten in jedem Kanal eine unterschiedliche Anzahl von Schritten aufweisen können. Nach der Regularisierung ist die Anzahl der Schritte in einem Kanal möglicherweise kleiner als ![Zeigt d-Abonnement (k).](images/transformcreation-image061.gif) .

## <a name="interpolation"></a>Interpolation

Sie können die Stratifizierung des Einheiten Cubes durch Öffnen von LUT Schichten und geschlossenen LUT-Schichten erstellen. Führen Sie die folgenden Schritte aus, um Interpolationen mit der "sparseslut-Struktur" auszuführen. Angenommen, ein angegebener Eingabegeräte Wert ![Zeigt (x Index 1, x Index 2,..., x-Index Index n) an.](images/transformcreation-image049.gif) .

Schritt 1: Ermitteln der Anzahl aktiver Kanäle Dies ist die Anzahl der Kanäle, die nicht NULL sind. Dadurch wird die Schichten Dimension *k* für die Suche nach dem enthaltenden Stratum bestimmt. Genauer ist, dass die Schichten Dimension 3 ist, wenn die Anzahl aktiver Kanäle ![ kleiner als oder gleich 3 angezeigt wird.](images/transformcreation-image063.gif) , andernfalls ist die Schichten Dimension mit der Anzahl der aktiven Kanäle identisch.

Schritt 2: innerhalb von ![Zeigt die von Sigma abonniert k.](images/transformcreation-image026.gif) Suchen Sie nach dem enthaltenden Stratum. Ein Geräte Wert ist in einer offenen strateration enthalten, wenn alle Kanäle, die dem stratin entsprechen, einen Wert ungleich 0 (null) aufweisen und alle anderen Kanäle NULL sind. Ein Geräte Wert ist in einer geschlossenen strateration enthalten, wenn jeder Kanal, der nicht durch die Stratum repräsentiert wird, 0 (null) ist. Wenn kein enthaltenes Schema gefunden wird, gibt es eine Fehlerbedingung. Abbrechen und Fehler melden. Wenn eine enthaltende Stratum gefunden wird, fahren Sie mit dem nächsten Schritt fort.

Schritt 3: Wenn die enthaltende Stratum geschlossen ist, kann die interpolung innerhalb des stratums von jedem bekannten Interpolations Algorithmus durchgeführt werden. In dieser Implementierung ist die Auswahl des Algorithmus "tetrahedral Interpolations". Wenn die enthaltende Stratum geöffnet ist und der Geräte Wert streng innerhalb des stratums liegt, d. h.

![Zeigt an, dass der X-Index größer als oder gleich... ](images/transformcreation-image065.gif) Erster Knoten im *i* . Channel

Wenn *ich* ein channelindex für den Stratum bin, funktioniert der Standard Interpolations Algorithmus, wie z. b. die "tetrahedral interpoleration".

Wenn ![ für einige i den Eintrag X Index i less than... ](images/transformcreation-image067.gif) First Node in *i* Th Channel anzeigt, fällt der Wert des Geräts zwischen dem Stratum und den unteren dimensionalen Teilbereichen in die "Lücke". Dieser Moi beschäftigt sich nicht mit einem Interpolations Algorithmus pro SE. Daher kann jeder Interpolations Algorithmus verwendet werden, um in dieser "Lücke" zu interpolieren, obwohl der bevorzugte Algorithmus die folgende transaktionsinterpolung ist.

Die Architektur des Interpolations Moduls wird in den beiden Teilen von Abbildung 1 veranschaulicht.

![Diagramm, das einen Teil der Interpolations Modul Architektur anzeigt.](images/transformcreation-image068.png)

![Diagramm, das den Teil 2 der Interpolations Modul Architektur anzeigt.](images/transformcreation-image070.png)

**Abbildung 1:** Architektur des intepolationmoduls

Wie bereits erwähnt, kann dieser Algorithmus eine ziemlich Dichte Stichprobenentnahme in den Bereichen des geräteraums erzielen, die eine wichtige Kombination von Colorants enthalten, während gleichzeitig die Gesamtgröße der benötigten LUTs minimiert wird. Die folgende Tabelle zeigt einen Vergleich der Anzahl der Knoten, die für die Sparse-Implementierung mit geringer Dichte (mit Algorithmus \# 1 und Normalmodus) und der entsprechenden Uniform LUT-Implementierung erforderlich sind.



| **Anzahl der Eingabe Kanäle** | **Sparseslut** | **Einheitlicher LUT** |
|------------------------------|----------------|-----------------|
| 5                            | 142498         | 1419857         |
| 6                            | 217582         | 24137567        |
| 7                            | 347444         | 410338673       |
| 8                            | 559618         | 6975757441      |



 

## <a name="interpolation-within-a-unit-cube"></a>Interpolations innerhalb eines Einheiten Cubes

Ein grundlegender Schritt im Fall eines rechteckigen Rasters ist die interpolung in einer einschließenden Zelle. Bei einem Eingabe Punkt können Sie die einschließende Zelle problemlos bestimmen. In einem rechteckigen Raster wird der Ausgabewert an jedem der Vertices (Eckpunkte) der einschließenden Zelle angegeben. Sie sind auch die einzigen begrenzungsbedingungen (BCS), die ein interpolant erfüllen muss: der interpolant muss alle diese Punkte passieren. Beachten Sie, dass sich diese begrenzungsbedingungen auf "diskrete" Punkte (in diesem Fall die 2N-Eckpunkte der Zelle) befinden, wobei n die Dimension des Farbraums ist.

Es ist hilfreich, das Konzept der begrenzungsbedingungen zu formalisieren, bevor Sie fortfahren. Für alle Teilmengen der Grenze der einschließenden Zelle (der Einheiten Cube in n Dimensionen) ist eine Begrenzungs Bedingung für S eine Spezifikation der Funktion "BC: S → RM", wobei "m" die Ausgabe Dimension ist. Mit anderen Worten: ein interpolant, der möglicherweise als "interp: \[ 0, 1 \] n → RM" bezeichnet wird, muss Folgendes erfüllen: interp (x) = BC (x) für alle x in S.

Im Standardszenario der interpolung des Einheiten Cubes ist S der Satz diskreter Punkte, bei denen es sich um die 2N-Vertices des Cubes handelt.

Sie können nun die begrenzungsbedingungen verallgemeinern, um die zuvor beschriebenen Probleme zu beheben und einen neuen Interpolations Algorithmus innerhalb des Einheiten Cubes bereitzustellen. Anstatt nur diskrete Begrenzungs Punkte zuzulassen, können begrenzungsbedingungen an eine ganzzahlige Grenze des Cubes erhoben werden. Die genauen Annahmen lauten wie folgt:

(a) der Punkt VN = (1, 1,..., 1) ist ein besonderes Zeichen, und nur eine diskrete Begrenzungs Bedingung ist zulässig. Anders ausgedrückt: Es können keine kontinuierlichen begrenzungsbedingungen an der n-Grenze mit XI = 1 (i = 1,..., n) erzwungen werden.

(b) für jede der verbleibenden n-Begrenzungen mit dem Wert XI = 0 (i = 1,..., n) kann eine Begrenzungs Bedingung auf der ganzen Seite festgelegt werden. dabei ist der Kompatibilitäts Zustand, dass sich zwei Gesichter überschneiden, die Grenzbedingungen der Flächen sollten der Schnittmenge zustimmen.

(c) alle Scheitel Punkte, die nicht in den Gesichtern mit begrenzungsbedingungen enthalten sind, weisen eine einzelne (diskrete) Begrenzungs Bedingung auf.

Sie können auf eine diskrete Begrenzungs Bedingung als endliche Daten und eine fortlaufende Begrenzungs Bedingung als Transaktionsdaten in der Erörterung der Interpolationen mit begrenzten und Transaktionsdaten verweisen.

Überprüfen Sie zunächst die standardmäßige "tetrahedral"-interpolung (z. b., die im Patent von Sakamoto verwendet wird), mit der die Notationen für diese spezielle Formulierung des Problems festgelegt werden Es ist bekannt, dass der Einheits Cube \[ 0, 1 \] n in n unterteilt werden kann. "tetrahedra", parametrisiert durch den Satz von Permutationen für n-Symbole. Genauer gesagt, wird jeder derartige Tetrahedron durch Ungleichheiten definiert.

![Zeigt die Formel für die inequalites der Tetrahedrons an.](images/transformcreation-image073.gif)

WHERE: {1, 2,.., n} → {1, 2,..., n} ist eine permutations der Symbole 1, 2,..., n, d. h., es handelt sich um eine bijective Zuordnung des Satzes von n Symbolen. Wenn z. b. "n = 3" und "= (3, 2, 1)", d. h. "(1) = 3, (2) = 2,... = 1", verwendet wird, wird der zugehörige "Tetrahedron" durch z bis y für x definiert, wobei die allgemeine Notation x, y, z für x1, x2 Beachten Sie, dass diese Tetrahedrons nicht voneinander getrennt sind. Für den Zweck der interpolung haben Punkte, die auf einer gemeinsamen Oberfläche von zwei unterschiedlichen hashhedrons liegen, denselben Interpolations Wert, unabhängig davon, welcher Tetrahedron in der Interpolations Funktion verwendet wird. Im Standardszenario der interinterpolation auf Endpunkten wird für einen bestimmten Eingabe Punkt (x1,..., Xn) zuerst festgelegt, in welchem Tetrahedron der Wert liegt oder gleichwertig mit der entsprechenden permutations übereinstimmt. Anschließend wird der tetrahedral-interpolant als

![Zeigt die Gleichung an, die den tetrahedral-interpolant definiert.](images/transformcreation-image075.png)

where ![Zeigt die Gleichung für die Standard-Basis Vektoren an.](images/transformcreation-image077.png) für i = 1,..., n und E1,..., sind en die Standard-Basis Vektoren. Bevor Sie mit der Generalisierung fortfahren, beachten Sie, dass v0, v1,..., VN die Scheitel Punkte des Tetrahedron sind, und ![Zeigt die Bar-zentrierten Koordinaten an.](images/transformcreation-image079.png) sind die "baryzentrierte Koordinaten".

Für den allgemeinen Fall von BCS auf Begrenzungs Flächen können Sie das Konzept der baryzentrischen Projektion verwenden. Legen Sie wie zuvor für einen gegebenen Eingabe Punkt (x1,..., Xn) zuerst fest, in welchem Tetrahedron er liegt, oder gleichwertig die entsprechende permutations. Führen Sie dann wie folgt eine Reihe von baryzentrischen Projektionen aus. Die erste Projektion ![Zeigt bproj Index 1 (x).](images/transformcreation-image081.gif) sendet den Punkt an die Ebene. ![Zeigt das X-Index Index (1) gleich 0 (null) an.](images/transformcreation-image083.gif) anderes ![Zeigt X gleich V Index n an.](images/transformcreation-image085.gif) in diesem Fall wird Sie nicht geändert. Die genaue Definition der Map bproj wird wie folgt definiert:

![Zeigt die Gleichung für die genaue Definition der Map bproj an.](images/transformcreation-image087.png)

durch ![Zeigt die Gleichung für P-Index k an.](images/transformcreation-image089.png) und k = 1, 2,..., n.

Im Fall ![Zeigt an, dass X gleich V Index n ist.](images/transformcreation-image085.gif) können Sie den Vorgang abbrechen, da der BC-Vorgang bei der VN-Annahme (a) definiert ist. Im Fall ![Zeigt an, dass X nicht gleich V Index n ist.](images/transformcreation-image091.gif) , es ist klar, dass ![Zeigt bproj Index 1 (X).](images/transformcreation-image081.gif) Gibt an, dass die Komponente (1) der Komponente vernichtet wird. Anders ausgedrückt: Es befindet sich in einem der Grenzflächen. Entweder befindet es sich auf einem Gesicht, auf dem BC definiert ist. in diesem Fall können Sie den Vorgang abbrechen, oder Sie führen eine andere barzentrierte Projektion aus. ![Zeigt bproj Index 2 (X ') an.](images/transformcreation-image093.gif) where ![Zeigt x ' ist gleich ' bproj Index 1 (x) ' an.](images/transformcreation-image095.gif) . Und wenn ![Zeigt X ' ' = bproj Index 1 (X ') an.](images/transformcreation-image097.gif) Wenn Sie sich auf einem Gesicht befinden, auf dem BC definiert ist, können Sie den Vorgang abbrechen. andernfalls eine weitere Projektion ausführen ![Zeigt bproj Index 3 (X ' ') an.](images/transformcreation-image099.gif) . Da jede Projektion eine Komponente vernichtet, wird die effektive Dimension verringert, damit Sie wissen, dass der Prozess letztendlich beendet werden muss. Im ungünstigsten Fall führen Sie n Projektionen bis zu Dimension 0 aus, d. h. Scheitel Punkte im Cube, die der Annahme (c) entsprechen und für die Sie wissen, dass BC definiert wird.

Vorausgesetzt, dass K Projektionen ausgeführt wurden, mit

![Zeigt eine Gleichung, die verwendet wird, wenn K-Projektion ausgeführt wurde.](images/transformcreation-image101.png)

x (0) = x, der Eingabe Punkt und der BC-Wert werden bei x (k) definiert. Entladen Sie dann die Projektionen, indem Sie eine Reihe von Ausgabe Vektoren definieren:

![Zeigt Gleichungen für eine Reihe von Ausgabe Vektoren an.](images/transformcreation-image103.png)

where ![Zeigt die Gleichung für Y hoch gestellt (K) an.](images/transformcreation-image105.gif) und schließlich erhalten Sie die Antwort.

![Zeigt interp (x) gleich y hoch gestellt (0) an.](images/transformcreation-image107.gif)

## <a name="worked-example"></a>Arbeitsbeispiel

![Diagramm, das ein bearbeitetes Beispiel für Interpolationen mit einem Einheiten Cube anzeigt.](images/transformcreation-image108.png)

**Abbildung 2:** Bearbeitetes Beispiel

Sehen Sie sich die in Abbildung 2 dargestellte Situation an, in der n = 3, m = 1 ist und Sie über die folgenden BCS verfügen:

(a) vier diskrete BCS auf den Vertices

(0,0):-001 001

(0, 1, 1):-011

(1, 0, 1): β 101

(1, 1, 1): β 111

(b) ein fortlaufender BC auf dem Gesicht X3 = 0: F (x1, x2)

Berechnung \# 1: Eingabe Punkt x = (0,8, 0,5, 0,2). Der einschließende Tetrahedron ist der permutations &lt; 1, 2, 3 zugeordnet &gt; .

1. Projektion: ![Zeigt die Gleichung für die erste Projektion an.](images/transformcreation-image110.png)

Dies befindet sich bereits auf dem Gesicht X3 = 0, sodass Sie den Vorgang abbrechen können. Rückwärts Ersetzung gibt dann

![Zeigt die Antwort für die erste Projektion an.](images/transformcreation-image112.png) Das ist die Antwort.

Berechnung \# 2: Eingabe Punkt x = (0,2, 0,5, 0,8). Der einschließende Tetrahedron ist der permutations &lt; 3, 2, 1 zugeordnet &gt; .

1. Projektion: ![Zeigt die Gleichung für die erste Projektion der Berechnung 2 an.](images/transformcreation-image113.png)

2. Projektion: ![Zeigt die Gleichung für die zweite Projektion von Berechnung 2 an.](images/transformcreation-image115.png)

Dritt-Projektion: ![Zeigt die Gleichung für die dritte Projektion von Berechnung 2 an.](images/transformcreation-image117.png) , die sich auf dem Gesicht X3 = 0 befindet. Rückwärts Ersetzung gibt dann

![Zeigt die ersten beiden Gleichungen für die rückwärts Ersetzung.](images/transformcreation-image119.png)

![Zeigt die dritte Gleichung für den rückwärts Austausch an.](images/transformcreation-image123.png), was die endgültige Antwort ist.

## <a name="applications"></a>Anwendungen

*(a) sequenzielle tetrahedral-Interpolations*

![Das Diagramm, das die sequenzielle, tetrahedral-Interpolierung anzeigt](images/transformcreation-image124.png)

**Abbildung 3:** Sequenzielle tetrahedral-Interpolations

Weitere Informationen finden Sie in Abbildung 3. Wenn Sie zwischen zwei Ebenen interpolieren möchten, auf denen inkompatible Raster erzwungen wurden, sollten Sie eine Zelle in Erwägung nehmen, die ein angegebenes Punkt P in der Abbildung einschließt. Die "oberen" Scheitel Punkte der Zelle stammen direkt aus dem Raster in der obersten Ebene. Die Scheitel Punkte im unteren Bereich sind nicht mit dem Raster in der unteren Ebene kompatibel. Daher wird die ganze Fläche so behandelt, als hätte Sie eine BC mit Werten, die durch Interpolationen im Raster auf der unteren Ebene abgerufen werden. Dann ist klar, dass diese Einrichtung die Annahmen (a), (b) und (c) oben erfüllt, und Sie können den Interpolations Algorithmus anwenden.

Außerdem ist klar, dass der Algorithmus die Dimension des Interpolations Problems um 1 reduziert hat, da das Ergebnis eine lineare Kombination von Werten an den Scheitel Punkten im oberen Raster ist, und Interpolationen in der unteren Ebene mit einer Dimension, die kleiner als 1 ist. Wenn in der unteren Ebene eine ähnliche Konfiguration der Konfiguration mit einer Größe vorhanden ist, können Sie die Prozedur in dieser Ebene anwenden, um die Dimension um 1 weiter zu reduzieren. Dieses Verfahren kann fortgesetzt werden, bis Sie Dimension 0 erreichen. Diese Cascade of Projektionen und Interpolationen können als "sequenzielle tetrahedrale Interpolation" bezeichnet werden.

*(b) GAP-Interpolations*

![Diagramm, das die GAP-Interpolations Zeichen anzeigt.](images/transformcreation-image126.jpg)

**Abbildung 4:** Lücken interpolung

Hierbei handelt es sich um ein Raster, das für einen Cube, der sich strikt innerhalb des positiven Quadranten befindet, Der Cube selbst verfügt über ein Raster, und jede Koordinaten Ebene verfügt über Raster, die nicht notwendigerweise kompatibel sind. Die "Lücke" zwischen dem Cube und den Koordinaten Flächen weist einen quer Abschnitt auf, der "L-geformt" ist und nicht für Standardverfahren geeignet ist. Mit dem hier eingeführten Verfahren können Sie jedoch problemlos Zellen einführen, die diese Lücke abdecken. Abbildung 4 zeigt eine dieser beiden. Die Raster auf den Koordinaten Ebenen unterstützen Interpolation, die die erforderlichen BCS für alle untersten Flächen der Zelle bereitstellt, wobei ein verbleibender Scheitelpunkt in der unteren Ecke des Cubes vorhanden ist.

## <a name="final-note-on-implementation"></a>Abschließende Notiz zur Implementierung

In der eigentlichen Anwendung wird der "Einheiten Cube", bei dem es sich um die grundlegende Einstellung des Algorithmus handelt, aus größeren Lattices extrahiert, und für die Werte in den Scheitel Punkten ist möglicherweise eine aufwändige Berechnung erforderlich. Andererseits ist auch klar, dass die-Interpolationen von tetrahedral nur die Werte an den Scheitel Punkten des Tetrahedron-Werts erfordert, bei dem es sich um eine Teilmenge aller Scheitel Punkte des Einheiten Cubes handelt. Daher ist es effizienter, zu implementieren, was als "verzögerte Auswertung" bezeichnet werden kann. In einer Software Implementierung des vorangehenden Algorithmus ist es typisch, eine Unterroutine zu haben, die den Unit-Cube und die Werte in den Scheitel Punkten als Eingabe annimmt. Verzögerte Auswertung bedeutet, dass anstelle der Übergabe der Werte in den Scheitel Punkten die erforderlichen Informationen zum Auswerten der Werte der Scheitel Punkte übergeben werden, ohne die Auswertung tatsächlich auszuführen. Innerhalb der Unterroutine wird die tatsächliche Auswertung dieser Werte nur für die Scheitel Punkte ausgeführt, die zum einschließenden Tetrahedron gehören, nachdem der einschließende Tetrahedron festgelegt wurde.

## <a name="lookup-table-for-use-with-high-dynamic-range-virtual-rgb-source-devices"></a>Such Tabelle für die Verwendung mit hochleistungsfähigen virtuellen RGB-Quell Geräten

Wenn eine Transformation mit einem Quellgerät erstellt wird, das als virtuelles RGB-Gerät modelliert wird, ist es möglich, dass die Quell-Colorant-Werte negativ oder größer als Unity (1,0) sein können. Wenn dies auftritt, wird auf das Quellgerät als ein hoher dynamischer Bereich (HDR) verwiesen. Dies wird in diesem Fall besonders berücksichtigt.

Im Fall von HDR-Transformationen können die minimalen und maximalen Werte für jeden Colorant-Kanal von der Spiel Grenze des Geräts bestimmt werden. Durch die Verwendung dieser Werte wird eine einfache Skalierung für jeden Colorant-Kanal angewendet, sodass Colorant-Werte, die dem minimalen Colorant entsprechen, in 0,0 konvertiert werden, und Colorant-Werte, die dem maximalen Colorant entsprechen, werden in 1,0 konvertiert, wobei die Werte zwischen 0,0 und 1,0 linear skaliert werden.

### <a name="iccprofilefromwcsprofile"></a>Iccprofilefromwcsprofile

Der Hauptzweck dieses Features ist die Unterstützung von Windows-Versionen vor Vista, die in der ICC-Spezifikation "ICC. 1:1998-09" definiert 2,2 sind. In bestimmten Fällen (Weitere Informationen finden Sie in der folgenden Tabelle "Baselineversion für die profilklassen Zuordnung"). Sie können ein Matrix-oder TRC-basiertes ICC-Profil aus einem WCS-Profil erstellen. In anderen Fällen besteht das ICC-Profil aus LUTs. Im folgenden Verfahren wird das Erstellen der ATOB-und bdea-LUTs beschrieben. Natürlich haben auch die-ICC-Profile andere Felder. Einige der Daten können aus dem WCS-Profil abgeleitet werden. Für andere Daten müssen Sie intelligente Standardeinstellungen entwickeln. Das Copyright wird Microsoft zugewiesen. Da es sich um eine Microsoft-Technologie handelt, die zum Erstellen der LUTs verwendet wird.

Dieser Entwurf sollte für alle Arten von Geräte Modellen, einschließlich Plug-ins, funktionieren. Wenn das Plug-in über ein zugeordnetes Baseline-Gerätemodell verfügt, kann der zugrunde liegende Gerätetyp bestimmt werden.

Der schwierigste Teil der Erstellung eines ICC-Profils ist das Erstellen der ATOB-und bdea-Nachschlage Tabellen. Diese Tabellen werden zwischen dem Geräte Speicherplatz (z. b. RGB oder CMYK) und dem Profil Verbindungsbereich (PCs), der eine Variante von CIELAB ist, zugeordnet. Dies ist im Grunde das gleiche wie der Farb Verwaltungsprozess, der in der "Zitat"-Transformation verwendet wird, um vom Gerätespeicher zu einem Gerätespeicher zuzuordnen. Sie müssen jedoch über die folgenden Informationen verfügen, um die Transformation vornehmen zu können.

1) Verweis Anzeige Bedingungen für die PCs.

2) Referenz-PCs.

3) Gerätemodell, das zwischen PCs-Werten und farmetriedaten konvertiert.

Das WCS-Profil und das dazugehörige CAM werden als Parameter bereitgestellt. Es gibt zwei grundlegende Gerätemodelle, die zwischen farmetriedaten und der PCs-Codierung konvertieren. Der Grund, warum Sie zwei benötigen, wird im folgenden erläutert.

1) Sie können die Verweis Anzeige Bedingungen für die PCs von der Spezifikation für das ICC-Profil Format abrufen. Die Informationen in der Spezifikation für das ICC-Profil Format reichen aus, um alle Daten zu berechnen, die zum Initialisieren der vom CMS verwendeten CAM erforderlich sind. Aus Gründen der Konsistenz und Flexibilität werden diese Informationen in einem WCS-Farbprofil gespeichert.

2) Sie können ein WCS-Profil auch zum Speichern von Beispielen verwenden, die den verweiscode der PCs definieren. Das "CIT Color Management System (CMS)" bietet zwei Möglichkeiten zum Erstellen von spielgrenzen. Eine besteht darin, ein Beispiel für den gesamten Gerätebereich zu erstellen und das Gerätemodell zum Erstellen von Messwerten zu verwenden. Die zweite Methode besteht darin, gemessene Stichproben aus dem Profil zu verwenden, um eine Verweis-Farbskala-Grenze zu erstellen. Da der Umfang der ICC-PCs zu groß ist, um ein nützliches Verweis Spiel zu erstellen, ist die erste Methode ungeeignet. Die zweite Methode ist jedoch ein flexibler, Profil basierter Ansatz. Zum Neudefinieren des Referenz-PCs können Sie die Mess Daten im Geräte Profil des PCs ändern.

3) Die ICC-PCs sind eine Modellierung eines idealen Geräts. Wenn Sie ein Modell der PCs als echtes Gerät erstellen, können Sie den Farb Verwaltungsprozess nutzen, der im intelligenten CMM verwendet wird. Das Erstellen eines Geräte Modells aus farmetriedaten zur PCs-Codierung ist einfach. Sie ordnen einfach zwischen den true-Werten für farbige Metriken und den von PCs codierten Werten zu. Da die CMS-Schnittstelle für Gerätemodelle nur XYZ-Werte unterstützt, müssen Sie möglicherweise auch zwischen XYZ und Lab zuordnen. Dies ist eine bekannte Transformation. Dieses Modell wird im Dokument 2.2.02 "Baseline-Gerätemodelle" in den Abschnitten 7,9 und 7,10 beschrieben.

Möglicherweise müssen Sie eine gewisse Spiel Zuordnung durchführen, wenn die Größe des Geräts größer ist als die Größe der PCs. Die baselinegmms können zu diesem Zweck verwendet werden. Beachten Sie, dass ein ordnungsgemäß erstelltes "ICC-Profil" Nachschlage Tabellen für die relative farbige Metrik, die perzeptive und die Sättigung hat, obwohl diese möglicherweise intern auf denselben LUT zeigen.

![Diagramm, das die Erstellung einer t o B L U T anzeigt.](images/transformcreation-image128.png)

**Abbildung 5:** Erstellung eines ATOB-LUT

Dieser Prozess ist in Abbildung 5 dargestellt. Zuerst wird das Gerätemodell von den Daten im DM-Profil aus initialisiert. Erstellen Sie dann wie folgt eine Grenze für das Geräte Spiel. Eine Stichprobe der Daten aus dem Gerätemodell wird über das Gerätemodell ausgeführt, um Farbige Metrikdaten zu erhalten. Die farbige Metrikdaten werden über die Cam durchlaufen, um Darstellungs Daten zu erstellen. Die Darstellungs Daten werden verwendet, um die Geräte-Farbskala-Grenze zu erstellen.

Verwenden Sie als nächstes Daten aus dem Mess Profil "Referenz-PCs", um eine Farbskala-Grenze für die PCs zu erstellen.

Verwenden Sie die beiden soeben erstellten Roaminggrenzen, um ein GMM zu initialisieren. Verwenden Sie dann das Gerätemodell, GMM und das Gerätemodell "PCs", um eine Transformation zu erstellen. Führen Sie eine Stichprobe des Geräte Speicherplatzes durch die Transformation aus, um einen ATOB-LUT zu erstellen.

![Diagramm, das die Erstellung einer t o B L U T mithilfe einer Stichprobe von P C s anzeigt.](images/transformcreation-image130.png)

**Abbildung 6:** Erstellung eines BPER-a-LUT

In Abbildung 6 wird die Erstellung der BPER a-LUT veranschaulicht. Dies ist nahezu identisch mit dem Erstellen einer ATOB-LUT, bei der die Rollen Quelle und Ziel ausgetauscht wurden. Außerdem müssen Sie ein Beispiel für den gesamten PCs erstellen, um den LUT zu erstellen.

Beachten Sie Folgendes: da der Cam-Code (CIECAM02 in WCS) an dem Prozess beteiligt ist, wird die statische Anpassung zwischen dem Medien weißen und dem PCs-weißen Punkt (von "ICC" als "von D50" vorgeschrieben) transparent von der Cam beeinflusst.

## <a name="hdr-virtual-rgb-devices"></a>Virtuelle HDR-Geräte in HDR

Beim Erstellen von Profilen für virtuelle HDR-Geräte müssen besondere Aspekte berücksichtigt werden. Das heißt, Geräte, für die die Colorant-Werte kleiner als 0,0 oder größer als 1,0 sein können. Bei der Generierung des ATOB-LUT wird ein größerer Satz von 1D-Eingabe-LUTs erstellt. Colorant-Werte werden auf den Bereich 0 (null) skaliert und versetzt. 1 Verwenden der minimalen und maximalen Colorant-Werte im WCS-Profil.

Da der Colorant-Speicherplatz für HDR-Geräte wahrscheinlich nicht vollständig aufgefüllt ist, wird auch im 3D-LUT für das Tag eine spezielle Unterstützung bereitgestellt. Um Farben im dünn gefüllten Bereich zu verarbeiten, werden die Colorants so neu angeordnet, dass die Extrapolierung über 0,0 und 1,0 erreicht werden kann. Der verwendete Bereich ist-1. + 4.

Da die Neuerstellung auf den 3D-LUT angewendet wird, wird ein Satz von 1D-Ausgabe-LUTs erstellt, um das Ergebnis wieder dem Bereich 0 zuzuordnen. 1.

## <a name="more-than-one-pcs"></a>Mehr als ein PC

Der IStGH hat festgestellt, dass ein PC nicht ausreichend flexibel war, um alle beabsichtigten Verwendungsmöglichkeiten eines CMS zu erfüllen. In Version 4 der Profil Spezifikation hat der IStGH festgestellt, dass tatsächlich zwei PCs Codierungen vorhanden sind. Eine wird für die farbige metrikintents verwendet. eine andere wird für die wahrnehmsame Absicht verwendet. (Für die Sättigung ist kein PC angegeben. Der IStGH hat diesen Teil nicht eindeutig gelassen.) Die farbige Metrik-PCs haben eine minimale und maximale Helligkeit angegeben, aber die Werte für "Chroma" und "Hue" reichen von ungefähr ± 127. Diese PCs sehen wie ein rechteckiges Prism aus. Wie bereits erwähnt, ähnelt das Volume für die perzeptive PCs dem Spiel in einem Inkjet-Drucker.

Die beiden "ICC pcss" verfügen ebenfalls über zwei verschiedene digitale Codierungen. In den perzeptive PCs stellt der Wert 0 (null) eine Helligkeit von NULL dar. In den PCs mit der Farbmetrik stellt der Wert 0 (null) die minimale Helligkeit der PCs dar, die größer als 0 (null) ist. Sie können dieses Problem beheben, indem Sie für jede der PCs Codierungen ein anderes Gerätemodell haben.

## <a name="gamut-mapping"></a>Gamut-Zuordnung

Um die ATOB-LUTs in einem ICC-Profil zu erstellen, ordnen Sie den entsprechenden PCs aus dem Gerätebereich zu. Zum Erstellen der bjea-LUTs ordnen Sie den Speicherplatz auf dem Gerät zu. Die Zuordnung für die ATOB-LUTs ähnelt der in einem Mess basierten CMS verwendeten. Ordnen Sie für die perzeptive PCs das als "Gerät" plausible Farbskala der Wahrnehmungsgrenze für "perzeptive PCs" zu. verwenden Sie entweder Clipping oder Komprimierung für alle Farben, die nicht im Spiel sind. Für die farbige metrikintents müssen Sie möglicherweise die Helligkeit abschneiden, aber die Werte für "Chroma" und "Hue" werden alle in den Farb verkabelten PCs angepasst.

Die Zuordnung für die BTO a-LUTs ist ein wenig anders. Die farmetrieintents sind immer noch einfach. Sie schneiden lediglich PCs-Werte an den Geräte Gamut aus. Der IStGH erfordert jedoch, dass alle möglichen PCs-Werte einem Geräte Wert zugeordnet werden, nicht nur den Werten im Verweis Spiel der perzeptive PCs. Daher müssen Sie sicherstellen, dass die GMMs Quell Farben verarbeiten können, die sich außerhalb des Verweis gamses befinden. Dies kann durch Clipping dieser Farben an die Geräte Spiel Grenze behandelt werden.

## <a name="baseline-device-to-icc-profile-class-mapping"></a>Zuordnung von baselinegerät zu ICC-Profilklasse



| Baselinegerätetyp              | ICC-Profilklasse       | Anmerkung                                                                      |
|-----------------------------------|-------------------------|-----------------------------------------------------------------------------|
| RGB-Erfassungsgerät                | Eingabegerät ("SCNR")   | PCs sind CIELAB. AToB0Tag ist ein Gerät für PCs mit relativer farbmetrikabsicht. |
| CRT, LCD-Monitor                  | Gerät anzeigen ("MNTR") | PCs sind CIEXYZ. Sehen Sie sich die folgenden Informationen zur Modell Konvertierung an.                      |
| RGB-Projektor                     | Farbraum ("SPAC")    | PCs sind CIELAB.                                                              |
| RGB-und CMYK-Drucker              | Ausgabegerät ("PRTR")  | PCs sind CIELAB.                                                              |
| Virtuelles RGB-Gerät (nicht-HDR-Fall) | Gerät anzeigen ("MNTR") | PCs sind CIEXYZ.                                                              |
| RGB virtuelles Gerät (HDR-Fall)     | Farbraum ("SPAC")    | PCs sind CIELAB.                                                              |



 

Die Konvertierung von monitorprofilen umfasst nicht das Erstellen von LUTs, sondern besteht darin, ein Matrix-oder TRC-Modell zu erstellen. Das in "ICC" verwendete Modell unterscheidet sich geringfügig von dem in der WCS-CRT oder der LCD-Modellierung verwendeten Modell, da der Begriff "schwarze Korrektur" fehlt. Sie haben folgende Möglichkeiten:

WCS-Modell: ![Zeigt ein W-C-S-Modell an.](images/transformcreation-image132.png)

ICC-Modell: ![Zeigt ein I c c-Modell an.](images/transformcreation-image134.png)

Die Konvertierung vom WCS-Modell in das Modell "ICC" erfolgt wie folgt.

Definieren Sie neue Kurven:

![Zeigt eine Matrix zum Definieren neuer Kurven.](images/transformcreation-image136.png)

Dabei handelt es sich nicht um audioreproduktions Kurven, da Sie 1 nicht zu 1 zuordnen. Dies wird durch eine Normalisierung erreicht. Die abschließenden Definitionen des Modells "ICC" lauten wie folgt:

![Zeigt die endgültigen Definitionen des I c c-Modells an.](images/transformcreation-image138.png)

![Zeigt die endgültige Matrix für das I c c-Modell an.](images/transformcreation-image140.png)

Bei nicht-HDR RGB-Geräten erzeugen Sie auch ein Display-ICC-Profil, um die Speicherplatz Effizienz zu erhöhen. In diesem Fall kann der Matrix M- *ICC* von "400" aus den primären Replikaten des WCS-Profils ohne die oben genannte Modell Konvertierung abgerufen werden. Ein letztes, aber wichtig ist, dass diese matrixmatrixmatrix statisch an die D50 angepasst werden muss, damit Sie der ICC-Spezifikation der PCs entspricht. Mit anderen Worten, die Einträge für jede Zeile der Matrix, die im ICC-Profil codiert werden soll, müssen sich jeweils auf 96,42, 100 und 82,49 summieren. In der aktuellen Implementierung wird die chromatische Anpassung von CAT02 durchgeführt. Dies ist auch die in CAM02 verwendete Transformation für die chromatische Anpassung.

## <a name="black-preservation-and-black-generation"></a>Schwarze Beibehaltung und schwarze Generierung

Die Implementierung der Black-Beibehaltung ist mit der Generierung des schwarzen Kanals in Geräten verbunden, die einen schwarzen Kanal unterstützen. Um dies zu erreichen, werden Informationen zu den einzelnen Quell Farben gesammelt, um Geräte Modellen zu ermöglichen, die einen schwarzen Kanal unterstützen, um zu bestimmen, wie der schwarze Kanal bei der Ausgabe am besten festgelegt wird Obwohl die schwarze Beibehaltung für Farb Transformationen wichtig ist, die zwischen einem blackchannel-Gerät in ein anderes konvertieren, wird die schwarze Generierung für alle Transformationen implementiert, die ein Ziel Gerät mit schwarzem Kanal betreffen.

Informationen zu blackchannels werden in einer Datenstruktur namens [**blackinformation**](/previous-versions/windows/desktop/api/WcsPlugIn/ns-wcsplugin-_blackinformation)aufgezeichnet. Die **blackinformation** -Struktur enthält einen booleschen Wert, der angibt, ob die Farbe nur schwarze Colorant und einen numerischen Wert enthält, der den Grad der "schwarze Gewichtung" angibt. Bei Quell Geräten, von denen ein schwarzer Kanal unterstützt wird, ist die schwarze Gewichtung der Prozentsatz der schwarzen Colorant in der Quellfarbe. Für Quell Geräte, die keinen schwarzen Kanal enthalten, wird die schwarze Gewichtung mit den anderen Colorants und dem Darstellungs Wert berechnet. Ein Wert mit dem Namen "Color Purity" wird berechnet, indem der Unterschied zwischen dem maximalen Colorant-Wert und dem minimalen Colorant-Wert dividiert durch den maximalen Colorant-Wert genommen wird. Ein Wert mit dem Namen "relative Helligkeit" wird berechnet, indem der Unterschied zwischen der Tiefe der Farbe und der minimalen Helligkeit für das Zielgerät dividiert durch den Unterschied zwischen der minimalen und maximalen Helligkeit für das Zielgerät unterschieden wird. Wenn das Quellgerät ein Additiv Gerät (Monitor oder Projektor) ist, wird das schwarze Gewicht als 1,0 abzüglich der Farben Reinheit, multipliziert mit der relativen Helligkeit, festgelegt. Wenn das Quellgerät beispielsweise ein RGB-Monitor ist, werden der Höchstwert und der minimale Wert von R, G und B für jede Farbe berechnet, und die schwarze Gewichtung wird durch die Formel bestimmt:

BW = (1,0 – (max (r, g, b) – min (r, g, b))/Max (r, g, b)) \* relative Helligkeit

Wenn das Quellgerät subtraktive Farbgebung (z. b. einen CMY-Drucker) unterstützt, müssen die einzelnen Colorants vor der Verwendung in der vorhergehenden Formel "Ones" (von "1,0" subtrahiert) werden. Daher gilt für einen CMY-Drucker R = 1,0 – C, G = 1,0 – M und B = 1,0 – Y.

Die schwarzen Informationen für jede Farbe, die von der Farb Transformation verarbeitet wird, werden während des Farb Übersetzungs Vorgangs bestimmt. Die nur-schwarz-Informationen werden nur bestimmt, wenn die schwarze Beibehaltung angegeben wird. Die schwarze Gewichtung wird immer bestimmt, wenn das Zielgeräte Modell einen schwarzen Colorant unterstützt. Die schwarzen Informationen werden über die [**farbige metrictodevicecolorswithblack**](/previous-versions/windows/desktop/api/WcsPlugIn/nf-wcsplugin-idevicemodelplugin-colorimetrictodevicecolorswithblack) -Methode an das Zielgeräte Modell übergeben, die den resultierenden LUT verwendet.

Beachten Sie, dass der oben genannte Prozess aufgrund der Farb Transformations Optimierung nur während der Erstellung der optimierten Transformation "LUT" auftritt, nicht während der Ausführung der Methode "translatecolors".

## <a name="optimization-for-transforms-with-more-than-three-source-channels"></a>Optimierung für Transformationen mit mehr als drei Quell Kanälen

Die Größe der optimierten Transformation wird durch verschiedene Faktoren bestimmt: die Anzahl der farbchannels im Quellgerät, die Anzahl der Schritte in der Tabelle für jeden Quell Farbkanal und die Anzahl der farbchannels im Ausgabegerät. Die Formel zum Bestimmen der Transformations Tabellengröße lautet:

Größe = Anzahl von Schritten pro <sub>channelquelle \ Gerät (Nummer \ von \ Channels \ in \ Quelle \ Gerät)</sub> x Anzahl der Kanäle im Ausgabegerät

Wie Sie sehen können, wächst die Größe der Tabelle in Abhängigkeit von der Anzahl der Kanäle im Quellgerät exponentiell. Viele Quell Geräte unterstützen drei Farbkanäle, z. b. rot, grün und blau. Wenn ein Quellgerät jedoch vier Kanäle unterstützt, wie z. b. CMYK, wird die Größe der Tabelle und die Zeit, die zum Erstellen der Tabelle erforderlich ist, um den Faktor der Anzahl von Schritten vergrößert. In einem Mess basierten CMS, in dem Transformationen dynamisch erstellt werden, ist diese Zeit möglicherweise nicht akzeptabel.

Um die Zeit zu verkürzen, die zum Erstellen der Tabelle für die Farbkonvertierung erforderlich ist, können Sie zwei Fakten nutzen. Wenn das Quellgerät möglicherweise mehr als drei Farbkanäle unterstützt, weist der zwischen geräteunabhängige farbliche Leerraum (CIECAM02 ja <sub>c</sub> b <sub>c</sub> ) nur drei Farbkanäle auf. Zweitens ist der zeitaufwändigste Teil der Verarbeitung nicht die Geräte Modellierung (die von Koordinaten für Geräte Farben in die Werte von "Wert" für den Wert von "Wert"), sondern die Farbskala-Zuordnung. Mithilfe dieser Fakten können Sie eine vorläufige Farb Konvertierungstabelle erstellen, die Farben in den geräteunabhängigen Farbraum durch die Farbskala-Zuordnungen und schließlich durch das Ausgabegeräte-Farbmodell konvertiert. Die Erstellung dieser Tabelle ist eine Dimension von drei. Anschließend erstellen wir die Dimension vier abschließende Farb Konvertierungstabelle, indem wir die Quell Farbkombinationen in zwischen geräteunabhängigen Raum konvertieren. Anschließend wird die Konvertierung in den Ausgabegeräte-Farbraum mithilfe der vorläufigen Farb Konvertierungstabelle abgeschlossen. Daher verringern Sie die Anzahl der Schritte in der Nachschlage Tabelle (Anzahl der Schritte in der Nachschlage Tabelle) <sub>Anzahl \ der Channels</sub> , die für die Zuordnung von Berechnungen zu der Anzahl von Schritten in der zwischen Tabelle ₃ Farbskala-Mapping-Berechnungen ausgeführt werden. Obwohl Sie die Anzahl der Schritte in der (Nachschlage Tabelle) <sub>Anzahl \ der Channels</sub> -Berechnungen von Geräte Modellierung und dreidimensionalen Tabellen Suchvorgängen ausführen müssen, ist dies nach wie vor die ursprüngliche Berechnung erheblich schneller.

Der vorherige Prozess funktioniert gut, wenn es nicht erforderlich ist, dass Informationen zwischen dem Quell Gerätemodell und einer anderen Komponente in der Farb Transformation übergeben werden. Wenn jedoch sowohl das Ausgabegerät als auch das Quellgerät einen schwarzen Colorant unterstützen, und der Quell-schwarze Colorant zum Ermitteln der Ausgabe blackcolorant verwendet wird, kann der Prozess die schwarzen Informationen der Quelle nicht ordnungsgemäß kommunizieren. Ein alternativer Prozess besteht darin, eine vorläufige Farb Konvertierungstabelle zu erstellen, die Farben in den geräteunabhängigen Farbraum nur durch die Schritte zum Erstellen von Farbskala-Zuordnungen konvertiert. Erstellen Sie dann mit den folgenden Schritten die Dimension vier abschließende Farb Konvertierungstabelle: a) konvertieren Sie die Kombination aus Quell Farben in zwischen geräteunabhängigen Raum, b) führen Sie die Schritte zum Zuordnen der Schritte aus, indem Sie in der vorläufigen Farbtabelle interpolieren, anstatt die tatsächlichen gamingzuordnungsprozesse anzuwenden, und c) verwenden Sie die resultierenden Werte aus den Farbskala-zuordnungsschritten und alle Informationen zu den schwarzen Kanälen der Quelle, um die Ausgabegeräte Dieser Prozess kann auch verwendet werden, wenn Informationen zwischen den Quell-und Ausgabegeräte Modellen übertragen werden, auch wenn kein schwarzer Kanal vorhanden ist. beispielsweise, wenn die beiden Module mit einer Plug-in-Architektur implementiert werden, die einen Datenaustausch zwischen Modulen ermöglicht.

Die beiden vorangegangenen Prozesse können verwendet werden, um die Zeit, die zum Erstellen der vierdimensionalen Farb Transformations Tabelle benötigt wird, effektiv zu verbessern.

### <a name="checkgamut"></a>Prüfpunkt

Der ICM Ruft ein Wort von Flagwerten auf, bei denen es sich bei den ICM **-aufrufen um die** Überprüfung der über \_ \_ Prüfung. Wenn dieses Flag festgelegt ist, muss die Transformation von "Cite" unterschiedlich erstellt werden. Die ersten Schritte sind identisch: die Quell-und Ziel-Cams müssen initialisiert werden, dann müssen die-Quell-und Ziel-Begrenzungs Deskriptoren initialisiert werden. Unabhängig von der angegebenen Absicht muss der Prüfpunkt GMM verwendet werden. Der Prüfpunkt-GMM sollte mit den Quell-und Zielgeräte Modellen und den Deskriptoren für die Spiel Grenze initialisiert werden. Die Transformation sollte dann jedoch eine abgeschnittene Transformation erstellen, die das Quell Gerätemodell, die Quell-Cam, alle Beteiligten GMMs und den Prüfpunkt GMM umfasst. Dadurch wird sichergestellt, dass die von der Prüfpunkt-CMM ausgegebene Delta-, Delta-C-und Delta-h-Werte zu den endgültigen resultierenden Werten werden.

Die Bedeutung von checkgamut ist klar, wenn in der Transformation nur zwei Geräteprofile vorhanden sind. Wenn mehr als zwei Geräteprofile und mehr als zwei GMMs vorhanden sind, meldet checkgamut, ob die Farben, die durch das erste Gerätemodell und alle außer dem letzten GMM transformiert wurden, in den Spielpunkt des Zielgeräts fallen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Konzepte der grundlegenden Farbverwaltung](basic-color-management-concepts.md)
</dt> <dt>

[Windows Color System: Schemas und Algorithmen](windows-color-system-schemas-and-algorithms.md)
</dt> </dl>

 

 




