---
description: Sie können die Sicherungs- und Wiederherstellungsfunktionen der Certadm.dll nicht verwenden, um die privaten Schlüssel der Zertifikatdienste zu sichern.
ms.assetid: 27ee8caa-8f5e-46dc-b55d-afde5471507e
title: Sichern und Wiederherstellen des privaten Schlüssels der Zertifikatdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a65b8c25e627e516d92b8dc8219db9c7933bd8d9902b1f75bea204d723edd61f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879780"
---
# <a name="backing-up-and-restoring-the-certificate-services-private-key"></a>Sichern und Wiederherstellen des privaten Schlüssels der Zertifikatdienste

Sie können die Sicherungs- und Wiederherstellungsfunktionen der Certadm.dll nicht verwenden, um die [*privaten Schlüssel*](../secgloss/p-gly.md)der Zertifikatdienste zu sichern. Private Schlüssel können nicht durch diese Funktionen gesichert werden, da diese Funktionen zum Sichern und Wiederherstellen der Zertifikatdienstdatenbank (und zugehöriger Dateien) vorgesehen sind und diese Datenbank keine privaten Schlüssel enthält (auch nicht für selbst ausgestellte Zertifikate).

Verwenden Sie zum Sichern eines privaten Zertifikatdienstschlüssels das MMC-Snap-In der Zertifizierungsstelle oder den Befehl certutil (mit angegebener Angabe von -backup oder -backupkey). Das Sichern des privaten Schlüssels mit dem ZERTIFIZIERUNGSSTELLEN-MMC-Snap-In oder certutil führt dazu, dass der private Schlüssel in die PKCS \# 12-Datei geschrieben wird. Obwohl diese PKCS \# 12-Datei kennwortgeschützt ist, sollte sie als äußerst vertraulich betrachtet und sicher gespeichert werden. Das Kennwort für die PKCS \# 12-Datei sollte auch vor nicht autorisierten Personen geschützt werden.

Ebenso können private Schlüssel nicht von den Sicherungs- und Wiederherstellungsfunktionen der Zertifikatdienste wiederhergestellt werden. Ein in einer PKCS 12-Datei enthaltener Zertifikatdienste-Sicherungsschlüssel \# kann durch das MMC-Snap-In der Zertifizierungsstelle oder durch den Befehl certutil (unter Angabe der Verben -restore oder -restorekey) wiederhergestellt werden. Beachten Sie, dass die Person, die den Wiederherstellungsvorgang ausführt, das Kennwort für die PKCS \# 12-Datei kennen muss.

Es gibt nur zwei Fälle, in denen ein privater Zertifikatdienste-Schlüssel gesichert werden muss. Der erste Fall ist nach der Installation von Zertifikatdiensten. Der zweite Fall ist nach einem Erneuerungsvorgang des Zertifikatdienstzertifikats.

 

 
