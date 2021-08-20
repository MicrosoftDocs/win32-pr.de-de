---
description: Gleichzeitige Installationen, auch als geschachtelte Installationen bezeichnet, sind ein veraltetes Feature des Windows Installers.
ms.assetid: 579ae4ee-47a0-440e-81ca-ea8bf60c5349
title: Gleichzeitige Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09264df8c47c08f7d1512b46d65572d3572d5190f960254c8ed13182dd668657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118144407"
---
# <a name="concurrent-installations"></a>Gleichzeitige Installationen

Gleichzeitige Installationen, auch als geschachtelte Installationen bezeichnet, sind ein veraltetes Feature des Windows Installers. Anwendungen, die mit gleichzeitigen Installationen installiert werden, können schließlich fehlschlagen, da sie für Kunden schwierig zu bedienen sind. Verwenden Sie keine gleichzeitigen Installationen, um Produkte zu installieren, die für die Veröffentlichung in der Öffentlichkeit vorgesehen sind. Gleichzeitige Installationen können in kontrollierten Unternehmensumgebungen eingeschränkt anwendbar sein, wenn sie zum Installieren von Anwendungen verwendet werden, die nicht für die öffentliche Veröffentlichung vorgesehen sind. Die Dokumentation zu gleichzeitigen Installationen wird für Paketautoren bereitgestellt, die gleichzeitige Installationen mit Anwendungen verwenden möchten, die nicht für die öffentliche Verteilung vorgesehen sind.

Eine gleichzeitige Installationsaktion installiert während einer aktuell ausgeführten Installation ein weiteres Windows Installer-Pakets. Eine gleichzeitige Installation wird einem Paket hinzugefügt, indem eine parallele Installationsaktion in der [Tabelle CustomAction](customaction-table.md) erstellt und diese benutzerdefinierte Aktion in den Sequenztabellen geplant wird. Das Feld Target der Tabelle CustomAction enthält eine Zeichenfolge mit öffentlichen Eigenschafteneinstellungen, die von der gleichzeitigen Installation verwendet werden. Das Feld Quelle der Tabelle CustomAction identifiziert das gleichzeitige Paket. Eine gleichzeitige Installationsaktion kann nur eine Anwendung neu installieren oder entfernen, die vom Installationspaket der aktuellen Anwendung installiert wurde.

Der Typ der gleichzeitigen Installationsaktion wird im Feld Typ der Tabelle CustomAction angegeben. Abhängig vom benutzerdefinierten Aktionstyp kann sich das Paket für die gleichzeitige Anwendung in einer Unterspeicherung des Hauptpakets, als Datei an einem durch eine Eigenschaft angegebenen Speicherort oder als angekündigte Anwendung auf dem Computer des Benutzers befinden. Die folgenden Arten von benutzerdefinierten Aktionen führen eine gleichzeitige Installation durch.



| Benutzerdefinierter Aktionstyp                                 | Beschreibung                                                                     |
|----------------------------------------------------|---------------------------------------------------------------------------------|
| [Benutzerdefinierter Aktionstyp 7](custom-action-type-7.md)   | Gleichzeitige Installation eines Produkts im Installationspaket.      |
| [Benutzerdefinierter Aktionstyp 23](custom-action-type-23.md) | Gleichzeitige Installation eines Installationspakets innerhalb der aktuellen Quellstruktur. |
| [Benutzerdefinierter Aktionstyp 39](custom-action-type-39.md) | Gleichzeitige Installation eines angekündigten Installationspakets.                     |



 

Eine gleichzeitige Installation verwendet die gleiche Benutzeroberfläche und die gleichen Protokollierungseinstellungen wie die Hauptinstallation.

Gleichzeitige Installationsaktionen sollten zwischen der [Aktion InstallInitialize](installinitialize-action.md) und der [InstallFinalize-Aktion](installfinalize-action.md) der Aktionssequenz der Hauptinstallation platziert werden. Beim Rollback der Hauptinstallation führt das Installationsprogramm dann auch ein Rollback für die gleichzeitige Installation aus. Die Verwendung der [verzögerten Ausführung](deferred-execution-custom-actions.md) mit gleichzeitigen Installationsaktionen ist nicht erforderlich, da das Installationsprogramm Rollbackinformationen von gleichzeitigen und Hauptinstallationen kombiniert. Alle Änderungen werden bei einer Rollbackinstallation rückgängig gemacht.

Die Rückgabewerte für gleichzeitige Installationsaktionen sind identisch mit denen für andere benutzerdefinierte Aktionen. Weitere Informationen finden Sie unter [Rückgabewerte für benutzerdefinierte Aktionen.](custom-action-return-values.md)

Standardaktionen oder benutzerdefinierte Aktionen, die einen automatischen Neustart des Systems angeben oder den Benutzer zum Neustart auffordern, können auch einen Neustart oder eine Anforderung innerhalb einer gleichzeitigen Installation ausführen.

Sobald das Installationsprogramm eine gleichzeitige Installation startet, sperrt es alle anderen Installationen, bis die gleichzeitige Installation abgeschlossen ist und bevor die Hauptinstallation fortgesetzt wird. Das Installationsprogramm kann gleichzeitige Installationen nur als synchrone benutzerdefinierte Aktionen ausführen. Weitere Informationen finden Sie unter [Synchrone und asynchrone benutzerdefinierte Aktionen.](synchronous-and-asynchronous-custom-actions.md) Die unter [Benutzerdefinierte Aktion Rückgabeverarbeitungsoptionen](custom-action-return-processing-options.md) beschriebenen Optionsflags müssen auf none (+0) oder **msidbCustomActionTypeContinue** (+64) festgelegt werden.

Eine gleichzeitige Installationsaktion kann eine Anwendung installieren, die lokal, von der Quelle ausgeführt, neu installiert oder auf die gleiche Weise wie bei der Verwendung von [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) für eine reguläre Installation entfernt werden soll. Um den Installationstyp anzugeben, übergeben Sie entweder die Eigenschaft [**ADDLOCAL,**](addlocal.md) [**ADDSOURCE,**](addsource.md) [**REINSTALL**](reinstall.md)oder [**REMOVE**](remove.md) an die gleichzeitige Installationsaktion.

Gleichzeitige Installationsaktionen können in Paaren erstellt werden, eine Aktion, die für die Installation verwendet wird, und die andere Aktion, die zum Entfernen der gleichzeitigen Installation verwendet wird. Ein [benutzerdefinierter Aktionstyp 7](custom-action-type-7.md) oder [benutzerdefinierter Aktionstyp 23](custom-action-type-23.md) wird normalerweise für die Installation verwendet. Ein [benutzerdefinierter Aktionstyp 39](custom-action-type-39.md) wird normalerweise verwendet, um die gleichzeitige Installation zu entfernen, wenn das übergeordnete Produkt deinstalliert wird. Der Datensatz für die benutzerdefinierte Aktion zum Entfernen in der [Tabelle CustomAction](customaction-table.md) kann die Produktcode-GUID im Feld Quelle und "REMOVE=ALL" im Feld Ziel enthalten. Die beiden benutzerdefinierten Aktionen müssen in der Aktionssequenztabelle mit sich gegenseitig ausschließenden Bedingungen erstellt werden. Für die benutzerdefinierte Aktion, die das Produkt installiert, kann beispielsweise "NOT Installed" im Feld Bedingung enthalten sein, und die benutzerdefinierte Aktion entfernt die gleichzeitige Installation und kann REMOVE="ALL" im Feld Bedingung enthalten.

Es gibt keine Methode zum Abfragen der Kosten eines Pakets. Dies erschwert die Kosten für gleichzeitige Installationen. Zeilen müssen der [ReserveCost-Tabelle](reservecost-table.md) hinzugefügt werden, um die Ordner und im schlimmsten Fall die Kosten der Komponente anzugeben, die der gleichzeitigen Installation zugeordnet ist.

Die einzigen optionen für [die Rückgabeverarbeitung benutzerdefinierter Aktionen,](custom-action-return-processing-options.md) die mit gleichzeitigen Installationsaktionen verfügbar sind, sind none (+0) oder **msidbCustomActionTypeContinue** (+64).

Beachten Sie, dass eine übergeordnete Installation kein eigenes Paket als gleichzeitige Installationsaktion aufrufen kann.

Beachten Sie Folgendes: Wenn bei einer Installation pro Computer versucht wird, eine gleichzeitige Installation pro Benutzer auszuführen, registriert das Installationsprogramm die übergeordnete Installation standardmäßig als benutzerspezifische Installation. Dies kann dazu führen, dass das Installationsprogramm die Anwendung falsch entfernt, da das Installationsprogramm versucht, die Anwendung pro Computer zu deinstallieren, wenn sie tatsächlich als pro Benutzer registriert ist. Um zu erzwingen, dass der Status einer gleichzeitigen Installation den Status der übergeordneten Installation nachverfolgt, geben Sie ALLUSERS=" \[ ALLUSERS \] " in die Target -Spalte der [CustomAction-Tabelle](customaction-table.md)ein. In diesem Fall erfolgt die gleichzeitige Installation pro Computer, wenn das übergeordnete Element pro Computer ist, und die gleichzeitige Installation pro Benutzer, wenn das übergeordnete Element pro Benutzer ist.

Entwickler sollten beim Erstellen gleichzeitiger Installationen die folgenden Warnungen beachten.

-   Gleichzeitige Installationen können keine Komponenten gemeinsam nutzen.
-   Eine Administratorinstallation darf keine gleichzeitige Installation enthalten.
-   Das Patchen und Aktualisieren funktioniert möglicherweise nicht mit gleichzeitigen Installationen.
-   Das Installationsprogramm kostet eine gleichzeitige Installation möglicherweise nicht ordnungsgemäß.
-   Integrierte ProgressBars können nicht mit gleichzeitigen Installationen verwendet werden.
-   Ressourcen, die angekündigt werden sollen, können von der gleichzeitigen Installation nicht installiert werden.
-   Ein Paket, das eine gleichzeitige Installation einer Anwendung ausführt, sollte auch die gleichzeitige Anwendung deinstallieren, wenn das übergeordnete Produkt deinstalliert wird.

Um zu verhindern, dass ein Paket jemals als gleichzeitige Installation installiert wird, fügen Sie der [LaunchCondition-Tabelle](launchcondition-table.md) eine der folgenden bedingten Anweisungen hinzu. Dadurch wird verhindert, dass das Paket jemals von einer gleichzeitigen Installationsaktion installiert wird, die von einer anderen Installation ausgeführt wird. Dies verhindert nicht, dass das Paket durch die [RemoveExistingProducts-Aktion](removeexistingproducts-action.md) entfernt wird. Siehe auch die [**ParentOriginalDatabase-Eigenschaft**](parentoriginaldatabase.md) und die [**ParentProductCode-Eigenschaft.**](parentproductcode.md)

``` syntax
"Not ParentProductCode"
```

``` syntax
"Not ParentOriginalDatabase"
```

 

 



