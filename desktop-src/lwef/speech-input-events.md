---
title: Spracheingabeereignisse
description: Spracheingabeereignisse
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3babdfb38f302bd2ca5934fec4d8b54a84f7452befbec0dfba45b078747f532
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746261"
---
# <a name="speech-input-events"></a>Spracheingabeereignisse

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Zusätzlich zur Command-Ereignisbenachrichtigung benachrichtigt der -Agent auch den eingabeaktiven Client, wenn der Server den Lauschmodus aktiviert oder deaktiviert, indem die [**ListenStart-**](listenstart-event.md) und [**ListenComplete-Ereignisse**](listencomplete-event.md) ([**IAgentNotifySinkEx::ListeningState**](iagentnotifysinkex--listeningstate.md)) verwendet werden. [](command-event.md) Wenn der Benutzer jedoch die Taste für den Lauschenmodus drückt und keine passende Spracherkennungs-Engine für das oberste Zeichen des eingabeaktiven Clients verfügbar ist, startet der Server das Time out im Hotkeymodus "Lauschen", generiert jedoch kein **ListenStart-Ereignis** für den aktiven Client des Zeichens. Wenn der Benutzer vor Abschluss des Time outs ein weiteres Zeichen mit Spracherkennungs-Engine-Unterstützung aktiviert, versucht der Server, die Spracheingabe zu aktivieren, und generiert das **ListenStart-Ereignis.**

Wenn ein Client versucht, den Lauschmodus mithilfe der [**Listen-Methode**](listen-method.md) zu aktivieren, und keine entsprechende Spracherkennungs-Engine verfügbar ist, schlägt der Aufruf fehl, und der Server generiert kein [**ListenStart-Ereignis.**](listenstart-event.md) Im Microsoft Agent-Steuerelement gibt die **Listen-Methode** **False zurück,** aber der Aufruf gibt keinen Fehler aus.

Wenn der Lauschen-Schlüsselmodus aktiviert ist und der Benutzer zu einem Zeichen wechselt, das eine andere Spracherkennungs-Engine verwendet, wechselt der Server zu dieser Engine und aktiviert sie und löst eine [**ListenComplete**](listencomplete-event.md) und dann ein [**ListenStart-Ereignis**](listenstart-event.md) aus. Wenn das aktivierte Zeichen nicht über eine verfügbare Spracherkennungs-Engine verfügt (da keines installiert ist oder keiner mit der Sprach-ID-Einstellung des aktivierten Zeichens übereinstimmen), löst der Server das **ListenComplete-Ereignis** für das zuvor aktivierte Zeichen aus und übergibt einen Wert im **Cause-Parameter** zurück. Der Server generiert jedoch keine **ListenStart-** oder **ListenComplete-Ereignisse** für die Clients, die keine Spracherkennung unterstützen.

Wenn ein Client erfolgreich die [**Listen-Methode**](listen-method.md) aufruft und ein Zeichen ohne Spracherkennungs-Engine-Unterstützung eingabeaktiv wird, bevor das Time out des Lauschenmodus abgeschlossen ist, und der Benutzer dann zurück zum Zeichen des ursprünglichen Clients wechselt, generiert der Server ein [**ListenStart-Ereignis**](listenstart-event.md) für diesen Client.

Wenn der Eingabe-Aktiv-Client die Spracherkennungs-Engines wechselt, indem [**er srModeID**](srmodeid-property.md) im Lauschenmodus ändert, wechselt der Server zu und aktiviert diese Engine, ohne das ListenStart-Ereignis erneut [**auszulösen.**](listenstart-event.md) Wenn die angegebene Engine jedoch nicht verfügbar ist, schlägt der Aufruf fehl (löst einen Fehler im -Steuerelement aus), und der Server ruft auch das [**ListenComplete-Ereignis**](listencomplete-event.md) auf.

 

 




