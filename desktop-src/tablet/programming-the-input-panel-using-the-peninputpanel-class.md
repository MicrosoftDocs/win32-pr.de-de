---
description: Beschreibung der Verwendung des PenInputPanel-Objekts zum Programmieren des Tablet PC-Eingabebereichs auf Systemebene.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programmieren des Eingabebereichs mit der PenInputPanel-Klasse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d430b002fb967652aea046919ec7341a984f420f756fd936e8c68dbfce8c055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449384"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programmieren des Eingabebereichs mit der PenInputPanel-Klasse

\[[**PenInputPanel**](peninputpanel-class.md) wurde durch [Microsoft.Ink.TextInput](/previous-versions/ms581554(v=vs.100))ersetzt. Weitere Informationen finden Sie unter [Programmieren des Texteingabebereichs.](programming-the-text-input-panel.md)\]

Beschreibung der Verwendung des [**PenInputPanel-Objekts**](peninputpanel-class.md) zum Programmieren des Tablet PC-Eingabebereichs auf Systemebene.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Eingabebereich im Vergleich zum PenInputPanel-Objekt

In Microsoft Windows XP Tablet PC Edition Version 1.0 bietet der Tablet PC-Eingabebereich auf Systemebene einen universellen Mechanismus zum Durchführen von Texteingaben auf der Windows Plattform, bietet aber keinen programmgesteuerten Zugriff. In Windows XP Tablet PC Edition Software Development Kit (SDK) Version 1.5 und höher ermöglicht ihnen das [**PenInputPanel-Objekt**](peninputpanel-class.md) die direkte Integration von Texteingabetools in Ihre Anwendungen und bietet eine zuvor nicht verfügbare Steuerungsebene. Ab der Windows XP Tablet PC Edition 2005 wurde der Eingabebereich auf Systemebene aktualisiert, um die vom **PenInputPanel-Objekt** bereitgestellte Funktion für die eingabeeingestellte Eingabe und vieles mehr einzubeziehen.

Die folgende Grafik zeigt den Eingabebereich, der im Beispiel zum Beispiel für das Formular für [automatische Ansprüche](auto-claims-form-sample.md) angezeigt wird.

![Eingabebereich, der über einem Formular angezeigt wird, das für Automobilansprüche verwendet wird](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Der Eingabebereich ersetzt [**penInputPanel,**](peninputpanel-class.md) indem für jede Anwendung, die auf Windows XP Tablet PC Edition 2005 oder höher ausgeführt wird, die gleiche Funktion für die eingabeseitige Eingabe zur Verfügung gestellt wird, ohne dass zusätzlicher Code erforderlich ist. Dieser Artikel zur Verwendung des **PenInputPanel-Objekts** wird aus Gründen der Abwärtskompatibilität bereitgestellt. Anwendungen, die bereits das **PenInputPanel-Objekt** verwenden, funktionieren genauso, außer dass der Eingabebereich anstelle von **PenInputPanel** angezeigt wird, wenn die Anwendung auf Windows XP Tablet PC Edition 2005 oder höher ausgeführt wird.

Wenn Sie eine neue Anwendung für den Tablet-PC entwickeln und über eine lösung für die benutzerseitige Eingabe verfügen möchten, stellt der Eingabebereich dies automatisch auf Windows XP Tablet PC Edition 2005 oder höher bereit. Es ist nicht erforderlich, das [**PenInputPanel-Objekt**](peninputpanel-class.md) zu instanziieren.

## <a name="disabling-the-input-panel"></a>Deaktivieren des Eingabebereichs

Es kann fälle geben, in denen Sie den Eingabebereich deaktivieren möchten. Es gibt zwei Möglichkeiten, dies zu erreichen. Sie können dies programmgesteuert oder durch Festlegen eines Registrierungseintrags erreichen, der den Eingabebereich für Ihre gesamte Anwendung deaktiviert.

### <a name="disabling-input-panel-programmatically"></a>Programmgesteuertes Deaktivieren des Eingabebereichs

Um den Eingabebereich programmgesteuert zu deaktivieren, instanziieren Sie das [**PenInputPanel,**](peninputpanel-class.md) und legen Sie dessen [**AutoShow-Eigenschaft**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) auf **False** fest.


```C++
using Microsoft.Ink;

// ...

private PenInputPanel theInputPanel;

// ...

private void Form1_Load(object sender, System.EventArgs e)
{
// Attach the Input Panel to a specific TextBox control.
theInputPanel = new PenInputPanel(textBox1);

// Disable the Input Panel for the TextBox.
theInputPanel.AutoShow = false;
}
```



Um den Eingabebereich für mehrere Steuerelemente in einer einzelnen Anwendung zu deaktivieren, instanziieren Sie entweder ein [**PenInputPanel-Objekt**](peninputpanel-class.md) für jedes Steuerelement, und legen Sie die [**AutoShow-Eigenschaft**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)für jedes Steuerelement auf **False** fest, oder instanziieren Sie ein einzelnes **PenInputPanel,** und verschieben Sie es von Steuerelement zu Steuerelement, wenn sich der Eingabefokus ändert. Weitere Informationen zu diesen beiden Techniken finden Sie im Thema [PenInputPanel-Beispiel.](peninputpanel-sample.md)

### <a name="disabling-input-panel-through-the-registry"></a>Deaktivieren des Eingabebereichs über die Registrierung

Sie können einen Registrierungseintrag festlegen, um den Eingabebereich für Ihre gesamte Anwendung zu deaktivieren. Dies wird jedoch auch für gängige Dialogfelder wie das Dialogfeld **Datei öffnen,** das Dialogfeld **Drucken** und das Dialogfeld **Dateispeicher** deaktiviert. Dadurch kann die Benutzeroberfläche in Ihrer Anwendung mit anderen Tablet PC-Anwendungen inkonsistent sein.

Wenn Sie den `DisableInPlace` Registrierungsschlüssel auf 0 festlegen, wird verhindert, dass die Benutzeroberfläche des Eingabebereichs in einer Anwendung angezeigt wird. Sie müssen den `DisableInPlace` Registrierungsschlüssel unter `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` platzieren. Fügen Sie dann einen neuen Registrierungswert hinzu, indem Sie den vollständigen Pfad der Anwendung verwenden, in der Sie den Eingabebereich deaktivieren möchten. Der folgende Beispielregistrierungseintrag deaktiviert den Eingabebereich in einer Anwendung namens MyApp:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Wenn in Ihrer Anwendung nach dem Deaktivieren der Benutzeroberfläche des Eingabebereichs weiterhin ein Problem auftritt, kann es erforderlich sein, das zugrunde liegende Framework zu deaktivieren, das Ihre Anwendung nach dem Caretspeicherort abfragt. Beispielsweise kann der Eingabebereich einen Fehler im Caretzeichen-Nachverfolgungscode Ihrer Anwendung verfügbar machen. Wenn Sie die Nachverfolgungsabfrage für Caretzeichen deaktivieren, wird auch verhindert, dass die Benutzeroberfläche des Eingabebereichs angezeigt wird. Um das Framework zu deaktivieren, legen Sie den `EnableCaretTracking` Registrierungsschlüssel auf 0 (null) fest. Suchen Sie diesen Schlüssel unter `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Barrierefreiheitstools und Sprachtechnologie in Windows XP verwenden dieses Framework ebenfalls, sodass durch das Deaktivieren der Abfrage auch diese Features in Ihrer Anwendung deaktiviert werden.

 

## <a name="the-input-panel-and-web-pages"></a>Eingabebereich und Webseiten

Um eine API auf einer Webseite verwenden zu können, muss sie in einer teilweise vertrauenswürdigen Umgebung funktionieren. Alle [**PenInputPanel-Klassenmember**](peninputpanel-class.md) erfordern volle Vertrauenswürdigkeit mit Ausnahme der folgenden:

-   [PenInputPanel-Konstruktoren](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (nur verwalteter Code)
-   [Dispose-Methode](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (nur verwalteter Code)
-   [AttachedEditControl-Eigenschaft](/previous-versions/ms582239(v=vs.100)) (nur verwalteter Code)
-   [**AutoShow-Eigenschaft**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Diese APIs funktionieren in einer teilweise vertrauenswürdigen Umgebung, z. B. einer Webseite, sodass Sie ein [**PenInputPanel-Objekt**](peninputpanel-class.md) instanziieren, es an ein Steuerelement anfügen und den Eingabebereich für dieses Steuerelement deaktivieren können. Weitere Informationen finden Sie unter Programmieren des Eingabebereichs mithilfe der PenInputPanel-Klasse und [Ink im Web.](ink-on-the-web.md)

## <a name="the-peninputpanel-object"></a>Das PenInputPanel-Objekt

Im weiteren Verlauf dieses Themas wird beschrieben, wie Sie das [**PenInputPanel-Objekt**](peninputpanel-class.md) in Ihren Tablet PC-fähigen Anwendungen verwenden. Genauer gesagt bezieht sich dieses Thema auf das **PenInputPanel-Objekt,** wenn es um das Programmierobjekt geht, den Stifteingabebereich, wenn auf das Benutzeroberflächenelement verwiesen wird, und den PC-Eingabebereich (oder Eingabebereich), wenn auf das globale Eingabepanel verwiesen wird, das sich normalerweise auf der Seite des Tablet PC-Bildschirms befindet.

In den folgenden Abschnitten werden das [**PenInputPanel-Objekt**](peninputpanel-class.md) und die Benutzeroberfläche beschrieben.

-   [Informationen zum Eingabebereich](about-the-input-panel.md)
-   [Instanziieren der PenInputPanel-Klasse](instantiating-the-peninputpanel-class.md)
-   [Factoid-Unterstützung](factoid-support.md)
-   [Textdienstframework](text-services-framework.md)
-   [Bewährte Methoden](best-practices.md)

 

 
