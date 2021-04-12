---
title: Menüs (Entwurfs Grundlagen)
description: Menüs sind hierarchische Listen von Befehlen oder Optionen, die für Benutzer im aktuellen Kontext verfügbar sind.
ms.assetid: 3772ff8e-8057-476d-b62b-efbd5e07907f
ms.topic: article
ms.date: 10/20/2020
ms.openlocfilehash: 8054a01e4198f3592a34ae09635dd60f392da1eb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "104218936"
---
# <a name="menus-design-basics"></a>Menüs (Entwurfs Grundlagen)

> [!NOTE]
> Dieses Entwurfs Handbuch wurde für Windows 7 erstellt und wurde für neuere Versionen von Windows nicht aktualisiert. Ein Großteil der Anleitungen gilt weiterhin im Prinzip, aber die Präsentation und die Beispiele entsprechen nicht unseren [aktuellen Entwurfs Anleitungen](/windows/uwp/design/).

Menüs sind hierarchische Listen von Befehlen oder Optionen, die für Benutzer im aktuellen Kontext verfügbar sind.

Dropdown Menüs sind Menüs, die bei Bedarf angezeigt werden, wenn Sie mit der Maus darauf zeigen. Sie sind in der Regel in der Ansicht ausgeblendet und stellen daher eine effiziente Möglichkeit zur Erhaltung des Bildschirm Raums dar. Ein Untermenü oder ein kaskadierungmenü ist ein sekundäres Menü, das bei Bedarf von einem Menü aus angezeigt wird. Sie werden durch einen Pfeil am Ende der unter Menü Bezeichnung angegeben. Bei einem Menü Element handelt es sich um einen einzelnen Befehl oder eine Option in einem Menü.

Menüs werden häufig in einer Menüleiste angezeigt. Hierbei handelt es sich um eine Liste von beschrifteten Menü Kategorien, die sich in der Regel am oberen Rand eines Fensters befinden. Im Gegensatz dazu wird ein Kontextmenü angezeigt, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, das ein Kontextmenü unterstützt.

![Screenshot der Menüleiste mit Menü und Untermenü ](images/cmd-menus-image1.png)

Eine typische Menüleiste, in der ein Dropdown Menü und ein Untermenü angezeigt werden.

> [!Note]  
> Richtlinien, die sich auf [Befehls](ctrl-command-buttons.md)Schaltflächen, [Symbolleisten](cmd-toolbars.md)und [Tastatur](inter-keyboard.md) beziehen, werden in separaten Artikeln dargestellt.

 

## <a name="usage-patterns"></a>Verwendungsmuster

Menüs haben mehrere Verwendungs Muster:



|                                                                                                                                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Menüleisten**<br/> in einer Menüleiste werden Befehle und Optionen in Dropdown Menüs angezeigt. <br/>                                               | Menüleisten sind häufig und leicht zu finden sowie eine effiziente Verwendung von Speicherplatz. <br/> ![Screenshot der Menüleiste mit dem Dropdown Menü ](images/cmd-menus-image2.png)<br/> Eine Menüleiste von Windows Mail.<br/>                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Symbolleisten Menüs**<br/> eine Menüleiste, die als Symbolleiste implementiert ist. <br/>                                                                   | Symbolleisten Menüs sind Symbolleisten, die hauptsächlich aus Befehlen in [Menü](ctrl-command-buttons.md) Schaltflächen und Trenn Schaltflächen bestehen, bei denen es sich nur um einige direkte Befehle handelt. <br/> ![Screenshot des Symbolleisten Menüs mit Dropdown Menü ](images/cmd-menus-image3.png)<br/> Ein Symbolleisten Menü in der Windows-Fotogalerie.<br/> Richtlinien zu diesem Muster finden Sie unter [Symbolleisten](cmd-toolbars.md).<br/>                                                                                                                                                                                                             |
| **Registerkarten Menüs**<br/> Schaltflächen innerhalb von Registerkarten, auf denen ein kleiner Satz von Befehlen und Optionen angezeigt wird, die sich auf eine Registerkarte in einem Dropdown Menü beziehen. <br/> | Registerkarten mit Menüs sehen wie normale Registerkarten mit Ausnahme des unteren Teils eine Schaltfläche mit einem Dropdown Pfeil. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdown Menü angezeigt, anstatt die Registerkarte auszuwählen. <br/> ![Screenshot des Registerkarten Menüs mit Dropdown Menü ](images/cmd-menus-image4.png)<br/> Registerkarten Menüs werden in Windows-Media Player verwendet.<br/>                                                                                                                                                                                                                                                                                           |
| **Menü Schaltflächen**<br/> Befehls Schaltflächen, die einen kleinen Satz verwandter Befehle in einem Dropdown Menü anzeigen. <br/>                       | [Menü](ctrl-command-buttons.md) Schaltflächen sehen wie normale Befehls Schaltflächen aus, mit der Ausnahme, dass Sie einen Dropdown Pfeil enthalten. Wenn Sie auf die Schaltfläche klicken, wird ein Dropdown Menü angezeigt, anstatt einen Befehl auszuführen.<br/> unter [teilte Schalt](ctrl-command-buttons.md) Flächen ähneln Menü Schaltflächen, mit dem Unterschied, dass Sie Variationen eines Befehls sind, und durch Klicken auf den linken Bereich der Schaltfläche wird die Aktion direkt auf der Bezeichnung ausgeführt.<br/> ![Screenshot der Menü Schaltfläche mit Dropdown Befehlen ](images/cmd-menus-image5.png)<br/> Eine Menü Schaltfläche mit einem kleinen Satz verwandter Befehle.<br/> |
| **Kontextmenüs**<br/> Dropdown Menüs, in denen ein kleiner Satz von Befehlen und Optionen angezeigt wird, die sich auf den aktuellen Kontext beziehen. <br/>       | Dropdown Menü für Kontextmenüs, wenn Benutzer mit der rechten Maustaste auf ein Objekt oder einen Fensterbereich klicken, der ein Kontextmenü unterstützt. <br/> ![Screenshot des Kontextmenüs, das Befehle anzeigt ](images/cmd-menus-image6.png)<br/> ein Kontextmenü von Windows-Explorer.<br/> Wenn Kontextmenüs die beste Menüoption sind, Sie jedoch eine Lösung benötigen, die für alle Benutzer geeignet ist, können Sie eine Dropdown-Schaltfläche für das Dropdown Menü verwenden. <br/> ![Screenshot des Fotos mit Dropdown Menü Schaltfläche ](images/cmd-menus-image7.png)<br/> Ein Kontextmenü, das mit einer Dropdown Schaltfläche für Menüs sichtbar gemacht wird.<br/>                                                   |
| **Aufgabenbereich-Menüs**<br/> ein kleiner Satz von Befehlen im Zusammenhang mit dem ausgewählten Objekt-oder Programmmodus. <br/>                              | im Gegensatz zu Kontextmenüs werden Sie automatisch innerhalb eines Fenster Bereichs angezeigt, anstatt bei Bedarf. <br/> ![Screenshot des Fotos mit dem Menü "Aufgabenbereich" auf der rechten Seite ](images/cmd-menus-image8.png)<br/> Ein Aufgabenbereich-Menü aus dem Windows Photo Gallery Viewer.<br/>                                                                                                                                                                                                                                                                                                                                                         |



 

## <a name="is-this-the-right-user-interface"></a>Handelt es sich um die richtige Benutzeroberfläche?

Orientieren Sie sich an folgenden Fragen:

### <a name="menu-bars"></a>Menüleisten

Wenden Sie die folgenden Bedingungen an:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es viele Menü Elemente?
-   Gibt es viele Menü Kategorien?
-   Gelten die meisten Menü Elemente für das gesamte Programm und das primäre Fenster?
-   Muss das Menü für alle Benutzer funktionieren?

Wenn dies der Fall ist, sollten Sie eine Menüleiste verwenden.

### <a name="toolbar-menus"></a>Symbolleisten Menüs

Wenden Sie die folgenden Bedingungen an:

-   Ist das Fenster ein primäres Fenster?
-   Hat das Fenster eine Symbolleiste?
-   Gibt es nur wenige Menü Kategorien?
-   Muss das Menü für alle Benutzer funktionieren?

Wenn dies der Fall ist, sollten Sie ein Symbolleisten Menü anstelle von oder zusätzlich zu einer Menüleiste verwenden.

### <a name="tab-menus"></a>Registerkarten Menüs

Wenden Sie die folgenden Bedingungen an:

-   Ist das Fenster ein primäres Fenster?
-   Verfügt das Fenster über Registerkarten, wobei jede Registerkarte für eine dedizierte Gruppe von Aufgaben verwendet wird (im Gegensatz zur Verwendung von Registerkarten zum Anzeigen unterschiedlicher Ansichten)?
-   Gibt es eine Menükategorie, die für jede Registerkarte gilt?
-   Gibt es viele Befehle und Optionen, aber nur eine kleine Gruppe für jede Registerkarte?

Wenn dies der Fall ist, sollten Sie ein Registerkarten Menü anstelle einer Menüleiste verwenden.

### <a name="context-menu"></a>Kontextmenü

Wenden Sie die folgenden Bedingungen an:

-   Gibt es einen kleinen Satz kontextbezogener Befehle und Optionen, die für das ausgewählte Objekt oder den ausgewählten Fensterbereich gelten?
-   Sind diese Menü Elemente redundant?
-   Sind die Ziel Benutzer mit Kontextmenüs vertraut?

Wenn dies der Fall ist, sollten Sie Kontextmenüs für die Objekte und Fensterbereiche bereitstellen, die diese benötigen.

Bei browserbasierten Programmen sind Menüs im Aufgabenbereich eine gängigste Lösung für kontextabhängige Befehle. Derzeit erwarten Benutzer, dass Kontextmenüs in browserbasierten Programmen generisch und nicht hilfreich sind.

### <a name="task-pane-menu"></a>Menü "Aufgabenbereich"

Wenden Sie die folgenden Bedingungen an:

-   Ist das Fenster ein primäres Fenster?
-   Gibt es einen kleinen Satz kontextbezogener Befehle und Optionen, die für das ausgewählte Objekt oder den Programmmodus gelten?
-   Gibt es einige Menü Kategorien?
-   Muss das Menü für alle Benutzer funktionieren?

Wenn dies der Fall ist, sollten Sie anstelle eines Kontextmenüs ein Menü im Aufgabenbereich verwenden.

## <a name="design-concepts"></a>Entwurfskonzepte

Effektive Menüs, die eine gute Benutzer Darstellung fördern:

-   Verwenden Sie eine Befehls Darstellung, die dem Programmtyp, den Fenstertypen, der Befehls Verwendung und den Ziel Benutzern entspricht.
-   Sie sind gut organisiert und verwenden Standardmenü Organisation, wenn dies angebracht ist.
-   Verwenden Sie Menüleisten, Symbolleisten und Kontextmenüs effektiv.
-   Verwenden Sie Symbole effektiv.
-   Verwenden Sie Zugriffsschlüssel und Tastenkombinationen.

**Wenn Sie nur eine Aktion ausführen...**

Wählen Sie eine Befehls Darstellung aus, die dem Programmtyp, den Fenstertypen, der Befehls Verwendung und den Ziel Benutzern entspricht.

## <a name="guidelines"></a>Richtlinien

### <a name="general"></a>Allgemein

-   **Alle Menü Muster außer Menüleisten benötigen einen Dropdown Pfeil, um anzuzeigen, dass ein Pulldownmenü vorhanden ist.** Das vorhanden sein von Menüs läuft nicht in einer Menüleiste, aber nicht in den anderen Mustern.
-   **Ändern Sie die Namen der Menü Elemente nicht dynamisch.** Dies ist verwirrend und unerwartet. Ändern Sie z. b. die Option Hochformat nicht bei Auswahl in Querformat. Verwenden Sie für Modi stattdessen die [Zeichen-und Häkchen](#bullets-and-checkmarks) .
    -   **Ausnahme:** Sie können die Namen von Menü Elementen, die auf Objektnamen basieren, dynamisch ändern. Beispielsweise können Listen der zuletzt verwendeten Dateien oder Fensternamen dynamisch sein.

### <a name="menu-bars"></a>Menüleisten

-   **Entfernen Sie Menüleisten mit drei oder weniger Menü Kategorien.** Wenn nur wenige Befehle vorhanden sind, bevorzugen Sie leichtere Alternativen wie z. b. Symbolleisten Menüs oder weitere direkte Alternativen, wie z. b. Befehls Schaltflächen und Links.
-   **Sie haben nicht mehr als 10 Menü Kategorien.** Zu viele Menü Kategorien sind überwältigend und machen die Menüleiste schwer zu verwenden.
-   Sie **sollten die Menüleiste** ausblenden, wenn die Symbolleiste oder die direkt Befehle fast alle Befehle bereitstellen, die von den meisten Benutzern benötigt werden. Hiermit wird Benutzern ermöglicht, eine Menüleisten-Kontrollkästchen-Option in einem Symbolleisten Menü anzuzeigen oder auszublenden.

![Screenshot der Optionsliste mit ausgewählter Menüleiste ](images/cmd-menus-image9.png)

In diesem Beispiel stellt Windows Internet Explorer eine Menüleisten Option bereit.

Weitere Informationen finden Sie unter Ausblenden von [Menüleisten](#hiding-menu-bars).

### <a name="hiding-menu-bars"></a>Ausblenden von Menüleisten

Im Allgemeinen funktionieren Symbolleisten hervorragend zusammen mit Menüleisten, da beide die Möglichkeit haben, sich ohne Kompromisse auf ihre Stärken zu konzentrieren.

-   Blendet die Menüleiste standardmäßig aus, wenn der Symbolleisten Entwurf eine Menüleiste redundant macht.
-   Blenden Sie die Menüleiste aus, anstatt sie vollständig zu entfernen, da Menüleisten für Tastatur Benutzer besser zugänglich sind.
-   Um die Menüleiste wiederherzustellen, geben Sie eine Menüleisten-Kontrollkästchen-Option in der Ansicht (für primäre Symbolleisten) oder Tools (für sekundäre Symbolleisten) an. Weitere Informationen finden Sie unter [Standard Menü und unterteilte Schalt](cmd-toolbars.md)Flächen.

### <a name="menu-categories"></a>Menü Kategorien

-   **Wählen Sie einzelne Word-Namen für Menü Kategorien aus.** Durch die Verwendung mehrerer Wörter wird die Trennung zwischen Kategorien verwirrend.
-   **Verwenden Sie für Programme, die Dokumente erstellen oder anzeigen, die Standardmenü Kategorien** , z. b. Datei, bearbeiten, anzeigen, Tools und Hilfe. Dadurch werden allgemeine Menü Elemente vorhersagbar und leichter zu finden.
-   **Berücksichtigen Sie bei anderen Programmtypen die Organisation ihrer Befehle und Optionen in nützlicheren, natürlichen Kategorien,** die auf dem Zweck des Programms basieren, und die Art und Weise, wie Benutzer ihre Aufgaben und Ziele vorstellen. Fühlen Sie sich nicht verpflichtet, die Standardmenü Organisation zu verwenden, wenn Sie nicht für Ihr Programm geeignet ist.
-   **Wenn Sie sich für die Verwendung nicht standardmäßiger Menü Kategorien entscheiden, müssen Sie gute Kategorienamen auswählen.** Weitere Informationen finden Sie im Abschnitt [Bezeichnungen](#labels) .
-   **Bevorzugen von aufgabenorientierten Menü Kategorien gegenüber generischen Kategorien.** Aufgabenorientierte Kategorien machen Menü Elemente leichter zu finden.

![Screenshot der Menüleiste mit RIP, Burn und Sync ](images/cmd-menus-image10.png)

In diesem Beispiel verwendet Windows Media Player aufgabenorientierte Menü Kategorien.

-   **Vermeiden Sie Menü Kategorien mit nur einem oder zwei Menü Elementen.** Wenn sinnvoll, konsolidieren Sie mit anderen Menü Kategorien, möglicherweise mit einem Untermenü.
-   **Sie sollten dasselbe Menü Element in mehreren Kategorien nur dann platzieren, wenn Folgendes gilt:**
    -   Das Menü Element gehört logisch zu mehreren Menü Kategorien.
    -   Es werden Daten angezeigt, die zeigen, dass Benutzer Probleme beim Suchen des Elements in einer einzelnen Menükategorie haben.
    -   In mehreren Kategorien sind nur ein oder zwei fest zusuchende Menü Elemente vorhanden.
-   **Legen Sie keine unterschiedlichen Menü Elemente fest, die denselben Namen in mehreren Kategorien verwenden.** Sie haben z. b. keine unterschiedlichen Menü Elemente für Optionen in mehreren Kategorien.
    -   **Ausnahme:** Das Registerkarten-Menü Muster kann unterschiedliche Optionen und Hilfe Menü Elemente in jedem Registerkarten Menü enthalten.

![Screenshot von Registerkarten Menüs mit wiederholten Menü Elementen ](images/cmd-menus-image11.png)

In diesem Beispiel enthält Windows Media Player Optionen und Hilfe Menü Elemente in jedem Registerkarten Menü.

### <a name="menu-item-organization-and-order"></a>Menü Element Organisation und-Reihenfolge

-   **Ordnen Sie die Menü Elemente in Gruppen von sieben oder weniger stark verwandten Elementen an.** Hierzu zählen Untermenüs als einzelnes Menü Element im übergeordneten Menü.
-   **Fügen Sie nicht mehr als 25 Elemente innerhalb einer einzelnen Menü Ebene ein** (ohne Untermenüs).
-   **Legen Sie Trennzeichen zwischen den Gruppen innerhalb eines Menüs ab.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.
-   **Fügen Sie die Gruppen in einem Menü in ihre logische Reihenfolge ein.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Gruppen.
-   **Fügen Sie die Elemente innerhalb einer Gruppe in ihre logische Reihenfolge ein.** Wenn keine logische Reihenfolge vorhanden ist, platzieren Sie zuerst die am häufigsten verwendeten Elemente. Numerische Elemente (z. b. Zoom Prozentsätze) in numerischer Reihenfolge einfügen.

### <a name="submenus"></a>Submenus

-   **Vermeiden Sie unnötige Verwendung von Untermenüs.** Die Verwendung von Untermenüs erfordert mehr physischen Aufwand, und das Auffinden der Menü Elemente ist im allgemeinen schwieriger.
-   **Fügen Sie häufig verwendete Menü Elemente nicht in einem Untermenü ein.** Dies würde dazu führen, dass die Verwendung dieser Befehle ineffizient ist. Sie können jedoch häufig verwendete Befehle in einem Untermenü platzieren, wenn Sie normalerweise direkt auf Sie zugreifen, z. b. mit einer Symbolleiste.
-   **Verwenden Sie ein Untermenü, wenn Folgendes gilt:**
    -   Dadurch wird das übergeordnete Menü vereinfacht, da es über viele Elemente (20 oder mehr) verfügt, oder das Untermenü gehört zu einer Gruppe von mehr als sieben Elementen.
    -   Die Elemente im Untermenü werden weniger häufig als die Elemente im übergeordneten Menü verwendet.
    -   Das Untermenü würde drei oder mehr Elemente enthalten.
    -   Es gibt drei oder mehr Befehle, die mit demselben Wort beginnen. Verwenden Sie in diesem Fall dieses Wort als unter Menü Bezeichnung.

![Screenshot des Menüs "neu" mit vier unter Menü Elementen ](images/cmd-menus-image12.png)

In diesem Beispiel ersetzt das neue Untermenü separate Befehle für eine neue e-Mail-Nachricht, eine neue Nachricht, einen neuen Ordner und einen neuen Kontakt.

-   **Verwenden Sie maximal drei Ebenen von Menüs.** Das heißt, Sie können über ein primäres Menü und höchstens zwei Ebenen von Untermenüs verfügen. Zwei Ebenen von Untermenüs sollten selten vorkommen.

### <a name="presentation"></a>Präsentation

-   **Deaktivieren Sie Menü Elemente, die nicht auf den aktuellen Kontext angewendet werden,** anstatt Sie zu entfernen. Dadurch werden Menüleisten Inhalte stabil und leichter zu finden. **Ausnahmen:**
    -   Entfernen Sie für Kontextmenü Kategorien **anstelle von Kontextmenü Elementen, die nicht auf den aktuellen Kontext angewendet werden.** Eine Menükategorie ist kontextbezogen, wenn Sie nur für bestimmte Modi angezeigt wird, z. b. Wenn ein bestimmter Objekttyp ausgewählt wird. Weitere Informationen finden Sie in den Richtlinien zum [Entfernen und deaktivieren](#context-menus) von Kontextmenüs.
    -   Wenn Sie feststellen, wann ein Menü Element deaktiviert werden soll, wird das Menü Element aktiviert, und bei Bedarf wird die Auswahl in einer Fehlermeldung angezeigt.

### <a name="tab-menus"></a>Registerkarten Menüs

-   **Jedes Registerkarten Menü kann kontextspezifische Optionen und Hilfe Menü Elemente enthalten.** Dies steht im Gegensatz zu allen anderen Menü Mustern. Jede Registerkarte wird für eine dedizierte Gruppe von Aufgaben verwendet, sodass jede Redundanz über Registerkarten Menüs nicht verwirrend ist.

### <a name="context-menus"></a>Kontextmenüs

-   **Verwenden Sie Kontextmenüs nur für kontextabhängige Befehle und Optionen.** Die Menü Elemente sollten nur auf das ausgewählte (oder angeklickte) Objekt oder den Fensterbereich, nicht auf das gesamte Programm angewendet werden.
-   **Stellen Sie Befehle nicht nur über Kontextmenüs zur Verfügung.** Kontextmenüs sind wie Tastenkombinationen eine alternative Möglichkeit, Befehle auszuführen und Optionen auszuwählen. Beispielsweise ist ein Eigenschaften Befehl auch über die Menüleiste oder die Tastenkombination Alt + Eingabe verfügbar.
-   **Stellen Sie Kontextmenüs für alle Objekte und Fensterbereiche bereit** , die von einem kleinen Satz kontextbezogener Befehle und Optionen profitieren. Viele Benutzer klicken regelmäßig mit der rechten Maustaste und erwarten Kontextmenüs an beliebiger Stelle.
-   **Verwenden Sie ggf. eine Dropdown-Schaltfläche für Menüs für Kontextmenüs, die für alle Benutzer vorgesehen sind.** Normalerweise eignen sich Kontextmenüs für Befehle und Optionen, die auf Erweiterte Benutzer ausgerichtet sind. Sie können jedoch eine Dropdown Schaltfläche für Menüs verwenden, wenn Kontextmenüs die beste Menüoption sind und Sie alle Benutzer als Ziel festlegen müssen.

![Screenshot des Fotos mit Dropdown Menü Schaltfläche ](images/cmd-menus-image7.png)

In diesem Beispiel wird eine Dropdown-Schaltfläche für Menüs verwendet, um ein Kontextmenü sichtbar zu machen.

**Menü Element Organisation und-Reihenfolge**

-   **Ordnen Sie die Menü Elemente in Gruppen von sieben oder weniger stark verwandten Elementen an.**
-   **Vermeiden Sie die Verwendung von Untermenüs** , um Kontextmenüs einfach, direkt und effizient zu halten.
-   **Fügen Sie nicht mehr als 15 Elemente in einem Kontextmenü ein.**
-   **Legen Sie Trennzeichen zwischen den Gruppen innerhalb eines Menüs ab.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.
-   **Stellen Sie Menü Elemente in der folgenden Reihenfolge zur Verfügung:**

<dl> Primäre Befehle (am häufigsten verwendet)<dl> Öffnen  
Ausführen  
Abspielen  
Gedruck <separator>  
</dl> </dd> <dd>Sekundäre Befehle, die vom Objekt unterstützt werden<dl> <separator>  
</dl> </dd> Übertragungs Befehle<dl> Ausschneiden  
Kopieren  
Kle <separator>  
</dl> </dd> <dd>Objekt Einstellungen<dl> <separator>  
</dl> </dd> Objekt Befehle<dl> Löschen  
Benen <separator>  
Eigenschaften
</dl> </dd> </dl>

**Präsentation**

-   **Zeigen Sie den Standardbefehl mithilfe von Fett an.** Wenn dies praktikabel ist, machen Sie es auch zum ersten Menü Element. Der Standardbefehl wird aufgerufen, wenn Benutzer auf ein Objekt doppelklicken oder ein Objekt auswählen und die EINGABETASTE drücken.
-   **Entfernen Sie anstelle von Kontextmenü Elementen, die nicht auf den aktuellen Kontext angewendet werden.** Dadurch werden Kontextmenüs kontextbezogen und effizient.
    -   **Ausnahme:** Deaktivieren Sie Menü Elemente, die nicht angewendet werden, wenn eine angemessene Annahme besteht, dass Sie verfügbar sein müssen:
        -   Sie haben immer die relevanten standardmäßigen Kontextmenü Befehle, z. b. Ausschneiden, kopieren, einfügen, löschen und umbenennen.
        -   Immer über die Befehle verfügen, mit denen Verwandte Sätze vervollständigt werden. Wenn z. b. ein Back vorhanden ist, sollte auch ein vorwärts vorhanden sein. Wenn eine Ausschneide vorhanden ist, haben Sie immer eine Kopie und einen Kopiervorgang.

### <a name="bullets-and-checkmarks"></a>Aufzählungen und Häkchen

-   **Menü Elemente, die Optionen sind, können Aufzählungs Zeichen und Häkchen verwenden.** Befehle sind möglicherweise nicht möglich.
-   **Wählen Sie eine Option aus einer kleinen Gruppe von sich gegenseitig ausschließenden Optionen aus.** In einer Gruppe sollten immer mindestens zwei Aufzählungen vorhanden sein. Weitere Informationen finden Sie unter Options [Felder.](ctrl-radio-buttons.md)
-   **Verwenden Sie ein Häkchensymbol, um eine unabhängige Einstellung ein-oder auszuschalten.** Wenn die ausgewählten und gelöschten Zustände nicht klar und eindeutige Gegensätze sind, verwenden Sie stattdessen eine Reihe von Aufzählungs Zeichen. Weitere Informationen finden Sie unter [Kontrollkästchen](ctrl-check-boxes.md).
-   **Wenn Sie einen gemischten Prüfzeichen Zustand haben, zeigen Sie ein Menü Element ohne Häkchensymbol an.** Der gemischte Zustand wird für Mehrfachauswahl verwendet, um anzugeben, dass die Option für einige, aber nicht für alle Objekte festgelegt ist, sodass jedes einzelne Objekt entweder den Status "aktiviert" oder "deaktiviert" aufweist. Der gemischte Zustand wird nicht als dritter Zustand eines einzelnen Elements verwendet.
-   **Fügen Sie Trennzeichen zwischen den zugehörigen Sätzen von Häkchen oder Aufzählungs Zeichen ein.** Ein Trennzeichen ist eine einzelne Zeile, die die Breite des Menüs umfasst.

### <a name="icons"></a>Symbole

-   **Erwägen Sie in folgenden Fällen Symbole für die Menüpunkte einzurichten:**
    -   Die am häufigsten verwendeten Menü Elemente.
    -   Menü Elemente, deren Symbol Standard und bekannt ist.
    -   Menüpunkte, deren Funktion auf einfache Weise mit einem Symbol veranschaulicht werden kann.
-   **Wenn Sie Symbole verwenden, sind Sie nicht verpflichtet, Sie für alle Menü Elemente anzugeben.** Kryptische Symbole sind nicht hilfreich, machen das Menü unübersichtlich und hindern Benutzer daran, wichtige Menüpunkte einfach aufzufinden.

![Screenshot von Menü Elementen mit und ohne Symbole ](images/cmd-menus-image13.png)

In diesem Beispiel enthält das Menü organisieren nur Symbole für die am häufigsten verwendeten Menü Elemente.

-   **Stellen Sie sicher, dass die Menü Symbole den Aero-Style-Symbol Richtlinien entsprechen.**

Weitere Informationen und Beispiele finden Sie unter [Symbole](vis-icons.md).

### <a name="access-keys"></a>Zugriffsschlüssel

-   **Weisen Sie allen Menü Elementen Zugriffstasten zu.** Keine Ausnahmen.
-   **Weisen Sie nach Möglichkeit Zugriffsschlüssel für häufig verwendete Befehle gemäß den Standard Zuordnungen für Zugriffsschlüssel zu.** Obwohl konsistente Zugriffsschlüssel Zuweisungen nicht immer möglich sind, werden Sie sicherlich bevorzugt, insbesondere für häufig verwendete Befehle.
-   **Für dynamische Menü Elemente (z. b. zuletzt verwendete Dateien) weisen Sie Zugriffsschlüssel numerisch zu.**

![Screenshot von Menü Elementen mit numerischen Zugriffs Schlüsseln ](images/cmd-menus-image14.png)

In diesem Beispiel weist das Paint-Programm in Windows den kürzlich verwendeten Dateien numerische Zugriffstasten zu.

-   **Zuweisen von eindeutigen Zugriffs Schlüsseln innerhalb einer Menü Ebene.** Sie können Zugriffsschlüssel über verschiedene Menüebenen hinweg wieder verwenden.
-   **Machen Sie Zugriffsschlüssel leicht zu finden:**
    -   Wählen Sie für die am häufigsten verwendeten Menü Elemente die Zeichen am Anfang des ersten oder zweiten Worts der Bezeichnung aus, vorzugsweise das erste Zeichen.
    -   Wählen Sie für weniger häufig verwendete Menü Elemente Buchstaben aus, die eine unterschiedliche konsonante oder einen Vokal in der Bezeichnung darstellen.
-   **Zeichen mit breiter Breite** (z. b. w, m und Großbuchstaben) bevorzugen.
-   **Bevorzugen Sie einen unverwechselbaren Konsonanten oder einen vowel,** z. b. "x" in "Exit".
-   **Vermeiden Sie die Verwendung von Zeichen, die die Unterstreichung schwer zu erkennen machen,** wie z. b. (vom problematischsten bis zum geringsten problematischen)
    -   Buchstaben, die nur ein Pixel breit sind, z. b. i und l.
    -   Buchstaben mit Nachfolger, wie z. b. g, j, p, q und y.
    -   Buchstaben neben einem Buchstaben mit einem descender.

Weitere Richtlinien und Beispiele finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="shortcut-keys"></a>Tastenkombinationen

-   **Zuweisen von Tastenkombinationen zu den am häufigsten verwendeten Menü Elementen.** Nicht häufig verwendete Menü Elemente benötigen keine Tastenkombinationen, da Benutzer stattdessen Zugriffstasten verwenden können.
-   **Stellen Sie keine Tastenkombination als einzige Möglichkeit zum Ausführen einer Aufgabe dar.** Benutzer sollten auch die Maus oder die Tastatur mit Tab, Pfeil und Zugriffstasten verwenden können.
-   **Verwenden Sie die Standard Zuweisungen für bekannte Tastenkombinationen.**
-   **Weisen Sie bekannten Tastenkombinationen keine unterschiedlichen Bedeutungen zu.** Da Sie gespeichert werden, sind nicht konsistente Bedeutungen für bekannte Verknüpfungen frustrierend und fehleranfällig. Die von Windows-Programmen verwendeten, bekannten Tastenkombinationen finden Sie untertasten Kombinationen für Windows.
-   **Versuchen Sie nicht, systemweite Programm-Tastenkombinationen zuzuweisen.** Die Tastenkombinationen des Programms werden nur wirksam, wenn das Programm den Eingabefokus besitzt.
-   **Dokumentieren Sie alle Tastenkombinationen.** Dies hilft Benutzern dabei, die Tastenkombinationen zu erlernen.
    -   **Ausnahme:** Zeigen Sie keine Tastenkombinationen für Tastenkombinationen innerhalb von Kontextmenüs an. Kontextmenüs zeigen die Tastenkombinationen nicht an, da Sie für Effizienz optimiert sind.
-   **Für nicht standardmäßige schlüsselzuweisungen:**
    -   **Wählen Sie Tastenkombinationen aus, die keine Standard Zuweisungen aufweisen.** Standardmäßige Tastenkombinationen nie neu zuweisen.
    -   **Verwenden Sie nicht standardmäßige schlüsselzuweisungen konsistent im gesamten Programm.** Weisen Sie unterschiedliche Bedeutungen nicht in unterschiedlichen Fenstern zu.
    -   **Wenn möglich, wählen Sie mnetmonische schlüsselzuweisungen aus,** insbesondere für häufig verwendete Befehle.
    -   **Verwenden Sie Funktionstasten für Befehle, die einen kleinen Effekt aufweisen,** wie z. b. Befehle, die für das ausgewählte Objekt gelten. Beispielsweise benennt F2 das ausgewählte Element um.
    -   **Verwenden Sie STRG-Tastenkombinationen für Befehle, die einen umfangreichen Effekt aufweisen,** z. b. Befehle, die für ein gesamtes Dokument gelten. Beispielsweise speichert STRG + S das aktuelle Dokument.
    -   **Verwenden Sie UMSCHALT Tastenkombinationen für Befehle, mit denen die Aktionen der Standard-Tastenkombination erweitert oder ergänzt werden.** Beispielsweise wird mit der Tastenkombination Alt + Tab die öffnenden primären Fenster durchlaufen, wohingegen Alt + Umschalt + Tab in umgekehrter Reihenfolge angezeigt wird. Ebenso zeigt F1 die Hilfe an, während UMSCHALT + F1 kontextbezogene Hilfe anzeigen.
    -   **Verwenden Sie die folgenden Zeichen nicht für Tastenkombinationen:** @ $ {} \[ \] \\  ~  \| ^ '  < >. Diese Zeichen erfordern unterschiedliche Schlüssel Kombinationen in verschiedenen Sprachen oder sind Gebiets Schema spezifisch.
    -   **Verwenden Sie STRG + ALT-Kombinationen nicht,** da Windows diese Kombination in einigen Sprachversionen als AltGr-Schlüssel interpretiert, der alphanumerische Zeichen generiert.
-   **Wenn das Programm viele Tastenkombinationen zuweist, können Sie die Zuweisungen anpassen.** Auf diese Weise können Benutzer widersprüchliche Tastenkombinationen neu zuweisen und von anderen Produkten migrieren. Die meisten Programme weisen nicht genügend Tastenkombinationen zu, um dieses Feature zu benötigen.

Weitere Richtlinien und Standard Zuweisungen für Tastenkombinationen finden Sie unter [Tastatur](inter-keyboard.md).

### <a name="standard-menus"></a>Standard Menüs

-   **Verwenden Sie die Standardmenü Organisation für Programme, die Dokumente erstellen oder anzeigen.** Die Standardmenü Organisation macht allgemeine Menü Elemente vorhersagbar und leichter zu finden.
-   **Bei anderen Programmtypen sollten Sie die Standardmenü Organisation nur verwenden, wenn es für sinnvoll ist.** Berücksichtigen Sie die Organisation ihrer Befehle und Optionen in nützlicheren, natürlichen Kategorien, die auf dem Zweck des Programms basieren, und die Art und Weise, wie Benutzer ihre Aufgaben und Ziele vorstellen.

**Standard Menüleisten**

Die Standard-Menüleisten Struktur lautet wie folgt. Diese Liste zeigt die Menükategorie und die Element Bezeichnungen, ihre Reihenfolge mit Trennzeichen, Ihren Zugriff und Ihre Tastenkombinationen und ihre Ellipsen.

<dl> File<dl> Neu STRG + N  
Öffnen Sie... STRG + O  
Schließen <separator>  
STRG + S speichern  
Speichern unter... <separator>  
Senden an <separator>  
Drucken... STRG + P  
Seitenansicht  
Seite einrichten <separator>  
1 <filename> 2 <filename> 3 <filename> ... <separator>  
Exit Alt + F4 (in der Regel nicht angegeben)
</dl> </dd> Edit<dl> Rückgängig Strg + Z  
Wiederholung STRG + Y <separator>  
Ausschneiden STRG + X  
Kopieren STRG + C  
STRG + V Einfügen <separator>  
Alle auswählen STRG + A <separator>  
ENTF löschen (in der Regel nicht angegeben) <separator>  
Suchen... STRG + F  
Nächste F3 suchen (Befehl in der Regel nicht angegeben)  
Ersetzen... STRG + H  
Gehe zu... STRG + G
</dl> </dd> View<dl> Symbolleisten  
Status Leiste <separator>  
</dl> </dd> Zoom<dl> Vergrößern Strg + +  
Vergrößern Strg +- <separator>  
Vollbild F11  
F5 aktualisieren
</dl> </dd> <dd>Tools<dl> ... <separator>  
Optionen
</dl> </dd> Hilfe<dl> <program name> Hilfe F1 <separator>  
Zu <program name>  
</dl> </dd> </dl>

**Menü Schaltflächen "Standard"**

Die standardmäßigen Symbolleisten-Menü Schaltflächen lauten wie folgt. Diese Liste zeigt die Menükategorie und die Element Bezeichnungen, ihre Reihenfolge mit Trennzeichen, Ihre Tastenkombinationen und ihre Ellipsen.

<dl> Tools<dl> Full screenF11 (Zugriffsschlüssel erneut zuweisen, wenn die Suche ebenfalls verwendet wird.)  
Symbolleisten (Beachten Sie, dass der Menüleisten Befehl hier angezeigt wird.) <separator>  
Drucken...  
Suchen... <separator>  
Zoom  
Textgröße <separator>  
Optionen
</dl> </dd> Organize<dl> Neuer folderstrg + N <separator>  
Schneide STRG + X  
Copystrg + C  
Pastectrl + V <separator>  
Wählen Sie allstrg + A <separator>  
Deletedel (in der Regel nicht angegeben)  
Benen <separator>  
Optionen
</dl> </dd> Page<dl> Neuer windowstrg + N <separator>  
Zoom  
Textgröße
</dl> </dd> </dl>

**Standard Kontextmenüs**

Die standardmäßigen Kontextmenü Inhalte lauten wie folgt. Diese Liste zeigt die Menü Element Bezeichnungen, ihre Reihenfolge mit Trennzeichen, die Zugriffstasten und die Auslassungs Punkte. Kontextmenüs zeigen keine Tastenkombinationen an.

<dl> Öffnen  
Ausführen  
Abspielen  
Bearbeiten  
Drucken... <separator>  
Ausschneiden  
Kopieren  
Kle <separator>  
Löschen  
Benen <separator>  
Sperren Sie das <object name> (Häkchen).  
Eigenschaften
</dl>

### <a name="using-ellipses"></a>Verwenden von Ellipsen

Während Menübefehle für sofortige Aktionen verwendet werden, sind möglicherweise weitere Informationen erforderlich, um die Aktion auszuführen. **Geben Sie einen Befehl an, der zusätzliche Informationen (einschließlich einer Bestätigung) benötigt, indem Sie am Ende der Bezeichnung ein Ellipsen hinzufügen.**

![Screenshot des Druckbefehls und des Druck Dialogfelds ](images/cmd-menus-image15.png)

In diesem Beispiel wird der Druck... Befehl zeigt ein Druck Dialogfeld an, um weitere Informationen zu sammeln.

**Die korrekte Verwendung von Ellipsen ist wichtig, um anzugeben, dass Benutzer vor der Durchführung der Aktion weitere Möglichkeiten treffen oder sogar die Aktion vollständig abbrechen können.** Der visuelle Hinweis, der von einem Ellipsen angeboten wird, ermöglicht es Benutzern, Ihre Software ohne Angst zu untersuchen.

**Dies bedeutet nicht, dass Sie immer dann eine Ellipse verwenden sollten, wenn eine Aktion ein anderes Fenster nur dann anzeigt** , wenn zusätzliche Informationen erforderlich sind, um die Aktion auszuführen. Beispielsweise müssen die Befehle about, Advanced, Help, Options, Properties und Settings ein anderes Fenster anzeigen, wenn Sie darauf klicken, aber keine zusätzlichen Informationen vom Benutzer erfordern. Daher benötigen Sie keine Ellipsen.

**Bei Mehrdeutigkeit (z. b. bei der Befehls Bezeichnung fehlt ein Verb), entscheiden Sie sich für die wahrscheinlichste Benutzeraktion.** Wenn die Anzeige des Fensters eine gängige Aktion ist, verwenden Sie keine Auslassungs Punkte.

**Richtig:**

Weitere Farben...

Versionsinformationen

Im ersten Beispiel wählen Benutzer wahrscheinlich eine Farbe aus, sodass die Verwendung eines Ellipsen korrekt ist. Im zweiten Beispiel werden Benutzer wahrscheinlich die Versionsinformationen anzeigen, sodass Ellipsen unnötig sind.

> [!Note]  
> Wenn Sie bestimmen, ob für einen Menübefehl ein Auslassungs Zeichen erforderlich ist, verwenden Sie nicht die Notwendigkeit, Berechtigungen als Faktor zu [erhöhen](winenv-uac.md) .

 

Die Rechte Erweiterung ist nicht erforderlich, um einen Befehl auszuführen (sondern um die Berechtigung zu erteilen), und die Notwendigkeit, die Rechte zu erhöhen, wird durch das Sicherheitsschild angegeben.

## <a name="labels"></a>Bezeichnungen

-   **Verwenden Sie für Überschriften die Standardgroß- und kleinschreibung.**
    -   **Ausnahme:** Bei älteren Anwendungen können Sie ggf. die Groß-/Kleinschreibung von Titeln verwenden, um das Mischen von Groß-/Kleinschreibung

### <a name="menu-category-names"></a>Menü Kategorienamen

-   **Verwenden Sie Menü Kategorienamen, die einzelne Wort Verben oder Nomen sind.** Eine Bezeichnung mit mehreren Wörtern kann für 2 1-Word-Bezeichnungen verwechselt werden.
-   **Verb-basierte Menü Namen bevorzugen.** Lassen Sie jedoch das Verb aus, wenn es erstellen, anzeigen, anzeigen oder verwalten ist. Die folgenden Menü Kategorien haben z. b. keine Verben:
    -   Tabelle
    -   Tools
    -   Fenster
-   Verwenden Sie für nicht standardmäßige Kategorien Amen **ein einzelnes, bestimmtes Wort, das den Menü Inhalt eindeutig und genau beschreibt.** Obwohl die Namen nicht so allgemein sein müssen, dass Sie alles im Menü beschreiben, sollten Sie vorhersehbar genug sein, damit die Benutzer nicht überrascht sind, was Sie im Menü finden.

### <a name="menu-item-names"></a>Menü Elementnamen

-   **Verwenden Sie Menü Elementnamen, die mit einem Verb, einem Substantiv oder einem Substantiv Ausdruck beginnen.**
-   **Verb-basierte Menü Namen bevorzugen.** Lassen Sie jedoch das Verb aus, wenn:
    -   **Das Verb ist erstellen, anzeigen, anzeigen oder verwalten.** Die folgenden Befehle verfügen z. b. nicht über Verben:
        -   Info
        -   Fortgeschrittene
        -   Vollbildmodus
        -   Neu
        -   Optionen
        -   Eigenschaften
    -   **Das Verb ist mit dem Menü Kategorienamen identisch, um Wiederholungen zu vermeiden.** Verwenden Sie z. b. in der Kategorie Menü Einfügen Text, Tabelle und Bild anstelle von Text einfügen, Tabelle einfügen und Bild einfügen.
-   **Verwenden Sie bestimmte Verben.** Vermeiden Sie generische, nicht hilfreiche Verben wie z. b. ändern und verwalten.
-   **Verwenden Sie Singular Nomen für Befehle, die auf ein einzelnes Objekt angewendet** werden, und verwenden Sie andernfalls Plural Nomen.
-   **Verwenden Sie bei Bedarf modifiziererer, um zwischen ähnlichen Befehlen zu unterscheiden.** Beispiele: Zeile oberhalb einfügen, Zeile unten einfügen.
-   **Wählen Sie für Paare von ergänzenden Befehlen eindeutig ergänzende Namen aus.** Beispiele: Hinzufügen, entfernen; Anzeigen, ausblenden; Einfügen, löschen.
-   **Wählen Sie die Namen der Menü Elemente basierend auf den Benutzer Zielen und Aufgaben, nicht auf der Technologie aus.**

**Richtig:**

![Screenshot des Menü Elements "RIP" im Menü "Format" ](images/cmd-menus-image16.png)

**Falsch:**

![Screenshot des Menü Elements "RIP" im Menü "Codec" ](images/cmd-menus-image17.png)

Im falschen Beispiel basiert das Menü Element auf seiner Technologie.

-   Verwenden Sie die folgenden Menü Elementnamen für den angegebenen Zweck:
    -   **Optionen** , Um Programmoptionen anzuzeigen.
    -   **Anpassen** Zum Anzeigen der Programmoptionen, die sich speziell auf die Konfiguration der mechanischen Benutzeroberfläche beziehen.
    -   **Personalisieren** Um eine Zusammenfassung der häufig verwendeten [Personalisierungs](glossary.md) Einstellungen anzuzeigen.
    -   **Einstellungen** Verwenden Sie nicht. Verwenden Sie stattdessen Optionen.
    -   **Eigenschaften** , Wenn das Eigenschaften Fenster eines Objekts angezeigt werden soll.
    -   **Einstellungen** Verwenden Sie nicht als Menü Bezeichnung. Verwenden Sie stattdessen Optionen.

### <a name="submenu-names"></a>Unter Menü Namen

-   **Menü Elemente, in denen Untermenüs angezeigt werden, haben nie eine Ellipse für ihre Bezeichnung.** Der unter Menü Pfeil gibt an, dass eine andere Auswahl erforderlich ist.

**Falsch:**

![Screenshot des neuen Menü Elements mit Auslassungs Zeichen ](images/cmd-menus-image18.png)

In diesem Beispiel weist das neue Menü Element fälschlicherweise eine Ellipse auf.

## <a name="documentation"></a>Dokumentation

Beim Verweis auf Menüs:

-   Weitere Informationen finden Sie in den Menüleisten Unterbefehle zum ein-oder Ausblenden von Menüs. Nicht als klassisches Menü bezeichnen.
-   Weitere Informationen finden Sie in den Menüs. Verwenden Sie den genauen Bezeichnungs Text, einschließlich der Groß-und Kleinschreibung, aber nicht den Unterstrich oder die Auslassungs Punkte des Zugriffsschlüssels
-   Verwenden Sie zum Verweisen auf Menü Kategorien "im <category name> Menü". Wenn der Speicherort eines Menü Elements aus dem Kontext gelöscht wird, müssen Sie nicht die Menükategorie erwähnen.
-   Um die Benutzerinteraktion von Menü Elementen zu beschreiben, verwenden Sie Click, ohne das Wort Menü oder den Befehl. Verwenden Sie SELECT, SELECT oder Pick nicht. Verweisen Sie nicht auf ein Menü Element als Menü Element außer in der technischen Dokumentation.
-   Wenn Sie das Entfernen eines Häkchens über eine Menüoption beschreiben möchten, klicken Sie auf, um das Häkchen zu entfernen. Verwenden Sie nicht Clear.
-   Sie können Kontextmenüs als Kontextmenüs, nicht als Kontextmenüs verwenden.
-   Verwenden Sie keine Cascading-, Pulldown-, Dropdown-oder Popup-Menüs, um Menüs zu beschreiben, außer in der Programmier Dokumentation.
-   Verweisen Sie auf nicht verfügbare Menü Elemente als nicht verfügbar, nicht als abgeblendet, deaktiviert oder abgeblendet. Verwenden Sie deaktivierte in der Programmier Dokumentation.
-   Formatieren Sie die Bezeichnungen nach Möglichkeit mithilfe von fettem Text. Andernfalls sollten Sie die Bezeichnungen nur in Anführungszeichen setzen, wenn dies erforderlich ist, um Verwirrung zu vermeiden.

Beispiele:

-   Klicken Sie im Menü **Datei** auf **Drucken** , um das Dokument zu drucken.
-   Zeigen Sie im Menü **Ansicht** auf **Symbolleisten**, und klicken Sie dann auf **Formatierung**.

 

