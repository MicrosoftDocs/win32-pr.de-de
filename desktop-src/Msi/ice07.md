---
description: ICE07 überprüft, ob das Installationspaket angibt, dass die Schriftarten in den Ordner "fonsor" installiert werden. Wenn eine Schriftart in einem anderen Ordner als dem Ordner "fonsorfolder" installiert wird, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a79bcb681a57bb09ff235b35a5287492a4f39c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362568"
---
# <a name="ice07"></a>ICE07

ICE07 überprüft, ob das Installationspaket angibt, dass die Schriftarten in den Ordner "fonsor" installiert werden. Wenn eine Schriftart in einem anderen Ordner als dem Ordner "fonsorfolder" installiert wird, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.

Die benutzerdefinierte Aktion ICE07 führt die folgenden Aktionen für jede Schriftart in der [Schriftart Tabelle](font-table.md)aus.

1.  Sucht die Schriftart Datei, zu der jeder Schriftart Titel gehört, mithilfe der [Schriftart Tabelle](font-table.md).
2.  Fragt die Komponenten \_ Spalte der [Dateitabelle](file-table.md) für die Komponente ab, die die einzelnen Dateien steuert.
3.  Fragt die Verzeichnis \_ Spalte der [Komponenten Tabelle](component-table.md) ab, um einen Schlüssel in der Verzeichnis Tabelle abzurufen.
4.  Löst die [Verzeichnis Tabelle](directory-table.md) auf, um den Namen des Ordners zu bestimmen, in dem das Installationsprogramm die Schriftart Datei installieren soll.
5.  Gibt einen Fehler aus, wenn die Schriftart Datei in einem anderen Ordner als dem Ordner "Foner" installiert wird.

## <a name="result"></a>Ergebnis

ICE07 gibt einen Fehler aus, wenn feststellt, dass die Datenbank angibt, dass eine Schriftart Datei in einem anderen Ordner als dem Ordner "Foner" installiert werden soll.

## <a name="example"></a>Beispiel

IC07 würde die folgende Fehlermeldung für das gezeigte Beispiel veröffentlichen.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Schriftart Tabelle](font-table.md)



| Datei\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Dateitabelle](file-table.md) (partiell)



| File   | Komponente\_   |
|--------|---------------|
| Myrtle | Myrtle- \_ Strand |



 

[Komponenten Tabelle](component-table.md) (partiell)



| Komponente     | Verzeichnis\_ |
|---------------|-------------|
| Myrtle- \_ Strand | Sand Leiste     |



 

In diesem Beispiel wird die Schriftart Tahoma der Schriftart Datei Myrtle zugeordnet. Die Datei Myrtle gehört zum komponentenstrand der Komponente \_ . Die Auflösung der Verzeichnis Tabelle zeigt, dass alle Dateien, die zu Myrtle Beach gehören, \_ im Ordner Sand Bar installiert werden müssen. Da dies nicht der Ordner "Foner" ist, wird von ICE07 eine Fehlermeldung ausgegeben.

Beachten Sie, dass \_ die Schriftart Tahoma möglicherweise nicht zum Myrtle-Strand gehört, wenn der Myrtle-komponentenplatz tatsächlich im Sand leisten Ordner und nicht im Ordner "Foner" gehört \_ . Eine mögliche Lösung für den Fehler wäre das Einschließen von Tahoma in eine andere Komponente, die im Verzeichnis "fonsorfolder" installiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



