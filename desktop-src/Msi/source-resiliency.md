---
description: Anwendungen, die sich auf die Netzwerkressourcen für die Bedarfs gesteuerte Installation stützen, sind anfällig für Quell Fehler, wenn sich der Quell Speicherort aus irgendeinem Grund ändern oder beschädigt werden soll.
ms.assetid: 3d6a0524-d5df-4d4c-b861-d4a7da95ce40
title: Quellen Resilienz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46944804db1c4b91c6c6757303fd2af90638b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958736"
---
# <a name="source-resiliency"></a>Quellen Resilienz

Anwendungen, die sich auf die Netzwerkressourcen für die [Bedarfs gesteuerte Installation](installation-on-demand.md) stützen, sind anfällig für Quell Fehler, wenn sich der Quell Speicherort aus irgendeinem Grund ändern oder beschädigt werden soll. Der Windows Installer bietet die Quellen Resilienz für Features, die bei Bedarf mithilfe einer Quell Liste installiert werden. Die Quell Liste enthält die Speicherorte, die vom Installationsprogramm nach Installationspaketen durchsucht werden. Die Einträge in dieser Liste können Netzwerkspeicher Orte, URLs (Uniform Resource Locators) oder Compact Disks sein. Wenn eine dieser Quellen fehlschlägt, kann das Installationsprogramm schnell und nahtlos den nächsten Versuch durchführen.

Der Anwendungsentwickler muss keine besonderen Informationen in das Installer-Paket integrieren, um die Resilienz der Quelle sicherzustellen. Nachdem die Anwendung installiert wurde, hat das Installationsprogramm das Verhalten, die zuletzt erfolgreich verwendete Quelle als Eintrag in der Quell Liste hinzuzufügen. Standardmäßig ist diese Quelle der Speicherort, von dem aus das Installer-Paket erstmalig installiert wird, und entspricht der [**SourceDir**](sourcedir.md) -Eigenschaft.

Ein Systemadministrator kann die Quell Liste durch Anwenden einer [Transformation](merges-and-transforms.md) oder durch Ändern der [**SourceList**](sourcelist.md) -Eigenschaft von der Befehlszeile oder in der [Eigenschaften Tabelle](property-table.md)ändern.

Das Installationsprogramm beginnt mit der Suche nach einer Quelle, indem der zuletzt verwendete Quell Speicherort in der Quell Liste überprüft wird. Wenn bei dieser Suche ein Fehler auftritt, durchsucht das Installationsprogramm die Liste der Netzwerk Quellen, anschließend die Medienquellen und schließlich URL-Quellen. Systemadministratoren können diese Such Reihenfolge mithilfe der [SearchOrder](searchorder.md) -System Richtlinie ändern. Wenn diese Suchvorgänge fehlschlagen, stellt das Installationsprogramm möglicherweise ein Dialog Feld zum [Durchsuchen](browse-dialog.md) dar, sodass der Benutzer manuell nach der Quelle suchen kann. Das Dialogfeld durchsuchen kann nicht angezeigt werden, wenn die Benutzeroberflächen Ebene auf keine festgelegt ist. Weitere Informationen finden Sie unter [Benutzeroberflächen Ebenen](user-interface-levels.md).

Häufig sollte das Installationsprogramm nur ein Dialogfeld zum Durchsuchen anzeigen, wenn der aktuelle Benutzer ein Administrator ist, oder wenn die Installation keine erhöhten Rechte erfordert. Ein Administrator kann die Anzeige des Dialog Felds durchsuchen für Benutzer mit den Richtlinien [disablebrowse](disablebrowse.md) und [AllowLockdownBrowse](allowlockdownbrowse.md) steuern. Ein Administrator steuert auch, ob Benutzer Anwendungen mithilfe der Richtlinien [disablemedia](disablemedia.md) und [AllowLockdownMedia](allowlockdownmedia.md) aus Quellen, die sich auf den Medien befinden, installieren können. Die Verwendung dieser Richtlinien hängt von der Windows Installer Version ab. Weitere Informationen finden Sie in den folgenden Bereichen:

-   [Resilienzrichtlinie für Quelle](source-resiliency-policy-windows-installer-version-2-0.md)

 

 



