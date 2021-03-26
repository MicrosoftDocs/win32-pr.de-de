---
description: Sie können eine eindeutige Eigenschaften Liste für Inhalts Ansichten und ein Layoutmuster für den Dateityp oder das Element registrieren.
ms.assetid: EA5A3ADA-4DFD-4F85-A176-93577D822815
title: Registriert einen Inhalts Ansichts Satz von Eigenschaften und layoutmustern für einen Dateityp oder ein Element.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13e84861a0761f2f5ebb9737f62409c8f72e00bd
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104350799"
---
# <a name="how-to-register-a-unique-content-view-set-of-properties-and-layout-pattern-for-the-file-type-or-item"></a>Registrieren eines eindeutigen Inhalts Ansichts Satzes von Eigenschaften und eines Layoutmusters für den Dateityp oder das Element

Sie können eine eindeutige Eigenschaften Liste für Inhalts Ansichten und ein Layoutmuster für den Dateityp oder das Element registrieren. Wenn Ihr Dateityp oder ein Element auch einer Art zugeordnet ist, überschreibt die Registrierung für die jeweilige Inhaltsansicht des Dateityps oder-Elements die Kind-Registrierung. Dies kann hilfreich sein, wenn sich die wichtigsten Eigenschaften für dieses Element von anderen Elementen derselben Art unterscheiden. Wenn Sie den Dateityp oder das Element nicht einem Elementtyp zuordnen oder die Inhaltsansicht direkt registrieren, verwendet das System die Standardinformationen der Inhaltsansicht (die in einem Registrierungsschlüssel gespeichert sind, auf den das letzte Element im Zuordnungs Array der Elemente, HKEY \_ Classes \_ root \\ \* ) folgt.

Bevor Sie eine benutzerdefinierte Eigenschaften Liste für Ihren Dateityp registrieren, sollten Sie sich mit dem Suchergebnis Modus und dem Suchmodus sowie den layoutmustern vertraut machen, die Ihnen zur Verfügung stehen.

## <a name="instructions"></a>Instructions

### <a name="step-1-understanding-the-search-result-mode-and-browse-mode"></a>Schritt 1: Grundlegendes zum Suchergebnis Modus und Durchsuchen-Modus

Die Inhaltsansicht erfordert das Definieren eines Layoutmusters und eines Satzes von Eigenschaften Listen für ein Element in einem Satz von Suchergebnissen (Suchergebnis Modus) und beim Durchsuchen eines shellorts (Durchsuchen-Modus). Sie können dieselben Werte für das Suchergebnis verwenden und wie durchsuchen `Kind.Music` . Alternativ dazu können Sie auch eine andere Eigenschaften Liste und/oder ein anderes Layoutmuster definieren `Kind.Document` .

Im Fall von `Kind.Document` Suchen Benutzer häufig nach Wörtern im Text des Dokuments. Daher ist das Einschließen von mehr Beispiel Text in das Suchergebnis möglicherweise die beste Wahl. Im folgenden Beispiel wird die Ansicht Inhalt Durchsuchen von veranschaulicht `Kind.Document` .

![Durchsuchen der Inhaltsansicht von kind.docUmschlag](images/content-view/browsecontentviewkinddocument.png)

Da Benutzer beim Durchsuchen von Dokumenten nur selten nach einem bestimmten Text suchen, ist die Optimierung der Auswahl von Eigenschaften und des Layouts für mehr Suchergebnisse auf dem Bildschirm möglicherweise die beste Wahl. Der folgende Screenshot veranschaulicht die Such Inhaltsansicht von `Kind.Document` .

### <a name="step-2-understanding-layout-patterns"></a>Schritt 2: Grundlegendes zu layoutmustern

Es gibt vier Layoutmuster: Alpha, Beta, Gamma und Delta.

**Alpha Layout**

Das Alpha-Layoutmuster ist für Dokument Suchergebnisse optimiert, die Ausschnitte enthalten. Es verfügt über die folgenden Spezifikationen:

-   Zeilen: 4
-   Eigenschaften: 7
-   Alpha Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.

    ![Alpha-Layoutmuster](images/content-view/layout1.png)

-   In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.

    ![Diagramm mit einem Alpha Layoutbeispiel](images/content-view/alphaviewmore.png)

-   In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element weniger als 350 Pixel horizontalen Leerraum aufweist.

    ![Screenshot, der ein Alpha-Layoutbeispiel in Microsoft Word zeigt.](images/content-view/layout2.png)

-   In der folgenden Abbildung ist das Alpha-Layout dargestellt, wenn das Element weniger als 350 Pixel horizontalen Leerraum aufweist.

    ![Alpha Layout-Beispiel](images/content-view/alphaviewless.png)

**Beta-Layout**

Das Beta-Layoutmuster ist für e-Mail-Dokument Suchergebnisse optimiert, die Auszüge enthalten. Es verfügt über die folgenden Spezifikationen:

-   Zeilen: 4
-   Eigenschaften: 5
-   Das Beta Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.

    ![Das Diagramm zeigt ein Beispiel für ein Beta Layout.](images/content-view/layout3.png)

-   Die folgende Abbildung zeigt das Beta Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.

    ![Screenshot, der ein Beta-Layoutbeispiel für e-Mail anzeigt.](images/content-view/betaviewmore.png)

-   Die folgende Abbildung zeigt das Beta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.

    ![Das Diagramm zeigt ein Beispiel für einen Beta-Layout mit weniger als 350 Pixeln horizontaler Leerraum.](images/content-view/layout4.png)

-   Die folgende Abbildung zeigt das Beta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt:

    ![Beispiel für das Beta Layout](images/content-view/betaviewless.png)

**Gamma Layout**

Das Gamma Layout-Muster ähnelt Alpha, verwendet aber ein zweizeilige Layout anstelle von vier. Dieses Layout eignet sich ideal für Szenarien, in denen Sie einen Ausschnitt sehen möchten, aber mehr Elemente auf dem Bildschirm anpassen möchten, oder für Dateitypen, die weniger Speicherplatz benötigen, um die kritischsten Informationen anzuzeigen. Das Gamma Layout verfügt über die folgenden Spezifikationen:

-   Zeilen: 2
-   Eigenschaften: 4
-   Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.

    ![Diagramm, das ein Beispiel für ein Gamma Layout anzeigt.](images/content-view/layout5.png)

-   Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über 350 Pixel oder mehr horizontalen Leerraum verfügt.

    ![Screenshot, der ein Gamma Layout-Beispiel für ein Prüfliste-Element zeigt.](images/content-view/gammaviewmore.png)

-   Die folgende Abbildung zeigt das Gamma Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.

    ![Das Diagramm zeigt ein Beispiel für ein Gamma Layout mit weniger als 350 Pixeln horizontaler Leerraum.](images/content-view/layout6.png)

-   Beispiel für das Gamma Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.

    ![Beispiel für Gamma Layout](images/content-view/gammaviewless.png)

**Delta Layout**

Das Delta Layoutmuster ist für die Anzeige zahlreicher kürzerer Eigenschaften wie z. b. für Musik und Bilder optimiert. Es verfügt über die folgenden Spezifikationen:

-   Zeilen: 2
-   Eigenschaften: 6
-   Delta Layout, wenn das Element über 700 Pixel oder mehr horizontalen Leerraum verfügt, wie in der folgenden Abbildung dargestellt.

    ![Diagramm, das ein Delta Layoutbeispiel zeigt.](images/content-view/layout7.png)

-   Beispiel für das Delta Layout, wenn das Element über 700 Pixel oder mehr horizontalen Leerraum verfügt.

    ![Screenshot, der ein Delta Layout-Beispiel für eine Musikdatei zeigt.](images/content-view/deltalayoutmore.png)

-   Delta Layout, wenn das Element zwischen 350 und 700 Pixel horizontalen Leerraum aufweist.

    ![Diagramm, das ein Delta Layoutbeispiel anzeigt, das zwischen 350 und 700 Pixel horizontalen Leerraum enthält.](images/content-view/layout8.png)

-   Beispiel für das Delta Layout, wenn das Element zwischen 350 und 700 Pixel horizontalen Leerraum liegt.

    ![Beispiel für Delta Layout](images/content-view/deltaviewbetween.png)

-   Delta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.

    ![Layoutbeispiel](images/content-view/layout9.png)

-   Beispiel für das Delta Layout, wenn das Element über weniger als 350 Pixel horizontalen Leerraum verfügt.

    ![Screenshot, der ein Delta Layoutbeispiel für eine Musikdatei mit weniger als 350 Pixeln horizontaler Leerraum zeigt.](images/content-view/deltaviewless.png)

### <a name="step-3-registering-custom-properties-and-layout-for-your-file-type"></a>Schritt 3: Registrieren von benutzerdefinierten Eigenschaften und Layout für Ihren Dateityp

Nachdem Sie den Suchergebnis Modus, den Durchsuchenmodus und die Layoutmuster verstanden haben, können Sie eine benutzerdefinierte Eigenschaften Liste für den Dateityp registrieren.

**, Um eine benutzerdefinierte Eigenschaften Liste und ein Layoutmuster für den Dateityp zu registrieren.**

1.  Wählen Sie aus den vier layoutmustern: Alpha, Beta, Gamma oder Delta.
2.  Berücksichtigen Sie die folgenden Formatierungs Regeln, die gleichermaßen für alle vier Layoutmuster gelten:
    -   Eigenschaft 1 wird immer in einer größeren Schriftgröße angezeigt. Der Umfang der großen Schriftart, der in der Regel für den Elementnamen verwendet wird, aber auch für den Anker oder eine andere Element Eigenschaft verwendet werden kann.
    -   Eigenschaft 4 ist für Ausschnitte in den Alpha-, Beta-und Gamma layoutmustern vorgesehen. Dieser Eigenschaft wird mehr Platz in diesen Mustern zugewiesen, und Sie wird in einer grauen Schriftfarbe angezeigt, im Gegensatz zu den anderen Eigenschaften, um Sie zu unterstützen.
    -   Die unten angegebenen Pixel Messungen liegen in relativen Pixeln vor, und die Größe enthält das Symbol/die Miniaturansicht links neben den Eigenschaften und das Leerzeichen zwischen Symbol/Miniaturansicht und Auswahl Rechteck.
    -   Die meisten Eigenschaften verfügen über eine minimale Anzeige Größe. Aus diesem Grund werden Sie nicht angezeigt, wenn auf einer bestimmten Ansichts Größe nicht genügend Speicherplatz vorhanden ist. Die minimale Größe ist normalerweise 100 Pixel breit.
    -   Jedes Layoutmuster definiert die Anzahl der Zeilen und die Anzahl der Eigenschaften in jeder Zeile.
3.  Entscheiden Sie, welche Eigenschaften im Layout angezeigt werden sollen und welche Eigenschaft Sie an jedem Speicherort anzeigen möchten. Berücksichtigen Sie bei der Entscheidung, welche Eigenschaft an jeder Position im Layout angezeigt werden soll, die typische Länge der Eigenschaft, ihre Wichtigkeit für den Benutzer und ob Sie gelöscht werden soll, wenn die Fenstergröße zu klein ist, um alle Eigenschaften zu enthalten.
4.  Registrieren Sie ein Layoutmuster und eine Eigenschaften Liste für Ihren Dateityp oder Elementtyp, indem Sie die folgenden Schlüssel unter dem ProgID-Registrierungsschlüssel für den Dateityp oder das Element hinzufügen (in diesem Beispiel für den Dateityp ". xyz").

    ```
    HKEY_CLASSES_ROOT\*
       Contoso.xyzfile
          (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
          (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
          (ContentViewModeLayoutPatternForSearch) = <PropertyList>
    ```

5.  Beachten Sie die folgenden Formatierungs Richtlinien zum Registrieren von Eigenschaften:

    -   Jede Registrierung beginnt mit `prop:`
    -   Jede Eigenschaft erfordert den vollständigen Eigenschaftsnamen.
    -   Eigenschaften werden durch ein Semikolon ohne Leerzeichen voneinander getrennt.
    -   Eigenschaften werden in der Reihenfolge angezeigt, in der das ausgewählte Layoutmuster definiert ist.
    -   `~` Gibt an, dass die Eigenschaften Bezeichnung nicht angezeigt werden soll.
    -   `~System.LayoutPattern.PlaceHolder` sollte verwendet werden, wenn Sie eine im Layoutmuster angegebene Eigenschaft leer lassen möchten.

    Der folgende Beispiel Registrierungsschlüssel veranschaulicht diese Formatierungs Richtlinien.

    ```
    HKEY_CLASSES_ROOT\
       Kind.Document
          (ContentViewModeForBrowse) = <PropertyList>
    ```

    Mögliche Werte für (contentviewmodeforbrowse) umfassen Folgendes: Prop: ~ System. itemnamedisplay; System. Author; System. layoutpattern. Platzhalter; System. Keywords; System. DateModified; ~ System. Size

## <a name="remarks"></a>Bemerkungen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dateitypen](fa-file-types.md)
</dt> <dt>

[Kind-Namen](../properties/building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[System. proplist. contentviewmodeforbrowse](../properties/props-system-proplist-contentviewmodeforbrowse.md)
</dt> <dt>

[System. proplist. contentviewmodeforsearch](../properties/props-system-proplist-contentviewmodeforsearch.md)
</dt> </dl>

 

 
