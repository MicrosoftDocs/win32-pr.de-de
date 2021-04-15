---
title: Symbole (Entwurfsgrundlagen)
description: Symbole sind visuelle Darstellungen von Objekten, wichtig nicht nur aus Gründen der visuellen Darstellung im Rahmen der visuellen Identität eines Programms, sondern auch aus den Verwendungs Gründen als Kurzform, um zu vermitteln, dass Benutzer nahezu sofort wahrnehmen.
ms.assetid: 6f88cb32-ecfe-4e6e-a41b-31891cf510cf
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 9dc0994aa4e7aa07709a8051f9b13b72142bcb7b
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104568977"
---
# <a name="icons-design-basics"></a>Symbole (Entwurfsgrundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Symbole sind visuelle Darstellungen von Objekten, wichtig nicht nur aus Gründen der visuellen Darstellung im Rahmen der visuellen Identität eines Programms, sondern auch aus den Verwendungs Gründen als Kurzform, um zu vermitteln, dass Benutzer nahezu sofort wahrnehmen. Windows Vista führt eine neue Art von Ikonographie ein, die für Windows einen höheren Detail-und Raffinierungs Grad bietet.

**Hinweis:** Richtlinien im Zusammenhang mit [Standardsymbolen](vis-std-icons.md) werden in einem separaten Artikel dargestellt.

## <a name="design-concepts"></a>Entwurfskonzepte

Aero ist der Name für die Benutzeroberfläche von Windows Vista und repräsentiert sowohl die Werte, die im Design der Ästhetik enthalten sind, als auch die Vision hinter der Benutzeroberfläche. Aero steht für: authentisch, energisch, reflektiert und offen. Aero soll ein Design einrichten, das sowohl professionell als auch schön ist. Die Aero-Ästhetik sorgt für eine qualitativ hochwertige und elegante Benutzeroberflächen, die die Produktivität der Benutzer und sogar eine emotionale Reaktion ermöglicht.

Windows Vista-Symbole unterscheiden sich von Symbolen im Windows XP-Stil wie folgt:

-   Die Formatvorlage ist realistischer als die Veranschaulichung, aber nicht ganz mit dem Foto. Symbole sind symbolische Bilder, die besser als photorealist aussehen sollten.
-   Symbole haben eine maximale Größe von 256 x 256 Pixel, sodass Sie für High-dpi-Anzeige (Punkte pro Zoll) geeignet sind. Diese Symbole mit hoher Auflösung ermöglichen eine hohe visuelle Qualität in Listenansichten mit großen Symbolen.
-   Wenn Sie praktisch sind, werden die Symbole fester Dokumente durch Miniaturansichten des Inhalts ersetzt, sodass Dokumente leichter zu identifizieren und zu finden sind.
-   Symbolleisten Symbole haben weniger Details und keine Perspektive, um für kleinere Größen und visuelle Besonderheiten zu optimieren.

Gut entworfene Symbole:

-   Verbessern Sie die visuelle Kommunikation Ihres Programms.
-   Der allgemeine Eindruck des visuellen Entwurfs des Programms und seine Anpassung an den Benutzer werden stark beeinträchtigt.
-   Verbessern Sie die Benutzerfreundlichkeit, indem Sie Programme, Objekte und Aktionen leichter identifizieren, erlernen und finden.

In den folgenden Abbildungen wird dargestellt, wie sich der Aero-Stil von Ikonographie in Windows Vista von dem in Windows XP verwendeten unterscheidet.

![Bilder von Sperr-und Schlüssel Symbolen](images/vis-icons-image1.png)

Die Windows Vista-Symbole (die Sperre und die Taste auf der linken Seite) sind authentisch, knusprig und ausführlich. Sie werden gerendert und nicht gezeichnet, aber nicht vollständig mit der Foto

![Bilder der Symbole "Globus" und "Spiral Notebook"](images/vis-icons-image2.png)

Die Windows Vista-Symbole (die beiden auf der linken Seite) sind professionell und schön, mit Details, die die Qualität der Symbol Produktion verbessern.

![Bilder von Notebook, Lock, Monitor und Paper](images/vis-icons-image3.png)

Diese Windows Vista-Symbole zeigen den optischen Saldo und die wahrgenommene Genauigkeit in Perspektive und Details. Auf diese Weise können Sie groß oder klein oder in einer Entfernung sehen. Außerdem funktioniert diese Art von iconographie für Bildschirme mit hoher Auflösung.

![Bild eines drahtlosen routersymbols](images/vis-icons-image4.png)![Abbildung eines Blatts mit Papier Symbol](images/vis-icons-image5.png)![Bild eines großen, grünen Rechtspfeil Symbols](images/vis-icons-image6.png)

Diese Beispiele zeigen verschiedene Arten von Symbolen, einschließlich eines dreidimensionalen Objekts in der Perspektive, ein Front-of-Symbol (flaches Symbol) und ein Symbolleisten Symbol.

## <a name="guidelines"></a>Richtlinien

### <a name="perspective"></a>Perspektive

-   **Symbole in Windows Vista sind entweder dreidimensional und in Perspektive als Solid Objects oder zweidimensionale Objekte, die direkt angezeigt werden.** Verwenden Sie flache Symbole für Dateien und für Objekte, die tatsächlich flach sind, wie z. b. Dokumente oder Papier Teile.

    ![Images von 3D--Computern und flachen, 2D-Papier ](images/vis-icons-image7.png)

    Typische 3D-und flache Symbole.

-   **Dreidimensionale Objekte werden als Solid-Objekte dargestellt, die von einer unteren Vogelperspektive mit zwei verschwindenden Punkten angesehen werden.**

    ![Bild von Notebook mit Zeilen, die eine Perspektive zeigen](images/vis-icons-image8.png)

    Dieses Beispiel zeigt Perspektiven und verschwindende Punkte, die typisch für 3D-Symbole sind.

-   **In der kleineren Größe kann sich das gleiche Symbol von Perspektive in direkt ändern.** Bei einer Größe von 16x16 Pixel und kleiner wird das rendersymbol direkt angezeigt (Front-End). Verwenden Sie für größere Symbole die Perspektive.

    -   **Ausnahme:** Symbolleisten Symbole sind immer in der Vorderseite, sogar in größeren Größen.

    ![Abbildung von großen 3D--Computern und kleinen 2D-Computern ](images/vis-icons-image9.png)

    Dieses Beispiel zeigt, wie das gleiche Symbol abhängig von der Größe anders behandelt wird.

### <a name="light-source"></a>Lichtquelle

-   **Die helle Quelle für Objekte innerhalb des perspektivischen Rasters ist oberhalb, etwas vor und leicht links vom Objekt.**
-   **Die Light-Quelle wandelt Schatten ein, die sich leicht nach hinten und rechts neben der Basis des Objekts befinden.**
-   **Alle Lichtstrahlen sind parallel, und das Objekt wird auf denselben Winkel (wie die Sun) hin.** Das Ziel besteht darin, eine einheitliche Beleuchtung für alle Symbole und Spotlight-Effekte zu haben. Parallele Lichtstrahlen verursachen Schatten, die alle die gleiche Länge und Dichte aufweisen und eine weitere Unity über mehrere Symbole hinweg bereitstellen.

### <a name="shadows"></a>Shadows

**Allgemein**

-   **Verwenden Sie Shadowing zum visuellen Lift von Objekten aus dem Hintergrund und zum Anzeigen von 3D-Objekten auf der Grundlage von unflexiblen Leerraum.**
-   **Verwenden Sie für Schatten einen Deckkraft Bereich von 30-50 Prozent.** Manchmal sollte eine andere Schattenebene verwendet werden, je nach Form oder Farbe eines Symbols.
-   **Sie können den Schatten bei Bedarf verkleinern, um zu verhindern, dass er von der Symbolfeld Größe abgeschnitten wird.**
-   **Verwenden Sie keine Schatten in Symbolen mit einer Größe von rund um die Uhr oder weniger.**

    ![Bilder von 3D--Symbolen mit Schatten ](images/vis-icons-image10.png)

    Typische Symbol Schatten.

**Flache Symbole**

-   **Flache Symbole werden im Allgemeinen für Dateisymbole und flache reale Objekte verwendet,** z. b. ein Dokument oder ein Papier Stück.
-   **Die flache Symbol Beleuchtung wird von links oben um 130 Grad angezeigt.**
-   **Kleinere Symbole (z. b. 16x16 und 32x32) werden zur besseren Lesbarkeit vereinfacht.** Wenn Sie jedoch eine Reflektion innerhalb des Symbols (häufig vereinfacht) enthalten, verfügen Sie möglicherweise über einen engen Schlag Schatten. Der Ablage Schatten liegt bei einer Deckkraft von 30-50 Prozent.
-   **Ebeneneffekte können für flache Symbole verwendet werden, sollten aber mit anderen flachen Symbolen verglichen werden.** Die Schatten für Objekte variieren in gewisser Weise, je nachdem, was am besten aussieht und am ehesten innerhalb der Größe festgelegt ist, und mit den anderen Symbolen in Windows Vista. In manchen Fällen kann es sogar notwendig sein, die Schatten zu ändern. Dies trifft vor allem dann zu, wenn Objekte über andere festgelegt werden.
-   **Ein feiner Bereich von Farben kann verwendet werden, um das gewünschte Ergebnis zu erzielen.** Shadows helfen Objekten dabei, sich im Raum zu befinden. Die Farbe wirkt sich auf die wahrgenommene Gewichtung des Schattens aus und kann das Bild verzerren, wenn es zu stark ist.

![Screenshot des Dialog Felds mit geprüftem Schlag Schatten ](images/vis-icons-image11.png)![Screenshot des Papier Symbols mit engem Schlag Schatten ](images/vis-icons-image12.png)

Die Drop Shadow-Option im Ebenenstil-Dialogfeld und ein typischer Schatten für ein flaches Symbol.

**Grundlegende flache Symbol Schattenbereiche**



| Merkmal                              | Range                                                         |
|-------------------------------|----------------------------------------------------------|
| Color<br/>              | Schwarz<br/>                                         |
| Blend-Modus<br/>         | Multiplizieren<br/>                                      |
| Opacity<br/>            | 22-50 Prozent, abhängig von der Farbe des Elements<br/> |
| Angle<br/>              | 120-130 (globales Licht verwenden)<br/>                    |
| Entfernung<br/>           | 3 für 256 x 256, im Bereich von 32 x 32 bis 1<br/>    |
| Spread<br/>             | 0<br/>                                             |
| Size<br/>               | 7 für 256 x 256, mit bis zu 2 für 32x32<br/>    |



 

**Dreidimensionale Symbole**

-   Erstellen Sie Schatten Kopien für 3D-Symbole, und legen Sie für die Groß-/Kleinschreibung fest, dass Sie in einen Bereich von Umwandlungs Entfernung passen und die Darstellung vollständig transparent gestalten können. Erstellen Sie die Bilder in einer Größe, die kleiner ist als die Gesamtgröße der Symbolgröße, um Platz für einen Ablage Schatten zuzulassen (für die Größen, die eine solche Größe erfordern). Stellen Sie sicher, dass der Schatten am Rand des Symbols nicht abrupt endet.

![Abbildung der Erstellung von Schatten in Photoshop](images/vis_icons_image13.jpeg)

![Abbildung von vier Objekten mit unterschiedlichen Schatten](images/vis_icons_image14.jpeg)

Diese Beispiele helfen dabei, Variationen zu veranschaulichen, die auf Grundlage der Form und Position des Objekts selbst erstellt werden. Der Schatten muss manchmal gefiedert oder verkürzt werden, damit er nicht von der Größe des Symbol Felds abgeschnitten wird.

### <a name="color-and-saturation"></a>Farbe und Sättigung

-   **Farben sind im Allgemeinen weniger ausgelastet als Windows XP.**
-   **Verwenden Sie Farbverläufe, um ein realistischeres Abbild zu erstellen.**
-   **Obwohl es keine bestimmte Farbpalette für Standardsymbole gibt, sollten Sie daran denken, dass Sie in vielen Kontexten und Designs gut zusammenarbeiten müssen.** Standardsatz von Farben bevorzugen; Standardsymbole, wie z. b. Warnungs Symbole, werden nicht neu gefärbt, da dadurch die Benutzer Fähigkeit gestört wird, Bedeutungen zu interpretieren. Weitere Richtlinien finden Sie unter [Color](vis-color.md).
-   Für **Symbol Dateien sind ebenfalls 8-Bit-und 4-Bit-palettenversionen erforderlich,** um die Standardeinstellung in einem Remote Desktop zu unterstützen. Diese Dateien können über einen Batch Prozess erstellt werden. Sie sollten jedoch überprüft werden, da einige für eine bessere Lesbarkeit erforderlich sind.

    ![Screenshot der Farbauswahl (Dialogfeld) ](images/vis-icons-image15.png)

    Es gibt keine strikte Farb paletteneinschränkung. Es wird nur die volle Sättigung (Top Right) vermieden.

-   Bitlevels: ico-Entwurf für 32-Bit (Alpha eingeschlossen) + 8-Bit + 4-Bit (herabstufen automatisch Pixel schaffen nur am kritischsten). Es sollte nur eine 32-Bit-Kopie des 256 x 256 Pixel-Bilds eingeschlossen werden, und nur das 256 x 256 Pixel Bild sollte komprimiert werden, um die Dateigröße zu verkleinern. Mehrere Symbol Tools bieten eine Komprimierung für Windows Vista.
-   Bitlevels: Symbolleisten 24-Bit + Alpha (1 Bit mask), 8-Bit und 4-Bit.
-   Symbolleisten oder AVI-Dateien: Verwenden Sie Magenta (R255 G0 B255) als Hintergrund Transparenz Farbe.

### <a name="size-requirements"></a>Größenanforderungen

**Allgemein**

-   **Achten Sie besonders auf Symbole mit hoher Sichtbarkeit,** wie z. b. Haupt Anwendungs Symbole, Dateisymbole, die in Windows Explorer angezeigt werden können, und Symbole, die im Startmenü oder auf dem Desktop angezeigt werden.
    -   **Anwendungs Symbole und System Steuerungselemente:** Der vollständige Satz umfasst 16x16, 32x32, 48x48 und 256x256 (Code Skalen zwischen 32 und 256). Das Dateiformat ". ico" ist erforderlich. Für den klassischen Modus beträgt der vollständige Satz 16x16, 24x24, 32x32, 48 und 64x64.
    -   **Optionen für das Listenelement Symbol:** Verwenden Sie Live Miniaturansichten oder Dateisymbole des Dateityps (z. b.. doc); vollständiger Satz.
    -   **Symbolleisten Symbole:** 16x16, 24x24, 32x32. Beachten Sie, dass Symbolleisten Symbole immer flach und nicht 3D sind, sogar mit der Größe 32x32.
    -   **Dialog-und Assistenten Symbole:** 32x32 und 48x48.
    -   Über **Lagerungen:** Kernshellcode (z. b. eine Verknüpfung) 10X10 (für 16x16), 16x16 (32 x 32), 24x24 (für 48x48), 128 x 128 (bei 256 x 256). Beachten Sie, dass einige davon etwas kleiner sind, sich aber in der Nähe dieser Größe befinden, abhängig von der Form und dem optischen Gleichgewicht.
    -   **Bereich Schnellstart:** Symbole werden von 48 in der dynamischen Überlagerungen Alt + Tab herunterskaliert. Fügen Sie jedoch für eine präzigere Version eine Datei mit einer Größe von 40 x 40 zu. ico hinzu.
    -   Sprechblasen **Symbole:** 32x32 und 40X40.
    -   **Weitere Größen:** Diese sind nützlich, wenn Sie über eine Hand als Ressourcen verfügen, um andere Dateien (z. b. Anmerkungen, Symbolleisten Streifen, Überlagerungen, hohe dpi-und Sonderfälle) zu erstellen: 128 x 128, 96x96, 64x64, 40X40, 24x24, 22x22, 14x14, 10X10 und 8x8. Abhängig vom Code in diesem Bereich können Sie ICO-, PNG-, BMP-oder andere Dateiformate verwenden.

**Für hohe dpi-**

-   Windows Vista hat 96 dpi-und 120 dpi-Ziele.

Die folgenden Tabellen zeigen Beispiele für Skalierungs Verhältnisse, die auf zwei allgemeine Symbolgrößen angewendet werden. Beachten Sie, dass nicht alle dieser Größen in die ICO-Datei eingeschlossen werden müssen. Der Code wird in größerem Umfang skaliert.



| dpi                   | Symbolgröße                         | Skalierungsfaktor                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 16 x 16<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 20 x 20<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 24x24<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 32 x 32<br/>         | 2,0 (200%)<br/>       |



 



| dpi                   | Symbolgröße                         | Skalierungsfaktor                            |
|--------------------|--------------------------|-----------------------------|
| 96<br/>      | 32 x 32<br/>         | 1,0 (100%)<br/>       |
| 120<br/>     | 40 x 40<br/>         | 1,25 (125%)<br/>      |
| 144<br/>     | 48x48<br/>         | 1,5 (150%)<br/>       |
| 192<br/>     | 64 x 64<br/>         | 2,0 (200%)<br/>       |



 

**ICO-Dateigrößen (Standard)**

![Diagramm, das verschiedene standardmäßige routersymbole anzeigt.](images/vis-icons-image16.png)

**ICO-Dateigrößen (Sonderfälle)**

![Abbildung von routersymbolen mit unterschiedlichen Größen ](images/vis-icons-image17.png)

**Anmerkungen und Überlagerungen**

-   Anmerkungen werden in der unteren rechten Ecke des Symbols angezeigt und sollten 25 Prozent des Symbol Bereichs ausfüllen.
    -   **Ausnahme:** 16x16-Symbole nehmen 10X10-Anmerkungen auf.
-   Verwenden Sie nicht mehr als eine Anmerkung für ein Symbol.
-   Überlagerungen wechseln in der unteren linken Ecke des Symbols und sollten 25 Prozent des Symbol Bereichs ausfüllen.
    -   **Ausnahme:** 16x16-Symbole akzeptieren 10X10-Überlagerungen.

### <a name="level-of-detail"></a>Detailgrad

-   die 16x16-Größe vieler dieser Symbole wird immer noch häufig verwendet und ist daher wichtig.
-   Die Details in einem Symbol dieser Größe müssen den Schlüsselpunkt des Symbols eindeutig anzeigen.
-   Wenn ein Symbol kleiner wird, sollten Transparenz und einige besondere Details in größerer Größe geopfert werden, um den Punkt zu vereinfachen und zu übernehmen.
-   Attribute und Farben sollten übertrieben und verwendet werden, um die Schlüssel Formulare hervorzuheben.

    ![Abbildung von einem großen und zwei kleinen Geräten ](images/vis-icons-image18.png)

    Bei 16x16 könnte das Symbol für das Portable Audiogerät leicht falsch für ein Mobiltelefon sein, sodass es sich bei dem Ohr um ein wichtiges visuelles Detail handelt.

-   Das einfache horizontale Herunterskalieren aus der Größe 256 x 256 funktioniert nicht.
-   Für alle Größen ist ein relevanter Detailgrad erforderlich. desto kleiner ist das Symbol, desto mehr müssen Sie die definierenden Details übertreiben.

    ![Abbildung von Mobiltelefonen mit klaren Details ](images/vis-icons-image19.png)

    ![Abbildung von Mobiltelefonen mit Verschwommene Details ](images/vis-icons-image20.png)

### <a name="icon-development"></a>Symbol Entwicklung

**Entwerfen und Erstellen von Symbolen**

-   **Beauftragen Sie einen erfahrenen Grafikdesigner.** Gute Grafiken, Bilder und Symbole arbeiten mit Experten. Es wird empfohlen, in Abbildungen mithilfe von Vektorgrafiken oder 3D-Programmen zu arbeiten.
-   **Planen Sie die Ausführung von Reihe von Iterationen,** von den ersten Konzeptskizzen bis hin zu in-context-Mock-ups, bis zur abschließenden Produktions Überprüfung und zum Anpassen von Symbolen im Arbeits Produkt.
-   **Die Erstellung des Symbols für das vorhersehen kann kostspielig sein.** Erfassen Sie alle vorhandenen Details und Anforderungen, z. b.: die vollständige Gruppe von Symbolen, die benötigt werden. Die Hauptfunktion und die Bedeutung für jede. Familien oder Cluster in der Menge, die Sie offenlegen möchten. Marken Anforderungen; die genauen Dateinamen; in Ihrem Code verwendete Bildformate; und Größenanforderungen. Stellen Sie sicher, dass Sie das meiste Zeit mit dem Designer erreichen können.
-   **Beachten Sie, dass der Designer möglicherweise nicht mit Ihrem Produkt vertraut ist. Geben Sie daher nach Bedarf funktionale Informationen, Bildschirmaufnahmen und Spezifikationen ein.**
-   **Planen Sie gegebenenfalls geopolitische und rechtliche Überprüfungen ein.**
-   **Ordnen Sie einen Zeitrahmen zu, und weisen Sie eine reguläre Kommunikation auf**

**Von der Konzeptskizze bis zum Endprodukt**

![Abbildung der Entwicklung von Skizzen von Mobiltelefonen ](images/vis-icons-image21.png)

-   Erstellen von Konzeptskizzen.
-   Testen Sie das Konzept in unterschiedlichen Größen.
-   Bei Bedarf in 3D Rendering.
-   Test Größen für verschiedene Hintergrundfarben.
-   Auswerten von Symbolen im Kontext der realen Benutzeroberfläche.
-   Erzeugt die endgültige ICO-Datei oder andere Grafik Ressourcen Formate.

**Extras**

-   **Stift und Papier:** Erste Konzeptideen, aufgelistet und skizziert.
-   **3D Studio Max:** Rendering von 3D-Objekten in der Perspektive.
-   **Adobe Photoshop:** Skizzieren und iterieren Sie, bereinigen Sie den Kontext, und Finalisieren Sie die Details.
-   **Adobe Illustrator/Macromedia FreeHand:** Sketch und Iterate, Finalize Details.
-   **Gamani Gif Movie Gear:** Die ICO-Datei wird erzeugt (bei Bedarf mit Komprimierung).
-   **Axialis-Symbol Workshop:** Die ICO-Datei wird erzeugt (bei Bedarf mit Komprimierung).
-   Microsoft Visual Studio unterstützt keine Windows Vista-Symbole (Alphakanäle oder mehr als 256 Farben werden nicht unterstützt).

**Produktion**

> [!TIP]
> Führen Sie die folgenden Schritte aus, um eine einzelne ICO-Datei zu erstellen, die mehrere Bildgrößen und Farbtiefe enthält.

**Schritt 1: konzeptualisieren**

-   Verwenden Sie nach Möglichkeit etablierte Konzepte, um die Konsistenz der Bedeutungen für das Symbol und seine Relevanz für andere Verwendungszwecke sicherzustellen.
-   Beachten Sie, wie das Symbol im Kontext der Benutzeroberfläche angezeigt wird und wie es im Rahmen eines Satzes von Symbolen funktionieren kann.
-   Wenn Sie ein vorhandenes Symbol überarbeiten, sollten Sie Bedenken, ob Komplexität reduziert werden kann.
-   Sehen Sie sich die kulturellen Auswirkungen Ihrer Grafiken an. Vermeiden Sie es, Buchstaben, Wörter, Hände oder Gesichter in Symbolen zu verwenden. Stellen Sie bei Bedarf Darstellungen von Personen oder Benutzern so generisch wie möglich dar.
-   Wenn Sie mehrere Objekte zu einem einzelnen Bild in einem Symbol kombinieren, berücksichtigen Sie, wie das Bild auf kleinere Größen skaliert wird. Verwenden Sie nicht mehr als drei Objekte in einem Symbol (zwei werden bevorzugt). In der Größe 16x16 können Sie Objekte entfernen oder das Image vereinfachen, um die Erkennung zu verbessern.
-   Verwenden Sie das Windows-Flag nicht in Symbolen.

**Schritt 2: veranschaulichen**

-   Verwenden Sie ein Vektor Tool wie Macromedia Freehand oder Adobe Illustrator, um Windows Aero-Stil Symbole zu veranschaulichen. Verwenden Sie die Palette und die Stilmerkmale, wie weiter oben in diesem Artikel beschrieben.
-   Veranschaulichen Sie das Bild mit Freehand oder Illustrator. Kopieren Sie die Vektorbilder, und fügen Sie Sie in Adobe Photoshop ein.
-   Stellen Sie eine Vorlagen Ebene in Photoshop her, und verwenden Sie Sie, um sicherzustellen, dass die Arbeit innerhalb der quadratischen Bereiche der regulierten Größen erfolgt.
-   Erstellen Sie die Bilder in einer Größe, die kleiner ist als die Gesamtgröße der Symbolgröße, um Platz für einen Ablage Schatten (für die Größen, die eine solche benötigen) zuzulassen.
-   Platzieren Sie Bilder am unteren Rand der Quadrate, damit alle Symbole in einem Verzeichnis konsistent positioniert werden. Vermeiden Sie das Ausschalten von Schatten.
-   Wenn Sie einem Bild oder einer Reihe ein weiteres Objekt hinzufügen, behalten Sie das Hauptobjekt an einer Position fester Position bei, und platzieren Sie Flatfiles mit geringer Größe an einer bestimmten Position, z. b. in der linken unteren oder oberen rechten Ecke.

**Schritt 3: Erstellen der 24-Bit-Images**

-   Nachdem Sie die Größen in Photoshop eingefügt haben, überprüfen Sie die Lesbarkeit von Bildern, insbesondere bei 16x16 und kleineren Größen. Möglicherweise ist ein Pixel-Poking mithilfe von Prozentsätzen von Farben erforderlich. Möglicherweise ist auch eine Verringerung der Transparenz erforderlich. Es ist üblich, Aspekte in geringerer Größe zu übertreiben und auch Aspekte zu beseitigen, damit Sie sich auf den Schlüsselpunkt konzentrieren können.
-   Die 8-Bit-Symbole werden in einem beliebigen Farbmodus kleiner als 32 Bit angezeigt, und der 8-Bit-Alphakanal ist nicht vorhanden, sodass Sie ggf. Ihre Ränder oder eine höhere Bereinigung benötigen, da es kein Antialiasing gibt (Kanten sind möglicherweise verzweigt, und das Bild ist möglicherweise schwer lesbar).
-   Duplizieren Sie in Photoshop die 24-Bit-Bild Ebene, und benennen Sie die Ebene in 4-Bit-Images um. Indizieren Sie 4-Bit-Bilder mit der Farbpalette von Windows 16.
-   Bereinigen Sie Bilder nur mit den Farben aus der 16-Farbpalette. Aus den Farben dunkler oder heller Versionen der Farben des Objekts vorgenommene Gliederungen sind normalerweise grau oder schwarz vorzuziehen.
-   Wenn Sie an einer Bitmap arbeiten, achten Sie darauf, dass die Hintergrundfarbe im Bild selbst nicht verwendet wird, da diese Farbe die transparente Farbe ist. Magenta (R255 G0 B255) wird häufig als Hintergrund Transparenz Farbe verwendet.

**Schritt 4: Erstellen der 8-Bit-und 4-Bit-Images**

-   Da die 24-Bit-Images nun in 32-Bit-Symbolen erstellt werden können, müssen 8-Bit-Versionen erstellt werden.
-   Dies ist ein guter Zeitpunkt, um kontextabhängige Screenshots zu testen. Es ist erstaunlich, was Sie entdecken können, indem Sie andere Symbole oder eine Familie von Symbolen im Kontext anzeigen. Mit diesem Schritt können Sie Zeit und Geld sparen. Es ist viel besser, Probleme zu erfassen, bevor Dateien die Produktion durchlaufen und übergeben werden.
-   Fügen Sie Ihren Bildern den Schlag Schatten in Größen hinzu, die Sie benötigen.
-   Zusammenführen des Schlag Schattens und der 24-Bit-Bilder.
-   Erstellen Sie für jede Größe eine neue Photoshop-Datei. Kopieren Sie das entsprechende Bild, und fügen Sie es ein. Speichern Sie jede Datei als. PSD-Datei.
-   Führen Sie die Bild Ebene nicht mit der Hintergrund Ebene zusammen. Es ist hilfreich, beim Arbeiten die Größe und Farbtiefe in den Dateinamen einzuschließen, aber die Datei muss letztendlich umbenannt werden.

**Schritt 5: Erstellen der ICO-Datei**

-   Wählen Sie die Anwendung aus, die die Anforderungen und Fähigkeiten von Künstlern am besten erfüllt. Beachten Sie, dass in einem Liefer Produkt zu verwendende Symbole in einem Tool erstellt werden müssen, das gekauft oder lizenziert wurde. Dies bedeutet, dass Testversionen nicht verwendet werden können.
-   Beide unten aufgeführten Produkte wurden von Designern verwendet, die Symbole für Windows Vista erstellt haben, und Sie bieten die Möglichkeit, in Adobe Photoshop CS zu exportieren.
    -   Gamani Gif Movie Gear: erzeugt eine ICO-Datei
    -   Axialis-Symbol Workshop:. ico-Datei wird erzeugt
-   Visual Studio unterstützt keine Windows Vista-Symbole (es gibt keine Unterstützung für Alphakanäle oder mehr als 256 Farben). Daher wird die Verwendung nicht empfohlen.
-   Symbol Dateien (. ico) müssen die 4-und 8-Bit-Versionen sowie die 24-Bit-und Alpha-Dateien enthalten.
-   Speichern Sie Dateien als "Windows-Symbol (. ico)", unabhängig davon, welches Programm für die Erstellung von Symbolen Sie verwenden möchten.
-   Bei einigen iconografischen Assets handelt es sich möglicherweise um bitmapstreifen, die ebenfalls einen Alphakanal erfordern (z. b. für Symbolleisten), oder PNG-Dateien, die mit Transparenz gespeichert werden. Nicht alle sind notwendigerweise das ICO-Format. Überprüfen Sie, welches Format im Code unterstützt wird.

**Schritt 6: auswerten**

-   Sehen Sie sich alle Größen an.
-   Sehen Sie sich die Familie an, um die Ähnlichkeit von Familien, den optischen Saldo und den Unterschied zu bewerten.
-   Betrachten Sie den Kontext, um relative Gewichtungen und Sichtbarkeit auszuwerten (stellen Sie sicher, dass eine solche nicht dominieren).
-   Fälle, die möglicherweise nicht verwendet werden, aber in naher Zukunft auftreten können. Kann dieses Symbol jemals kommentiert werden oder eine Überlagerung aufweisen?
-   Suchen Sie im Code.

### <a name="icons-in-the-context-of-list-views-toolbars-and-tree-views"></a>Symbole im Kontext von Listenansichten, Symbolleisten und Struktur Ansichten

**Listenansichten**

-   Verwenden Sie für Windows Vista Miniaturansichten für Dateien mit Inhalten, die sich in geringem Umfang visuell unterscheiden, sodass Benutzer die gesuchte Datei direkt erkennen können. (Verwenden Sie hierfür die Anwendungsprogrammierschnittstelle Windows Thumbnailing.)

    ![Screenshot von Windows-Explorer mit Ordner Symbolen ](images/vis-icons-image22.png)

-   Anwendungssymbol Überlagerungen (hier nicht dargestellt) bei Miniaturansichten helfen bei der Zuordnung mit der Anwendung für den Dateityp, zusätzlich zum Anzeigen der Vorschau der Datei.

**Hinweis:** Verwenden Sie für Dateien ohne visuell unterschiedlichen Inhalt keine Miniaturansichten. Verwenden Sie stattdessen herkömmliche Symbole für symbolische Dateien, die die Objektdarstellung und die zugeordnete Anwendung oder den zugehörigen Typ darstellen.

**Symbolleisten**

-   Symbole, die in einer Symbolleiste angezeigt werden, müssen über einen optischen Saldo in Größe, Farbe und Komplexität verfügen.
-   Testen potenzieller Symbole in einem kontextbezogenen Screenshot, um unerwünschte Dominanz oder Ungleichgewichte zu vermeiden.
-   Tests in Bildschirmfotos erleichtern die Vermeidung kostspieliger Iterationen im Code.
-   Überprüfen Sie auch die Symbole im Code. Bewegung und andere Faktoren können sich auf den Erfolg eines Symbols auswirken. in einigen Fällen sind möglicherweise weitere Iterationen erforderlich.

![Screenshot der Symbolleiste mit kleinen Symbolen und Bezeichnungen ](images/vis-icons-image23.png)

Im obigen Beispiel wurde das optische Guthaben noch nicht erreicht.

![Abbildung von Symbolen auf unterschiedlichen Hintergründen ](images/vis-icons-image24.png)

Iterationen im Kontext testen.

**Strukturansichten**

-   Ein optischer Saldo ist erforderlich, um die Hierarchie in einem Strukturansicht-Steuerelement beizubehalten.
-   Daher sollten Symbole, die normalerweise in diesem Kontext verwendet werden, dort ausgewertet werden. Manchmal sollte ein bestimmtes 16x16-Symbol kleiner gemacht werden, da seine Form eine optische Dominanz gegenüber anderen hat.
-   Die Kompensierung für optische Ungleichgewichte ist ein wichtiger Bestandteil der Erstellung von Symbolen höchster Qualität.

![Abbildung von zwei Gruppen von Ordnern in der Strukturansicht ](images/vis-icons-image25.png)

 

