---
title: Aufrufen von SRSetRestorePoint
description: Eine Anwendung kann einen Wiederherstellungspunkt erstellen, bevor sie eine erhebliche Systemänderung verursacht, z. B. eine Installation, Deinstallation oder ein Featureupdate.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84ee2fc64fc74dd9ceeff4856a6a63effe0667ff2bd837d7dc8ae521172a1c7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119592210"
---
# <a name="calling-srsetrestorepoint"></a>Aufrufen von SRSetRestorePoint

Eine Anwendung kann einen Wiederherstellungspunkt erstellen, bevor sie eine erhebliche Systemänderung verursacht, z. B. eine Installation, Deinstallation oder ein Featureupdate.

Installationsprogramme sollten unmittelbar vor der Installation einen Wiederherstellungspunkt erstellen, indem sie die [**SRSetRestorePoint-Funktion**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) aufrufen, wobei der **dwEventType-Member** der [**RESTOREPOINTINFO-Struktur**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) auf BEGIN SYSTEM CHANGE festgelegt \_ \_ ist. Um die Systemwiederherstellung zu benachrichtigen, dass die Installation abgeschlossen wurde, rufen Sie **SRSetRestorePoint** auf, wobei **dwEventType** auf END SYSTEM CHANGE festgelegt \_ \_ ist.

Wenn der Benutzer die Anwendungsinstallation abbricht, kann das Installationsprogramm den Wiederherstellungspunkt entfernen, den er zu Beginn der Installation erstellt hat. Das Entfernen des Wiederherstellungspunkts ist optional und kann verhindern, dass der Benutzer unbeabsichtigte Änderungen wiederhergestellt, die vom Installationsprogramm während des Abbruchs vorgenommen wurden. Wenn das Installationsprogramm einen Wiederherstellungspunkt entfernen soll, kann er die [**SRRemoveRestorePoint-Funktion**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) aufrufen oder [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) aufrufen, wobei **dwRestorePointType** auf CANCELLED \_ OPERATION, **dwEventType** auf END \_ SYSTEM CHANGE und \_ **llSequenceNumber** auf den Wert festgelegt ist, der durch den ersten Aufruf von **SRSetRestorePoint** zurückgegeben wird.

**Windows 8: **

Mit einem neuen Registrierungsschlüssel können Anwendungsentwickler die Häufigkeit der Wiederherstellungspunkterstellung ändern.

Anwendungen sollten diesen Schlüssel erstellen, um ihn zu verwenden, da er im System nicht bereits vorhanden ist. Wenn der Schlüssel nicht vorhanden ist, gilt standardmäßig Folgendes. Wenn eine Anwendung die **SRSetRestorePoint-Funktion** aufruft, um einen Wiederherstellungspunkt zu erstellen, überspringt Windows die Erstellung dieses neuen Wiederherstellungspunkts, wenn in den letzten 24 Stunden Wiederherstellungspunkte erstellt wurden. Die Systemwiederherstellung legt den **IISequenceNumber-Member** der [**STATEMGRSTATUS-Struktur**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) auf die Sequenznummer für den Wiederherstellungspunkt fest, der zuvor am Tag erstellt wurde, und legt den Wert des **nStatus-Members** auf **ERROR \_ SUCCESS** fest. Die **SRSetRestorePoint-Funktion** gibt **TRUE** zurück.

Entwickler können Anwendungen schreiben, die den **DWORD-Wert** **SystemRestorePointCreationFrequency** unter dem Registrierungsschlüssel **HKLM \\ Software Microsoft Windows \\ NT \\ \\ CurrentVersion \\ SystemRestore** erstellen. Der Wert dieses Registrierungsschlüssels kann die Häufigkeit der Erstellung des Wiederherstellungspunkts ändern. Der Wert dieses Registrierungsschlüssels kann die Häufigkeit der Erstellung des Wiederherstellungspunkts ändern.

Wenn die Anwendung **SRSetRestorePoint** aufruft, um einen Wiederherstellungspunkt zu erstellen, und der Registrierungsschlüsselwert 0 ist, überspringt die Systemwiederherstellung nicht das Erstellen des neuen Wiederherstellungspunkts.

Wenn die Anwendung **SRSetRestorePoint** aufruft, um einen Wiederherstellungspunkt zu erstellen, und der Registrierungsschlüsselwert die ganze Zahl N ist, überspringt die Systemwiederherstellung die Erstellung eines neuen Wiederherstellungspunkts, wenn in den letzten N Minuten Wiederherstellungspunkte erstellt wurden.

**Windows 8: **

Die auf Windows 8 ausgeführte Systemwiederherstellung überwacht Dateien auf dem Startvolume, die nur für die Systemwiederherstellung relevant sind. Momentaufnahmen des Startvolumes, das von system restore erstellt wurde und auf Windows 8 ausgeführt wird, können gelöscht werden, wenn die Momentaufnahme anschließend von einer früheren Version von Windows verfügbar gemacht wird. Beachten Sie, dass zwar nur ein Systemvolume vorhanden ist, aber für jedes Betriebssystem in einem Multistartsystem ein Startvolume vorhanden ist.

Entwickler können Anwendungen schreiben, die den **DWORD-Wert** **ScopeSnapshots** unter dem Registrierungsschlüssel **HKLM \\ Software Microsoft Windows \\ NT \\ \\ CurrentVersion \\ SystemRestore** erstellen. Wenn dieser Registrierungsschlüsselwert 0 ist, erstellt die Systemwiederherstellung Momentaufnahmen des Startvolumes auf die gleiche Weise wie in früheren Versionen von Windows. Wenn dieser Wert gelöscht wird, wird die Auf Windows 8 ausgeführte Systemwiederherstellung mit dem Erstellen von Momentaufnahmen fortgesetzt, die Dateien auf dem Startvolume überwachen, die nur für die Systemwiederherstellung relevant sind.

Ein Beispiel finden Sie unter [Verwenden der Systemwiederherstellung.](using-system-restore.md)

 

 




