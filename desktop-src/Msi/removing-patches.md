---
description: Ab Windows Installer&\# 160;Version&160;3.0 ist es möglich, Patches zu erstellen und zu installieren, die singingiert und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu \# müssen.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Entfernen von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18998207ead28729101fd8782432cb25bf31f0d4763faa8e99c341f9b1fde7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117990700"
---
# <a name="removing-patches"></a>Entfernen von Patches

Ab Windows Installer Version 3.0 ist es möglich, Patches zu erstellen und zu installieren, die singly und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu müssen. Windows Installer 3.0 ermöglicht auch das Erstellen von [Patchpaketen](patch-packages.md) mit einer [MsiPatchSequence-Tabelle,](msipatchsequence-table.md) die Informationen zur Patchsequenzierung enthält. Bei Versionen des Windows Installers vor Windows Installer 3.0 besteht die einzige Methode zum Entfernen bestimmter Patches aus einer Anwendung in der Deinstallation der gesamten gepatchten Anwendung und der anschließenden Neuinstallation, ohne dass patches entfernt werden.

Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch verfasst wurde, welche Version des Windows Installers zum Installieren des Patches verwendet wird und welche Änderungen der Patch an der Anwendung vorgenommen hat. Wenn ein Patch nicht deinstalliert werden kann, besteht die einzige Möglichkeit zum Entfernen des Patches in der Deinstallation der gesamten Anwendung und der Neuinstallation, ohne dass der Patch entfernt wird.

Sie können ein oder mehrere Patches mithilfe einer Befehlszeilenoption, der Skriptschnittstelle oder durch Aufrufen von [**MsiRemovePatches aus einer**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) anderen Anwendung deinstallieren. Weitere [Informationen zum Deinstallieren von Patches](uninstalling-patches.md) finden Sie unter Deinstallieren von Patches.

Der Wert der [**MSIPATCHREMOVE-Eigenschaft**](msipatchremove.md) listet die zu deinstallierenden Patches auf. Für jeden Patch in der Liste überprüft das Installationsprogramm, ob der Patch deinstalliert werden kann. Wenn der Benutzer keine Berechtigungen zum Entfernen des Patches hat, der Patch für das Produkt unbekannt ist, die Patchrichtlinie das Entfernen verhindert oder der Patch als nicht deinstallationsfähig markiert wurde, gibt das Installationsprogramm einen Fehler zurück, der auf eine fehlgeschlagene Installationstransaktion hinweist. Weitere [Informationen dazu, was bestimmt,](uninstallable-patches.md) ob ein Patch nicht deinstalliert werden kann, finden Sie unter Deinstallationsfähige Patches.

Nachdem der Patch als Wechselmedium überprüft wurde, entfernt das Installationsprogramm den Patch aus der Patchanwendungssequenz. Weitere Informationen dazu, wie Windows Installer 3.0 bestimmt, welche Sequenz beim Anwenden von Patches verwendet werden soll, finden Sie unter [Sequenzieren von Patches.](sequencing-patches.md) Beachten Sie, dass das Entfernen von Patches aus der Sequenz dazu führen kann, dass Patches, die als veraltet markiert oder ersetzt wurden, aktiv werden.

Alle patches, die zum Entfernen ausgewählt wurden, werden in der [**MsiPatchRemovalList-Eigenschaft**](msipatchremovallist.md) aufgeführt. Diese Eigenschaft ist eine private Eigenschaft, die vom Installationsprogramm festgelegt wird und in bedingten Ausdrücken verwendet oder von benutzerdefinierten [Aktionen abgefragt werden kann.](custom-actions.md) Die -Eigenschaft enthält die Liste der Patchcode-GUIDs der zu entfernenden Patches. Eine benutzerdefinierte Aktion kann bestimmen, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem [**msiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) oder die [**PatchProperty-Eigenschaft**](patch-patchproperty.md) des [Patchobjekts aufruft.](patch-object.md)

Nachdem ein Patch entfernt wurde, ist der Status der Anwendung identisch mit dem, wenn der Patch nie installiert wurde. Wenn möglich, schränkt das Installationsprogramm den Prozess auf die Teilmenge der Features ein, die vom entfernten Patch betroffen sind. Das Installationsprogramm legt die [**REINSTALL-Eigenschaft**](reinstall.md) automatisch auf die Liste der betroffenen Features fest. Dateien, die durch den Patch hinzugefügt wurden, werden entfernt, und Dateien, die durch den Patch geändert wurden, werden überschrieben. Dateien und Registrierungseinträge werden auf die Version wiederhergestellt, die vom Produkt abzüglich des Patches erwartet wird. Die Registrierung von Features und Komponenten, die durch den Patch hinzugefügt wurden, wird bei der Anwendung aufgehoben. Beachten Sie, dass zusätzliche Inhalte, die vom Patch hinzugefügt werden, auf dem Computer des Benutzers verbleiben können, wenn der Inhalt von einem anderen Patch verwendet wird, der weiterhin anwendbar ist.

Wenn eine Datei einer freigegebenen Komponente durch einen Patch aktualisiert wird, wirkt sich die Änderung auf alle Anwendungen aus, die die Komponente gemeinsam nutzen. Wenn der Patch entfernt wird, wirkt sich die Änderung erneut auf alle Anwendungen aus, die die Komponente gemeinsam nutzen. Dies bedeutet, dass das Entfernen eines Patches durch eine Anwendung die Datei der freigegebenen Komponente auf eine niedrigere Version wiederherstellen kann, als für eine andere Anwendung erforderlich ist. Dies könnte die erste Anwendung beheben, aber dazu führen, dass die zweite Anwendung nicht mehr funktioniert. In diesem Fall kann die zweite Anwendung repariert werden, indem die zweite Anwendung mithilfe der methoden neu installiert wird, die unter [Neuinstallieren](reinstalling-a-feature-or-application.md)eines Features oder einer Anwendung beschrieben sind. Dadurch wird die gepatchte Version der Datei wiederhergestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**MsiEnumapplicationsEx**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**MSIPATCHREMOVE**](msipatchremove.md)
</dt> <dt>

[**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Benutzerdefinierte Aktionen zur Patchdeinstallation](patch-uninstall-custom-actions.md)
</dt> <dt>

[Deinstallationsfähige Patches](uninstallable-patches.md)
</dt> <dt>

[Deinstallieren von Patches](uninstalling-patches.md)
</dt> </dl>

 

 



