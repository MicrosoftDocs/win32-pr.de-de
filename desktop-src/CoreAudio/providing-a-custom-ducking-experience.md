---
description: Eine Anwendung kann die vom System behandelte Standardbenutzeroberfläche für Entzungen deaktivieren und durch eine benutzerdefinierte Implementierung ersetzen.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Bereitstellen eines benutzerdefinierten Entzungsverhaltens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72cf4bb254b97a6a9d6b5c9d415d48a2c95f528f20efbf2ffbe4782ae5980400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406368"
---
# <a name="providing-a-custom-ducking-behavior"></a>Bereitstellen eines benutzerdefinierten Entzungsverhaltens

Eine Anwendung kann die vom System [behandelte Standardbenutzeroberfläche für Entzungen](stream-attenuation.md) deaktivieren und durch eine benutzerdefinierte Implementierung ersetzen.

Eine Anwendung kann eine benutzerdefinierte Benutzeroberfläche bereitstellen. Beispielsweise bietet Windows Media Player eine eigene Benutzeroberfläche, indem der aktuelle Mediendatenstrom während einer Kommunikationssitzung angehalten und die Wiedergabe nach dem Schließen der Sitzung fortsetzen wird. Eine Beispielmedienanwendung, die Enten implementiert, ist in Windows SDK-Beispielen enthalten. Weitere Informationen finden Sie unter [EnteningMediaPlayer.](duckingmediaplayer.md) Informationen zum Simulieren des Öffnens und Schließens von Kommunikationsdatenströmen sowie zum Generieren von Entschließungsereignissen finden Sie unter [EntschließenCaptureSample](duckingcapturesample.md), das auch in Windows SDK-Beispielen enthalten ist.

Eine Medienanwendung, die zu dämpfungsfähige Sounds abspielt, muss die Kommunikationsdatenströme kennen, wenn sie im System geöffnet und geschlossen werden. Die benutzerdefinierte Implementierung kann mit MediaFoundation, DirectShow oder DirectSound bereitgestellt werden, die die Core Audio-APIs verwenden. Ein direkter WASAPI-Client kann auch die Standardbehandlung überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.

**Um eine benutzerdefinierte Benutzeroberfläche bereitzustellen, muss ein WASAPI-Client die folgenden Aufgaben ausführen:**

1.  Registrieren Sie sich, um Entenereignisse vom *Enten-Manager* zu empfangen – eine Komponente des Audiosystems, die Benachrichtigungen im Zusammenhang mit Änderungen des Kommunikationsdatenstroms verarbeitet. Weitere Informationen erhalten Sie unter [Getting Vereigen von Ereignissen.](handling-audio-ducking-events-from-communication-devices.md)
    > [!Note]  
    > Wenn der Client für den Empfang von Entenbenachrichtigungen registriert wird, deaktiviert der Enten-Manager das vom System bereitgestellte Standardverhalten. Wenn das Standardverhalten explizierend deaktiviert ist (siehe Deaktivieren der Standardbenutzeroberfläche für [Enten),](disabling-the-ducking-experience.md)und der Client kein Ersatzverhalten bereitstellt, tritt für die Anwendung kein Abfangverhalten auf.

     

2.  Lauschen Sie auf die vom Enten-Manager gesendeten Benachrichtigungen zu Denkereignissen, und führen Sie das gewünschte Entenverhalten aus. Weitere Informationen zum Implementieren eines Verengungsverhaltens finden Sie unter [Implementierungsüberlegungen für Entenbenachrichtigungen.](handling-audio-ducking-events-from-communication-devices.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines Kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßige Benutzeroberfläche](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardbenutzeroberfläche für die Entzung](disabling-the-ducking-experience.md)
</dt> <dt>

[Überlegungen zur Implementierung von Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Abrufen von Entzungsereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



