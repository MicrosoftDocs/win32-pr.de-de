---
description: Die frei Hand Auflistung beginnt mit dem Digitalisierer.
ms.assetid: 95e49f5b-d6f0-4a5a-868b-aa0caf87c39c
title: Ink-Auflistung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fcd5bf0d73f48e63366843c85c9d6dd7cd388f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525307"
---
# <a name="ink-collection"></a>Ink-Auflistung

Die frei Hand Auflistung beginnt mit dem Digitalisierer. Ein Benutzer platziert einen Stift für den Digitalisierer und beginnt mit dem Schreiben. Mithilfe der frei Hand Sammlungs Funktionen der API können Sie die Sammlung von frei Hand Daten verwalten, die vom Stift "Flows" werden. Sie haben Zugriff auf Informationen zur verfügbaren Hardware auf Tablet PC über die [**Tablets**](/windows/desktop/api/msinkaut/nf-msinkaut-iinktablets-item) -Sammlung und das [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Objekt. Anschließend verwenden Sie das [**InkCollector**](inkcollector-class.md) -Objekt, um die Daten aus dem Digitalisierer zu erhalten.

## <a name="tablets-and-the-tablet-object"></a>Tablets und das Tablet-Objekt

Ein [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) stellt ein Digitalisierungsprogramm des Tablet PCs dar. Ein Tablet PC verfügt möglicherweise über mehr als einen Digitalisierer. Mithilfe des **Tablet** -Objekts können Sie die verfügbaren digitalisierergeräte Abfragen, die an Tablet PC angeschlossen sind, sowie die jeweiligen Hardwarefunktionen. Beispielsweise können Sie feststellen, ob das **Tablet** , mit dem Sie arbeiten, in die Anzeige integriert ist oder ob es sich um ein separates externes Gerät handelt.

## <a name="inkcollector-object"></a>InkCollector-Objekt

Das [**InkCollector**](inkcollector-class.md) -Objekt erfasst Freihand Eingaben von verfügbaren [**Tablet**](/windows/desktop/api/msinkaut/nn-msinkaut-iinktablet) -Geräten. Das **InkCollector** -Objekt sammelt nur frei Hand Eingaben und Gesten, die in ein bestimmtes Fenster eingegeben werden. Eine sehr effiziente Ereignis Senke rendert diese Eingabe in Echtzeit. Das **InkCollector** -Objekt erfasst die Eingabe und leitet Sie an ein [**Ink**](inkdisp-class.md) -Objekt weiter.

> [!Note]  
> Die gleichzeitige Einrichtung von frei Hand Eingaben mit mehreren stiften hängt von den Hardwarefunktionen des Digitalisierungsprogramms ab.

 

### <a name="how-the-ink-collector-works"></a>Funktionsweise des Ink Collector

Das [**InkCollector**](inkcollector-class.md) -Objekt wird an ein bekanntes Anwendungsfenster angefügt. Anschließend können Benutzer beliebige verfügbare Tablet PC-Geräte (einschließlich der Maus) verwenden, um frei Hand Eingaben in Echtzeit in diesem Fenster zu verwenden. Die gesammelten Hand Striche werden in einem zugeordneten [**Ink**](inkdisp-class.md) -Objekt gespeichert. Diese Striche können dann bearbeitet oder zur Erkennung an eine Erkennungsfunktion gesendet werden. Das **InkCollector** -Objekt benachrichtigt die Anwendung auch, wenn ein Cursor in den Bereich eines der verwendeten Tablet PC-Geräte fällt.

Damit das [**InkCollector**](inkcollector-class.md) -Objekt den Mauszeiger in einem frei Hand Eingabe fähigen Fenster exakt festlegen kann, muss das Fenster die WM- **\_ SetCursor** -Nachricht empfangen können. Dies ist für alle regulären Fenster erfolgreich, aber bei einem Steuerelement in einem Dialogfeld wird diese Meldung durch das übergeordnete Dialogfeld des Steuer Elements gefiltert. Damit das Steuerelement die Meldung empfängt, legen Sie den **SS- \_ Benachrichtigungs** Stil fest.

## <a name="inkoverlay-object"></a>InkOverlay-Objekt

Das zuvor beschriebene [**InkCollector**](inkcollector-class.md) -Objekt eignet sich für Anwendungen zum Bereitstellen eines eigenen Modells für das auswählen, löschen und andere Benutzerinteraktionen. Das [**InkOverlay**](inkoverlay-class.md) -Objekt ist eine supermenge des **InkCollector** -Objekts, das Bearbeitungs Unterstützung bereitstellt. Dies ist hilfreich, wenn Anwendungen das Zeichnen und Bearbeiten von Hand Eingaben in Ihre eigene Dokument Canvas integrieren möchten, indem Sie eine Reihe von standardmäßigen frei Handauswahl Modellen verwenden, die das Objekt bereitstellt.

Sowohl das [**InkCollector**](inkcollector-class.md) -Objekt als auch das [**InkOverlay**](inkoverlay-class.md) -Objekt (sowie das [InkPicture](inkpicture-control.md) -Steuerelement) verwenden allgemeine Konstrukte, wie z. b. das [**Ink**](inkdisp-class.md) -Objekt und die [**DrawingAttributes**](inkdrawingattributes-class.md) -Auflistung, sodass die grundlegende Methode zum Ändern der farbliche Ink-Methode überall gleich ist. Dies ermöglicht es Ihnen, Code wiederzuverwenden und allgemeinen programmgesteuerten Zugriff zu erhalten. Dies kann besonders wichtig sein, wenn Sie in Ihrer Anwendung Skriptunterstützung anbieten.

[**InkOverlay**](inkoverlay-class.md) ist ein COM-Objekt, das für Anmerkung-Szenarios nützlich ist, in denen Benutzer sich nicht mit der Erkennung von frei Hand Eingaben befassen, sondern vielmehr an der Größe, der Form, der Farbe und der Position der Handschrift interessiert sind. Sie eignet sich gut für Notizen und grundlegende scriberend. Die Standardbenutzer Oberfläche ist ein transparentes Rechteck mit undurchsichtigem frei Hand Eingaben.

[**InkOverlay**](inkoverlay-class.md) erweitert die [**InkCollector**](inkcollector-class.md) -Klasse auf drei Arten:

-   Es werden Ereignisse für die Änderungen am Anfang, am Ende des Strichs und an Ink-Attributen ausgelöst.
-   Er ermöglicht Benutzern das auswählen, löschen und Ändern der Größe von frei Hand Eingaben.
-   Sie unterstützt Befehle zum Ausschneiden, kopieren und einfügen.

Ein typisches Szenario, in dem [**InkOverlay**](inkoverlay-class.md) nützlich ist, ist das Markieren einer Präsentations Folie oder eines Bilds. Das **InkOverlay** -Objekt ermöglicht eine einfache Implementierung der frei Hand-und Layoutfunktionen, die für dieses Szenario erforderlich sind.

Wenn Sie mit [**InkOverlay**](inkoverlay-class.md)arbeiten möchten, können Sie Folgendes tun:

1.  Instanziieren Sie ein [**InkOverlay**](inkoverlay-class.md) -Objekt.
2.  Fügen Sie das HWND (handle, in verwaltetem Code) eines Fensters an die [**HWND**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_hwnd) -Eigenschaft des [**InkOverlay**](inkoverlay-class.md) -Objekts an ([handle](/previous-versions/ms582171(v=vs.100)) -Eigenschaft in verwaltetem Code).
3.  Legen Sie die [**aktivierte**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_enabled) Eigenschaft des [**InkOverlay**](inkoverlay-class.md) -Objekts auf " **true**" fest.

Das [**InkOverlay**](inkoverlay-class.md) -Objekt enthält grundlegende Druckunterstützung, aber Sie müssen die Druckvorschau oder andere erweiterte Druckfunktionen implementieren.

[**InkOverlay**](inkoverlay-class.md) speichert Frei Hand Eingaben im frei Hand Format (Ink serialisiert Format, ISF).

> [!Note]  
> Wenn die [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_editingmode) -Eigenschaft des [**InkOverlay**](inkoverlay-class.md) -Objekts auf **Delete** oder **Select** festgelegt ist, werden andere Ereignisse (z. b. [**InkAdded**](inkdisp-inkadded.md), [**InkDeleted**](inkdisp-inkdeleted.md)und [**Stroke**](inkoverlay-stroke.md)) ausgelöst. Diese Ereignisse sind nützlich, wenn Sie Ihre eigenen Lösch-oder SELECT-Modi implementieren möchten.

 

### <a name="selecting-ink"></a>Freihand auswählen

Das [**InkOverlay**](inkoverlay-class.md) -Objekt ermöglicht Benutzern die Verwendung eines Lassopfad-Tools, um frei Hand Objekte auszuwählen, die in einem nach verfolgten Bereich enthalten sind. Benutzer können auch Ink auswählen, indem Sie [**auf ein frei**](inkdisp-class.md) Hand Objekt tippen.

Verwenden Sie die [**Auswahl**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) Eigenschaft, um eine [**Striche**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) -Auflistung zurückzugeben, die Sie zum Bearbeiten der Auswahl eines Benutzers verwenden können.

Wenn ein [**Ink**](inkdisp-class.md) -Objekt oder ein Satz **von frei** Hand Objekten ausgewählt wird, werden die Größen Zieh Punkte in den vier Ecken des umgebenden Felds der frei Hand Eingabe und in allen Mittelpunkten zwischen angrenzenden Ecken angezeigt. Wenn der Benutzer eine beliebige Stelle innerhalb des ausgewählten Bereichs zieht, wird die frei Hand Eingabe im Steuerelement verschoben.

### <a name="default-behavior"></a>Standardverhalten

Das [**InkOverlay**](inkoverlay-class.md) -Objekt ist so festgelegt, dass frei Hand Eingaben standardmäßig gesammelt werden "Ink" ist 53 frei Hand Einheiten breit (wobei 1 frei Hand Raumeinheit = 1 HIMETRIC). Ink ist schwarz, wenn der Benutzer nicht im Modus mit hohem Kontrast ausgeführt wird. Andernfalls wird Ink auf den Color- **\_ WindowText** -Wert (**WindowText** in verwaltetem Code) festgelegt. [**Fitum Curve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) ist **false**.

### <a name="cursor-and-button-objects"></a>Cursor-und Schaltflächen Objekte

Ein Cursor entspricht der Spitze des Stifts, der auf Tablet PC verwendet wird. Beispielsweise weist ein Stift zwei Enden auf. Normalerweise wird ein Ende zum Schreiben verwendet, und das andere wird zum Löschen verwendet. Diese beiden Enden entsprechen zwei Cursorn. Die [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Klasse wird nicht mit [**System. Windows. Forms. Cursor**](/dotnet/api/system.windows.forms.cursor?view=netcore-3.1)verwechselt.

Auf Tablet PC wird normalerweise ein Cursor definiert, der zum Schreiben oder Löschen verwendet werden kann. Ein Cursor kann möglicherweise Rollen ändern, wenn die Anwendung diese Funktion aktiviert. Für einige Tablet PC-Geräte sind mehrere Stifte zulässig. Jeder Cursor verfügt über eine zugeordnete Cursor-ID, die im System eindeutig ist. Einem Cursor können NULL oder mehr zugeordnete Schaltflächen zugeordnet werden. Diese Schaltflächen werden der Anwendung als Cursor Button-Objekte bereitgestellt. Die Anwendung kann für jeden beliebigen Cursor ein bestimmtes [**DrawingAttributes**](inkdrawingattributes-class.md) -Objekt bereitstellen.

### <a name="drawing-attributes-object"></a>Zeichnungs Attribute-Objekt

Ein [**DrawingAttributes**](inkdrawingattributes-class.md) -Objekt beschreibt, wie ein bekannter Satz von frei Hand Eingaben gezeichnet werden muss. Ein **DrawingAttributes** -Objekt enthält grundlegende Eigenschaften wie [**Color**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_color), [**Width**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_width)und [**ptip**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_pentip). Sie kann auch erweiterte Parameter umfassen, z. b. Variable Transparenz und Bezier-Glättung, die interessante Effekte bereitstellen oder die Lesbarkeit der Lesbarkeit verbessern können.

### <a name="peninputpanel-object"></a>"Pinputpanel"-Objekt

> [!Note]  
> Die Klasse " [**pinputpanel**](peninputpanel-class.md) " ist veraltet. Die Klasse " **pinputpanel** " wurde durch die [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) -Klasse ersetzt.

 

Mit dem [**PenInputPanel**](peninputpanel-class.md) -Objekt können Sie Ihren Anwendungen problemlos direkte Stift Eingaben hinzufügen. Der " **pinputpanel** " steht als anfügbares Objekt zur Verfügung, mit dem Sie vorhandenen Steuerelementen Tablet PC-Eingabe Bereichs Funktionen hinzufügen können. Die Benutzeroberfläche wird größtenteils von der aktuellen Eingabe Sprache vorgeschrieben. Sie haben die Möglichkeit, die Standardeingabe Methode für das " **Pendel Panel**"-Steuerelement ("Handschrift" oder "Tastatur") auszuwählen. Der Endbenutzer kann mithilfe von Schaltflächen auf der Benutzeroberfläche zwischen Eingabemethoden wechseln.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**InkCollector-Klasse (C++)**](inkcollector-class.md)
</dt> <dt>

[**InkOverlay-Klasse (C++)**](inkoverlay-class.md)
</dt> <dt>

[**Microsoft. Ink-Namespace**](/previous-versions/dotnet/netframework-3.5/ms581553(v=vs.90))
</dt> </dl>

 

 
