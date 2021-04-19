---
description: Die Sicherungs-und Wiederherstellungs Funktionen des Certadm.dll können nicht zum Sichern der privaten Schlüssel der Zertifikat Dienste verwendet werden.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Sichern und Wiederherstellen des privaten Schlüssels für Zertifikat Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 891794f36e87b2aa4b6a5d5c8dde55304da20601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356792"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Sichern und Wiederherstellen des privaten Schlüssels für Zertifikat Dienste

Die Sicherungs-und Wiederherstellungs Funktionen des Certadm.dll können nicht zum Sichern der [*privaten Schlüssel*](../secgloss/p-gly.md)der Zertifikat Dienste verwendet werden. Private Schlüssel können nicht von diesen Funktionen gesichert werden, da diese Funktionen zum Sichern und Wiederherstellen der Zertifikat Dienst Datenbank (und zugehöriger Dateien) vorgesehen sind, und diese Datenbank enthält keine privaten Schlüssel (selbst für selbst ausgestellte Zertifikate).

Verwenden Sie das MMC-Snap-in "Zertifizierungsstelle" oder den Befehl "Certutil" (with-Backup oder-backupkey), um einen privaten Schlüssel für die Zertifikat Dienste zu sichern. Beim Sichern des privaten Schlüssels mit dem MMC-Snap-in "Zertifizierungsstelle" oder "Certutil" wird der private Schlüssel in die PKCS \# 12-Datei geschrieben. Obwohl diese PKCS \# 12-Datei Kenn Wort geschützt ist, sollte Sie als äußerst sensibel eingestuft werden und muss sicher gespeichert werden. das Kennwort für die PKCS \# 12-Datei sollte auch vor nicht autorisierten Personen geschützt werden.

Auf ähnliche Weise können private Schlüssel nicht durch die Sicherungs-und Wiederherstellungs Funktionen der Zertifikat Dienste wieder hergestellt werden. Ein Sicherungs Schlüssel für Zertifikat Dienste, der in einer PKCS \# 12-Datei enthalten ist, kann mit dem MMC-Snap-in "Zertifizierungsstelle" oder mit dem Befehl "Certutil" (Angabe von "-Restore" oder "-restorekey") wieder hergestellt werden. Beachten Sie, dass die Person, die den Wiederherstellungs Vorgang ausführt, das Kennwort für die \# Datei

Es gibt nur zwei Fälle, in denen der private Schlüssel der Zertifikat Dienste gesichert werden muss. Der erste Fall ist die Installation von Zertifikat Diensten. Der zweite Fall ist nach jedem Erneuerungs Vorgang des Zertifikat Dienst Zertifikats.

 

 
