---
title: Menüs (Entwurfsgrundlagen)
description: Menüs sind hierarchische Listen von Befehlen oder Optionen, die Benutzern im aktuellen Kontext zur Verfügung stehen.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 7d5c52e56c88f4066e8f1dc068ac89070c7d4974
ms.sourcegitcommit: 8ebcf6cd36f67f8bcf78e76ae8923d65b8995c8a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/05/2021
ms.locfileid: "111524374"
---
# <a name="menus-design-basics"></a>Menüs (Entwurfsgrundlagen)

> [!NOTE]
> Dieser Entwurfsleitfaden wurde für Windows 7 erstellt und für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt immer noch im Prinzip, aber die Präsentation und die Beispiele spiegeln nicht unsere [aktuellen Entwurfsleitfäden](/windows/uwp/design/)wider.

Menüs sind hierarchische Listen von Befehlen oder Optionen, die Benutzern im aktuellen Kontext zur Verfügung stehen.

Dropdownmenüs sind Menüs, die bei Bedarf per Mausklick oder mit dem Mauszeiger darauf angezeigt werden. Sie werden normalerweise in der Ansicht ausgeblendet und sind daher ein effizientes Mittel, um Bildschirmfläche zu sparen. Ein Untermenü oder kaskadierendes Menü ist ein sekundäres Menü, das bei Bedarf innerhalb eines Menüs angezeigt wird. Sie werden durch einen Pfeil am Ende der Untermenübezeichnung angezeigt. Ein Menüelement ist ein einzelner Befehl oder eine Option innerhalb eines Menüs.

Menüs werden häufig über eine Menüleiste angezeigt, bei der es sich um eine Liste mit beschrifteten Menükategorien handelt, die sich in der Regel am oberen Rand eines Fensters befinden. Im Gegensatz dazu fällt ein Kontextmenü aus, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, der ein Kontextmenü unterstützt.

![Screenshot der Menüleiste mit Menü und Untermenü ](images/cmd-menus-image1.png)

Eine typische Menüleiste, die ein Dropdownmenü und ein Untermenü anzeigt.

> [!Note]  
> Richtlinien für [Befehlsschaltflächen,](ctrl-command-buttons.md) [Symbolleisten](cmd-toolbars.md)und [Tastatur](inter-keyboard.md) werden in separaten Artikeln dargestellt.

 

## <a name="usage-patterns"></a>Verwendungsmuster

Menüs weisen mehrere Verwendungsmuster auf:



| Verwendung                                                                                                                                                |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Menüleisten**<br/> Eine Menüleiste zeigt Befehle und Optionen in Dropdownmenüs an. <br/>                                               | Menüleisten sind sehr häufig und leicht zu finden sowie eine effiziente Nutzung des Speicherplatzes. <br/> ![Screenshot der Menüleiste mit Dropdownmenü ](images/cmd-menus-image2.png)<br/> Eine Menüleiste aus Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Symbolleistenmenüs**<br/> eine Menüleiste, die als Symbolleiste implementiert ist. <br/>                                                                   | Symbolleistenmenüs sind Symbolleisten, die in erster Linie aus Befehlen in [Menüschaltflächen](ctrl-command-buttons.md) und geteilten Schaltflächen bestehen, wobei ggf. nur wenige direkte Befehle vorhanden sind. <br/> ![Screenshot des Symbolleistenmenüs mit Dropdownmenü ](images/cmd-menus-image3.png)<br/> Ein Symbolleistenmenü in Windows Fotogalerie.<br/> Richtlinien zu diesem Muster finden Sie unter [Symbolleisten](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Registerkartenmenüs**<br/> Schaltflächen in Registerkarten, die einen kleinen Satz von Befehlen und Optionen im Zusammenhang mit einer Registerkarte in einem Dropdownmenü anzeigen. <br/> | Registerkarten mit Menüs sehen wie gewöhnliche Registerkarten aus, mit dem Unterschied, dass ihr unterer Teil eine Schaltfläche mit Dropdownpfeil enthält. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdownmenü angezeigt, anstatt die Registerkarte auszuwählen. <br/> ![Screenshot des Registerkartenmenüs mit Dropdownmenü ](images/cmd-menus-image4.png)<br/> Registerkartenmenüs werden in Windows Media Player verwendet.<br/>                                                                                                                                                                                                                                                                                           |
| **Menüschaltflächen**<br/> Befehlsschaltflächen, die einen kleinen Satz verwandter Befehle in einem Dropdownmenü anzeigen. <br/>                       | [Menüschaltflächen](ctrl-command-buttons.md) sehen wie gewöhnliche Befehlsschaltflächen aus, außer dass sie über einen Dropdownpfeil verfügen. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdownmenü angezeigt, anstatt einen Befehl auszuführen.<br/> [Geteilte Schaltflächen](ctrl-command-buttons.md) ähneln Menüschaltflächen, außer dass es sich um Variationen eines Befehls handelt, und wenn Sie auf den linken Teil der Schaltfläche klicken, wird die Aktion direkt auf der Bezeichnung ausgeführt.<br/> ![Screenshot der Menüschaltfläche mit Dropdownbefehlen ](images/cmd-menus-image5.png)<br/> Eine Menüschaltfläche mit einem kleinen Satz verwandter Befehle.<br/> |
| **Kontextmenüs**<br/> Dropdownmenüs, die einen kleinen Satz von Befehlen und Optionen im Zusammenhang mit dem aktuellen Kontext anzeigen. <br/>       | Kontextmenüs, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, der ein Kontextmenü unterstützt. <br/> ![Screenshot des Kontextmenüs mit Befehlen ](images/cmd-menus-image6.png)<br/> ein Kontextmenü aus dem Windows-Explorer.<br/> Wenn Kontextmenüs die beste Menüauswahl sind, Sie aber eine für alle Benutzer geeignete Lösung benötigen, können Sie eine Dropdownpfeilschaltfläche im Menü verwenden. <br/> ![Screenshot des Fotos mit der Dropdownmenüschaltfläche ](images/cmd-menus-image7.png)<br/> Ein Kontextmenü, das mit einer Dropdownschaltfläche des Menüs sichtbar gemacht wird.<br/>                                                   |
| **Menüs im Aufgabenbereich**<br/> eine kleine Gruppe von Befehlen im Zusammenhang mit dem ausgewählten Objekt oder Programmmodus. <br/>                              | Im Gegensatz zu Kontextmenüs werden sie nicht bei Bedarf, sondern automatisch in einem Fensterbereich angezeigt. <br/> ![Screenshot des Fotos mit Menü "Aufgabenbereich" auf der rechten Seite ](images/cmd-menus-image8.png)<br/> Ein Aufgabenbereichsmenü im Windows Fotogalerie Viewer.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

### <a name="menu-bars"></a>Menüleisten

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es viele Menüelemente?
-   Gibt es viele Menükategorien?
-   Gelten die meisten Menüelemente für das gesamte Programm und das primäre Fenster?
-   Muss das Menü für alle Benutzer funktionieren?

Falls ja, sollten Sie eine Menüleiste verwenden.

### <a name="toolbar-menus"></a>Symbolleistenmenüs

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Verfügt das Fenster über eine Symbolleiste?
-   Gibt es nur wenige Menükategorien?
-   Muss das Menü für alle Benutzer funktionieren?

Falls ja, sollten Sie ein Symbolleistenmenü anstelle von oder zusätzlich zu einer Menüleiste verwenden.

### <a name="tab-menus"></a>Registerkartenmenüs

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Verfügt das Fenster über Registerkarten, auf denen jede Registerkarte für einen dedizierten Satz von Aufgaben verwendet wird (im Gegensatz zur Verwendung von Registerkarten zum Anzeigen verschiedener Ansichten)?
-   Gibt es eine Menükategorie, die für jede Registerkarte gilt?
-   Gibt es viele Befehle und Optionen, aber nur einen kleinen Satz für jede Registerkarte?

Falls ja, sollten Sie ein Registerkartenmenü anstelle einer Menüleiste verwenden.

### <a name="context-menu"></a>Kontextmenü

Gehen Sie wie folgt vor:

-   Gibt es einen kleinen Satz kontextabhängiger Befehle und Optionen, die für das ausgewählte Objekt oder den ausgewählten Fensterbereich gelten?
-   Sind diese Menüelemente redundant?
-   Sind die Zielbenutzer mit Kontextmenüs vertraut?

Falls ja, sollten Sie Kontextmenüs für die Objekte und Fensterbereiche bereitstellen, die sie benötigen.

Bei browserbasierten Programmen sind Menüs im Aufgabenbereich eine häufigere Lösung für kontextbezogene Befehle. Derzeit erwarten Benutzer, dass Kontextmenüs in browserbasierten Programmen generisch und nicht hilfreich sind.

### <a name="task-pane-menu"></a>Menü "Aufgabenbereich"

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es einen kleinen Satz kontextabhängiger Befehle und Optionen, die für das ausgewählte Objekt oder den ausgewählten Programmmodus gelten?
-   Gibt es einige Menükategorien?
-   Muss das Menü für alle Benutzer funktionieren?

Falls ja, sollten Sie ein Aufgabenbereichsmenü anstelle eines Kontextmenüs verwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Menüs, die eine gute Benutzererfahrung fördern:

-   Verwenden Sie eine Befehlspräsentation, die ihrem Programmtyp, Den Fenstertypen, der Befehlsverwendung und den Zielbenutzern entspricht.
-   Sind gut organisiert und verwenden bei Bedarf die Standardmenüorganisation.
-   Verwenden Sie Menüleisten, Symbolleisten und Kontextmenüs effektiv.
-   Verwenden Sie Symbole effektiv.
-   Verwenden Sie Zugriffsschlüssel und Tastenkombinationen effektiv.

**Wenn Sie nur eine Sache tun...**

Wählen Sie eine Befehlspräsentation aus, die Ihrem Programmtyp, Den Fenstertypen, der Befehlsverwendung und den Zielbenutzern entspricht.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Alle Menümuster außer Menüleisten benötigen einen Dropdownpfeil, um das Vorhandensein eines Pull-Down-Menüs anzuzeigen.** Das Vorhandensein von Menüs ist in einer Menüleiste selbstverständlich, aber nicht in den anderen Mustern.
-   **Ändern Sie menüelementnamen nicht dynamisch.** Dies ist verwirrend und unerwartet. Ändern Sie z. B. bei auswahl keine Option für den Hochformatmodus in Querformat. Verwenden Sie für Modi stattdessen [Aufzählungszeichen und Häkchen.](#bullets-and-checkmarks)
    -   **Ausnahme:** Sie können Menüelementnamen, die auf Objektnamen basieren, dynamisch ändern. Beispielsweise können Listen mit zuletzt verwendeten Dateien oder Fensternamen dynamisch sein.

### <a name="menu-bars"></a>Menüleisten

-   **Erwägen Sie, Menüleisten mit drei oder weniger Menükategorien zu entfernen.** Wenn nur wenige Befehle vorhanden sind, bevorzugen Sie leichtere Alternativen wie Symbolleistenmenüs oder direktere Alternativen wie Befehlsschaltflächen und Links.
-   **Sie haben nicht mehr als 10 Menükategorien.** Zu viele Menükategorien sind überwältigend und erschweren die Verwendung der Menüleiste.
-   **Erwägen Sie das Ausblenden der Menüleiste,** wenn die Symbolleiste oder direkte Befehle fast alle Befehle bereitstellen, die von den meisten Benutzern benötigt werden. Benutzern das Ein- oder Ausblenden mit der Option Menüleisten-Häkchen in einem Symbolleistenmenü gestatten.

![Screenshot der Optionsliste mit ausgewählter Menüleiste ](images/cmd-menus-image9.png)

In diesem Beispiel stellt Windows Internet Explorer eine Menüleistenoption bereit.

Weitere Informationen finden Sie unter [Ausblenden von Menüleisten.](#hiding-menu-bars)

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend zusammen mit Menüleisten, da sich beide auf ihre Stärken konzentrieren können, ohne kompromittiert zu werden.

-   Blenden Sie die Menüleiste standardmäßig aus, wenn das Symbolleistendesign eine Menüleiste redundant macht.
-   Blenden Sie die Menüleiste aus, anstatt sie vollständig zu entfernen, da Für Tastaturbenutzer besser auf Menüleisten zugegriffen werden kann.
-   Um die Menüleiste wiederherzustellen, geben Sie eine Menüleisten-Häkchenoption in der Menükategorie Ansicht (für primäre Symbolleisten) oder Extras (für sekundäre Symbolleisten) an. Weitere Informationen finden Sie unter [Standardmenü und Unterteilte Schaltflächen.](cmd-toolbars.md)

### <a name="menu-categories"></a>Menükategorien

-   **Wählen Sie einzelne Wortnamen für Menükategorien aus.** Die Verwendung mehrerer Wörter macht die Trennung zwischen Kategorien verwirrend.
-   **Verwenden Sie für Programme, die Dokumente erstellen oder anzeigen, die Standardmenükategorien** wie Datei, Bearbeiten, Ansicht, Tools und Hilfe. Dies macht allgemeine Menüelemente vorhersagbar und einfacher zu finden.
-   **Für andere Arten von Programmen sollten Sie ihre Befehle und Optionen in nützlicheren, natürlicheren Kategorien organisieren,** die auf dem Zweck Ihres Programms und der Art und Weise basieren, wie Benutzer über ihre Aufgaben und Ziele denken. Denken Sie nicht daran, die Standardmenüorganisation zu verwenden, wenn sie nicht für Ihr Programm geeignet ist.
-   **Wenn Sie nicht standardmäßige Menükategorien verwenden möchten, müssen Sie gute Kategorienamen auswählen.** Weitere Informationen finden Sie im Abschnitt [Bezeichnungen.](#labels)
-   **Bevorzugen Sie aufgabenorientierte Menükategorien gegenüber generischen Kategorien.** Aufgabenorientierte Kategorien erleichtern die Suche nach Menüelementen.

![Screenshot der Menüleiste mit "Rip", "Burn" und "Sync" ](images/cmd-menus-image10.png)

In diesem Beispiel verwendet Windows Media Player aufgabenorientierte Menükategorien.

-   **Vermeiden Sie Menükategorien mit nur ein oder zwei Menüelementen.** Wenn dies sinnvoll ist, konsolidieren Sie sie mit anderen Menükategorien, z. B. mithilfe eines Untermenüs.
-   **Erwägen Sie, das gleiche Menüelement nur dann in mehrere Kategorien zu unterteilen, wenn:**
    -   Das Menüelement gehört logisch zu mehreren Menükategorien.
    -   Sie verfügen über Daten, die zeigen, dass Benutzer Probleme haben, das Element in einer einzelnen Menükategorie zu finden.
    -   Es gibt nur ein oder zwei schwer zu findende Menüelemente in mehreren Kategorien.
-   **Legen Sie nicht verschiedene Menüelemente, die den gleichen Namen verwenden, in mehrere Kategorien ein.** Beispielsweise verfügen Sie nicht über unterschiedliche Menüelemente im Menü Optionen in mehreren Kategorien.
    -   **Ausnahme:** Das Registerkartenmenümuster kann in jedem Registerkartenmenü unterschiedliche Optionen und Hilfemenüelemente enthalten.

![Screenshot von Registerkartenmenüs mit wiederholten Menüelementen ](images/cmd-menus-image11.png)

In diesem Beispiel enthält Windows Media Player die Menüelemente Optionen und Hilfe in jedem Registerkartenmenü.

### <a name="menu-item-organization-and-order"></a>Organisation und Bestellung des Menüelements

-   **Organisieren Sie die Menüelemente in Gruppen von sieben oder weniger stark verknüpften Elementen.** Hierfür werden Untermenüs als einzelnes Menüelement im übergeordneten Menü gezählt.
-   **Legen Sie nicht mehr als 25 Elemente innerhalb einer einzelnen Menüebene** ab (ohne Untermenüs).
-   **Setzen Sie Trennzeichen zwischen den Gruppen in einem Menü.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.
-   **Legen Sie in einem Menü die Gruppen in ihrer logischen Reihenfolge ab.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Gruppen.
-   **Legen Sie die Elemente innerhalb einer Gruppe in ihrer logischen Reihenfolge ab.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Elemente. Legen Sie numerische Elemente (z. B. Zoomprozentsätze) in numerischer Reihenfolge ab.

### <a name="submenus"></a>Submenus

-   **Vermeiden Sie unnötige Untermenüs.** Untermenüs erfordern mehr physischen Aufwand und erschweren in der Regel die Suche nach Menüelementen.
-   **Legen Sie nicht häufig verwendete Menüelemente in ein Untermenü ein.** Dies würde die Verwendung dieser Befehle ineffizient machen. Sie können jedoch häufig verwendete Befehle in ein Untermenü aufnehmen, wenn normalerweise direkter auf sie zugegriffen wird, z. B. mit einer Symbolleiste.
-   **Erwägen Sie die Verwendung eines Untermenüs, wenn:**
    -   Dadurch wird das übergeordnete Menü vereinfacht, da es über viele Elemente (20 oder mehr) verfügt oder das Untermenü Teil einer Gruppe von mehr als sieben Elementen ist.
    -   Die Elemente im Untermenü werden seltener verwendet als die Elemente im übergeordneten Menü.
    -   Das Untermenü hätte drei oder mehr Elemente.
    -   Es gibt drei oder mehr Befehle, die mit demselben Wort beginnen. Verwenden Sie in diesem Fall dieses Wort als Untermenübezeichnung.

![Screenshot des Menüs "Neu" mit vier Untermenüelementen ](images/cmd-menus-image12.png)

In diesem Beispiel ersetzt das Untermenü Neu separate Befehle für Neue E-Mail-Nachricht, Neue Nachrichtennachricht, Neuer Ordner und Neuer Kontakt.

-   **Verwenden Sie höchstens drei Menüebenen.** Das heißt, Sie können über ein primäres Menü und höchstens zwei Untermenüebenen verfügen. Zwei Untermenüebenen sollten selten sein.

### <a name="presentation"></a>Präsentation

-   **Deaktivieren Sie Menüelemente, die nicht für den aktuellen Kontext gelten,** anstatt sie zu entfernen. Dadurch wird der Inhalt der Menüleiste stabil und leichter zu finden. **Ausnahmen:**
    -   Entfernen Sie für Kontextmenükategorien **Kontextmenüelemente, die nicht für den aktuellen Kontext gelten,** anstatt sie zu deaktivieren. Eine Menükategorie ist kontextbezogen, wenn sie nur für bestimmte Modi angezeigt wird, z. B. wenn ein bestimmter Objekttyp ausgewählt wird. Weitere Informationen finden Sie in den Richtlinien [zum Entfernen und Deaktivieren](#context-menus) von Kontextmenüs.
    -   Wenn die Bestimmung, wann ein Menüelement deaktiviert werden soll, zu spürbaren Leistungsproblemen führt, lassen Sie das Menüelement aktiv, und führen Sie bei Bedarf zu einer Fehlermeldung.

### <a name="tab-menus"></a>Registerkartenmenüs

-   **Jedes Registerkartenmenü kann kontextspezifische Optionen und Hilfemenüelemente enthalten.** Dies steht im Gegensatz zu allen anderen Menümustern. Jede Registerkarte wird für einen dedizierten Satz von Aufgaben verwendet, sodass jede Redundanz über Registerkartenmenüs hinweg nicht verwirrend ist.

### <a name="context-menus"></a>Kontextmenüs

-   **Verwenden Sie Kontextmenüs nur für kontextbezogene Befehle und Optionen.** Die Menüelemente sollten nur für das ausgewählte (oder angeklickte) Objekt oder den ausgewählten Fensterbereich und nicht für das gesamte Programm gelten.
-   **Machen Sie Befehle nicht nur über Kontextmenüs verfügbar.** Wie Tastenkombinationen sind Kontextmenüs alternative Möglichkeiten zum Ausführen von Befehlen und Auswählen von Optionen. Beispielsweise ist ein Properties-Befehl auch über die Menüleiste oder die ALT+EINGABETASTE verfügbar.
-   **Stellen Sie Kontextmenüs für alle Objekte und Fensterbereiche** bereit, die von einem kleinen Satz kontextabhängiger Befehle und Optionen profitieren. Viele Benutzer klicken regelmäßig mit der rechten Maustaste und erwarten, kontextbezogene Menüs überall zu finden.
-   **Erwägen Sie die Verwendung einer Dropdownpfeilschaltfläche für Kontextmenüs für alle Benutzer.** Normalerweise sind Kontextmenüs für Befehle und Optionen geeignet, die auf fortgeschrittene Benutzer ausgerichtet sind. Sie können jedoch eine Dropdown-Menüschaltfläche verwenden, wenn Kontextmenüs die beste Menüauswahl sind und Sie alle Benutzer als Ziel verwenden müssen.

![Screenshot des Fotos mit der Dropdownmenüschaltfläche ](images/cmd-menus-image7.png)

In diesem Beispiel wird eine Dropdown-Menüschaltfläche verwendet, um ein Kontextmenü sichtbar zu machen.

**Organisation und Bestellung des Menüelements**

-   **Organisieren Sie die Menüelemente in Gruppen von sieben oder weniger stark verknüpften Elementen.**
-   **Vermeiden Sie die Verwendung von Untermenüs,** um Kontextmenüs einfach, direkt und effizient zu halten.
-   **Legen Sie nicht mehr als 15 Elemente in einem Kontextmenü ab.**
-   **Setzen Sie Trennzeichen zwischen den Gruppen in einem Menü.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.
-   **Zeigen Sie Menüelemente in der folgenden Reihenfolge an:**

<dl> Primäre (am häufigsten verwendete) Befehle<dl> Öffnen  
Ausführen  
Abspielen  
Drucken <separator>  
</dl> </dd> <dd>Vom -Objekt unterstützte sekundäre Befehle<dl> <separator>  
</dl> </dd> Übertragen von Befehlen<dl> Ausschneiden  
Kopieren  
Einfügen <separator>  
</dl> </dd> <dd>Objekteinstellungen<dl> <separator>  
</dl> </dd> Objektbefehle<dl> Löschen  
Umbenennen <separator>  
Eigenschaften
</dl> </dd> </dl>

**Präsentation**

-   **Zeigen Sie den Standardbefehl fett an.** Wenn dies praktisch ist, machen Sie es auch zum ersten Menüelement. Der Standardbefehl wird aufgerufen, wenn Benutzer auf ein Objekt doppelklicken oder es auswählen und die EINGABETASTE drücken.
-   **Entfernen Sie Kontextmenüelemente, die nicht für den aktuellen Kontext gelten, anstatt sie zu deaktivieren.** Dadurch werden Kontextmenüs kontextabhängig und effizient.
    -   **Ausnahme:** Deaktivieren Sie Menüelemente, die nicht angewendet werden, wenn eine angemessene Erwartung besteht, dass sie verfügbar sind:
        -   Verwenden Sie immer die relevanten Standardkontextmenübefehle, z. B. Ausschneiden, Kopieren, Einfügen, Löschen und Umbenennen.
        -   Verwenden Sie immer die Befehle, die verwandte Sätze abschließen. Wenn z. B. ein Zurück vorhanden ist, sollte auch ein Forward vorhanden sein. Wenn ein Ausschneiden vorhanden ist, sollten Sie immer kopieren und einfügen.

### <a name="bullets-and-checkmarks"></a>Aufzählungszeichen und Häkchen

-   **Menüelemente, die Optionen sind, können Aufzählungszeichen und Häkchen verwenden.** Befehle können dies nicht sein.
-   **Verwenden Sie einen Aufzählungszeichen, um eine Option aus einer kleinen Gruppe von sich gegenseitig ausschließenden Optionen auszuwählen.** In einer Gruppe sollten immer mindestens zwei Aufzählungszeichen vorhanden sein. Weitere Informationen finden Sie unter [Optionsfelder.](ctrl-radio-buttons.md)
-   **Verwenden Sie ein Häkchen, um eine unabhängige Einstellung ein- oder auszuschalten.** Wenn die ausgewählten und gelöschten Zustände keine klaren und eindeutigen Gegensätze sind, verwenden Sie stattdessen eine Reihe von Aufzählungszeichen. Weitere Informationen finden Sie unter [Kontrollkästchen.](ctrl-check-boxes.md)
-   **Für einen gemischten Häkchenzustand zeigen Sie ein Menüelement ohne Häkchen an.** Der gemischte Zustand wird für die Mehrfachauswahl verwendet, um anzugeben, dass die Option für einige, aber nicht für alle Objekte festgelegt ist, sodass jedes einzelne Objekt entweder über den ausgewählten oder den gelöschten Zustand verfügt. Der gemischte Zustand wird nicht als dritter Zustand für ein einzelnes Element verwendet.
-   **Setzen Sie Trennzeichen zwischen den verknüpften Sätzen von Häkchen oder Aufzählungszeichen.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.

### <a name="icons"></a>Symbole

-   **Erwägen Sie in folgenden Fällen Symbole für die Menüpunkte einzurichten:**
    -   Die am häufigsten verwendeten Menüelemente.
    -   Menüelemente, deren Symbol standard und bekannt ist.
    -   Menüpunkte, deren Funktion auf einfache Weise mit einem Symbol veranschaulicht werden kann.
-   **Wenn Sie Symbole verwenden, sind Sie nicht dazu aufgefordert, sie für alle Menüelemente bereitzustellen.** Kryptische Symbole sind nicht hilfreich, machen das Menü unübersichtlich und hindern Benutzer daran, wichtige Menüpunkte einfach aufzufinden.

![Screenshot von Menüelementen mit und ohne Symbole ](images/cmd-menus-image13.png)

In diesem Beispiel enthält das Menü Organisieren nur Symbole für die am häufigsten verwendeten Menüelemente.

-   **Stellen Sie sicher, dass Die Menüsymbole den Richtlinien für Symbole im Stile des Menüs entsprechen.**

Weitere Informationen und Beispiele finden Sie unter [Symbole.](vis-icons.md)

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Weisen Sie allen Menüelementen Zugriffsschlüssel zu.** Keine Ausnahmen.
-   **Weisen Sie nach Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß den Standardzugriffsschlüsselzuweisungen zu.** Konsistente Zuweisungen von Zugriffsschlüsseln sind zwar nicht immer möglich, werden jedoch bevorzugt – insbesondere bei häufig verwendeten Befehlen.
-   **Weisen Sie zugriffstasten für dynamische Menüelemente (z. B. zuletzt verwendete Dateien) numerisch zu.**

![Screenshot von Menüelementen mit numerischen Zugriffsschlüsseln ](images/cmd-menus-image14.png)

In diesem Beispiel weist das Paint-Programm in Windows zuletzt verwendeten Dateien numerische Zugriffsschlüssel zu.

-   **Weisen Sie eindeutige Zugriffsschlüssel innerhalb einer Menüebene zu.** Sie können Zugriffsschlüssel auf verschiedenen Menüebenen wiederverwenden.
-   **Einfaches Auffinden von Zugriffsschlüsseln:**
    -   Wählen Sie für die am häufigsten verwendeten Menüelemente Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menüelemente Buchstaben aus, die ein eindeutiger Konsonant oder ein Vokal in der Bezeichnung sind.
-   **Bevorzugen Sie Zeichen mit breiter Breite,** z. B. w, m und Großbuchstaben.
-   **Bevorzugen Sie einen typischen Konsonanten oder einen Vokal,** z. B. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwierig zu erkennen machen,** z. B. (von den problematischsten bis zu den am wenigsten problematischen):
    -   Buchstaben, die nur ein Pixel breit sind, z. B. i und l.
    -   Buchstaben mit Nachfolgern wie g, j, p, q und y.
    -   Buchstaben neben einem Buchstaben mit einem Nachfolger.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur.](inter-keyboard.md)

### <a name="shortcut-keys"></a>Tastenkombinationen

-   **Weisen Sie den am häufigsten verwendeten Menüelementen Tastenkombinationen zu.** Selten verwendete Menüelemente benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffsschlüssel verwenden können.
-   **Machen Sie eine Tastenkombination nicht zur einzigen Möglichkeit, eine Aufgabe auszuführen.** Benutzer sollten auch in der Lage sein, die Maus oder Tastatur mit Tabulatortasten, Pfeilen und Zugriffsschlüsseln zu verwenden.
-   **Verwenden Sie für bekannte Tastenkombinationen die Standardzuweisungen.**
-   **Weisen Sie bekannten Tastenkombinationen keine unterschiedlichen Bedeutungen zu.** Da sie sich merken, sind inkonsistente Bedeutungen für bekannte Tastenkombinationen frustrierend und fehleranfällig. Die bekannten Tastenkombinationen, die von Windows-Programmen verwendet werden, finden Sie unter Windows-Tastenkombinationen.
-   **Versuchen Sie nicht, systemweite Programmverknüpfungsschlüssel zuzuweisen.** Die Tastenkombinationen des Programms haben nur dann Auswirkungen, wenn ihr Programm den Eingabefokus besitzt.
-   **Dokumentieren Sie alle Tastenkombinationen.** Auf diese Weise können Benutzer die Tastenkombinationszuweisungen erlernen.
    -   **Ausnahme:** Zeigen Sie keine Tastenkombinationszuweisungen in Kontextmenüs an. Kontextmenüs zeigen die Tastenkombinationszuweisungen nicht an, da sie für Effizienz optimiert sind.
-   **Für nicht standardmäßige Schlüsselzuweisungen:**
    -   **Wählen Sie Tastenkombinationen ohne Standardzuweisungen aus.** Weisen Sie standard-Tastenkombinationen nie neu zu.
    -   **Verwenden Sie nicht standardmäßige Schlüsselzuweisungen konsistent im gesamten Programm.** Weisen Sie in verschiedenen Fenstern keine unterschiedlichen Bedeutungen zu.
    -   Wählen Sie nach **Möglichkeit mnemonische Schlüsselzuweisungen aus,** insbesondere für häufig verwendete Befehle.
    -   **Verwenden Sie Funktionstasten für Befehle, die einen kleinen Effekt haben,** z. B. Befehle, die für das ausgewählte Objekt gelten. Beispielsweise benennt F2 das ausgewählte Element um.
    -   **Verwenden Sie Tastenkombinationen mit STRG für Befehle mit umfangreichen Auswirkungen,** z. B. Befehle, die für ein gesamtes Dokument gelten. Beispielsweise speichert STRG+S das aktuelle Dokument.
    -   **Verwenden Sie Tastenkombinationen umschalten für Befehle, die die Aktionen der Standardtaste erweitern oder ergänzen.** Die Tastenkombination ALT+TAB durchkreist z. B. geöffnete primäre Fenster, während ALT+UMSCHALT+TAB in umgekehrter Reihenfolge zyklen. Auf ähnliche Weise zeigt F1 Hilfe an, während UMSCHALT+F1 kontextbezogene Hilfe anzeigt.
    -   **Verwenden Sie nicht die folgenden Zeichen für Tastenkombinationen:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Diese Zeichen erfordern unterschiedliche Tastenkombinationen in verschiedenen Sprachen oder sind gebietsschemaspezifisch.
    -   **Verwenden Sie keine Tastenkombinationen mit STRG+ALT,** da Windows diese Kombination in einigen Sprachversionen als ALTGR-Taste interpretiert, die alphanumerische Zeichen generiert.
-   **Wenn Ihr Programm viele Tastenkombinationen zuweist, können Sie die Zuweisungen anpassen.** Auf diese Weise können Benutzer in Konflikt geratene Tastenkombinationen neu zuweisen und von anderen Produkten migrieren. Die meisten Programme weisen nicht genügend Tastenkombinationen zu, um dieses Feature zu benötigen.

Weitere Richtlinien und Standardzuweisungen für Tastenkombinationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="standard-menus"></a>Standardmenüs

-   **Verwenden Sie die Standardmenüorganisation für Programme, die Dokumente erstellen oder anzeigen.** Die Standardmenüorganisation macht allgemeine Menüelemente vorhersagbar und leichter zu finden.
-   **Verwenden Sie für andere Arten von Programmen nur dann die Standardmenüorganisation, wenn dies sinnvoll ist.** Erwägen Sie, Ihre Befehle und Optionen basierend auf dem Zweck Ihres Programms und der Art und Weise, wie Benutzer über ihre Aufgaben und Ziele denken, in nützlicheren, natürlicheren Kategorien zu organisieren.

**Standardmenüleisten**

Die Standardstruktur der Menüleiste lautet wie folgt. In dieser Liste werden die Menükategorie- und Elementbezeichnungen, ihre Reihenfolge mit Trennzeichen, deren Zugriffs- und Tastenkombinationen und ihre Auslassungszeichen angezeigt.

<dl> Datei<dl> Neue STRG+N  
Öffnen... STRG+O  
Schließen <separator>  
Strg+S speichern  
Speichern unter... <separator>  
Senden an <separator>  
Drucken... STRG+P  
Seitenansicht  
Seiteneinrichtung <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Beenden Sie ALT+F4 (Verknüpfung wird normalerweise nicht angegeben)
</dl> </dd> Edit<dl> Strg+Z rückgängig  
Redo STRG+Y <separator>  
Strg+X ausschneiden  
Kopieren von STRG+C  
Strg+V einfügen <separator>  
Wählen Sie strg+A aus. <separator>  
Delete Del (Verknüpfung in der Regel nicht angegeben) <separator>  
Finden... STRG+F  
Suche nach F3 (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG+H  
Gehe zu... STRG+G
</dl> </dd> View<dl> Symbolleisten  
Statusleiste <separator>  
</dl> </dd> Zoom<dl> Zoomen in STRG++  
Verkleinern Sie STRG+- <separator>  
Vollbild F11  
F5 aktualisieren
</dl> </dd> <dd>Tools<dl> ... <separator>  
Optionen
</dl> </dd> Hilfe<dl> <program name> Hilfe F1 <separator>  
Über <program name>  
</dl> </dd> </dl>

**Standardsymbolleisten-Menüschaltflächen**

Die Standardschaltflächen des Symbolleistenmenüs sind wie folgt. Diese Liste zeigt die Menükategorie- und Elementbezeichnungen, ihre Reihenfolge mit Trennzeichen, ihre Tastenkombinationen und ihre Ellipsen.

<dl> Tools<dl> VollbildF11(Zugriffsschlüssel neu zuweisen, wenn auch Suchen verwendet wird.)  
Symbolleisten (Beachten Sie, dass der Befehl Menüleiste hier angezeigt wird.) <separator>  
Drucken...  
Finden... <separator>  
Zoom  
Textgröße <separator>  
Optionen
</dl> </dd> Organize<dl> Neuer OrdnerCtrl+N <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Wählen Sie allCtrl+A aus. <separator>  
DeleteDel(shortcut normalerweise nicht angegeben)  
Umbenennen <separator>  
Optionen
</dl> </dd> Page<dl> Neues FensterCtrl+N <separator>  
Zoom  
Textgröße
</dl> </dd> </dl>

**Standardkontextmenüs**

Der Standardinhalt des Kontextmenüs lautet wie folgt. In dieser Liste werden die Menüelementbezeichnungen, ihre Reihenfolge mit Trennzeichen, ihre Zugriffsschlüssel und ihre Auslassungszeichen angezeigt. Kontextmenüs zeigen keine Tastenkombinationen an.

<dl> Öffnen  
Ausführen  
Abspielen  
Bearbeiten  
Drucken... <separator>  
Ausschneiden  
Kopieren  
Einfügen <separator>  
Löschen  
Umbenennen <separator>  
Sperren des <object name> (Häkchens)  
Eigenschaften
</dl>

### <a name="using-ellipses"></a>Verwenden von Ausellipsen

Während Menübefehle für sofortige Aktionen verwendet werden, sind möglicherweise weitere Informationen erforderlich, um die Aktion auszuführen. **Geben Sie einen Befehl an, der zusätzliche Informationen (einschließlich einer Bestätigung) benötigt, indem Sie am Ende der Bezeichnung auslassungszeichen hinzufügen.**

![Screenshot des Druckbefehls und des Druckdialogfelds ](images/cmd-menus-image15.png)

In diesem Beispiel wird die Druck-... -Befehl zeigt ein Dialogfeld Drucken an, um weitere Informationen zu sammeln.

**Die ordnungsgemäße Verwendung von Ausellipsen ist wichtig, um anzugeben, dass Benutzer vor dem Ausführen der Aktion weitere Entscheidungen treffen oder die Aktion sogar vollständig abbrechen können.** Die visuellen Hinweise, die durch auslassungsbare Elemente geboten werden, ermöglichen es Benutzern, Ihre Software ohne Sorge zu untersuchen.

**Dies bedeutet nicht, dass Sie** immer dann eine Auslassungsellipse verwenden sollten, wenn eine Aktion nur dann ein anderes Fenster anzeigt, wenn zusätzliche Informationen zum Ausführen der Aktion erforderlich sind. Beispielsweise müssen die Befehle Info, Erweitert, Hilfe, Optionen, Eigenschaften und Einstellungen ein weiteres Fenster anzeigen, wenn sie angeklickt werden, aber keine zusätzlichen Informationen vom Benutzer erfordern. Daher benötigen sie keine Ausellipsen.

**Bei Mehrdeutigkeit (z. B. fehlt in der Befehlsbezeichnung ein Verb), entscheiden Sie basierend auf der wahrscheinlichsten Benutzeraktion.** Wenn das einfache Anzeigen des Fensters eine gängige Aktion ist, verwenden Sie keine Auslassungsellipse.

**Richtig:**

Weitere Farben...

Versionsinformationen

Im ersten Beispiel wählen Benutzer wahrscheinlich eine Farbe aus, daher ist die Verwendung von Ausellipsen richtig. Im zweiten Beispiel werden Benutzer wahrscheinlich die Versionsinformationen anzeigen, wodurch Ellipsen nicht erforderlich sind.

> [!Note]  
> Wenn Sie bestimmen, ob ein Menübefehl [Auslassungspunkte](winenv-uac.md) benötigt, verwenden Sie nicht die Notwendigkeit, Berechtigungen als Faktor zu erhöhen.

 

Erhöhte Rechte sind keine Informationen, die zum Ausführen eines Befehls erforderlich sind (sondern aus Berechtigungsgründen), und die Notwendigkeit einer Erhöhung wird mit dem Sicherheitsschutz angezeigt.

## <a name="labels"></a>Bezeichnungen

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf die Groß-/Formatvorlagen verwenden, um das Mischen von Groß-/Formatvorlagen zu vermeiden.

### <a name="menu-category-names"></a>Menükategorienamen

-   **Verwenden Sie Menükategorienamen, bei denen es sich um Einzelwortverben oder Nomen handelt.** Eine Bezeichnung mit mehreren Wörtern kann für zwei Bezeichnungen mit einem Wort verwirrend sein.
-   **Bevorzugen Sie verbbasierte Menünamen.** Lässt das Verb jedoch weg, wenn es "Create", "Show", "View" oder "Manage" ist. Die folgenden Menükategorien verfügen beispielsweise nicht über Verben:
    -   Tabelle
    -   Tools
    -   Fenster
-   Verwenden Sie für nicht standardmäßige Kategorienamen **ein einzelnes, spezifisches Wort,** das den Menüinhalt eindeutig und genau beschreibt. Obwohl die Namen nicht so allgemein sein müssen, dass sie alles im Menü beschreiben, sollten sie vorhersagbar genug sein, damit Benutzer nicht von dem, was sie im Menü finden, nicht überraschend sind.

### <a name="menu-item-names"></a>Menüelementnamen

-   **Verwenden Sie Menüelementnamen, die mit einem Verb, Nomen oder Nomenphrasen beginnen.**
-   **Bevorzugen Sie verbbasierte Menünamen.** Das Verb sollte jedoch ausgelassen werden, wenn:
    -   **Das Verb ist "Create", "Show", "View" oder "Manage".** Die folgenden Befehle enthalten beispielsweise keine Verben:
        -   Info
        -   Fortgeschrittene
        -   Vollbildmodus
        -   Neu
        -   Optionen
        -   Eigenschaften
    -   **Das Verb ist mit dem Namen der Menükategorie identisch, um Wiederholungen zu vermeiden.** Verwenden Sie in der Menükategorie Einfügen beispielsweise Text, Tabelle und Bild anstelle von Text einfügen, Tabelle einfügen und Bild einfügen.
-   **Verwenden Sie bestimmte Verben.** Vermeiden Sie generische, nicht hilfreiche Verben wie Change und Manage.
-   **Verwenden Sie singulare Nomen für Befehle, die für ein einzelnes Objekt gelten.** Verwenden Sie andernfalls Pluralnunen.
-   **Verwenden Sie nach Bedarf Modifizierer, um zwischen ähnlichen Befehlen zu unterscheiden.** Beispiele: Zeile oben einfügen, Zeile unten einfügen.
-   **Wählen Sie für Paare von ergänzenden Befehlen eindeutig ergänzende Namen aus.** Beispiele: Hinzufügen, Entfernen; Anzeigen, Ausblenden; Einfügen, Löschen.
-   **Wählen Sie Menüelementnamen basierend auf Benutzerzielen und Aufgaben aus, nicht auf Technologie.**

**Richtig:**

![Screenshot des Menüs "Rip" mit Formatmenüelement ](images/cmd-menus-image16.png)

**Falsch:**

![Screenshot des Menüs "Rip" mit codec-Menüelement ](images/cmd-menus-image17.png)

Im falschen Beispiel basiert das Menüelement auf seiner Technologie.

-   Verwenden Sie die folgenden Menüelementnamen für den angegebenen Zweck:
    -   **Optionen** So zeigen Sie Programmoptionen an.
    -   **Anpassen** So zeigen Sie die Programmoptionen an, die sich speziell auf die Konfiguration der maschinellen Benutzeroberfläche bezieht.
    -   **Personalisieren** So zeigen Sie eine Zusammenfassung der häufig verwendeten [Personalisierungseinstellungen](glossary.md) an.
    -   **Einstellungen** Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.
    -   **Eigenschaften** So zeigen Sie das Eigenschaftenfenster eines Objekts an.
    -   **Einstellungen** Verwenden Sie nicht als Menübezeichnung. Verwenden Sie stattdessen Optionen.

### <a name="submenu-names"></a>Untermenünamen

-   **Menüelemente, die Untermenüs anzeigen, haben nie Auslassungspunkte auf ihrer Bezeichnung.** Der Untermenüpfeil gibt an, dass eine weitere Auswahl erforderlich ist.

**Falsch:**

![Screenshot des neuen Menüelements mit Auslassungsellipsen ](images/cmd-menus-image18.png)

In diesem Beispiel verfügt das Menüelement Neu fälschlicherweise über Auslassungspunkte.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Menüs:

-   In Befehlen, die Menüs ein- oder ausblenden, verweisen Sie auf Menüleisten. Verweisen Sie nicht auf klassische Menüs.
-   Verweisen Sie auf Menüs nach ihren Bezeichnungen. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Unterstriche, aber schließen Sie den Unterstrich oder die Auslassungszeichen der Zugriffsschlüssel nicht ein.
-   Um auf Menükategorien zu verweisen, verwenden Sie "Im <category name> Menü". Wenn die Position eines Menüelements aus dem Kontext klar ist, müssen Sie die Menükategorie nicht erwähnen.
-   Um die Benutzerinteraktion von Menüelementen zu beschreiben, verwenden Sie Click ohne das Wortmenü oder den Befehl . Verwenden Sie nicht auswählen, auswählen oder auswählen. Verweisen Sie nur in der technischen Dokumentation auf ein Menüelement als Menüelement.
-   Um das Entfernen eines Häkchens aus einer Menüoption zu beschreiben, verwenden Sie klicken, um das Häkchen zu entfernen. Verwenden Sie nicht clear.
-   Kontextmenüs werden als Kontextmenüs und nicht als Kontextmenüs bezeichnet.
-   Verwenden Sie keine Cascading-, Pull-Down-, Dropdown- oder Popupmenüs, um Menüs zu beschreiben, außer in der Programmierdokumentation.
-   Verweisen Sie auf nicht verfügbare Menüelemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder grau. Verwenden Sie deaktiviert in der Programmierdokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnungen nur dann in Anführungszeichen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Klicken Sie **im Menü** Datei auf **Drucken,** um das Dokument zu drucken.
-   Zeigen Sie **im Menü** Ansicht auf **Symbolleisten**, und klicken Sie dann **auf Formatieren.**

 

