---
description: Für den Active Directory Writer sind bei Sicherungs Vorgängen keine besonderen Aktionen erforderlich.
ms.assetid: 66efd5e5-e6c9-4179-b119-1b5b977b0f9f
title: VSS-Sicherung und-Wiederherstellung des Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d4441a05e06e67c23467887857a0f7bbcde73f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526291"
---
# <a name="vss-backup-and-restore-of-the-active-directory"></a>VSS-Sicherung und-Wiederherstellung des Active Directory

Für den Active Directory Writer sind bei Sicherungs Vorgängen keine besonderen Aktionen erforderlich. Der Writer stellt dem Anforderer Informationen zu Komponenten-und Datei Satz Informationen zur Verfügung, und der Anforderer verwendet diese Informationen, um zu entscheiden, welche Dateien auf die Sicherungsmedien kopiert werden sollen. Zum Sichern des Active Directory müssen keine speziellen APIs verwendet werden.

Die Art und Weise, wie eine Wiederherstellung ausgeführt wird, hängt davon ab, ob die Active Directory im Rahmen eines Notfall Wiederherstellungs Vorgangs wieder hergestellt wird oder ob die Wiederherstellung auf einem System ausgeführt wird, auf dem die Active Directory ausgeführt wird. Außerdem kann das Alter der Sicherungskopie des Active Directory Zustands aufgrund Active Directory Tombstones ein Problem sein.

## <a name="active-directory-restoration-following-disaster-recovery"></a>Active Directory Wiederherstellung nach der Notfall Wiederherstellung

Nach einem Absturz, der eine Notfall Wiederherstellung erfordert, kann der Active Directory im Rahmen der Wiederherstellung des Betriebssystem Status wieder hergestellt werden.

Dieser Wiederherstellungs Vorgang ist im Wesentlichen eine Schreib lose Wiederherstellung.

## <a name="active-directory-restoration-on-the-system-where-it-is-running"></a>Active Directory Wiederherstellung auf dem System, auf dem es ausgeführt wird

Das System muss im Modus für die Verzeichnisdienst Wiederherstellung neu gestartet werden, wenn die Active Directory derzeit auf dem Server ausgeführt wird.

Das Betriebssystem wird dann ohne den Active Directory ausgeführt, und alle Benutzer Validierung erfolgt über den Security Accounts Manager (Sam) in der Registrierung. Nur der Administrator verfügt über die Berechtigung zum Wiederherstellen des Active Directory.

Im Verzeichnisdienst-Wiederherstellungs Modus kann eine VSS-Wiederherstellung normal fortgesetzt werden. Es gibt keinen Grund, nicht-VSS-Win32-Active Directory-APIs zu verwenden, um den Active Directory-Zustand wiederherzustellen.

## <a name="active-directory-restores-and-active-directory-tombstones"></a>Active Directory Wiederherstellungen und Active Directory Tombstones

Jeder Wiederherstellungs Plan sollte sicherstellen, dass das Alter der Sicherung die Active Directory Tombstone-Lebensdauer (Standardwert 60 Tage) nicht überschreitet.

Durch die Wiederherstellung einer Sicherung, die älter als der Tombstone ist, werden von einem Domänen Controller Objekte verwendet, die nicht auf den anderen Servern repliziert werden.

Diese Objekte, die nicht repliziert werden, werden auf dem (wiederhergestellten) Domänen Controller nicht automatisch gelöscht, da die Tombstones dieser Objekte auf den anderen Replikaten bereits gelöscht wurden.

Ein Administrator muss alle Objekte auf dem wiederhergestellten Domänen Controller, die nicht repliziert werden, manuell löschen. Inkrementelle Sicherungen der Active Directory werden nicht unterstützt. eine vollständige Sicherung ist erforderlich.

 

 



