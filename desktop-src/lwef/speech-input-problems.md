---
title: Spracheingabeprobleme
description: Spracheingabeprobleme
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d135ac8a098f52066854c6003c22caa7290efbd01c8038bda116cd843b21a2e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118246229"
---
# <a name="speech-input-problems"></a>Spracheingabeprobleme

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>Das Zeichen antwortet nicht auf meine gesprochene Eingabe.

Dieses Symptom kann durch eine Reihe von Problemen verursacht werden. Versuchen Sie Folgendes, um das Problem zu isolieren:

-   Vergewissern Sie sich, dass Ihr Mikrofon ordnungsgemäß angeschlossen ist. Es empfiehlt sich, sie mit einer anderen Soundeingabeanwendung zu testen, um sicherzustellen, dass sie ordnungsgemäß funktioniert.
-   Überprüfen Sie, ob eine kompatible Sprach-Engine installiert ist. Öffnen Sie unter Windows 95, Windows 98 und Windows NT 4.0 die Systemsteuerung. Wenn Sie das Speech-Objekt dort finden, öffnen Sie es, und es listet die verfügbaren und auf Ihrem System installierten Speech-Engines auf.
-   Vergewissern Sie sich, dass Ihre Soundkarte mit Microsoft Windows 95, Windows 98 oder Windows NT kompatibel ist.

    Die beste Möglichkeit hierfür ist das Ausführen der Sound Recorder-Anwendung, die im Lieferumfang von Windows ist. Sie finden sie in der Regel auf der Startmenü. Klicken Sie auf die Schaltfläche "Start", klicken Sie auf Programme, klicken Sie auf Zubehör, klicken Sie auf Multimedia, und klicken Sie dann auf Sound Recorder. Wenn das Fenster Sound Recorder angezeigt wird, klicken Sie auf die Schaltfläche **Aufzeichnen,** und sprechen Sie mit Ihrem Mikrofon. Die Zeile im Fenster sollte als Reaktion auf Ihre Spracheingabe animiert werden.

    Wenn die Sound Recorder-Anwendung auf Ihrem System nicht funktioniert, wenden Sie sich an die technische Supportabteilung des Soundkartenherstellers, um Unterstützung zu erhalten. Ihre Soundkarte ist möglicherweise nicht mit Windows kompatibel, oder es besteht ein Problem mit den Softwaretreibern für Ihre Soundkarte.

-   Vergewissern Sie sich, dass Ihre Soundeingabe für die Spracheingabe richtig festgelegt ist.
    1.  Öffnen Sie das Speech-Eingabeobjekt im Systemsteuerung. Wenn das Speech-Objekt nicht vorhanden ist, installieren Sie eines.
    2.  Wählen Sie die installierte Spracheingabe-Engine aus.
    3.  Wählen Sie die Schaltfläche Mikrofon Einstellungen Assistenten aus. Wenn diese Schaltfläche deaktiviert angezeigt wird, ist keine kompatible Sprach-Engine installiert, oder die installierte Sprach-Engine unterstützt möglicherweise keine automatische Anpassung.
-   Überprüfen Sie, ob die Agent-fähige Anwendung oder Webseite Spracheingaben unterstützt. Nicht alle Seiten (oder Anwendungen) unterstützen Spracheingaben. Drücken Sie die Taste Lauschen, und halten Sie sie gedrückt. In der Regel ist dies die Scrollsperre, sofern Sie sie nicht geändert haben. Unter dem Zeichen sollte ein Popupfenster angezeigt werden. Der Text im Trinkgeld teilt Ihnen den Lauschenzustand des Zeichens mit. Wenn kein Tipp angezeigt wird, unterstützt die Anwendung oder Webseite keine Spracheingaben, oder Sie haben keine kompatible Sprach-Engine installiert. Wenn der Tipp angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der Sprachbefehle des Zeichens. Wenn Sie nicht wissen, welche Sprachbefehle verfügbar sind, geben Sie die Taste Lauschen frei, und klicken Sie mit der rechten Maustaste auf das Zeichen. Wählen Sie dann im Popupmenü Voice Commands Window (Sprachbefehlsfenster öffnen) aus. Wenn der Befehl nicht angezeigt wird, ist die Sprachunterstützung für die von Ihnen verwendete Anwendung oder Webseite nicht verfügbar. Wenn sie angezeigt wird, drücken Sie , und halten Sie die Taste Lauschen erneut gedrückt. Wenn der Lauschen-Tipp unter dem Zeichen angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der im Fenster aufgeführten Befehle. Wenn das Zeichen nicht antwortet, fahren Sie mit dem nächsten Schritt fort.
-   Vergewissern Sie sich, dass derzeit keine andere Anwendung das Audioausgabegerät verwendet.
-   Stellen Sie sicher, dass der Audiokanal durch den Microsoft-Agent nicht durch die Verwendung von QUOTT blockiert wird .(Weitere Informationen finden Sie im Abschnitt Ausgabeprobleme unter [Anwendungen, die DIE AUDIO-Ausgabe wiedergeben, wenn der Microsoft-Agent ausgeführt wird.)](output-problems.md)
-   Wenn Sie die obigen Schritte ausgeführt haben, aber weiterhin Probleme mit der Spracheingabe haben, überprüfen Sie, ob Ihre Soundkarte und Treibersoftware mit der verwendeten Sprach-Engine kompatibel ist. Wenden Sie sich an den technischen Support für Ihre Soundkarte und den Hersteller Ihrer Sprach-Engine.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>Der TONE-Ton scheint die Spracheingabe zu unterbrechen.

Reduzieren Sie das VOLUMES-Volume mit den folgenden Schritten.

1.  Öffnen Sie das Fenster Volumesteuerung, indem Sie mit der rechten Maustaste auf das Lautsprechersymbol in der Taskleiste klicken oder indem Sie das Multimedia-Objekt im Systemsteuerung öffnen. Klicken Sie auf der Audioseite im Abschnitt Wiedergabe auf die Schaltfläche Volume.
2.  Verringern Sie das VOLUMES-Volume, indem Sie den Schieberegler nach unten bewegen.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>Das Zeichen reagiert nicht auf Spracheingaben, aber ich kann meine Stimme über meine Lautsprecher hören, wenn ich mit dem Mikrofon sprach.

Ihre Soundkarte ist nicht ordnungsgemäß für die Verwendung mit Dem Microsoft-Agent eingerichtet. Wählen Sie im Eigenschaftenblatt des Speech-Objekts im Systemsteuerung den Assistenten für mikrofon Einstellungen aus. Informationen zum Zugriff auf diese Schaltfläche finden Sie in den Schritten für " Das Zeichen antwortet nicht auf[meine gesprochene Eingabe".](#the-character-does-not-respond-to-my-spoken-input)

 

 




