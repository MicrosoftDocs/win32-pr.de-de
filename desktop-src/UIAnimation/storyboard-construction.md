---
title: Übersicht über Storyboards
description: Diese Übersicht konzentriert sich darauf, wie Übergänge und Storyboards in der Windows-Animation verwendet werden.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Windows Animation Windows Animation, Storyboard (Übersicht)
- Storyboards Windows-Animation, beschrieben
- Übergänge Windows-Animation, beschrieben
- Übergänge Windows-Animation, Benutzer definiert
- Windows-Animation für Interpolatoren, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22d8e0af3937cd31ccdc43216a9d3426bad0e7b0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728104"
---
# <a name="storyboard-overview"></a>Übersicht über Storyboards

Diese Übersicht konzentriert sich darauf, wie Übergänge und Storyboards in der Windows-Animation verwendet werden. Eine Übersicht über die Komponenten der Windows-Animation finden Sie unter [Übersicht über die Windows-Animation](scenic-animation-api-overview.md).

Dieses Thema enthält folgende Abschnitte:

-   [Transitions](#custom-transitions)
    -   [Übergangs Bibliothek](#transition-library)
    -   [Benutzerdefinierte Übergänge](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Aufbau eines einfachen Storyboards](#building-a-simple-storyboard)
    -   [Verwenden einer Context-Sensitive Dauer](#using-a-context-sensitive-duration)
    -   [Entwickeln eines komplexeren Storyboards](#building-a-more-complex-storyboard)
    -   [Verwenden von Keyframes](#using-keyframes)
    -   [Halten von Variablen](#holding-variables)
    -   [Planen eines Storyboards](#scheduling-a-storyboard)
-   [Zugehörige Themen](#related-topics)

## <a name="transitions"></a>Transitions

Ein Übergang definiert, wie sich eine einzelne Animations Variable über ein bestimmtes Zeitintervall ändert. Die Windows-Animation umfasst eine Bibliothek allgemeiner Übergänge, die Entwickler auf eine oder mehrere Animations Variablen anwenden können. Verschiedene Arten von Übergängen verfügen über unterschiedliche Sätze von Parametern, die möglicherweise den Wert der Variablen nach Abschluss des Übergangs, die Dauer des Übergangs oder die für die zugrunde liegende mathematische Funktion eindeutigen Mengen enthalten, wie z. b. Beschleunigung oder Bereich der Schwingung.

Alle Übergänge haben zwei implizite Parameter gemeinsam: den Anfangswert und die anfängliche Geschwindigkeit (Steigung) der mathematischen Funktion. Diese können explizit von der Anwendung angegeben werden, werden jedoch in der Regel vom Animations-Manager auf den Wert und die Geschwindigkeit der Animations Variablen festgelegt, wenn der Übergang beginnt.

-   [Übergangs Bibliothek](#transition-library)
-   [Benutzerdefinierte Übergänge](#custom-transitions)

### <a name="transition-library"></a>Übergangs Bibliothek

Die folgenden Übergänge werden zurzeit von der Übergangs Bibliothek bereitgestellt. Wenn eine Anwendung einen Effekt erfordert, der nicht mithilfe der Übergangs Bibliothek angegeben werden kann, können Entwickler andere Arten von Übergängen erstellen, indem Sie einen benutzerdefinierten interpolators für die Anwendung implementieren oder eine Übergangs Bibliothek von einem Drittanbieter verwenden.



| Übergangs Name                        | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Beschleunigung: Verlangsamung<br/>       | Die Animations Variable beschleunigt die Geschwindigkeit und verlangsamt Sie dann über eine bestimmte Dauer.<br/>                                                                                                               |
| Konstante<br/>                    | Die Animations Variable verbleibt während des Übergangs in Ihrem Anfangswert.<br/>                                                                                                            |
| Kubisch<br/>                       | Die Animations Variable ändert sich von Ihrem Anfangswert in einen angegebenen endgültigen Wert, mit einer angegebenen endgültigen Geschwindigkeit, über eine bestimmte Dauer.<br/>                                                 |
| Discrete<br/>                    | Die Animations Variable verbleibt für eine angegebene Verzögerungszeit in Ihrem Anfangswert und wechselt dann sofort zu einem angegebenen Endwert und verbleibt bei diesem Wert für eine bestimmte haltenzeit.<br/> |
| sofortige<br/>               | Die Animations Variable ändert sich umgehend von Ihrem aktuellen Wert in einen angegebenen Endwert.<br/>                                                                                               |
| linear<br/>                      | Die Animations Variable wechselt linear von Ihrem Anfangswert in einen angegebenen Endwert über eine bestimmte Dauer.<br/>                                                                      |
| linear von der Geschwindigkeit<br/>           | Die Animations Variable wechselt linear von Ihrem Anfangswert in einen angegebenen Endwert mit einer angegebenen Geschwindigkeit.<br/>                                                                     |
| aus Beschleunigung<br/> | Die Animations Variable wechselt von Ihrem Anfangswert in einen angegebenen Endwert, mit einer angegebenen endgültigen Geschwindigkeit, wobei die Geschwindigkeit durch eine angegebene Beschleunigung geändert wird.<br/>               |
| Schluss<br/>                    | Die Richtung der Variablen ändert sich für eine bestimmte Dauer. Der endgültige Wert ist identisch mit dem Anfangswert, und die endgültige Geschwindigkeit ist der negative Wert der anfänglichen Geschwindigkeit.<br/>          |
| Sinus förmigem aus Bereich<br/>       | Die Variable wird für eine angegebene Dauer innerhalb eines angegebenen Wertebereichs mit einem angegebenen Zeitraum in der Gültigkeitsdauer in einem angegebenen Zeitraum osziert.<br/>                                                                     |
| Sinus förmigem von Velocity<br/>    | Die-Variable wird für eine angegebene Dauer mit einem angegebenen Zeitraum der Gültigkeitsdauer osziiert. Die Amplitude der Schwingung wird durch die anfängliche Geschwindigkeit der Variablen bestimmt.<br/>                      |
| Smooth-Pause<br/>                 | Die Animations Variable wird innerhalb eines maximalen Zeitraums zu einem reibungslosen Ende an einem angegebenen Endwert.<br/>                                                                              |



 

In der folgenden Tabelle sind Abbildungen für die einzelnen Übergänge enthalten.



|                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Darstellung eines sofortigen Übergangs](images/instantaneoustransition.png)  ![Abbildung eines konstanten Übergangs](images/constanttransition.png)  ![Abbildung eines linearen Übergangs](images/lineartransition.png)  ![Abbildung eines lineat-Übergangs von der Geschwindigkeit](images/lineartransitionfromspeed.png)  ![Darstellung eines diskreten Übergangs](images/discretetransition.png) |
| ![Abbildung eines Parametern, der sich von der Beschleunigung unterscheidet](images/parabolictransitionfromacceleration.png)  ![Abbildung eines kubischen Übergangs](images/cubictransition.png)  ![Abbildung eines reibungslosen Übergangs Übergangs](images/smoothstoptransition.png)                                                                                                                                       |
| ![Abbildung eines Umkehr Übergangs](images/reversaltransition.png)  ![Abbildung eines Sinus förmigem-Übergangs von der Geschwindigkeit](images/sinusolidaltransitionfromvelocity.png)  ![Abbildung eines Sinus förmigem-Übergangs vom Bereich](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![Abbildung von accellerate und verzögerenden Übergängen](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Benutzerdefinierte Übergänge

Ein *interpolators* definiert die mathematische Funktion, die bestimmt, wie sich eine Animations Variable im Laufe der Zeit ändert, wenn Sie von Ihrem Anfangswert auf einen Endwert übergeht. Jeder Übergang in der Übergangs Bibliothek verfügt über ein zugeordnetes interpolatorobjekt, das vom System bereitgestellt wird und die interpolatorfunktion implementiert. Wenn eine Anwendung einen Effekt erfordert, der nicht mithilfe der Übergangs Bibliothek angegeben werden kann, kann Sie einen oder mehrere benutzerdefinierte Übergänge implementieren, indem für jeden neuen Übergang ein interpolatorobjekt implementiert wird. Interpolatorobjekte können nicht direkt von Anwendungen verwendet werden und müssen stattdessen in einem zugeordneten Übergang umschließt werden. Eine *transitorfactory* wird verwendet, um Übergänge von einem interpolatorobjekt zu generieren. Weitere Informationen finden Sie unter [**iuianimationinterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) und [**iuianimationtransitionfactory**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory) .

Beachten Sie, dass die meisten Anwendungen über alle Übergängen verfügen, die Sie mithilfe der Übergangs Bibliothek benötigen, und daher keinen Interpolator implementieren müssen.

## <a name="storyboards"></a>Storyboards

Ein Storyboard ist eine Auflistung von Übergängen, die im Laufe der Zeit auf eine oder mehrere Animations Variablen angewendet werden. Es ist garantiert, dass die Übergänge in einem Storyboard relativ zueinander synchronisiert bleiben und dass das Storyboard als Einheit geplant oder abgebrochen wird. Nachdem Sie die gewünschten Übergänge erstellt haben, erstellt eine Anwendung mithilfe des Animations-Managers ein Storyboard, fügt die Übergänge zum Storyboard hinzu, konfiguriert das Storyboard entsprechend und plant die Wiedergabe so bald wie möglich. Der Animations-Manager bestimmt die tatsächliche Startzeit des Storyboards, da es möglicherweise zu Konflikten mit anderen Storyboards kommt, die derzeit die gleichen Variablen animieren.

Die Gesamtdauer eines Storyboards hängt von der Dauer der Übergänge innerhalb des Storyboards ab. Die Dauer eines Übergangs muss nicht korrigiert werden. Sie kann durch den Wert und die Geschwindigkeit der animierten Variablen bestimmt werden, wenn der Übergang beginnt. Daher kann die Dauer eines Storyboards auch vom Zustand der zu animierenden Variablen abhängen.

In den folgenden Beispielen wird davon ausgegangen, dass ein Animations-Manager, eine Übergangs Bibliothek und ein Timer erstellt wurden. Weitere Informationen finden Sie unter [Erstellen der Haupt Animations Objekte](adding-animation-to-an-application.md). In den Beispielen wird auch davon ausgegangen, dass die Anwendung drei Animations Variablen (X, Y und Z) mithilfe der [**iuianimationmanager:: foateanimationvariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) -Methode und fünf Übergänge (T1, T2, T3, T4 und T5) mit einer der Methoden der [**iuianimationtransitionlibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) -Schnittstelle erstellt hat.

-   [Aufbau eines einfachen Storyboards](#building-a-simple-storyboard)
-   [Verwenden einer Context-Sensitive Dauer](#using-a-context-sensitive-duration)
-   [Entwickeln eines komplexeren Storyboards](#building-a-more-complex-storyboard)
-   [Verwenden von Keyframes](#using-keyframes)
-   [Halten von Variablen](#holding-variables)
-   [Planen eines Storyboards](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Aufbau eines einfachen Storyboards

Verwenden Sie zum Erstellen eines einfachen Storyboards den [**iuianimationmanager:: die Methode "kreatestoryboard**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) " zum Erstellen eines neuen Storyboards, der [**iuianimationtransitionlibrary:: foratelineartransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) -Methode zum Erstellen eines linearen Übergangs, T1 und der [**iuianimationstoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) -Methode zum Anwenden des T1-Übergangs auf die Variable X und zum Hinzufügen des resultierenden Übergangs zum Storyboard.

Dieser Prozess ergibt ein einfaches Storyboard, wie in der folgenden Abbildung dargestellt. Das Storyboard enthält einen Übergang, T1, sodass sich der Wert von Variable X linear über eine festgelegte Zeitdauer ändert.

![Darstellung eines einfachen Storyboards mit fester Dauer](images/simplestoryboardfixedduration.png)

Beachten Sie, dass es für ein solch einfaches Szenario eine alternative Option ist, die [**iuianimationmanager:: scheduletransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) -Methode zu verwenden.

### <a name="using-a-context-sensitive-duration"></a>Verwenden einer Context-Sensitive Dauer

Während einige Übergänge eine bestimmte Dauer aufweisen, hängt die Dauer der anderen vom Anfangswert oder der Geschwindigkeit der animierten Variablen ab, wenn der Übergang beginnt. Beispielsweise erstellt die [**iuianimationtransitionlibrary:: foatelineartransitionfromspeed**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) -Methode einen Übergang mit einer Dauer, die proportional zum Unterschied zwischen dem Anfangswert der Animations Variablen und dem angegebenen Endwert ist. In dieser Abbildung und den verbleibenden Abbildungen werden solche Übergänge mit willkürlichen dauern mit einem Fragezeichen (?) angezeigt, und ihre tatsächliche Dauer wird bei der Wiedergabe des Storyboards festgelegt.

![Darstellung eines einfachen Storyboards mit einer unbekannten Dauer](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Entwickeln eines komplexeren Storyboards

Nachdem Sie ein Storyboard erstellt und einen einzelnen Übergang, T1, hinzugefügt haben, können Sie einen zweiten Übergang für die X-Variable anfügen, indem Sie die [**iuianimationstoryboard:: addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) -Methode erneut aufrufen, aber mit T2 anstelle von T1.

Vorausgesetzt, dass der T2-Übergang eine kontextabhängige Dauer aufweist, enthält das Storyboard nun zwei Back-to-Back-Übergänge der beliebigen Dauer, die die Variable X betreffen.

![Abbildung mit einem Storyboard, das zwei Übergänge in derselben Variablen enthält](images/appendingwithaddtransition.png)

Wenn Sie [**addtransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) erneut mit der Variablen Y und Transition T3 aufrufen, wird am Anfang des Storyboards ein Dritter Übergang hinzugefügt. Abhängig von den Werten von X und Y, wenn das Storyboard abgespielt wird, kann T3 nach T1 oder sogar nach T2 enden.

![Abbildung der Darstellung eines Storyboards mit Übergängen über mehrere Variablen hinweg](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Verwenden von Keyframes

Um einen Übergang am Anfang des Storyboards zu einem Offset hinzuzufügen, müssen Sie zuerst einen Keyframe hinzufügen. Keyframes stellen Zeitangaben dar und haben selbst keine Auswirkung auf das Verhalten des Storyboards. Jedes Storyboard verfügt über einen impliziten Keyframe, der den Anfang des Storyboards darstellt, das Storyboard des [**UI- \_ Animations \_ Keyframes \_ \_**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85)). Sie können neue Keyframes bei Offsets von Anfang an hinzufügen, indem Sie die [**iuianimationstoryboard:: addkeyframeatoffset**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) -Methode mit der **UI- \_ Animation \_ Keyframe \_ Storyboard \_ Start** aufrufen.

Der Offset, bei dem Sie einen Keyframe hinzufügen, ist immer relativ zu einem anderen Keyframe. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens von keyframe1 und der Übergangs T4, die auf die Variable Z angewendet, mit keyframe1 ausgerichtet und mit einer festgelegten Dauer erstellt wird. Da die Dauer der anderen Übergänge noch nicht bekannt ist, ist T4 möglicherweise nicht der letzte Übergang zum Ende.

![Abbildung zum Hinzufügen eines Übergangs, der an einem Keyframe ausgerichtet ist](images/addtransitionatkeyframe.png)

Keyframes können auch an den Enden von Übergängen mithilfe der [**iuianimationstoryboard:: addkeyframeaftertransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) -Methode platziert werden. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens von keyframe2 nach T1 und keyframe3 nach T2.

![Abbildung, die das Hinzufügen von Keyframes nach verschiedenen Übergängen anzeigt](images/addkeyframeaftertransition.png)

Da die Dauer von T1 und T2 erst bekannt ist, wenn das Storyboard abgespielt wird, werden die Offsets von keyframe2 und keyframe3 auch erst dann bestimmt. Folglich können keyframe2 und sogar keyframe3 vor keyframe1 auftreten.

Sowohl der Anfang als auch das Ende eines Übergangs können mithilfe der [**iuianimationstoryboard:: addtransitionbetweenkeyframes**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) -Methode an Keyframes ausgerichtet werden. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens eines fünften Übergangs, T5, auf Variable Y zwischen keyframe2 und keyframe3. Dadurch wird die Dauer von T5 geändert, je nach den relativen Offsets von keyframe2 und keyframe3.

![Abbildung der außerdem eines Übergangs zwischen Keyframes](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Halten von Variablen

Wenn T4 nach T2 und T5 endet, stoppt das Storyboard die Animation der Variablen X und Y, sodass Sie für andere Storyboards zum Animieren verfügbar sind. Die Anwendung kann jedoch die [**iuianimationstoryboard:: holdvariable**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) -Methode aufzurufen, um anzufordern, dass das Storyboard einige oder alle Variablen enthält, die es mit den endgültigen Werten animiert, bis das Storyboard abgeschlossen ist. Im folgenden Diagramm wird das Ergebnis der Aufbewahrung von X und Z angezeigt, wenn T4 zuletzt abgeschlossen wurde. Beachten Sie, dass das Storyboard X bis zum endgültigen Wert enthält, bis das Storyboard abgeschlossen ist. Der Halt hat keine Auswirkung auf Z, da das Storyboard endet, wenn T4 abgeschlossen ist.

![Abbildung zur Darstellung der Speicherung von Variablen an abschließenden Werten bis zum Abschluss des Storyboards](images/holdvariable.png)

Obwohl Y nicht in diesem Storyboard enthalten ist, ändert sich der Wert nicht, nachdem T5 abgeschlossen wurde, es sei denn, es wird von einem anderen Storyboard animiert. Da y nicht gehalten wird, kann jedes andere Storyboard unabhängig von der Priorität y animieren, nachdem T5 abgeschlossen wurde. Im Gegensatz dazu kann ein Storyboard mit niedrigerer Priorität x nicht animieren, bis dieses Storyboard beendet ist.

Alle diese Abbildungen haben bei der Wiedergabe des Storyboards einen beliebigen Satz aktueller Werte für die Variablen angenommen. Wenn andere Werte gefunden werden, unterscheiden sich die Dauer der kontextbezogenen Übergänge wahrscheinlich anders, wie in der folgenden Abbildung dargestellt.

![Abbildung, die das Ergebnis der Änderung der anfänglichen für die vorherige Abbildung verwendeten Bedingungen anzeigt](images/holdvariablez.png)

In diesem Szenario beginnt T5, bevor T3 abgeschlossen ist, und T3 wird daher gekürzt. Da T4 vor t2 und T5 abgeschlossen wird, wird der Wert von Z bis zum Ende des Storyboards beibehalten. Im Allgemeinen können die Werte und Geschwindigkeiten von Variablen, wenn ein Storyboard beginnt, die Keyframe-Reihenfolge und die Gesamtlänge und Form des Storyboards beeinflussen.

### <a name="scheduling-a-storyboard"></a>Planen eines Storyboards

Beim Planen eines Storyboards wird seine Startzeit durch seine Gliederung und die im Rahmen des Zeitplans aktuell konfigurierte Storyboards festgelegt. Der erste und letzte Moment, in dem das Storyboard jede einzelne Variable animiert, bestimmt, ob und wann zwei Storyboards miteinander kollidieren, aber die internen Details der Übergänge in sind nicht wichtig.

Die folgende Abbildung zeigt die Gliederung eines Storyboards mit fünf Übergängen, die drei Variablen animieren.

![Abbildung mit einem Storyboard mit fünf Übergängen, die drei Variablen animieren](images/storyboardwithoutline.png)

Ein Eckpfeiler der Windows-Animations Plattform ist die Unterstützung für die Fertigstellung einer Animation, bevor Sie ggf. eine andere startet. Obwohl dadurch viele logische Probleme vermieden werden, wird auch eine willkürliche Latenz in der Benutzeroberfläche eingeführt. Um dies zu erreichen, können Anwendungen die *am längsten akzeptable Verzögerung* für das Starten eines Storyboards angeben, indem Sie die [**iuianimationstoryboard:: setlongestaccept tabledelay**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) -Methode verwenden, und der Animations-Manager verwendet diese Informationen, um das Storyboard zu planen, bevor die angegebene Latenzzeit Spanne abläuft. Wenn ein Storyboard geplant ist, bestimmt der Animations-Manager, ob andere Storyboards zuerst abgebrochen, gekürzt, geschlossen und/oder komprimiert werden müssen.

Eine Anwendung kann einen Handler registrieren, der aufgerufen wird, wenn sich der Status eines Storyboards ändert. Dadurch kann die Anwendung Antworten, wenn das Storyboard mit der Wiedergabe beginnt, bis abgeschlossen ist, vollständig aus dem Zeitplan entfernt wird oder aufgrund einer Unterbrechung durch ein Storyboard mit höherer Priorität nicht abgeschlossen werden kann. Um die Storyboards zu identifizieren, die an Storyboard-Ereignishandler (oder Prioritäts Vergleiche) übertragen werden, kann eine Anwendung mit der [**iuianimationstoryboard:: settag**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) -Methode Tags auf Storyboards anwenden, ähnlich denen, die zum Identifizieren von Variablen verwendet werden können. Wie bei der Wiederverwendung von Storyboards müssen Entwickler bei der Verwendung von Tags zur Identifizierung von Storyboards Vorsicht walten lassen und sicherstellen, dass Mehrdeutigkeiten nicht auftreten, wenn Benutzeraktionen dazu führen, dass viele Storyboards in die Warteschlange eingereiht werden.

Die folgenden Beispiele zeigen zwei Variationen des Versuchs, das Storyboard zu planen, das in den vorherigen Abschnitten dieses Themas erstellt wurde.

In diesem Szenario wurden sechs Storyboards a bis F bereits zum Animieren der Variablen "W", "X", "Y" und "Z" eingeplant, aber nur "A" und "B" wurden gestartet. Das neue Storyboard mit der Bezeichnung G hat die längste zulässige Verzögerung auf die in der folgenden Abbildung gezeigte Dauer festgelegt.

![Abbildung der Addition eines neuen Storyboards zum vorhandenen Zeitplan](images/existingschedule1withlines.png)

Die Anwendung hat Prioritäts Vergleiche registriert, die folgende Logik einschließen:

-   Mit G können nur C und E abgebrochen werden, und nur um Fehler zu verhindern.
-   Mit G können nur A, C, E und F beschnitten werden, und nur um Fehler zu verhindern.
-   Jedes Storyboard kann beliebige andere Storyboards komprimieren (die Komprimierung wird immer nur durchgeführt, um Fehler zu verhindern).

> [!Note]  
> Der Qualifizierer "nur zum Verhindern von Fehlern" bedeutet, dass die registrierten Prioritäts Vergleiche "S OK" nur dann zurückgeben, \_ Wenn der *priorityeffect* -Parameter einen **\_ \_ \_ \_ Fehler** bei der Benutzeroberflächen Animation Ausführliche Informationen finden Sie in der [**iuianimationprioritycomparison:: haspriority**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority) -Methode.

 

Um G zu starten, bevor die am längsten akzeptable Verzögerung verstrichen ist, muss der Animations-Manager folgende Aktionen ausführen:

-   Trim F
-   E Abbrechen

Wenn E abgebrochen wird, werden D und F gelöscht und auf ihre ursprünglichen umrissen zurückgesetzt:

![Darstellung der ursprünglichen umrissen](images/existingschedule1bwithlines.png)

Der Animations-Manager muss C nicht abbrechen oder kürzen, bevor die am längsten akzeptable Verzögerung abgelaufen ist, sodass die Besprechung von c und g festlegt, wann G gestartet wird.

![Abbildung, die anzeigt, dass f gekürzt wird, damit c und g erreicht werden können](images/schedule1withgwithlines.png)

Nachdem G erfolgreich geplant wurde, können die Dauer der Übergänge bestimmt werden, und der Rest der Gliederung ist daher bekannt. Der Umriss kann sich jedoch ändern, wenn ein anderes Storyboard nachfolgend aus dem Zeitplan entfernt wird.

Sehen Sie sich als zweites Beispiel ein Szenario wie das obige an, aber mit einer kürzeren, am längsten zulässigen Verzögerung für G.

![Darstellung des vorherigen Szenarios, aber mit einer kürzeren, längsten akzeptablen Verzögerung für g](images/existingschedule2withlines.png)

In diesem Fall werden die folgenden Aktionen durchgeführt:

-   Trim F
-   E Abbrechen
-   Abbrechen von C

Außerdem muss der Animations-Manager D mit dem angezeigten Betrag komprimieren, damit G nach seiner längsten akzeptablen Verzögerung gestartet werden kann.

![Abbildung, die anzeigt, wo d komprimiert werden muss, damit g mit der längsten akzeptablen Verzögerung gestartet werden kann](images/trimmedandcancelledwithlines.png)

Um die relative zeitliche Steuerung beizubehalten, werden A, B und F ebenfalls komprimiert.

![Abbildung, die die Komprimierung a, b, d und f zeigt](images/schedule2withgwithlines.png)

Storyboards für nicht verknüpfte Variablen (nicht angezeigt) werden jedoch nicht komprimiert.

Der Umriss von g ist nun bekannt und unterscheidet sich vom Ergebnis im ersten Szenario, da die Variablen unterschiedliche Werte aufweisen, wenn G beginnt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iuianimationmanager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**Iuianimationprioritycomparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**Iuianimationstoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**Iuianimationtransitionlibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

