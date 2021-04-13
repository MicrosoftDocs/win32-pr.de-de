---
title: Animationen
description: Animationen
ms.assetid: 8bd9ac94-3f86-4168-bf33-7a2c8d11907d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf1b9f5e8daa320390f5c19c3c4c27cb8195a8fe
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "104560729"
---
# <a name="animations"></a>Animationen

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Animationen eines Zeichens entsprechen Geschlecht, Alter, Persönlichkeit und Verhalten. Die Anzahl und die Typen von Animationen, die Sie für ein Zeichen erstellen, hängen davon ab, was Ihr Zeichen tut und wie es auf verschiedene Situationen reagiert.

Wie herkömmliche Animationen beinhalten digitale Animationen das Erstellen einer Reihe von leicht abweichenden Bildern, die, wenn Sie sequenziell angezeigt werden, die Illusion der Aktion bereitstellen. Die Erstellung hochwertiger Animations Bilder erfordert möglicherweise einen qualifizierten Animator, aber der Stil und die Darstellung des von Ihnen erstellten Zeichens wirken sich auch auf die Qualität aus. Zweidimensionale Zeichen mit einfachen Formen und Features können in manchen Fällen so effektiv wie die hoch gerenderten Zeichen (oder effektiver als) sein. Es ist nicht erforderlich, ein realistisches Bild zu erstellen, um ein effektives Zeichen darzustellen. Viele gängige Zeichen in Zeichen sind in Ihrer Präsentation nicht realistisch, aber Sie sind effektiv, da der Animator weiß, wie Aktionen und Emotionen vermittelt werden. Der Anhang enthält allgemeine Informationen zu grundlegenden Animations Entwurfs Prinzipien.

### <a name="frames"></a>Frames

Jede Animation, die Sie für ein Microsoft-agentzeichen erstellen, besteht aus einer zeitgesteuerten Sequenz von Frames. Jeder Frame in der Animation besteht aus mindestens einem Bitmap-Bild. Bilder können so klein sein, wie Sie benötigen, oder so groß wie der Frame selbst.

Animations Details, wie z. b. Eye blinkt oder Fingerbewegung, können als zusätzliche Bilder für den Frame eingefügt werden. Sie können mehrere Bilder überlagern, um einen zusammengesetzten zu erstellen und ihre Position in den Ebenen zu verändern. Mit dieser Methode können Sie Images in mehreren Frames wieder verwenden und die Details ändern, die sich ändern. Wenn Sie z. b. ein Zeichen in der Hand haben möchten, können Sie für jeden Frame ein Basis Bild mit allem, aber der Hand verwenden und das Basis Bild mit einem anderen Hand Bild überlagern. Wenn Sie das Zeichen Blinzeln machen möchten, können Sie auch einen anderen Satz von Augen über ein Basis Bild für jeden Frame überlagern. Bilder können auch aus dem Basis Image versetzt werden. Es wird jedoch nur der Teil des Bilds angezeigt, der innerhalb der Rahmengröße vorhanden ist.

Sie können beliebig viele Frames in einer Animation enthalten. eine typische Animation durchschnittlich ungefähr 14 Frames, sodass Sie nicht mehr als sechs Sekunden dauert. Diese bescheidene Zeitspanne stellt sicher, dass Ihr Zeichen in der Benutzereingabe reaktionsfähig erscheint. Je größer die Anzahl der Frames, desto größer ist die Animations Datei. Bei heruntergeladenen webbasierten Zeichen behalten Sie die Größe Ihrer Animations Datei so klein wie möglich bei, während Sie immer noch einen relativ großen Satz von Frames bereitstellen, sodass die Animation des Zeichens nicht ruckartig erscheint.

### <a name="image-design"></a>Bild Entwurf

Sie können ein beliebiges Grafik-oder Animations Tool zum Erstellen von Bildern für Animations Frames verwenden, vorausgesetzt, dass Sie die abschließenden Bilder in der Windows-Bitmap () speichern. BMP) formatieren. Wenn die Images erstellt werden, verwenden Sie den Zeichen-Editor von Microsoft-Agent (verfügbar im [Download](https://www.microsoft.com/download/en/details.aspx?id=14765)Programm), um die Bilder zusammenzustellen, zu sequenzieren und zu warten, andere Zeichen Informationen anzugeben und alle Informationen in eine endgültige Zeichen Datei zu kompilieren.

Zeichen Bilder müssen auf eine 256-farbige Palette ausgelegt sein, wobei die 20 standardmäßigen Windows-Systemfarben an ihrer Standardposition in der Palette (die ersten 10 und die letzten 10 Positionen) beibehalten werden. Dies bedeutet, dass die Farbpalette Ihres Zeichens die Standardsystem Farben und bis zu 236 andere Farben verwenden kann. Fügen Sie beim Definieren der Palette alle von Ihrem Zeichen in der Animation verwendeten Eigenschaften ein. Wenn die Palette Ihres Zeichens Farben in den System Farb Positionen platziert, werden diese Zeichen Farben mit den Systemfarben überschrieben, wenn der Microsoft-Agent die Palette erstellt.

Je größer die Anzahl der Farben in der Farbpalette eines Zeichens ist, desto größer ist die Wahrscheinlichkeit, dass ein Teil der Farben Ihres Zeichens für Systeme neu zugeordnet werden kann, die für eine 8-Bit-Farbeinstellung (256) konfiguriert sind. Beachten Sie auch die palettenverwendung der Anwendung, in der das Zeichen verwendet wird. Am besten vermeiden Sie, dass das Zeichen die Farben seiner Host Anwendung neu zuordnen muss und umgekehrt. Wenn Sie planen, mehrere gleichzeitig angezeigte Zeichen zu unterstützen, sollten Sie auch eine konsistente Palette für diese Zeichen beibehalten. Sie sollten in Erwägung gezogen werden, nur die Standardsystem Farben in Ihrem Zeichen zu verwenden, wenn Sie Benutzer mit einer 8-Bit-Farbkonfiguration als Ziel verwenden. Dies verhindert jedoch möglicherweise die Neuzuordnung der Zeichenfarbe, wenn die Farbpalette von einer anderen Anwendung umfassend neu definiert wird. Auf Systemen, die auf eine höhere Farbauflösung festgelegt sind, sollte das Neuzuordnen der Farbpalette kein Problem darstellen, da das System die Farbpaletten automatisch verwaltet.

Die Verwendung einer größeren Anzahl von Farben in einem Bild kann auch die Gesamtgröße der Animations Datei erhöhen. Mit der Anzahl der Farben und der Häufigkeit der Variation kann festgelegt werden, wie gut die Zeichen Datei komprimiert. Beispielsweise wird ein zweidimensionales Zeichen, das nur ein paar Farben verwendet, besser komprimiert als ein dreidimensionales, schattiertes Zeichen.

Sie müssen für die gesamte Zeichen Datei dieselbe Farbpalette verwenden. Die Palette für verschiedene Animationen kann nicht geändert werden. Wenn Sie versuchen, 8-Bit-farbkonfigurationen zu unterstützen, sollten Sie die gleiche Palette für die Anwendung und alle anderen Zeichen verwenden, die Sie unterstützen möchten.

Die 11<sup>.</sup> Position in der Palette ist standardmäßig als Transparenz (oder Alpha Farbe) definiert, obwohl Sie die Farbe auch mit dem Microsoft-Agent-Zeichen-Editor festlegen können. Die Microsoft-Agent-Animations Dienste können alle Pixel in dieser Farbe transparent darstellen. verwenden Sie daher die Farbe in Ihren Bildern nur, wenn Sie Transparenz wünschen.

Ziehen Sie die Form Ihres Zeichens sorgfältig in Erwägung, da es sich auf die Animations Leistung auswirken kann. Um das Zeichen anzuzeigen, erstellen die Animations Dienste ein Regions Fenster, das auf dem gesamten Bild basiert. Bei kleinen unregelmäßigen Bereichen sind häufig mehr Regions Daten erforderlich, und die Animations Leistung Ihres Zeichens kann reduziert werden. Vermeiden Sie daher, wenn möglich, Lücken oder Elemente und Details mit einem Pixel.

Vermeiden Sie das Antialiasing des äußeren Rands Ihres Zeichens. Obwohl Antialiasing eine gute Methode zum Reduzieren von verzweigten Kanten ist, basiert Sie auf angrenzenden Farben. Da Ihr Zeichen möglicherweise auf einer Vielzahl von Farben angezeigt wird, kann das Antialiasing des äußeren Rands dazu führen, dass das Zeichen für andere Hintergründe schlecht erscheint. Allerdings können Sie Antialiasing für die inneren Details Ihres Zeichens verwenden, ohne dieses Problem zu beheben.

### <a name="frame-size"></a>Frame Größe

Die Frame Größe sollte in der Regel nicht größer als 128 x 128 Pixel sein. Obwohl Zeichen in beiden Dimensionen größer oder kleiner sein können, verwendet der Microsoft-Agent-Zeichen-Editor dies als Anzeige Größe und skaliert Zeichen Bilder, wenn Sie eine größere Frame Größe definieren. Die 128 x 128-Frame Größe bringt angemessene Kompromisse mit dem Platz, den das Zeichen auf dem Bildschirm einnimmt. Die Anwendung kann ein Zeichen zur Laufzeit skalieren.

### <a name="frame-duration"></a>Frame Dauer

Sie können den Zeichen-Editor von Microsoft-Agent verwenden, um festzulegen, wie lange die einzelnen Frame der Animation angezeigt werden, bevor Sie zum nächsten Frame wechseln. Legen Sie die Dauer der einzelnen Frames auf mindestens 10 Hundertstel Sekunden (10 Frames pro Sekunde) fest. bei manchen Systemen ist nichts möglicherweise nicht wahrnehmbar. Sie können auch die Dauer länger festlegen, aber unnatürliche Pausen in der Aktion vermeiden.

Der Microsoft-Agent-Zeichen-Editor unterstützt auch Verzweigungen von einem Frame in einer Animation zu einem anderen, basierend auf den von Ihnen angegebenen Wahrscheinlichkeits Prozentwerten. Für einen beliebigen Frame können Sie bis zu drei verschiedene Verzweigungen definieren. Mithilfe der Verzweigung können Sie Animationen erstellen, die sich unterscheiden, wenn Sie wiedergegeben werden, und Animationen in der Schleife Gehen Sie jedoch bei der Verwendung von Verzweigungen vorsichtig vor, da dadurch Probleme auftreten können, wenn Sie versuchen, eine Animation nach einem anderen wiederzugeben. Wenn Sie z. b. eine Schleifen-oder Verzweigungs Animation wiedergeben, kann Sie unbegrenzt fortgesetzt werden, es sei denn, Sie verwenden eine Methode zum [**Anhalten**](stop-method.md) . Wenn Sie unsicher sind, vermeiden Sie Verzweigungen.

Rahmen, die keine Bilder aufweisen und auf die NULL-Dauer festgelegt ist, werden nicht angezeigt, wenn Sie in einer Animation enthalten sind. Sie können diese Funktion verwenden, um Frames zu erstellen, die Verzweigungen unterstützen, ohne sichtbar zu sein. Ein Frame, der noch keine Bilder enthält, wird jedoch angezeigt. Vermeiden Sie daher das einschließen leerer Frames in der Animation, da der Benutzer möglicherweise nicht in der Lage ist, einen leeren Frame voneinander zu unterscheiden, wenn das Zeichen ausgeblendet ist.

### <a name="frame-transition"></a>Frame Übergang

Beachten Sie beim Entwerfen einer Animation, wie Sie nahtlos von und zur Animation wechseln. Wenn Sie z. b. eine Animation erstellen, in der die Zeichen Gesten rechts und eine andere, in der die Zeichen Gesten Links angezeigt werden, sollten Sie das Zeichen reibungslos von einer Position zum anderen animieren. Obwohl Sie dies in Animation erstellen können, ist es eine bessere Lösung, eine neutrale oder Übergangs Position zu definieren, von der aus das Zeichen beginnt und zurückgegeben wird. Die Animation an der neutralen Position kann als Teil jeder Animation oder als separate Animation integriert werden. Im Zeichen-Editor von Microsoft-Agent können Sie eine ergänzende **Rückgabe** Animation für jede Animation für Ihr Zeichen angeben. Die **Rückgabe** Animation sollte in der Regel nicht mehr als 2-4 Frames sein, damit das Zeichen schnell zur neutralen Position übergehen kann.

Beispielsweise können Sie mithilfe des Szenarios "gesturung right, then gesturging Left" eine **gestureright** -Animation erstellen, beginnend mit einem Rahmen, in dem das Zeichen an einer neutralen Position angezeigt wird, und Frames mit Bildern hinzufügen, die die Handzeichen des Zeichens nach rechts erweitern. Erstellen Sie dann die **Rückgabe** Animation: eine ergänzende Animation mit Bildern, die das Zeichen an seine neutrale Position zurückgibt. Sie können dies als Rückgabe Animation für die **gestureright** -Animation zuweisen. Erstellen Sie als nächstes die **gestureleft** -Animation, die von der neutralen Position aus beginnt und den Arm-Wert des Zeichens nach links erweitert. Erstellen Sie schließlich auch eine ergänzende **Rückgabe** Animation für diese Animation. Eine **Rückgabe** Animation beginnt in der Regel mit einem Bild, das auf das letzte Bild der vorangehenden Animation folgt.

Das Starten und zurückkehren zur gleichen neutralen Position, entweder innerhalb einer Animation oder mithilfe einer Rückgabe Animation, ermöglicht es Ihnen, jede Animation in beliebiger Reihenfolge wiederzugeben. Die Microsoft-Agent-Animations Dienste spielen ihre festgelegte Rückgabe Animation in vielen Situationen automatisch wieder. Die Dienste spielen z. b. die angegebene Rückgabe Animation, bevor Sie die idck State-Animationen Ihres Zeichens **wiedergeben** . Es empfiehlt sich, **Rückgabe** Animationen zu definieren und zuzuweisen, wenn Ihre Animationen nicht bereits an der neutralen Position enden.

Wenn Sie Ihre eigenen Übergänge zwischen bestimmten Animationen bereitstellen möchten. Beispielsweise können Sie die Definition von **Rückgabe** Animationen vermeiden, weil Sie Sie immer in einer klar definierten Reihenfolge abspielen. Es ist jedoch immer noch eine gute Idee, die Reihenfolge der Animationen von der neutralen Position aus zu beginnen und zu beenden.

### <a name="speaking-animation"></a>Sprach Animation

Geben Sie für jede Animation, in der das Zeichen gesprochen werden soll, Mund Bilder an, es sei denn, das Design des Zeichens hat keinen animierten Mund oder einen Hinweis auf eine gesprochene Ausgabe. Im Allgemeinen ist die Mund Bewegung sehr wichtig. Ein Zeichen kann weniger intelligent, likable oder ehrlich erscheinen, wenn seine Mundbewegung nicht mit seiner Sprache synchronisiert wird. Mit Mund Bildern kann das Zeichen mit der gesprochenen Ausgabe synchron synchronisiert werden. Sie definieren Mund Bilder separat und als Windows-Bitmapdateien. Sie müssen mit der gleichen Farbpalette wie die anderen Bilder in der Animation übereinstimmen.

Die Microsoft-Agent-Animations Dienste zeigen die Mund Animations Rahmen oberhalb des letzten Frames einer Animation an, die auch als *sprach Rahmen* der Animation bezeichnet werden. Wenn z. b. das Zeichen in der **gestureright** -Animation spricht, überlagern die Animations Dienste die Mund Animations Rahmen im letzten Rahmen von **gestureright**. Ein Zeichen kann nicht während der Animation gesprochen werden, sodass Sie nur für den letzten Frame einer Animation Mund Bilder bereitstellen. Außerdem muss es sich bei dem sprechenden Frame um den Endframe einer Animation handeln, sodass ein Zeichen nicht in einer Schleifen Animation gesprochen werden kann.

Normalerweise würden Sie die Mund Bilder in der gleichen Größe wie der Frame (und das Basis Bild) bereitstellen, aber nur den Bereich einschließen, der als Teil der Mundbewegung animiert, und den Rest des Bilds in der transparenten Farbe darstellen. Entwerfen Sie das Bild so, dass es mit dem Bild im sprechenden Frame übereinstimmt, wenn es oberhalb dieses Rahmens liegt. Damit er ordnungsgemäß funktioniert, ist es wahrscheinlich, dass Sie für jede Animation, in der das Zeichen spricht, einen separaten Satz von Mund Bildern erstellen müssen.

Ein Mundbild kann mehr als den Mund selbst enthalten, wie z. b. das Kinn oder andere Teile des Zeichen Texts, während er spricht. Wenn Sie jedoch eine Hand oder einen Teil verschieben, beachten Sie, dass Sie möglicherweise nach dem Zufallsprinzip verschoben wird, da das angezeigte mundoverlay auf dem aktuellen Phonem eines gesprochenen Ausdrucks basiert. Außerdem schneidet der Server das Mund Bild an die Gliederung des sprechenden Frame Bilds ab. Entwerfen Sie Ihr mundüberlagerungs Bild so, dass es innerhalb des Gliederung seines Frame Bilds für das Basis Bild verbleibt, da der Server das Basis Image zum Erstellen der Fenster Begrenzung für das Zeichen verwendet.

Mit dem Zeichen-Editor von Microsoft-Agent können Sie sieben grundlegende mundpositionen definieren, die den in der folgenden Tabelle dargestellten allgemeinen Phonem-Mund Formen entsprechen:

**Bild für Mund Animation**



| Mundposition | Beispiel Bild                       | Darstellung                                                                                                                     |
|----------------|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Geschlossen         | :::image type="icon" source="images/g07ci01.gif":::<br/> | Normale Mund geschlossene Form. Wird auch für Phoneme wie "m" wie in "MOM", "b" wie in "Bob", "f" wie in "Fife" verwendet.<br/>           |
| Open-Wide 1    | :::image type="icon" source="images/g07ci02.gif":::<br/> | Der Mund ist in voller Breite etwas offen. Wird für Phoneme wie z. b. "g" wie in "GAG", "l" wie in "Lull", "EAR" wie in "Hear" verwendet.<br/> |
| Open-Wide 2    | :::image type="icon" source="images/g07ci03.gif":::<br/> | Der Mund ist teilweise geöffnet, bei voller Breite. Wird für Phoneme wie "n" wie in "Nonne", "d" wie in "Dad", "t" wie in "tot" verwendet.<br/>    |
| Open-Wide 3    | :::image type="icon" source="images/g07ci04.gif":::<br/> | Der Mund ist in voller Breite geöffnet. Wird für Phoneme verwendet, wie z. b. "u", wie in "Hütte", "EA" wie in "Head", "Your" as in "weh".<br/>          |
| Open-Wide 4    | :::image type="icon" source="images/g07ci05.gif":::<br/> | Der Mund ist vollständig geöffnet, in voller Breite. Wird für Phoneme wie "a" wie in "hat", "ow" wie in "How" verwendet.<br/>                   |
| Open-Medium    | :::image type="icon" source="images/g07ci06.gif":::<br/> | Der Mund ist in halber Breite geöffnet. Wird für Phoneme verwendet, wie z. b. "Oy" wie in "Ahoy", "o", wie in "Hot".<br/>                              |
| Offen/schmal    | :::image type="icon" source="images/g07ci07.gif":::<br/> | Der Mund ist in schmaler Breite geöffnet. Wird für Phoneme verwendet, wie z. b. "o", wie in "Hoop", "o", wie in "Hope", "w", wie in "nass".<br/>           |



 

 

 





