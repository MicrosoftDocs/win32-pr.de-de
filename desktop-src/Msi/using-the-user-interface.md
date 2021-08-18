---
description: In diesem Abschnitt geht es in erster Linie darum, wie Entwickler von Installationspaketen eine Benutzeroberfläche für die Installation erstellen, indem sie die Datenbank des Installationsprogramms und die interne Benutzeroberfläche verwenden.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Verwenden der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a2303ddcdf589b69abb819ab1cdee9060f4918c1bd238e161677da7987300bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995990"
---
# <a name="using-the-user-interface"></a>Verwenden der Benutzeroberfläche

In diesem Abschnitt geht es in erster Linie darum, wie Entwickler von Installationspaketen eine Benutzeroberfläche für die Installation erstellen, indem sie die Datenbank des Installationsprogramms und die interne Benutzeroberfläche verwenden. Weitere Informationen zum Unterschied zwischen einer internen und einer externen Benutzeroberfläche finden Sie unter [Informationen zum Benutzeroberfläche](about-the-user-interface.md).

Um während der Installation eine Dialogfeldsequenz oder ein -Ereignis anzuzeigen, muss der Name des Dialogfelds in die Spalte Aktion der entsprechenden Aktionssequenztabelle eingegeben werden. Der Name des Dialogfelds muss in der Tabelle [InstallUISequence](installuisequence-table.md) oder [AdminUISequence](adminuisequence-table.md) angezeigt werden, je nachdem, ob die Ausführung der Benutzeroberfläche unter [der](install-action.md)Install-, [ADVERTISE-](advertise-action.md)oder [ADMIN-Aktion](admin-action.md)geplant ist.

Obwohl das Installationsprogramm die Erstellung von benutzerdefinierten Dialogfeldern und -ausschnitten unterstützt, gibt es auch eine Reihe von reservierten Namen für bestimmte Dialogfeldsequenzen. Da das Installationsprogramm diese Namen beim Ausführen bestimmter Aktionen verwendet, dürfen diese Namen nur mit den Typen von Dialogfeldern verwendet werden, für die sie reserviert sind. Eine Liste dieser reservierten Namen und eine Beschreibung der einzelnen speziellen Dialogfeldsequenzen werden in [Dialogfeldern angegeben.](dialog-boxes.md)

Die Eigenschaften der einzelnen Dialogfelder oder Tabellen auf der Benutzeroberfläche müssen in den Tabellen [Dialog](dialog-table.md) bzw. [BillBoard](billboard-table.md) angegeben werden. Der Stil jedes Dialogfelds muss auch in der Tabelle Dialog angegeben werden, indem das [Formatbitflag des Dialogs](dialog-style-bits.md) festgelegt wird.

Steuerelemente und Text müssen dem Dialogfeld hinzugefügt werden, und diese müssen an [ControlEvents](controlevent-overview.md)gebunden sein, damit der Benutzer mit dem Installationsprozess interagieren kann. Weitere Informationen zum Hinzufügen von Steuerelementen zu einem Dialogfeld finden Sie unter [Hinzufügen von Steuerelementen und Text.](adding-controls-and-text.md)

Windows Der interne Benutzeroberflächenhandler des Installationsprogramms kann Dialogfelder selektiv anzeigen oder ausblenden, um die Interaktivitätsebene des Endbenutzers während der Installation zu steuern. Diese Ebenen der Interaktivität von Endbenutzern werden als vollständig, reduziert, einfach und keine bezeichnet. Weitere Informationen finden Sie [unter Benutzeroberfläche Ebenen.](user-interface-levels.md) eine vollständige Beschreibung dieser UIlevels.

Es gibt zwei Methoden zum Festlegen der Benutzeroberflächenebene. Die Benutzeroberflächenebene kann programmgesteuert mit einem Aufruf von [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)festgelegt werden, und der erste Parameter von **MsiSetInternalUI** gibt die Benutzeroberflächenebene an. Paketentwickler können die Benutzeroberflächenebene auch mithilfe der [Befehlszeilenoption](command-line-options.md) "/q" festlegen.

Das Verhalten der einzelnen Benutzeroberflächenebenen wird durch die Erstellung der .msi-Datei durch den Paketentwickler bestimmt. Der Autor einer internen Benutzeroberfläche verfügt über Flexibilität beim Verhalten dieser Ebenen für ein Paket. Die Verfügbarkeit dieser Ebenen hängt von der Erstellung des Installationspakets ab. Der Autor muss jedes Dialogfeld und Steuerelement auf der Benutzeroberfläche in den Tabellen Dialog und Steuerelement angeben.

-   Eine vollständige Benutzeroberfläche weist in der Regel das Verhalten des Assistenten für die [Benutzeroberfläche](user-interface-wizard-behavior.md)auf, z. B. jedes Dialogfeld in einer Sequenz, die die Schaltfläche **Weiter>>** enthält. Diese Form der Benutzeroberfläche ist vielen Benutzern vertraut und ist der gängigste Benutzeroberflächentyp, den ein Autor erstellen kann. Das Installationsprogramm zeigt eine logische Sequenz von Dialogfeldern an und fordert den Benutzer auf, mit Steuerelementen in den einzelnen Dialogfeldern zu interagieren.
-   Eine reduzierte Benutzeroberfläche unterdrückt in der Regel die Anzeige des Assistentenverhaltens.
-   Eine einfache Benutzeroberfläche zeigt dem Benutzer in der Regel nur Statusmeldungen an.
-   Die Benutzeroberflächenebene "None" bedeutet eine unbeaufsichtigt installierte Installation.

Windows Das Installationsprogramm stellt eine eindeutige Statusanzeige im [ProgressBar-Steuerelement](progressbar-control.md) bereit, die dem Benutzer eine Schätzung der gesamt verbleibenden Zeit bis zum Abschluss der Installation anzeigt. Weitere Informationen zur Statusanzeige finden Sie unter [Erstellen eines ProgressBar-Steuerelements.](authoring-a-progressbar-control.md)

Benutzeroberflächenautoren sollten allen Benutzern den Zugriff auf ihre Anwendung oder ihr Produkt erleichtern. Weitere Informationen zu Active Accessibility und Windows Installer finden Sie unter [Barrierefreiheit.](accessibility.md)

Weitere Informationen zum Erstellen einer Benutzeroberfläche finden Sie unter [Hinzufügen von Steuerelementen und Text,](adding-controls-and-text.md) [Erstellen eines ProgressBar-Steuerelements,](authoring-a-progressbar-control.md)Erstellen von [Datenträgereingabeaufforderungsmeldungen,](authoring-disk-prompt-messages.md) [Erstellen eines bedingten "Please Wait . . "." Meldungsfeld](authoring-a-conditional-please-wait-------message-box.md)und [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md). Weitere Informationen zu Autorenautoren finden Sie unter [Anzeigen von Schriftflächen in einem moduslosen Dialogfeld.](displaying-billboards-on-a-modeless-dialog.md)

Ab Windows Installer 4.5 kann eine benutzerdefinierte Benutzeroberfläche in das paket Windows Installer eingebettet werden. Ein Beispiel für eine eingebettete benutzerdefinierte Benutzeroberfläche finden Sie unter [Verwenden einer eingebetteten Benutzeroberfläche.](using-an-embedded-ui.md)

 

 



