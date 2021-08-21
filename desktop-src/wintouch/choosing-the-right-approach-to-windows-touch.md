---
title: Auswählen des richtigen Ansatzes für die Windows Toucheingabe
description: In diesem Abschnitt werden die verschiedenen Ansätze für Windows Touch erläutert, die Sie verwenden können.
ms.assetid: 983023e4-355b-45ba-8572-d93c460d2ff8
keywords:
- Windows Toucheingabe, verschiedene Ansätze
- Windows Toucheingabe, Auswählen von Ansätzen
- Windows Toucheingabe, Erweitern von Anwendungen
- Windows Toucheingabe, Zoomunterstützung
- Windows Toucheingabe, Legacyunterstützung
- Windows Touch,RealTimeStylus-Plug-In
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd5ad8be1a460b7c91b01a4c566566c424feabc10206482cca72ae3739584c75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118030347"
---
# <a name="choosing-the-right-approach-to-windows-touch"></a>Auswählen des richtigen Ansatzes für die Windows Toucheingabe

In diesem Abschnitt werden die verschiedenen Ansätze für Windows Touch erläutert, die Sie verwenden können.

Sie können Anwendungen mit Windows Touch-Features auf unterschiedliche Weise verbessern. Bevor Sie eine Methode übernehmen, sollten Sie überlegen, was Sie mit Ihrer Anwendung tun möchten. Die folgenden Szenarien sind typisch für Windows Touch:

-   Sie möchten, dass sich Ihre Anwendung wie in Legacyversionen von Windows verhält, aber Windows Touch-Nachrichten einheitlich verhalten sollen.
-   Sie möchten benutzerdefinierte Objektrotation, Übersetzung, Schwenken oder Zoomunterstützung in Ihrer Anwendung.
-   Sie möchten, dass Ihre Anwendung eine differenzierte Interpretation Windows Touchgesten oder mehrere Berührungen in einer Anwendung interpretiert, die speziell für Windows Toucheingabe optimiert ist.
-   Sie verfügen über eine Anwendung, die das [**RealTimeStylus-Objekt**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus) verwendet und es mit Windows Touchfunktionen erweitern möchte.

## <a name="you-want-your-application-to-behave-as-it-did-in-legacy-versions-of-windows"></a>Sie möchten, dass sich Ihre Anwendung wie in Legacyversionen von Windows

In Windows 7 generieren Anwendungen standardmäßig Nachrichten, die Windows Touch-Funktionalität ermöglichen. Beispielsweise lösen Schwenkgesten WM \_ \* SCROLL-Meldungen aus. Zusätzlich zur Schwenkunterstützung unterstützt der WM \_ GESTURE-Standardhandler in Windows 7 Das Feedback zu Grenzen, zoomen und drücken und tippen. Begrenzungsfeedback wird auch über Legacyunterstützung aktiviert. Weitere Informationen zur Zuordnung von Gesten zu Nachrichten finden Sie in der [Übersicht über Windows Touchgesten.](windows-touch-gestures-overview.md) Entwickler, die nur diese grundlegende Funktionalität benötigen, müssen nicht direkt mit der Windows Touch-API arbeiten.

> [!Note]  
> Benutzerdefinierte Scrollleistenhandler müssen die **SM \_ THUMBPOSITION-Anforderung** für **\_ WM-VSCROLL-Nachrichten** unterstützen und die **SB \_ LINELEFT-Anforderung** und die **SB \_ LINERIGHT-Anforderung** für **WM \_ HSCROLL-Nachrichten** unterstützen.

 

-   Im Abschnitt [Legacy support for Panning with Scroll Bars (Legacyunterstützung für das Schwenken mit Scrollleisten)](legacy-support-for-panning-with-scrollbars.md) wird erläutert, wie Sie sicherstellen können, dass sich Ihre Anwendung so verhält, wie benutzer es in Windows 7 erwarten.

## <a name="you-want-custom-object-rotation-translation-panning-or-zoom-support"></a>Sie möchten benutzerdefinierte Objektrotation, Übersetzung, Schwenken oder Zoomunterstützung.

Wenn Sie eine eingeschränkte Unterstützung für Toucheingaben wünschen, aber das Standardverhalten, das Windows 7 bietet, nicht für Ihre Anwendung geeignet ist, können Sie Gesten verwenden, um Ihre Anwendung zu verbessern. Mithilfe von Gesten können Sie die Gestenbefehle interpretieren, indem Sie die [**WM \_ GESTURE-Meldung**](wm-gesture.md) verarbeiten. Weitere Informationen zu Gesten finden Sie im Abschnitt [Windows Touch-Gesten](guide-multi-touch-gestures.md). Wenn Ihre Anwendung nur Unterstützung für Drehungen mit hoher Granularität, verbesserte Zoomunterstützung oder Einfache-Finger-Schwenken benötigt, ist Gesten der beste Ansatz für Windows Touchentwicklung. Zusätzlich zum Interpretieren der Gestennachricht können Sie auch Unterstützung für Grenzfeedback erhalten. Weitere Informationen zum Grenzfeedback finden Sie im Abschnitt [Boundary Feedback](boundary-feedback.md) der Windows Touch Programming Reference ( Referenz zur [Touchprogrammierung).](windows-touch-programming-reference.md) In Windows 7 profitieren die Eingabeaufforderung und Internet Explorer von Grenzfeedback und Gesten.

-   Im Abschnitt [Improving the Single Finger Panning Experience (Verbessern der Single Finger Panning Experience)](improving-the-single-finger-panning-experience.md) wird erläutert, wie Sie die Schwenkerfahrung anpassen, indem Sie die WM [**\_ GESTURE-Meldung**](wm-gesture.md) verarbeiten.

## <a name="you-want-fine-grained-gesture-interpretation-or-custom-handling-of-multiple-touch-points"></a>Sie möchten eine differenzierte Gesteninterpretation oder benutzerdefinierte Behandlung mehrerer Berührungspunkte.

Wenn Sie eine noch spezifischere Steuerung der Gesten wünschen, als die [**WM \_ GESTURE-Nachricht**](wm-gesture.md) bietet, oder wenn Sie mehrere Gesten für mehrere Objekte interpretieren möchten, sollten Sie den Bearbeitungsprozessor verwenden. Der Bearbeitungsprozessor ist im Wesentlichen eine Obermenge von Gesten. Die Verwendung des Manipulationsprozessors erfordert, dass Sie eine Ereignissenke für Manipulationen implementieren, an die Sie Touchrohdaten übermitteln.

Wenn Sie neben der Interpretation der Gesten auch eine einfache Objektarchitektur wünschen, sollten Sie einen Trägheitsprozessor in Verbindung mit dem Manipulationsprozessor verwenden. Der Trägheitsprozessor arbeitet mit dem Manipulationsprozessor zusammen, indem geschwindigkeitswerte vom Manipulationsprozessor nach Abschluss der Bearbeitung verwendet werden.

Wenn Sie mehrere Berührungspunkte in Ihrer Anwendung interpretieren möchten, sollten Sie einen Meldungshandler für die [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) erstellen.

-   Im Abschnitt [Windows TouchEingabe](guide-multi-touch-input.md) wird erläutert, wie Sie die [**WM \_ TOUCH-Nachricht**](wm-touchdown.md) interpretieren können.
-   Im Abschnitt [Erkennen und Nachverfolgen mehrerer Berührungspunkte](detecting-and-tracking-multiple-touch-points.md) wird veranschaulicht, wie Sie eine einfache Anwendung erstellen, die mehrere Eingaben interpretiert.
-   Im Abschnitt [Manipulationen und Trägheit](manipulation-and-inertia.md) wird erläutert, wie Sie den flexibelsten Ansatz für die Windows Touch ermöglichen.

## <a name="you-want-to-enable-windows-touch-input-to-an-application-that-uses-the-realtimestylus"></a>Sie möchten Windows Toucheingabe für eine Anwendung aktivieren, die den RealTimeStylus verwendet.

Wenn Sie die Eingabe für mehrere Kontakte auf der Tablet PC-Plattform aktivieren möchten, müssen Sie ein benutzerdefiniertes RealTimeStylus-Plug-In implementieren, das die Windows Touch-Daten interpretiert. Microsoft hat die Schnittstellen [**ITablet3**](/windows/desktop/tablet/itablet3) und [**IRealTimeStylus3**](/windows/desktop/api/rtscom/nn-rtscom-irealtimestylus3) eingeführt, um eingaben von mehreren Kontakten im RealTimeStylus-Plug-In zu ermöglichen. Diese Schnittstellen vereinfachen das Erweitern von RealTimeStylus-Plug-Ins zur Unterstützung mehrerer Kontaktpunkte.

Um zu überprüfen, ob die Unterstützung für mehrere Kontakte aktiviert ist, rufen Sie [**IsMultiTouch**](/windows/desktop/tablet/itablet3-ismultitouch)auf. Rufen [**Sie GetMaximumCursors**](/windows/desktop/tablet/itablet3-getmaximumcursors)auf, um die Anzahl der unterstützten Kontakte zu überprüfen. Um den Support für mehrere Kontaktkontakte zu aktivieren oder zu deaktivieren, rufen Sie [**MultiTouchEnabled auf.**](/windows/desktop/api/rtscom/nf-rtscom-irealtimestylus3-get_multitouchenabled)

> [!Note]  
> Wenn Sie im RealTimeStylus nicht mehrere Kontaktpunkte aktivieren, erhalten Sie Gestenmeldungen wie Schwenken und Zoomen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 