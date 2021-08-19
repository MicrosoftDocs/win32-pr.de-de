---
description: Audiositzungen
ms.assetid: b8a1b656-a582-4112-99e9-bd575719ebb3
title: Audiositzungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d5b8cee0a3a53709d2c450bef36ae00e3a6f4d9323c75ff80e96b19550eb39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119929410"
---
# <a name="audio-sessions"></a>Audiositzungen

Eine *Audiositzung* ist eine Gruppe verwandter Audiostreams, die ein WASAPI-Client gemeinsam verwalten kann. Clients können die Volumeebene und den Mutingzustand jeder einzelnen Sitzung steuern. Das System wendet vom Client angegebene Volume- und Stummschaltungseinstellungen einheitlich auf alle Datenströme in der Sitzung an.

Wenn ein Client einen Audiostream initialisiert, weist er den Audiostream einer Audiositzung zu. Weitere Informationen finden Sie unter [**IAudioClient::Initialize**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-initialize).

Eine Audiositzung enthält entweder Renderingstreams oder Erfassungsstreams, aber nicht beides. Standardmäßig sind die Volume- und Stummschaltungseinstellungen für eine Renderingsitzung über Systemneustarts hinweg persistent. Die Volume- und Stummschaltungseinstellungen für eine Aufzeichnungssitzung sind nicht persistent. (Eine Sitzung, die Streams enthält, die im Loopbackmodus ausgeführt werden, wird wie eine Aufzeichnungssitzung behandelt. Das heißt, die Sitzungseinstellungen sind nicht persistent. Weitere Informationen zum Loopbackmodus finden Sie unter [Loopbackaufzeichnung](loopback-recording.md).)

Jeder Audiostream gehört zu genau einer Sitzung. Ein Client weist einer bestimmten Sitzung zum Zeitpunkt der Initialisierung des Streamobjekts einen Audiostream zu. Der Stream behält seine Mitgliedschaft in der Sitzung für die Lebensdauer des Streams bei. Nachdem ein Streamobjekt erstellt wurde, ist das Objekt vorhanden, bis ein Client den letzten gezählten Verweis auf das Objekt freigibt und das Objekt dann gelöscht wird.

Obwohl ein Client die Sitzung, der ein vorhandener Stream zugewiesen ist, nicht ändern kann, kann er einen ähnlichen Effekt erzielen, indem er den Stream löscht (indem er alle Verweise auf ihn freigibt), einen neuen Stream erstellt, um den gelöschten Stream zu ersetzen, und den neuen Stream einer anderen Sitzung zuweist.

Jede Renderingsitzung stellt eine Teilmenge der Streams dar, die die globale Mischung bilden, die über ein [bestimmtes Audioendpunktgerät](audio-endpoint-devices.md)wiedergegeben wird. Die globale Mischung kombiniert alle Sitzungen aller Anwendungen, die das Gerät gemeinsam nutzen.

Häufig weist eine Anwendung mit mehreren Streams alle ihre Streams derselben Sitzung zu. Die Anwendung kann jedoch optional verschiedene Streams verschiedenen Sitzungen zuweisen. Jeder Stream, den die Anwendung nicht explizit einer Sitzung zuweist, gehört zur Standardsitzung.

Typische Audioanwendungen sollten das Ändern der Lautstärke und das Stummschalten von Einstellungen für Sitzungen vermeiden. Stattdessen steuern Benutzer diese Einstellungen über die Benutzeroberflächen von Steuerungsprogrammen. Beispielsweise zeigt das vom System bereitgestellte Programm in Windows Vista Sndvol.exe ein Volumesteuerelement und ein Stummschaltungssteuerelement für jede aktive oder kürzlich aktive Renderingsitzung im System an. Über diese Steuerelemente können Benutzer das Volume anpassen und einstellungen für alle Sitzungen im System stummschalten.

Das Sndvol-Programm zeigt derzeit Volumesteuerelemente nur für Geräte mit Audiorenderingendpunkt an. Es werden keine Lautstärkeregler für Audioaufnahmegeräte angezeigt.

Eine Sitzung ist aktiv, wenn sie einen oder mehrere aktive Streams enthält. Ein aktiver Stream befindet sich im *Ausführungsstatus*. Ein inaktiver Stream befindet sich im *beendeten Zustand*. Eine Sitzung wird aktiv, wenn der erste Stream aktiv wird. Eine Sitzung wird inaktiv, wenn der letzte aktive Stream inaktiv wird. Nachdem eine Sitzung für einen bestimmten Zeitraum inaktiv war, ändert das System den Zustand der Sitzung von inaktiv in abgelaufen.

Sndvol zeigt Lautstärke- und Stummschaltsteuerelemente für alle aktiven und inaktiven Renderingsitzungen an. Sndvol entfernt das Volume und stummgeschaltete Steuerelemente für eine Sitzung, wenn sich der Zustand der Sitzung von inaktiv in abgelaufen ändert oder wenn die Sitzung beendet wird. (Eine Sitzung wird beendet, wenn der letzte ihrer Streams gelöscht wird, d. h., wenn ein Client den endgültigen Verweiszähler für das letzte verbleibende Streamobjekt in der Sitzung freigibt.) Eine Ausnahme von dieser Regel ist für Systembenachrichtigungssounds. Sndvol zeigt immer die Lautstärke- und Stummschaltungssteuerelemente für Systembenachrichtigungssounds an, unabhängig vom Zustand der Sitzung für diese Sounds.

In der Regel gehört ein Stream zu einer Sitzung, die nur den Prozess umfasst, der die Anwendung enthält, die den Stream erstellt hat. Anwendungen haben jedoch die Möglichkeit, prozessübergreifende Sitzungen zu definieren, die Datenströme von zwei oder mehr Prozessen kombinieren.

WASAPI unterstützt in erster Linie prozessübergreifende Sitzungen, sodass:

-   Das Sndvol-Programm kann dem Benutzer eine einzelne Volumesteuerung zur Verwaltung von Systembenachrichtigungssounds für alle Anwendungen bieten.
-   Ein Medienplayer, der in einem Prozess ausgeführt wird, kann geschützte Inhalte an ein Entschlüsselungsprogramm streamen, das in einem anderen Prozess ausgeführt wird.

Ähnlich wie die Steuerelementeinstellungen für prozessspezifische Renderingsitzungen sind die Steuerelementeinstellungen für prozessübergreifende Renderingsitzungen standardmäßig über Systemneustarts hinweg persistent. WASAPI bietet dieses Verhalten in erster Linie zum Vorteil von Systembenachrichtigungssounds, die das Volume und die Stummschaltungseinstellungen des Benutzers beibehalten müssen, da sich die Anwendungsmischung im Laufe der Zeit ändert.

Das Sndvol-Programm bezeichnet das Volumesteuerelement für jede Sitzung mit einem Anzeigenamen und einem Symbol. Ein Client hat die Möglichkeit, einer Sitzung explizit einen Anzeigenamen und ein Symbol zuzuweisen. Wenn der Client diese Elemente nicht bereitstellt, zeigt Sndvol stattdessen einen Standardnamen und ein Standardsymbol an. Der Standardname enthält Informationen wie den Titel des Anwendungsfensters. Das Standardsymbol ist das Symbol für das Anwendungsfenster. Nur bei prozessspezifischen Sitzungen stellen diese Standardeinstellungen benutzern aussagekräftige Informationen bereit. Beachten Sie, dass eine prozessübergreifende Sitzung mehreren Anwendungen zugeordnet werden kann. In diesem Fall sind nur ein vom Client bereitgestellter Anzeigename und ein Symbol sinnvoll.

Obwohl die Volume- und Stummschaltungseinstellungen für eine Renderingsitzung standardmäßig bei Systemneustarts persistent sind, sind der vom Client bereitgestellte Anzeigename und das Symbol nicht vorhanden. Um sicherzustellen, dass Sndvol den vom Client bereitgestellten Namen und das Symbol anzeigt, muss der Client den Namen und das Symbol explizit der Sitzung zuweisen, wenn der Client der Sitzung den ersten Stream zuweist. Das System behält den Anzeigenamen und das Symbol für eine Sitzung nur bei, bis die Sitzung beendet wird.

Jede Sitzung wird durch eine Sitzungs-GUID identifiziert. Wenn ein Client einen Stream öffnet, weist der Client diesen Stream einer bestimmten Sitzung zu. Der Client stellt die folgenden beiden Informationen bereit, um diese Sitzung zu identifizieren:

-   Eine Sitzungs-GUID.
-   Unabhängig davon, ob es sich bei der Sitzung um eine prozessübergreifende oder prozessspezifische Sitzung handelt– eine prozessspezifische Sitzung enthält nur Datenströme aus dem Clientprozess.

Diese Informationen sind ausreichend, um eine bestimmte Sitzung von allen anderen Sitzungen auf demselben Computer zu unterscheiden. Die Sitzungs-GUID für eine prozessspezifische Sitzung identifiziert die Sitzung eindeutig nur innerhalb des Bereichs des Prozesses, der die Sitzung besitzt. Im Gegensatz dazu ist die Sitzungs-GUID für eine prozessübergreifende Sitzung innerhalb des Bereichs aller Prozesse eindeutig, die auf dem Computer ausgeführt werden.

Im Fall einer prozessspezifischen Sitzung verwendet das System eine Kombination aus Sitzungs-GUID und Prozess-ID, um die Sitzung innerhalb des Bereichs des Computers eindeutig zu identifizieren. Wenn Clients in zwei verschiedenen Prozessen also ihre jeweiligen Datenströme zwei prozessspezifischen Sitzungen mit identischen Sitzungs-GUIDs zuweisen, behandelt das System die Sitzungen als getrennt, da ihre Prozess-IDs unterschiedlich sind. Wenn eine prozessübergreifende Sitzung die gleiche Sitzungs-GUID wie eine oder mehrere prozessspezifische Sitzungen verwendet, behandelt das System die prozessübergreifende Sitzung als von den prozessspezifischen Sitzungen getrennt, obwohl sie dieselbe Sitzungs-GUID verwenden.

In Windows Vista weisen beispielsweise APIs auf höherer Ebene, z. B. die Windows Multimediafunktionen **waveOutXxx** und DirectSound, die audiostreams, die sie erstellen, in der Regel prozessspezifische Standardsitzungen zu, die durch den GUID-Wert DER Sitzungs-GUID NULL identifiziert \_ werden. Für Clients dieser APIs ist die Standardsitzung für jeden Clientprozess von den Standardsitzungen für andere Clientprozesse getrennt, obwohl die Sitzungen identische Sitzungs-GUIDs aufweisen. Wenn eine oder mehrere Anwendungen der prozessübergreifenden Sitzung Streams zuweisen, die durch den GUID-Wert FÜR DIE SITZUNG NULL identifiziert \_ werden, behandelt das System diese prozessübergreifende Sitzung außerdem als getrennt von den prozessspezifischen Standardsitzungen, die dieselbe Sitzungs-GUID gemeinsam nutzen. Entsprechend zeigt das Sndvol-Programm ein separates Volumesteuerelement für die standardmäßige, prozessspezifische Sitzung jedes Clients an und zeigt ein zusätzliches Volumesteuerelement für die prozessübergreifende Sitzung an, das durch den GUID-Wert DER Sitzung NULL identifiziert \_ wird, sofern diese Sitzung vorhanden ist.

Jede Sitzung ist nur einem Audioendpunktgerät zugeordnet. Wenn zwei Sitzungen über identische Sitzungs-GUIDs und Prozess-IDs verfügen, aber verschiedenen Geräten zugeordnet sind, behandelt das System die beiden Sitzungen als getrennt. Eine Sitzung kann nie sowohl Erfassungs- als auch Renderingstreams enthalten, da ein Erfassungsstream nur einem Erfassungsgerät zugeordnet werden kann und ein Renderingstream nur einem Renderinggerät zugeordnet werden kann.

Wie bereits erwähnt, sind die Volume- und Stummschaltungseinstellungen für eine Sitzung bei Systemneustarts persistent. Zwei oder mehr Instanzen einer Anwendung können prozessspezifische Sitzungen mit identischen Sitzungs-GUIDs erstellen. Über das Sndvol-Programm kann der Benutzer für jede dieser Sitzungen unterschiedliche Volume- und Stummschaltungseinstellungen auswählen. Nachdem diese Sitzungen beendet wurden, behält das System die Steuerungseinstellungen nur einer dieser Sitzungen bei – der letzten Sitzung, die beendet werden soll. Wenn eine neue Instanz der Anwendung später eine prozessspezifische Sitzung mit der gleichen Sitzungs-GUID wie zuvor erstellt, erbt diese Sitzung das zuvor gespeicherte Volume und stummgeschaltete Einstellungen.

Eine Anwendung sollte nicht versuchen, der Volumeebene einer Sitzung, die sich im Besitz einer anderen, nicht verknüpften Anwendung befindet, einen Stream hinzuzufügen oder diese zu steuern. Darüber hinaus sollte eine Anwendung nicht versuchen, die Lautstärke der vom System verwalteten Sitzung für Benachrichtigungsgeräusche zu steuern. Eine Anwendung kann jedoch einen Sound über die Systemsitzung für Benachrichtigungssounds wiedergeben, indem die **PlaySound-Funktion** aufgerufen wird. Weitere Informationen finden Sie unter [Notification Sounds for Legacy Audio Applications](notification-sounds-for-legacy-audio-applications.md).

Eine Anwendung kann sich registrieren, um Benachrichtigungen zu erhalten, wenn sich der Zustand einer Sitzung ändert. Weitere Informationen finden Sie unter [Audiositzungsereignisse.](audio-session-events.md)

In seltenen Fällen muss eine Anwendung, die eine prozessspezifische Sitzung erstellt, möglicherweise die Steuerung der prozessspezifischen Sitzungen für zwei oder mehr Anwendungsinstanzen unter einer einzelnen Volumesteuerung in Sndvol konsolidieren. Weitere Informationen finden Sie unter [Gruppierungsparameter.](grouping-parameters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierhandbuch](programming-guide.md)
</dt> </dl>

 

 



