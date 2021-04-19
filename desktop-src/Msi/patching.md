---
description: In diesen Abschnitten wird das Patchen einer Windows Installer-Installation beschrieben.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Patching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3117723bda1699eeae341fc75db201421f6ae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359578"
---
# <a name="patching"></a>Patching

Eine Anwendung, die mithilfe des Microsoft Windows Installer installiert wurde, kann durch erneutes Installieren eines aktualisierten Installationspakets (MSI-Datei) oder durch Anwenden eines Windows Installer Patches (MSP-Datei) auf die Anwendung aktualisiert werden.

Ein Windows Installer Patch (MSP-Datei) ist ein eigenständiges Paket, das die Updates für die Anwendung enthält und beschreibt, welche Versionen der Anwendung den Patch empfangen können. Patches enthalten mindestens zwei Daten Bank Transformationen und können Patchdateien enthalten, die im CAB-Datei Datenstrom des Patchpakets gespeichert werden. Weitere Informationen zu den Teilen eines Windows Installer Patchpakets finden Sie unter [Patch-Pakete](patch-packages.md).

Die Wartung von Anwendungen durch die Bereitstellung eines Windows Installer Patch anstelle eines kompletten Installationspakets für das aktualisierte Produkt kann Vorteile haben. Ein Patch kann eine ganze Datei oder nur die Datei Bits enthalten, die zum Aktualisieren eines Teils der Datei erforderlich sind. Dadurch kann der Benutzer einen Upgradepatch herunterladen, der wesentlich kleiner ist als das Installationspaket für das gesamte Produkt. Ein Update mit einem Patch kann eine Benutzeranpassung der Anwendung über das Upgrade erhalten.

* * Windows Installer 4,5 und höher: * *

Ab Windows Installer 4,5 können Entwickler Komponenten in einem Patch mit dem **msidbcomponentattributesuninstallonablösung** -Wert in der [Component-Tabelle](component-table.md)markieren. Wenn ein späterer Patch installiert wird, der mit dem **msidbpatchsequencesupersedefrüher** -Wert in der [msipatchsequence-Tabelle](msipatchsequence-table.md) gekennzeichnet ist, um den ersten Patch zu ersetzen, können Windows Installer 4,5 und höher die Registrierung aufheben und die Komponenten deinstallieren, die mit " **msidbcomponentattributesuninstallonablösung** " gekennzeichnet sind. Wenn die Komponente mit diesem Bit nicht mit markiert ist, kann die Installation des ersetzenden Patches eine nicht verwendete Komponente auf dem Computer belassen. Das Festlegen der **msiuninstallablösung dedcomponents** -Eigenschaft hat dieselbe Auswirkung wie das Festlegen dieses Bits für alle Komponenten.

* * Windows Installer 3,0 und höher: * *

Entwickler, die Windows Installer 3,0 verwenden und Patchpakete mit der [msipatchsequence-Tabelle](msipatchsequence-table.md) erstellen, können Patchpakete erstellen, die folgende Aktionen ausführen:

-   Verwenden Sie die vom Installer zwischengespeicherte Produktbasis Linie, um Anwendungen mit kleineren Delta Patches leichter zu bedienen. Weitere Informationen zur Verwendung der Product Baseline finden Sie unter [verringern der Patchgröße](reducing-patch-size.md).
-   Überspringen Sie Aktionen im Zusammenhang mit bestimmten Tabellen, die vom Patch nicht geändert werden. Dies kann die erforderliche Zeit für die Installation des Patches erheblich verkürzen. Weitere Informationen zu den Tabellen, die übersprungen werden können, finden Sie unter [Patch Optimization](patch-optimization.md).
-   Erstellen und installieren Sie Patches, die einzeln und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu müssen. Weitere Informationen zum Deinstallieren von Patches finden Sie unter [Entfernen von Patches](removing-patches.md).
-   Anwenden von Patches in konstanter Reihenfolge, unabhängig von der Reihenfolge, in der die Patches dem System bereitgestellt werden. Weitere Informationen dazu, wie die Windows Installer die zum Anwenden von Patches verwendete Sequenz bestimmt, finden Sie unter [Sequenzieren von Patches](sequencing-patches.md).
-   Anwenden von Patches auf eine Anwendung, die in einem pro Benutzer verwalteten Kontext installiert wurde. Weitere Informationen finden Sie unter [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).

* * Windows Installer 2,0: * *

Die [msipatchsequence-Tabelle](msipatchsequence-table.md) wird nicht unterstützt. Ab Windows Installer 3,0 können Patchpakete Informationen enthalten, die die patchsequenz für den Patch relativ zu anderen Updates und weitere beschreibende Informationen beschreiben.

Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zur Patcherstellung, wie z. b. [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md). Entwickler können eine patcherstellungs Datei generieren, wie im Abschnitt: [Erstellen eines Patchpakets](creating-a-patch-package.md)beschrieben. Die Erstellung eines Patch für kleine Updates wird im folgenden Abschnitt beschrieben: [Beispiel für das Patchen von kleinen Updates](a-small-update-patching-example.md).

Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen Patch. Weitere Informationen zum Installieren eines Patches, der sich auf einem Webserver befindet, finden Sie unter [herunterladen und Installieren eines Patches aus dem Internet](downloading-and-installing-a-patch-from-the-internet.md).

Wenn eine Anwendung zum ersten Mal installiert wird, kann ein einzelner Windows Installer Patch (. msp-Datei) auf das Installationspaket angewendet werden. Weitere Informationen finden Sie unter [Patchen von anfänglichen Installationen](patching-initial-installations.md).

Es ist nicht möglich, alle Umstände auszuschließen, wenn für die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erforderlich ist. Beachten Sie jedoch die im folgenden Abschnitt aufgeführten Punkte, um die Möglichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprüngliche Quelle benötigt: [verhindern, dass ein Patch Zugriff auf die ursprüngliche Installationsquelle benötigt](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md).

Um die Möglichkeit zu minimieren, dass Ihr Patch durch eine nachfolgende Anpassungs Transformation nicht beschädigt wird, wird der Patch in der Regel zuerst installiert, gefolgt von der Anpassung. Wenn Sie Anpassungs Transformationen zuerst installieren, und dann der Patch, kann die Anpassung möglicherweise unterbrechen. Weitere Informationen zum Patchen von angepassten Anwendungen finden Sie unter [Patchen von angepassten Anwendungen](patching-customized-applications.md).

 

 



