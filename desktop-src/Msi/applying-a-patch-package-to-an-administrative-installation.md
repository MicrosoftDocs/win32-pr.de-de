---
description: Sie können das kleine Update auf ein administratives Quell Abbild von MNP2000.msi anwenden, indem Sie das Beispiel Patch MNP2000. msp installieren, das beim Erstellen eines Patchpakets erstellt wurde.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Anwenden eines Patchpakets auf eine administrative Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9e0645bdd2c472e725a3a5eeef22693aa35b8d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959536"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Anwenden eines Patchpakets auf eine administrative Installation

Sie können das kleine Update auf ein administratives Quell Abbild von MNP2000.msi anwenden, indem Sie das Beispiel Patch MNP2000. msp installieren, das beim [Erstellen eines Patchpakets](generating-a-patch-package.md)erstellt wurde. Das Update kann dann an Benutzer weitergegeben werden, indem angefordert wird, dass die Anwendung erneut aus dem neuen administrativen Quell Image installiert wird.

Ein Administrator kann die folgende Befehlszeile verwenden, um das administrative Quell Image unter MNP2000.msi//Server/auf ein neues Quell Image zu aktualisieren, das von einer administrativen Installation von einer vollständig aktualisierten CD-ROM erstellt wird.

**msiexec/a//Server/MNP2000.msi/p MNP2000. msp**

Mitglieder der Arbeitsgruppe, die MNP2000 verwendet, müssen dann die Anwendung erneut aus dem neuen administrativen Quell Image installieren, um das Update zu erhalten.

Um die Anwendungen vollständig neu zu installieren und die aktualisierte MSI-Datei auf dem Computer des Benutzers zwischenzuspeichern, können Benutzer einen der folgenden Befehle eingeben.

**msiexec/fvomus//Server/MNP2000.msi**

**msiexec/I//Server/MNP2000.msi REINSTALL = ALL REINSTALLMODE = vomus**

Wenn Sie nur das aktualisierte Konzert Feature neu installieren und die aktualisierte MSI-Datei auf dem Computer des Benutzers zwischenspeichern möchten, können Benutzer den folgenden Befehl eingeben.

**msiexec/I//Server/MNP2000.msi REINSTALL = Concert REINSTALLMODE = vomus**

## <a name="next-example"></a>Nächstes Beispiel

[Beispiel für eine Lokalisierung](a-localization-example.md)

 

 



