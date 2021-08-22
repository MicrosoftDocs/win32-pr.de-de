---
description: Die Featuretabelle definiert die logische Struktur von Features und enthält die in der folgenden Tabelle gezeigten Spalten.
ms.assetid: 1faee1d5-6e39-43ea-bf92-a0b3986a13a1
title: Featuretabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65dcf9177c44f407876cbe339925ca4524034a1335393161bb40310d60c158ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119251760"
---
# <a name="feature-table"></a>Featuretabelle

Die Featuretabelle definiert die logische Struktur von Features und enthält die in der folgenden Tabelle gezeigten Spalten.



| Spalte          | Typ                         | Key | Nullwerte zulässig |
|-----------------|------------------------------|-----|----------|
| Komponente         | [Identifier](identifier.md) | J   | N        |
| \_Übergeordnetes Feature | [Identifier](identifier.md) | N   | J        |
| Titel           | [Text](text.md)             | N   | J        |
| BESCHREIBUNG     | [Text](text.md)             | N   | J        |
| Anzeige         | [Integer](integer.md)       | N   | J        |
| Ebene           | [Integer](integer.md)       | N   | N        |
| Verzeichnis\_     | [Identifier](identifier.md) | N   | J        |
| Attribute      | [Integer](integer.md)       | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Feature"></span><span id="feature"></span><span id="FEATURE"></span>Feature
</dt> <dd>

Der Primärschlüssel, der zum Identifizieren eines bestimmten Featuredatensatzes verwendet wird. Der Wert in diesem Feld darf eine maximale Länge von 38 Zeichen nicht überschreiten.

</dd> <dt>

<span id="Feature_Parent"></span><span id="feature_parent"></span><span id="FEATURE_PARENT"></span>\_Übergeordnetes Feature
</dt> <dd>

Ein optionaler Schlüssel eines übergeordneten Datensatzes in derselben Tabelle.

Der Schlüssel zeigt auf die Spalte Feature. Wenn das übergeordnete Feature nicht ausgewählt ist, wird dieses Feature nicht installiert. Ein NULL-Wert in diesem Feld gibt an, dass dieses Feature kein übergeordnetes Element besitzt und ein Stammelement ist. Die \_ Spalte Feature Parent darf nicht mit der Spalte Feature desselben Datensatzes identisch sein.

> [!Note]  
> Die maximale Tiefe jedes Features beträgt 16. Der [Fehler 2701](windows-installer-error-messages.md) tritt auf, wenn ein Feature vorhanden ist, das diese maximale Tiefe überschreitet.

 

</dd> <dt>

<span id="Title"></span><span id="title"></span><span id="TITLE"></span>Titel
</dt> <dd>

Eine kurze Textzeichenfolge, die ein Feature identifiziert.

Diese Zeichenfolge wird vom [SelectionTree-Steuerelement](selectiontree-control.md) des [Auswahldialogfelds](selection-dialog.md)als Element aufgelistet.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Beschreibung
</dt> <dd>

Eine längere Textzeichenfolge, die ein Feature beschreibt.

Diese lokalisierbare Zeichenfolge wird vom [Textsteuerelement](text-control.md) des [Auswahldialogfelds](selection-dialog.md)angezeigt.

</dd> <dt>

<span id="Display"></span><span id="display"></span><span id="DISPLAY"></span>Anzeigen
</dt> <dd>

Die Zahl in diesem Feld gibt die Reihenfolge an, in der das Feature auf der Benutzeroberfläche angezeigt werden soll.

Der Wert bestimmt auch, ob das Feature anfänglich erweitert oder reduziert angezeigt wird. Wenn der Wert NULL oder 0 (null) ist, wird der Datensatz nicht angezeigt.

-   Wenn der Wert ungerade ist, wird der Featureknoten anfänglich erweitert.
-   Wenn der Wert gerade ist, wird der Featureknoten anfänglich reduziert.

</dd> <dt>

<span id="Level"></span><span id="level"></span><span id="LEVEL"></span>Ebene
</dt> <dd>

Die anfängliche Installationsebene dieses Features. Die Verarbeitung der [Bedingungstabelle](condition-table.md) kann den Ebenenwert ändern.

Eine Installationsebene von 0 (null) deaktiviert das Element und verhindert, dass es angezeigt wird. Ein Feature mit einer Installationsstufe von 0 (null) wird während einer Installation nicht installiert, einschließlich administrativer Installationen. Weitere Informationen finden Sie unter "Installationsebene" im Abschnitt "Hinweise" dieses Themas.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Verzeichnis\_
</dt> <dd>

Die Spalte Verzeichnis \_ gibt den Namen eines Verzeichnisses an, das mit einem [Auswahldialogfeld](selection-dialog.md)konfiguriert werden kann.

Da dieses Feld ein Schlüssel in der [Verzeichnistabelle](directory-table.md)ist, muss das angegebene Verzeichnis in der ersten Spalte der Verzeichnistabelle aufgeführt werden. Sie müssen eine [öffentliche Eigenschaft](public-properties.md) in diese Spalte eingeben, um das Verzeichnis konfigurierbar zu machen und um im [Auswahldialogfeld](selection-dialog.md)die Schaltfläche **Durchsuchen** anzuzeigen.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attribute
</dt> <dd>

Die Remoteausführungsoption für Features, die nicht installiert sind und für die keine Funktionszustandsanforderung mit einer der folgenden Eigenschaften erfolgt.

-   [**ADDLOCAL-Eigenschaft**](addlocal.md)
-   [**ADDSOURCE-Eigenschaft**](addsource.md)
-   [**ADDDEFAULT-Eigenschaft**](adddefault.md)
-   [**COMPADDLOCAL-Eigenschaft**](compaddlocal.md)
-   [**COMPADDSOURCE-Eigenschaft**](compaddsource.md)
-   [**FILEADDLOCAL-Eigenschaft**](fileaddlocal.md)
-   [**FILEADDSOURCE-Eigenschaft**](fileaddsource.md)
-   [**REMOVE-Eigenschaft**](remove.md)
-   [**REINSTALL-Eigenschaft**](reinstall.md)
-   [**ADVERTISE-Eigenschaft**](advertise.md)

Fügen Sie dem Gesamtwert dieser Spalte die angegebenen Bits hinzu, um eine Remoteausführungsoption einzuschließt.

-   Wenn dieses Feld leer ist, wird standardmäßig der Wert 0 (null) und msidbFeatureAttributesFavorLocal verwendet.
-   Wenn die Installationsebene des Features 0 (null) oder größer oder gleich der aktuellen Installationsebene ist, wird der Featurezustand nicht geändert.



| Name                                         | Decimal | Hexadezimal | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------|---------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msidbFeatureAttributesFavorLocal             | 0       | 0x0000      | Komponenten dieses Features, die nicht für die Installation aus der Quelle markiert sind, werden lokal installiert. Eine Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, von denen einige auf msidbFeatureAttributesFavorLocal und andere auf msidbFeatureAttributesFavorSource festgelegt sind, wird lokal installiert. Komponenten, die als msidbComponentAttributesSourceOnly in der [Komponententabelle](component-table.md) gekennzeichnet sind, werden immer von der Quell-CD/dem Quellserver ausgeführt. Die Bits msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource funktionieren mit Funktionen, die nicht in der [**ADVERTISE-Eigenschaft**](advertise.md)aufgeführt sind.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| msidbFeatureAttributesFavorSource            | 1       | 0x0001      | Komponenten dieses Features, die nicht für die lokale Installation markiert sind, werden installiert, um von der CD-ROM-Quelldatei oder dem Quellserver aus ausgeführt zu werden. Eine Komponente, die von zwei oder mehr Features gemeinsam genutzt wird, von denen einige auf msidbFeatureAttributesFavorLocal und einige auf msidbFeatureAttributesFavorSource festgelegt sind, wird installiert, um lokal ausgeführt zu werden. Komponenten, die in der [Komponententabelle](component-table.md) als msidbComponentAttributesLocalOnly gekennzeichnet sind, werden immer lokal installiert. Die Bits msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource funktionieren mit Funktionen, die nicht in der [**ADVERTISE-Eigenschaft**](advertise.md)aufgeführt sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesFollowParent           | 2       | 0x0002      | Legen Sie dieses Attribut fest, und der Status des Features entspricht dem Zustand des übergeordneten Elements des Features. Sie können diese Option nicht verwenden, wenn sich das Feature im Stamm einer Featurestruktur befindet. Lassen Sie dieses Attribut aus, und der Featurezustand wird anhand von msidbFeatureAttributesDisallowAdvertise und msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource bestimmt.<br/> Um sicherzustellen, dass der Zustand des untergeordneten Features immer dem Zustand des übergeordneten Elements folgt, müssen Sie sowohl msidbFeatureAttributesFollowParent als auch msidbFeatureAttributesUIDisallowAbsent in die Attribute des untergeordneten Features einschließen, auch wenn das untergeordnete und das übergeordnete Element anfänglich im SelectionTree-Steuerelement nicht vorhanden sind.<br/> Beachten Sie Folgendes: Wenn Sie msidbFeatureAttributesFollowParent festlegen, ohne msidbFeatureAttributesUIDisallowAbsent festzulegen, kann das Installationsprogramm das untergeordnete Feature nicht aus dem nicht verfügbaren Zustand erzwingen. In diesem Fall stimmt die untergeordnete Funktion nur dann mit dem Installationsstatus des übergeordneten Elements überein, wenn das untergeordnete Element auf einen anderen als den nicht fehlenden Festgelegt ist.<br/> Legen Sie msidbFeatureAttributesFollowParent und msidbFeatureAttributesUIDisallowAbsent fest, um sicherzustellen, dass ein untergeordnetes Feature dem Zustand des übergeordneten Features folgt.<br/> |
| msidbFeatureAttributesFavorAdvertise         | 4       | 0x0004      | Legen Sie dieses Attribut fest, und der Funktionsstatus lautet "Ankündigen". Wenn das Feature von der [**ADDDEFAULT-Eigenschaft**](adddefault.md) aufgelistet wird, wird dieses Bit ignoriert, und der Featurestatus wird anhand von msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource bestimmt. Lassen Sie dieses Attribut aus, und der Featurezustand wird anhand von msidbFeatureAttributesDisallowAdvertise und msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource bestimmt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| msidbFeatureAttributesDisallowAdvertise      | 8       | 0x0008      | Beachten Sie, dass dieses Bit nur mit Features funktioniert, die von der [**ADVERTISE-Eigenschaft**](advertise.md)aufgelistet werden. Legen Sie dieses Attribut fest, um zu verhindern, dass das Feature angekündigt wird.<br/> Legen Sie dieses Attribut fest, und wenn das aufgeführte Feature kein übergeordnetes oder untergeordnetes Element ist, wird das Feature gemäß msidbFeatureAttributesFavorLocal und msidbFeatureAttributesFavorSource installiert.<br/> Legen Sie dieses Attribut für das übergeordnete Element eines aufgelisteten Features fest, und das übergeordnete Element wird installiert.<br/> Legen Sie dieses Attribut für das untergeordnete Element eines aufgelisteten Features fest, und der Status des untergeordneten Features ist Absent.<br/> Lässt dieses Attribut aus, und wenn das aufgeführte Feature kein übergeordnetes oder untergeordnetes Element ist, lautet der Funktionsstatus Ankündigen.<br/> Lässt dieses Attribut aus, und wenn das aufgelistete Feature ein übergeordnetes oder untergeordnetes Element ist, lautet der Status beider Features Ankündigen.<br/>                                                                                                                                                                                                                                                                                                                                                                                          |
| msidbFeatureAttributesUIDisallowAbsent       | 16      | 0x0010      | Legen Sie dieses Attribut fest, und auf der Benutzeroberfläche wird keine Option zum Ändern des Funktionszustands in Absent angezeigt. Das Festlegen dieses Attributs erzwingt den Installationsstatus des Features, unabhängig davon, ob das Feature auf der Benutzeroberfläche sichtbar ist. Lassen Sie dieses Attribut aus, und auf der Benutzeroberfläche wird eine Option zum Ändern des Funktionszustands in Absent angezeigt.<br/> Legen Sie msidbFeatureAttributesFollowParent und msidbFeatureAttributesUIDisallowAbsent fest, um sicherzustellen, dass ein untergeordnetes Feature dem Zustand des übergeordneten Features folgt.<br/> Das Festlegen dieses Attributs wirkt sich nicht nur auf die Benutzeroberfläche aus, sondern erzwingt auch den Installationszustand des Features, unabhängig davon, ob das Feature auf der Benutzeroberfläche sichtbar ist oder nicht.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| msidbFeatureAttributesNoUnsupportedAdvertise | 32      | 0x0020      | Legen Sie dieses Attribut fest, und die Ankündigung ist für das Feature deaktiviert, wenn die Betriebssystemshell Windows Installer-Deskriptoren nicht unterstützt. Dieses Attribut auslassen, und die Werbung ist nicht deaktiviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Einige Attribute sind exklusiv voneinander. Der Versuch, diese Attribute für dasselbe Feature zusammen festzulegen, führt dazu, dass das Installationspaket die [**Paketvalidierung nicht erfolgreich ist.**](package-validation.md)

-   Verwenden Sie msidbFeatureAttributesFavorAdvertise nicht mit msidbFeatureAttributesDisallowAdvertise.
-   Verwenden Sie msidbFeatureAttributesNoUnsupportedAdvertise nicht zusammen mit msidbFeatureAttributesDisallowAdvertise.
-   Verwenden Sie msidbFeatureAttributesFollowParent nicht mit msidbFeatureAttributesFavorSource.
-   Beachten Sie, dass sich die Werte msidbFeatureAttributesFollowParent und msidbFeatureAttributesFavorLocal gegenseitig ausschließen. Wenn der wert msidbFeatureAttributesFollowParent verwendet wird, wird davon ausgegangen, dass der wert msidbFeatureAttributesFavorLocal nicht vorhanden ist.

</dd> </dl>

Beachten Sie, dass bei der Installation eines untergeordneten Features auch das übergeordnete Feature installiert ist. Wenn ein übergeordnetes Feature installiert ist, wird sein untergeordnetes Feature nicht unbedingt installiert, es sei denn, die Attribute msidbFeatureAttributesFollowParent und msidbFeatureAttributesUIDisallowAbsent sind festgelegt. Diese hierarchische Beziehung der Installation übergeordneter und untergeordneter Features wird auch für gui-Installationen und -Installationen verwendet, die Befehlszeileneigenschaften verwenden.

## <a name="remarks"></a>Hinweise

Dieser Tabelle werden mehrere zusätzliche temporäre Spalten hinzugefügt, wenn sie für Berechnungen, die von der Auswahl der Kosten und der Benutzeroberfläche (UI) verwendet werden, in den Arbeitsspeicher geladen wird.

Eine Komponente kann von zwei oder mehr Features oder Anwendungen gemeinsam genutzt werden. Wenn sich zwei oder mehr Features auf dieselbe Komponente beziehen, wird diese Komponente für die Installation ausgewählt, wenn eines der zugeordneten Features ausgewählt ist. Dies kann auch der Grund dafür sein, dass untergeordnete Features nicht deinstalliert werden, wenn ein übergeordnetes Feature entfernt wird. Wenn das untergeordnete Feature aus Komponenten besteht, die von anderen Features oder Anwendungen benötigt werden, entfernt der Windows Installer das untergeordnete Feature nicht.

Weitere Informationen finden Sie unter [Steuern von Funktionsauswahlzuständen.](controlling-feature-selection-states.md)

Installationsebene:

-   Für jede Installation gibt es eine definierte Installationsebene, die einen ganzzahligen Wert von 1 bis 32.767 darstellt. Der Anfangswert wird durch die [**INSTALLLEVEL-Eigenschaft**](installlevel.md)bestimmt, die in der [Eigenschaftentabelle](property-table.md)festgelegt ist.
-   Ein Feature wird nur installiert, wenn der Featureebenenwert kleiner oder gleich der aktuellen Installationsebene ist. Die Benutzeroberfläche kann so erstellt werden, dass der Benutzer beim Initialisieren der Installation die Installationsebene jedes Features in der Featuretabelle ändern kann. Beispielsweise kann ein Autor Werte auf Installationsebene definieren, die bestimmte Installationsoptionen darstellen, z. **B. Benutzerdefiniert,** **Typisch** oder **Minimum,** und dann ein Dialogfeld erstellen, das [SetInstallLevel ControlEvents](setinstalllevel-controlevent.md) verwendet, um dem Benutzer die Auswahl eines dieser Zustände zu ermöglichen.
-   Abhängig vom vom Benutzer ausgewählten Zustand legt das Dialogfeld die Eigenschaft auf Installationsebene auf den entsprechenden Wert fest. Wenn der Autor **Typisch** eine Ebene von 100 zuweist und der Benutzer **Typisch** auswählt, werden nur die Features mit einer Ebene von 100 oder weniger installiert. Darüber hinaus kann die Option **Benutzerdefiniert** zu einem anderen Dialogfeld führen, das ein [SelectionTree-Steuerelement](selectiontree-control.md)enthält. Mit dem SelectionTree-Steuerelement kann der Benutzer dann einzeln ändern, ob jedes Feature installiert ist.

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

 

 




