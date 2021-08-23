---
description: ICE07 überprüft, ob das Installationspaket angibt, dass Schriftarten im FontsFolder installiert werden. Wenn eine Schriftart in einem anderen Ordner als dem FontsFolder installiert ist, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.
ms.assetid: aa51b077-fb7b-4e09-9de1-ef1905144a94
title: ICE07
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4226a0e555a35c7d5735abe0b14520d000bfeea8c888488ce37b15a78674ff9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581290"
---
# <a name="ice07"></a>ICE07

ICE07 überprüft, ob das Installationspaket angibt, dass Schriftarten im FontsFolder installiert werden. Wenn eine Schriftart in einem anderen Ordner als dem FontsFolder installiert ist, erstellt das Installationsprogramm eine Verknüpfung, anstatt die Schriftart tatsächlich zu installieren.

Die benutzerdefinierte ICE07-Aktion führt für jede Schriftart in der [Schriftarttabelle Folgendes aus.](font-table.md)

1.  Sucht die Schriftartdatei, zu der jeder Schriftarttitel gehört, mithilfe der [Schriftarttabelle](font-table.md).
2.  Fragt die Spalte Komponente der Dateitabelle nach der \_ Komponente [ab,](file-table.md) die die einzelnen Dateien steuert.
3.  Fragt die Directory \_ -Spalte der [Component-Tabelle ab,](component-table.md) um einen Schlüssel in der Directory-Tabelle zu erhalten.
4.  Löst die [Directory-Tabelle auf,](directory-table.md) um den Namen des Ordners zu bestimmen, in dem das Installationsprogramm die Schriftartdatei installieren soll.
5.  Gibt einen Fehler aus, wenn die Schriftartdatei in einem anderen Ordner als dem FontsFolder installiert wird.

## <a name="result"></a>Ergebnis

ICE07 gibt einen Fehler aus, wenn die Datenbank angibt, dass eine Schriftartdatei in einem anderen Ordner als dem FontsFolder installiert wird.

## <a name="example"></a>Beispiel

IC07 würde die folgende Fehlermeldung für das gezeigte Beispiel veröffentlichen.

``` syntax
'Tahoma' is a font and must be installed to the FontsFolder directory. Current Install Directory: 'Sandbar'.
```

[Schriftarttabelle](font-table.md)



| Datei\_ | FontTitle |
|--------|-----------|
| Myrtle | Tahoma    |



 

[Dateitabelle](file-table.md) (partiell)



| Datei   | Komponente\_   |
|--------|---------------|
| Myrtle | Myrtle \_ Beach |



 

[Komponententabelle](component-table.md) (partiell)



| Komponente     | Verzeichnis\_ |
|---------------|-------------|
| Myrtle \_ Beach | Sandbank     |



 

In diesem Beispiel wird die Schriftart Tahoma der Schriftartdatei Myrtle angezeigt. Die Datei Myrtle gehört zur Komponente Myrtle \_ Beach. Die Auflösung der Directory-Tabelle zeigt, dass alle Dateien, die zu Myrtle Beach gehören, im \_ Sandbar-Ordner installiert werden sollen. Da dies nicht der FontsFolder ist, gibt ICE07 eine Fehlermeldung aus.

Beachten Sie Folgendes: Wenn die Komponente Myrtle Beach wirklich zum Ordner Sandbar und nicht zum Ordner FontsFolder gehört, gehört die Schriftart Tahoma möglicherweise nicht \_ zu Myrtle \_ Beach. Eine mögliche Lösung für den Fehler wäre, Tahoma in eine andere Komponente einbetten, die im Verzeichnis FontsFolder installiert wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



