---
title: Auswählen des richtigen Ansatzes für Windows-Finger Eingaben
description: In diesem Abschnitt werden die verschiedenen Ansätze für Windows-Finger Eingaben erläutert, die Sie verwenden können.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows-Fingereingabe, unterschiedliche Ansätze
- Windows-Fingereingabe, auswählen von Ansätzen
- Windows-Interaktion, verbessern von Anwendungen
- Windows-Fingereingabe, Zoom Unterstützung
- Windows-Fingereingabe, Legacy Unterstützung
- Windows-Fingereingabe, RealTimeStylus-Plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86cdd35b73989541fadd5449efbb3f95d76bfa5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039366"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Auswählen des richtigen Ansatzes für Windows-Finger Eingaben

In diesem Abschnitt werden die verschiedenen Ansätze für Windows-Finger Eingaben erläutert, die Sie verwenden können.

Sie können Anwendungen in vielerlei Hinsicht mithilfe von Windows-Berührungs Features verbessern. Bevor Sie eine Methode anwenden, sollten Sie berücksichtigen, was Sie mit der Anwendung tun möchten. Die folgenden Szenarien sind typisch für Windows-Berührungen:

-   Sie möchten, dass sich Ihre Anwendung genauso verhält wie in älteren Versionen von Windows, Sie möchten jedoch, dass sich Windows-Fingereingabe Nachrichten konsistent Verhalten.
-   Sie möchten eine benutzerdefinierte Objekt Rotation, Übersetzung, Schwenken oder Zoom Unterstützung in Ihrer Anwendung.
-   Sie möchten, dass Ihre Anwendung eine differenzierte Interpretation von Windows Touch-Gesten durchläuft oder mehrere Berührungen in einer Anwendung interpretiert, die speziell für Windows Touch-Eingaben optimiert ist.
-   Sie verfügen über eine Anwendung, die das [**RealTimeStylus**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) -Objekt verwendet und es mit den Windows-Berührungs Funktionen verbessern möchte.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Sie möchten, dass sich Ihre Anwendung wie in älteren Versionen von Windows verhält.

In Windows 7 generieren Anwendungen standardmäßig Nachrichten, die die Windows-Berührungs Funktion ermöglichen. Beispielsweise löst Pan-Gesten WM- \_ \* scrollnachrichten aus. Zusätzlich zur Unterstützung von Pan unterstützt der standardmäßige WM- \_ Gesten Handler in Windows 7 das Begrenzungs Feedback, den Zoom und das Drücken und tippen. Das Begrenzungs Feedback wird auch durch den Legacy Support ermöglicht. Weitere Informationen zur Zuordnung von Gesten zu Nachrichten finden Sie unter [Übersicht über Windows-Touchgesten](windows-touch-gestures-overview.md) . Entwickler, die nur diese grundlegenden Funktionen benötigen, müssen nicht direkt mit der Windows-Touchscreen-API arbeiten.

> [!Note]  
> Benutzerdefinierte Scrollleisten-Handler müssen die **SM- \_ thumbpositions** -Anforderung für **WM- \_ VScroll** -Nachrichten unterstützen und die **SB- \_ LineLeft** -Anforderung und die **SB- \_ LineRight** -Anforderung für **WM- \_ HScroll** -Nachrichten

 

-   Im Abschnitt [Legacy Unterstützung für das Schwenken mit Schiebe leisten](legacy-support-for-panning-with-scrollbars.md) wird erläutert, wie Sie sicherstellen, dass sich Ihre Anwendung verhält, wenn Benutzer in Windows 7 erwarten.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Sie möchten eine benutzerdefinierte Objekt Rotation, Übersetzung, Schwenken oder Zoom Unterstützung.

Wenn Sie nur eingeschränkte Unterstützung für die Toucheingabe benötigen, aber das Standardverhalten, das Windows 7 bietet, für Ihre Anwendung nicht geeignet ist, können Sie Gesten verwenden, um Ihre Anwendung zu verbessern. Mithilfe von Gesten können Sie die Gesten Befehle interpretieren, indem Sie die [**WM- \_ Gesten**](wm-gesture.md) Nachricht verarbeiten. Weitere Informationen zu Gesten finden Sie im Abschnitt Windows- [Touchgesten](guide-multi-touch-gestures.md). Wenn Ihre Anwendung nur für Rotationen mit hoher Granularität, verbesserter Zoom Unterstützung oder Einzel fingerschwenken benötigt wird, ist Gesten der beste Ansatz für die Entwicklung von Windows Touch. Zusätzlich zur Interpretation der Gesten Nachricht können Sie auch die Unterstützung für das Feedback von Grenzen festlegen. Weitere Informationen zu Begrenzungs Feedback finden Sie im Abschnitt " [Boundary Feedback](boundary-feedback.md) " der [Referenz zur Windows-touchprogrammierung](windows-touch-programming-reference.md). In Windows 7 nutzen die Eingabeaufforderung und Internet Explorer das Feedback und die Gesten von Grenzen.

-   Im Abschnitt [verbessern der Single fingerpanning](improving-the-single-finger-panning-experience.md) -Darstellung wird erläutert, wie Sie die Schwenk barkeit anpassen, indem Sie die Meldung der [**WM- \_ Geste**](wm-gesture.md) verarbeiten.

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Sie möchten eine fein abgestimmte Gesten Interpretation oder eine benutzerdefinierte Handhabung mehrerer Touchpoints.

Wenn Sie die Gesten noch genauer steuern möchten, als von der [**WM- \_ Gesten**](wm-gesture.md) Nachricht angeboten werden, oder wenn Sie mehrere Gesten für mehrere Objekte interpretieren möchten, sollten Sie den Manipulations Prozessor verwenden. Der Manipulations Prozessor ist im Wesentlichen ein Obermenge von Gesten. Die Verwendung des Manipulations Prozessors erfordert, dass Sie eine Ereignis Senke für Manipulationen implementieren, in die Sie rohdatenberührungsdaten eingeben.

Wenn Sie eine einfache Objekt Physik zusätzlich zur Interpretation der Gesten wünschen, sollten Sie einen Trägheits Prozessor in Verbindung mit dem Manipulations Prozessor verwenden. Der Trägheits Prozessor kann mit dem Manipulations Prozessor verwendet werden, indem beim Bearbeitungs Abschluss Geschwindigkeitswerte vom Manipulations Prozessor übernommen werden.

Wenn Sie mehrere Berührungspunkte in Ihrer Anwendung interpretieren möchten, sollten Sie einen Nachrichten Handler für die WM- [**Finger \_**](wm-touchdown.md) Eingabe Nachricht erstellen.

-   Der Abschnitt " [Windows-Eingabe Eingabe](guide-multi-touch-input.md) " erläutert, wie Sie die WM-Fingereingabe Nachricht interpretieren können. [**\_**](wm-touchdown.md)
-   Der Abschnitt [erkennen und Nachverfolgen mehrerer Berührungspunkte](detecting-and-tracking-multiple-touch-points.md) veranschaulicht, wie Sie eine einfache Anwendung erstellen, die mehrere Eingaben interpretiert.
-   Im Abschnitt [Manipulationen und Trägheit](manipulation-and-inertia.md) wird erläutert, wie Sie den flexibelsten Ansatz für Windows-Finger Eingaben aktivieren.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Sie möchten Windows-Fingereingabe Eingaben für eine Anwendung aktivieren, die RealTimeStylus verwendet.

Wenn Sie die Eingabe für mehrere Kontakte auf der Tablet PC-Plattform aktivieren möchten, müssen Sie ein benutzerdefiniertes RealTimeStylus-Plug-in implementieren, das die Windows-Berührungs Daten interpretiert. Microsoft hat die [**ITablet3**](/windows/desktop/tablet/itablet3) -und [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) -Schnittstellen eingeführt, um Eingaben aus mehreren Kontakten im RealTimeStylus-Plug-in zu aktivieren. Diese Schnittstellen vereinfachen das Erweitern von RealTimeStylus-Plug-ins, um mehrere Kontaktpunkte zu unterstützen.

Um zu prüfen, ob die Unterstützung für mehrere Kontakte aktiviert ist, wenden Sie sich an [**ismulticontacts**](/windows/desktop/tablet/itablet3-ismultitouch). Um die Anzahl der unterstützten Kontakte zu überprüfen, müssen Sie [**getmaximumcursors**](/windows/desktop/tablet/itablet3-getmaximumcursors)aufrufen. Um mehrere Kontakt Unterstützung zu aktivieren oder zu deaktivieren, müssen Sie [**multitouchenabled**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)aufrufen.

> [!Note]  
> Wenn Sie nicht mehrere Kontaktpunkte in RealTimeStylus aktivieren, erhalten Sie Gesten Meldungen wie z. b. Schwenken und Zoom.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 