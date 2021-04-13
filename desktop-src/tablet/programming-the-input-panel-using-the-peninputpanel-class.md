---
description: Beschreibung der Verwendung des "pinputpanel"-Objekts zum Programmieren des Tablet PC-Eingabe Bereichs auf Systemebene.
ms.assetid: f83c7709-86dc-4c64-ad17-2ad660eb57b7
title: Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80e00d1cb10983255ab2e532aa08de6e9e6a0fb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349389"
---
# <a name="programming-the-input-panel-using-the-peninputpanel-class"></a>Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel"

\[" [**Pinputpanel**](peninputpanel-class.md) " wurde durch " [Microsoft. Ink. TextInput](/previous-versions/ms581554(v=vs.100))" ersetzt. Weitere Informationen finden Sie unter [Programmieren des Text Eingabe Panels](programming-the-text-input-panel.md).\]

Beschreibung der Verwendung des " [**pinputpanel**](peninputpanel-class.md) "-Objekts zum Programmieren des Tablet PC-Eingabe Bereichs auf Systemebene.

## <a name="input-panel-vs-the-peninputpanel-object"></a>Eingabebereich im Vergleich zum Objekt "das Objekt" "

In der Version 1,0 von Microsoft Windows XP Tablet PC Edition stellt der Eingabebereich des Tablet PCs auf Systemebene einen universellen Mechanismus zum Ausführen von Texteingaben auf der Windows-Plattform bereit, bietet jedoch keinen programmgesteuerten Zugriff. In Windows XP Tablet PC Edition Software Development Kit (SDK), Version 1,5 und höher, können Sie mit [**dem Objekt "**](peninputpanel-class.md) " "" "" "" mit dem "" "" "" "" "" "". Beginnend mit Windows XP Tablet PC Edition 2005 wurde der Eingabebereich auf Systemebene aktualisiert, um die direkte Eingabe Funktionalität zu enthalten **, die vom Objekt "** " mit dem ""-Objekt "" und mehr bereitgestellt wird.

In der folgenden Abbildung wird der Eingabebereich angezeigt, der über dem Beispiel für ein [Automatisches Anspruchsformular](auto-claims-form-sample.md) angezeigt wird.

![Eingabebereich, der über einem für Automobile-Ansprüche verwendeten Formular angezeigt wird](images/36eaa36b-1b0c-4363-96fa-092f70663ffa.jpg)

Der Eingabebereich hat Vorrang vor dem [**tabinputpanel**](peninputpanel-class.md) , indem für jede Anwendung, die unter Windows XP Tablet PC Edition 2005 oder höher ausgeführt wird, dieselbe direkte Eingabe Funktion bereitgestellt wird, ohne dass zusätzlicher Code erforderlich ist. In diesem Artikel zur Verwendung des Objekts " **pinputpanel** " wird die Abwärtskompatibilität bereitgestellt. Anwendungen, die das Objekt " **pinputpanel** " bereits verwenden, funktionieren identisch, mit dem Unterschied, dass der Eingabebereich anstelle von " **tabinputpanel** " angezeigt wird, wenn die Anwendung unter Windows XP Tablet PC Edition 2005 oder höher ausgeführt wird.

Wenn Sie eine neue Anwendung für den Tablet PC entwickeln und eine direkte Benutzereingabe Lösung wünschen, bietet der Eingabebereich dies automatisch unter Windows XP Tablet PC Edition 2005 oder höher. Es ist nicht erforderlich, das " [**poinputpanel**](peninputpanel-class.md) "-Objekt zu instanziieren.

## <a name="disabling-the-input-panel"></a>Der Eingabebereich wird deaktiviert.

Es kann vorkommen, dass Sie den Eingabebereich deaktivieren möchten. Es gibt zwei Möglichkeiten, dies zu erreichen. Sie können dies Programm gesteuert oder durch Festlegen eines Registrierungs Eintrags erreichen, der den Eingabebereich für Ihre gesamte Anwendung deaktiviert.

### <a name="disabling-input-panel-programmatically"></a>Programm gesteuertes Deaktivieren des Eingabe Bereichs

Um den Eingabebereich Programm gesteuert zu deaktivieren, instanziieren Sie den " [**poinputpanel**](peninputpanel-class.md) ", und legen Sie dessen [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) -Eigenschaft auf **false** fest.


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



Um den Eingabebereich für mehrere Steuerelemente in einer einzelnen Anwendung zu deaktivieren, instanziieren Sie entweder ein " [**poinputpanel**](peninputpanel-class.md) "-Objekt für jedes Steuerelement, und legen Sie für jedes Steuerelement die [**AutoShow**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)-Eigenschaft auf " **false** " fest, oder Instanziieren Sie ein einzelnes " **poinputpanel** ", und verschieben Sie es von Control Weitere Informationen zu diesen beiden Techniken finden Sie im Thema zum Beispiel für den " [tainputpanel](peninputpanel-sample.md) ".

### <a name="disabling-input-panel-through-the-registry"></a>Der Eingabebereich wird durch die Registrierung deaktiviert.

Sie können einen Registrierungs Eintrag festlegen, um den Eingabebereich für Ihre gesamte Anwendung zu deaktivieren. Dies wird jedoch auch für allgemeine Dialogfelder, wie z. b. das Dialogfeld zum **Öffnen von Dateien** , das Dialogfeld **Drucken** und das Dialogfeld **Datei speichern** deaktiviert. Dies kann dazu führen, dass der Benutzer in Ihrer Anwendung inkonsistent mit anderen Tablet PC-Anwendungen ist.

Das Festlegen des `DisableInPlace` Registrierungsschlüssels auf 0 (null) verhindert, dass die Benutzeroberfläche des Eingabe Bereichs in einer Anwendung angezeigt wird. Sie müssen den `DisableInPlace` Registrierungsschlüssel unter platzieren `HKEY_LOCAL_MACHINE\Software\Microsoft\TabletTip\` . Fügen Sie dann einen neuen Registrierungs Wert hinzu, indem Sie den vollständigen Pfad der Anwendung verwenden, in der Sie den Eingabebereich deaktivieren möchten. Mit dem folgenden Beispiel Registrierungs Eintrag wird der Eingabebereich in einer Anwendung mit dem Namen "MyApp" deaktiviert:

`[HKEY_LOCAL_MACHINE \SOFTWARE\Microsoft\WindowsNT\TabletTIP\DisableInPlace]``"C:\Program Files\My App\MyApp.exe"=dword:00000000`

Wenn in Ihrer Anwendung weiterhin ein Problem auftritt, nachdem Sie die Benutzeroberfläche des Eingabe Panels deaktiviert haben, kann es erforderlich sein, das zugrunde liegende Framework zu deaktivieren, das Ihre Anwendung nach dem Speicherort der Einfügemarke abfragt. Beispielsweise kann der Eingabebereich einen Fehler im Caretzeichen der Caretzeichen der Anwendung verfügbar machen. Durch das Ausschalten der Abfrage der Einfügemarke wird außerdem verhindert, dass die Benutzeroberfläche des Eingabe Panels angezeigt wird Um das Framework zu deaktivieren, legen `EnableCaretTracking` Sie den Registrierungsschlüssel auf 0 (null) fest. Suchen Sie diesen Schlüssel unter `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\WindowsNT\CurrentVersion\AppCompatFlags\CaretTracking\` .

> [!Note]  
> Barrierefreiheits Tools und Sprachtechnologie in Windows XP verwenden ebenfalls dieses Framework, sodass durch das Deaktivieren der Abfrage auch diese Features in Ihrer Anwendung deaktiviert werden.

 

## <a name="the-input-panel-and-web-pages"></a>Der Eingabebereich und die Webseiten

Damit eine API auf einer Webseite verwendet werden kann, muss Sie in einer teilweise vertrauenswürdigen Umgebung funktionieren. Alle " [**pinputpanel**](peninputpanel-class.md) "-Klassenmember erfordern volle Vertrauenswürdigkeit mit Ausnahme der folgenden:

-   " [Tzinputpanel"-Konstruktoren](/previous-versions/dotnet/netframework-3.5/ms571341(v=vs.90)) (nur verwalteter Code)
-   Verwerfen- [Methode](/previous-versions/dotnet/netframework-3.5/ms571343(v=vs.90)) (nur verwalteter Code)
-   [AttachedEditControl-Eigenschaft](/previous-versions/ms582239(v=vs.100)) (nur verwalteter Code)
-   [**Autoshow (Eigenschaft)**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow)

Diese APIs funktionieren in einer teilweise vertrauenswürdigen Umgebung, z. b. einer Webseite, sodass Sie ein " [**poinputpanel**](peninputpanel-class.md) "-Objekt instanziieren, an ein Steuerelement anfügen und den Eingabebereich für dieses Steuerelement deaktivieren können. Weitere Informationen finden Sie unter Programmieren des Eingabe Bereichs mithilfe der Klasse "pinputpanel" und frei Hand Eingaben [im Web](ink-on-the-web.md).

## <a name="the-peninputpanel-object"></a>Das "pinputpanel"-Objekt

Im weiteren Verlauf dieses Themas wird beschrieben, wie Sie das Objekt " [**pinputpanel**](peninputpanel-class.md) " in Ihren Tablet PC – aktivierten Anwendungen verwenden. Genauer gesagt bezieht sich dieses Thema auf das **PenInputPanel** -Objekt, wenn es das Programmier Objekt erläutert, den Stift Eingabebereich beim Verweisen auf das UI-Element und den Eingabebereich des PCs (oder den Eingabebereich) beim Verweis auf den globalen Eingabebereich, der sich normalerweise auf der Seite des Tablet PC-Bildschirms befindet.

In den folgenden Abschnitten werden das Objekt und die Benutzeroberfläche von " [**pinputpanel**](peninputpanel-class.md) " beschrieben

-   [Informationen zum Eingabebereich](about-the-input-panel.md)
-   [Instanziieren der Klasse "poinputpanel"](instantiating-the-peninputpanel-class.md)
-   [Unterstützung von Faktoids](factoid-support.md)
-   [Textdienstframework](text-services-framework.md)
-   [Bewährte Methoden](best-practices.md)

 

 
