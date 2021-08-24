---
description: Standardeinstellung für die Beeinschnung
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Standardeinstellung für die Beeinschnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec323bdaf01a7bba0821a9dee2c349239b3a53660334d2ac57edbf71287f396d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695015"
---
# <a name="default-ducking-experience"></a>Standardeinstellung für die Beeinschnung

Stellen Sie sich ein Szenario vor, in dem ein Benutzer beim Lauschen auf Musik auf dem Computer einen Telefonanruf empfängt. Während des Telefonanrufs möchte der Benutzer die Lautstärke der Musik reduzieren, während er sich an den Telefonanrufen nimmt, und das ursprüngliche Volume fortsetzen, nachdem der Telefonanruf beendet wurde. Abhängig von den optionen, die vom Benutzer in der **Sound-Systemsteuerung** angegeben  werden, stellt das Betriebssystem diese Funktionalität automatisch durch Dämpfung von Strömen oder Streamen zur Verfügung – Verringerung der Intensität eines Audiostreams.

Die Standardeinstellung für die Dämpfung hängt von der Einstellung des Benutzers ab, wie in der Option Sound der **Systemsteuerung** angegeben. Auf der **Registerkarte** Kommunikation kann der Benutzer eine Dämpfungsstufe auswählen (Der Standardwert ist 80 %), alle nicht kommunikationsbasierten Datenströme stummschalten oder die Standardmäßige Streamdämpfungserfahrung deaktivieren. Das System ermöglicht das Öffnen neuer Nichtkommunikationsstreams (mit Ausnahme neuer Systemklänge) während der Kommunikationssitzung, aber die neuen Streams werden nicht automatisch abgedämpft. Wenn alle Kommunikationsstreams geschlossen sind, beendet das System die Kommunikationssitzung und stellt das Volume der Datenströme wieder wieder auf, die während der Kommunikationssitzung abgedämpft wurden.

Um die Streamdämpfung visuell anzugeben, ändert das System die Einstellungen des Volumemixers je nach Benutzereinstellung. Wenn der Benutzer beispielsweise eine Dämpfungsstufe angibt, senkt der Volumemixer den Schieberegler, zeigt das neue abgedämpfte Volume an und zeigt die ursprüngliche Volumeebene an. Die folgende Abbildung veranschaulicht diesen Prozess.

![Diagramm des standarden Streamdämpfungsverhaltens in Windows 7](images/stream-aatenuation.jpg)

Eine Anwendung kann die Streamdämpfung überschreiben und eine benutzerdefinierte Beschningserfahrung implementieren, wenn sie weiß, wann die Kommunikationssitzung gestartet und beendet wird. Weitere Informationen finden Sie unter [Bereitstellen eines benutzerdefinierten Verhaltens für die Zurückdringung.](providing-a-custom-ducking-experience.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Deaktivieren der Standardmäßigen Begeherfahrung](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Verhaltens bei der Abschüssung](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Getting GettingIng Events (Getting GettingIng Events) (Abrufen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



