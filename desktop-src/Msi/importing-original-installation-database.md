---
description: Beginnen Sie, das Upgradepaket zu erstellen, indem Sie das Installationspaket und die Quellverzeichnis Struktur des ursprünglichen Produkts kopieren.
ms.assetid: 279f0ab6-a6fc-4594-af6c-5a69d6167300
title: Importieren der ursprünglichen Installations Datenbank
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390a51e1ef068124fcdf85142ab01406d92f9a85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373160"
---
# <a name="importing-original-installation-database"></a>Importieren der ursprünglichen Installations Datenbank

Beginnen Sie, das Upgradepaket zu erstellen, indem Sie das Installationspaket und die Quellverzeichnis Struktur des ursprünglichen Produkts kopieren. Anweisungen zum Erstellen des Installationspakets für MNP2000 sind in [einem Installations Beispiel](an-installation-example.md)angegeben. Kopieren Sie die Inhalte der folgenden Ordner:

C: \\ Beispiel \\MNP2000.msi

C: \\ Beispiel für \\ Notepad\\

C: \\ Beispiel \\ Binär\\

C: \\ Beispiel \\ Symbol\\

Aktualisieren Sie den Inhalt des Ordners Notepad, damit Sie mit der unter [Planen eines größeren Upgrades](planning-a-major-upgrade.md)beschriebenen Quelle identisch sind. Entfernen Sie alle veralteten Quelldateien, z. b. Baseball.txt, und ersetzen Sie durch die aktualisierten Dateien, z. b. Baseba01.txt. Fügen Sie die zusätzlichen neuen, vom Upgrade bereitgestellten Dateien hinzu, z. b. Opera01.txt.

Benennen Sie MNP2000.msi in MNP2001.msi um. In den nachfolgenden Schritten verwenden Sie einen Tabellen-Editor, um diese Datenbank für das Upgrade in die MSI-Datei zu ändern. Datenbanktabellen, die nicht explizit in den nachfolgenden Abschnitten geändert werden, sind identisch mit den Tabellen in der Datenbank des ursprünglichen Produkts, MNP2000.msi.

[Fortsetzen](updating-directory-structure-for-an-upgrade.md)

 

 



