---
description: Windows Das Installationsprogramm kann Dateien reparieren, ersetzen und überprüfen, die in einer Anwendung enthalten sind. Eine teilweise oder vollständige Neuinstallation der Anwendung ist möglicherweise erforderlich, wenn Dateien oder Registrierungseinträge, die einem Feature zugeordnet sind, fehlen oder beschädigt sind.
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: Erneutes Installieren eines Features oder einer Anwendung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 803fc3271cb69280ae84ae096e7a411dbf599f0a321bf15baac6dbd5ca8e1512
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120086000"
---
# <a name="reinstalling-a-feature-or-application"></a>Erneutes Installieren eines Features oder einer Anwendung

Windows Das Installationsprogramm kann Dateien reparieren, ersetzen und überprüfen, die in einer Anwendung enthalten sind. Eine teilweise oder vollständige Neuinstallation der Anwendung ist möglicherweise erforderlich, wenn Dateien oder Registrierungseinträge, die einem Feature zugeordnet sind, fehlen oder beschädigt sind.

Wenn ein Feature oder eine Anwendung neu installiert wird, werden auch alle Dienste, Umgebungsvariablen und benutzerdefinierten Aktionen, die zum Feature oder zur Anwendung gehören, neu installiert. Beachten Sie, dass dies bedeutet, dass alle Änderungen an Umgebungsvariablen zwischen der ursprünglichen Installation und der Neuinstallation verloren gehen.

Die folgende Liste enthält Methoden zum erneuten Installieren eines Features oder Produkts. Die ersten beiden Methoden wurden vom Installationsprogramm automatisiert:

-   Reparieren, ersetzen oder überprüfen Sie Dateien, indem Sie die [**MsiReinstallFeature-Funktion**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) aufrufen.
-   Installieren Sie das gesamte Produkt erneut, indem Sie die [**MsiReinstallProduct-Funktion**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) aufrufen.
-   Installieren Sie Dateien erneut, ersetzen oder überprüfen Sie sie über die Schaltfläche Install [ControlEvent (ControlEvent neu installieren)](reinstall-controlevent.md)mit einem Benutzeroberflächen-Steuerelement für das Installationsprogramm.
-   Installieren, ersetzen oder überprüfen Sie Dateien über eine Befehlszeile, indem Sie die [**REINSTALL-Eigenschaft**](reinstall.md) und die [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) festlegen.

Weitere Informationen zum erneuten Installieren eines Features oder einer Anwendung finden Sie unter [Resilienz](resiliency.md).

**So installieren Sie ein Produkt mithilfe des Installationsprogramms neu**

-   Rufen Sie [**MsiReinstallProduct auf.**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)

**So installieren Sie ein Feature mithilfe des Installationsprogramms neu**

-   Rufen [**Sie MsiReinstallFeature auf.**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)

**So installieren Sie ein Produkt oder Feature mit einer Installer-Benutzeroberfläche neu**

1.  Fügen Sie dem angegebenen Dialogfeld eine Schaltfläche hinzu, indem Sie der [Control-Tabelle einen Eintrag hinzufügen.](control-table.md)
2.  Fügen Sie der ControlEvent-Tabelle ein [ReinstallMode ControlEvent](reinstallmode-controlevent.md) hinzu, und verweisen die Felder Dialog und Control auf das in Schritt 1 erstellte \_ \_ Schaltflächen-Steuerelement. Geben Sie im Feld Argument eine Zeichenfolge ein, die die Buchstaben enthält, die den von Ihnen unterstützten Neuinstallationsmodi (die zulässigen Werte für dieses Feld sind identisch mit denen, die für die [**REINSTALLMODE-Eigenschaft akzeptiert**](reinstallmode.md) werden). Der Wert in der Spalte Ordering für dieses Ereignis sollte 1 sein.
3.  Fügen Sie der [ControlEvent-Tabelle](reinstall-controlevent.md) ein Neuinstallationsereignis für [ControlEvent hinzu,](controlevent-table.md)das wiederum auf das gleiche Schaltflächensteuerfeld zeigt. Das Argumentfeld für dieses Ereignis ist normalerweise ALL, um die Neuinstallation aller Features zu erzwingen. Sie können den Namen eines bestimmten Features jedoch hier platzieren. Der Wert in der Spalte Ordering für dieses Ereignis sollte 2 sein.
4.  Fügen Sie ein zusätzliches Ereignis hinzu, das an dasselbe Schaltflächensteuerfeld gebunden ist, um die Neuinstallation tatsächlich zu initiieren. Dies kann ein EndDialog-Ereignis (mit dem Argument Return) sein. In der Regel wird hier jedoch ein NewDialog-Ereignis verwendet, um zum Bestätigungsdialogfeld Möchten Sie sicher sein, dass Sie neu installieren **möchten?** zu springen. Der Wert in der Spalte Ordering für dieses Ereignis sollte 3 sein.

    Bei Wunsch können mehrere [**REINSTALL-Schaltflächen**](reinstall.md) für ein einzelnes Dialogfeld erstellt werden, sodass der Benutzer den Typ der durchgeführten Neuinstallation auswählen kann. In diesem Fall wird jede Schaltfläche wie im vorherigen Verfahren beschrieben mit einem anderen [ReinstallMode ControlEvent-Parameter](reinstallmode-controlevent.md) für jede Schaltfläche verfasst.

Nachdem ein bestimmtes Produkt installiert wurde (mit einigen oder allen Features des Produkts), kann eine Neuinstallation über die Befehlszeile durchgeführt werden:

**So installieren Sie ein Produkt oder Feature über eine Befehlszeile neu**

1.  Geben Sie an der Eingabeaufforderung die [**REINSTALL-Eigenschaft**](reinstall.md) an.
2.  Geben Sie an der Eingabeaufforderung die [**REINSTALLMODE-Eigenschaft**](reinstallmode.md) an.

    Wenn Sie diese Eigenschaften angeben, kann der Benutzer alle Features des Produkts neu installieren. Der Typ der Neuinstallation kann ebenfalls angegeben werden. Beispielsweise können Sie angeben, dass nur die Dateien, die vollständig fehlen, neu installiert werden sollen oder dass nur beschädigte Dateien (z. B. ausführbare Dateien, deren Prüfsumme nicht mit dem tatsächlichen Dateiinhalt übereinstimmen) ersetzt werden sollen.

 

 



