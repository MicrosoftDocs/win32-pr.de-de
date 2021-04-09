---
title: Schaltflächentypen
description: Es gibt mehrere Arten von Schaltflächen und mindestens einen Schaltflächen Stil, um zwischen den Schaltflächen desselben Typs zu unterscheiden.
ms.assetid: bfc8b88b-0da2-46f6-b8c2-72f693ee1e7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 682cc39ed2f88ce88f499757fbc4f902bfdceeea
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730600"
---
# <a name="button-types"></a>Schaltflächentypen

Es gibt mehrere Arten von Schaltflächen und mindestens einen Schaltflächen Stil, um zwischen den Schaltflächen desselben Typs zu unterscheiden.

In diesem Dokument werden die folgenden Themen behandelt.

-   [Schaltflächen Typen und-Stile](#button-types-and-styles)
-   [Kontrollkästchen](#check-boxes)
-   [Gruppenfelder](#group-boxes)
-   [Pushschaltflächen](#push-buttons)
-   [Options Felder](#radio-buttons)
-   [Zugehörige Themen](#related-topics)

## <a name="button-types-and-styles"></a>Schaltflächen Typen und-Stile

Eine Schaltfläche gehört zu einem Typ und kann über zusätzliche Stile verfügen, die sich auf die Darstellung und das Verhalten auswirken. Eine Tabelle mit Schaltflächen Formaten finden Sie unter [Button Styles](button-styles.md).

Der folgende Screenshot zeigt die verschiedenen Typen von Schaltflächen.

![Screenshot eines Dialog Felds, in dem Beispiele für acht Arten von Schaltflächen angezeigt werden](images/buttontypes.png)

Der Screenshot zeigt, wie Schaltflächen in Windows Vista angezeigt werden können. Die Darstellung variiert in verschiedenen Versionen des Betriebssystems und entsprechend dem vom Benutzer festgelegten Design.

Beachten Sie die folgenden Punkte zur Abbildung:

-   Das Kontrollkästchen drei Status wird im unbestimmten Zustand angezeigt. Wenn dieses Kontrollkästchen aktiviert oder deaktiviert ist, sieht es wie ein normales Kontrollkästchen aus.
-   Die Schaltfläche für großen Push wurde Programm gesteuert auf den Push-Zustand festgelegt (durch Senden der [**BM- \_ SetState**](bm-setstate.md) -Nachricht), sodass Sie Ihre Darstellung beibehält, auch wenn Sie nicht darauf geklickt wird.
-   Im visuellen Stil wird der Hintergrund der standardmäßigen Push-Schaltfläche (oder einer anderen Schaltfläche mit dem Eingabefokus) zwischen Blau und grau angezeigt.

## <a name="check-boxes"></a>Kontrollkästchen

Ein *Kontrollkästchen* besteht aus einem quadratischen Feld und einer Anwendungs definierten Bezeichnung, einem Symbol oder einer Bitmap, die eine Auswahl angibt, die der Benutzer durch Auswählen der Schaltfläche treffen kann. Anwendungen zeigen in der Regel Kontrollkästchen an, damit der Benutzer eine oder mehrere Optionen auswählen kann, die sich nicht gegenseitig ausschließen.

Ein Kontrollkästchen kann einen von vier Formaten aufweisen: Standard, automatisch, drei-Status und automatisch drei-Status-, wie durch das [**\_ Kontrollkästchen**](button-styles.md)"Konstanten", " [**\_ bautocheckbox**](button-styles.md)", " [**SB \_ 3STATE**](button-styles.md)" bzw. "SB [**\_ AUTO3STATE**](button-styles.md)" definiert. Jeder Stil kann zwei Kontroll Zustände annehmen: aktiviert (ein Häkchen im Feld) oder gelöscht (kein Häkchen). Außerdem kann ein Kontrollkästchen mit drei Zuständen einen unbestimmten Zustand annehmen (ein schattiertes Kontrollkästchen innerhalb des Kontrollkästchens). Dies kann darauf hinweisen, dass der Benutzer keine Auswahl getroffen hat. Wenn Sie wiederholt auf ein Standard-oder ein automatisches Kontrollkästchen klicken, wird das Kontrollkästchen von aktiviert in deaktiviert und wieder zurück gewechselt. Durch wiederholtes Klicken auf ein Kontrollkästchen mit drei Zuständen wird die Option von "aktiviert" in "unbestimmt" deaktiviert und dann wiederholt.

Wenn der Benutzer auf ein Kontrollkästchen (eines beliebigen Stils) klickt, empfängt das Kontrollkästchen den Tastaturfokus. Das System sendet das übergeordnete Fenster des Kontrollkästchens eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, die den auf der Milliarde-Wert [ \_ angeklickten](bn-clicked.md) Das übergeordnete Fenster muss diese Nachricht nicht verarbeiten, wenn Sie aus einem automatischen Kontrollkästchen oder einem automatischen drei-Status-Kontrollkästchen stammt, da das System automatisch den Integritäts Status für diese Stile festlegt. Das übergeordnete Fenster muss die Nachricht jedoch verarbeiten, wenn Sie aus einem nicht automatischen Kontrollkästchen oder einem Kontrollkästchen mit drei Zuständen stammt, da das übergeordnete Fenster für das Festlegen des Prüf Zustands für diese Stile zuständig ist. Unabhängig von der Art des Kontrollkästchens zeichnet das System das Kontrollkästchen automatisch, sobald der Status geändert wird.

Die Anwendung kann den Status eines Kontrollkästchens mithilfe der [**isdlgbuttoncheckfunktion**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) überprüfen.

## <a name="group-boxes"></a>Gruppenfelder

Ein *Gruppenfeld* ist ein Rechteck, das eine Reihe von Steuerelementen umgibt, z. b. Kontrollkästchen oder Options Felder, mit einer von der Anwendung definierten Text Bezeichnung in der oberen linken Ecke. Der einzige Zweck eines Gruppen Felds besteht darin, Steuerelemente zu organisieren, die durch einen gemeinsamen Zweck (in der Regel durch die Bezeichnung gekennzeichnet) verknüpft sind. Das Gruppenfeld hat nur einen Stil, der durch die Gruppe Constant [**SB \_ GroupBox**](button-styles.md)definiert wird. Da ein Gruppenfeld nicht ausgewählt werden kann, hat es keinen Prüf Zustand, keinen Fokus Zustand oder keinen pushzustand.

## <a name="push-buttons"></a>Pushschaltflächen

Eine *pushschaltfläche* ist ein Rechteck, das eine von der Anwendung definierte Text Bezeichnung, ein Symbol oder eine Bitmap enthält, die angibt, welche Aktionen die Schaltfläche durchführt, wenn der Benutzer Sie auswählt.

Eine Schaltfläche "Push" kann eines von zwei Stilen ("Standard" oder "Standard") sein, wie von den Konstanten [**SB " \_ PUSHBUTTON**](button-styles.md) " und " [**SB \_ DEFPUSHBUTTON**](button-styles.md)" Eine Standard-Push-Schaltfläche wird normalerweise verwendet, um einen Vorgang zu starten. Er empfängt den Tastaturfokus, wenn der Benutzer darauf klickt. Eine Standard-Push-Schaltfläche wird normalerweise verwendet, um die gängigste oder Standardauswahl anzugeben, z. b. das Schließen des Dialog Felds. Es handelt sich um eine Schaltfläche, die der Benutzer auswählen kann, indem er einfach die EINGABETASTE drückt, wenn im Dialogfeld keine andere Schaltfläche für den Eingabefokus steht.

Wenn der Benutzer auf die Schaltfläche "Push" klickt, wird der Tastaturfokus empfangen. Das System sendet das übergeordnete Fenster der Schaltfläche mit einer [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, die den auf die Milliarde-Code [ \_ geklickt](bn-clicked.md) hat.

Die unter *teilte Schaltfläche* ist eine besondere Art von Push-Schaltfläche, die in Windows Vista und [Version 6,00](common-control-versions.md)eingeführt wurde. Eine unterteilte Schaltfläche ist in zwei Teile unterteilt. Der Hauptteil funktioniert wie eine reguläre oder standardmäßige pushschaltfläche. Der zweite Teil weist einen Pfeil nach unten auf. In der Regel wird ein Menü angezeigt, wenn auf den Pfeil geklickt wird.

Eine unterteilte Schaltfläche verfügt über den [**\_ SplitButton**](button-styles.md) -Stil von ' ' oder ' ', wenn es sich um die Standard [**Schaltfläche in \_**](button-styles.md) einem Dialogfeld handelt. Sie können die Darstellung der Schaltfläche ändern, indem Sie die [**BCM- \_ setsplitinfo**](bcm-setsplitinfo.md) -Nachricht oder die entsprechende [**Schaltfläche \_ setsplitinfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) -Makro verwenden.

Wenn der Benutzer auf den Hauptteil der Trenn Schaltfläche klickt, sendet er eine auf eine [Milliarde \_ angeklickte](bn-clicked.md) Benachrichtigung, wie eine normale pushtaste. Wenn der Benutzer jedoch auf den Pfeil nach unten klickt, sendet er eine [BCN- \_ Dropdown](bcn-dropdown.md) Benachrichtigung. Die Anwendung ist dafür verantwortlich, ein Menü als Antwort auf die BCN- \_ Dropdown Liste anzuzeigen.

Windows Vista und [Version 6,00](common-control-versions.md) haben auch eine andere Art von Push-Schaltfläche eingeführt, den *Befehls Link*. Ein Befehls Link unterscheidet sich visuell von der normalen Schaltfläche "Push", aber er verfügt über die gleiche Funktionalität. Ein Befehls Link zeigt in der Regel ein Pfeilsymbol, eine Textzeile und zusätzlichen Text in einer kleineren Schriftart an.

## <a name="radio-buttons"></a>Options Felder

Ein Options *Feld (auch* Options Schaltfläche genannt) besteht aus einer runden Schaltfläche und einer Anwendungs definierten Bezeichnung, einem Anwendungs definierten Symbol oder einer Bitmap, die eine Auswahl angibt, die der Benutzer durch Auswählen der Schaltfläche treffen kann. Eine Anwendung verwendet in der Regel Options Felder in einem Gruppenfeld, um dem Benutzer zu ermöglichen, eine Gruppe verwandter, aber sich gegenseitig ausschließender Optionen auszuwählen.

Bei einem Optionsfeld kann es sich um einen von zwei Stilen handeln: Standard oder automatisch, wie von den Format Konstanten " [**\_ RadioButton**](button-styles.md) " und " [**SB \_ AUTORADIOBUTTON**](button-styles.md)" definiert. Jeder Stil kann zwei Kontroll Zustände annehmen: aktiviert (ein Punkt in der Schaltfläche) oder gelöscht (kein Punkt in der Schaltfläche).

Wenn der Benutzer einen der beiden Zustände auswählt, erhält das Optionsfeld den Tastaturfokus. Das System sendet das übergeordnete Fenster der Schaltfläche eine [**WM- \_ Befehls**](/windows/desktop/menurc/wm-command) Nachricht, die den auf die Milliarde-Code [ \_ geklickt](bn-clicked.md) hat. Das übergeordnete Fenster muss diese Nachricht nicht verarbeiten, wenn Sie von einem automatischen Optionsfeld stammt, da das System automatisch den Integritäts Status für diesen Stil festlegt. Das übergeordnete Fenster sollte die Nachricht jedoch verarbeiten, wenn Sie von einem nicht automatischen Optionsfeld stammt, da das übergeordnete Fenster für das Festlegen des Prüf Zustands für diesen Stil zuständig ist. Unabhängig vom Optionsfeld Stil zeichnet das System die Schaltfläche automatisch, wenn sich der Zustand ändert.

Options Felder werden in Gruppen angeordnet, und es kann immer nur eine Schaltfläche in der Gruppe aktiviert werden. Wenn das kennflag der [**WS- \_ Gruppe**](/windows/desktop/winmsg/window-styles) für ein Optionsfeld festgelegt ist, ist diese Schaltfläche die erste Schaltfläche in einer Gruppe, und alle Schaltflächen, die auf diese Schaltfläche folgen, werden direkt in der Aktivier Reihenfolge angezeigt (aber nicht selbst über das **WS- \_ gruppenflag** ). Wenn keine Options Felder das **WS- \_ gruppenflag** aufweisen, werden alle Options Felder im Dialogfeld als eine einzelne Gruppe behandelt.

Die Anwendung kann mithilfe der [**isdlgbuttoncheckfunktion**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) ermitteln, ob ein Optionsfeld aktiviert ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Schaltflächenstile](button-styles.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Verwenden von Schaltflächen](using-buttons.md)
</dt> </dl>

 

 