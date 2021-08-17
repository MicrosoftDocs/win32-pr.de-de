---
description: Der Active Directory Writer erfordert während Sicherungsvorgängen keine besonderen Aktionen.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: VSS-Sicherung und -Wiederherstellung von Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e8312e974d705cd193eaaecdaa163a2d408836aedfb14c21ff97f72486efbf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117751483"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>VSS-Sicherung und -Wiederherstellung von Active Directory

Der Active Directory Writer erfordert während Sicherungsvorgängen keine besonderen Aktionen. Der Writer stellt dem Anfordernden Komponenten- und Dateisatzinformationen zur Verfügung, und der Anfordernde verwendet diese Informationen, um zu entscheiden, welche Dateien auf Sicherungsmedien kopiert werden sollen. Es ist nicht notwendig, spezielle APIs zum Sichern von Active Directory zu verwenden.

Wie eine Wiederherstellung durchgeführt wird, hängt davon ab, ob Active Directory im Rahmen eines Notfallwiederherstellungsvorgang wiederhergestellt wird oder ob die Wiederherstellung auf einem System erfolgt, auf dem Active Directory ausgeführt wird. Darüber hinaus kann das Alter der Sicherungskopie des Active Directory-Zustands aufgrund von Active Directory-Tombstones ein Problem sein.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory-Wiederherstellung nach der Notfallwiederherstellung

Nach einem Absturz, der eine Notfallwiederherstellung erfordert, kann Active Directory im Rahmen der Wiederherstellung des Betriebssystemstatus wiederhergestellt werden.

Dieser Wiederherstellungsvorgang ist im Wesentlichen eine schreiblose Wiederherstellung.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory-Wiederherstellung auf dem System, auf dem es ausgeführt wird

Das System muss im Verzeichnisdienst-Wiederherstellungsmodus neu gestartet werden, wenn das Active Directory derzeit auf dem Server ausgeführt wird.

Das Betriebssystem wird dann ohne Active Directory ausgeführt, und alle Benutzerüberprüfungen erfolgen über den Sicherheitskonten-Manager (SAM) in der Registrierung. Nur der Administrator verfügt über die Berechtigung zum Wiederherstellen von Active Directory.

Im Wiederherstellungsmodus des Verzeichnisdiensts kann eine VSS-Wiederherstellung normal fortgesetzt werden. Es gibt keinen Grund, Nicht-VSS-Win32-Active Directory-APIs zum Wiederherstellen des Active Directory-Zustands zu verwenden.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory-Wiederherstellungen und Active Directory-Tombstones

Bei jedem Wiederherstellungsplan sollte sichergestellt werden, dass das Alter der Sicherung die Active Directory-Tombstonelebensdauer nicht überschreitet (Der Standardwert ist 60 Tage).

Die Wiederherstellung einer Sicherung, die älter als der Tombstone ist, verursacht, dass ein Domänencontroller Objekte enthält, die nicht auf die anderen Server repliziert werden.

Objekte, die nicht repliziert werden, werden auf diesem (wiederhergestellten) Domänencontroller nicht automatisch gelöscht, da die Tombstones dieser Objekte auf den anderen Replikaten bereits gelöscht wurden.

Ein Administrator muss jedes nicht replizierte Objekt auf dem wiederhergestellten Domänencontroller manuell löschen. Inkrementelle Sicherungen von Active Directory werden nicht unterstützt. Eine vollständige Sicherung ist erforderlich.

 

 



