---
description: Ab Windows Installer&\# 160; Version&\# 160; 3.0 ist es möglich, Patches zu erstellen und zu installieren, die einzeln und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu müssen.
ms.assetid: 2ad30ac9-eac9-49cf-98ae-5c053a0b500a
title: Entfernen von Patches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cd54db3bde3a356a0c3adb299555248bbc87a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358992"
---
# <a name="removing-patches"></a>Entfernen von Patches

Ab Windows Installer Version 3,0 ist es möglich, Patches zu erstellen und zu installieren, die einzeln und in beliebiger Reihenfolge deinstalliert werden können, ohne die gesamte Anwendung und andere Patches deinstallieren und neu installieren zu müssen. Windows Installer 3,0 ermöglicht außerdem die Erstellung von [patchpaketen](patch-packages.md) mit einer [msipatchsequence-Tabelle](msipatchsequence-table.md) , die Informationen zur Patchsequenzierung enthält. Bei Versionen Windows Installer von, die älter sind als Windows Installer 3,0, besteht die einzige Möglichkeit, bestimmte Patches aus einer Anwendung zu entfernen, darin, die gesamte gepatchte Anwendung zu deinstallieren und dann erneut zu installieren, ohne die zu entfernenden Patches erneut anzuwenden

Ob ein Patch deinstalliert werden kann, hängt davon ab, wie der Patch erstellt wurde, der Version von Windows Installer, die zur Installation des Patches verwendet wurde, und der Änderungen, die vom Patch an der Anwendung vorgenommen wurden. Wenn ein Patch nicht deinstalliert werden kann, besteht die einzige Möglichkeit zum Entfernen des Patches darin, die gesamte Anwendung zu deinstallieren und neu zu installieren, ohne dass der zu entfernende Patch angewendet wird.

Sie können ein oder mehrere Patches mithilfe der Befehlszeilenoption, der Skript Schnittstelle oder durch Aufrufen von [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa) aus einer anderen Anwendung deinstallieren. Weitere Informationen zum Deinstallieren von Patches finden Sie unter Deinstallieren von [Patches](uninstalling-patches.md) .

Der Wert der Eigenschaft [**msipatchremove**](msipatchremove.md) listet die zu entfernenden Patches auf. Für jeden Patch in der Liste überprüft das Installationsprogramm, ob der Patch nicht installiert werden kann. Wenn der Benutzer nicht über Berechtigungen zum Entfernen des Patches verfügt, ist der Patch für das Produkt unbekannt, die patchrichtlinie verhindert das Entfernen, oder der Patch wurde als nicht deinstallable gekennzeichnet. der Installer gibt einen Fehler zurück, der auf eine fehlgeschlagene Installations Transaktion hinweist. Weitere Informationen zu den Informationen, die bestimmen, ob ein Patch nicht installiert werden kann, finden Sie unter [nicht installierbare Patches](uninstallable-patches.md) .

Nachdem der Patch als Wechsel Datenträger überprüft wurde, entfernt das Installationsprogramm den Patch aus der Patch-Anwendungs Sequenz. Weitere Informationen darüber, wie Windows Installer 3,0 bestimmt, welche Sequenz beim Anwenden von Patches verwendet werden soll, finden Sie unter [Sequenzieren von Patches](sequencing-patches.md). Beachten Sie, dass das Entfernen von Patches aus der Sequenz dazu führen kann, dass Patches als veraltet markiert oder ersetzt werden.

Alle Patches, die zum Entfernen ausgewählt wurden, werden in der [**msipatchremovallist**](msipatchremovallist.md) -Eigenschaft aufgeführt. Diese Eigenschaft ist eine private Eigenschaft, die vom Installationsprogramm festgelegt und in bedingten Ausdrücken verwendet oder durch [benutzerdefinierte Aktionen](custom-actions.md)abgefragt werden kann. Die-Eigenschaft enthält die Liste der Patch-Code-GUIDs von Patches, die entfernt werden sollen. Eine benutzerdefinierte Aktion kann ermitteln, ob der Installationsstatus des Patches angewendet, veraltet oder ersetzt wird, indem die [**msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa) -Eigenschaft oder die [**patchproperty**](patch-patchproperty.md) -Eigenschaft des [Patch-Objekts](patch-object.md)aufgerufen wird.

Nachdem ein Patch entfernt wurde, ist der Status der Anwendung identisch mit dem Zeitpunkt, an dem der Patch nie installiert wurde. Wenn möglich, schränkt der Installer den Prozess auf die Teilmenge der Features ein, die von dem zu entfernenden Patch betroffen sind. Das Installationsprogramm legt die Eigenschaft [**neu installieren**](reinstall.md) automatisch auf die Liste der betroffenen Features fest. Dateien, die vom Patch hinzugefügt wurden, werden entfernt, und Dateien, die vom Patch geändert wurden, werden überschrieben. Dateien und Registrierungseinträge werden in der Version wieder hergestellt, die vom Produkt abzüglich des Patches erwartet wird. Die Registrierung von Features und Komponenten, die vom Patch hinzugefügt wurden, wird in der Anwendung aufgehoben. Beachten Sie, dass zusätzliche Inhalte, die vom Patch hinzugefügt werden, auf dem Computer des Benutzers verbleiben können, wenn der Inhalt von einem anderen Patch verwendet wird, der weiterhin anwendbar ist.

Wenn eine Datei einer freigegebenen Komponente durch einen Patch aktualisiert wird, wirkt sich diese Änderung auf alle Anwendungen aus, die die Komponente gemeinsam verwenden. Wenn der Patch entfernt wird, wirkt sich die Änderung erneut auf alle Anwendungen aus, die die Komponente gemeinsam verwenden. Dies bedeutet, dass durch das Entfernen eines Patches durch eine Anwendung die Datei der freigegebenen Komponente in einer niedrigeren Version wieder hergestellt werden kann, als von einer anderen Anwendung benötigt wird. Dadurch kann die erste Anwendung behoben werden, aber die zweite Anwendung funktioniert nicht mehr. In diesem Fall kann die zweite Anwendung repariert werden, indem Sie die zweite Anwendung mithilfe der Methoden, die in [Neuinstallation eines Features oder einer Anwendung](reinstalling-a-feature-or-application.md)beschrieben werden, neu installieren. Dadurch wird die gepatchte Version der Datei wieder hergestellt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Msienumapplicationsex**](/windows/desktop/api/Msi/nf-msi-msienumproductsexa)
</dt> <dt>

[**Msigetpatchinfoex**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[**Msipatchremove**](msipatchremove.md)
</dt> <dt>

[**Msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[Patchsequenzierung](sequencing-patches.md)
</dt> <dt>

[Patch zum Deinstallieren benutzerdefinierter Aktionen](patch-uninstall-custom-actions.md)
</dt> <dt>

[Nicht installierbare Patches](uninstallable-patches.md)
</dt> <dt>

[Patches werden deinstalliert.](uninstalling-patches.md)
</dt> </dl>

 

 



