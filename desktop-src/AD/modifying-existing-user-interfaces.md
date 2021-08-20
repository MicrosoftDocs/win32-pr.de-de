---
title: Ändern vorhandener Benutzeroberflächen
description: Im Ergebnisbereich des Active Directory-Benutzer und -Computer MMC-Snap-Ins werden mehrere Spalten mit Attributdaten für Objekte innerhalb eines Containers angezeigt, z. B. die Attribute Name und Description.
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Ändern vorhandener Benutzeroberflächen in AD
- Benutzer- und Computer-Snap-In AD, Anzeige ändern
- Benutzer- und Computer-Snap-In AD, Hinzufügen von Spalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcf6ef4743009086ae19148c42a8addc5974e4ac833cdad8eee675fdce76a5f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025868"
---
# <a name="modifying-existing-user-interfaces"></a>Ändern vorhandener Benutzeroberflächen

Im Ergebnisbereich des Active Directory-Benutzer und -Computer MMC-Snap-Ins werden mehrere Spalten mit Attributdaten für Objekte innerhalb eines Containers angezeigt, z. B. die Attribute **Name** und **Description.** Mit dem Snap-In kann der Benutzer die im Ergebnisbereich des Snap-Ins angezeigten Spalten hinzufügen und entfernen.

Um die Anzeige zu ändern, verwendet der Benutzer das Pull-Down-Menü **Ansicht** und wählt **Spalten hinzufügen/entfernen** aus. Im Dialogfeld **Spalten hinzufügen/entfernen** gibt es eine Liste von Spalten, aus denen der Benutzer auswählen kann, um sie im Ergebnisbereich anzuzeigen.

Das Active Directory-Benutzer und -Computer MMC-Snap-In, das in Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition und Windows Server 2003 Datacenter Edition enthalten ist, bietet die Möglichkeit, die Liste der Spalten zu ändern, die im Ergebnisbereich des Snap-Ins für einen Container angezeigt werden können. Dieses Feature ist nur vorhanden, wenn das Snap-In auf eine Gesamtstruktur mit Windows Server 2003-Schema ausgerichtet ist.

Um der Liste eine Spalte hinzuzufügen, fügen Sie dem **extraColumns-Attribut** des Anzeigespezifizierrs für den Objekttyp, dem das Attribut zugeordnet ist, einen Wert hinzu. Das **extraColumns-Attribut** ist ein mehrwertiges Zeichenfolgenattribut, bei dem jede Zeichenfolge im folgenden Format vorliegt.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



In der folgenden Tabelle sind die Inhalte dieser Werte aufgeführt.



| Wert                        | BESCHREIBUNG                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapdisplayname &gt; "    | Enthält eine Zeichenfolge, die den **ldapDisplayName** des Attributs darstellt.                                                         |
| " &lt; Spaltenüberschrift &gt; "      | Enthält eine Zeichenfolge, die den im Header für die Spalte angezeigten Text darstellt.                                                  |
| " &lt; Standardsichtbarkeit &gt; " | Enthält einen numerischen Wert, der 0 ist, wenn das Attribut standardmäßig ausgeblendet ist, oder 1, wenn das Attribut standardmäßig sichtbar ist.               |
| " &lt; width &gt; "              | Enthält die Breite der Spalte in Pixel. Wenn dieser Wert -1 ist, wird die Breite der Spalte auf die Breite des Spaltenheaders festgelegt. |
| " &lt; nicht verwendet &gt; "             | Nicht verwendet. Muss Null sein.                                                                                                               |



 

Um beispielsweise eine Spalte hinzuzufügen, die den kanonischen Namen für Objekte in einer Organisationseinheit anzeigt, wird dem **extraColumns-Attribut** des **organizationalUnit-Display-Objekts** im Container display specifiers ein Wert für das **canonicalName-Attribut** hinzugefügt. Die Zeichenfolge, die dem **extraColumns-Attribut** des **organizationalUnit-Display-Objekts** hinzugefügt wird, sieht wie folgt aus.


```C++
canonicalName,Canonical Name,0,150,0
```



Im Dialogfeld **Spalten hinzufügen/entfernen** werden nur die Spalten angezeigt, die im **extraColumns-Attribut** des **displaySpecifier-Objekts** des angezeigten Containertyps enthalten sind. Wenn das **extraColumns-Attribut** keine Werte enthält, zeigt das Dialogfeld **Spalten hinzufügen/entfernen** einen festen Satz von Spalten an. Eine Kopie des festen Spaltensatzes ist im **extraColumns-Attribut** des **default-Display-Objekts** enthalten.

Um der Liste der Spalten für ein bestimmtes Objekt eine oder mehrere Spalten hinzuzufügen, müssen Sie alle **extraColumns-Werte** aus dem **Default-Display-Objekt** in das Zielobjekt kopieren und dann die benutzerdefinierten Spalten hinzufügen. Wenn Sie das **extraColumns-Attribut** für eine bestimmte Klasse angeben, verwendet diese Klasse diese Spalten und führt sie nicht mit den Spalten zusammen, die in der **default-Display-Klasse** angegeben sind. Daher haben weitere Änderungen an der **Default-Display-Klasse** keine Auswirkungen auf dieses Objekt.

Um eine benutzerdefinierte Spalte für alle Containertypen anzuzeigen, für die keine benutzerdefinierten Spalten registriert sind, fügen Sie dem **extraColumns-Attribut** des **default-Display-Objekts** einen Wert für die Spalte hinzu.

 

 




