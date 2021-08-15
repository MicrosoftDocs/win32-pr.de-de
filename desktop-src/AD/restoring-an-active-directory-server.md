---
title: Wiederherstellen eines Active Directory-Servers
description: Active Directory-Server müssen offline wiederhergestellt werden.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Wiederherstellen von Active Directory Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 865389b4ad80ad8c3009a86a881ff4cf291a4fc1b4606e78e8ecd01ceef7c893
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184293"
---
# <a name="restoring-an-active-directory-server"></a>Wiederherstellen eines Active Directory-Servers

Active Directory-Server müssen offline wiederhergestellt werden. Das System muss im Verzeichnisdienstwiederherstellungsmodus neu gestartet werden. In diesem Modus wird das Betriebssystem ohne Active Directory Domain Services ausgeführt, und die gesamte Benutzerüberprüfung erfolgt über den Sicherheitskonten-Manager (SAM) in der Registrierung. Verwenden Sie zum Wiederherstellen Active Directory Domain Services die Anmeldeinformationen eines lokalen Administrators auf dem wiederhergestellten Domänencontroller.

Der Aufrufer der Wiederherstellungsfunktionen muss über die **zugriffsberechtigung SE \_ RESTORE \_ NAME** verfügen. Verwenden Sie die [**DsSetAuthIdentity-Funktion,**](dssetauthidentity.md) um den Sicherheitskontext festzulegen, unter dem die Verzeichnissicherungs- und Wiederherstellungsfunktionen aufgerufen werden.

Beachten Sie, dass Sie beim Wiederherstellen Active Directory Domain Services auch die anderen Systemstatuskomponenten wiederherstellen müssen.

**So stellen Sie Active Directory Domain Services**

1.  Rufen Sie die [**DsIsNTDSOnline-Funktion**](dsisntdsonline.md) auf, um zu bestimmen, ob Active Directory Domain Services ausgeführt werden.
2.  Wenn Active Directory Domain Services nicht ausgeführt werden, wird die [**DsRestorePrepare-Funktion**](dsrestoreprepare.md) aufgerufen, um den Wiederherstellungsvorgang zu initialisieren und ein Sicherungskontexthandle abzurufen. Wenn Active Directory Domain Services ausgeführt werden, kann sie nicht wiederhergestellt werden, und die Wiederherstellungsanwendung muss den Wiederherstellungsvorgang fehlschlagen. Die **DsRestorePrepare-Funktion** erfordert, dass das Ablauftoken während des Sicherungsvorgangs von der [**DsBackupPrepare-Funktion**](dsbackupprepare.md) abgerufen wird.
3.  Rufen Sie die [**DsRestoreGetDatabaseLocations-Funktion**](dsrestoregetdatabaselocations.md) auf, um die Verzeichnisse zu bestimmen, in denen die Dateien wiederhergestellt werden sollen. Wenn diese Funktion fehlschlägt, stellen Sie die Daten wieder im ursprünglichen Sicherungsquellverzeichnis wieder her. Dies ist das Verzeichnis, aus dem die Daten gesichert wurden.
4.  Rufen Sie die [**DsRestoreRegister-Funktion**](dsrestoreregister.md) auf, um den Active Directory-Server für den Wiederherstellungsvorgang vorzubereiten und die Wiederherstellungsverzeichnisse zu sperren.
5.  Verwenden Sie Win32-Standardfunktionen, um die Dateien wiederherzustellen. Löschen Sie zunächst alle Dateien im Zielverzeichnis. Kopieren Sie dann die Sicherungsdateien in das Zielverzeichnis.
6.  Rufen Sie die [**DsRestoreRegisterComplete-Funktion**](dsrestoreregistercomplete.md) auf, um anzugeben, dass die Wiederherstellung abgeschlossen wurde.
7.  Rufen Sie die [**DsRestoreEnd-Funktion**](dsrestoreend.md) auf, um alle Ressourcen freizugeben, die dem Kontext zugeordnet sind.

Nach einer Wiederherstellung im Verzeichnisdienst-Wiederherstellungsmodus sollte der Domänencontroller im normalen Modus neu gestartet werden. Wenn der Verzeichnisdienst gestartet wird, führt der Domänencontroller die normale Konsistenzprüfung durch, und das wiederhergestellte Verzeichnis ist dann online.

Beachten Sie, dass die Wiederherstellung eines Active Directory-Servers immer ein zweiteiligen Vorgang ist. Stellen Sie zunächst die Datenbank auf einen Zeitpunkt wieder her, zu dem die Sicherung erstellt wurde. Zweitens replizieren Sie das Verzeichnis, in dem das neu wiederhergestellte DSA Updates nach der Sicherung von anderen DSAs in der Domäne und der Unternehmensgestruktur repliziert.

Ein Computer, der auf Windows 2000 oder Windows Server 2003 ausgeführt wird und ein Replikat des Verzeichnisdiensts enthält, ist ein Domänencontroller.

Die [**DsRestoreRegister-Funktion**](dsrestoreregister.md) fügt der Registrierung Daten hinzu, die den Registrierungswiederherstellungsprozess überstehen müssen, damit die Wiederherstellung ordnungsgemäß funktioniert. Um sicherzustellen, dass diese Registrierungsdaten beibehalten werden, stellen Sie Active Directory Domain Services mit den Funktionen **DsRestore \** _ wieder her, bevor Sie den Computer neu starten, nachdem die [*_RegReplaceKey-Funktion* *](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) aufgerufen wurde. Dieser Prozess funktioniert, da **RegReplaceKey** die Registrierungsstruktur erst ersetzt, wenn der Computer neu gestartet wird und die von der **DsRestoreRegister-Funktion hinzugefügten** Registrierungsdaten während eines Registrierungswiederherstellungsvorgangs explizit von der Ersetzung ausgeschlossen werden.

 

 