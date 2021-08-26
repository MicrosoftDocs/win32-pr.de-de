---
description: In diesen Abschnitten wird das Patchen einer installation Windows Installer beschrieben.
ms.assetid: e3c233bc-4344-449e-9e79-1a3b96ad2d08
title: Patching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb90436c2a33495aaa818d0796c5d749e5d76286db4dbdc247ec4ee58c7ea6ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926236"
---
# <a name="patching"></a>Patching

Eine Anwendung, die mithilfe des Microsoft Windows Installers installiert wurde, kann aktualisiert werden, indem ein aktualisiertes Installationspaket (.msi-Datei) neu installiert oder ein Windows Installer-Patch (eine MSP-Datei) auf die Anwendung angewendet wird.

Ein Windows Installer-Patch (MSP-Datei) ist ein eigenständiges Paket, das die Updates für die Anwendung enthält und beschreibt, welche Versionen der Anwendung den Patch empfangen können. Patches enthalten mindestens zwei Datenbanktransformationen und können Patchdateien enthalten, die im Cab-Dateistream des Patchpakets gespeichert sind. Weitere Informationen zu den Teilen eines Windows Installer-Patchpakets finden Sie unter [Patchpakete](patch-packages.md).

Die Wartung von Anwendungen durch Bereitstellen eines Windows Installer-Patches anstelle eines vollständigen Installationspakets für das aktualisierte Produkt kann Vorteile haben. Ein Patch kann eine ganze Datei oder nur die Dateibits enthalten, die zum Aktualisieren eines Teils der Datei erforderlich sind. Dadurch kann der Benutzer einen Upgradepatch herunterladen, der viel kleiner als das Installationspaket für das gesamte Produkt ist. Ein Update mit einem Patch kann eine Benutzeranpassung der Anwendung durch das Upgrade beibehalten.

**Windows Installer 4.5 und höher: **

Ab Windows Installer 4.5 können Entwickler Komponenten in einem Patch mit dem Wert **msidbComponentAttributesUninstallOnSupersedence** in der [Tabelle Component](component-table.md)markieren. Wenn ein nachfolgender Patch installiert wird, der mit dem **msidbPatchSequenceSupersedeEarlier-Wert** in der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) markiert ist, um den ersten Patch zu ersetzen, kann Windows Installer 4.5 und höher die Registrierung aufheben und Komponenten deinstallieren, die **als msidbComponentAttributesUninstallOnSupersedence** gekennzeichnet sind, um zu verhindern, dass ungenutzte Komponenten auf dem Computer zurückgelassen werden. Wenn die Komponente nicht mit diesem Bit gekennzeichnet ist, kann die Installation des abgelösten Patches eine nicht verwendete Komponente auf dem Computer belassen. Das Festlegen der **MSIUNINSTALLSUPERSEDEDCOMPONENTS-Eigenschaft** hat die gleiche Auswirkung wie das Festlegen dieses Bits für alle Komponenten.

**Windows Installer 3.0 und höher: **

Entwickler, die Windows Installer 3.0 verwenden und Patchpakete mit der [MsiPatchSequence-Tabelle](msipatchsequence-table.md) erstellen, können Patchpakete erstellen, die folgende Schritte ausführen:

-   Verwenden Sie die vom Installationsprogramm zwischengespeicherte Produktbaseline, um Anwendungen mit kleineren Deltapatches einfacher bedienen zu können. Weitere Informationen zur Verwendung der Produktbaseline finden Sie unter Reduzieren der [Patchgröße.](reducing-patch-size.md)
-   Überspringt Aktionen, die bestimmten Tabellen zugeordnet sind, die vom Patch nicht geändert werden. Dies kann den Zeitaufwand für die Installation des Patches erheblich reduzieren. Weitere Informationen dazu, welche Tabellen übersprungen werden können, finden Sie unter [Patchoptimierung.](patch-optimization.md)
-   Erstellen und installieren Sie Patches, die singly und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu müssen. Weitere Informationen zum Deinstallieren von Patches finden Sie unter [Entfernen von Patches.](removing-patches.md)
-   Wenden Sie Patches in einer konstanten Reihenfolge an, unabhängig von der Reihenfolge, in der die Patches für das System bereitgestellt werden. Weitere Informationen dazu, wie der Windows Installer die Sequenz bestimmt, die zum Anwenden von Patches verwendet wird, finden Sie unter [Sequenzieren von Patches.](sequencing-patches.md)
-   Wenden Sie Patches auf eine Anwendung an, die in einem vom Benutzer verwalteten Kontext installiert wurde. Weitere Informationen finden Sie unter [Patching Per-User Managed Applications](patching-per-user-managed-applications.md).

**Windows Installer 2.0: **

Die [MsiPatchSequence-Tabelle](msipatchsequence-table.md) wird nicht unterstützt. Ab Windows Installer 3.0 können Patchpakete Informationen enthalten, die die Patchsequenz für den Patch relativ zu anderen Updates und zusätzliche beschreibende Informationen beschreiben.

Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung von Tools zum Erstellen von Patches wie [Msimsp.exe](msimsp-exe.md) und [Patchwiz.dll](patchwiz-dll.md). Entwickler können eine Patcherstellungsdatei generieren, wie im Abschnitt [Erstellen eines Patchpakets](creating-a-patch-package.md)beschrieben. Die Erstellung eines kleinen Updatepatches wird im Abschnitt [A Small Update Patching Example (Beispiel für ein kleines Updatepatching)](a-small-update-patching-example.md)beschrieben.

Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen Patch. Weitere Informationen zum Installieren eines Patches auf einem Webserver finden Sie unter [Herunterladen und Installieren eines Patches aus dem Internet.](downloading-and-installing-a-patch-from-the-internet.md)

Ein einzelner Windows Installerpatch (MSP-Datei) kann auf das Installationspaket angewendet werden, wenn eine Anwendung zum ersten Mal installiert wird. Weitere Informationen finden Sie unter [Patching Initial Installations](patching-initial-installations.md).

Es ist nicht möglich, alle Umstände auszuschließen, in denen die Anwendung eines Patches möglicherweise Zugriff auf die ursprüngliche Installationsquelle erfordert. Um jedoch die Möglichkeit zu minimieren, dass Ihr Patch Zugriff auf die ursprüngliche Quelle benötigt, befolgen Sie die Im folgenden Abschnitt aufgeführten Punkte: Verhindern, dass [ein Patch Zugriff auf die ursprüngliche Installationsquelle erfordert.](preventing-a-patch-from-requiring-access-to-the-original-installation-source.md)

Um die Möglichkeit zu minimieren, dass Ihr Patch nicht durch eine nachfolgende Anpassungstransformation unterbrochen wird, wird der Patch in der Regel zuerst installiert, gefolgt von der Anpassung. Die Installation von Anpassungstransformationen zuerst und dann des Patches kann die Anpassung unterbrechen. Weitere Informationen zum Patchen benutzerdefinierter Anwendungen finden Sie unter [Patchen benutzerdefinierter Anwendungen.](patching-customized-applications.md)

 

 



