---
title: Trägheit-Mechanik
description: Trägheit-Mechanik
ms.assetid: 188b6936-b36e-4e57-9118-8b61ed134c17
keywords:
- Windows-Fingereingabe, Trägheit
- Windows-Fingereingabe, Smooth Animation
- Windows-Fingereingabe, elastischer Rand
- Trägheit, Mechanik
- Trägheit, Berechnungsgrundlagen
- Trägheit, Übersicht über die Physik
- Trägheit, Smooth Animation
- Trägheit, elastischer Rand
- Smooth Animation
- elastischer Rand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be79b27900c6921c972710e7e922ab42b834afc1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309523"
---
# <a name="inertia-mechanics"></a>Trägheit-Mechanik

Trägheit wird zum Durchführen von Berechnungen für die Animation von Objekt Verschiebungen und zum Aktivieren der Unterstützung allgemeiner Nutzbarkeit in Anwendungen verwendet, die Windows-Finger Eingaben integrieren. In diesem Abschnitt werden die folgenden Funktionen veranschaulicht, die durch Trägheit aktiviert werden.

-   Eine kurze Übersicht über die Trägheit-Physik.
-   Smooth-Objekt Animation mit den Geschwindigkeits-und Verlangsamungs Eigenschaften.
-   Smooth-Objekt Animation, die eine Verschiebungs Eigenschaft verwendet.
-   Springen von den Bildschirm Kanten mit elastischen Begrenzungen.

## <a name="inertia-physics-overview"></a>Übersicht über Trägheit-Physik

Der Trägheits Prozessor verwendet ein einfaches Physik-Modell, das eine Position, einen Verlangsamungs Wert und eine anfängliche Geschwindigkeit umfasst. Die Zeit wird als dynamische Eingabe für das Modell verwendet, um die aktuelle Position eines Objekts zu ermitteln, das verschoben wird. Das folgende Diagramm und die Formel gliedern das zum Berechnen von Objektpositionen verwendete Physikmodell.

![Darstellung des Diagramms und der zum Berechnen von Objektpositionen verwendeten Formel](images/velocity.png)

In der für die Berechnung der aktuellen Position (x) verwendeten Formel wird die anfängliche Geschwindigkeit (v) mit der verstrichenen Zeit (t) multipliziert und durch den Zeitaufwand für die Verlangsamungs Faktor Zeit (d) verringert. Dies führt zu einer Smooth-Objekt Verlangsamung. In der obigen Abbildung am ursprünglichen (am weitesten links stehenden) Teil der Kurve bewegt sich das Objekt schnell, da die aktuelle Geschwindigkeit die anfängliche Geschwindigkeit ist. Am letzten (äußersten rechten) Teil der Kurve wurde das Objekt vollständig beendet, da die Geschwindigkeit 0 beträgt. Objekt Geschwindigkeits Berechnungen für die x-Geschwindigkeit, y-Geschwindigkeit und Rotationsgeschwindigkeit verwenden diese Formel für Berechnungen.

Der gesamte für den Trägheits Prozessor verwendete Abstand ist relativ. Wenn Sie Bildschirm Koordinaten verwenden möchten, übergeben Sie Bildschirm Koordinaten an den Bearbeitungs Prozessor (oder Trägheit). Wenn Sie absolute Koordinaten verwenden möchten, übergeben Sie diese an den verwendeten Prozessor. Unabhängig von den Werten, die Sie verwenden, verwendet der Manipulations Prozessor Millisekunden-Takt Einheiten, um die Zeit zu verarbeiten. Diese Werte können entweder direkt an den Trägheits Prozessor mithilfe der [**ProcessTime**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-processtime) -Methode oder mithilfe des Standardzeit Stempels durch Aufrufe der [**Verarbeitung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)übermittelt werden.

## <a name="smooth-object-animation-using-the-velocity-and-deceleration-properties"></a>Smooth-Objekt Animation mithilfe der Geschwindigkeits-und Verlangsamungs Eigenschaften

Sie können Smooth Animation aktivieren, indem Sie die Geschwindigkeit und die Verlangsamungs Werte in der Trägheits Prozessor Schnittstelle festlegen und dann [**Process**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-process)aufrufen. Durch den aufrufenden **Prozess** werden Objekt Manipulationen ausgelöst, die wiederum Aktualisierungen der Benutzeroberfläche verursachen sollten. Objekt Geschwindigkeitswerte, die an den Trägheits Prozessor übertragen werden, werden normalerweise nach Abschluss des Bearbeitungs Prozessors Der Verlangsamungs Wert ist davon abhängig, wie lange das Objekt animiert werden soll und welche Einheiten für die Berechnungen verwendet werden. Da die Werte abhängig sind, müssen Sie in einigen Fällen die Eingabe Geschwindigkeit des manierationsprozessors skalieren und beliebige Werte für die Verlangsamung verwenden. Die folgenden Werte sind typisch für verschiedene Szenarios, in denen Sie die Werte von centipixels aus den x-und y-Eigenschaften der [**TOUCHINPUT**](/windows/win32/api/winuser/ns-winuser-touchinput) -Struktur an den Manipulations Prozessor übergeben.



| Szenario    | Eigenschaftensatz                                                                       | Verlangsamungs Wert | Typische Geschwindigkeits Eingabe Skalierung                                  | Notizen                                                                                 |
|-------------|------------------------------------------------------------------------------------|--------------------|-----------------------------------------------------------------|---------------------------------------------------------------------------------------|
| Sprachübersetzung | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,003 f             | Keine.                                                           | Die Verwendung dieses Werts führt bei der Verwendung von Finger Eingaben zu längeren Entfernungs Animationen.    |
| Sprachübersetzung | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,001 f             | 1/20. anfängliche Geschwindigkeit für Berührungs Eingaben, keine für Maus Eingaben | Wenn Sie diesen Wert verwenden, wird eine Animation für ungefähr eine Sekunde mit typischen Geschwindigkeits Eingaben durchzuführen.      |
| Sprachübersetzung | [**DesiredDeceleration**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desireddeceleration)               | 0,5 f               | Keine                                                            | Die Verwendung dieses Werts sorgt für eine natürliche Darstellung der Animation auf großen Windows-Finger Eingabefenstern.   |
| Drehung    | [**Desiredangularverlangsamung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000015 f          | Bogenmaß in Grad konvertiert.                                   | Wenn Sie diesen Wert verwenden, treten bei der Verwendung von Finger Eingaben längere Rotations Animationen auf.      |
| Drehung    | [**Desiredangularverlangsamung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.00001 f           | 1/40. Drehung für Berührungs Eingaben, keine für Maus Eingaben   | Dieser Wert ist im Bogenmaße, sodass Sie sehr kleine Verlangsamungs-und Geschwindigkeitswerte verwenden müssen. |
| Drehung    | [**Desiredangularverlangsamung**](/windows/desktop/api/manipulations/nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration) | 0.000005 f          | Keine                                                            | Dieser Wert hat auf großen Windows-Finger Eingabeanzeige ein natürliches Gefühl.                        |



 

## <a name="smooth-object-animation-using-the-desired-displacement-property"></a>Smooth-Objekt Animation mit der gewünschten Verschiebungs Eigenschaft

In einigen Fällen ist es nicht sinnvoll, die Benutzereingaben für die Objekt Verschiebung zu verwenden, aber Sie möchten dennoch, dass ein Objekt auf dem Bildschirm reibungslos animiert werden kann. In diesem Fall können Sie die Verschiebungs Eigenschaften im Trägheits Prozessor verwenden, damit der Prozessor die anfängliche Geschwindigkeit zum Verschieben eines Objekts auf dem Bildschirm berechnet.

## <a name="controlling-object-position-using-elastic-bounds"></a>Steuern der Objekt Position mit elastischen Begrenzungen

Wenn Sie über ein Objekt verfügen, das sich auf dem Bildschirm befindet, sollten Sie es in der Regel beenden, bevor es den Standpunkt des Benutzers übersteigt. Der Trägheits Prozessor ermöglicht diese Funktionalität über die Eigenschaften für Grenze und elastischen Rand. In der folgenden Abbildung werden die verschiedenen Begrenzungs-und Rand Eigenschaften in einer typischen Anwendung veranschaulicht.

![Screenshot der Eigenschaften "Grenze" und "elastischer Rand"](images/elastic-illustrated.png)

Sie legen die linken, oberen, rechten und unteren Grenzen und elastischen Ränder für die Anwendung fest, und der Trägheits Prozessor behandelt die Beibehaltung von Benutzeroberflächen Elementen innerhalb der Grenzen. Wenn ein Objekt einen elastischen Rand erreicht, wird es verlangsamt, bis die Grenze erreicht ist. Dieser Rand bleibt während der Trägheit nie wieder erhalten, wird jedoch immer noch verschoben, bis die Komponente mit der senkrechten Trägheit des Objekts auf 0 (null) verlangsamt wird. In der Abbildung wird ein Kreis in Richtung der linken elastischen Grenze verschoben. Der durch vollste Pfeil zeigt die Bearbeitungsrichtung an. der voll Bild Kreis ist die Anfangsposition des Objekts. der durch vollste Pfeil ist die Änderungen, die vorgenommen werden, bevor der Kreis auf den elastischen Rand trifft. der gestrichelte Pfeil zeigt an, wo der Trägheits Prozessor den Kreis manipuliert, nachdem er den Rand erreicht hat. und die gestrichelten Kreise zeigen an, wo das Objekt beendet wird.

> [!Note]  
> Durch Festlegen der Rand Eigenschaften werden die Begrenzungen nach außen verschoben. Wenn die obere Grenze beispielsweise auf 50 festgelegt ist und Sie den oberen elastischen Rand auf 10 festlegen, wird die obere Grenze tatsächlich 40.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Behandeln von Trägheit in nicht verwaltetem Code](handling-inertia-in-unmanaged-code.md)
</dt> <dt>

[Trägheit](getting-started-with-inertia.md)
</dt> <dt>

[Manipulationen](getting-started-with-manipulations.md)
</dt> </dl>

 

 




