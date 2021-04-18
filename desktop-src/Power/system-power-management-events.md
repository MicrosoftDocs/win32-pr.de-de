---
description: Ein System Energie Verwaltungs Ereignis ist eine Änderung des System Energiestatus, des Betriebsmodus eines Geräts oder des Systems oder des Werts einer Energie Einstellung.
ms.assetid: f73b072a-1f69-4e26-9712-dab428edca18
title: Ereignisse der System Energie Verwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab18fad9116cfff9e1cd35703e32a49e3b12c8b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358887"
---
# <a name="system-power-management-events"></a>Ereignisse der System Energie Verwaltung

Ein System Energie Verwaltungs Ereignis ist eine Änderung des System Energiestatus, des Betriebsmodus eines Geräts oder des Systems oder des Werts einer Energie Einstellung. Da diese Ereignisse den Betrieb von Anwendungen und installierbaren Treibern beeinflussen können, benachrichtigt das System alle Anwendungen und installierbaren Treiber, indem eine Benachrichtigung für jedes Ereignis gesendet wird. Anwendungen und Dienste registrieren sich mithilfe der [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) -Funktion für Benachrichtigungen. Benachrichtigungen werden über die [**WM- \_ powerbroadcast**](wm-powerbroadcast.md) -Nachricht empfangen, in der das Energie Verwaltungs Ereignis und alle zugehörigen ereignisspezifischen Daten enthalten sind.

## <a name="system-power-status-events"></a>System Energie Status-Ereignisse

Ein *System Energiestatus-Ereignis* tritt auf, wenn sich die Stromversorgung oder der System Akku Status ändert. Das System überträgt z. b. ein [PBT \_ apmpowerstatuschange](pbt-apmpowerstatuschange.md) -Ereignis, wenn der Benutzer von der Akku-in die Stromversorgung oder umgekehrt wechselt. Das System leitet dieses Ereignis auch dann weiter, wenn die verbleibende Akkuleistung unter einen vom Benutzer festgelegten Wert sinkt oder sich um einen angegebenen Prozentsatz ändert.

## <a name="operational-mode-events"></a>Betriebsmodus-Ereignisse

Ein *Betriebsmodus-Ereignis* tritt auf, wenn sich der Stromverbrauch ändert, z. b. wenn das System aufgrund von Inaktivität in den Ruhezustand wechselt oder der Benutzer das System manuell in den Standbymodus versetzt. Das System überträgt Ereignisse über diese Änderungen, bevor die Änderung des Stromverbrauchs erfolgt. Wenn das System z. b. erkennt, dass es sich im Leerlauf befindet, sendet es ein [PBT \_ apmsuspend](pbt-apmsuspend.md) -Ereignis, das Anwendungen und Treibern benachrichtigt, dass der Betrieb und der Standbymodus angehalten werden, um Energie zu sparen. Anwendungen und Treiber können sich auf den Standbymodus vorbereiten, indem Sie Dateien schließen und Daten speichern, um potenzielle Datenverluste zu vermeiden.

Wenn das System eine kritische unter *Brechung* durchführt, wird das System sofort aufgrund einer kritischen Bedingung, z. b. eines kritischen Akku Alarms, in den Standbymodus versetzt. Im Gegensatz zu einem normalen Ruhezustand benachrichtigt das Systemanwendungen und Treiber nicht, bevor eine kritische Unterbrechung durchgeführt wird. Daher müssen Anwendungen darauf vorbereitet sein, kritische Suspendierungen zu verarbeiten.

Wenn der System Vorgang wieder hergestellt wird, nachdem er angehalten wurde, benachrichtigt das System alle Anwendungen und Treiber. Außerdem wird angegeben, ob das System von einer kritischen Unterbrechung fortgesetzt wird, damit die Anwendung oder der Treiber die entsprechenden Schritte ausführen kann, um die Daten wiederherzustellen und den Vorgang fortzusetzen.

Anwendungen sollten jeden Versuch, den Übergang in den Ruhezustand zu versetzen, ohne Benutzereingriff durchführen zu müssen, da der Benutzer möglicherweise nicht antwortet. Beispielsweise kann der Deckel auf dem Notebook-Computer geschlossen werden. Wenn eine Anwendung eine Benachrichtigung erhält, dass das System in den Standbymodus wechselt, sollte Sie alle notwendigen Vorgänge schnell ausführen und die Nachrichten Schleife zurückgeben. Das System lässt bei der Verarbeitung dieser Nachricht maximal zwei Sekunden pro Anwendung zu, bevor ein Timeout eintritt.

## <a name="power-setting-change-events"></a>Energie Einstellungs Änderungs Ereignisse

Ein Energie Einstellungs Änderungs Ereignis tritt auf, wenn der Wert einer Energie Einstellung geändert wird. Der Benutzer ändert z. b. in der Systemsteuerung in der Anwendung Energieoptionen den Energie Sparplan von hohe Leistung in ausgeglichen. In diesem Fall würde das System ein Ereignis übertragen, das angibt, dass sich der Energie Sparplan geändert hat. Dieses Ereignis enthält den neuen Wert für die Energie Einstellung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Energie Verwaltung](about-power-management.md)
</dt> </dl>

 

 



