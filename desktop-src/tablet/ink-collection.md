---
description: Die Auflistung von Ink beginnt mit dem Digitizer.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Ink-Sammlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e45988ea93aac5016391e22c352b9d0123a5e122f4a79c55e41e06834ed040e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452066"
---
# <a name="ink-collection"></a>Ink-Sammlung

Die Auflistung von Ink beginnt mit dem Digitizer. Ein Benutzer platziert einen Stift auf dem Digitizer und beginnt mit dem Schreiben. Sie können die Ink-Sammlungsfeatures der API verwenden, um die Sammlung von Ink-Daten zu verwalten, die aus dem Stift "fließen". Sie haben Über die [**Tablets-Sammlung**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) und das [**Tablet-Objekt**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Zugriff auf Informationen zur verfügbaren Hardware auf dem Tablet-PC. Anschließend verwenden Sie das [**InkCollector-Objekt,**](inkcollector-class.md) um die Daten abzurufen, die vom Digitizer stammen.

## <a name="tablets-and-the-tablet-object"></a>Tablets und das Tablet-Objekt

Ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) stellt ein Digitizergerät von Tablet PC dar. Ein Tablet-PC kann über mehrere Digitizer verfügen. Mithilfe des **Tablet-Objekts** können Sie die verfügbaren Digitizergeräte abfragen, die an den Tablet PC und die jeweiligen Hardwarefunktionen angefügt sind. Beispielsweise können Sie ermitteln, ob das **Tablet,** mit dem Sie arbeiten, in die Anzeige integriert ist oder ein separates externes Gerät ist.

## <a name="inkcollector-object"></a>InkCollector-Objekt

Das [**InkCollector-Objekt**](inkcollector-class.md) erfasst Freihandeingaben von verfügbaren [**Tablet-Geräten.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Das **InkCollector-Objekt** erfasst nur Ink- und Gesten, die in ein bestimmtes Fenster eingegeben werden. Eine sehr effiziente Ereignissenke rendert diese Eingabe in Echtzeit. Das **InkCollector-Objekt** erfasst die Eingabe und leitet sie an ein [**Ink-Objekt**](inkdisp-class.md) weiter.

> [!Note]  
> Die gleichzeitige Verlegung von Ink mit mehreren Stiften funktioniert abhängig von den Hardwarefunktionen des Digitizergeräts möglicherweise oder nicht.

 

### <a name="how-the-ink-collector-works"></a>Funktionsweise des Ink-Collectors

Das [**InkCollector-Objekt**](inkcollector-class.md) fügt sich an ein bekanntes Anwendungsfenster an. Anschließend können Benutzer jedes verfügbare Tablet PC-Gerät (einschließlich der Maus) verwenden, um Freihand in Echtzeit in diesem Fenster zu legen. Die erfassten Ink-Striche werden in einem zugeordneten [**Ink-Objekt**](inkdisp-class.md) gespeichert. Diese Striche können dann bearbeitet oder zur Erkennung an eine Erkennung gesendet werden. Das **InkCollector-Objekt** benachrichtigt die Anwendung auch, wenn ein Cursor in den Bereich eines der verwendeten Tablet PC-Geräte gelangt.

Damit das [**InkCollector-Objekt**](inkcollector-class.md) den Mauszeiger innerhalb eines ink-fähigen Fensters genau festlegen kann, muss dieses Fenster in der Lage sein, die **WM \_ SETCURSOR-Meldung** zu empfangen. Dies ist für alle regulären Fenster erfolgreich, aber für ein Steuerelement innerhalb eines Dialogfelds filtert das übergeordnete Dialogfeld des Steuerelements diese Meldung. Damit das Steuerelement die Nachricht empfangen kann, legen Sie den **SS \_ NOTIFY-Stil** fest.

## <a name="inkoverlay-object"></a>InkOverlay-Objekt

Das zuvor [**erläuterte InkCollector-Objekt**](inkcollector-class.md) ist für Anwendungen nützlich, um ein eigenes Modell für die Auswahl, Löschung und andere Benutzerinteraktion bereitzustellen. Das [**InkOverlay-Objekt**](inkoverlay-class.md) ist eine Obermenge des **InkCollector-Objekts,** das Bearbeitungsunterstützung bereitstellt. Dies ist nützlich für Anwendungen, um Das Zeichnen und Bearbeiten von Ink in ihren eigenen Dokumentzeichenbereich zu integrieren, indem ein Satz von Standard-Ink-Auswahlmodellen verwendet wird, die das -Objekt bereitstellt.

Sowohl das [**InkCollector-Objekt**](inkcollector-class.md) als auch das [**InkOverlay-Objekt**](inkoverlay-class.md) (sowie das [InkPicture-Steuerelement)](inkpicture-control.md) verwenden allgemeine Konstrukte wie das [**Freihandobjekt**](inkdisp-class.md) und die [**DrawingAttributes-Auflistung, sodass**](inkdrawingattributes-class.md) die grundlegende Methode zum Ändern der Farbe von Freihand überall gleich ist. Dadurch können Sie Code wiederverwenden und über gemeinsamen programmgesteuerten Zugriff verfügen. Dies kann besonders wichtig sein, wenn Sie Skriptunterstützung in Ihrer Anwendung anbieten.

[**InkOverlay**](inkoverlay-class.md) ist ein COM-Objekt, das für Anmerkungsszenarien nützlich ist, in denen Es benutzern nicht darum geht, Freihanderkennung durchzuführen, sondern stattdessen die Größe, Form, Farbe und Position der Freihand. Es eignet sich gut für Notizen und einfaches Scribbling. Die Standardbenutzerschnittstelle ist ein transparentes Rechteck mit nicht transparentem Ink.

[**InkOverlay**](inkoverlay-class.md) erweitert die [**InkCollector-Klasse**](inkcollector-class.md) auf drei Arten:

-   Es löst Ereignisse für Änderungen des Begin-Stroke-, End-Stroke- und Ink-Attributs aus.
-   Sie ermöglicht Benutzern das Auswählen, Löschen und Ändern der Größe von Ink.
-   Die Befehle Ausschneiden, Kopieren und Einfügen werden unterstützt.

Ein typisches Szenario, in dem [**InkOverlay**](inkoverlay-class.md) nützlich ist, ist das Markieren einer Präsentationsfolie oder eines Bilds. Das **InkOverlay-Objekt** ermöglicht eine einfache Implementierung der Ink- und Layoutfunktionen, die für dieses Szenario erforderlich sind.

Um mit [**InkOverlay**](inkoverlay-class.md)zu arbeiten, müssen Sie:

1.  Instanziieren Sie ein [**InkOverlay-Objekt.**](inkoverlay-class.md)
2.  Fügen Sie den hWnd (Handle in verwaltetem Code) eines Fensters an die [**hWnd-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) des [**InkOverlay-Objekts**](inkoverlay-class.md) an ([Handle-Eigenschaft,](/previous-versions/ms582171(v=vs.100)) in verwaltetem Code).
3.  Legen Sie die [**Enabled-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) des [**InkOverlay-Objekts**](inkoverlay-class.md) auf **TRUE** fest.

Das [**InkOverlay-Objekt**](inkoverlay-class.md) enthält grundlegende Druckunterstützung, sie müssen jedoch die Druckvorschau oder andere erweiterte Druckfunktionen implementieren.

[**InkOverlay**](inkoverlay-class.md) bleibt ink im ink serialisierten Format (ISF) erhalten.

> [!Note]  
> Wenn [**editingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) des [**InkOverlay-Objekts**](inkoverlay-class.md) auf **Löschen** oder **Auswählen** festgelegt ist, werden andere Ereignisse (z. B. [**InkAdded,**](inkdisp-inkadded.md) [**InkDeleted**](inkdisp-inkdeleted.md)und [**Stroke)**](inkoverlay-stroke.md)ausgelöst. Diese Ereignisse sind nützlich, wenn Sie Ihren eigenen Lösch- oder Auswahlmodus implementieren möchten.

 

### <a name="selecting-ink"></a>Auswählen von "Ink"

Das [**InkOverlay-Objekt**](inkoverlay-class.md) ermöglicht Benutzern die Verwendung eines Lassotools, um Ink-Objekte auszuwählen, die in einem nachverfolgten Bereich enthalten sind. Benutzer können auch Ink auswählen, indem sie auf ein beliebiges [**Ink-Objekt**](inkdisp-class.md) tippen.

Verwenden Sie die [**Selection-Eigenschaft,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) um eine [**Strokes-Sammlung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) zurückzugeben, mit der Sie die Auswahl eines Benutzers bearbeiten können.

Wenn ein [**Ink-Objekt**](inkdisp-class.md) oder eine Gruppe von **Ink-Objekten** ausgewählt ist, werden Größenziehpunkte an den vier Ecken des umgebenden Felds der Ink und an allen Mittelpunkten zwischen benachbarten Ecken angezeigt. Wenn der Benutzer eine beliebige Stelle innerhalb des ausgewählten Bereichs zieht, wird die Ink innerhalb des Steuerelements verschiebbar.

### <a name="default-behavior"></a>Standardverhalten

Das [**InkOverlay-Objekt**](inkoverlay-class.md) ist standardmäßig auf die Erfassung von Ink festgelegt. Freihand ist 53 Freihandraumeinheiten breit (wobei 1 Freihandraumeinheit = 1 HIMETRIC ist). Ink ist schwarz, wenn der Benutzer nicht im Modus mit hohem Kontrast ausgeführt wird. Andernfalls wird ink auf den **COLOR \_ WINDOWTEXT-Wert** **(WindowText** in verwaltetem Code) festgelegt. [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) ist **FALSE.**

### <a name="cursor-and-button-objects"></a>Cursor- und Schaltflächenobjekte

Ein Cursor entspricht der Spitze des Stifts, der auf tablet PC verwendet wird. Beispielsweise hat ein Stift zwei Enden. In der Regel wird ein Ende zum Schreiben und das andere zum Löschen verwendet. Diese beiden Enden entsprechen zwei Cursorn. Die [**Cursor-Klasse**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) wird nicht mit [**System.Windows verwechselt. Forms.Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

Auf Tablet PC ist ein Cursor normalerweise so definiert, dass er zum Schreiben oder Löschen verwendet wird. Ein Cursor kann rollenverändern, wenn die Anwendung diese Funktionalität aktiviert. Einige Tablet PC-Geräte lassen mehrere Stifte zu. Jeder Cursor verfügt über eine zugeordnete Cursor-ID, die im System eindeutig ist. Einem Cursor können 0 (null) oder mehr Schaltflächen zugeordnet sein. Diese Schaltflächen werden der Anwendung als CursorButton-Objekte bereitgestellt. Die Anwendung kann ein [**bestimmtes DrawingAttributes-Objekt**](inkdrawingattributes-class.md) für jeden angegebenen Cursor bereitstellen.

### <a name="drawing-attributes-object"></a>Zeichnungsattribute-Objekt

Ein [**DrawingAttributes-Objekt**](inkdrawingattributes-class.md) beschreibt, wie jeder bekannte Satz von Ink gezeichnet werden soll. Ein **DrawingAttributes-Objekt** enthält grundlegende Eigenschaften wie [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)und [**PenTip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). Sie kann auch erweiterte Parameter wie variable Transparenz und Bézierglättung umfassen, die interessante Effekte bieten oder die Lesbarkeit von Ink verbessern können.

### <a name="peninputpanel-object"></a>PenInputPanel-Objekt

> [!Note]  
> Die [**PenInputPanel-Klasse**](peninputpanel-class.md) ist veraltet. Die **PenInputPanel-Klasse** wurde durch die [**TextInputPanel-Klasse**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ersetzt.

 

Mit dem [**PenInputPanel-Objekt**](peninputpanel-class.md) können Sie Ihren Anwendungen ganz einfach Stifteingaben hinzufügen. Das **PenInputPanel** ist als anfügebares Objekt verfügbar, mit dem Sie vorhandenen Steuerelementen Tablet PC Input Panel-Funktionen hinzufügen können. Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabesprache gefordert. Sie haben die Möglichkeit, die Standardeingabemethode für das **PenInputPanel** auszuwählen , entweder Handschrift oder Tastatur. Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkCollector-Klasse (C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay-Klasse (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Microsoft.Ink-Namespace**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
