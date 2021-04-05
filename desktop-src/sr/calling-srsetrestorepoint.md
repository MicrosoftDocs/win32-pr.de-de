---
title: Aufrufen von srsettrestorepoint
description: Eine Anwendung kann einen Wiederherstellungspunkt erstellen, bevor Sie eine bedeutende Systemänderung, z. b. eine Installation, Deinstallation oder ein Featureupdate, verursacht.
ms.assetid: 77981e75-8c3f-4ecc-82f4-e88d68df661a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b877c4fe73bcedad363bb4c9cc770a9638550dbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712983"
---
# <a name="calling-srsetrestorepoint"></a>Aufrufen von srsettrestorepoint

Eine Anwendung kann einen Wiederherstellungspunkt erstellen, bevor Sie eine bedeutende Systemänderung, z. b. eine Installation, Deinstallation oder ein Featureupdate, verursacht.

Installationsprogramme sollten vor der Installation einen Wiederherstellungspunkt erstellen, indem Sie die [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) -Funktion mit dem **dwEventType** -Member der [**restorepointinfo**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-restorepointinfoa) -Struktur aufrufen, der auf System Änderung starten festgelegt ist \_ \_ . Um die Systemwiederherstellung zu benachrichtigen, dass die Installation abgeschlossen wurde, nennen Sie **SRSetRestorePoint** , wobei **dwEventType** auf End System Change festgelegt ist \_ \_ .

Wenn der Benutzer die Installation der Anwendung abbricht, kann das Installationsprogramm den Wiederherstellungspunkt entfernen, der beim Start der Installation erstellt wurde. Das Entfernen des Wiederherstellungs Punkts ist optional und kann verhindern, dass der Benutzer während des Abbruchs vom Installationsprogramm vorgenommene Änderungen wiederherstellt. Wenn das Installationsprogramm einen Wiederherstellungspunkt entfernen soll, kann er die [**srremoverestorepoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srremoverestorepoint) -Funktion aufrufen oder [**SRSetRestorePoint**](/windows/desktop/api/SRRestorePtAPI/nf-srrestoreptapi-srsetrestorepointa) aufrufen, wobei **dwrestorepointtype** auf "abgebrochen" festgelegt ist, \_ **dwEventType** auf End System Change festgelegt ist \_ \_ und **llsequencenumber** auf den Wert festgelegt ist, der durch den ursprünglichen Aufrufen von **srsetre**

**Windows 8:  **

Ein neuer Registrierungsschlüssel ermöglicht Anwendungsentwicklern das Ändern der Häufigkeit der Wiederherstellungspunkt Erstellung.

Anwendungen sollten diesen Schlüssel erstellen, um ihn zu verwenden, da er im System nicht bereits vorhanden ist. Wenn der Schlüssel nicht vorhanden ist, wird standardmäßig Folgendes angewendet: Wenn eine Anwendung die **SRSetRestorePoint** -Funktion aufruft, um einen Wiederherstellungspunkt zu erstellen, überspringt Windows das Erstellen dieses neuen Wiederherstellungs Punkts, wenn in den letzten 24 Stunden Wiederherstellungspunkte erstellt wurden. Bei der System Wiederherstellung wird das Element " **iisequencenumber** " der [**statemgrstatus**](/windows/win32/api/srrestoreptapi/ns-srrestoreptapi-statemgrstatus) -Struktur auf die Sequenznummer für den zuvor erstellten Wiederherstellungspunkt festgelegt, und der Wert des **nStatus** -Members wird auf " **Fehler \_ erfolgreich**" festgelegt. Die **srsettrestorepoint** -Funktion gibt **true** zurück.

Entwickler können Anwendungen schreiben, die den **DWORD** -Wert **systemrestorepointkreationfrequency** unter dem Registrierungsschlüssel **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** erstellen. Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden. Mit dem Wert dieses Registrierungsschlüssels kann die Häufigkeit der Wiederherstellungspunkt Erstellung geändert werden.

Wenn die Anwendung **SRSetRestorePoint** aufruft, um einen Wiederherstellungspunkt zu erstellen, und der Registrierungsschlüssel Wert 0 ist, wird die Erstellung des neuen Wiederherstellungs Punkts von der Systemwiederherstellung nicht übersprungen.

Wenn die Anwendung **SRSetRestorePoint** aufruft, um einen Wiederherstellungspunkt zu erstellen, und der Registrierungsschlüssel Wert die Ganzzahl N ist, überspringt die Systemwiederherstellung die Erstellung eines neuen Wiederherstellungs Punkts, wenn in den letzten N Minuten Wiederherstellungspunkte erstellt wurden.

**Windows 8:  **

Bei der Systemwiederherstellung, die auf Windows 8 ausgeführt wird, werden Dateien im Start Volume überwacht, die nur für die Systemwiederherstellung relevant Momentaufnahmen des von der System Wiederherstellung auf Windows 8 erstellten Start Volumes können gelöscht werden, wenn die Momentaufnahme später durch eine frühere Version von Windows verfügbar gemacht wird. Beachten Sie, dass zwar nur ein System Volume vorhanden ist, aber für jedes Betriebssystem in einem Multiboot-System ein Start Volume vorhanden ist.

Entwickler können Anwendungen schreiben, die den **DWORD** -Wert **scopesnapshots** unter dem Registrierungsschlüssel **HKLM \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion \\ SystemRestore** erstellen. Wenn dieser Registrierungsschlüssel Wert 0 ist, erstellt die System Wiederherstellung Momentaufnahmen des Start Volumes auf die gleiche Weise wie in früheren Versionen von Windows. Wenn dieser Wert gelöscht wird, wird bei der Systemwiederherstellung, die auf Windows 8 ausgeführt wird, das Erstellen von Momentaufnahmen, die Dateien im Start Volume überwachen, die nur für die Systemwiederherstellung

Ein Beispiel finden Sie unter [Verwenden der System Wiederherstellung](using-system-restore.md).

 

 




