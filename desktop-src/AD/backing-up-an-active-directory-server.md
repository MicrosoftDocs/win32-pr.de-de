---
title: Sichern eines Active Directory Servers
description: Eine Active Directory Server-Sicherung erfordert, dass Sie die Datenbank und die Transaktionsprotokolle sichern. Dieses Thema enthält eine exemplarische Vorgehensweise, wie eine Sicherungs Anwendung den Active Directory Directory-Dienst sichert.
ms.assetid: 250b2f40-6d43-4aa5-a588-b0cd4839828d
ms.tgt_platform: multiple
keywords:
- Sichern Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5affde952ee543afe1bb9b794cce074a74382aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036263"
---
# <a name="backing-up-an-active-directory-server"></a>Sichern eines Active Directory Servers

Eine Active Directory Server-Sicherung erfordert, dass Sie die Datenbank und die Transaktionsprotokolle sichern. Dieses Thema enthält eine exemplarische Vorgehensweise, wie eine Sicherungs Anwendung den Active Directory Directory-Dienst sichert.

Der Aufrufer dieser Sicherungsfunktionen muss über die Berechtigung " **SE \_ Backup \_ Name** " verfügen. Sie können die [**dssetauthidentity**](dssetauthidentity.md) -Funktion verwenden, um den Sicherheitskontext festzulegen, unter dem die Funktionen zum Sichern und Wiederherstellen von Verzeichnissen aufgerufen werden.

**Führen Sie die folgenden Schritte aus, um einen Active Directory Server zu sichern:**

1.  Ruft die [**dsisntdsonline**](dsisntdsonline.md) -Funktion auf, um zu bestimmen, ob Active Directory Domain Services ausgeführt werden.
2.  Wenn Active Directory Domain Services ausgeführt werden, wird die [**dsbackupprepare**](dsbackupprepare.md) -Funktion aufgerufen, um ein Sicherungs Kontext Handle zu initialisieren. Wenn Active Directory Domain Services nicht ausgeführt werden, kann es nicht gesichert werden, und die Sicherungs Anwendung muss den Sicherungs Vorgang nicht ausführen.
3.  Aufrufen der [**dsbackupgetdatabasenames**](dsbackupgetdatabasenames.md) -Funktion, um eine Liste der zu sichernden Dateien abzurufen. Um den von dieser Funktion zurückgegebenen Arbeitsspeicher freizugeben, nennen Sie die Funktion [**dsbackupfree**](dsbackupfree.md) .
4.  Rufen Sie für jeden Namen in der zurückgegebenen Liste der Dateien die [**dsbackupopenfile**](dsbackupopenfile.md) -Funktion auf, gefolgt von wiederholten Aufrufen der [**dsbackupread**](dsbackupread.md) -Funktion, bis die gesamte Datei gelesen wurde. Wenn Sie mit dem Lesen der Datei fertig sind, müssen Sie die Funktion [**dsbackupclose**](dsbackupclose.md) zum Schließen der Datei abrufen.
5.  Nachdem alle Datenbankdateien gesichert wurden, können Sie die Funktion [**dsbackupgetbackuplogs**](dsbackupgetbackuplogs.md) aufrufen, um eine Liste der Transaktionsprotokolle abzurufen. Diese Liste wird genau wie die Liste der Datenbankdateien behandelt.
6.  Wenn Sie die Sicherung des Transaktions Protokolls abgeschlossen haben, können Sie die [**dsbackuptruneurelogs**](dsbackuptruncatelogs.md) -Funktion zum Löschen sämtlicher zugesicherter Transaktionsprotokolle, die gesichert wurden, löschen.
7.  Speichern Sie den Inhalt des Ablauf Tokens, das von der [**dsbackupprepare**](dsbackupprepare.md) -Funktion bereitgestellt wird. Dies kann in einer Datei oder einem anderen persistenten Speicher gespeichert werden. Dieses Token muss an die [**dsrestoreprepare**](dsrestoreprepare.md) -Funktion übergeben werden, um einen Wiederherstellungs Vorgang zu initiieren.
8.  Gibt den Arbeitsspeicher für das Ablauf Token frei, indem der tokenzeiger an die [**dsbackupfree**](dsbackupfree.md) -Funktion übergeben wird.
9.  Zum Schluss wird die [**dsbackupend**](dsbackupend.md) -Funktion aufgerufen, um alle dem Sicherungs Kontext Handle zugeordneten Ressourcen freizugeben.

 

 




