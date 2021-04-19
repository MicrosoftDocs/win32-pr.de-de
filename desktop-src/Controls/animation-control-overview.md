---
title: Informationen zu Animations Steuerelementen
description: Ein Animations Steuerelement ist ein Fenster, in dem ein Audio-Video Interleaved (AVI)-Clip angezeigt wird. Ein AVI-Clip ist eine Reihe von bitmapframes, wie z. b. einem Film. Von Animations Steuerelementen können nur AVI-Clips angezeigt werden, die keine Audiodaten enthalten.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1625828e5f4febce7314da365c9db93ce3a07136
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106341563"
---
# <a name="about-animation-controls"></a>Informationen zu Animations Steuerelementen

Ein *Animations Steuer* Element ist ein Fenster, in dem ein Audio-Video Interleaved (AVI)-Clip angezeigt wird. Ein AVI-Clip ist eine Reihe von bitmapframes, wie z. b. einem Film. Von Animations Steuerelementen können nur AVI-Clips angezeigt werden, die keine Audiodaten enthalten.

Ein Animations Steuerelement wird häufig verwendet, um die Systemaktivität während eines langen Vorgangs anzuzeigen. Dies ist möglich, da der Vorgangs Thread weiterhin ausgeführt wird, während der AVI-Clip angezeigt wird. Im Dialogfeld Suchen von Windows Explorer wird z. b. ein beweglicher Vergrößerungsglas angezeigt, während das System nach einer Datei sucht.

> [!Note]  
> Wenn Sie ComCtl32.dll Version 6 verwenden, wird der Thread nicht unterstützt. Stellen Sie sicher, dass die Benutzeroberfläche nicht von der Anwendung blockiert wird, da andernfalls keine Animation stattfindet.

 

Ein Animations Steuerelement kann einen AVI-Clip anzeigen, der aus einer unkomprimierten AVI-Datei oder aus einer mit der Lauf Zeit Länge (BI RLE8) komprimierten AVI-Datei stammt \_ . Sie können den AVI-Clip als AVI-Ressource zu Ihrer Anwendung hinzufügen, oder der Clip kann die Anwendung als separate AVI-Datei begleiten.

> [!Note]  
> Die AVI-Datei bzw. Ressource darf keinen Audiokanal aufweisen. Die Funktionen des Animations Steuer Elements sind sehr eingeschränkt und können geändert werden. Wenn Sie ein Steuerelement benötigen, um Multimedia-Wiedergabe-und Aufzeichnungsfunktionen für Ihre Anwendung bereitzustellen, können Sie das mciwnd-Steuerelement verwenden. Weitere Informationen finden Sie unter [mciwnd Window Class](/windows/desktop/Multimedia/mciwnd-window-class).

 

In diesem Abschnitt werden die folgenden Themen behandelt.

-   [Erstellen eines Animations Steuer Elements](#animation-control-creation)
-   [Informationen zu Animations Steuerungs Meldungen](#about-animation-control-messages)
-   [Standard Nachrichtenverarbeitung](#default-message-processing)

## <a name="animation-control-creation"></a>Erstellen eines Animations Steuer Elements

Ein Animations Steuerelement gehört zur [**animieren \_ Class**](common-control-window-classes.md) Window-Klasse. Sie erstellen ein Animations Steuerelement mit der Funktion "up [**Window**](/windows/desktop/api/winuser/nf-winuser-createwindowa) " oder "up Create [**" oder dem**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) Makro " [**animieren \_ Erstellen**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ". Das-Makro positioniert das Animations Steuerelement in der oberen linken Ecke des übergeordneten Fensters und legt die Breite und Höhe des Steuer Elements auf der Grundlage der Abmessungen eines Frames im AVI-Clip fest, wenn der [**ACS- \_ Mittelwert**](animation-control-styles.md) nicht angegeben ist. Wenn **ACS \_ Center** angegeben ist, legt **animieren \_ Create** die Breite und Höhe des Steuer Elements auf 0 (null) fest. Sie können die [**SetWindowPos**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) -Funktion verwenden, um die Position und Größe des Steuer Elements festzulegen.

Wenn Sie ein Animations Steuerelement in einem Dialogfeld oder einer Dialogfeld Ressource erstellen, wird das Steuerelement automatisch zerstört, wenn der Benutzer das Dialogfeld schließt. Wenn Sie ein Animations Steuerelement in einem Fenster erstellen, müssen Sie das Steuerelement explizit zerstören.

## <a name="about-animation-control-messages"></a>Informationen zu Animations Steuerungs Meldungen

Eine Anwendung sendet Nachrichten an ein Animations Steuerelement, um den entsprechenden AVI-Clip zu öffnen, wiederzugeben, zu beenden und zu schließen. Jede Nachricht verfügt über ein oder mehrere Makros, die Sie verwenden können, statt die Nachricht explizit zu senden.

Nach dem Erstellen eines Animations Steuer Elements sendet eine Anwendung die [**\_ geöffnete ACM**](acm-open.md) -Nachricht, um einen AVI-Clip zu öffnen und in den Arbeitsspeicher zu laden. Die Meldung gibt entweder den Pfad einer AVI-Datei oder den Namen einer AVI-Ressource an. Das System lädt die AVI-Ressource aus dem Modul, das das Animations Steuerelement erstellt hat.

Wenn das Animations Steuerelement über die [**ACS- \_ AutoPlay**](animation-control-styles.md) -Art verfügt, beginnt das Steuerelement, den AVI-Clip sofort nach dem Öffnen der AVI-Datei oder der AVI-Ressource abspielen. Andernfalls kann eine Anwendung die [**ACM- \_ Wiedergabe**](acm-play.md) Nachricht verwenden, um den AVI-Clip zu starten. Eine Anwendung kann den Clip jederzeit beenden, indem Sie die [**ACM- \_ Stoppnachricht**](acm-stop.md) sendet. Der letzte wiedergegebene Frame wird angezeigt, wenn das-Steuerelement die Wiedergabe des AVI-Clips oder das Senden von **ACM \_** beendet hat.

Ein Animations Steuerelement kann zwei Benachrichtigungs Codes an das übergeordnete Fenster senden: [ACN \_ Start](acn-start.md) und [ACN \_ Beenden](acn-stop.md). Die meisten Anwendungen verarbeiten keine Benachrichtigung.

Um die AVI-Datei oder die AVI-Ressource zu schließen und aus dem Arbeitsspeicher zu entfernen, kann eine Anwendung das [**animieren \_ Close**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) -Makro verwenden, das [**ACM \_ geöffnet**](acm-open.md) sendet, wobei der Dateiname oder der Ressourcen Name auf **null** festgelegt ist.

## <a name="default-message-processing"></a>Standard Nachrichtenverarbeitung

In diesem Abschnitt werden die Fenster Meldungen beschrieben, die von der Fenster Prozedur für die Animation [**\_ Class**](common-control-window-classes.md) Window Class behandelt werden.



| `Message`                                    | Verarbeitung wird ausgeführt                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ Schließen**](/windows/desktop/winmsg/wm-close)           | Gibt die dem Animations Steuerelement zugeordnete AVI-Datei oder AVI-Ressource frei.                                                                                                                                                                                                                   |
| [**WM \_ zerstören**](/windows/desktop/winmsg/wm-destroy)       | Gibt die AVI-Datei oder die AVI-Ressource frei, gibt eine interne Datenstruktur frei und ruft dann die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion auf.                                                                                                                                                |
| [**WM- \_ erasebkgnd**](/windows/desktop/winmsg/wm-erasebkgnd) | Löscht den Fenster Hintergrund mithilfe der aktuellen Hintergrundfarbe für statische Steuerelemente.                                                                                                                                                                                                        |
| [**WM- \_ nccreate**](/windows/desktop/winmsg/wm-nccreate)     | Ordnet eine interne Datenstruktur zu und initialisiert sie und ruft dann [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)auf.                                                                                                                                                                              |
| [**WM- \_ nchittest**](/windows/desktop/inputdev/wm-nchittest) | Gibt den Wert für den httransparent-Treffer Test zurück.                                                                                                                                                                                                                                                   |
| [**WM- \_ Paint**](/windows/desktop/gdi/wm-paint)              | Zeichnet einen AVI-Frame im Animations Steuerelement.                                                                                                                                                                                                                                                |
| [**WM- \_ Größe**](/windows/desktop/winmsg/wm-size)             | Überprüft, ob das Steuerelement über den [**ACS- \_ mittelstil**](animation-control-styles.md) verfügt. Wenn das-Steuerelement dies nicht bewirkt, wird [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)aufgerufen. Andernfalls wird die Animation im Steuerelement zentriert, das Steuerelement für ungültig erklärt und dann " **defwindowproc**" aufgerufen. |



 

 

 