---
description: Caching-Steuerelement in transaktionalen NTFS.
ms.assetid: 0fd272ee-cf5f-4ba9-b8aa-ff0016f51d4b
title: Bereitstellen von transaktionalen NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7c44e0ad3b83854e56d18171072a7cb4615d5c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959355"
---
# <a name="deploying-transactional-ntfs"></a>Bereitstellen von transaktionalen NTFS

Transaktionale NTFS (TxF), wie die meisten Transaktions Mechanismen, sind von der korrekten Reihenfolge der Daten Schreibvorgänge abhängig. Die Gewährleistung einer ordnungsgemäßen Schreib Reihenfolge erfordert eine explizite Steuerung der Zwischenspeicherung Um diese Anforderung zu erfüllen, erfordert TxF, dass die Festplattenlaufwerke die cachingsteuerungmechanismen implementieren, die Teil standardisierter Laufwerk Schnittstellen wie SCSI, SATA und ATA sind.

Der von TxF verwendete Cache Steuerungsmechanismus ist ein Flag, das als "Force Unit Access (Fua)"-Funktion bezeichnet wird. Dieses Flag gibt an, dass das Laufwerk die Daten vor dem Abschluss der Signalisierung in den stabilen Medien Speicher schreiben soll. An bestimmten kritischen Punkten innerhalb einer Transaktion muss TxF einen Fua ausgeben, um sicherzustellen, dass einige Steuerungsdaten, die für ein erfolgreiches Rollback einer Transaktion erforderlich sind, bei einem Stromausfall nicht verloren gehen.

Laufwerke der Server Klasse (SCSI-und Fiber-Channel) unterstützen in der Regel das Fua-Flag. Ab Vista unterstützt Windows das Fua-Flag nur für SCSI-und Fiber-Kanal Datenträger.

Bei waren Laufwerken (ATA/SATA/USB) verfügt TxF über Zeiträume, in denen ein Laufwerks Stromausfall dazu führen kann, dass TxF die Transaktion nicht ordnungsgemäß zurücksetzen kann, sodass die Daten in einem inkonsistenten Zustand belassen werden, es sei denn, der Schreib Cache des Laufwerks ist deaktiviert.

Einige Hostbus Adapter (HBAs) und Speichercontroller (z. b. RAID-Systeme) verfügen über integrierte Cache Caches. Da diese Geräte beim Auftreten eines Strom Fehlers zwischengespeicherte Daten erhalten, müssen alle mit ihnen verbundenen Datenträger das Fua-Flag nicht berücksichtigen. Außerdem muss ein Datenträger, dessen Stromversorgung durch eine unterbrechungsfreie Stromversorgung (UPS) geschützt ist, das Fua-Flag nicht berücksichtigen. Dies liegt daran, dass die UPS die Leistung so lange aufrechterhalten, dass der Datenträger den Cache auf die Medien leert.

Durch das Deaktivieren des Schreib Caches eines Laufwerks entfällt die Anforderung, dass das Laufwerk das Fua-Flag beachtet. Sie können den Schreib Cache eines Datenträgers deaktivieren, indem Sie den Steuerungs Code für den [**IOCTL- \_ \_ Datenträger Satz \_ Cache \_ Informationen**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_disk_set_cache_information) auf dem Datenträger ausgeben. Der Status des Schreib Caches (ein/aus) wird über Systemneustarts hinweg beibehalten. Das Ausstellen dieses Steuerungs Codes hat für alle e/a-Vorgänge, die für diesen Datenträger ausgegeben werden, sehr deutliche Auswirkungen auf die Leistung, was höchstwahrscheinlich eine spürbare Leistungsminderung darstellt. Die Verwendung dieses Steuerungs Codes sollte vor der Bereitstellung sorgfältig in Erwägung gezogen werden.

> [!Note]  
> Damit TxF die Integrität Ihrer Daten durch Stromausfälle konsistent schützen kann, muss das System mindestens eines der folgenden Kriterien erfüllen:
>
> -   Verwenden Sie Server-Klassen Datenträger (SCSI, Fiber-Channel).
> -   Stellen Sie sicher, dass die Datenträger mit einem HBA mit Akku gestütztem Zwischenspeicher verbunden sind.
> -   Verwenden Sie einen Speichercontroller (z. b. RAID-System) als Speichergerät.
> -   Stellen Sie sicher, dass die Stromversorgung des Datenträgers durch ein UPS geschützt ist
> -   Stellen Sie sicher, dass das Schreib Cache Feature des Datenträgers deaktiviert ist.

 

 

 



