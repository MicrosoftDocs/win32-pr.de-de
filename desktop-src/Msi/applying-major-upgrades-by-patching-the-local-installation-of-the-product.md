---
description: Ein großes Upgrade kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung über die Befehlszeile oder eine ausführbare Datei Patchen.
ms.assetid: be651457-5c66-478b-89d5-3d7607702b8e
title: Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 043d106ed9f8d6455ab4412959b70854a526a4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864483"
---
# <a name="applying-major-upgrades-by-patching-the-local-installation-of-the-product"></a>Anwenden von größeren Upgrades durch Patchen der lokalen Installation des Produkts

Ein großes Upgrade kann auf eine Anwendung angewendet werden, indem Sie die lokale Installation der Anwendung über die Befehlszeile oder eine ausführbare Datei Patchen.

> [!Note]  
> Das Bereitstellen eines größeren Upgrades als Patch-Paket wird nicht empfohlen, da ein wichtiges Upgradepatch-Paket nicht mit anderen Updates sequenziert werden kann und da es sich bei dem Patch nicht um einen nicht [installierbaren Patch](uninstallable-patches.md)handelt. Das [Msimsp.exe](msimsp-exe.md) -Hilfsprogramm kann nicht zum Generieren eines Patchpakets verwendet werden, das ein großes Upgrade anwendet. Wenden Sie stattdessen größere Upgrades an, wie unter [Anwenden von größeren Upgrades durch die Installation des Produkts](applying-major-upgrades-by-installing-the-product.md)beschrieben.

 

**So wenden Sie einen wichtigen Upgradepatch auf eine lokale Installation des Produkts an**

1.  Starten Sie die Installation des Patches von der Befehlszeile aus, oder verwenden Sie eine ausführbare Datei. Um von der Befehlszeile aus zu starten, verwenden Sie msiexec/p Patch. msp. Um von einer ausführbaren Datei zu starten, rufen Sie [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder die [**Applypatch-Methode**](installer-applypatch.md) auf, und geben Sie dieselben Befehlszeilenargumente an.
2.  Beim Patchen einer Client Installation wird die Installationsquelle vom Installationsprogramm ignoriert, und die Dateien, die bereits auf dem Computer des Benutzers installiert sind, werden gepatcht.
3.  Das Installationsprogramm ändert alle gepatchten Komponenten, die als "Run-From-Source" gekennzeichnet sind, in "lokal Benutzer können diese Komponenten nicht aus der Quelle ausführen, solange der Patch auf dem Computer verbleibt.
4.  Das Installationsprogramm fügt alle Transformationen hinzu, die zum Aktualisieren der MSI-Datei verwendet werden, oder fügt dem Benutzerprofil patchspezifische Informationen hinzu.
5.  Das Installationsprogramm speichert die MSI-Datei auf dem Computer des Benutzers zwischen, sodass die Anwendung bei Bedarf installiert, neu installiert und repariert werden kann. Nachdem ein Patch auf eine eigenständige Installation angewendet wurde, verweist das Installationsprogramm auf zwei oder mehr Quell Listen auf externe Dateien: eine für die ursprüngliche Quelle und eine für jeden angewendeten Patch.

 

 



