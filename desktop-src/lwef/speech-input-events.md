---
title: Spracheingabe Ereignisse
description: Spracheingabe Ereignisse
ms.assetid: d7b621fe-9274-4b16-af8a-664b0b296c89
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0dc75bb010286b7645c206d192913017472829d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037632"
---
# <a name="speech-input-events"></a>Spracheingabe Ereignisse

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Außerdem benachrichtigt der Agent bei [**der Ereignis**](command-event.md) Benachrichtigungs Benachrichtigung den aktiven Client, wenn der Server den Empfangsmodus aktiviert oder deaktiviert, mithilfe der Ereignisse [**ListenStart**](listenstart-event.md) und [**listencomplete**](listencomplete-event.md) ([**iagentnotifysink Ex:: listeningstate**](iagentnotifysinkex--listeningstate.md)). Wenn der Benutzer jedoch die Taste für den Lesemodus drückt und keine passende sprach Erkennungs-Engine für das oberste Zeichen des Eingabe aktiven Clients verfügbar ist, startet der Server den lauschenden Hotkey-Modus, aber generiert kein **ListenStart** -Ereignis für den aktiven Client des Zeichens. Wenn der Benutzer vor dem Abschluss des Timeouts ein anderes Zeichen mit Unterstützung für sprach Erkennungs-Engine aktiviert, versucht der Server, die Spracheingabe zu aktivieren und das **ListenStart** -Ereignis zu generieren.

Wenn ein Client versucht [**, den Empfangsmodus mithilfe der Abhör**](listen-method.md) Methode zu aktivieren, und keine passende sprach Erkennungs-Engine verfügbar ist, schlägt der-Befehl fehl, und der Server generiert kein [**ListenStart**](listenstart-event.md)-Ereignis. Im Microsoft-Agent-Steuerelement gibt die Abhör Methode **false** zurück, **aber der-** Befehl gibt keinen Fehler aus.

Wenn der Modus für den Überwachungs Schlüssel aktiviert ist und der Benutzer zu einem Zeichen wechselt, das eine andere Spracherkennungs-Engine verwendet, schaltet der Server zu und aktiviert diese Engine und löst ein [**listencomplete**](listencomplete-event.md) -Ereignis und dann ein [**ListenStart**](listenstart-event.md) -Ereignis aus. Wenn das aktivierte Zeichen nicht über eine verfügbare Spracherkennungs-Engine verfügt (weil eine nicht installiert ist oder keine mit der Sprach-ID-Einstellung des aktivierten Zeichens identisch ist), löst der Server das **listencomplete** -Ereignis für das zuvor aktivierte Zeichen aus und gibt einen Wert im Parameter " **Ursache** " zurück. Der Server generiert jedoch keine **ListenStart** -oder **listencomplete** -Ereignisse für Clients, für die keine sprach Erkennungs Unterstützung vorhanden ist.

Wenn ein [**Client die Abhör**](listen-method.md) Methode erfolgreich aufruft und ein Zeichen ohne sprach Erkennungs-Engine-Unterstützung vor Abschluss des Timeouts für die sprach Erkennungs-Engine in den Eingangs Modus wechselt, wird vom Server ein [**ListenStart**](listenstart-event.md) -Ereignis für diesen Client generiert.

Wenn der Input-Active Client die Spracherkennungs-Engines durch Ändern von [**srmodeid**](srmodeid-property.md) im Empfangsmodus wechselt, schaltet der Server zu und aktiviert diese Engine, ohne das [**ListenStart**](listenstart-event.md) -Ereignis erneut auszulösen. Wenn die angegebene Engine jedoch nicht verfügbar ist, schlägt der Aufruf fehl (löst einen Fehler im-Steuerelement aus), und der Server ruft auch das [**listencomplete**](listencomplete-event.md) -Ereignis auf.

 

 




