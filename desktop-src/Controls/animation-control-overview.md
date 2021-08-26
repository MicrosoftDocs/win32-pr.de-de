---
title: Informationen zu Animationssteuerelementen
description: Ein Animationssteuer steuerelement ist ein Fenster, in dem ein Audio-Video AVI-Clip (Interleaved) angezeigt wird. Ein AVI-Clip ist eine Reihe von Bitmapframes wie ein Film. Animationssteuerelemente können nur AVI-Clips anzeigen, die keine Audiodaten enthalten.
ms.assetid: 6be69d1a-5b2c-41d5-b6d7-e86ddac2cb0d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57a2a579334fe266499884ccf40ad1154b3465ffd301c92643f248ff2664ed4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119921790"
---
# <a name="about-animation-controls"></a>Informationen zu Animationssteuerelementen

Ein *Animationssteuer steuerelement* ist ein Fenster, in dem ein Audio-Video ZWISCHENAB-Clip (Interleaved) angezeigt wird. Ein AVI-Clip ist eine Reihe von Bitmapframes wie ein Film. Animationssteuerelemente können nur AVI-Clips anzeigen, die keine Audiodaten enthalten.

Eine häufige Verwendung für ein Animationssteuer steuerelement ist das Angeben der Systemaktivität während eines längeren Vorgangs. Dies ist möglich, da der Vorgangsthread weiterhin ausgeführt wird, während der AVI-Clip angezeigt wird. Beispielsweise zeigt das Dialogfeld Suchen des Windows Explorer eine sich bewegende Lupe an, während das System nach einer Datei sucht.

> [!Note]  
> Wenn Sie Version ComCtl32.dll 6 verwenden, wird der Thread nicht unterstützt. Stellen Sie sicher, dass Ihre Anwendung die Benutzeroberfläche nicht blockiert, da die Animation sonst nicht erfolgt.

 

Ein Animationssteuersatz kann einen AVI-Clip anzeigen, der entweder aus einer unkomprimierten AVI-Datei oder aus einer AVI-Datei stammt, die mithilfe der Codierung der Ausführungslänge (BI \_ RLE8) komprimiert wurde. Sie können den AVI-Clip ihrer Anwendung als AVI-Ressource hinzufügen, oder der Clip kann Ihre Anwendung als separate AVI-Datei begleiten.

> [!Note]  
> Die AVI-Datei oder -Ressource darf keinen Soundkanal haben. Die Funktionen des Animationssteuer steuerelements sind sehr eingeschränkt und können sich ändern. Wenn Sie ein Steuerelement benötigen, um Multimediawiedergabe- und Aufzeichnungsfunktionen für Ihre Anwendung zu bieten, können Sie das MCIWnd-Steuerelement verwenden. Weitere Informationen finden Sie unter [MCIWnd Window Class](/windows/desktop/Multimedia/mciwnd-window-class).

 

In diesem Abschnitt werden die folgenden Themen erläutert.

-   [Erstellung von Animationssteuer steuerelementen](#animation-control-creation)
-   [Informationen zu Animationssteuerungsmeldungen](#about-animation-control-messages)
-   [Standardnachrichtenverarbeitung](#default-message-processing)

## <a name="animation-control-creation"></a>Erstellung von Animationssteuer steuerelementen

Ein Animationssteuer steuerelement gehört zur [**Fensterklasse ANIMATE \_ CLASS.**](common-control-window-classes.md) Sie erstellen ein Animationssteuerobjekt mit der [**CreateWindow- oder**](/windows/desktop/api/winuser/nf-winuser-createwindowa) [**CreateWindowEx-Funktion**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) oder dem [**Animieren des \_ Create-Makros.**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) Das Makro positioniert das Animationssteuerobjekt in der oberen linken Ecke des übergeordneten Fensters und legt die Breite und Höhe des Steuerelements basierend auf den Abmessungen eines Frames im AVI-Clip fest, wenn der [**ACS \_ CENTER-Stil**](animation-control-styles.md) nicht angegeben ist. Wenn **ACS \_ CENTER angegeben** ist, legt **\_ Animieren erstellen** die Breite und Höhe des Steuerelements auf 0 (null) fest. Sie können die [**SetWindowPos-Funktion**](/windows/desktop/api/winuser/nf-winuser-setwindowpos) verwenden, um die Position und Größe des Steuerelements festlegen.

Wenn Sie ein Animationssteuerfeld innerhalb eines Dialogfelds oder aus einer Dialogfeldressource erstellen, wird das Steuerelement automatisch zerstört, wenn der Benutzer das Dialogfeld schließt. Wenn Sie ein Animationssteuer steuerelement innerhalb eines Fensters erstellen, müssen Sie das Steuerelement explizit zerstören.

## <a name="about-animation-control-messages"></a>Informationen zu Animationssteuerungsmeldungen

Eine Anwendung sendet Nachrichten an ein Animationssteuer steuerelement, um den entsprechenden AVI-Clip zu öffnen, wiederzuhalten, zu beenden und zu schließen. Jede Nachricht verfügt über ein oder mehrere Makros, die Sie verwenden können, anstatt die Nachricht explizit zu senden.

Nach dem Erstellen eines Animationssteuer steuerelements sendet eine Anwendung die [**ACM \_ OPEN-Nachricht,**](acm-open.md) um einen AVI-Clip zu öffnen und in den Arbeitsspeicher zu laden. Die Meldung gibt entweder den Pfad einer AVI-Datei oder den Namen einer AVI-Ressource an. Das System lädt die AVI-Ressource aus dem Modul, das das Animationssteuer steuerelement erstellt hat.

Wenn das Animationssteuerfeld über den [**ACS \_ AUTOPLAY-Stil**](animation-control-styles.md) verfügt, beginnt das Steuerelement mit der Wiedergabe des AVI-Clips unmittelbar nach dem Öffnen der AVI-Datei oder DER AVI-Ressource. Andernfalls kann eine Anwendung die [**ACM \_ PLAY-Nachricht verwenden,**](acm-play.md) um den AVI-Clip zu starten. Eine Anwendung kann den Clip jederzeit beenden, indem sie die [**ACM \_ STOP-Nachricht**](acm-stop.md) sendet. Der letzte abgespielte Frame wird angezeigt, wenn das Steuerelement die Wiedergabe des AVI-Clips beendet oder **ACM \_ STOP** gesendet wird.

Ein Animationssteuer steuerelement kann zwei Benachrichtigungscodes an das übergeordnete Fenster senden: [ACN \_ START](acn-start.md) und [ACN \_ STOP.](acn-stop.md) Die meisten Anwendungen verarbeiten keine der beiden Benachrichtigungen.

Um die AVI-Datei oder DIE AVI-Ressource zu schließen und aus dem Arbeitsspeicher zu entfernen, kann eine Anwendung das [**Makro Schließen \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) animieren verwenden, das [**ACM \_ OPEN**](acm-open.md) sendet, bei dem der Dateiname oder Ressourcenname auf **NULL festgelegt ist.**

## <a name="default-message-processing"></a>Standardnachrichtenverarbeitung

In diesem Abschnitt werden die Fenstermeldungen beschrieben, die von der Fensterprozedur für die [**ANIMATE \_ CLASS-Fensterklasse**](common-control-window-classes.md) verarbeitet werden.



| `Message`                                    | Verarbeitung ausgeführt                                                                                                                                                                                                                                                                        |
|--------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)           | Gibt die AVI-Datei oder DIE AVI-Ressource frei, die dem Animationssteuer steuerelement zugeordnet ist.                                                                                                                                                                                                                   |
| [**WM \_ DESTROY**](/windows/desktop/winmsg/wm-destroy)       | Gibt die AVI-Datei oder DIE AVI-Ressource frei, gibt eine interne Datenstruktur frei und ruft dann die [**DefWindowProc-Funktion**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) auf.                                                                                                                                                |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd) | Löscht den Fensterhintergrund mithilfe der aktuellen Hintergrundfarbe für statische Steuerelemente.                                                                                                                                                                                                        |
| [**WM \_ NCCREATE**](/windows/desktop/winmsg/wm-nccreate)     | Ordnet eine interne Datenstruktur zu und initialisiert sie und ruft [**dann DefWindowProc auf.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)                                                                                                                                                                              |
| [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) | Gibt den HTTRANSPARENT-Treffertestwert zurück.                                                                                                                                                                                                                                                   |
| [**WM \_ PAINT**](/windows/desktop/gdi/wm-paint)              | Zeichnet einen AVI-Frame im Animation-Steuerelement.                                                                                                                                                                                                                                                |
| [**WM \_ SIZE**](/windows/desktop/winmsg/wm-size)             | Überprüft, ob das Steuerelement den [**ACS \_ CENTER-Stil**](animation-control-styles.md) auf hat. Wenn das Steuerelement dies nicht tut, ruft es [**DefWindowProc auf.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Andernfalls wird die Animation im -Steuerelement centert, das Steuerelement für ungültig erklärt und **dann DefWindowProc aufruft.** |



 

 

 