---
description: Eine Anwendung kann die standardmäßige Ducking-Benutzerfreundlichkeit, die vom System verarbeitet wird, ablehnen und durch eine benutzerdefinierte Implementierung ersetzen.
ms.assetid: 18290d05-b114-476b-8365-6bbb5fe6cffc
title: Bereitstellen eines benutzerdefinierten Ducking-Verhaltens
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4051dc7b79f698f10d007beaafa97e90d79f3b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127425"
---
# <a name="providing-a-custom-ducking-behavior"></a>Bereitstellen eines benutzerdefinierten Ducking-Verhaltens

Eine Anwendung kann die [standardmäßige Ducking](stream-attenuation.md) -Benutzerfreundlichkeit, die vom System verarbeitet wird, ablehnen und durch eine benutzerdefinierte Implementierung ersetzen.

Eine Anwendung kann eine benutzerdefinierte Ducking-Benutzerfreundlichkeit bereitstellen. Beispielsweise bietet Windows Media Player eine eigene Ducking-Umgebung, indem der aktuelle Mediendaten Strom während einer Kommunikationssitzung angehalten und die Wiedergabe fortgesetzt wird, wenn die Sitzung geschlossen wird. Ein Beispiel für eine Medien Anwendung, die das Ducking implementiert, ist in Windows SDK Beispielen enthalten. Weitere Informationen finden Sie unter [duckingmediaplayer](duckingmediaplayer.md). Informationen zum Simulieren des Öffnens und Schließens von Kommunikationsstreams und zum Erstellen von Ducking-Ereignissen finden Sie unter " [duckingcapturesample](duckingcapturesample.md)", das auch in Windows SDK Beispielen enthalten ist.

Eine Medien Anwendung, die zu dämpfende Sounds wieder gibt, muss die Kommunikationsstreams beachten, wenn Sie im System geöffnet und geschlossen werden. Die benutzerdefinierte Implementierung kann mithilfe von mediafoundations, DirectShow oder DirectSound bereitgestellt werden, die die kernaudio-APIs verwenden. Ein direkter WASAPI-Client kann die Standardbehandlung auch überschreiben, wenn er weiß, wann die Kommunikationssitzung gestartet und beendet wird.

**Zum Bereitstellen einer benutzerdefinierten Ducking-Funktion muss ein WASAPI-Client die folgenden Aufgaben ausführen:**

1.  Registrieren Sie sich für den Empfang von abzurufenden Ereignissen vom *Ducking-Manager*– eine Komponente des Audiosystems, die Benachrichtigungen im Zusammenhang mit Änderungen des Kommunikationsdaten Stroms verarbeitet Weitere Informationen finden Sie unter [erhalten von Ducking-Ereignissen](handling-audio-ducking-events-from-communication-devices.md).
    > [!Note]  
    > Wenn der Client für den Empfang von Benachrichtigungen registriert wird, wird das vom System bereitgestellte Standardverhalten deaktiviert. Wenn das Standardverhalten explizit deaktiviert ist (siehe [Deaktivieren der standardmäßigen Ducking](disabling-the-ducking-experience.md)-Darstellung) und der Client kein Ersatz Verhalten bereitstellt, tritt bei der Anwendung kein Ducking-Verhalten auf.

     

2.  Lauschen Sie auf die vom Ducking-Manager gesendeten Enten Ereignis Benachrichtigungen, und führen Sie das gewünschte Ducking-Verhalten aus. Weitere Informationen zum Implementieren eines Ducking-Verhaltens finden Sie unter [Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden eines kommunikationsgeräts](using-the-communication-device.md)
</dt> <dt>

[Standardmäßiges ducken](stream-attenuation.md)
</dt> <dt>

[Deaktivieren der Standardeinstellung für das ducken](disabling-the-ducking-experience.md)
</dt> <dt>

[Implementierungs Überlegungen für Ducking-Benachrichtigungen](handling-audio-ducking-events-from-communication-devices.md)
</dt> <dt>

[Erhalten von Ducking-Ereignissen](getting-ducking-events-from-a-communication-device.md)
</dt> </dl>

 

 



