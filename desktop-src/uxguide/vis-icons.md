---
title: Symbole (Entwurfsgrundlagen)
description: Symbole sind bildliche Darstellungen von Objekten, die nicht nur aus optischen Gründen als Teil der visuellen Identität eines Programms wichtig sind, sondern auch aus utilittarischen Gründen als Kurzform für die Darstellung der Bedeutung, die Benutzer fast sofort wahrnimmt.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: ad788338adc81bd9bc796412eebf4bef87ceca2b7a3855e024702a3e1bb23e49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119841857"
---
# <a name="icons-design-basics"></a>Symbole (Entwurfsgrundlagen)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Symbole sind bildliche Darstellungen von Objekten, die nicht nur aus optischen Gründen als Teil der visuellen Identität eines Programms wichtig sind, sondern auch aus utilittarischen Gründen als Kurzform für die Darstellung der Bedeutung, die Benutzer fast sofort wahrnimmt. Windows Vista führt einen neuen Stil der Symbolografie ein, der einen höheren Detail- und Raffinessesgrad Windows.

**Hinweis:** Richtlinien im Zusammenhang [mit Standardsymbolen](vis-std-icons.md) werden in einem separaten Artikel vorgestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Der Name für die Benutzeroberfläche von Windows Vista, der sowohl die werte darstellt, die im Design der Erscheinungsbilder als auch die Vision hinter der Benutzeroberfläche (UI) verankert sind. Schriftschrift: Authentic, Authentistik, Reflektierend und Offen. Es ist das Ziel eines Entwurfs, der sowohl professional als auch schön ist. Die Vonnäktik von Stil sorgt für eine hochwertige und elegante Erfahrung, die die Produktivität der Benutzer erleichtert und sogar eine emotionale Reaktion antreibt.

Windows Vista-Symbole unterscheiden sich Windows Xp-Symbolen auf folgende Weise:

-   Der Stil ist realistischer als veranschaulichend, aber nicht ganz fotorealistisch. Symbole sind symbolische Bilder, die besser aussehen sollten als fotorealistisch!
-   Symbole haben eine maximale Größe von 256 x 256 Pixeln und eignen sich daher für Anzeige mit hohen DPI-Zeichen (Punkte pro Zoll). Diese hochauflösenden Symbole ermöglichen eine hohe visuelle Qualität in Listenansichten mit großen Symbolen.
-   Wenn dies praktisch ist, werden feste Dokumentsymbole durch Miniaturansichten des Inhalts ersetzt, wodurch Dokumente leichter zu identifizieren und zu finden sind.
-   Symbolleistensymbole haben weniger Details und keine Perspektive, um sie für kleinere Größen und visuelle Unterscheidung zu optimieren.

Gut entworfene Symbole:

-   Verbessern Sie die visuelle Kommunikation Ihres Programms.
-   Wirkt sich stark auf den allgemeinen Eindruck der Benutzer des visuellen Designs Ihres Programms aus und ist auf die Anpassung und Denkleistung des Programms sehr gut geeignet.
-   Verbessern Sie die Benutzerfreundlichkeit, indem Sie Programme, Objekte und Aktionen leichter identifizieren, lernen und finden können.

In den folgenden Abbildungen wird dargestellt, was den Stil der Symbolografie in Windows Vista von dem in Windows XP unterscheidet.

![Bilder von Sperre und Schlüsselsymbolen](images/vis-icons-image1.png)

Die Windows Vista-Symbole (die Sperre und die Taste auf der linken Seite) sind authentifiziert, klar und detailliert. Sie werden gerendert und nicht gezeichnet, sind aber nicht vollständig fotorealistisch.

![Bilder von Symbolen für Welt- und Notebooks](images/vis-icons-image2.png)

Die Windows Vista-Symbole (die beiden auf der linken Seite) sind professional und schön, mit Aufmerksamkeit auf Details, die die Qualität der Symbolproduktion verbessern.

![Bilder von Notebook, Sperre, Monitor und Papier](images/vis-icons-image3.png)

Diese Windows Vista-Symbole zeigen den optischen Ausgleich und die wahrgenommene Genauigkeit in Perspektive und Details. Dadurch können sie groß oder klein, nah oder aus der Entfernung aussehen. Darüber hinaus funktioniert diese Art der Symbolografie für hochauflösende Bildschirme.

![Bild eines Drahtlosroutersymbols](images/vis-icons-image4.png)![Bild eines Papierblattsymbols](images/vis-icons-image5.png)![Bild eines großen, grünen Pfeilsymbols nach rechts](images/vis-icons-image6.png)

Diese Beispiele zeigen verschiedene Arten von Symbolen, einschließlich eines dreidimensionalen Objekts aus Perspektive, eines nach vorne gerichteten (flachen) Symbols und eines Symbolleistensymbols.

## <a name="guidelines"></a>Richtlinien

### <a name="perspective"></a>Perspektive

-   **Symbole in Windows Vista sind entweder dreidimensional und werden perspektivisch als solide Objekte oder zweidimensionale Objekte direkt dargestellt.** Verwenden Sie flache Symbole für Dateien und Objekte, die tatsächlich flach sind, z. B. Dokumente oder Papierteile.

    ![Bilder von 3D-Computern und flachem 2d-Papier ](images/vis-icons-image7.png)

    Typische 3D- und flache Symbole.

-   **Dreidimensionale Objekte werden perspektivisch als solide Objekte dargestellt, die aus einer niedrigen Sicht mit den Augen der Augen mit zwei schlichen Punkten betrachtet werden.**

    ![Abbildung des Notebooks mit Zeilen, die die Perspektive zeigen](images/vis-icons-image8.png)

    In diesem Beispiel werden perspektiven- und verschwindende Punkte dargestellt, die typisch für 3D-Symbole sind.

-   **In kleineren Größen kann sich dasselbe Symbol von Perspektive zu Direktformat ändern.** Rendern Sie Symbole mit einer Größe von 16 x 16 Pixeln und kleiner direkt (nach vorne gerichtet). Verwenden Sie für größere Symbole die Perspektive.

    -   **Ausnahme:** Symbolleistensymbole sind immer nach vorne gerichtet, auch in größeren Größen.

    ![Abbildung eines großen 3D-Computers und eines kleinen 2D-Computers ](images/vis-icons-image9.png)

    In diesem Beispiel wird gezeigt, wie dasselbe Symbol je nach Größe unterschiedlich behandelt wird.

### <a name="light-source"></a>Lichtquelle

-   **Die Lichtquelle für Objekte im Perspektivraster befindet sich oberhalb, leicht vor und etwas links vom Objekt.**
-   **Die Lichtquelle wirft Schatten, die sich leicht hinter und rechts von der Basis des Objekts befinden.**
-   **Alle Lichtlichtlichter sind parallel und schlagen das Objekt entlang desselben Winkels (z. B. die Sonnenlichter).** Das Ziel ist es, eine einheitliche Beleuchtungsform für alle Symbole und Spotlighteffekte zu erhalten. Parallele Lichtlichtlichter erzeugen Schatten, die alle dieselbe Länge und Dichte aufweisen, was eine weitere Einheit über mehrere Symbole hinweg bietet.

### <a name="shadows"></a>Shadows

**Allgemein**

-   **Verwenden Sie Schatten, um Objekte visuell aus dem Hintergrund zu heben und 3D-Objekte geerbt und nicht umknallig im Raum zu sehen.**
-   **Verwenden Sie einen Deckkraftbereich von 30 bis 50 Prozent für Schatten.** Manchmal sollte je nach Form oder Farbe eines Symbols eine andere Schattenebene verwendet werden.
-   **Federn Sie den Schatten, oder kürzen Sie ihn bei Bedarf, damit er nicht durch die Größe des Symbolfelds zugeschnitten wird.**
-   **Verwenden Sie keine Schatten in Symbolen mit 24 x 24 oder kleineren Größen.**

    ![Bilder von 3D-Symbolen mit Schatten ](images/vis-icons-image10.png)

    Typische Symbolschatten.

**Flache Symbole**

-   **Flache Symbole werden in der Regel für Dateisymbole und flache** reale Objekte wie ein Dokument oder ein Papier verwendet.
-   **Die Beleuchtung des flachen Symbols stammt von oben links bei 130 Grad.**
-   **Kleinere Symbole (z. B. 16 x 16 und 32 x 32) werden zur Vereinfachung der Lesbarkeit vereinfacht.** Wenn sie jedoch eine Reflektion innerhalb des Symbols enthalten (häufig vereinfacht), können sie einen engen Schlagschatten haben. Der Schlagschattenbereich liegt bei Durchlässigkeit zwischen 30 und 50 Prozent.
-   **Ebeneneffekte können für flache Symbole verwendet werden, sollten aber mit anderen flachen Symbolen verglichen werden.** Die Schatten für Objekte variieren etwas, je nach dem, was am besten aussieht und am konsistentesten innerhalb der festgelegten Größe und mit den anderen Symbolen in Windows Vista ist. In einigen Fällen kann es sogar erforderlich sein, die Schatten zu ändern. Dies gilt insbesondere, wenn Objekte über andere objekte gelegt werden.
-   **Ein feiner Farbbereich kann verwendet werden, um das gewünschte Ergebnis zu erzielen.** Schatten helfen Objekten im Raum. Die Farbe wirkt sich auf die wahrgenommene Gewichtung des Schattens aus und kann das Bild verzerren, wenn es zu stark ist.

![Screenshot des Dialogfelds mit aktivierter Schlagschattenprüfung ](images/vis-icons-image11.png)![Screenshot des Papiersymbols mit schmalem Schlagschatten ](images/vis-icons-image12.png)

Die Option Schlagschatten im Dialogfeld Ebenenstil und ein typischer Schatten für ein flaches Symbol.

**Einfache Flache Symbolschattenbereiche**



| Merkmal                              | Range                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Schwarz<br/>                                         |
| Blend-Modus<br/>         | Multiplizieren<br/>                                      |
| Opacity<br/>            | 22 bis 50 Prozent, abhängig von der Farbe des Elements<br/> |
| Angle<br/>              | 120-130 (globales Licht verwenden)<br/>                    |
| Entfernung<br/>           | 3 für 256 x 256, im Bereich von bis zu 1 für 32 x 32<br/>    |
| Spread<br/>             | 0<br/>                                             |
| Size<br/>               | 7 für 256 x 256, im Bereich von bis zu 2 für 32 x 32<br/>    |



 

**Dreidimensionale Symbole**

-   Erstellen Von Fall zu Fall Schatten für 3D-Symbole mit dem Aufwand, innerhalb eines Bereichs von Umwandlungsabstand und Federung vollständig transparent zu sein. Erstellen Sie die Bilder in einer Größe, die etwas kleiner als die Gesamtgröße des Symbols ist, um Platz für einen Fallschatten zu schaffen (für die Größen, die einen benötigen). Stellen Sie sicher, dass der Schatten nicht plötzlich am Rand des Symbols endet.

![Abbildung des Erstellens von Schatten in Bildern](images/vis_icons_image13.jpeg)

![Abbildung von vier Objekten mit unterschiedlichen Schatten](images/vis_icons_image14.jpeg)

Anhand dieser Beispiele können Variationen veranschaulicht werden, die basierend auf der Form und Position des Objekts selbst erstellt wurden. Der Schatten muss manchmal mit Federn versehen oder verkürzt werden, damit er nicht durch die Größe des Symbolfelds zugeschnitten wird.

### <a name="color-and-saturation"></a>Farbe und Sättigung

-   **Farben sind im Allgemeinen weniger überlasteten als Windows XP.**
-   **Verwenden Sie Farbverläufe, um ein realistischeres Bild zu erstellen.**
-   **Obwohl es keine spezifische Farbpalette für Standardsymbole gibt, denken Sie daran, dass sie in vielen Kontexten und Designs gut zusammenarbeiten müssen.** Bevorzugen Sie den Standardsatz von Farben. Standardsymbole, z. B. Warnsymbole, werden nicht neu farbig dargestellt, da dies die Fähigkeit der Benutzer zum Interpretieren der Bedeutung beeinträchtigt. Weitere Richtlinien finden Sie unter [Farbe.](vis-color.md)
-   **Symboldateien erfordern auch 8-Bit- und 4-Bit-Palettenversionen,** um die Standardeinstellung auf einem Remotedesktop zu unterstützen. Diese Dateien können über einen Batchprozess erstellt werden, sollten jedoch überprüft werden, da einige dateien retouching erfordern, um die Lesbarkeit zu verbessern.

    ![Screenshot des Dialogfelds "Farbauswahl" ](images/vis-icons-image15.png)

    Es gibt keine strikte Einschränkung der Farbpalette. Es wird nur die vollständige Sättigung (oben rechts) vermieden.

-   Bitebenen: ICO-Entwurf für 32-Bit (Alpha enthalten) + 8-Bit + 4-Bit (automatisch abgeblendet, pixelgenau nur am kritischsten). Es sollte nur eine 32-Bit-Kopie des Bilds mit 256 x 256 Pixeln enthalten sein, und nur das Bild mit 256 x 256 Pixeln sollte komprimiert werden, um die Dateigröße zu verkleinern. Mehrere Symboltools bieten eine Komprimierung für Windows Vista.
-   Bitebenen: Symbolleisten 24-Bit + Alpha (1-Bit-Maske), 8-Bit und 4-Bit.
-   Symbolleisten oder AVI-Dateien: Verwenden Sie Magenta (R255 G0 B255) als Hintergrundtransparenzfarbe.

### <a name="size-requirements"></a>Größenanforderungen

**Allgemein**

-   **Achten Sie besonders auf Symbole** mit hoher Sichtbarkeit, z. B. Hauptanwendungssymbole, Dateisymbole, die in Windows Explorer angezeigt werden können, und Symbole, die im Startmenü oder auf dem Desktop angezeigt werden.
    -   **Anwendungssymbole und Systemsteuerung Elemente:** Der vollständige Satz umfasst 16 x 16, 32 x 32, 48 x 48 und 256 x 256 (Code skaliert zwischen 32 und 256). Das ICO-Dateiformat ist erforderlich. Für den klassischen Modus ist der vollständige Satz 16x16, 24x24, 32x32, 48x48 und 64x64.
    -   **Optionen für Listenelementsymbole:** Verwenden Sie Liveminiaturansichten oder Dateisymbole des Dateityps (z. B. .doc). vollständiger Satz.
    -   **Symbolleistensymbole:** 16x16, 24x24, 32x32. Beachten Sie, dass Symbolleistensymbole immer flach und nicht 3D sind, auch bei einer Größe von 32 x 32.
    -   **Dialogfeld- und Assistentensymbole:** 32 x 32 und 48 x 48.
    -   **Überlagerungen:** Core Shell-Code (z.B. eine Verknüpfung) 10x10 (für 16x16), 16x16 (für 32x32), 24x24 (für 48x48), 128x128 (für 256x256). Beachten Sie, dass einige davon etwas kleiner sind, aber je nach Form und optischem Gleichgewicht in der Nähe dieser Größe liegen.
    -   **Schnellstart Bereich:** Symbole werden von 48 x 48 in dynamischen ALT+TAB-Überlagerungen herunterskaliert, aber für eine präziseere Version fügen Sie eine 40x40-Datei zur ICO-Datei hinzu.
    -   **Sprechblasensymbole:** 32 x 32 und 40 x 40.
    -   **Zusätzliche Größen:** Diese sind nützlich, um als Ressourcen andere Dateien zu erstellen (z. B. Anmerkungen, Symbolleistenstreifen, Überlagerungen, hohe dpi und Sonderfälle): 128x128, 96x96, 64x64, 40x40, 24x24, 22x22, 14x14, 10x10 und 8x8. Sie können je nach Code in diesem Bereich ICO-, .png-, .bmp- oder andere Dateiformate verwenden.

**Für hohe DPI-Daten**

-   Windows Vista ist auf 96 dpi und 120 dpi ausgerichtet.

Die folgenden Tabellen zeigen Beispiele für Skalierungsverhältnisse, die auf zwei gängige Symbolgrößen angewendet werden. Beachten Sie, dass nicht alle diese Größen in der ICO-Datei enthalten sein müssen. Der Code skaliert größere herunter.



| dpi                   | Symbolgröße                         | Skalierungsfaktor                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16 x 16<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 20 x 20<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 32 x 32<br/>         | 2.0 (200%)<br/>       |



 



| dpi                   | Symbolgröße                         | Skalierungsfaktor                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32 x 32<br/>         | 1.0 (100%)<br/>       |
| 120<br/>     | 40 x 40<br/>         | 1.25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1.5 (150%)<br/>       |
| 192<br/>     | 64 x 64<br/>         | 2.0 (200%)<br/>       |



 

**ICO-Dateigrößen (Standard)**

![Diagramm, das verschiedene Routersymbole im Standardformat zeigt.](images/vis-icons-image16.png)

**ICO-Dateigrößen (Sonderfälle)**

![Abbildung von Routersymbolen unterschiedlicher Größe ](images/vis-icons-image17.png)

**Anmerkungen und Überlagerungen**

-   Anmerkungen befinden sich in der unteren rechten Ecke des Symbols und sollten 25 Prozent des Symbolbereichs ausfüllen.
    -   **Ausnahme:** 16 x 16 Symbole nehmen 10 x 10 Anmerkungen an.
-   Verwenden Sie nicht mehr als eine Anmerkung über einem Symbol.
-   Überlagerungen befinden sich in der unteren linken Ecke des Symbols und sollten 25 Prozent des Symbolbereichs ausfüllen.
    -   **Ausnahme:** 16 x 16 Symbole nehmen 10 x 10 Überlagerungen an.

### <a name="level-of-detail"></a>Detailgrad

-   Die Größe 16 x 16 vieler dieser Symbole wird weiterhin häufig verwendet und ist daher wichtig.
-   Die Details in einem Symbol dieser Größe müssen den Schlüsselpunkt des Symbols deutlich anzeigen.
-   Wenn ein Symbol kleiner wird, sollten Transparenz und einige spezielle Details, die in größeren Größen gefunden werden, reduziert werden, um den Punkt zu vereinfachen und zu erreichen.
-   Attribute und Farben sollten hervorgehoben und verwendet werden, um die wichtigsten Formen hervorzuheben.

    ![Abbildung eines großen und zwei kleinen Geräts ](images/vis-icons-image18.png)

    Bei 16x16 kann das Symbol für das portable Audiogerät leicht mit einem Mobiltelefon verwechselt werden, sodass das Hörgerät ein wichtiges visuelles Detail ist, das angezeigt werden soll.

-   Das einfache Herunterskalierung von 256 x 256 funktioniert nicht.
-   Alle Größen benötigen eine relevante Detailstufe. Je kleiner das Symbol ist, desto mehr müssen Sie die definierenden Details abschätzen.

    ![Abbildung von Mobiltelefonen mit eindeutigen Details ](images/vis-icons-image19.png)

    ![Abbildung von Mobiltelefonen mit unscharfen Details ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Symbolentwicklung

**Entwerfen und Erstellen von Symbolen**

-   **Stellen Sie einen erfahrenen Grafikdesigner ein.** Für hervorragende Grafiken, Bilder und Symbole arbeiten Sie mit Experten zusammen. Erfahrung in Abbildungen mit Vektorart oder 3D-Programmen wird empfohlen.
-   Planen Sie eine **Reihe von Iterationen,** von anfänglichen Konzeptzeichnungen über Kontextmodelle bis hin zu abschließenden Produktionsüberprüfungen und Anpassungen von Symbolen im funktionierenden Produkt.
-   **Die Erstellung von Think-Ahead-Symbolen kann teuer sein.** Erfassen Sie alle vorhandenen Details und Anforderungen, z. B.: den vollständigen Satz von benötigten Symbolen; die Hauptfunktion und die Bedeutung für jede; Familien oder Cluster in der Gruppe, die sie sichtbar machen möchten; Markenanforderungen; die genauen Dateinamen; Bildformate, die in Ihrem Code verwendet werden; - und -Größenanforderungen. Stellen Sie im Voraus sicher, dass Sie Ihre Zeit mit dem Designer optimal nutzen können.
-   **Denken Sie daran, dass der Designer möglicherweise nicht mit Ihrem Produkt vertraut ist. Geben Sie daher ggf. funktionale Informationen, Screenshots und Spezifikationsabschnitte an.**
-   **Planen Sie ggf. geopolitische und rechtliche Überprüfungen.**
-   **Ordnen Sie einen Zeitrahmen zu, und kommunizieren Sie regelmäßig.**

**Vom Konzept skizzieren zum Endprodukt**

![Abbildung der Entwicklung von Zeichnungen von Mobiltelefonen ](images/vis-icons-image21.png)

-   Erstellen sie Konzept skizzieren.
-   Probieren Sie das Konzept in verschiedenen Größen aus.
-   Rendern Sie bei Bedarf in 3D.
-   Testgrößen in verschiedenen Hintergrundfarben.
-   Wertet Symbole im Kontext der echten Benutzeroberfläche aus.
-   Erstellen Sie eine endgültige ICO-Datei oder andere Grafikressourcenformate.

**Tools**

-   **Stift und Papier:** Anfängliche Konzeptideen, aufgelistet und gezeichnet.
-   **Max. 3D Studio:** Rendern von 3D-Objekten in perspektive.
-   **Adobe Adobe:** Skizzieren und Iterieren, Modellieren im Kontext und Abschließen von Details.
-   **Adobe Adobe/ Macromedia Freehand:** Skizzieren und iterieren, Details abschließen.
-   **Gamani Gif Movie Gear:** Erstellen Sie eine ICO-Datei (bei Bedarf mit Komprimierung).
-   **Workshop zum Symbol "Oisis":** Erstellen Sie eine ICO-Datei (bei Bedarf mit Komprimierung).
-   Microsoft Visual Studio unterstützt Windows Vista-Symbole nicht (alphakanal- oder mehr als 256 Farben werden nicht unterstützt).

**Produktion**

> [!TIP]
> Führen Sie diese Schritte aus, um eine einzelne ICO-Datei zu erstellen, die mehrere Bildgrößen und Farbtiefe enthält.

**Schritt 1: Konzeptualisierung**

-   Verwenden Sie nach Möglichkeit bewährte Konzepte, um die Konsistenz der Bedeutungen für das Symbol und seine Relevanz für andere Verwendungen sicherzustellen.
-   Überlegen Sie, wie das Symbol im Kontext der Benutzeroberfläche angezeigt wird und wie es als Teil einer Reihe von Symbolen funktionieren kann.
-   Wenn Sie ein vorhandenes Symbol überarbeiten, sollten Sie überlegen, ob die Komplexität reduziert werden kann.
-   Berücksichtigen Sie die kulturellen Auswirkungen Ihrer Grafiken. Vermeiden Sie die Verwendung von Buchstaben, Wörtern, Händen oder Gesichtern in Symbolen. Stellen Sie Darstellungen von Personen oder Benutzern bei Bedarf so generisch wie möglich dar.
-   Wenn Sie mehrere Objekte in einem einzelnen Bild in einem Symbol kombinieren, sollten Sie berücksichtigen, wie das Bild auf kleinere Größen skaliert wird. Verwenden Sie nicht mehr als drei Objekte in einem Symbol (zwei werden bevorzugt). Bei einer Größe von 16 x 16 sollten Sie objekte entfernen oder das Bild vereinfachen, um die Erkennung zu verbessern.
-   Verwenden Sie nicht das Windows-Flag in Symbolen.

**Schritt 2: Veranschaulichen**

-   Um Windows Stilsymbole zu veranschaulichen, verwenden Sie ein Vektortool wie Macromedia Freehand oder Adobe Styles. Verwenden Sie die Palette und die Stilmerkmale, wie weiter oben in diesem Artikel beschrieben.
-   Abbildung mitHilfe von Freehand oder Erfolgt. Kopieren Sie die Vektorbilder, und fügen Sie sie in AdobePhoto ein.
-   Verwenden Sie eine Vorlagenebene in Bildern, um sicherzustellen, dass die Arbeit in quadratischen Bereichen der regulierten Größen ausgeführt wird.
-   Erstellen Sie die Bilder in einer Größe, die etwas kleiner als die Gesamtgröße des Symbols ist, um Platz für einen Fallschatten zu schaffen (für größen, die einen benötigen).
-   Platzieren Sie Bilder am unteren Rand der Quadrate, sodass alle Symbole in einem Verzeichnis konsistent positioniert werden. Vermeiden Sie das Abschneiden von Schatten.
-   Wenn Sie einem Bild oder einer Reihe ein weiteres Objekt hinzufügen, behalten Sie das Hauptobjekt an einer festen Position bei, und platzieren Sie flache Bilder mit geringerer Größe an einer festen Position, z. B. unten links oder oben rechts, je nach Groß-/Kleinschreibung.

**Schritt 3: Erstellen der 24-Bit-Images**

-   Nachdem Sie Größen in Photos eingefügt haben, überprüfen Sie die Lesbarkeit von Bildern, insbesondere bei 16 x 16 und kleineren Größen. Es kann erforderlich sein, pixelbasierte Färbung mitHilfe von Prozentsätzen von Farben zu verwenden. Es kann auch erforderlich sein, die Transparenz zu reduzieren. Es ist üblich, Aspekte in kleineren Größen zu vermeiden und aspekte zu beseitigen, um sich auf den Schlüsselpunkt zu konzentrieren.
-   Die 8-Bit-Symbole werden in einem beliebigen Farbmodus angezeigt, der kleiner als 32-Bit ist, und verfügen nicht über den 8-Bit-Alphakanal. Daher müssen sie möglicherweise ihre Ränder oder mehr bereinigt werden, da kein Antialiasing vorhanden ist (Kanten sind möglicherweise verzweigt und Das Bild ist möglicherweise schwer zu lesen).
-   Duplizieren Sie in Photos die 24-Bit-Bildebene, und benennen Sie die Ebene in 4-Bit-Bilder um. Indizierung von 4-Bit-Bildern in die Windows 16-Farbpalette.
-   Bereinigen Sie Bilder, indem Sie nur die Farben aus der 16-Farbpalette verwenden. Konturen aus dunkleren oder leichteren Versionen der Farben des Objekts sind in der Regel grau oder schwarz vorzuziehen.
-   Wenn Sie an einer Bitmap arbeiten, stellen Sie sicher, dass die Hintergrundfarbe nicht im Bild selbst verwendet wird, da diese Farbe die transparente Farbe ist. Magenta (R255 G0 B255) wird häufig als Hintergrundtransparenzfarbe verwendet.

**Schritt 4: Erstellen der 8-Bit- und 4-Bit-Bilder**

-   Nachdem die 24-Bit-Bilder nun in 32-Bit-Symbole umgewandelt werden können, müssen 8-Bit-Versionen erstellt werden.
-   Dies ist ein guter Zeitpunkt, um kontextbezogene Screenshots zu testen. Es ist verblüffend, was durch das Anzeigen anderer Symbole oder einer Familie von Symbolen im Kontext ermittelt werden kann. Dieser Schritt kann Zeit und Geld sparen. Es ist viel besser, Probleme abzufangen, bevor Dateien in die Produktion gehen und übergeben werden.
-   Fügen Sie Ihren Bildern den Schatten in Größen hinzu, die sie erfordern.
-   Führen Sie den Schattenschatten und die 24-Bit-Bilder zusammen.
-   Erstellen Sie für jede Größe eine neue Csv-Datei. Kopieren Sie das entsprechende Bild, und fügen Sie es ein. Speichern Sie jede Datei als .psd Datei.
-   Führen Sie die Bildebene nicht mit der Hintergrundebene zusammen. Es ist hilfreich, die Größe und Farbtiefe während der Arbeit in den Dateinamen aufzunehmen, aber die Datei muss möglicherweise letztendlich umbenannt werden.

**Schritt 5: Erstellen der ICO-Datei**

-   Wählen Sie die Anwendung aus, die den Anforderungen und Fähigkeiten von Interpreten am besten entspricht. Denken Sie daran, dass Symbole, die in einem Versandprodukt verwendet werden sollen, in einem Tool erstellt werden müssen, das erworben oder lizenziert wurde. Dies bedeutet, dass Keine Testversionen verwendet werden können.
-   Beide unten aufgeführten Produkte wurden von Designern verwendet, die Symbole für Windows Vista erstellt haben, und bieten jeweils die Möglichkeit, nach Adobe Acrobat CS zu exportieren.
    -   Gamani Gif Movie Gear: Produce .ico file (Gamani Gif Movie Gear: ICO-Datei erstellen)
    -   Workshop zu Oisis-Symbolen: Erstellen einer ICO-Datei
-   Visual Studio unterstützt Windows Vista-Symbole nicht (alphakanal- oder mehr als 256 Farben werden nicht unterstützt), daher wird die Verwendung nicht empfohlen.
-   Symboldateien (.ico-Format) müssen die 4- und 8-Bit-Versionen sowie die 24-Bit- und Alphaversionen enthalten.
-   Speichern Sie Dateien als "Windows Symbol (.ico)", unabhängig davon, welches Symbolerstellungsprogramm Sie verwenden möchten.
-   Einige symbolografische Objekte können tatsächlich Bitmaps sein, die auch einen Alphakanal (z. B. für Symbolleisten) oder .png Dateien erfordern, die transparent gespeichert sind. Nicht alle sind notwendigerweise das ICO-Format. Überprüfen Sie, welches Format im Code unterstützt wird.

**Schritt 6: Auswerten**

-   Sehen Sie sich alle Größen an.
-   Sehen Sie sich die Familie zusammen an, um die Ähnlichkeit der Familie, das optische Gleichgewicht und die Unterscheidung zu bewerten.
-   Sehen Sie sich dies im Kontext an, um relative Gewichtungen und Sichtbarkeit auszuwerten (stellen Sie sicher, dass sie nicht vorherrschen).
-   Berücksichtigen Sie Fälle, die derzeit möglicherweise nicht verwendet werden, aber in naher Zukunft auftreten können. Kann dieses Symbol jemals mit Anmerkungen versehen werden oder eine Überlagerung aufweisen?
-   Sehen Sie sich im Code an.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Symbole im Kontext von Listenansichten, Symbolleisten und Strukturansichten

**Listenansichten**

-   Verwenden Sie für Windows Vista Miniaturansichten für Dateien mit Inhalten, die sich visuell in kleinem Umfang unterscheiden, sodass Benutzer die gesuchte Datei direkt erkennen können. (Verwenden Sie hierfür die Anwendungsprogrammierschnittstelle Windows Thumbnailing.)

    ![Screenshot des Windows-Explorers mit Ordnersymbolen ](images/vis-icons-image22.png)

-   Anwendungssymbolüberlagerungen (hier nicht gezeigt) auf Miniaturansichten helfen bei der Zuordnung zur Anwendung für den Dateityp, zusätzlich zur Anzeige der Vorschau der Datei.

**Hinweis:** Verwenden Sie für Dateien ohne visuell unterschiedlichen Inhalt keine Miniaturansichten. Verwenden Sie stattdessen herkömmliche symbolische Dateisymbole, die die Objektdarstellung und die zugeordnete Anwendung oder den typ anzeigen.

**Symbolleisten**

-   Symbole, die auf einer Symbolleiste angezeigt werden, müssen ein optisches Gleichgewicht in Größe, Farbe und Komplexität haben.
-   Testen Sie potenzielle Symbole in einem kontextbezogenen Screenshot, um unerwünschte Dominanz oder Störungen zu vermeiden.
-   Durch einfaches Testen in Screenshots lassen sich teure Iterationen im Code vermeiden.
-   Überprüfen Sie auch die Symbole im Code. Bewegung und andere Faktoren können sich auf den Erfolg eines Symbols auswirken. in einigen Fällen sind möglicherweise weitere Iterationen erforderlich.

![Screenshot der Symbolleiste mit kleinen Symbolen und Bezeichnungen ](images/vis-icons-image23.png)

Im obigen Beispiel wurde der optische Ausgleich noch nicht erreicht.

![Abbildung von Symbolen auf unterschiedlichen Hintergründen ](images/vis-icons-image24.png)

Probieren Sie Iterationen im Kontext aus.

**Strukturansichten**

-   Ein optischer Ausgleich ist erforderlich, um die Hierarchie in einem Strukturansicht-Steuerelement zu erhalten.
-   Daher sollten Symbole, die normalerweise in diesem Kontext verwendet werden, dort ausgewertet werden. Manchmal sollte ein bestimmtes 16x16-Symbol kleiner werden, da seine Form eine optische Dominanz gegenüber anderen hat.
-   Die Kompensation für optische Sehenswürdigkeiten ist ein wichtiger Bestandteil der Erstellung von Symbolen der besten Qualität.

![Abbildung von zwei Gruppen von Ordnern in der Strukturansicht ](images/vis-icons-image25.png)

 

