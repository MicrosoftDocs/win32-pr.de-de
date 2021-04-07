---
title: Überlegungen zur Active Directory Domain Services Sicherung
description: Verzeichnisdienst Daten können repliziert werden. Vor der Wiederherstellung muss ein Wiederherstellungs Plan erstellt werden.
ms.assetid: b03215db-1b8d-45b0-85e8-c325b225c6eb
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory, Wiederherstellungs Planung
- Active Directory Domain Services Active Directory, Sicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52bf284804ba5a8882ecee6f6e03ae95249e5435
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038792"
---
# <a name="considerations-for-active-directory-domain-services-backup"></a>Überlegungen zur Active Directory Domain Services Sicherung

Verzeichnisdienst Daten können repliziert werden. Vor der Wiederherstellung muss ein Wiederherstellungs Plan erstellt werden. Eine Möglichkeit besteht darin, ein Replikat eines Verzeichnisses wiederherzustellen und dann Änderungen, die seit der Sicherung aufgetreten sind, von anderen Replikaten in der Domäne weiterzugeben.

In einigen Fällen möchten Sie möglicherweise, dass das wiederhergestellte Replikat Vorrang vor den anderen Replikaten in der Domäne hat. Wenn ein Objekt z. b. versehentlich gelöscht und der Löschvorgang auf allen Domänen Controllern repliziert wird, können Sie das Objekt wiederherstellen, indem Sie ein Replikat aus einer Sicherung wiederherstellen, die vor dem Löschen des Objekts erstellt wurde. Anschließend verwenden Sie das Hilfsprogramm Ntdsutil, um das wiederhergestellte Objekt als autoritativ wieder hergestellt zu markieren. Das wiederhergestellte Objekt wird dann auf die anderen DCS repliziert, und das wiederhergestellte Replikat empfängt die Updates für alle anderen Objekte, die seit dem Zeitpunkt der Sicherungs Erstellung aufgetreten sind. Das Endergebnis für alle Replikate ist das gleiche wie vor der Wiederherstellung, mit der Ausnahme, dass das autoritativ wiederhergestellte Objekt nicht mehr gelöscht wird.

Alle während der Sicherung auftretenden Änderungen werden in einem temporären Protokoll gespeichert und am Ende des Sicherungs Satzes hinzugefügt, wenn die Sicherung abgeschlossen ist.

Jeder Wiederherstellungs Plan sollte sicherstellen, dass das Alter der Sicherung die Active Directory Tombstone-Lebensdauer nicht überschreitet. Weitere Informationen zur Tombstone-Lebensdauer finden Sie im TechNet-Thema- [Einführung in die Verwaltung von Active Directory Sicherung und Wiederherstellung](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc816677(v=ws.10)). Die Wiederherstellung einer Sicherung, die älter als die Tombstone-Lebensdauer ist, kann dazu führen, dass der wiederhergestellte Domänen Controller Objekte enthält, die nicht auf anderen DCS repliziert Dies tritt auf, wenn ein Objekt gelöscht wird, nachdem die Sicherung erstellt wurde, und die Wiederherstellung erfolgt, nachdem der Tombstone-Wert für das gelöschte Objekt dauerhaft entfernt wurde. Der wiederhergestellte Domänen Controller verfügt über das Objekt, so wie es vor dem Löschvorgang vorhanden war, und die anderen DCS hätten keinen Datensatz, dass das Objekt jemals vorhanden war. In diesem Fall muss ein Administrator jedes nicht replizierte Objekt auf dem wiederhergestellten Domänen Controller manuell löschen.

Inkrementelle Sicherungen von Active Directory Domain Services werden nicht unterstützt. vollständige Sicherungen sind erforderlich.

 

 