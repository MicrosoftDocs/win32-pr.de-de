---
description: Parallele Installationen, auch geschmierte Installationen genannt, sind eine veraltete Funktion der Windows Installer.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Parallele Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d89f2ef4af062c8151935fefab471603f79d7633
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866368"
---
# <a name="concurrent-installations"></a>Parallele Installationen

Parallele Installationen, auch geschmierte Installationen genannt, sind eine veraltete Funktion der Windows Installer. Anwendungen, die mit gleichzeitigen Installationen installiert werden, können letztendlich fehlschlagen, da Sie für Kunden schwierig zu bedienen sind. Verwenden Sie keine gleichzeitigen Installationen, um Produkte zu installieren, die für die Öffentlichkeit freigegeben werden sollen. Gleichzeitige Installationen können bei der Installation von Anwendungen, die nicht für die öffentliche Freigabe vorgesehen sind, eine eingeschränkte Anwendbarkeit in kontrollierten Unternehmensumgebungen haben. Die Dokumentation zur parallelen Installation wird für Paket Ersteller bereitgestellt, die parallele Installationen mit Anwendungen verwenden möchten, die nicht für die öffentliche Verteilung vorgesehen sind.

Bei einer Aktion zur gleichzeitigen Installation wird während einer aktuell ausgeführten Installation ein weiteres Windows Installer Paket installiert. Eine parallele Installation wird einem Paket hinzugefügt, indem eine parallele Installations Aktion in der [Tabelle "CustomAction](customaction-table.md) " und die benutzerdefinierte Aktion in den Sequenz Tabellen geplant wird. Das Zielfeld der CustomAction-Tabelle enthält eine Zeichenfolge der öffentlichen Eigenschafts Einstellungen, die von der gleichzeitigen Installation verwendet werden. Das Feld "Source" der Tabelle "CustomAction" identifiziert das gleichzeitige Paket. Bei einer Aktion zur gleichzeitigen Installation kann eine Anwendung, die vom Installationspaket der aktuellen Anwendung installiert wurde, nur erneut installiert oder entfernt werden.

Der Typ der gleichzeitigen Installation wird im type-Feld der CustomAction-Tabelle angegeben. Abhängig vom benutzerdefinierten Aktionstyp kann sich das Paket für die parallele Anwendung in einem unter Speicher des Haupt Pakets befinden, als Datei an einem Speicherort, der durch eine Eigenschaft angegeben wird, oder als angekündigte Anwendung auf dem Computer des Benutzers. Die folgenden Typen von benutzerdefinierten Aktionen führen eine parallele Installation durch.



| Benutzerdefinierter Aktionstyp                                 | BESCHREIBUNG                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 7](custom-action-type-7.md)   | Parallele Installation eines Produkts im Installationspaket.      |
| [Benutzerdefinierter Aktionstyp 23](custom-action-type-23.md) | Gleichzeitige Installation eines Installer-Pakets innerhalb der aktuellen Quell Struktur. |
| [Benutzerdefinierter Aktionstyp 39](custom-action-type-39.md) | Gleichzeitige Installation eines angekündigten Installer-Pakets.                     |



 

Bei einer gleichzeitigen Installation werden die gleichen Einstellungen für die Benutzeroberfläche und die Protokollierung wie bei der Haupt Installation durch

Gleichzeitige Installations Aktionen sollten zwischen der Aktion [installinitialisieren](installinitialize-action.md) und der Aktion [InstallFinalize](installfinalize-action.md) der Aktions Sequenz der Haupt Installation durchgesetzt werden. Bei einem Rollback der Haupt Installation führt das Installationsprogramm ein Rollback der gleichzeitigen Installation aus. Die Verwendung der [verzögerten Ausführung](deferred-execution-custom-actions.md) mit gleichzeitigen Installations Aktionen ist nicht erforderlich, da das Installationsprogramm Rollback-Informationen aus den parallelen und Haupt Installationen kombiniert. Alle Änderungen werden bei einer Rollback-Installation rückgängig gemacht.

Die Rückgabewerte für gleichzeitige Installations Aktionen sind identisch mit denen für andere benutzerdefinierte Aktionen. Siehe [Rückgabewerte für benutzerdefinierte Aktionen](custom-action-return-values.md).

Standard mäßige oder benutzerdefinierte Aktionen, die einen automatischen Neustart des Systems angeben oder den Neustart des Benutzers anfordern, können auch einen Neustart oder eine Anforderung von innerhalb einer gleichzeitigen Installation ausführen.

Sobald der Installer eine parallele Installation startet, sperrt er alle anderen Installationen, bis die parallele Installation fertiggestellt ist und die Haupt Installation fortgesetzt wird. Das Installationsprogramm kann nur parallele Installationen als synchrone benutzerdefinierte Aktionen ausführen. Siehe [synchrone und asynchrone benutzerdefinierte Aktionen](synchronous-and-asynchronous-custom-actions.md). Die in [benutzerdefinierte Aktion Rückgabe Verarbeitungsoptionen](custom-action-return-processing-options.md) beschriebenen Optionsflags müssen auf None (+ 0) oder **msidbcustomaction typecontinue** (+ 64) festgelegt werden.

Eine parallele Installations Aktion kann eine Anwendung installieren, die lokal ausgeführt, von der Quelle ausgeführt, neu installiert oder auf dieselbe Weise wie bei Verwendung von [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) für eine reguläre Installation entfernt werden soll. Um den Installationstyp anzugeben, übergeben Sie die [**ADDLOCAL**](addlocal.md)-, [**addsource**](addsource.md)-, [**neuinstall**](reinstall.md)-oder [**Remove**](remove.md) -Eigenschaft an die parallel Installation-Aktion.

Gleichzeitige Installations Aktionen können paarweise, eine Aktion, die für die Installation von verwendet wird, und die andere Aktion zum Entfernen der gleichzeitigen Installation erstellt werden. Der [benutzerdefinierte Aktionstyp 7](custom-action-type-7.md) oder der [benutzerdefinierte Aktionstyp 23](custom-action-type-23.md) wird normalerweise zur Installation von verwendet. Der [benutzerdefinierte Aktionstyp 39](custom-action-type-39.md) wird normalerweise verwendet, um die gleichzeitige Installation zu entfernen, wenn das übergeordnete Produkt deinstalliert wird. Der Datensatz für die benutzerdefinierte Aktion "entfernen" in der [Tabelle "CustomAction](customaction-table.md) " kann die Produktcode-GUID im Feld "Source" und "Remove = All" im Feld "target" aufweisen. Die zwei benutzerdefinierten Aktionen müssen in der Aktions Sequenz Tabelle mit sich gegenseitig ausschließenden Bedingungen erstellt werden. Beispielsweise kann die benutzerdefinierte Aktion, mit der das Produkt installiert wird, "nicht installiert" im Feld "Bedingung" aufweisen, und die benutzerdefinierte Aktion entfernt die parallele Installation kann "Remove =" All "im Feld" Bedingung "aufweisen.

Es gibt keine Methode zum Abfragen eines Pakets, um die Kosten zu beheben. Dies erschwert die Kosten für gleichzeitige Installationen. Der [Tabelle ReserveCost](reservecost-table.md) müssen Zeilen hinzugefügt werden, um die Ordner und die schlechtesten Kosten der Komponente anzugeben, die mit der gleichzeitigen Installation verknüpft ist.

Die einzige [benutzerdefinierte Aktion zur Rückgabe von Verarbeitungsoptionen](custom-action-return-processing-options.md) , die für gleichzeitige Installations Aktionen verfügbar sind, sind None (+ 0) oder **msidbcustomaction typecontinue** (+ 64).

Beachten Sie, dass eine übergeordnete Installation das eigene Paket nicht als parallele Installations Aktion aufruft.

Beachten Sie Folgendes: Wenn bei einer Installation pro Computer versucht wird, eine parallele Installation pro Benutzer auszuführen, registriert das Installationsprogramm die übergeordnete Installation standardmäßig als Benutzer pro Benutzer. Dies kann bewirken, dass das Installationsprogramm die Anwendung fälschlicherweise entfernt, da das Installationsprogramm versucht, die Anwendung pro Computer zu deinstallieren, wenn Sie tatsächlich als Benutzer pro Benutzer registriert ist. Um den Zustand einer parallelen Installation zu erzwingen, um den Status der übergeordneten Installation zu überprüfen, geben Sie ALLUSERS = " \[ ALLUSERS \] " in die Ziel Spalte der [CustomAction-Tabelle](customaction-table.md)ein. In diesem Fall ist die parallele Installation pro Computer, wenn das übergeordnete Objekt pro Computer ist, und die gleichzeitige Installation erfolgt pro Benutzer, wenn das übergeordnete Element pro Benutzer ist.

Beim Erstellen gleichzeitiger Installationen sollten Entwickler die folgenden Warnungen beachten:

-   Parallele Installationen können keine Komponenten gemeinsam verwenden.
-   Eine administrative Installation kann nicht gleichzeitig eine parallele Installation enthalten.
-   Das Patchen und Aktualisieren funktioniert möglicherweise nicht mit gleichzeitigen Installationen.
-   Das Installationsprogramm kann eine gleichzeitige Installation nicht ordnungsgemäß Kosten.
-   Integrierte progressbars können nicht mit gleichzeitigen Installationen verwendet werden.
-   Ressourcen, die angekündigt werden sollen, können von der gleichzeitigen Installation nicht installiert werden.
-   Ein Paket, das eine parallele Installation einer Anwendung ausführt, sollte auch die gleichzeitige Anwendung deinstallieren, wenn das übergeordnete Produkt deinstalliert wird.

Fügen Sie der [LaunchCondition](launchcondition-table.md) -Tabelle eine der folgenden Bedingungs Anweisungen hinzu, um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird. Dadurch wird verhindert, dass das Paket jemals durch eine parallele Installations Aktion installiert wird, die von einer anderen Installation ausgeführt wird. Dies verhindert nicht, dass das Paket von der Aktion " [RemoveExistingProducts](removeexistingproducts-action.md) " entfernt wird. Weitere Informationen finden Sie auch in der Eigenschaft " [**parametenoriginaldatabase**](parentoriginaldatabase.md) " und der Eigenschaft " [**parametcode**](parentproductcode.md) ".

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



