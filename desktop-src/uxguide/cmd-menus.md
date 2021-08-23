---
title: Menüs (Designgrundkenntnisse)
description: Menüs sind hierarchische Listen von Befehlen oder Optionen, die Benutzern im aktuellen Kontext zur Verfügung stehen.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: e9b2c3559163ff77e8e3f08354b017c1b7cb53c95fd51802ae2565efdf71abcd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350173"
---
# <a name="menus-design-basics"></a>Menüs (Designgrundkenntnisse)

> [!NOTE]
> Dieses Entwurfshandbuch wurde für Windows 7 erstellt und für neuere Versionen von Windows. Ein Teil der Anleitungen gilt weiterhin im Prinzip, aber die Darstellung und die Beispiele spiegeln nicht unsere [aktuelle Entwurfsanleitung wider.](/windows/uwp/design/)

Menüs sind hierarchische Listen von Befehlen oder Optionen, die Benutzern im aktuellen Kontext zur Verfügung stehen.

Dropdownmenüs sind Menüs, die bei Bedarf per Mausklick oder Mauszeiger angezeigt werden. Sie werden normalerweise nicht angezeigt und sind daher ein effizientes Mittel, um Platz auf dem Bildschirm zu sparen. Ein Untermenü oder kaskadierenden Menü ist ein sekundäres Menü, das bei Bedarf innerhalb eines Menüs angezeigt wird. Sie werden durch einen Pfeil am Ende der Untermenübezeichnung angezeigt. Ein Menüelement ist ein einzelner Befehl oder eine Option innerhalb eines Menüs.

Menüs werden häufig über eine Menüleiste angezeigt. Dabei handelt es sich um eine Liste bezeichneter Menükategorien, die sich in der Regel am oberen Fensteranfang befinden. Im Gegensatz dazu wird ein Kontextmenü heruntergefahren, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, das ein Kontextmenü unterstützt.

![Screenshot der Menüleiste mit Menü und Untermenü ](images/cmd-menus-image1.png)

Eine typische Menüleiste mit einem Dropdownmenü und Untermenü.

> [!Note]  
> Richtlinien für [Befehlsschaltflächen,](ctrl-command-buttons.md) [Symbolleisten](cmd-toolbars.md)und [Tastatur](inter-keyboard.md) werden in separaten Artikeln vorgestellt.

 

## <a name="usage-patterns"></a>Verwendungsmuster

Menüs haben mehrere Verwendungsmuster:



| Verwendung                                                                                                                                                |    Beispiel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Menüleisten**<br/> In einer Menüleiste werden Befehle und Optionen in Dropdownmenüs angezeigt. <br/>                                               | Menüleisten sind sehr häufig und leicht zu finden sowie eine effiziente Nutzung des Platzes. <br/> ![Screenshot der Menüleiste mit Dropdownmenü ](images/cmd-menus-image2.png)<br/> Eine Menüleiste aus Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Symbolleistenmenüs**<br/> eine Als Symbolleiste implementierte Menüleiste. <br/>                                                                   | Symbolleistenmenüs sind Symbolleisten, die in erster Linie aus Befehlen [in](ctrl-command-buttons.md) Menüschaltflächen und geteilten Schaltflächen bestehen, mit nur wenigen direkten Befehlen(sofern verfügbar). <br/> ![Screenshot des Symbolleistenmenüs mit Dropdownmenü ](images/cmd-menus-image3.png)<br/> Ein Symbolleistenmenü in Windows Fotogalerie.<br/> Richtlinien zu diesem Muster finden Sie unter [Symbolleisten.](cmd-toolbars.md)<br/>                                                                                                                                                                                                             |
| **Registerkartenmenüs**<br/> Schaltflächen in Registerkarten, die eine kleine Gruppe von Befehlen und Optionen im Zusammenhang mit einer Registerkarte in einem Dropdownmenü anzeigen. <br/> | Registerkarten mit Menüs sehen wie normale Registerkarten aus, außer dass ihr unterer Teil über eine Schaltfläche mit Dropdownpfeil verfügt. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdownmenü angezeigt, anstatt die Registerkarte auszuwählen. <br/> ![Screenshot des Registerkartenmenüs mit Dropdownmenü ](images/cmd-menus-image4.png)<br/> Registerkartenmenüs werden in der Windows Media Player.<br/>                                                                                                                                                                                                                                                                                           |
| **Menüschaltflächen**<br/> -Befehlsschaltflächen, die eine kleine Gruppe verwandter Befehle in einem Dropdownmenü anzeigen. <br/>                       | [-Menüschaltflächen](ctrl-command-buttons.md) sehen wie normale Befehlsschaltflächen aus, außer dass sie einen Dropdownpfeil enthalten. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdownmenü angezeigt, anstatt einen Befehl auszuführen.<br/> [Teilungsschaltflächen](ctrl-command-buttons.md) ähneln Menüschaltflächen, mit dem Ausnahme, dass es sich um Variationen eines Befehls handelt. Wenn Sie auf den linken Teil der Schaltfläche klicken, wird die Aktion direkt auf der Bezeichnung ausgeführt.<br/> ![Screenshot der Menüschaltfläche mit Dropdownbefehlen ](images/cmd-menus-image5.png)<br/> Eine Menüschaltfläche mit einem kleinen Satz verwandter Befehle.<br/> |
| **Kontextmenüs**<br/> Dropdownmenüs, die eine kleine Gruppe von Befehlen und Optionen im Zusammenhang mit dem aktuellen Kontext anzeigen. <br/>       | Dropdownmenüs für Kontextmenüs, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, der ein Kontextmenü unterstützt. <br/> ![Screenshot des Kontextmenüs mit Befehlen ](images/cmd-menus-image6.png)<br/> ein Kontextmenü aus dem Windows-Explorer.<br/> Wenn Kontextmenüs die beste Menüauswahl sind, Sie aber eine lösung benötigen, die für alle Benutzer geeignet ist, können Sie eine Dropdownpfeil-Schaltfläche im Menü verwenden. <br/> ![Screenshot des Fotos mit Dropdownmenüschaltfläche ](images/cmd-menus-image7.png)<br/> Ein Kontextmenü, das mit einer Dropdownschaltfläche angezeigt wird.<br/>                                                   |
| **Menüs im Aufgabenbereich**<br/> eine kleine Gruppe von Befehlen, die sich auf das ausgewählte Objekt oder den ausgewählten Programmmodus bezieht. <br/>                              | Im Gegensatz zu Kontextmenüs werden sie automatisch in einem Fensterbereich statt bei Bedarf angezeigt. <br/> ![Screenshot des Fotos mit Menü "Aufgabenbereich" auf der rechten Seite ](images/cmd-menus-image8.png)<br/> Ein Aufgabenbereichmenü im Windows Fotogalerie Viewer.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Ist dies die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

### <a name="menu-bars"></a>Menüleisten

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es viele Menüelemente?
-   Gibt es viele Menükategorien?
-   Gelten die meisten Menüelemente für das gesamte Programm und das primäre Fenster?
-   Muss das Menü für alle Benutzer funktionieren?

Wenn ja, sollten Sie eine Menüleiste verwenden.

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
-   Verfügt das Fenster über Registerkarten, in denen jede Registerkarte für einen dedizierten Satz von Aufgaben verwendet wird (im Gegensatz zur Verwendung von Registerkarten zum Anzeigen unterschiedlicher Ansichten)?
-   Gibt es eine Menükategorie, die für jede Registerkarte gilt?
-   Gibt es viele Befehle und Optionen, aber nur einen kleinen Satz für jede Registerkarte?

Falls ja, sollten Sie anstelle einer Menüleiste ein Registerkartenmenü verwenden.

### <a name="context-menu"></a>Kontextmenü

Gehen Sie wie folgt vor:

-   Gibt es einen kleinen Satz kontextbezogener Befehle und Optionen, die für das ausgewählte Objekt oder den ausgewählten Fensterbereich gelten?
-   Sind diese Menüelemente redundant?
-   Sind die Zielbenutzer mit Kontextmenüs vertraut?

Falls ja, sollten Sie Kontextmenüs für die Objekte und Fensterregionen bereitstellen, die sie benötigen.

Bei browserbasierten Programmen sind Aufgabenbereichmenüs eine gängigere Lösung für kontextbezogene Befehle. Derzeit erwarten Benutzer, dass Kontextmenüs in browserbasierten Programmen generisch und nicht hilfreich sind.

### <a name="task-pane-menu"></a>Menü "Aufgabenbereich"

Gehen Sie wie folgt vor:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es eine kleine Gruppe von kontextbezogenen Befehlen und Optionen, die für das ausgewählte Objekt oder den ausgewählten Programmmodus gelten?
-   Gibt es einige Menükategorien?
-   Muss das Menü für alle Benutzer funktionieren?

Falls ja, sollten Sie anstelle eines Kontextmenüs ein Aufgabenbereichmenü verwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Menüs, die eine gute Benutzerfreundlichkeit fördern:

-   Verwenden Sie eine Befehlspräsentation, die Ihrem Programmtyp, den Fenstertypen, der Befehlsverwendung und den Zielbenutzern entspricht.
-   Sind gut organisiert, und verwenden Sie bei Entsprechendm die Standardmenüorganisation.
-   Verwenden Sie Menüleisten, Symbolleisten und Kontextmenüs effektiv.
-   Verwenden Sie Symbole effektiv.
-   Verwenden Sie Zugriffsschlüssel und Tastenkombinationen effektiv.

**Wenn Sie nur eine Sache durchführen...**

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

Im Allgemeinen funktionieren Symbolleisten hervorragend mit Menüleisten, da sich beide auf ihre Stärken konzentrieren können, ohne kompromittiert zu werden.

-   Blenden Sie die Menüleiste standardmäßig aus, wenn das Symbolleistendesign eine Menüleiste redundant macht.
-   Blenden Sie die Menüleiste aus, anstatt sie vollständig zu entfernen, da Für Tastaturbenutzer besser auf Menüleisten zugegriffen werden kann.
-   Um die Menüleiste wiederherzustellen, geben Sie eine Menüleisten-Häkchenoption in der Menükategorie Ansicht (für primäre Symbolleisten) oder Extras (für sekundäre Symbolleisten) an. Weitere Informationen finden Sie unter [Standardmenü und unterteilte Schaltflächen.](cmd-toolbars.md)

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
-   **Legen Sie die Gruppen in einem Menü in ihrer logischen Reihenfolge ab.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Gruppen.
-   **Legen Sie die Elemente innerhalb einer Gruppe in ihrer logischen Reihenfolge ab.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Elemente. Legen Sie numerische Elemente (z. B. Zoomprozentsätze) in numerischer Reihenfolge ab.

### <a name="submenus"></a>Submenus

-   **Vermeiden Sie unnötige Untermenüs.** Untermenüs erfordern mehr physischen Aufwand und erschweren in der Regel das Auffinden der Menüelemente.
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
-   **Für einen gemischten Häkchenzustand zeigen Sie ein Menüelement ohne Häkchen an.** Der gemischte Zustand wird für die Mehrfachauswahl verwendet, um anzugeben, dass die Option für einige, aber nicht für alle Objekte festgelegt ist, sodass jedes einzelne Objekt entweder den ausgewählten oder den gelöschten Zustand hat. Der gemischte Zustand wird nicht als dritter Zustand für ein einzelnes Element verwendet.
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
-   **Weisen Sie bekannten Tastenkombinationen keine unterschiedlichen Bedeutungen zu.** Da sie sich merken, sind inkonsistente Bedeutungen für bekannte Tastenkombinationen frustrierend und fehleranfällig. Die bekannten Tastenkombinationen, die von Windows Programmen verwendet werden, finden Sie unter Windows Tastenkombinationen.
-   **Versuchen Sie nicht, systemweite Programmverknüpfungsschlüssel zuzuweisen.** Die Tastenkombinationen des Programms haben nur dann Auswirkungen, wenn ihr Programm den Eingabefokus besitzt.
-   **Dokumentieren Sie alle Tastenkombinationen.** Auf diese Weise können Benutzer die Tastenkombinationszuweisungen erlernen.
    -   **Ausnahme:** Zeigen Sie keine Tastenkombinationszuweisungen in Kontextmenüs an. Kontextmenüs zeigen die Tastenkombinationszuweisungen nicht an, da sie für Effizienz optimiert sind.
-   **Für nicht standardmäßige Schlüsselzuweisungen:**
    -   **Wählen Sie Tastenkombinationen aus, die keine Standardzuweisungen haben.** Zuweisen von Standardtastenkombinationen nie neu.
    -   **Verwenden Sie nicht standardmäßige Schlüsselzuweisungen im gesamten Programm konsistent.** Weisen Sie in verschiedenen Fenstern keine unterschiedlichen Bedeutungen zu.
    -   **Wählen Sie nach Möglichkeit mnemonische Schlüsselzuweisungen aus,** insbesondere für häufig verwendete Befehle.
    -   **Verwenden Sie Funktionsschlüssel für Befehle, die eine geringe** Auswirkung haben, z. B. Befehle, die für das ausgewählte Objekt gelten. Beispielsweise benennt F2 das ausgewählte Element um.
    -   **Verwenden Sie STRG-Tastenkombinationen für Befehle,** die einen großen Effekt haben, z. B. Befehle, die für ein gesamtes Dokument gelten. Strg+S speichert z. B. das aktuelle Dokument.
    -   **Verwenden Sie UMSCHALTTASTEnkombinationen für Befehle, die die Aktionen der Standardtastenkombination erweitern oder ergänzen.** Beispielsweise durchzyklen die Tastenkombination ALT+TAB geöffnete primäre Fenster, während ALT+UMSCHALT+TAB in umgekehrter Reihenfolge zyklen. Auf ähnliche Weise zeigt F1 Hilfe an, während UMSCHALT+F1 kontextorientierte Hilfe anzeigt.
    -   **Verwenden Sie nicht die folgenden Zeichen für Tastenkombinationen:** @ $ {} \[ \] \\  ~  \| ^ ' < >. Diese Zeichen erfordern unterschiedliche Tastenkombinationen in verschiedenen Sprachen oder sind lokal spezifisch.
    -   **Verwenden Sie keine Tastenkombinationen von STRG+ALT,** da Windows diese Kombination in einigen Sprachversionen als ALTGR-Taste interpretiert, die alphanumerische Zeichen generiert.
-   **Wenn Ihr Programm viele Tastenkombinationen zu weist, können Sie die Zuweisungen anpassen.** Auf diese Weise können Benutzer in Konflikt stehende Tastenkombinationen neu zuweisen und von anderen Produkten migrieren. Die meisten Programme weisen nicht genügend Tastenkombinationen zu, um dieses Feature zu benötigen.

Weitere Richtlinien und Standardzuweisungen für Tastenkombinationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="standard-menus"></a>Standardmenüs

-   **Verwenden Sie die Standardmenüorganisation für Programme, die Dokumente erstellen oder anzeigen.** Die Standardmenüorganisation macht allgemeine Menüelemente vorhersagbar und leichter zu finden.
-   **Verwenden Sie für andere Arten von Programmen die Standardmenüorganisation nur, wenn dies sinnvoll ist.** Erwägen Sie, Ihre Befehle und Optionen in nützlichere, natürliche Kategorien zu organisieren, die auf dem Zweck Ihres Programms und der Art und Weise basieren, wie Benutzer ihre Aufgaben und Ziele betrachten.

**Standardmenüleisten**

Die Standardstruktur der Menüleiste lautet wie folgt. In dieser Liste werden die Menükategorie- und Elementbezeichnungen, ihre Reihenfolge mit Trennzeichen, ihre Zugriffs- und Tastenkombinationen und ihre Ausellipsen angezeigt.

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
Alt+F4 beenden (Tastenkombination in der Regel nicht angegeben)
</dl> </dd> Edit<dl> Strg+Z rückgängig machen  
Wiederholen von STRG+Y <separator>  
Strg+X ausschneiden  
Kopieren von STRG+C  
Strg+V einfügen <separator>  
Wählen Sie alle STRG+A aus. <separator>  
Delete Del (Verknüpfung in der Regel nicht angegeben) <separator>  
Finden... STRG+F  
Suchen sie die nächste F3-Datei (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG+H  
Gehe zu... STRG+G
</dl> </dd> View<dl> Symbolleisten  
Statusleiste <separator>  
</dl> </dd> Zoom<dl> Zoomen in STRG++  
Verkleinern VON STRG+- <separator>  
Vollbild F11  
F5 aktualisieren
</dl> </dd> <dd>Tools<dl> ... <separator>  
Tastatur
</dl> </dd> Hilfe<dl> <program name> Hilfe F1 <separator>  
Über <program name>  
</dl> </dd> </dl>

**Standardsymbolleisten-Menüschaltflächen**

Die Standardmenüschaltflächen der Symbolleiste lauten wie folgt. In dieser Liste werden die Menükategorie und Elementbezeichnungen, ihre Reihenfolge mit Trennzeichen, ihre Tastenkombinationen und ihre Ausellipsen angezeigt.

<dl> Tools<dl> VollbildF11 (Zugriffsschlüssel neu zuweisen, wenn auch Suchen verwendet wird.)  
Symbolleisten (Beachten Sie, dass der Befehl Menüleiste hier angezeigt wird.) <separator>  
Drucken...  
Finden... <separator>  
Zoom  
Textgröße <separator>  
Tastatur
</dl> </dd> Organize<dl> Neuer OrdnerCtrl+N <separator>  
CutCtrl+X  
CopyCtrl+C  
PasteCtrl+V <separator>  
Wählen Sie allCtrl+A aus. <separator>  
DeleteDel(Verknüpfung in der Regel nicht angegeben)  
Umbenennen <separator>  
Tastatur
</dl> </dd> Page<dl> Neues FensterCtrl+N <separator>  
Zoom  
Textgröße
</dl> </dd> </dl>

**Standardkontextmenüs**

Die Standardinhalte des Kontextmenüs lauten wie folgt. In dieser Liste werden die Menüelementbezeichnungen, ihre Reihenfolge mit Trennzeichen, ihre Zugriffsschlüssel und ihre Ausellipsen angezeigt. Kontextmenüs zeigen keine Tastenkombinationen an.

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

### <a name="using-ellipses"></a>Verwenden von Ellipsen

Während Menübefehle für sofortige Aktionen verwendet werden, sind möglicherweise weitere Informationen erforderlich, um die Aktion auszuführen. **Geben Sie einen Befehl an, der zusätzliche Informationen benötigt (einschließlich einer Bestätigung), indem Sie am Ende der Bezeichnung eine Auslassungszeichen hinzufügen.**

![Screenshot des Dialogfelds "Befehl drucken" und "Drucken" ](images/cmd-menus-image15.png)

In diesem Beispiel wird der Druck... -Befehl zeigt ein Dialogfeld Drucken an, um weitere Informationen zu sammeln.

**Die richtige Verwendung von Ellipsen ist wichtig, um anzugeben, dass Benutzer vor dem Ausführen der Aktion weitere Entscheidungen treffen oder die Aktion sogar vollständig abbrechen können.** Die visuellen Hinweise, die von auslassungsbaren Ellipsen geboten werden, ermöglichen es Benutzern, Ihre Software ohne Sorge zu erkunden.

**Dies bedeutet nicht, dass Sie immer dann eine Auslassungszeichen verwenden sollten, wenn eine Aktion nur dann ein anderes Fenster anzeigt,** wenn zusätzliche Informationen zum Ausführen der Aktion erforderlich sind. Beispielsweise müssen die Befehle Info, Erweitert, Hilfe, Optionen, Eigenschaften und Einstellungen beim Klicken auf ein anderes Fenster anzeigen, benötigen jedoch keine zusätzlichen Informationen vom Benutzer. Daher benötigen sie keine Auslassungselpsen.

**Entscheiden Sie bei Mehrdeutigkeit (z. B. wenn die Befehlsbezeichnung kein Verb aufgibt) basierend auf der wahrscheinlichsten Benutzeraktion.** Wenn das einfache Anzeigen des Fensters eine gängige Aktion ist, verwenden Sie keine Auslassungszeichen.

**Richtig:**

Weitere Farben...

Versionsinformationen

Im ersten Beispiel wählen Benutzer höchstwahrscheinlich eine Farbe aus, sodass die Verwendung einer Ellipse richtig ist. Im zweiten Beispiel zeigen Benutzer höchstwahrscheinlich die Versionsinformationen an, sodass Ausellipsen nicht erforderlich sind.

> [!Note]  
> Wenn Sie feststellen, ob ein Menübefehl auslassungszeichen erfordert, verwenden Sie nicht die Notwendigkeit, Berechtigungen als Faktor zu [erhöhen.](winenv-uac.md)

 

Erhöhte Rechte sind keine Informationen, die zum Ausführen eines Befehls erforderlich sind (stattdessen für die Berechtigung), und die Notwendigkeit, erhöhte Rechte zu erhöhen, wird mit dem Sicherheitsschild angegeben.

## <a name="labels"></a>Bezeichnungen

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie bei Bedarf großgeschriebene Titel verwenden, um die Kombination von Groß-/Großschreibungsstilen zu vermeiden.

### <a name="menu-category-names"></a>Namen der Menükategorie

-   **Verwenden Sie Menükategorienamen, bei denen es sich um Einzelwortverben oder -nomen handelt.** Eine Bezeichnung mit mehreren Wörtern kann bei zwei Ein-Wort-Bezeichnungen verwechselt werden.
-   **Verbbasierte Menünamen bevorzugen.** Lassen Sie das Verb jedoch aus, wenn es "Erstellen", "Anzeigen", "Anzeigen" oder "Verwalten" lautet. Beispielsweise haben die folgenden Menükategorien keine Verben:
    -   Tabelle
    -   Tools
    -   Fenster
-   Verwenden Sie für nicht standardmäßige Kategorienamen **ein einzelnes, spezifisches Wort, das den Menüinhalt klar und genau beschreibt.** Obwohl die Namen nicht so allgemein sein müssen, dass sie alles im Menü beschreiben, sollten sie vorhersagbar genug sein, damit Benutzer nicht von dem, was sie im Menü finden, überrascht werden.

### <a name="menu-item-names"></a>Menüelementnamen

-   **Verwenden Sie Menüelementnamen, die mit einem Verb,Nomen oder Nomen-Ausdruck beginnen.**
-   **Verbbasierte Menünamen bevorzugen.** Lässt das Verb jedoch aus, wenn:
    -   **Das Verb ist "Create", "Show", "View" oder "Manage".** Die folgenden Befehle haben z. B. keine Verben:
        -   Info
        -   Fortgeschrittene
        -   Vollbildmodus
        -   Neu
        -   Tastatur
        -   Eigenschaften
    -   **Das Verb entspricht dem Namen der Menükategorie, um Wiederholungen zu vermeiden.** Verwenden Sie beispielsweise in der Menükategorie Einfügen Text, Tabelle und Bild anstelle von Text einfügen, Tabelle einfügenund Bild einfügen.
-   **Verwenden Sie bestimmte Verben.** Vermeiden Sie generische, nicht hilfreiche Verben wie Change und Manage.
-   **Verwenden Sie singulare Nomen für Befehle, die für ein einzelnes Objekt gelten.** Verwenden Sie andernfalls Plural nomen.
-   **Verwenden Sie bei Bedarf Modifizierer, um zwischen ähnlichen Befehlen zu unterscheiden.** Beispiele: Zeile oben einfügen, Zeile unten einfügen.
-   **Wählen Sie für Paare ergänzender Befehle eindeutig ergänzende Namen aus.** Beispiele: Hinzufügen, Entfernen; Einblenden, Ausblenden; Einfügen, Löschen.
-   **Wählen Sie Die Namen von Menüelements basierend auf Benutzerzielen und -aufgaben aus, nicht basierend auf der Technologie.**

**Richtig:**

![Screenshot des Menüs "Rip" mit Menüelement "Format" ](images/cmd-menus-image16.png)

**Falsch:**

![Screenshot des Menüs "Rip" mit Codecmenüelement ](images/cmd-menus-image17.png)

Im falschen Beispiel basiert das Menüelement auf seiner Technologie.

-   Verwenden Sie die folgenden Menüelementnamen für den angegebenen Zweck:
    -   **Optionen** So zeigen Sie Programmoptionen an
    -   **Anpassen** Um die Programmoptionen anzuzeigen, die sich speziell auf die Konfiguration der maschinellen Benutzeroberfläche beziehen.
    -   **Personalisieren** So zeigen Sie eine Zusammenfassung der häufig [verwendeten Personalisierungseinstellungen](glossary.md) an.
    -   **Einstellungen** Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.
    -   **Eigenschaften** So zeigen Sie das Eigenschaftenfenster eines Objekts an.
    -   **Einstellungen** Verwenden Sie nicht als Menübezeichnung. Verwenden Sie stattdessen Optionen.

### <a name="submenu-names"></a>Untermenünamen

-   **Menüelemente, die Untermenüs anzeigen, verfügen nie über Auslassungspunkte in ihrer Bezeichnung.** Der Untermenüpfeil gibt an, dass eine andere Auswahl erforderlich ist.

**Falsch:**

![Screenshot des neuen Menüelements mit Auslassungszeichen ](images/cmd-menus-image18.png)

In diesem Beispiel weist das Menüelement Neu fälschlicherweise die Auslassungszeichen auf.

## <a name="documentation"></a>Dokumentation

Beim Verweisen auf Menüs:

-   Informationen zu Befehlen, die Menüs anzeigen oder ausblenden, finden Sie unter Menüleisten. Sie werden nicht als klassische Menüs bezeichnet.
-   Verweisen Sie anhand ihrer Bezeichnungen auf Menüs. Verwenden Sie den genauen Bezeichnungstext, einschließlich der Groß-/Großschreibung, aber nicht den Zugriffsschlüsselunterstrich oder die Auslassungszeichen.
-   Um auf Menükategorien zu verweisen, verwenden Sie "Im <category name> Menü". Wenn der Speicherort eines Menüelements aus dem Kontext klar ist, müssen Sie die Menükategorie nicht erwähnen.
-   Um die Benutzerinteraktion von Menüelementen zu beschreiben, verwenden Sie klicken, ohne das Wort Menü oder Befehl. Verwenden Sie nicht "Auswählen", "Auswählen" oder "Auswählen". Verweisen Sie nur in der technischen Dokumentation auf ein Menüelement als Menüelement.
-   Um das Entfernen eines Häkchens aus einer Menüoption zu beschreiben, verwenden Sie klicken, um das Häkchen zu entfernen. Verwenden Sie nicht clear.
-   Verweisen Sie auf Kontextmenüs als Kontextmenüs, nicht als Kontextmenüs.
-   Verwenden Sie keine Cascading-, Pull-Down-, Dropdown- oder Popupmenüs, um Menüs zu beschreiben, außer in der Programmierdokumentation.
-   Beziehen Sie sich auf nicht verfügbare Menüelemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder grau. Verwenden Sie disabled in der Programmierdokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mit fett formatiertem Text. Andernfalls setzen Sie die Bezeichnungen nur in Anführungszeichen, wenn dies erforderlich ist, um Verwechslungen zu vermeiden.

Beispiele:

-   Klicken Sie im Menü **Datei** auf **Drucken,** um das Dokument zu drucken.
-   Zeigen **Sie** im Menü Ansicht auf **Symbolleisten**, und klicken Sie dann auf **Formatieren.**

 

