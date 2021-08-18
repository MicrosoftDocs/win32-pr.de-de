---
description: Die Ink-Sammlung beginnt mit dem Digitizer.
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

Die Ink-Sammlung beginnt mit dem Digitizer. Ein Benutzer platziert einen Stift auf dem Digitizer und beginnt mit dem Schreiben. Sie können die Funktionen der Ink-Sammlung der API verwenden, um die Sammlung von Ink-Daten zu verwalten, die aus dem Stift "fließen". Sie haben über die Tablets-Sammlung und [](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) das Tablet-Objekt Zugriff auf Informationen zur verfügbaren [**Hardware auf dem Tablet-PC.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Anschließend verwenden Sie das [**InkCollector-Objekt,**](inkcollector-class.md) um die Daten zu erhalten, die vom Digitizer stammen.

## <a name="tablets-and-the-tablet-object"></a>Tablets und das Tablet-Objekt

Ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) stellt ein Digitizergerät von Tablet PC dar. Ein Tablet-PC kann über mehrere Digitizer verfügen. Mithilfe **des Tablet-Objekts** können Sie die verfügbaren Digitizergeräte abfragen, die an den Tablet-PC angeschlossen sind, und deren jeweilige Hardwarefunktionen. Beispielsweise können Sie ermitteln, ob das **Tablet,** mit dem Sie arbeiten, in die Anzeige integriert ist oder ein separates externes Gerät ist.

## <a name="inkcollector-object"></a>InkCollector-Objekt

Das [**InkCollector-Objekt**](inkcollector-class.md) erfasst Freieingaben von verfügbaren [**Tablet-Geräten.**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) Das **InkCollector-Objekt** erfasst nur Ink- und Gesten, die in ein bestimmtes Fenster eingegeben werden. Eine sehr effiziente Ereignissenke rendert diese Eingabe in Echtzeit. Das **InkCollector-Objekt** erfasst die Eingabe und leitet sie an ein [**Ink-Objekt**](inkdisp-class.md) weiter.

> [!Note]  
> Das gleichzeitige Auflegen von Ink mit mehreren Stiften funktioniert abhängig von den Hardwarefunktionen des Digitizergeräts möglicherweise nicht.

 

### <a name="how-the-ink-collector-works"></a>Funktionsweise des Ink Collector

Das [**InkCollector-Objekt**](inkcollector-class.md) wird an ein bekanntes Anwendungsfenster angefügt. Anschließend können Benutzer ein beliebiges verfügbares Tablet PC-Gerät (einschließlich der Maus) verwenden, um frei in Echtzeit in diesem Fenster zu erstellen. Die erfassten Ink-Striche werden in einem zugeordneten [**Ink-Objekt**](inkdisp-class.md) gespeichert. Diese Striche können dann bearbeitet oder zur Erkennung an eine Erkennung gesendet werden. Das **InkCollector-Objekt** benachrichtigt die Anwendung auch, wenn ein Cursor in den Bereich eines der verwendeten Tablet PC-Geräte gerät.

Damit das [**InkCollector-Objekt**](inkcollector-class.md) den Mauscursor innerhalb eines ink-fähigen Fensters genau festlegen kann, muss dieses Fenster in der Lage sein, die **WM \_ SETCURSOR-Nachricht zu** empfangen. Dies ist für alle regulären Fenster erfolgreich, aber für ein Steuerelement in einem Dialogfeld filtert das übergeordnete Dialogfeld des Steuerelements diese Meldung. Damit das Steuerelement die Nachricht empfangen kann, legen Sie den **Stil SS \_ NOTIFY** fest.

## <a name="inkoverlay-object"></a>InkOverlay-Objekt

Das [**zuvor erläuterte InkCollector-Objekt**](inkcollector-class.md) ist nützlich für Anwendungen, um ein eigenes Modell zum Auswählen, Löschen und anderen Benutzerinteraktionen zur Verfügung zu stellen. Das [**InkOverlay-Objekt**](inkoverlay-class.md) ist eine Obermenge des **InkCollector-Objekts,** das Bearbeitungsunterstützung bietet. Dies ist nützlich für Anwendungen, um das Zeichnen und Bearbeiten von Ink-Zeichen in ihren eigenen Dokumentbereich zu integrieren, indem eine Reihe von Standard-Ink-Auswahlmodellen verwendet wird, die das -Objekt bietet.

Sowohl das [**InkCollector-Objekt**](inkcollector-class.md) als auch das [**InkOverlay-Objekt**](inkoverlay-class.md) (sowie das InkPicture-Steuerelement) verwenden allgemeine Konstrukte wie das [**Ink-Objekt**](inkdisp-class.md) und die [**DrawingAttributes-Auflistung,**](inkdrawingattributes-class.md) sodass die grundlegende Methode zum Ändern der Farbe der [InkPicture](inkpicture-control.md) überall gleich ist. Dadurch können Sie Code wiederverwenden und über allgemeinen programmgesteuerten Zugriff verfügen. Dies kann besonders wichtig sein, wenn Sie Skriptunterstützung in Ihrer Anwendung anbieten.

[**InkOverlay**](inkoverlay-class.md) ist ein COM-Objekt, das für Anmerkungsszenarien nützlich ist, in denen Benutzer keine Erkennung für Ink durchführen möchten, sondern stattdessen an Größe, Form, Farbe und Position der Ink interessiert sind. Sie eignet sich gut für Notizen und einfaches Abknausen. Die Standardbenutzeroberfläche ist ein transparentes Rechteck mit nicht transparenten Ink-Daten.

[**InkOverlay erweitert**](inkoverlay-class.md) die [**InkCollector-Klasse**](inkcollector-class.md) auf drei Arten:

-   Sie löst Ereignisse für Änderungen des Begin-Stroke-, Endstrich- und Ink-Attributs aus.
-   Sie ermöglicht Benutzern das Auswählen, Löschen und Ändern der Größe von Ink.
-   Die Befehle Ausschneiden, Kopieren und Einfügen werden unterstützt.

Ein typisches Szenario, in [**dem InkOverlay**](inkoverlay-class.md) nützlich ist, ist das Markieren einer Präsentationsfolie oder eines Bilds. Das **InkOverlay-Objekt** ermöglicht eine einfache Implementierung der Fürk- und Layoutfunktionen, die für dieses Szenario erforderlich sind.

Um mit [**InkOverlay zu arbeiten,**](inkoverlay-class.md)führen Sie Dies aus:

1.  Instanziieren Sie ein [**InkOverlay-Objekt.**](inkoverlay-class.md)
2.  Fügen Sie den hWnd (Handle, in verwaltetem Code) eines Fensters an die [**hWnd-Eigenschaft**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) des [**InkOverlay-Objekts**](inkoverlay-class.md) an ([Handle-Eigenschaft](/previous-versions/ms582171(v=vs.100)) in verwaltetem Code).
3.  Legen Sie die Enabled-Eigenschaft [](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) des [**InkOverlay-Objekts**](inkoverlay-class.md) auf TRUE **fest.**

Das [**InkOverlay-Objekt**](inkoverlay-class.md) enthält grundlegende Druckunterstützung, aber Sie müssen die Druckvorschau oder andere erweiterte Druckfunktionen implementieren.

[**InkOverlay bleibt**](inkoverlay-class.md) im ink serialisierten Format (ISF) erhalten.

> [!Note]  
> Wenn [**editingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) des [**InkOverlay-Objekts**](inkoverlay-class.md)  auf Delete oder **Select** festgelegt ist, werden andere Ereignisse ausgelöst (z.B. [**InkAdded,**](inkdisp-inkadded.md) [**InkDeleted**](inkdisp-inkdeleted.md)und [**Stroke).**](inkoverlay-stroke.md) Diese Ereignisse sind nützlich, wenn Sie Ihre eigenen Lösch- oder Auswahlmodi implementieren möchten.

 

### <a name="selecting-ink"></a>Auswählen von Ink

Mit [**dem InkOverlay-Objekt**](inkoverlay-class.md) können Benutzer mithilfe eines lasso-Tools Ink-Objekte auswählen, die in einem ablaufverfolgungsierten Bereich enthalten sind. Benutzer können auch Ink auswählen, indem sie auf ein [**beliebiges Ink-Objekt**](inkdisp-class.md) tippen.

Verwenden Sie [**die Selection-Eigenschaft,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) um eine [**Strokes-Auflistung**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) zurück, mit der Sie die Auswahl eines Benutzers bearbeiten können.

Wenn ein [**Ink-Objekt**](inkdisp-class.md) oder eine Reihe von **Ink-Objekten** ausgewählt ist, werden Größenziehpunkte an den vier Ecken des Begrenzungsfelds der Ink und an allen Mittelpunkten zwischen angrenzenden Ecken angezeigt. Wenn der Benutzer eine beliebige Stelle innerhalb des ausgewählten Bereich zieht, wird die Ink innerhalb des Steuerelements verschiebbar.

### <a name="default-behavior"></a>Standardverhalten

Das [**InkOverlay-Objekt**](inkoverlay-class.md) ist standardmäßig auf die Erfassung von Ink festgelegt. Ink ist 53 Freiraumeinheiten breit (wobei 1 Freiraumeinheit = 1 HIMETRIC ist). Die Ink-Farbe ist schwarz, wenn der Benutzer nicht im Modus mit hohem Kontrast ausgeführt wird. Andernfalls wird ink auf den **COLOR \_ WINDOWTEXT-Wert** (**WindowText** in verwaltetem Code) festgelegt. [**FitToCurve ist**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) **FALSE.**

### <a name="cursor-and-button-objects"></a>Cursor- und Schaltflächenobjekte

Ein Cursor entspricht der Spitze des Stifts, der auf dem Tablet PC verwendet wird. Ein Stift hat beispielsweise zwei Enden. In der Regel wird ein Ende zum Schreiben und das andere für das Löschen verwendet. Diese beiden Enden entsprechen zwei Cursorn. Die [**Cursor-Klasse**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) ist nicht mit [**System.Windows. Forms.Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1).

Auf einem Tablet-PC ist ein Cursor in der Regel so definiert, dass er entweder zum Schreiben oder Löschen verwendet wird. Ein Cursor kann die Rollen möglicherweise ändern, wenn die Anwendung diese Funktionalität aktiviert. Einige Tablet PC-Geräte lassen mehrere Stifte zu. Jeder Cursor verfügt über eine zugeordnete Cursor-ID, die im System eindeutig ist. Einem Cursor können null oder mehr Schaltflächen zugeordnet sein. Diese Schaltflächen werden der Anwendung als CursorButton-Objekte bereitgestellt. Die Anwendung kann ein [**bestimmtes DrawingAttributes-Objekt**](inkdrawingattributes-class.md) für jeden angegebenen Cursor bereitstellen.

### <a name="drawing-attributes-object"></a>Drawing Attributes-Objekt

Ein [**DrawingAttributes-Objekt**](inkdrawingattributes-class.md) beschreibt, wie ein bekannter Satz von Ink gezeichnet werden soll. Ein **DrawingAttributes-Objekt** enthält grundlegende Eigenschaften wie [**Color,**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color) [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)und [**PenTip.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip) Sie kann auch erweiterte Parameter wie variable Transparenz und Bézierglättung umfassen, die interessante Effekte bieten oder die Lesbarkeit von Ink verbessern können.

### <a name="peninputpanel-object"></a>PenInputPanel-Objekt

> [!Note]  
> Die [**PenInputPanel-Klasse**](peninputpanel-class.md) ist veraltet. Die **PenInputPanel-Klasse** wurde durch die [**TextInputPanel-Klasse**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) ersetzt.

 

Mit [**dem PenInputPanel-Objekt**](peninputpanel-class.md) können Sie Ihren Anwendungen ganz einfach eingaben. **PenInputPanel ist** als anfingbares Objekt verfügbar, mit dem Sie vorhandenen Steuerelementen Tablet PC Input Panel-Funktionen hinzufügen können. Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabesprache beauftragt. Sie haben die Möglichkeit, die Standardeingabemethode für **das PenInputPanel-Steuerelement**(Handschrift oder Tastatur) zu wählen. Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkCollector-Klasse (C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay-Klasse (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Microsoft.Ink-Namespace**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
