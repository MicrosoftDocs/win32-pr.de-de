---
title: Probleme bei der Spracheingabe
description: Probleme bei der Spracheingabe
ms.assetid: b42664a2-9615-4e15-97a6-115e9556096b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a7b29a85c79996eb0c01260c8e2b738fcd926f2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947611"
---
# <a name="speech-input-problems"></a>Probleme bei der Spracheingabe

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

### <a name="the-character-does-not-respond-to-my-spoken-input"></a>Das Zeichen antwortet nicht auf meine gesprochene Eingabe.

Dieses Symptom kann durch eine Reihe von Problemen verursacht werden. Versuchen Sie Folgendes, um das Problem zu isolieren:

-   Vergewissern Sie sich, dass Ihr Mikrofon ordnungsgemäß angeschlossen ist. Es ist eine gute Idee, Sie mit einer anderen Sound Eingabe Anwendung zu testen, um sicherzustellen, dass Sie ordnungsgemäß funktioniert.
-   Überprüfen Sie, ob eine kompatible Sprach-Engine installiert ist. Öffnen Sie unter Windows 95, Windows 98 und Windows NT 4,0 die Systemsteuerung. Wenn Sie das sprach Objekt dort finden, öffnen Sie es, und es werden die auf Ihrem System verfügbaren und installierten Sprach-Engines aufgelistet.
-   Vergewissern Sie sich, dass Ihre Soundkarte mit Microsoft Windows 95, Windows 98 oder Windows NT kompatibel ist.

    Die beste Möglichkeit hierfür ist, die in Windows verwendete Sound Recorder-Anwendung auszuführen. Sie befindet sich normalerweise im Startmenü. Klicken Sie auf die Schaltfläche Start, klicken Sie auf Programme, klicken Sie auf Zubehör, klicken Sie auf Multimedia und dann auf Sound Recorder. Wenn das Sound Recorder-Fenster angezeigt wird, klicken Sie auf die Schaltfläche **Datensatz** , und sprechen Sie mit Ihrem Mikrofon. Die Zeile im Fenster sollte als Reaktion auf Ihre Spracheingabe animiert werden.

    Wenn die Sound Recorder-Anwendung nicht auf Ihrem System funktioniert, wenden Sie sich an den technischen Support des Sound Karten Herstellers, um Unterstützung zu erhalten. Ihre Soundkarte ist möglicherweise nicht mit Windows kompatibel, oder es liegt ein Problem mit den Software Treibern für Ihre Soundkarte vor.

-   Überprüfen Sie, ob die Audioeingabe für die Spracheingabe ordnungsgemäß festgelegt ist.
    1.  Öffnen Sie das Spracheingabe Objekt in der Systemsteuerung. Wenn das sprach Objekt nicht vorhanden ist, installieren Sie eines.
    2.  Wählen Sie die Spracheingabe-Engine aus, die Sie installiert haben.
    3.  Wählen Sie die Schaltfläche Mikrofon Einstellungen-Assistent aus. Wenn diese Schaltfläche deaktiviert angezeigt wird, ist keine kompatible Sprach-Engine installiert, oder die von Ihnen installierte Sprach-Engine unterstützt möglicherweise keine automatische Anpassung.
-   Stellen Sie sicher, dass die agentaktivierte Anwendung oder Webseite Spracheingaben unterstützt. Nicht alle Seiten (oder Anwendungen) unterstützen Spracheingaben. Halten Sie die Abhör Taste gedrückt. In der Regel ist dies der Schiebe Sperr Schlüssel, es sei denn, Sie haben ihn geändert. Unter dem Zeichen sollte ein Popup Fenster angezeigt werden. Der Text im Tipp gibt Aufschluss über den Abhör Zustand des Zeichens. Wenn kein Tipp angezeigt wird, unterstützt weder die Anwendung noch die Webseite Spracheingaben, oder Sie verfügen nicht über eine kompatible Sprach-Engine. Wenn der Tipp angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der Sprachbefehle des Zeichens. Wenn Sie nicht wissen, welche Sprachbefehle verfügbar sind, geben Sie die Abhör Taste frei, und klicken Sie mit der rechten Maustaste auf das Zeichen. Wählen Sie dann im Popupmenü die Option Sprachbefehle öffnen aus. Wenn der Befehl nicht angezeigt wird, ist die Sprachunterstützung für die verwendete Anwendung oder Webseite nicht verfügbar. Wenn er angezeigt wird, halten Sie die überwachende Taste gedrückt. Wenn der lausch Text unter dem-Zeichen angezeigt wird und angibt, dass das Zeichen lauscht, sprechen Sie einen der im Fenster aufgeführten Befehle an. Wenn das Zeichen nicht antwortet, fahren Sie mit dem nächsten Schritt fort.
-   Vergewissern Sie sich, dass zurzeit keine andere Anwendung das Audioausgabegerät verwendet.
-   Vergewissern Sie sich, dass die Verwendung von MIDI durch den Microsoft-Agent den Audiokanal nicht blockiert (Weitere Informationen finden Sie in den [Anwendungen, die bei der Ausführung des Microsoft-Agents keine Audioausgabe haben](output-problems.md), im Abschnitt Ausgabe Probleme).
-   Wenn Sie die obigen Schritte ausgeführt haben, aber weiterhin Probleme mit der Spracheingabe haben, überprüfen Sie, ob Ihre Soundkarte und Treibersoftware mit der von Ihnen verwendeten Sprach-Engine kompatibel sind. Informieren Sie sich mit dem technischen Support für Ihre Soundkarte und ihren sprach Hersteller Hersteller.

### <a name="the-midi-tone-seems-to-disrupts-speech-input"></a>Der MIDI-Ton scheint die Spracheingabe zu stören.

Reduzieren Sie das MIDI-Volume mithilfe der folgenden Schritte.

1.  Öffnen Sie das Fenster volumesteuerung, indem Sie in der Taskleiste mit der rechten Maustaste auf das Redner Symbol klicken oder indem Sie in der Systemsteuerung das Multimediaobjekt öffnen. Klicken Sie im Abschnitt Wiedergabe der Seite Audioseite auf die Schaltfläche Volume.
2.  Verringern Sie das MIDI-Volume durch Verschieben des Schiebereglers.

### <a name="the-character-does-not-respond-to-voice-input-but-i-can-hear-my-voice-through-my-speakers-when-i-talk-into-my-microphone"></a>Das Zeichen antwortet nicht auf Spracheingaben, aber ich kann meine Stimme über meine Redner hören, wenn ich mit meinem Mikrofon spreche.

Ihre Soundkarte ist nicht ordnungsgemäß für die Verwendung mit dem Microsoft-Agent eingerichtet. Wählen Sie den Assistenten für die Mikrofon Einstellungen auf dem Eigenschaften Blatt des sprach Objekts in der Systemsteuerung aus. Informationen zum Zugriff auf diese Schaltfläche finden Sie in den Schritten für "[das Zeichen antwortet nicht auf meine gesprochene Eingabe](#the-character-does-not-respond-to-my-spoken-input)".

 

 




