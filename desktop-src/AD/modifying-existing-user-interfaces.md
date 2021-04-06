---
title: Ändern vorhandener Benutzeroberflächen
description: Im Ergebnisbereich des MMC-Snap-Ins "Active Directory-Benutzer und-Computer" werden mehrere Spalten mit Attributdaten für Objekte in einem Container angezeigt, z. b. die Attribute "Name" und "Description".
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- Ändern vorhandener Benutzeroberflächen anzeigen
- AD-Snap-in "Benutzer und Computer", Ändern der Anzeige
- AD-Snap-in "Benutzer und Computer", Hinzufügen von Spalten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855407"
---
# <a name="modifying-existing-user-interfaces"></a>Ändern vorhandener Benutzeroberflächen

Im Ergebnisbereich des MMC-Snap-Ins "Active Directory-Benutzer und-Computer" werden mehrere Spalten mit Attributdaten für Objekte in einem Container angezeigt, z. b. die Attribute " **Name** " und " **Description** ". Das Snap-in ermöglicht dem Benutzer das Hinzufügen und Entfernen der Spalten, die im Ergebnisbereich des Snap-Ins angezeigt werden.

Um die Anzeige zu ändern, verwendet der Benutzer das Pulldownmenü **anzeigen** und wählt **Spalten hinzufügen/entfernen** aus. Im Dialogfeld **Spalten hinzufügen/entfernen** finden Sie eine Liste der Spalten, aus denen der Benutzer auswählen kann, um ihn im Ergebnisbereich anzuzeigen.

Das MMC-Snap-in "Active Directory-Benutzer und-Computer", das in Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition und Windows Server 2003, Datacenter Edition enthalten ist, bietet die Möglichkeit, die Liste der Spalten zu ändern, die im Ergebnisbereich des Snap-Ins für einen Container angezeigt werden können. Diese Funktion ist nur vorhanden, wenn das-Snap-in auf eine Gesamtstruktur mit Windows Server 2003-Schema ausgerichtet ist.

Um der Liste eine Spalte hinzuzufügen, fügen Sie dem **extraColumns** -Attribut des Anzeige Spezifizierers einen Wert für den Objekttyp hinzu, dem das Attribut zugeordnet ist. Das **extraColumns** -Attribut ist ein mehr wertiges Zeichen folgen Attribut, bei dem jede Zeichenfolge das folgende Format hat.


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



In der folgenden Tabelle sind die Inhalte dieser Werte aufgeführt.



| Wert                        | BESCHREIBUNG                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| " &lt; ldapDisplayName &gt; "    | Enthält eine Zeichenfolge, die den **ldapDisplayName** des Attributs darstellt.                                                         |
| " &lt; Spalten Kopfzeile &gt; "      | Enthält eine Zeichenfolge, die den Text darstellt, der im Header der Spalte angezeigt wird.                                                  |
| " &lt; Standard Sichtbarkeit &gt; " | Enthält einen numerischen Wert, der 0 (null) ist, wenn das Attribut standardmäßig ausgeblendet ist, oder 1, wenn das Attribut standardmäßig sichtbar ist.               |
| " &lt; Width &gt; "              | Enthält die Breite der Spalte in Pixel. Wenn dieser Wert-1 ist, wird die Breite der Spalte auf die Breite des Spalten Headers festgelegt. |
| "nicht &lt; verwendet &gt; "             | Nicht verwendet. Muss Null sein.                                                                                                               |



 

Um z. b. eine Spalte hinzuzufügen, die den kanonischen Namen für Objekte in einer Organisationseinheit anzeigt, wird ein Wert für das Attribut " **CanonicalName** " dem Attribut " **extraColumns** " des Objekts " **organizationalUnit-Display** " im Container "Anzeige spezifiker" hinzugefügt. Die Zeichenfolge, die dem **extraColumns** -Attribut des **organizationalUnit-Display-** Objekts hinzugefügt wird, sieht wie folgt aus.


```C++
canonicalName,Canonical Name,0,150,0
```



Im Dialogfeld **Spalten hinzufügen/entfernen** werden nur die Spalten angezeigt, die im **extraColumns** -Attribut des **displaySpecifier** -Objekts des angezeigten Container Typs enthalten sind. Wenn das **extraColumns** -Attribut keine Werte enthält, wird im Dialogfeld **Spalten hinzufügen/entfernen** ein fester Satz von Spalten angezeigt. Eine Kopie des fixierten Satzes von Spalten ist im **extraColumns** -Attribut des **default-Display-** Objekts enthalten.

Wenn Sie einer Spaltenliste für ein bestimmtes Objekt eine oder mehrere Spalten hinzufügen möchten, müssen Sie alle **extraColumns** -Werte aus dem **default-Display-** Objekt in das Zielobjekt kopieren und dann die benutzerdefinierten Spalten hinzufügen. Wenn Sie das **extraColumns** -Attribut für eine bestimmte Klasse angeben, werden diese Spalten von dieser Klasse verwendet und nicht mit den Spalten zusammengeführt, die in der **default-Display-** Klasse angegeben sind. Folglich haben weitere Änderungen an der **default-Display-** Klasse keine Auswirkung auf dieses Objekt.

Wenn Sie eine benutzerdefinierte Spalte für alle Containertypen anzeigen möchten, für die keine benutzerdefinierten Spalten registriert sind, fügen Sie dem **extraColumns** -Attribut des **default-Display-** Objekts einen Wert für die Spalte hinzu.

 

 




