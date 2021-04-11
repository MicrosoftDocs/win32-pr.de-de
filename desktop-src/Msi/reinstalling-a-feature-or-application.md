---
description: Windows Installer können Dateien reparieren, ersetzen und überprüfen, die in einer Anwendung enthalten sind. Eine teilweise oder vollständige Neuinstallation der Anwendung ist möglicherweise erforderlich, wenn Dateien oder Registrierungseinträge, die einer Funktion zugeordnet sind, fehlen oder beschädigt sind.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Neuinstallieren eines Features oder einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131613"
---
# <a name="reinstalling-a-feature-or-application"></a>Neuinstallieren eines Features oder einer Anwendung

Windows Installer können Dateien reparieren, ersetzen und überprüfen, die in einer Anwendung enthalten sind. Eine teilweise oder vollständige Neuinstallation der Anwendung ist möglicherweise erforderlich, wenn Dateien oder Registrierungseinträge, die einer Funktion zugeordnet sind, fehlen oder beschädigt sind.

Wenn ein Feature oder eine Anwendung neu installiert wird, werden alle Dienste, Umgebungsvariablen und benutzerdefinierten Aktionen, die zu dem Feature oder der Anwendung gehören, ebenfalls neu installiert. Dies bedeutet, dass alle Änderungen, die an Umgebungsvariablen zwischen der ursprünglichen Installation und der Neuinstallation vorgenommen wurden, verloren gehen.

In der folgenden Liste sind die Methoden zum Neuinstallieren eines Features oder Produkts enthalten. Die ersten beiden Methoden wurden vom Installationsprogramm automatisiert:

-   Reparieren, ersetzen oder überprüfen Sie Dateien, indem Sie die Funktion [**msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) aufrufen.
-   Installieren Sie das gesamte Produkt neu, indem Sie die [**msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) -Funktion aufrufen.
-   Neuinstallieren, ersetzen oder Überprüfen von Dateien mit der Schaltfläche "Installer UI Control" durch die [REINSTALL ControlEvent](reinstall-controlevent.md).
-   Sie können Dateien über eine Befehlszeile neu installieren, ersetzen oder überprüfen, indem Sie die Eigenschaft [**neu installieren**](reinstall.md) und die Eigenschaft [**REINSTALLMODE**](reinstallmode.md) festlegen.

Weitere Informationen zum erneuten Installieren eines Features oder einer Anwendung finden Sie unter [Resilienz](resiliency.md).

**So installieren Sie ein Produkt mithilfe des Installationsprogramms neu**

-   [**Msireinstallproduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)abrufen.

**So installieren Sie ein Feature mithilfe des Installationsprogramms neu**

-   [**Msireinstallfeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)aufruft.

**So installieren Sie ein Produkt oder eine Funktion mit einer Installer-Benutzeroberfläche neu**

1.  Fügen Sie dem angegebenen Dialogfeld eine Schaltfläche hinzu, indem Sie der [Steuerelement Tabelle](control-table.md)einen Eintrag hinzufügen.
2.  Fügen Sie der ControlEvent-Tabelle eine [REINSTALLMODE-ControlEvent](reinstallmode-controlevent.md) hinzu, wobei die Dialog Feld \_ -und Steuerelement \_ Felder auf das in Schritt 1 erstellte Schaltflächen-Steuerelement verweisen. Geben Sie im Feld Argument eine Zeichenfolge mit den Buchstaben ein, die den gewünschten Neuinstallations Modi entsprechen (die zulässigen Werte für dieses Feld sind identisch mit denen, die für die Eigenschaft [**REINSTALLMODE**](reinstallmode.md) akzeptiert werden). Der Wert in der Spalte Reihenfolge für dieses Ereignis sollte 1 lauten.
3.  Fügen Sie der [ControlEvent-Tabelle](controlevent-table.md)ein [REINSTALL ControlEvent](reinstall-controlevent.md) -Ereignis hinzu, das wiederum auf dasselbe Schaltflächen-Steuerelement verweist. Das Argument Feld für dieses Ereignis ist normalerweise alle, um eine Neuinstallation aller Features zu erzwingen, aber Sie können den Namen eines bestimmten Features hier platzieren. Der Wert in der Spalte Reihenfolge für dieses Ereignis sollte 2 lauten.
4.  Fügen Sie ein Ereignis hinzu, das an dasselbe Schaltflächen-Steuerelement gebunden ist, um die Neuinstallation tatsächlich zu initiieren. Dabei kann es sich um ein EndDialog-Ereignis (mit dem Argument Return) handeln. In der Regel wird jedoch hier ein newdialog-Ereignis verwendet, um zu einer zu wechseln, **die Sie wirklich neu installieren möchten?** Bestätigungs Dialogfeld. Der Wert in der Spalte Reihenfolge für dieses Ereignis sollte 3 lauten.

    Wenn gewünscht, können mehrere [**Neuinstallations Schaltflächen**](reinstall.md) für ein einzelnes Dialogfeld erstellt werden, sodass der Benutzer den Typ der durchgeführten Neuinstallation auswählen kann. In diesem Fall wird jede Schaltfläche wie in der vorherigen Prozedur beschrieben erstellt, mit einem anderen [REINSTALLMODE-ControlEvent](reinstallmode-controlevent.md) -Parameter für jede Schaltfläche.

Nachdem ein bestimmtes Produkt installiert wurde (mit einigen oder allen Features des Produkts), kann eine erneute Installation über die Befehlszeile ausgeführt werden:

**So installieren Sie ein Produkt oder Feature über eine Befehlszeile neu**

1.  Geben Sie an der Eingabeaufforderung die Eigenschaft [**neu installieren**](reinstall.md) an.
2.  Geben Sie an der Eingabeaufforderung die [**REINSTALLMODE**](reinstallmode.md) -Eigenschaft an.

    Wenn Sie diese Eigenschaften angeben, kann der Benutzer alle Features des Produkts neu installieren. Der Typ der erneuten Installation kann auch angegeben werden. Sie können z. b. angeben, dass nur die Dateien, die vollständig fehlen, neu installiert werden sollen, oder dass nur beschädigte Dateien (z. b. jede ausführbare Datei, deren Prüfsumme nicht mit dem tatsächlichen Dateiinhalt identisch ist) ersetzt werden sollen.

 

 



