---
description: Audiositzungen
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Audiositzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57ae67a3eafe7a76add2fad192823868304e860d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127673"
---
# <a name="audio-sessions"></a>Audiositzungen

Eine *Audiositzung* ist eine Gruppe verwandter Audiostreams, die von einem WASAPI-Client gemeinsam verwaltet werden können. Clients können die Volumeebene und den stumm Schaltung-Status jeder einzelnen Sitzung steuern. Das System wendet vom Client angegebene Volume und stumm Einstellungen einheitlich auf alle Streams in der Sitzung an.

Wenn ein Client einen Audiostream initialisiert, wird der Audiostream einer Audiositzung zugewiesen. Weitere Informationen finden Sie unter [**iaudioclient:: Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Eine Audiositzung enthält entweder renderingstreams oder Erfassungsdaten Ströme, aber nicht beides. Standardmäßig sind das Volume und die stumm Einstellungen für eine renderingsitzung über Systemneustarts hinweg persistent. Das Volume und die stumm Einstellungen für eine Aufzeichnungs Sitzung sind nicht persistent. (Eine Sitzung, die Streams enthält, die im Loopback Modus betrieben werden, wird genauso behandelt wie eine Aufzeichnungs Sitzung. Das heißt, die Sitzungs Einstellungen sind nicht persistent. Weitere Informationen zum Loopback Modus finden Sie unter [Loopback-Aufzeichnung](loopback-recording.md).)

Jeder Audiostream gehört zu genau einer Sitzung. Ein Client weist einer bestimmten Sitzung einen Audiostream zu dem Zeitpunkt zu, zu dem er das Stream-Objekt initialisiert. Der Stream behält seine Mitgliedschaft in der Sitzung für die Lebensdauer des Streams bei. Nachdem ein Stream-Objekt erstellt wurde, ist das-Objekt vorhanden, bis ein Client den zuletzt gezählten Verweis auf das-Objekt freigibt und das Objekt dann gelöscht wird.

Obwohl ein Client die Sitzung, der ein vorhandener Stream zugewiesen ist, nicht ändern kann, kann er einen ähnlichen Effekt erzielen, indem der Stream gelöscht wird (indem alle Verweise darauf freigegeben werden), ein neuer Stream erstellt wird, um den gelöschten Stream zu ersetzen, und der neue Stream einer anderen Sitzung zugewiesen wird.

Jede renderingsitzung stellt eine Teilmenge der Streams dar, die den globalen Mix bilden, der über ein bestimmtes [audioendpunktgerät](audio-endpoint-devices.md)abgespielt wird. Mit der globalen Mischung werden alle Sitzungen von allen Anwendungen kombiniert, die das Gerät gemeinsam verwenden.

Häufig weist eine Anwendung mit mehreren Streams alle zugehörigen Datenströme derselben Sitzung zu. Die Anwendung kann jedoch verschiedene Datenströme anderen Sitzungen zuweisen. Alle Datenströme, die von der Anwendung nicht explizit einer Sitzung zugewiesen werden, gehören zur Standard Sitzung.

Typische Audioanwendungen sollten das Ändern des Volumes und das stumm schalten von Einstellungen für Sitzungen vermeiden. Stattdessen steuern die Benutzer diese Einstellungen über die Benutzeroberflächen der Steuerungsprogramme. In Windows Vista zeigt z. b. das vom System bereitgestellte Programm (Sndvol.exe) für jede aktive oder vor kurzem aktive renderingsitzung im System ein Volume-Steuerelement und ein stumm Steuerelement an. Über diese Steuerelemente können Benutzer das Volume anpassen und Einstellungen für alle Sitzungen im System stumm schalten.

Das sndvol-Programm zeigt zurzeit nur volumesteuerelemente für audiorendering-Endpunkt Geräte an. Es werden keine volumesteuerelemente für audioerfassungs Geräte angezeigt.

Eine Sitzung ist aktiv, wenn Sie mindestens einen aktiven Stream enthält. Ein aktiver Stream befindet sich im *Status*"wird ausgeführt". Ein inaktiver Stream befindet sich im *Status "beendet*". Eine Sitzung wird aktiviert, wenn der erste Stream aktiv wird. Eine Sitzung wird inaktiv, wenn der letzte aktive Stream inaktiv wird. Nachdem eine Sitzung für einen bestimmten Zeitraum inaktiv war, ändert das System den Status der Sitzung von inaktiv in abgelaufen.

Sndvol zeigt für alle aktiven und inaktiven renderingsitzungen Volumes und stumm Steuerelemente an. Sndvol entfernt das Volume und die stumm Steuerelemente für eine Sitzung, wenn sich der Status der Sitzung von "inaktiv" in "abgelaufen" ändert oder wenn die Sitzung beendet wird. (Eine Sitzung wird beendet, wenn die letzten Datenströme gelöscht werden, d. h., wenn ein Client den endgültigen Verweis Zähler für das letzte verbleibende Streamobjekt in der Sitzung freigibt.) Die einzige Ausnahme von dieser Regel ist für System Benachrichtigungs Sounds. Sndvol zeigt immer das Volume an und hört Steuerelemente für systembenachrichtigungshub unabhängig vom Status der Sitzung für diese Sounds an.

Normalerweise gehört ein Stream zu einer Sitzung, die nur den Prozess umfasst, der die Anwendung enthält, von der der Stream erstellt wurde. Anwendungen haben jedoch die Möglichkeit, prozessübergreifende Sitzungen zu definieren, die Datenströme aus zwei oder mehr Prozessen kombinieren.

WASAPI unterstützt prozessübergreifende Sitzungen hauptsächlich, um Folgendes zu tun:

-   Das sndvol-Programm kann dem Benutzer ein einzelnes volumensteuerelement zur Verfügung stellen, um System Benachrichtigungs Sounds für alle Anwendungen zu verwalten.
-   Ein Media Player, der in einem Prozess ausgeführt wird, kann geschützte Inhalte in ein Entschlüsselungs Programm streamen, das in einem anderen Prozess ausgeführt wird.

Ähnlich wie bei den Steuerelement Einstellungen für prozessspezifische renderingsitzungen sind die Steuerungseinstellungen für prozessübergreifende renderingsitzungen standardmäßig über Systemneustarts hinweg persistent. WASAPI bietet dieses Verhalten hauptsächlich für den Vorteil von Systembenachrichtigungs-Sounds, bei dem das Volume des Benutzers beibehalten und Einstellungen stumm geschaltet werden müssen, da sich die Anwendungs Mischung im Laufe der Zeit ändert.

Das sndvol-Programm bezeichnet das volumesteuerelement für jede Sitzung mit einem anzeigen Amen und einem Symbol. Ein Client hat die Möglichkeit, einer Sitzung explizit einen anzeigen Amen und ein Symbol zuzuweisen. Wenn der Client diese Elemente nicht bereitstellt, zeigt sndvol stattdessen einen Standardnamen und ein Standard Symbol an. Der Standardname enthält Informationen, z. b. den Titel des Anwendungsfensters. Das Standard Symbol ist das Symbol für das Anwendungsfenster. Diese Standardeinstellungen stellen nur bei prozessspezifischen Sitzungen sinnvolle Informationen für Benutzer bereit. Beachten Sie, dass eine prozessübergreifende Sitzung mehr als einer Anwendung zugeordnet werden kann. In diesem Fall ist nur ein vom Client bereitgestellter Anzeige Name und Symbol sinnvoll.

Obwohl die Volume-und stumm Einstellungen für eine renderingsitzung standardmäßig über Systemneustarts hinweg persistent sind, sind der vom Client bereitgestellte Anzeige Name und das Symbol nicht. Um sicherzustellen, dass sndvol den vom Client bereitgestellten Namen und das Symbol anzeigt, muss der Client den Namen und das Symbol der Sitzung explizit zuweisen, wenn der Client den ersten Datenstrom der Sitzung zuweist. Das System behält den anzeigen Amen und das Symbol für eine Sitzung nur so lange bei, bis die Sitzung beendet wird.

Jede Sitzung wird durch eine Sitzungs-GUID identifiziert. Wenn ein Client einen Stream öffnet, weist der Client diesen Stream einer bestimmten Sitzung zu. Der Client stellt die folgenden zwei Informationen bereit, um die Sitzung zu identifizieren:

-   Eine Sitzungs-GUID.
-   Ob die Sitzung eine prozessübergreifende oder prozessspezifische Sitzung ist – eine prozessspezifische Sitzung enthält nur Datenströme aus dem Client Prozess.

Diese Informationen sind ausreichend, um eine bestimmte Sitzung von allen anderen Sitzungen auf demselben Computer zu unterscheiden. Die Sitzungs-GUID für eine prozessspezifische Sitzung identifiziert die Sitzung eindeutig nur innerhalb des Gültigkeits Bereichs des Prozesses, der die Sitzung besitzt. Im Gegensatz dazu ist die Sitzungs-GUID für eine prozessübergreifende Sitzung innerhalb des Umfangs aller Prozesse, die auf dem Computer ausgeführt werden, eindeutig.

Bei einer prozessspezifischen Sitzung verwendet das System eine Kombination aus Sitzungs-GUID und Prozess-ID, um die Sitzung innerhalb des Gültigkeits Bereichs des Computers eindeutig zu identifizieren. Wenn die jeweiligen Datenströme von Clients in zwei verschiedenen Prozessen zwei prozessspezifischen Sitzungen mit identischen Sitzungs-GUIDs zugewiesen werden, werden die Sitzungen vom System als getrennt behandelt, da ihre Prozess-IDs unterschiedlich sind. Wenn eine prozessübergreifende Sitzung dieselbe Sitzungs-GUID wie eine oder mehrere prozessspezifische Sitzungen verwendet, behandelt das System außerdem die prozessübergreifende Sitzung von den prozessspezifischen Sitzungen, auch wenn Sie dieselbe Sitzungs-GUID verwenden.

Beispielsweise weisen in Windows Vista APIs auf höherer Ebene, wie z. b. die Windows Multimedia **waveoutxxx** -Funktionen und DirectSound, die von Ihnen erstellten Audiostreams in der Regel den standardmäßigen, prozessspezifischen Sitzungen zu, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert werden \_ . Für Clients dieser APIs ist die Standard Sitzung für jeden Client Prozess getrennt von den Standard Sitzungen für andere Client Prozesse, auch wenn die Sitzungen identische Sitzungs-GUIDs aufweisen. Wenn mindestens eine Anwendung Streams der prozessübergreifenden Sitzung zuweist, die durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ , behandelt das System diese prozessübergreifende Sitzung als getrennt von den standardmäßigen prozessspezifischen Sitzungen, die dieselbe Sitzungs-GUID verwenden. Entsprechend zeigt das sndvol-Programm ein separates volumesteuerelement für die standardmäßige prozessspezifische Sitzung jedes Clients an und zeigt ein zusätzliches volumesteuerelement für die prozessübergreifende Sitzung an, das durch den Sitzungs-GUID-Wert GUID NULL identifiziert wird \_ , wenn diese Sitzung vorhanden ist.

Jede Sitzung ist nur einem audioendpunktgerät zugeordnet. Wenn zwei Sitzungen identische Sitzungs-GUIDs und Prozess-IDs aufweisen, aber mit unterschiedlichen Geräten verknüpft sind, werden die beiden Sitzungen vom System als getrennt behandelt. Eine Sitzung kann niemals Erfassungs-und renderingdatenströme enthalten, da ein Erfassungsdaten Strom nur einem Erfassungsgerät zugeordnet werden kann und ein renderingstream nur einem renderinggerät zugeordnet werden kann.

Wie bereits erwähnt, sind das Volume und die stumm Einstellungen für eine Sitzung über Systemneustarts hinweg persistent. Mindestens zwei Instanzen einer Anwendung können prozessspezifische Sitzungen mit identischen Sitzungs-GUIDs erstellen. Über das sndvol-Programm kann der Benutzer für jede dieser Sitzungen andere Volumes und stumm Einstellungen auswählen. Nachdem diese Sitzungen beendet wurden, behält das System die Steuerungseinstellungen von nur einer dieser Sitzungen bei – der letzten Sitzung, die beendet werden soll. Wenn eine neue Instanz der Anwendung später eine prozessspezifische Sitzung mit derselben Sitzungs-GUID wie zuvor erstellt, erbt diese Sitzung das zuvor gespeicherte Volume und die stumm Einstellungen.

Eine Anwendung sollte nicht versuchen, einen Datenstrom hinzuzufügen oder die Volumeebene einer Sitzung zu steuern, die einer anderen, nicht verknüpften Anwendung gehört. Außerdem sollte eine Anwendung nicht versuchen, die Volumeebene der vom System verwalteten Sitzung für Benachrichtigungs Sounds zu steuern. Allerdings kann eine Anwendung durch Aufrufen der Funktion **PlaySound** einen Sound durch die System Sitzung für Benachrichtigungs Klänge abspielen. Weitere Informationen finden Sie unter [Benachrichtigungs Sounds für Legacy-Audioanwendungen](notification-sounds-for-legacy-audio-applications.md).

Eine Anwendung kann sich registrieren, um Benachrichtigungen zu empfangen, wenn sich der Status einer Sitzung ändert. Weitere Informationen finden Sie unter [audiositzungsereignisse](audio-session-events.md).

In seltenen Fällen muss eine Anwendung, die eine prozessspezifische Sitzung erstellt, möglicherweise die Steuerung der prozessspezifischen Sitzungen für zwei oder mehr Anwendungs Instanzen unter einem einzelnen volumesteuerelement in sndvol konsolidieren. Weitere Informationen finden Sie unter [Gruppieren von Parametern](grouping-parameters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



