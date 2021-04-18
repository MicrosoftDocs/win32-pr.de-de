---
description: Die Featuretabelle definiert die logische Struktur der Features und enthält die in der folgenden Tabelle gezeigten Spalten.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Funktions Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa91df750c4994a2d8a2308705213e48c864518
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347297"
---
# <a name="feature-table"></a>Funktions Tabelle

Die Featuretabelle definiert die logische Struktur der Features und enthält die in der folgenden Tabelle gezeigten Spalten.



| Spalte          | Typ                         | Schlüssel | Nullwerte zulässig |
|-----------------|------------------------------|-----|----------|
| Funktion         | [Bezeichner](identifier.md) | J   | N        |
| Über \_ geordnetes Element | [Bezeichner](identifier.md) | N   | J        |
| Titel           | [Text](text.md)             | N   | J        |
| BESCHREIBUNG     | [Text](text.md)             | N   | J        |
| Anzeige         | [Integer](integer.md)       | N   | J        |
| Ebene           | [Integer](integer.md)       | N   | N        |
| Verzeichnis\_     | [Bezeichner](identifier.md) | N   | J        |
| Attribute      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Befinden
</dt> <dd>

Der Primärschlüssel, der zum Identifizieren eines bestimmten Merkmals Datensatzes verwendet wird. Der Wert in diesem Feld darf eine maximale Länge von 38 Zeichen nicht überschreiten.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>Über \_ geordnetes Element
</dt> <dd>

Ein optionaler Schlüssel eines übergeordneten Datensatzes in derselben Tabelle.

Der Schlüssel verweist auf die Merkmals palte. Wenn das übergeordnete Feature nicht ausgewählt ist, wird dieses Feature nicht installiert. Ein NULL-Wert in diesem Feld gibt an, dass diese Funktion nicht über ein übergeordnetes Element verfügt und ein Stamm Element ist. Die \_ übergeordnete Spalte der Funktion darf nicht der Funktions Spalte desselben Datensatzes entsprechen.

> [!Note]  
> Die maximale Tiefe eines beliebigen Features beträgt 16. Ein [Fehler 2701](windows-installer-error-messages.md) ergibt sich, wenn eine Funktion vorhanden ist, die diese maximale Tiefe überschreitet.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Tel
</dt> <dd>

Eine kurze Text Zeichenfolge, die eine Funktion identifiziert.

Diese Zeichenfolge wird durch das [SelectionTree-Steuer](selectiontree-control.md) Element des [Auswahl Dialogfelds](selection-dialog.md)als Element aufgelistet.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine längere Text Zeichenfolge, die eine Funktion beschreibt.

Diese lokalisierbare Zeichenfolge wird durch das [Text Steuer](text-control.md) Element des [Auswahl Dialogfelds](selection-dialog.md)angezeigt.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Ausgestellten
</dt> <dd>

Die Zahl in diesem Feld gibt die Reihenfolge an, in der das Feature in der Benutzeroberfläche angezeigt werden soll.

Der Wert bestimmt auch, ob die Funktion anfänglich erweitert oder reduziert angezeigt wird. Wenn der Wert NULL oder 0 (null) ist, wird der Datensatz nicht angezeigt.

-   Wenn der Wert ungerade ist, wird der Funktions Knoten anfänglich erweitert.
-   Wenn der Wert gerade ist, wird der Funktions Knoten anfänglich reduziert.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Geringen
</dt> <dd>

Die anfängliche Installations Ebene dieses Features. Durch die Verarbeitung der Bedingungs [Tabelle](condition-table.md) kann der Wert der Ebene geändert werden.

Durch die Installations Ebene 0 (null) wird das Element deaktiviert und verhindert, dass es angezeigt wird. Eine Funktion mit einer Installations Ebene von 0 (null) wird während einer Installation nicht installiert, einschließlich administrativer Installationen. Weitere Informationen finden Sie im Abschnitt "Installationsstufe" im Abschnitt "Hinweise" in diesem Thema.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Befinden\_
</dt> <dd>

Die \_ Spalte Verzeichnis gibt den Namen eines Verzeichnisses an, das von einem [Auswahl Dialogfeld](selection-dialog.md)konfiguriert werden kann.

Da dieses Feld ein Schlüssel für die [Verzeichnis Tabelle](directory-table.md)ist, muss das angegebene Verzeichnis in der ersten Spalte der Verzeichnis Tabelle aufgeführt werden. Sie müssen eine [öffentliche Eigenschaft](public-properties.md) in dieser Spalte eingeben, um das Verzeichnis zu konfigurieren und im [Auswahl Dialogfeld](selection-dialog.md)eine Schaltfläche zum **Durchsuchen** anzuzeigen.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Legt
</dt> <dd>

Die Remote Ausführungs Option für Features, die nicht installiert sind und für die keine featurestatusanforderung durch die Verwendung einer der folgenden Eigenschaften erfolgt.

-   [**ADDLOCAL (Eigenschaft)**](addlocal.md)
-   [**Addsource (Eigenschaft)**](addsource.md)
-   [**Adddefault (Eigenschaft)**](adddefault.md)
-   [**Compaddlocal (Eigenschaft)**](compaddlocal.md)
-   [**Compaddsource (Eigenschaft)**](compaddsource.md)
-   [**Fileaddlocal (Eigenschaft)**](fileaddlocal.md)
-   [**Fileaddsource (Eigenschaft)**](fileaddsource.md)
-   [**Remove-Eigenschaft**](remove.md)
-   [**Eigenschaft neu installieren**](reinstall.md)
-   [**Ankündigungs Eigenschaft**](advertise.md)

Fügen Sie die angegeben Bits zum Gesamtwert dieser Spalte hinzu, um eine Remote Ausführungs Option einzuschließen.

-   Wenn dieses Feld leer ist, wird der Wert standardmäßig auf 0 (null) und msidbfeatureattributesfavorlocal festgelegt.
-   Wenn die featureinstallationsstufe 0 (null) oder größer oder gleich der aktuellen Installations Ebene ist, erfolgt keine Änderung im Funktionsstatus.



| Name                                         | Decimal | Hexadezimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbfeatureattributesfavorlocal             | 0       | 0x0000      | Komponenten dieses Features, die nicht für die Installation von der Quelle gekennzeichnet sind, werden lokal installiert. Eine Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, von denen einige auf msidbfeatureattributesfavorlocal und einige auf msidbfeatureattributesfavorsource festgelegt sind, wird lokal installiert. Komponenten, die in der [Komponenten Tabelle](component-table.md) als msidbcomponentattributessourceonly gekennzeichnet sind, werden immer von der Quell-CD/dem Server ausgeführt. Die Bits msidbfeatureattributesfavorlocal und msidbfeatureattributesfavorsource arbeiten mit Features, die nicht in der Ankündigungs [**Eigenschaft**](advertise.md)aufgeführt sind.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbfeatureattributesfavorsource            | 1       | 0x0001      | Komponenten dieses Features, die nicht für die lokale Installation gekennzeichnet sind, werden für die Installation von der Quell-CD-ROM oder vom Server installiert. Eine Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, von denen einige auf msidbfeatureattributesfavorlocal und einige auf msidbfeatureattributesfavorsource festgelegt sind, um lokal ausgeführt zu werden. Komponenten, die in der [Komponenten Tabelle](component-table.md) als "msidbcomponentattributeslocalonly" gekennzeichnet sind, werden immer lokal installiert. Die Bits msidbfeatureattributesfavorlocal und msidbfeatureattributesfavorsource arbeiten mit Features, die nicht in der Ankündigungs [**Eigenschaft**](advertise.md)aufgeführt sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbfeatureattributesfollowparent           | 2       | 0x0002      | Legen Sie dieses Attribut fest, und der Status des Features entspricht dem Status des übergeordneten Elements. Sie können diese Option nicht verwenden, wenn sich das Feature im Stammverzeichnis einer Funktionsstruktur befindet. Lassen Sie dieses Attribut aus, und der Funktionsstatus wird gemäß "msidbfeatureattributesdisallowankündigungs" und "msidbfeatureattributesfavorlocal" und "msidbfeatureattributesfavorsource" bestimmt.<br/> Um sicherzustellen, dass der Zustand der untergeordneten Funktion immer dem Zustand des übergeordneten Elements folgt, müssen Sie in den Attributen der untergeordneten Funktion sowohl msidbfeatureattributesfollowparent als auch, wenn das untergeordnete Element und das übergeordnete Element anfänglich auf Missing festgelegt sind.<br/> Beachten Sie Folgendes: Wenn Sie msidbfeatureattributesfollowparent festgelegt haben, ohne msidbfeatureattributesuidisallowmissing festzulegen, kann das Installationsprogramm nicht erzwingen, dass die untergeordnete Funktion den fehlenden Zustand verlässt. In diesem Fall stimmt das untergeordnete Feature nur mit dem Installationsstatus des übergeordneten Elements überein, wenn das untergeordnete Element auf einen anderen Wert als nicht vorhanden festgelegt ist<br/> Legen Sie msidbfeatureattributesfollowparent und msidbfeatureattributesuidisallowmissing fest, um sicherzustellen, dass ein untergeordnetes Feature dem Status der übergeordneten Funktion folgt.<br/> |
| msidbfeatureattributesfavorankündigungs-         | 4       | 0x0004      | Legen Sie dieses Attribut fest, und der Funktionsstatus ist ankündigen. Wenn die Funktion von der [**adddefault-Eigenschaft**](adddefault.md) aufgelistet wird, wird dieses Bit ignoriert, und der Funktionsstatus wird anhand von "msidbfeatureattributesfavorlocal" und "msidbfeatureattributesfavorsource" bestimmt. Lassen Sie dieses Attribut aus, und der Funktionsstatus wird gemäß "msidbfeatureattributesdisallowankündigungs" und "msidbfeatureattributesfavorlocal" und "msidbfeatureattributesfavorsource" bestimmt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbfeatureattributesdisallowankündigungs      | 8       | 0x0008      | Beachten Sie, dass dieses Bit nur mit Features funktioniert, die von der Ankündigungs [**Eigenschaft**](advertise.md)aufgelistet werden. Legen Sie dieses Attribut fest, um zu verhindern, dass die Funktion angekündigt wird.<br/> Legen Sie dieses Attribut fest, und wenn es sich bei der aufgelisteten Funktion nicht um ein übergeordnetes Element oder ein untergeordnetes Element handelt, wird das Feature gemäß msidbfeatureattributesfavorlocal und msidbfeatureattributesfavorsource installiert.<br/> Legen Sie dieses Attribut für das übergeordnete Element einer aufgelisteten Funktion fest, und das übergeordnete Element ist installiert.<br/> Legen Sie dieses Attribut für das untergeordnete Element einer aufgelisteten Funktion fest, und der Zustand des untergeordneten Elements ist nicht vorhanden.<br/> Lassen Sie dieses Attribut aus, und wenn es sich bei der aufgelisteten Funktion nicht um ein übergeordnetes Element oder ein untergeordnetes Element handelt, ist der Funktions<br/> Lassen Sie dieses Attribut aus, und wenn es sich bei der aufgelisteten Funktion um ein übergeordnetes Element oder ein untergeordnetes Element handelt, wird der Status beider Features angekündigt<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbfeatureattributesuidisallowmissing       | 16      | 0x0010      | Legen Sie dieses Attribut fest, und die Benutzeroberfläche zeigt keine Option zum Ändern des Funktions Zustands in "Missing" an. Wenn dieses Attribut festgelegt wird, wird der Installationsstatus des Features erzwungen, unabhängig davon, ob die Funktion in der Benutzeroberfläche sichtbar ist. Lassen Sie dieses Attribut aus, und die Benutzeroberfläche zeigt eine Option an, um den Funktionszustand in "Missing" zu ändern.<br/> Legen Sie msidbfeatureattributesfollowparent und msidbfeatureattributesuidisallowmissing fest, um sicherzustellen, dass ein untergeordnetes Feature dem Status der übergeordneten Funktion folgt.<br/> Das Festlegen dieses Attributs wirkt sich nicht nur auf die Benutzeroberfläche aus, sondern auch auf den Installationsstatus, ob die Funktion in der Benutzeroberfläche sichtbar ist oder nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbfeatureattributesnounsupportedankündigungs- | 32      | 0x0020      | Legen Sie dieses Attribut fest, und die Ankündigung ist für die Funktion deaktiviert, wenn die Betriebssystemshell Windows Installer Deskriptoren nicht unterstützt. Lassen Sie dieses Attribut aus, und Werbung ist nicht deaktiviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Einige Attribute sind exklusiv voneinander. Wenn Sie versuchen, diese Attribute in derselben Funktion festzulegen, tritt bei der [**Paket**](package-validation.md)Überprüfung für das Installationspaket ein Fehler auf.

-   Verwenden Sie msidbfeatureattributesfavorankündigungs nicht mit msidbfeatureattributesdisallowankündigungs.
-   Verwenden Sie msidbfeatureattributesnounsupportedankündigungs nicht zusammen mit msidbfeatureattributesdisallowankündigungs Ankündigung.
-   Verwenden Sie msidbfeatureattributesfollowparent nicht mit msidbfeatureattributesfavorsource.
-   Beachten Sie, dass sich die Werte "msidbfeatureattributesfollowparent" und "msidbfeatureattributesfavorlocal" gegenseitig ausschließen. Wenn der msidbfeatureattributesfollowparent-Wert verwendet wird, wird davon ausgegangen, dass der msidbfeatureattributesfavorlocal-Wert nicht vorhanden ist.

</dd> </dl>

Beachten Sie, dass bei der Installation einer untergeordneten Funktion auch das zugehörige übergeordnete Feature installiert wird. Wenn eine übergeordnete Funktion installiert ist, wird die untergeordnete Funktion nicht unbedingt installiert, es sei denn, die Attribute "msidbfeatureattributesfollowparent" und "msidbfeatureattributesuidisallowmissing" sind festgelegt. Diese hierarchische Beziehung der Installation von übergeordneten und untergeordneten Funktionen wird auch für die GUI-Installationen und-Installationen verwendet, die Befehlszeilen Eigenschaften verwenden.

## <a name="remarks"></a>Bemerkungen

Dieser Tabelle werden mehrere zusätzliche temporäre Spalten hinzugefügt, wenn Sie für Berechnungen, die von der Kosten-und Benutzeroberflächen Auswahl verwendet werden, in den Arbeitsspeicher geladen werden.

Eine Komponente kann von zwei oder mehr Features oder Anwendungen gemeinsam genutzt werden. Wenn zwei oder mehr Funktionen auf dieselbe Komponente verweisen, wird diese Komponente für die Installation ausgewählt, wenn eine der zugeordneten Features ausgewählt ist. Dies kann auch der Grund sein, warum untergeordnete Funktionen nicht deinstalliert werden, wenn ein übergeordnetes Feature entfernt wird. Wenn die untergeordnete Funktion aus Komponenten besteht, die von anderen Features oder Anwendungen benötigt werden, wird die untergeordnete Funktion nicht vom Windows Installer entfernt.

Weitere Informationen finden Sie unter [Steuern von Funktionsauswahl Zuständen](controlling-feature-selection-states.md).

Installationsstufe:

-   Für jede Installation gibt es eine definierte Installations Ebene, die ein ganzzahliger Wert zwischen 1 und 32.767 ist. Der Anfangswert wird durch die [**INSTALLLEVEL-Eigenschaft**](installlevel.md)bestimmt, die in der [Eigenschaften Tabelle](property-table.md)festgelegt wird.
-   Eine Funktion wird nur installiert, wenn der Wert auf Featureebene kleiner oder gleich der aktuellen Installations Ebene ist. Die Benutzeroberfläche kann so erstellt werden, dass der Benutzer beim Initialisieren der Installation die Installations Ebene eines beliebigen Features in der Featuretabelle ändern kann. Ein Autor kann z. b. auf installationsebenenwerte definieren, die bestimmte Installationsoptionen darstellen, z. b. **Benutzer** definiert, **typisch** oder **Minimal**, und dann ein Dialogfeld erstellen, das [setinstalllevel ControlEvents](setinstalllevel-controlevent.md) verwendet, damit der Benutzer einen dieser Zustände auswählen kann.
-   Abhängig vom Zustand, den der Benutzer auswählt, wird im Dialogfeld die Eigenschaft Installationsebene auf den entsprechenden Wert festgelegt. Wenn der Autor eine **typische** Ebene von 100 zuweist und der Benutzer **typische** auswählt, werden nur die Features mit einer 100 oder weniger installiert. Außerdem kann die **benutzerdefinierte** Option zu einem anderen Dialogfeld führen, das ein [SelectionTree-Steuer](selectiontree-control.md)Element enthält. Das SelectionTree-Steuerelement ermöglicht es dem Benutzer, einzeln zu ändern, ob die einzelnen Features installiert sind.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE10](ice10.md)  
[ICE14](ice14.md)  
[ICE21](ice21.md)  
[ICE32](ice32.md)  
[ICE41](ice41.md)  
[ICE45](ice45.md)  
[ICE47](ice47.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE62](ice62.md)  
[ICE67](ice67.md)  
[ICE79](ice79.md)  
[ICE86](ice86.md)  
[ICE94](ice94.md)  
</dl>

 

 




