---
description: In diesem Abschnitt geht es hauptsächlich darum, wie Entwickler von Installationspaketen mithilfe der-Datenbank und der internen Benutzeroberfläche des Installers eine Installations Benutzeroberfläche (User Interface, UI) erstellen.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Verwenden der Benutzeroberfläche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216030"
---
# <a name="using-the-user-interface"></a>Verwenden der Benutzeroberfläche

In diesem Abschnitt geht es hauptsächlich darum, wie Entwickler von Installationspaketen mithilfe der-Datenbank und der internen Benutzeroberfläche des Installers eine Installations Benutzeroberfläche (User Interface, UI) erstellen. Weitere Informationen zum Unterschied zwischen einer internen und externen Benutzeroberfläche finden Sie unter Informationen zur [Benutzeroberfläche](about-the-user-interface.md).

Wenn während der Installation eine Dialogfeld Sequenz oder ein Billboard angezeigt werden soll, muss der Name des Dialog Felds in die Aktionsspalte der entsprechenden Aktions Sequenz Tabelle eingegeben werden. Der Name des Dialog Felds muss in der Tabelle [InstallUISequence](installuisequence-table.md) oder [AdminUISequence](adminuisequence-table.md) angezeigt werden. Dies hängt davon ab, ob die Benutzeroberfläche für die Ausführung unter der Aktion " [Installieren](install-action.md) [", "](advertise-action.md)ankündigen" oder " [Administrator](admin-action.md)" geplant ist.

Obwohl das Installationsprogramm die Erstellung von benutzerdefinierten Dialogfeldern und Plakaten unterstützt, gibt es auch eine Reihe von reservierten Namen für bestimmte Dialogfeld Sequenzen. Da das Installationsprogramm diese Namen beim Ausführen bestimmter Aktionen verwendet, dürfen diese Namen nur mit den Dialogfeldern Typen verwendet werden, für die Sie reserviert sind. Eine Liste mit diesen reservierten Namen und eine Beschreibung der einzelnen Dialogfeld Sequenzen werden in [Dialogfeldern](dialog-boxes.md)angegeben.

Die Eigenschaften der einzelnen Dialogfelder bzw. der einzelnen Elemente in der Benutzeroberfläche müssen jeweils im [Dialog](dialog-table.md) Feld bzw. in [den Tabellen mit](billboard-table.md) den Tabellen definiert werden. Die Formatvorlagen der einzelnen Dialogfelder müssen auch in der Dialogfeld Tabelle angegeben werden, indem das [Style-Bitflag des Dialog Felds](dialog-style-bits.md) festgelegt wird.

Steuerelemente und Text müssen dem Dialogfeld hinzugefügt werden, und diese müssen an [ControlEvents](controlevent-overview.md)gebunden werden, damit der Benutzer mit dem Installationsvorgang interagieren kann. Weitere Informationen zum Hinzufügen von Steuerelementen zu einem Dialogfeld finden Sie unter Hinzufügen von Steuer [Elementen und Text](adding-controls-and-text.md) .

Windows Installer interner Benutzeroberflächen Handler kann Dialogfelder selektiv anzeigen oder ausblenden, um die Ebene der Interaktivität von Endbenutzern während der Installation zu steuern. Diese Ebenen der Endbenutzer-Interaktivität werden als "Full", "Reduced", "Basic" und "None" bezeichnet. Siehe [Benutzeroberflächen Ebenen](user-interface-levels.md). eine vollständige Beschreibung dieser uilevels.

Es gibt zwei Methoden, um die Benutzeroberflächen Ebene festzulegen. Die Benutzeroberflächen Ebene kann Programm gesteuert mit einem [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)-Befehl festgelegt werden, und der erste Parameter von **MsiSetInternalUI** gibt die Benutzeroberflächen Ebene an. Paket Entwickler können die Benutzeroberflächen Ebene auch mithilfe der [Befehlszeilenoption](command-line-options.md) "/q" festlegen.

Das Verhalten der einzelnen Benutzeroberflächen Ebenen wird durch die Erstellung der MSI-Datei durch den Paket Entwickler bestimmt. Der Autor einer internen Benutzeroberfläche bietet Flexibilität in der Art und Weise, wie sich diese Ebenen für ein Paket Verhalten. Die Verfügbarkeit dieser Ebenen hängt von der Erstellung des Installationspakets ab. Der Autor muss jedes Dialogfeld und Steuerelement in der Benutzeroberfläche in den Dialog-und Steuerelement Tabellen angeben.

-   Eine vollständige Benutzeroberfläche zeigt in der Regel das [Verhalten des Benutzeroberflächen-Assistenten](user-interface-wizard-behavior.md)an, z. b. jedes Dialogfeld in einer Sequenz, das **>>** eine Schaltfläche Diese Art von Benutzeroberfläche ist vielen Benutzern vertraut und ist die am häufigsten von einem Autor zu erstellende Art von Benutzeroberfläche. Das Installationsprogramm zeigt eine logische Sequenz von Dialogfeldern an und fordert den Benutzer auf, mit Steuerelementen zu interagieren, die sich in jedem Dialogfeld befinden.
-   Eine reduzierte Benutzeroberfläche unterdrückt in der Regel die Anzeige des Assistenten Verhaltens.
-   Eine grundlegende Benutzeroberfläche zeigt in der Regel nur Statusmeldungen für den Benutzer an.
-   Die Benutzeroberflächen Ebene "None" bedeutet eine unbeaufsichtigte Installation.

Windows Installer stellt einen eindeutigen Statusanzeige Indikator im [ProgressBar-Steuer](progressbar-control.md) Element bereit, das dem Benutzer eine Schätzung der Gesamtzeit anzeigt, die bis zum Abschluss der Installation verbleiben. Weitere Informationen zur Statusanzeige finden Sie unter [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements.

Benutzeroberflächen Autoren sollten die Barrierefreiheit Ihrer Anwendung oder Ihres Produkts für alle Benutzer vereinfachen. Weitere Informationen zu Active Accessibility und Windows Installer finden Sie unter [Barrierefreiheit](accessibility.md).

Weitere Informationen zum Erstellen einer Benutzeroberfläche finden Sie unter [Hinzufügen von Steuerelementen und Text](adding-controls-and-text.md), [Erstellen eines ProgressBar-Steuer](authoring-a-progressbar-control.md)Elements, Erstellen von Datenträger-Eingabe Aufforderungs [Meldungen](authoring-disk-prompt-messages.md), [Erstellen einer bedingten "Bitte warten..." ](authoring-a-conditional-please-wait-------message-box.md)Meldungs Feld und [Vorschau der Benutzeroberfläche](previewing-the-user-interface.md). Weitere Informationen zum Erstellen von Plakatwänden finden Sie [unter Anzeigen von Plakaten in einem](displaying-billboards-on-a-modeless-dialog.md) nicht modalem Dialog Feld

Ab Windows Installer 4,5 kann eine benutzerdefinierte Benutzeroberfläche in das Windows Installer Paket eingebettet werden. Ein Beispiel für eine eingebettete benutzerdefinierte Benutzeroberfläche finden [Sie unter Verwenden einer eingebetteten](using-an-embedded-ui.md)Benutzeroberfläche.

 

 



