---
title: Windows 7-Sicherung und-Wiederherstellung als veraltet markiert
description: Windows 7-Sicherung und-Wiederherstellung als veraltet markiert
ms.assetid: 89FB9C1B-FEE8-4508-9501-EA139F3706F7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc20fa7ada55ada1f3c2f70c54955cec3d51666
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "106340741"
---
# <a name="windows-7-backup-and-restore-deprecated"></a>Windows 7-Sicherung und-Wiederherstellung als veraltet markiert

## <a name="platform"></a>Plattform

**Clients** – Windows 8 


## <a name="description"></a>BESCHREIBUNG

Es gibt zwar keine Verhaltensänderungen an Sicherung und Wiederherstellung, diese Funktion ist jedoch veraltet und wird nicht aktualisiert. Sie wurde nur selten verwendet, und ihre Funktionalität wurde durch die neue Funktion "Datei Versionsverlauf" ersetzt. Es wird unter Windows 8 und Enthusiasten ausgeliefert, die von Windows 7 auf Windows 8 aktualisiert haben oder von der Sicherung und Wiederherstellung abhängig sind, oder die Datenträger Abbild Sicherung kann Sie weiterhin verwenden. Alle Zugriffspunkte für die Sicherung und Wiederherstellung, mit Ausnahme der Systemsteuerung, wurden jedoch entfernt. Das von der Sicherung und Wiederherstellung verwendete System Steuerungs Applet wurde in Windows 7-Dateiwiederherstellung umbenannt.

OEMs, die den Registrierungsschlüssel für die Deaktivierung der Sicherungs Benachrichtigung in Ihren Images festgelegt haben, müssen das nicht mehr tun.

Es wird nicht empfohlen, beide Features gleichzeitig zu verwenden. Der Datei Versionsverlauf überprüft, ob der Sicherungs Zeitplan vorhanden und aktiv ist. wenn er einen gefunden hat, kann er von Benutzern nicht eingeschaltet werden. In diesem Fall müssen Benutzer, die den Datei Versionsverlauf verwenden möchten, den Windows-Sicherungs Zeitplan löschen.

## <a name="manifestation"></a>Ausstrahlung

Workflows können unterbrochen werden, und die Dokumentation, die sich auf die vorherige Methode zum Zugreifen auf das Windows-Sicherungs-und Wiederherstellungs Feature bezieht, muss aktualisiert werden, um diese Änderungen widerzuspiegeln.

## <a name="mitigation"></a>Minderung

Apps, die möglicherweise die Sicherung und Wiederherstellung initiieren, sollten neu geschrieben werden, um zu überprüfen, ob der Datei Versionsverlauf auf ON fest steht, und Benutzern

 

 




