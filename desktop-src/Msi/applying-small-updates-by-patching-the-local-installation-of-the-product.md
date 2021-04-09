---
description: Ein kleines Update kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung Patchen.
ms.assetid: 2a04ffd0-d5b6-44f3-bef2-73f59179aed1
title: Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bced3e7f69761ff3e270046718eedb9032cab8a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959533"
---
# <a name="applying-small-updates-by-patching-the-local-installation-of-the-product"></a>Anwenden von kleinen Updates durch Patchen der lokalen Installation des Produkts

Ein kleines Update kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung Patchen.

**So wenden Sie einen kleinen Update Patch auf eine lokale Installation des Produkts an**

1.  Starten Sie die Installation des Patches von der Befehlszeile aus, oder verwenden Sie eine ausführbare Datei. Um von der Befehlszeile aus zu starten, verwenden Sie **msiexec/p Patch. msp \[ REINSTALL =**_Feature List_ *_\] REINSTALLMODE = omus_*. Um von einer ausführbaren Datei zu starten, rufen Sie [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder die [**Applypatch-Methode**](installer-applypatch.md) auf, und geben Sie dieselben Befehlszeilenargumente an.
2.  Beim Patchen einer Client Installation wird die Installationsquelle vom Installationsprogramm ignoriert, und die Dateien, die bereits auf dem Computer des Benutzers installiert sind, werden gepatcht.
3.  Das Installationsprogramm ändert alle gepatchten Komponenten, die als "Run-From-Source" gekennzeichnet sind, in "lokal Benutzer können diese Komponenten nicht aus der Quelle ausführen, solange der Patch auf dem Computer verbleibt.
4.  Das Installationsprogramm fügt alle Transformationen hinzu, die zum Aktualisieren der MSI-Datei verwendet werden, oder fügt dem Benutzerprofil patchspezifische Informationen hinzu.
5.  Das Installationsprogramm speichert die MSI-Datei auf dem Computer des Benutzers zwischen, sodass die Anwendung bei Bedarf installiert, neu installiert und repariert werden kann. Nach dem Anwenden eines Patches auf eine eigenständige Installation verweist das Installationsprogramm auf zwei oder mehr Quell Listen auf externe Dateien: eine für die ursprüngliche Quelle und eine für jeden angewendeten Patch.

 

 



