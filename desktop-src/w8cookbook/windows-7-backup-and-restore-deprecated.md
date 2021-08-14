---
title: 'Windows 7: Sicherung und Wiederherstellung veraltet'
description: 'Windows 7: Sicherung und Wiederherstellung veraltet'
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5975483797423515a4c04a35f8766de241553cb98a386bd53adcc7970977f7e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211229"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7: Sicherung und Wiederherstellung veraltet

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Es gibt zwar keine Verhaltensänderungen bei Sicherung und Wiederherstellung, diese Funktion ist jedoch veraltet und wird nicht aktualisiert. Es wurde selten verwendet, und seine Funktionalität wurde durch das neue feature Dateiversionsverlauf ersetzt. Es wird in Windows 8 geliefert, und Sports, die von Windows 7 auf Windows 8 aktualisiert haben oder von Sicherung und Wiederherstellung abhängig sind, oder Datenträgerimagesicherungen können sie weiterhin verwenden. Allerdings wurden alle Zugriffspunkte auf Sicherung und Wiederherstellung mit Ausnahme der Systemsteuerung entfernt. Das Systemsteuerung Applet, das von Backup and Restore verwendet wird, wurde in Windows 7 Dateiwiederherstellung umbenannt.

OEMs, die den Registrierungsschlüssel zum Deaktivieren der Sicherungsbenachrichtigung in ihren Images festgelegt haben, müssen dies nicht mehr tun.

Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden. Dateiversionsverlauf überprüft, ob der Sicherungszeitplan vorhanden ist und aktiv ist. Wenn ein Solcher gefunden wird, können Benutzer ihn nicht aktivieren. In diesem Fall müssen Benutzer, die Dateiversionsverlauf verwenden möchten, den Windows-Sicherung Zeitplan löschen.

## <a name="manifestation"></a>Manifestation

Workflows können unterbrochen werden, und die Dokumentation, die sich auf die vorherige Methode für den Zugriff auf die Windows-Sicherung- und Wiederherstellungsfunktion bezieht, muss aktualisiert werden, um diese Änderungen widerzuspiegeln.

## <a name="mitigation"></a>Minderung

Apps, die die Sicherung und Wiederherstellung auslösen können, sollten neu geschrieben werden, um zu überprüfen, ob Dateiversionsverlauf aktiviert ist, und Benutzern die Auswahl ihrer bevorzugten Methode ermöglichen.

 

 




