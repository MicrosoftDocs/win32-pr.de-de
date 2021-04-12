---
description: Im folgenden finden Sie häufig gestellte Fragen (FAQ) zur Entwicklung von Tablet PC-Platt Form Komponenten, die vom Windows Vista SDK installiert werden.
ms.assetid: eb349493-a2b2-4b58-bcbc-ee09953c8dc8
title: Häufig gestellte Fragen (Tablet PC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8722c00fa5aaf2b43494484fc015fa8b3e4c7826
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2020
ms.locfileid: "104391306"
---
# <a name="frequently-asked-questions-about-developing-for-the-tablet-pc-platform"></a>Häufig gestellte Fragen zum entwickeln für die Tablet PC-Plattform

Im folgenden finden Sie häufig gestellte Fragen (FAQ) zur Entwicklung von Tablet PC-Platt Form Komponenten, die vom Windows Vista SDK installiert werden.

## <a name="q-can-i-use-the-ink-apis-or-controls-in-a-web-page"></a>Q. Kann ich die frei Hand-APIs oder Steuerelemente auf einer Webseite verwenden?

A. Ja. Die von Tablet PC verwaltete Bibliothek unterstützt teilweise vertrauenswürdige Umgebungen, nämlich die Ausführung verwalteter Assemblys von Webseiten.

Es gibt auch Unterstützung für die Browser Bereitstellung von Anwendungen, die Windows Presentation Foundation verwenden.

## <a name="q-do-i-need-a-tablet-pc-to-develop-tablet-pc-applications"></a>Q. Benötige ich einen Tablet PC zum Entwickeln von Tablet PC-Anwendungen?

A. Nein, die Tablet PC-Platt Form Komponenten, die vom Windows SDK installiert werden, enthalten die Erweiterungen und Hilfsprogramme, die zum Entwickeln von Software für den Tablet PC auf einem Desktop-oder Laptop Computer erforderlich sind. Sie können eine Maus oder ein externes Tablet für Stift-und Handschrift Eingaben verwenden.

Die Komponenten der Tablet PC-Plattform, die vom Windows SDK installiert werden, können unter Windows XP Professional oder Windows Server 2003 installiert werden, aber für Ihre Anwendungen steht weniger Funktionalität zur Verfügung. Auf diesen Plattformen kann die Anwendung frei Hand Eingaben mit den [**InkCollector**](inkcollector-class.md) -und [**InkOverlay**](inkoverlay-class.md) -Objekten erfassen und getestet und gedeppt werden.

Außerdem können die Steuerelemente " [InkEdit](inkedit-control-reference.md) " und " [InkPicture](inkpicture-control-reference.md) " frei Hand Eingaben für diese Betriebssysteme nur dann sammeln, wenn die Komponenten der Tablet PC-Plattform vom Windows SDK (oder einer älteren Version des Tablet PC Development Kit) installiert wurden. Sie sammeln keine Freihand in Anwendungen, die auf nicht-Tablet-Computer verteilt werden, ohne dass die Platt Form Komponenten installiert sind.

## <a name="q-do-i-need-to-run-a-special-version-of-windows-to-do-handwriting-recognition"></a>Q. Muss ich eine spezielle Version von Windows ausführen, um die Handschrifterkennung auszuführen?

A. Nein. Obwohl nur Windows XP Tablet PC Edition und bestimmte Versionen von Windows Vista Hand schrifterkennungsfunktionen enthalten, können Sie das [Windows XP Tablet PC Edition 2005-Erkennungs Paket]( https://www.microsoft.com/downloads/details.aspx?FamilyId=080184DD-5E92-4464-B907-10762E9F918B&amp;displaylang=en) herunterladen und es nur zu Entwicklungszwecken unter Windows XP Professional oder Windows Server 2003 installieren. Sie dürfen die erkenzer nicht mit Ihrer Anwendung neu verteilen.

## <a name="q-what-is-the-difference-between-windows-vista-and-tablet-pc-technology"></a>Q. Worin besteht der Unterschied zwischen Windows Vista und Tablet PC-Technologie?

A. Tablet PCs führen das Windows Vista-Betriebssystem aus, das alle Funktionen von Windows Vista sowie zusätzliche Features speziell für den Tablet PC enthält. Diese Features der Tablet PC-Technologie ermöglichen Benutzern das Ausführen von Windows-und Windows-Anwendungen mithilfe eines Stifts, das Kommentieren von Dokumenten und das Erstellen von handschriftlichen Dokumenten mithilfe von Digital Ink. Die Tablet PC-Technologie ist in den meisten Versionen von Windows Vista verfügbar, und wenn Tablet PC-Hardware auf einem Computer verfügbar ist, funktionieren die Features einfach.

Bei früheren Versionen von Windows-Betriebssystemen, die frei Hand Eingaben nicht nativ unterstützen, können Sie die Tablet PC-Freihand-Steuerelemente neu verteilen und verwenden, um frei Hand Eingaben auf einem Tablet PC anzuzeigen.

## <a name="q-what-is-the-difference-between-windows-xp-tablet-pc-edition-and-windows-xp-tablet-pc-edition-2005"></a>Q. Worin besteht der Unterschied zwischen Windows XP Tablet PC Edition und Windows XP Tablet PC Edition 2005?

A. Windows XP Tablet PC Edition 2005 ist eine aktualisierte Version von Windows XP Tablet PC Edition.

## <a name="q-how-do-i-modify-my-application-to-run-on-a-tablet-pc"></a>Q. Gewusst wie meine Anwendung für die Verwendung auf einem Tablet PC ändern?

A. Microsoft Windows-Anwendungen, die auf einem Windows XP-Desktop Computer oder Laptop mit vergleichbarer Hardware ausgeführt werden, können ohne Änderungen auf einem Tablet PC ausgeführt werden.

## <a name="q-i-understand-that-i-dont-need-to-make-any-changes-to-my-application-but-it-is-difficult-to-use-it-with-a-pen-and-speech-what-can-i-do-to-optimize-my-application-for-a-tablet-pc"></a>Q. Ich bin mir bewusst, dass ich keine Änderungen an meiner Anwendung vornehmen muss, aber es ist schwierig, Sie mit einem Stift und einer Sprache zu verwenden. Was kann ich tun, um meine Anwendung für einen Tablet PC zu optimieren?

A. Die API-und Ink-Steuerelemente der Tablet PC-Platt Form Komponenten können verwendet werden, um Benutzeroberflächen zu erstellen, die besser für Stift-und Handschrift Eingaben geeignet sind. Weitere Informationen zu bestimmten Möglichkeiten, wie Sie Ihre Anwendung verbessern können, finden Sie unter [Richtlinien für mobile PC-Benutzer Funktionen für Entwickler](/previous-versions//dd356056(v=vs.85)).

## <a name="q-what-programming-languages-does-the-tablet-support"></a>Q. Welche Programmiersprachen unterstützt das Tablet?

A. Die Tablet PC-Technologie in Windows Vista unterstützt com (C++) und verwaltete Bibliotheken (die Suite von Visual Studio .NET-Sprachen).

Die Tablet PC-Technologie unterstützt auch Windows Presentation Foundation (WPF).

## <a name="q-do-i-have-sample-code-that-demonstrates-tablet-platform-capabilities"></a>Q. Habe ich Beispielcode, der Tablet Platform-Funktionen veranschaulicht?

A. Ja, Beispielcode für com und ausgewählte verwaltete Sprachen ist in den Tablet PC-Platt Form Komponenten enthalten, die vom Windows Platform SDK installiert werden.

Verfügbare Beispielanwendungen finden Sie unter:

- [Beispiele für mobile PCs und Tablet PCs](mobile-pc-and-tablet-pc-samples.md)
- [Digital Ink Samples, Windows Presentation Foundation (WPF)](/previous-versions/dotnet/netframework-3.0/aa972145(v=vs.85))
- <systemdrive>: \\ Programmdateien \\ Microsoft sdgs \\ Windows \\ v 6.0 \\ Beispiele \\ TabletPC

## <a name="q-whats-the-base-level-of-tablet-hardware-that-i-should-develop-for"></a>Q. Wie hoch ist die Basisebene der Tablet-Hardware, für die ich entwickeln sollte?

A. Im Allgemeinen sollten Sie für ein Windows Vista-kompatibles, Legacy freies System entwerfen.

## <a name="q-what-user-interface-guidelines-can-you-provide-for-tablet-applications"></a>Q. Welche Richtlinien für die Benutzeroberfläche können Sie für Tablet-Anwendungen bereitstellen?

A. Informationen aus der Dropdown Menü-Ausrichtung zur Bildschirm-/digitalisiererparametisierung werden im Abschnitt Mobile PC- [Richtlinien für Entwickler](/previous-versions//dd356056(v=vs.85)) im Abschnitt Mobile PCs des Windows SDK beschrieben.

## <a name="q-do-you-include-system-level-handwriting-gestures-for-commonly-used-keystrokes-can-i-create-my-own-gestures-for-use-when-an-application-is-running-or-has-focus"></a>Q. Fügen Sie Handschrift Gesten auf Systemebene für häufig verwendete Tastatureingaben ein? Kann ich meine eigenen Gesten erstellen, die verwendet werden, wenn eine Anwendung ausgeführt wird oder den Fokus hat?

A. Ja, wir schließen eine Reihe von Gesten für Mausereignisse ein. Außerdem können Sie Gesten für die Verwendung in Ihrer Anwendung erstellen. Weitere Informationen zu Gesten finden Sie unter [Verwenden von Gesten](using-gestures.md).

## <a name="q-how-can-i-determine-whether-my-application-is-running-on-a-tablet"></a>Q. Wie kann ich feststellen, ob meine Anwendung auf einem Tablet ausgeführt wird?

A. Verwenden Sie Windows getsystemmetricsapi, und übergeben Sie SM \_ TabletPC als Wert für den Index. SM \_ TabletPC ist in winuser. h definiert. Der Wert von SM \_ TabletPC ist 86.

Für die Webentwicklung sollten Sie die \_ Umgebungsvariable Benutzer-Agent- \_ Zeichenfolge lesen. Sie können auf diese Request. ServerVariables-Auflistung zugreifen.

Ausführliche Informationen zur Verwendung von GetSystemMetrics auf Tablet PCs, auf denen Windows Vista oder Windows XP Tablet PC Edition ausgeführt wird, finden Sie unter [bestimmen, ob ein PC ein Tablet PC ist](determining-whether-a-pc-is-a-tablet-pc.md).

## <a name="q-how-can-i-determine-whether-tablet-platform-components-are-available"></a>Q. Wie kann ich feststellen, ob Tablet Platform-Komponenten verfügbar sind?

A. Bestimmte Teile der Tablet PC-Plattform können auf nicht-Tablet-Versionen der Betriebssysteme Windows XP Professional, Windows Server 2003 und Windows 2000 installiert werden.

Die richtige Möglichkeit, um zu bestimmen, ob eine Komponente der API installiert ist, besteht darin, eine Instanz eines Objekts oder eines Steuer Elements zu erstellen und zu überprüfen, ob es vorhanden ist, bevor Sie versuchen, es zu verwenden.

Um z. b. zu ermitteln, ob das [**InkCollector**](inkcollector-class.md) -Objekt verfügbar ist, versuchen Sie, es mithilfe von [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)zu erstellen.

```C++
IInkCollector* pIInkCollector = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkCollector,
 NULL, CLSCTX_INPROC_SERVER, 
 IID_IInkCollector,
 (void **)&pIInkCollector);
if (SUCCEEDED(hr)) 
{ 
  /* InkCollector is usable. */ 
} else 
{
  /* InkCollector unavailable. */
}
```

## <a name="q-how-do-i-run-the-tablet-input-service-on-server-skus"></a>Q. Gewusst wie den Tablet Input Service auf Server-SKUs ausführen?

A. Tabletinputservice wurde bei der Installation des Client Pakets nicht automatisch in Server-SKUs ausgeführt. Client Pack installiert alle Komponenten auf der Plattform, sodass alle Tablet-Client Anwendungen ebenfalls auf einem Server ausgeführt werden können. Der Tablet Input-Dienst lauscht auf PNP-Benachrichtigung, dass ein externer Digitalisierer angeschlossen ist. Um den Tablet Input-Dienst auf einem Server zu aktivieren, verwenden Sie das Systemkonfigurations-Hilfsprogramm.

Wählen Sie im Menü **Start** die Option **Ausführen** aus. Geben Sie "msconfig" ein, und drücken Sie die EINGABETASTE. Wählen Sie die Registerkarte **Dienste** aus, suchen Sie die Dienste "HID Input Service", aktivieren Sie das Kontrollkästchen neben der Registerkarte, und klicken Sie dann auf **anwenden**. Schließen Sie das-Hilfsprogramm.

## <a name="q-more-faqs-and-other-resources"></a>Q. Weitere FAQs und weitere Ressourcen

- [Microsoft Developer Center](https://developer.microsoft.com)
- [Core Tablet PC-Referenz](./core-reference---tablet-pc-com-library.md)