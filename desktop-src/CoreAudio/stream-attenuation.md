---
description: Standardmäßiges ducken
ms.assetid: 2ad9482f-1888-4f19-bc41-9d47a8e0ed15
title: Standardmäßiges ducken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d81aa22254ab33ee7396fd4a22d83cc7f5a58041
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748529"
---
# <a name="default-ducking-experience"></a>Standardmäßiges ducken

Stellen Sie sich ein Szenario vor, in dem ein Benutzer einen Telefonanruf erhält, während er die Musik auf dem Computer hört. Während des Telefonanrufs möchte der Benutzer die Lautstärke der Musik reduzieren, während er an den Telefonanruf teilnimmt, und das ursprüngliche Volume fortsetzen, nachdem der Telefonanruf beendet wurde. Abhängig von den Optionen, die vom Benutzer in der **Sounds** -Systemsteuerung angegeben werden, stellt das Betriebssystem diese Funktion automatisch durch *Ducking* -oder *streamdämpfung* bereit – Verringerung der Intensität eines Audiostreams.

Die standardmäßige Dämpfung ist abhängig von der Benutzereinstellung, wie in der **Sound** Option der Systemsteuerung angegeben. Auf der Registerkarte **Kommunikation** kann der Benutzer eine Dämpfung auswählen (der Standardwert ist 80%), alle nicht-Kommunikationsstreams stumm schalten oder die standardmäßige Datenstrom Dämpfung deaktivieren. Das System ermöglicht das Öffnen neuer nicht-Kommunikationsstreams (außer bei neuen Systemsounds) während der Kommunikationssitzung, die neuen Streams werden jedoch nicht automatisch abgeschwächt. Wenn alle Kommunikationsstreams geschlossen sind, beendet das System die Kommunikationssitzung und stellt die Menge der Datenströme wieder her, die während der Kommunikationssitzung gedämpft wurden.

Um die streamdämpfung visuell anzugeben, ändert das System die volumemixer-Einstellungen abhängig von der Benutzereinstellung. Wenn der Benutzer z. b. eine Dämpfungs Ebene angibt, wird der Schieberegler vom volumemixer gesenkt, das neue abgedämpfte Volume wird angezeigt, und die ursprüngliche Volumeebene wird angezeigt. Dieses Verfahren wird in der folgenden Abbildung veranschaulicht.

![Diagramm des standardmäßigen streamdedäsierungsverhaltens in Windows 7](images/stream-aatenuation.jpg)

Eine Anwendung kann die Datenstrom Dämpfung überschreiben und eine benutzerdefinierte Ducking-Funktion implementieren, wenn Sie weiß, wann die Kommunikationssitzung beginnt und endet. Weitere Informationen finden Sie unter [Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Deaktivieren der Standardeinstellung für das ducken](disabling-the-ducking-experience.md)
</dt> <dt>

[Bereitstellen eines benutzerdefinierten Ducking-Verhaltens](providing-a-custom-ducking-experience.md)
</dt> <dt>

[Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Erhalten von Ducking-Ereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



