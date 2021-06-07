---
title: Übersicht über Storyboards
description: Diese Übersicht konzentriert sich darauf, wie Übergänge und Storyboards in der Windows-Animation verwendet werden.
ms.assetid: d37718ac-0256-4a24-a26c-d29173593be0
keywords:
- Windows-Animation Windows-Animation, Übersicht über Storyboards
- Storyboards Windows-Animation , beschrieben
- Übergängen der Windows-Animation , beschrieben
- übergehende Windows-Animation , benutzerdefiniert
- Interpolatoren Windows-Animation , beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58210ae98f6d3a96c554276466ad72b3364d72a1
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524284"
---
# <a name="storyboard-overview"></a>Übersicht über Storyboards

Diese Übersicht konzentriert sich darauf, wie Übergänge und Storyboards in der Windows-Animation verwendet werden. Eine Übersicht über die Komponenten der Windows-Animation finden Sie unter [Übersicht über Windows-Animationen.](scenic-animation-api-overview.md)

Dieses Thema enthält folgende Abschnitte:

-   [Transitions](#custom-transitions)
    -   [Übergangsbibliothek](#transition-library)
    -   [Benutzerdefinierte Übergänge](#custom-transitions)
-   [Storyboards](#storyboards)
    -   [Erstellen eines einfachen Storyboards](#building-a-simple-storyboard)
    -   [Verwenden einer Context-Sensitive Dauer](#using-a-context-sensitive-duration)
    -   [Erstellen eines komplexeren Storyboards](#building-a-more-complex-storyboard)
    -   [Verwenden von Keyframes](#using-keyframes)
    -   [Halten von Variablen](#holding-variables)
    -   [Planen eines Storyboards](#scheduling-a-storyboard)
-   [Verwandte Themen](#related-topics)

## <a name="transitions"></a>Transitions

Ein Übergang definiert, wie sich eine einzelne Animationsvariable in einem bestimmten Zeitintervall ändert. Die Windows-Animation enthält eine Bibliothek allgemeiner Übergänge, die Entwickler auf eine oder mehrere Animationsvariablen anwenden können. Verschiedene Arten von Übergängen verfügen über unterschiedliche Sätze von Parametern, z. B. den Wert der Variablen nach Abschluss des Übergangs, die Dauer des Übergangs oder die Mengen, die für die zugrunde liegende mathematische Funktion eindeutig sind, z. B. Beschleunigung oder Oszillationsbereich.

Alle Übergänge verwenden zwei implizite Parameter: den Anfangswert und die Anfängliche Geschwindigkeit (Steigung) der mathematischen Funktion. Diese können explizit von der Anwendung angegeben werden, werden jedoch in der Regel vom Animations-Manager auf den Wert und die Geschwindigkeit der Animationsvariablen festgelegt, wenn der Übergang beginnt.

-   [Übergangsbibliothek](#transition-library)
-   [Benutzerdefinierte Übergänge](#custom-transitions)

### <a name="transition-library"></a>Übergangsbibliothek

Die folgenden Übergänge werden derzeit von der Übergangsbibliothek bereitgestellt. Wenn eine Anwendung einen Effekt erfordert, der nicht mithilfe der Übergangsbibliothek angegeben werden kann, können Entwickler andere Arten von Übergängen erstellen, indem sie einen benutzerdefinierten Interpolator für die Anwendung implementieren oder eine Übergangsbibliothek von einem Drittanbieter verwenden.



| Übergangsname                        | BESCHREIBUNG                                                                                                                                                                                          |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| beschleunigungsentschleunigen<br/>       | Die Animationsvariable beschleunigt und verlangsamt sich dann über einen bestimmten Zeitraum.<br/>                                                                                                               |
| Konstante<br/>                    | Die Animationsvariable verbleibt während des Übergangs am Anfangswert.<br/>                                                                                                            |
| Kubisch<br/>                       | Die Animationsvariable ändert sich über einen bestimmten Zeitraum von ihrem Anfangswert in einen angegebenen Endwert mit einer angegebenen Endgeschwindigkeit.<br/>                                                 |
| Diskrete<br/>                    | Die Animationsvariable verbleibt während einer angegebenen Verzögerungszeit am Anfangswert, wechselt dann sofort zu einem angegebenen endgültigen Wert und bleibt für eine bestimmte Wartezeit bei diesem Wert.<br/> |
| Momentanen<br/>               | Die Animationsvariable ändert sich sofort von ihrem aktuellen Wert in einen angegebenen endgültigen Wert.<br/>                                                                                               |
| linear<br/>                      | Die Animationsvariable wechselt über einen bestimmten Zeitraum linear von ihrem Anfangswert zu einem angegebenen Endwert.<br/>                                                                      |
| linear von der Geschwindigkeit<br/>           | Die Animationsvariable wechselt linear von ihrem Anfangswert zu einem angegebenen Endgültigen Wert mit einer angegebenen Geschwindigkeit.<br/>                                                                     |
| Parabolisch von der Beschleunigung<br/> | Die Animationsvariable wechselt von ihrem Anfangswert zu einem angegebenen endgültigen Wert mit einer angegebenen Endgeschwindigkeit und ändert ihre Geschwindigkeit mit einer angegebenen Beschleunigung.<br/>               |
| Umkehrung<br/>                    | Die Variable ändert die Richtung über einen bestimmten Zeitraum. Der endgültige Wert entspricht dem Anfangswert, und die endgültige Geschwindigkeit ist die negative der anfänglichen Geschwindigkeit.<br/>          |
| sinusoidal aus Bereich<br/>       | Die Variable oszilliert innerhalb eines bestimmten Wertebereichs mit einem angegebenen Oszillationszeitraum für einen bestimmten Zeitraum.<br/>                                                                     |
| Sinusoidal von Geschwindigkeit<br/>    | Die Variable oszilliert für einen bestimmten Zeitraum mit einem angegebenen Oszillationszeitraum. Die Amplitude der Oszillation wird durch die Anfängliche Geschwindigkeit der Variablen bestimmt.<br/>                      |
| Smooth Stop<br/>                 | Die Animationsvariable erreicht einen reibungslosen Stopp an einem angegebenen Endwert innerhalb einer maximalen Zeitspanne.<br/>                                                                              |



 

Die folgende Tabelle enthält Abbildungen für jeden dieser Übergänge.



|    Abbildungen                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ![Abbildung eines sofortigen Übergangs](images/instantaneoustransition.png)  ![Abbildung eines konstanten Übergangs](images/constanttransition.png)  ![Abbildung eines linearen Übergangs](images/lineartransition.png)  ![Abbildung eines Lineatübergangs von der Geschwindigkeit](images/lineartransitionfromspeed.png)  ![Abbildung eines diskreten Übergangs](images/discretetransition.png) |
| ![Abbildung eines parabolischen Übergangs von der Beschleunigung](images/parabolictransitionfromacceleration.png)  ![Abbildung eines kubischen Übergangs](images/cubictransition.png)  ![Abbildung eines reibungslosen Stoppübergangs](images/smoothstoptransition.png)                                                                                                                                       |
| ![Abbildung eines Umkehrübergangs](images/reversaltransition.png)  ![Abbildung eines sinusförmigen Übergangs von der Geschwindigkeit](images/sinusolidaltransitionfromvelocity.png)  ![Abbildung eines sinusförmigen Übergangs vom Bereich](images/sinusolidaltransitionfromrange.png)                                                                                                                  |
| ![Abbildung von Beschleunigungs- und Verlangsamungsübergängen](images/acceleratedeceleratetransition.png)                                                                                                                                                                                                                                                                                               |



 

### <a name="custom-transitions"></a>Benutzerdefinierte Übergänge

Ein *Interpolator* definiert die mathematische Funktion, die bestimmt, wie sich eine Animationsvariable im Laufe der Zeit ändert, während sie von ihrem Anfangswert zu einem endgültigen Wert wechselt. Jeder Übergang in der Übergangsbibliothek verfügt über ein zugeordnetes Interpolatorobjekt, das vom System bereitgestellt wird und die Interpolatorfunktion implementiert. Wenn eine Anwendung einen Effekt erfordert, der nicht mithilfe der Übergangsbibliothek angegeben werden kann, kann sie einen oder mehrere benutzerdefinierte Übergänge implementieren, indem ein Interpolatorobjekt für jeden neuen Übergang implementiert wird. Interpolatorobjekte können nicht direkt von Anwendungen verwendet werden und müssen stattdessen von einem zugeordneten Übergang umschlossen werden. Eine *Übergangsfactory* wird verwendet, um Übergänge von einem Interpolatorobjekt zu generieren. Weitere Informationen finden Sie unter [**IUIAnimationInterpolator**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationinterpolator) und [**IUIAnimationTransitionFactory.**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionfactory)

Beachten Sie, dass die meisten Anwendungen alle benötigten Übergänge mithilfe der Übergangsbibliothek aufweisen und daher keinen Interpolator implementieren müssen.

## <a name="storyboards"></a>Storyboards

Ein Storyboard ist eine Sammlung von Übergängen, die im Laufe der Zeit auf eine oder mehrere Animationsvariablen angewendet werden. Die Übergänge in einem Storyboard bleiben garantiert relativ zueinander synchronisiert, und das Storyboard wird als Einheit geplant oder abgebrochen. Nachdem die gewünschten Übergänge erstellt wurden, erstellt eine Anwendung ein Storyboard mithilfe des Animations-Managers, fügt die Übergänge zum Storyboard hinzu, konfiguriert das Storyboard entsprechend und plant es so bald wie möglich ab. Der Animations-Manager bestimmt die tatsächliche Startzeit des Storyboards, da es möglicherweise Konflikte mit anderen Storyboards gibt, die derzeit die gleichen Variablen animieren.

Die Gesamtdauer eines Storyboards hängt von der Dauer der Übergänge innerhalb des Storyboards ab. Die Dauer eines Übergangs muss nicht festgelegt werden. Sie kann durch den Wert und die Geschwindigkeit der animierten Variablen bestimmt werden, wenn der Übergang beginnt. Daher kann die Dauer eines Storyboards auch vom Zustand der Variablen abhängen, die es animiert.

In den folgenden Beispielen wird davon ausgegangen, dass ein Animations-Manager, eine Übergangsbibliothek und ein Timer erstellt wurden. Weitere Informationen finden Sie unter [Erstellen der Hauptanimationsobjekte.](adding-animation-to-an-application.md) In den Beispielen wird auch davon ausgegangen, dass die Anwendung drei Animationsvariablen (X, Y und Z) mithilfe der [**IUIAnimationManager::CreateAnimationVariable-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createanimationvariable) und fünf Übergänge (T1, T2, T3, T4 und T5) erstellt hat, indem eine der Methoden der [**IUIAnimationTransitionLibrary-Schnittstelle**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary) verwendet wird.

-   [Erstellen eines einfachen Storyboards](#building-a-simple-storyboard)
-   [Verwenden einer Context-Sensitive Dauer](#using-a-context-sensitive-duration)
-   [Erstellen eines komplexeren Storyboards](#building-a-more-complex-storyboard)
-   [Verwenden von Keyframes](#using-keyframes)
-   [Halten von Variablen](#holding-variables)
-   [Planen eines Storyboards](#scheduling-a-storyboard)

### <a name="building-a-simple-storyboard"></a>Erstellen eines einfachen Storyboards

Verwenden Sie zum Erstellen eines einfachen Storyboards die [**IUIAnimationManager::CreateStoryboard-Methode,**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-createstoryboard) um ein neues Storyboard, die [**IUIAnimationTransitionLibrary::CreateLinearTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransition) zum Erstellen eines linearen Übergangs T1 und die [**IUIAnimationStoryboard::AddTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) zu erstellen, um den T1-Übergang auf die Variable X anzuwenden und den resultierenden Übergang zum Storyboard hinzuzufügen.

Dieser Prozess ergibt ein einfaches Storyboard, wie in der folgenden Abbildung dargestellt. Das Storyboard enthält einen Übergang, T1, damit sich der Wert der Variablen X über einen festen Zeitraum linear ändert.

![Abbildung eines einfachen Storyboards mit fester Dauer](images/simplestoryboardfixedduration.png)

Beachten Sie, dass für ein so einfaches Szenario eine alternative Option die Verwendung der [**IUIAnimationManager::ScheduleTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationmanager-scheduletransition) ist.

### <a name="using-a-context-sensitive-duration"></a>Verwenden einer Context-Sensitive Dauer

Während einige Übergänge eine feste Dauer haben, hängt die Dauer von anderen vom Anfangswert oder der Geschwindigkeit der animierten Variablen ab, wenn der Übergang beginnt. Beispielsweise erstellt die [**IUIAnimationTransitionLibrary::CreateLinearTransitionFromSpeed-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationtransitionlibrary-createlineartransitionfromspeed) einen Übergang mit einer Dauer, die proportional zum Unterschied zwischen dem Anfangswert der Animationsvariablen und dem angegebenen enden Wert ist. In dieser Abbildung und den verbleibenden Abbildungen werden solche Übergänge mit willkürlichen Daueren mit einem Fragezeichen (?) dargestellt, und ihre tatsächliche Dauer wird bestimmt, wenn das Storyboard abspielt.

![Abbildung eines einfachen Storyboards mit unbekannter Dauer](images/simplestoryboardunknownduration.png)

### <a name="building-a-more-complex-storyboard"></a>Erstellen eines komplexeren Storyboards

Nachdem Sie ein Storyboard erstellt und einen einzelnen Übergang T1 hinzugefügt haben, können Sie einen zweiten Übergang für die X-Variable anfügen, indem Sie die [**IUIAnimationStoryboard::AddTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) erneut aufrufen, jedoch mit T2 anstelle von T1.

Angenommen, der T2-Übergang hat eine dauer, die kontextsensible ist, enthält das Storyboard nun zwei Back-to-Back-Übergänge mit beliebiger Dauer, die sich auf die Variable X beeinflussen.

![Abbildung eines Storyboards, das zwei Übergänge für dieselbe Variable enthält](images/appendingwithaddtransition.png)

Durch [**das erneute Aufrufen von AddTransition**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransition) mit der Variablen Y und dem Übergang T3 wird am Anfang des Storyboards ein dritter Übergang hinzugefügt. Abhängig von den Werten von X und Y, wenn das Storyboard abspielt, kann T3 nach T1 oder sogar nach T2 enden.

![Abbildung eines Storyboards, das Übergänge über mehrere Variablen hinweg enthält](images/multivariablestoryboard.png)

### <a name="using-keyframes"></a>Verwenden von Keyframes

Um einen Übergang an einem Offset vom Anfang des Storyboards hinzuzufügen, müssen Sie zuerst einen Keyframe hinzufügen. Keyframes stellen Zeitpunkte dar und haben selbst keine Auswirkungen auf das Verhalten des Storyboards. Jedes Storyboard verfügt über einen impliziten Keyframe, der den Anfang des Storyboards darstellt, [**UI \_ ANIMATION \_ KEYFRAME \_ STORYBOARD \_ START.**](/previous-versions/windows/desktop/legacy/dd756780(v=vs.85))Sie können neue Keyframes bei Offsets von Anfang hinzufügen, indem Sie die [**IUIAnimationStoryboard::AddKeyframeAtOffset-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeatoffset) mit **UI ANIMATION \_ \_ KEYFRAME \_ STORYBOARD START \_ aufrufen.**

Der Offset, an dem Sie einen Keyframe hinzufügen, ist immer relativ zu einem anderen Keyframe. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens von keyframe1 und transition T4, das auf die Variable Z angewendet, an keyframe1 ausgerichtet und mit einer festen Dauer erstellt wird. Da die Dauer der anderen Übergänge noch nicht bekannt ist, ist T4 möglicherweise nicht der letzte abgeschlossene Übergang.

![Abbildung, die das Hinzufügen eines an einem Keyframe ausgerichteten Übergangs zeigt](images/addtransitionatkeyframe.png)

Keyframes können auch mithilfe der [**IUIAnimationStoryboard::AddKeyframeAfterTransition-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addkeyframeaftertransition) an den Enden von Übergängen platziert werden. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens von keyframe2 nach T1 und keyframe3 nach T2.

![Abbildung, die das Hinzufügen von Keyframes nach verschiedenen Übergängen zeigt](images/addkeyframeaftertransition.png)

Da die Dauer von T1 und T2 erst bekannt ist, wenn das Storyboard abspielt, werden die Offsets von keyframe2 und keyframe3 bis dahin ebenfalls nicht bestimmt. Folglich können keyframe2 und sogar keyframe3 vor keyframe1 auftreten.

Sowohl der Anfang als auch das Ende eines Übergangs können mithilfe der [**IUIAnimationStoryboard::AddTransitionBetweenKeyframes-Methode an Keyframes ausgerichtet**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-addtransitionbetweenkeyframes) werden. Das folgende Diagramm zeigt das Ergebnis des Hinzufügens eines fünften Übergangs(T5) für die Variable Y zwischen keyframe2 und keyframe3. Dadurch ändert sich die Dauer von T5, wodurch sie je nach relativen Offsets von keyframe2 und keyframe3 länger oder kürzer wird.

![Abbildung, die den Zusatz eines Übergangs zwischen Keyframes zeigt](images/addtransitionbetweenkeyframes.png)

### <a name="holding-variables"></a>Halten von Variablen

Wenn T4 nach T2 und T5 endet, beendet das Storyboard die Animation der Variablen X und Y und macht sie für andere Storyboards zum Animieren verfügbar. Die Anwendung kann jedoch die [**IUIAnimationStoryboard::HoldVariable-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-holdvariable) aufrufen, um an fordern, dass das Storyboard einige oder alle Variablen enthält, die es an seinen endgültigen Werten animiert, bis das Storyboard abgeschlossen ist. Das folgende Diagramm zeigt das Ergebnis des Haltens von X und Z, wenn T4 zuletzt abgeschlossen ist. Beachten Sie, dass das Storyboard X am endgültigen Wert enthält, bis das Storyboard abgeschlossen ist. Der Hold hat keine Auswirkungen auf Z, da das Storyboard endet, wenn T4 abgeschlossen ist.

![Abbildung, die das Halten von Variablen an den endgültigen Werten zeigt, bis das Storyboard abgeschlossen ist](images/holdvariable.png)

Auch wenn Y nicht von diesem Storyboard gehalten wird, ändert sich der Wert nach Abschluss von T5 nicht, es sei denn, es wird von einem anderen Storyboard animiert. Da Y nicht gehalten wird, kann jedes andere Storyboard unabhängig von der Priorität Y animieren, nachdem T5 abgeschlossen wurde. Da X dagegen gehalten wird, kann ein Storyboard mit niedrigerer Priorität X erst animieren, wenn dieses Storyboard fertig ist.

Alle diese Abbildungen haben angenommen, dass ein beliebiger Satz aktueller Werte für die Variablen verwendet wird, wenn das Storyboard abspielt. Wenn andere Werte gefunden werden, ist die Dauer der kontextsensitiven Übergänge wahrscheinlich unterschiedlich, wie in der folgenden Abbildung dargestellt.

![Abbildung, die das Ergebnis der Änderung der Anfangsbedingungen zeigt, die für die vorherige Abbildung verwendet wurden](images/holdvariablez.png)

In diesem Szenario beginnt T5, bevor T3 abgeschlossen ist, und T3 wird daher gekürzt. Da T4 vor T2 und T5 abgeschlossen ist, wird der Wert von Z bis zum Ende des Storyboards gehalten. Im Allgemeinen können sich die Werte und Geschwindigkeiten von Variablen beim Starten der Wiedergabe eines Storyboards auf die Keyframe-Reihenfolge und die Gesamtlänge und -form des Storyboards auswirken.

### <a name="scheduling-a-storyboard"></a>Planen eines Storyboards

Beim Planen eines Storyboards wird die Startzeit durch seine Kontur und die Konturen der Storyboards bestimmt, die sich derzeit im Zeitplan befinden. Insbesondere der erste und letzte Moment, in dem das Storyboard jede einzelne Variable animiert, bestimmt, ob und wann zwei Storyboards kollidieren, aber die internen Details der Übergänge in sind nicht wichtig.

Die folgende Abbildung zeigt die Gliederung eines Storyboards mit fünf Übergängen, die drei Variablen animieren.

![Abbildung eines Storyboards mit fünf Übergängen, die drei Variablen animieren](images/storyboardwithoutline.png)

Ein Wichtiger Bestandteil der Windows-Animationsplattform ist die Unterstützung dafür, dass eine Animation bei Bedarf abgeschlossen werden kann, bevor eine andere beginnt. Dies beseitigt zwar viele logische Probleme, führt aber auch zu einer beliebigen Latenz in der Benutzeroberfläche. Um dies zu adressieren, können Anwendungen die längste akzeptable Verzögerung für den Start eines Storyboards angeben, indem sie die [**IUIAnimationStoryboard::SetLongestAcceptableDelay-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-setlongestacceptabledelay) verwenden, und der Animations-Manager verwendet diese Informationen, um das Storyboard vor Ablauf des angegebenen Latenzzeitraums zu planen.  Wenn ein Storyboard geplant ist, bestimmt der Animations-Manager, ob andere Storyboards zuerst abgebrochen, gekürzt, abgeschlossen und/oder komprimiert werden müssen.

Eine Anwendung kann einen Handler registrieren, der aufgerufen wird, wenn sich der Status eines Storyboards ändert. Dadurch kann die Anwendung reagieren, wenn die Wiedergabe des Storyboards beginnt, bis zum Abschluss ausgeführt wird, vollständig aus dem Zeitplan entfernt wird oder aufgrund einer Unterbrechung durch ein Storyboard mit höherer Priorität am Abschluss gehindert wird. Um die Storyboards zu identifizieren, die an Storyboard-Ereignishandler (oder Prioritätsvergleiche) übergeben werden, kann eine Anwendung die [**IUIAnimationStoryboard::SetTag-Methode**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationstoryboard-settag) verwenden, um Tags auf Storyboards anzuwenden, ähnlich denen, die zum Identifizieren von Variablen verwendet werden können. Wie bei der Wiedervernutzung von Storyboards müssen Entwickler bei der Verwendung von Tags zum Identifizieren von Storyboards Vorsicht walten lassen und sicherstellen, dass es nicht zu Mehrdeutigkeiten kommt, wenn Benutzeraktionen dazu führen, dass viele Storyboards in die Warteschlange gestellt werden.

Die folgenden Beispiele zeigen zwei Variationen eines Versuchs, das in den früheren Abschnitten dieses Themas integrierte Storyboard zu planen.

In diesem Szenario wurden bereits sechs Storyboards ( A bis F) geplant, um die Variablen W, X, Y und Z zu animieren, aber nur A und B haben mit der Wiedergabe begonnen. Für das neue Storyboard mit der Bezeichnung G ist die längste zulässige Verzögerung auf die in der folgenden Abbildung dargestellte Dauer festgelegt.

![Abbildung, die das Addition eines neuen Storyboards zum vorhandenen Zeitplan zeigt](images/existingschedule1withlines.png)

Die Anwendung verfügt über registrierte Prioritätsvergleiche, die die folgende Logik enthalten:

-   G kann nur C und E abbrechen und nur, um Fehler zu verhindern.
-   G kann nur A, C, E und F kürzen, und nur, um Fehler zu verhindern.
-   Jedes Storyboard kann jedes andere Storyboard komprimieren (die Komprimierung erfolgt immer nur, um Fehler zu verhindern).

> [!Note]  
> Der Qualifizierer "nur zum Verhindern eines Fehlers" bedeutet, dass die registrierten Prioritätsvergleiche nur dann S OK zurückgeben, wenn der \_ *priorityEffect-Parameter* **UI ANIMATION PRIORITY EFFECT FAILURE \_ \_ \_ \_ ist.** Weitere Informationen finden Sie unter [**IUIAnimationPriorityComparison::HasPriority-Methode.**](/windows/desktop/api/UIAnimation/nf-uianimation-iuianimationprioritycomparison-haspriority)

 

Um G zu starten, bevor die längste akzeptable Verzögerung verstrichen ist, muss der Animations-Manager Folgendes tun:

-   Kürzen von F
-   Abbrechen E

Wenn E abgebrochen wird, werden D und F entdeckt und auf ihre ursprünglichen Konturen zurückverwendet:

![Abbildung mit ursprünglichen Konturen](images/existingschedule1bwithlines.png)

Der Animations-Manager muss C nicht abbrechen oder kürzen, bevor die längste akzeptable Verzögerung verstrichen ist. Daher bestimmt die Besprechung von C und G, wann G gestartet wird.

![Abbildung, die zeigt, dass f abgeschnitten wird, damit c und g erfüllt werden können](images/schedule1withgwithlines.png)

Nachdem G erfolgreich geplant wurde, kann die Dauer der Übergänge bestimmt werden, und der Rest der Kontur ist daher bekannt. Die Gliederung kann sich jedoch ändern, wenn anschließend ein anderes Storyboard aus dem Zeitplan entfernt wird.

Betrachten Sie als zweites Beispiel ein Szenario wie das oben beschriebene, aber mit einer kürzeren, längsten akzeptablen Verzögerung, die für G angegeben ist.

![Abbildung des vorherigen Szenarios, jedoch mit einer kürzeren längsten akzeptablen Verzögerung für g](images/existingschedule2withlines.png)

In diesem Fall werden die folgenden Aktionen durchgeführt:

-   Kürzen von F
-   Abbrechen E
-   Abbrechen C

Außerdem muss der Animations-Manager D um den angezeigten Betrag komprimieren, damit G nach der längsten akzeptablen Verzögerung und nicht später gestartet werden kann.

![Abbildung, die zeigt, wo d komprimiert werden muss, damit g bei der längsten zulässigen Verzögerung beginnen kann](images/trimmedandcancelledwithlines.png)

Zur A-, B- und F-Komprimierung werden auch die relativen Zeitsteuerungen beibehalten.

![Abbildung, die eine komprimierte a-, b-, d- und f-Komprimierung zeigt](images/schedule2withgwithlines.png)

Storyboards in nicht verknüpften Variablen (nicht dargestellt) würden jedoch nicht komprimiert.

Auch hier ist die Kontur von G jetzt bekannt und ist anders als das Ergebnis im ersten Szenario, da die Variablen zu Beginn von G unterschiedliche Werte haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IUIAnimationManager**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationmanager)
</dt> <dt>

[**IUIAnimationPriorityComparison**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationprioritycomparison)
</dt> <dt>

[**IUIAnimationStoryboard**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationstoryboard)
</dt> <dt>

[**IUIAnimationTransitionLibrary**](/windows/desktop/api/UIAnimation/nn-uianimation-iuianimationtransitionlibrary)
</dt> </dl>

 

