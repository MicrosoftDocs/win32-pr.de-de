---
description: 'Weitere Informationen: Programmier Überlegungen für das Schreiben von Ressourcen-Managern'
ms.assetid: 7f1e61e8-15e1-4a25-b864-eeadcac61108
title: Überlegungen zur Programmierung beim Schreiben von Ressourcen-Managern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bae64ead32c747a0e8499dcdc8821d36f01f06e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349466"
---
# <a name="programming-considerations-for-writing-resource-managers"></a>Überlegungen zur Programmierung beim Schreiben von Ressourcen-Managern

Wenn Sie die Kerneltransaktions-Manager-API verwenden, um Ihren Anwendungen Transaktionsunterstützung hinzuzufügen, sollten Sie Folgendes beachten:

-   Wenn Sie Ihren eigenen Ressourcen-Manager schreiben, sollten Sie über gute Kenntnisse der Verfahren und Protokolle der Transaktions Verwaltung verfügen.
-   Wenn Sie Ressourcen-Manager nicht ordnungsgemäß schreiben, können Sie Ihre eigenen Daten mit nicht ordnungsgemäß behandelten Wiederherstellungs Vorgängen beschädigen. Sie können auch das Ende des Transaktions Protokolls anheften und das Dateisystem mit Transaktions Protokollen auffüllen.
-   Wenn die Richtlinie für die Protokoll Größe nicht festgelegt ist, um zu verhindern, dass die Größe des Protokolls zunimmt, werden Transaktionen vom Ressourcen-Manager nicht angehalten. Ihr Ressourcen-Manager muss das System nicht mehr aktualisieren, sodass die Dateisystemressourcen nicht überschritten werden.
-   Ressourcen-Manager sollten Zugriffs Steuerungs Listen (Access Control Lists, ACLs) verwenden, um den Zugriff auf die Protokolldateien zu steuern. Andernfalls können Denial-of-Service-Angriffe durchführt werden.
-   Alle Ressourcen-Manager oder Transaktions Teilnehmer, die Daten zwischenspeichern, müssen sich für Benachrichtigungen vor der Vorbereitung anmelden. Wenn eine Benachrichtigung vor der Vorbereitung empfangen wird, müssen Sie alle Ihre Daten leeren, damit sich alle Downstream-Ressourcen-Manager vor der Vorbereitungsphase eintragen können. Alle weiteren Aufgaben in dieser Transaktion dürfen nicht zwischengespeichert werden.
-   Schließt ein Eintragung-Handle nicht, solange die Transaktion noch aktiv ist. Dies bewirkt, dass für die Transaktion ein Rollback ausgeführt wird.

 

 



