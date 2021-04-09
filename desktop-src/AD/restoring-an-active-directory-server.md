---
title: Wiederherstellen eines Active Directory Servers
description: Active Directory Server müssen offline wieder hergestellt werden.
ms.assetid: 91fbbdc1-0e84-4b89-8a38-4c8d0268992b
ms.tgt_platform: multiple
keywords:
- Active Directory wird wieder hergestellt Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 273d02fd50d6b3bd68a055a6a783566e4ebddcf7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103858121"
---
# <a name="restoring-an-active-directory-server"></a>Wiederherstellen eines Active Directory Servers

Active Directory Server müssen offline wieder hergestellt werden. Das System muss im Verzeichnisdienst-Wiederherstellungs Modus neu gestartet werden. In diesem Modus wird das Betriebssystem ohne Active Directory Domain Services ausgeführt, und alle Benutzer Validierung erfolgt über den Sicherheits Konten-Manager (Security Accounts Manager, Sam) in der Registrierung. Verwenden Sie zum Wiederherstellen Active Directory Domain Services die Anmelde Informationen eines lokalen Administrators auf dem wiederhergestellten Domänen Controller.

Der Aufrufer der Wiederherstellungs Funktionen muss über die Berechtigung " **SE \_ Restore \_ Name** Access" verfügen. Verwenden Sie die [**dssetauthidentity**](dssetauthidentity.md) -Funktion, um den Sicherheitskontext festzulegen, unter dem die Verzeichnis Sicherungs-und Wiederherstellungs Funktionen aufgerufen werden.

Beachten Sie, dass Sie bei der Wiederherstellung Active Directory Domain Services auch die anderen Systemstatus Komponenten wiederherstellen müssen.

**Wiederherstellung Active Directory Domain Services**

1.  Ruft die [**dsisntdsonline**](dsisntdsonline.md) -Funktion auf, um zu bestimmen, ob Active Directory Domain Services ausgeführt werden.
2.  Wenn Active Directory Domain Services nicht ausgeführt werden, wird die [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion aufgerufen, um den Wiederherstellungs Vorgang zu initialisieren und ein Sicherungs Kontext Handle abzurufen. Wenn Active Directory Domain Services ausgeführt wird, kann es nicht wieder hergestellt werden, und die Wiederherstellungs Anwendung muss den Wiederherstellungs Vorgang fehlschlagen. Die **dsrestoreprepare** -Funktion erfordert, dass das ablauftoken während des Sicherungs Vorgangs von der [**dsbackupprepare**](dsbackupprepare.md) -Funktion abgerufen wird.
3.  Aufrufen der [**dsrestoregetdatabaselocations**](dsrestoregetdatabaselocations.md) -Funktion zum Bestimmen der Verzeichnisse, in denen die Dateien wieder hergestellt werden sollen. Wenn diese Funktion fehlschlägt, stellen Sie die Daten im ursprünglichen Sicherungs Quellverzeichnis wieder her. Das ist das Verzeichnis, aus dem die Daten gesichert wurden.
4.  Wenden Sie die [**dsrestoreregiester**](dsrestoreregister.md) -Funktion an, um den Active Directory Server für den Wiederherstellungs Vorgang vorzubereiten und die Wiederherstellungs Verzeichnisse zu sperren.
5.  Verwenden Sie Win32-Standardfunktionen, um die Dateien wiederherzustellen. Löschen Sie zuerst alle Dateien im Zielverzeichnis. Kopieren Sie dann die Sicherungsdateien in das Zielverzeichnis.
6.  Wenden Sie die [**dsrestoreregistercomplete**](dsrestoreregistercomplete.md) -Funktion an, um anzugeben, dass die Wiederherstellung abgeschlossen wurde.
7.  Ruft die [**dsrestoreend**](dsrestoreend.md) -Funktion auf, um alle dem Kontext zugeordneten Ressourcen freizugeben.

Nach einer Wiederherstellung im Verzeichnisdienst-Wiederherstellungs Modus sollte der Domänen Controller im normalen Modus neu gestartet werden. Wenn der Verzeichnisdienst gestartet wird, führt der Domänen Controller die normale Konsistenzprüfung durch, und das wiederhergestellte Verzeichnis wird dann online geschaltet.

Beachten Sie, dass das Wiederherstellen eines Active Directory Servers immer ein zweiteilige Vorgang ist. Stellen Sie zunächst die Datenbank zu einem Zeitpunkt wieder her, zu dem die Sicherung erstellt wurde. Zweitens: Replizieren Sie das Verzeichnis, in dem die neu wiederhergestellten DSA-Updates nach der Sicherung von anderen DSAs in der Domäne und in der Unternehmens Gesamtstruktur repliziert werden.

Ein Computer unter Windows 2000 oder Windows Server 2003, der ein Replikat des Verzeichnis Dienstanbieter enthält, ist ein Domänen Controller.

Die [**dsrestoreregisterfunktion**](dsrestoreregister.md) fügt Daten zur Registrierung hinzu, die den Registrierungsvorgang für die Wiederherstellung überstehen müssen, damit die Wiederherstellung ordnungsgemäß funktioniert. Um sicherzustellen, dass diese Registrierungsdaten beibehalten werden, stellen Sie Active Directory Domain Services mit den **DSRestore \*** -Funktionen wieder her, bevor Sie den Computer neu starten, nachdem die [**RegReplaceKey**](/windows/desktop/api/winreg/nf-winreg-regreplacekeya) -Funktion aufgerufen wurde. Dieser Prozess funktioniert, weil **RegReplaceKey** die Registrierungs Struktur nicht tatsächlich ersetzt, bis der Computer neu gestartet wird, und die von der **dsrestoreregisterfunktion** hinzugefügten Registrierungsdaten werden beim Wiederherstellungs Vorgang einer Registrierung ausdrücklich ausgeschlossen.

 

 