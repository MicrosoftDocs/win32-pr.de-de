---
description: Ein Systemleistungsverwaltungsereignis ist eine Änderung des Systemleistungsstatus, des Betriebsmodus eines Geräts oder des Systems oder des Werts einer Energieeinstellung.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: System Power Management Events
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0558dfe0c846c6b48125a382d14f03181d7f18fb2d11deb4783af975e57c4cf0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032930"
---
# <a name="system-power-management-events"></a>System Power Management Events

Ein Systemleistungsverwaltungsereignis ist eine Änderung des Systemleistungsstatus, des Betriebsmodus eines Geräts oder des Systems oder des Werts einer Energieeinstellung. Da sich diese Ereignisse auf den Betrieb von Anwendungen und installierbaren Treibern auswirken können, benachrichtigt das System alle Anwendungen und installierbaren Treiber, indem es eine Benachrichtigung für jedes Ereignis sendet. Anwendungen und Dienste registrieren sich mithilfe der [**Funktion RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) für Benachrichtigungen. Benachrichtigungen werden über die [**WM \_ POWERBROADCAST-Nachricht**](wm-powerbroadcast.md) empfangen, die das Energieverwaltungsereignis und alle zugehörigen ereignisspezifischen Daten enthält.

## <a name="system-power-status-events"></a>System Power Status Events

Ein *Systemleistungsstatusereignis* tritt auf, wenn sich die Stromversorgung oder der Akkustatus des Systems ändern. Beispielsweise überträgt das System ein [ \_ PBT-APMPOWERSTATUSCHANGE-Ereignis,](pbt-apmpowerstatuschange.md) wenn der Benutzer vom Akku zum Netzbetrieb wechselt oder umgekehrt. Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.

## <a name="operational-mode-events"></a>Betriebsmodusereignisse

Ein *Betriebsmodusereignis* tritt auf, wenn sich der Stromverbrauch ändert, z. B. wenn das System aufgrund von Inaktivität in den Energiesparmodus wechselt oder der Benutzer das System manuell in den Energiesparmodus versetzt. Das System überträgt Ereignisse zu diesen Änderungen, bevor die Änderung des Stromverbrauchs vorgenommen wird. Wenn das System beispielsweise feststellt, dass es sich im Leerlauf befindet, sendet es ein [ \_ PBT-APMSUSPEND-Ereignis,](pbt-apmsuspend.md) das Anwendungen und Treiber benachrichtigt, dass der Betrieb angehalten und der Energiesparmodus unterbrochen wird, um Energie zu sparen. Anwendungen und Treiber können sich auf den Standbymodus vorbereiten, indem Sie Dateien schließen und Daten speichern, um potenzielle Datenverluste zu vermeiden.

Wenn das System eine *kritische Unterbrechung* ausführt, wird das System aufgrund eines kritischen Zustands, z. B. eines kritischen Akkualarms, sofort in den Energiesparmodus versetzt. Im Gegensatz zu einem normalen Standbyübergang benachrichtigt das System Anwendungen und Treiber nicht, bevor eine kritische Unterbrechung durchgeführt wird. Daher müssen Anwendungen darauf vorbereitet sein, kritische Unterbrechungen zu verarbeiten.

Wenn der Systemvorgang nach dem Anhalten wiederhergestellt wird, benachrichtigt das System alle Anwendungen und Treiber. Außerdem wird angegeben, ob das System nach einer kritischen Unterbrechung fortgesetzt wird, damit die Anwendung oder der Treiber geeignete Schritte ausführen kann, um seine Daten wiederherzustellen und den Betrieb fortzusetzen.

Anwendungen sollten jeden Versuch unternehmen, den Übergang in den Standbyzustand ohne Benutzereingriff zu verarbeiten, da der Benutzer möglicherweise nicht reagieren kann. Beispielsweise kann der Deckel auf dem Notebookcomputer geschlossen werden. Wenn eine Anwendung eine Benachrichtigung erhält, dass das System in den Standbymodus versetzt wird, sollte sie alle erforderlichen Vorgänge schnell ausführen und aus der Nachrichtenschleife zurückkehren. Das System lässt maximal zwei Sekunden pro Anwendung zu, wenn diese Meldung vor dem Timeout verarbeitet wird.

## <a name="power-setting-change-events"></a>Energieeinstellungsänderungsereignisse

Ein Energieeinstellungsänderungsereignis tritt auf, wenn der Wert einer Energieeinstellung geändert wird. Beispielsweise ändert der Benutzer den Energiesparplan in der anwendung Energieoptionen in Systemsteuerung von "Hohe Leistung" in "Ausgeglichen". In diesem Fall sendet das System ein Ereignis, das angibt, dass sich der Energiesparplan geändert hat. Dieses Ereignis enthält den neuen Wert für die Energieeinstellung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energieverwaltung](about-power-management.md)
</dt> </dl>

 

 



