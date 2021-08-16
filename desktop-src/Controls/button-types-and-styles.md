---
title: Schaltflächentypen
description: Es gibt mehrere Arten von Schaltflächen und einen oder mehrere Schaltflächenstile, um zwischen Schaltflächen desselben Typs zu unterscheiden.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5c3614f90c36d5a81603153ec7c8612d61e73e2e98c7f668cb53a6ad2bb584b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832495"
---
# <a name="button-types"></a>Schaltflächentypen

Es gibt mehrere Arten von Schaltflächen und einen oder mehrere Schaltflächenstile, um zwischen Schaltflächen desselben Typs zu unterscheiden.

In diesem Dokument werden die folgenden Themen erläutert.

-   [Schaltflächentypen und Stile](#button-types-and-styles)
-   [Kontrollkästchen](#check-boxes)
-   [Gruppenfelder](#group-boxes)
-   [Schaltflächen drücken](#push-buttons)
-   [Optionsfelder](#radio-buttons)
-   [Zugehörige Themen](#related-topics)

## <a name="button-types-and-styles"></a>Schaltflächentypen und Stile

Eine Schaltfläche gehört zu einem Typ und kann zusätzliche Stile aufweisen, die sich auf die Darstellung und das Verhalten auswirken. Eine Tabelle mit Schaltflächenstilen finden Sie unter [Schaltflächenstile.](button-styles.md)

Der folgende Screenshot zeigt die verschiedenen Arten von Schaltflächen.

![Screenshot eines Dialogfelds mit Beispielen für acht Arten von Schaltflächen](images/buttontypes.png)

Der Screenshot zeigt, wie Schaltflächen in Windows Vista angezeigt werden können. Die Darstellung variiert je nach Betriebssystemversion und dem vom Benutzer festgelegten Design.

Beachten Sie die folgenden Punkte zur Abbildung:

-   Das Kontrollkästchen mit drei Zuständen wird im unbestimmten Zustand angezeigt. Wenn dieses Kontrollkästchen aktiviert oder deaktiviert ist, sieht es wie ein normales Kontrollkästchen aus.
-   Die große Pushschaltfläche wurde programmgesteuert auf den Zustand "Gepusht" festgelegt (durch Senden der [**BM \_ SETSTATE-Nachricht),**](bm-setstate.md) sodass sie auch dann weiterhin angezeigt wird, wenn sie nicht angeklickt wird.
-   Im angezeigten visuellen Stil zyklen der Hintergrund der Standardtaste (oder einer anderen Schaltfläche mit dem Eingabefokus) zwischen Blau und Grau.

## <a name="check-boxes"></a>Kontrollkästchen

Ein *Kontrollkästchen* besteht aus einem quadratischen Feld und einer anwendungsdefiniert Bezeichnung, einem Symbol oder einer Bitmap, die eine Auswahl angibt, die der Benutzer durch Auswählen der Schaltfläche treffen kann. Anwendungen zeigen in der Regel Kontrollkästchen an, damit der Benutzer eine oder mehrere Optionen auswählen kann, die sich nicht gegenseitig ausschließen.

Ein Kontrollkästchen kann eine von vier Formatvorlagen sein: Standard, automatisch, drei Zustände und automatischer Dreizustand, wie durch die Konstanten [**BS \_ CHECKBOX,**](button-styles.md) [**BS \_ AUTOCHECKBOX,**](button-styles.md) [**BS \_ 3STATE**](button-styles.md)und [**BS \_ AUTO3STATE**](button-styles.md)definiert. Jeder Stil kann zwei Häkchenzustände annehmen: aktiviert (ein Häkchen innerhalb des Kontrollkästchens) oder gelöscht (kein Häkchen). Darüber hinaus kann ein Kontrollkästchen mit drei Zuständen einen unbestimmten Zustand annehmen (ein schattiertes Kontrollkästchen innerhalb des Kontrollkästchens), was darauf hindefinieren kann, dass der Benutzer keine Auswahl getroffen hat. Wenn Sie wiederholt auf ein Standard- oder automatisches Kontrollkästchen klicken, wird es von aktiviert in gelöscht und wieder zurückgeschaltet. Wenn Sie wiederholt auf ein Kontrollkästchen mit drei Zuständen klicken, wird das Kontrollkästchen von aktiviert in gelöscht in unbestimmt umgeschaltet, und anschließend wird der Zyklus wiederholt.

Wenn der Benutzer auf ein Kontrollkästchen (eines beliebigen Stils) klickt, erhält das Kontrollkästchen den Tastaturfokus. Das System sendet dem übergeordneten Fenster des Kontrollkästchens eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit dem [BN CLICKED-Benachrichtigungscode. \_](bn-clicked.md) Das übergeordnete Fenster muss diese Meldung nicht behandeln, wenn sie von einem automatischen Kontrollkästchen oder einem automatischen Kontrollkästchen mit drei Zuständen stammt, da das System den Überprüfungsstatus für diese Stile automatisch festlegt. Das übergeordnete Fenster muss die Meldung jedoch verarbeiten, wenn sie von einem nicht automatischen Kontrollkästchen oder einem Kontrollkästchen mit drei Zuständen stammt, da das übergeordnete Fenster für das Festlegen des Überprüfungszustands für diese Stile verantwortlich ist. Unabhängig vom Kontrollkästchenstil zeichnet das System das Kontrollkästchen automatisch neu, sobald sein Zustand geändert wird.

Die Anwendung kann den Status eines Kontrollkästchens mithilfe der [**IsDlgButtonChecked-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) ermitteln.

## <a name="group-boxes"></a>Gruppenfelder

Ein *Gruppenfeld* ist ein Rechteck, das einen Satz von Steuerelementen umschließt, z. B. Kontrollkästchen oder Optionsfelder, mit einer anwendungsdefinierte Textbezeichnung in der oberen linken Ecke. Der einzige Zweck eines Gruppenfelds besteht darin, Steuerelemente zu organisieren, die sich auf einen gemeinsamen Zweck beziehen (in der Regel durch die Bezeichnung angegeben). Das Gruppenfeld verfügt nur über einen Stil, der durch die Konstante [**BS \_ GROUPBOX**](button-styles.md)definiert wird. Da ein Gruppenfeld nicht ausgewählt werden kann, verfügt es über keinen Häkchenzustand, Fokuszustand oder Pushzustand.

## <a name="push-buttons"></a>Schaltflächen drücken

Eine *Pushschaltfläche* ist ein Rechteck, das eine anwendungsdefinierte Textbezeichnung, ein Symbol oder eine Bitmap enthält, die angibt, wie die Schaltfläche funktioniert, wenn der Benutzer sie auswählt.

Eine Schaltfläche kann eine von zwei Formaten sein: Standard oder Standard, wie durch die Konstanten [**BS \_ PUSHBUTTON**](button-styles.md) und [**BS \_ DEFPUSHBUTTON**](button-styles.md)definiert. In der Regel wird eine Standardtaste zum Starten eines Vorgangs verwendet. Er erhält den Tastaturfokus, wenn der Benutzer darauf klickt. In der Regel wird eine Standardtaste verwendet, um die gängigste oder standardverwendete Auswahl anzugeben, z. B. das Schließen des Dialogfelds. Es handelt sich um eine Schaltfläche, die der Benutzer auswählen kann, indem er einfach die EINGABETASTE drückt, wenn keine andere Schaltfläche im Dialogfeld den Eingabefokus besitzt.

Wenn der Benutzer auf eine Pushschaltfläche klickt, erhält er den Tastaturfokus. Das System sendet dem übergeordneten Fenster der Schaltfläche eine [**WM \_ COMMAND-Meldung,**](/windows/desktop/menurc/wm-command) die den [BN CLICKED-Benachrichtigungscode \_](bn-clicked.md) enthält.

Die *Unterteilte Schaltfläche* ist eine spezielle Art von Pushschaltfläche, die in Windows Vista und [Version 6.00](common-control-versions.md)eingeführt wurde. Eine Unterteilte Schaltfläche ist in zwei Teile unterteilt. Der Hauptteil funktioniert wie eine reguläre oder Standard-Pushschaltfläche. Der zweite Teil verfügt über einen Pfeil, der nach unten zeigt. In der Regel wird ein Menü angezeigt, wenn auf den Pfeil geklickt wird.

Eine Unterteilte Schaltfläche verfügt über den [**BS \_ SPLITBUTTON-Stil**](button-styles.md) oder den [**\_ BS-DEFSPLITBUTTON-Stil,**](button-styles.md) wenn es sich um die Standardschaltfläche in einem Dialogfeld handelt. Sie können die Darstellung der Schaltfläche ändern, indem Sie die [**BCM \_ SETSPLITINFO-Meldung**](bcm-setsplitinfo.md) oder das entsprechende [**Button \_ SetSplitInfo-Makro**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) verwenden.

Wenn der Benutzer auf den Hauptteil der Geteilt-Schaltfläche klickt, sendet er eine [ \_ BN-CLICKED-Benachrichtigung](bn-clicked.md) wie eine normale Pushschaltfläche. Wenn der Benutzer jedoch auf den Pfeil nach unten klickt, sendet er eine [ \_ BCN-DROPDOWN-Benachrichtigung.](bcn-dropdown.md) Es liegt in der Verantwortung der Anwendung, ein Menü als Reaktion auf die \_ BCN-DROPDOWNLISTE anzuzeigen.

Windows Vista und [Version 6.00](common-control-versions.md) haben auch eine andere Art von Pushschaltfläche eingeführt: den *Befehlslink*. Visuell unterscheidet sich ein Befehlslink stark von einer normalen Pushschaltfläche, verfügt aber über die gleiche Funktionalität. Ein Befehlslink zeigt in der Regel ein Pfeilsymbol, eine Textzeile und zusätzlichen Text in einer kleineren Schriftart an.

## <a name="radio-buttons"></a>Optionsfelder

Ein *Optionsfeld* (auch Optionsschaltfläche genannt) besteht aus einer runden Schaltfläche und einer anwendungsdefiniert Bezeichnung, einem Symbol oder einer Bitmap, die eine Auswahl angibt, die der Benutzer durch Auswählen der Schaltfläche treffen kann. Eine Anwendung verwendet in der Regel Optionsfelder in einem Gruppenfeld, damit der Benutzer eine der verwandten, aber sich gegenseitig ausschließenden Optionen auswählen kann.

Ein Optionsfeld kann einer von zwei Stilen sein: Standard oder automatisch, wie durch die Stilkonstanten [**BS \_ RADIOBUTTON**](button-styles.md) und [**BS \_ AUTORADIOBUTTON**](button-styles.md)definiert. Jeder Stil kann zwei Überprüfungszustände annehmen: aktiviert (ein Punkt in der Schaltfläche) oder gelöscht (kein Punkt in der Schaltfläche).

Wenn der Benutzer einen der Zustände auswählt, erhält das Optionsfeld den Tastaturfokus. Das System sendet dem übergeordneten Fenster der Schaltfläche eine [**WM \_ COMMAND-Meldung**](/windows/desktop/menurc/wm-command) mit dem [BN CLICKED-Benachrichtigungscode. \_](bn-clicked.md) Das übergeordnete Fenster muss diese Meldung nicht verarbeiten, wenn sie von einem automatischen Optionsfeld stammt, da das System automatisch den Überprüfungsstatus für diesen Stil festlegt. Das übergeordnete Fenster sollte die Meldung jedoch verarbeiten, wenn sie von einem nicht automatischen Optionsfeld stammt, da das übergeordnete Fenster für das Festlegen des Überprüfungszustands für diesen Stil zuständig ist. Unabhängig vom Optionsfeldstil fügt das System die Schaltfläche automatisch neu ein, wenn sich ihr Zustand ändert.

Optionsfelder werden in Gruppen angeordnet, und nur eine Schaltfläche in der Gruppe kann jederzeit aktiviert werden. Wenn das [**WS \_ GROUP-Flag**](/windows/desktop/winmsg/window-styles) für ein Optionsfeld festgelegt ist, ist diese Schaltfläche die erste Schaltfläche in einer Gruppe, und alle Schaltflächen, die direkt in der Registerkartenreihenfolge darauf folgen (aber nicht selbst über das **WS \_ GROUP-Flag** verfügen), sind Teil ihrer Gruppe. Wenn keine Optionsfelder das **WS \_ GROUP-Flag** aufweisen, werden alle Optionsfelder im Dialogfeld als einzelne Gruppe behandelt.

Die Anwendung kann mithilfe der [**IsDlgButtonChecked-Funktion**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) überprüfen, ob ein Optionsfeld aktiviert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Verwenden von Schaltflächen](using-buttons.md)
</dt> </dl>

 

 