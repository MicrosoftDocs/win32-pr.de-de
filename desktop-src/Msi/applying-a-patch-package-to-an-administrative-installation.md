---
description: Sie können das kleine Update auf ein administratives Quellimage von MNP2000.msi anwenden, indem Sie den Beispielpatch MNP2000.msp installieren, der unter Generieren eines Patchpakets erstellt wurde.
ms.assetid: 24ae9cd6-2057-4345-90ec-943da7620cb0
title: Anwenden eines Patchpakets auf eine Administratorinstallation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c29cbec604ae18745348a62f147d13d2ccbf06c0620b3a5dcca7c6c009045b7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105440"
---
# <a name="applying-a-patch-package-to-an-administrative-installation"></a>Anwenden eines Patchpakets auf eine Administratorinstallation

Sie können das kleine Update auf ein administratives Quellimage von MNP2000.msi anwenden, indem Sie den Beispielpatch MNP2000.msp installieren, der unter [Generieren eines Patchpakets](generating-a-patch-package.md)erstellt wurde. Das Update kann dann an Benutzer weitergegeben werden, indem angefordert wird, dass die Anwendung über das neue Administrative Source-Image neu installiert wird.

Ein Administrator kann die folgende Befehlszeile verwenden, um das administrative Quellimage unter "/server/MNP2000.msi" auf ein neues Quellimage zu aktualisieren, das mit dem identisch ist, das von einer Administratorinstallation aus einer vollständig aktualisierten CD-ROM erstellt wird.

**msiexec /a /server/MNP2000.msi /p MNP2000.msp**

Mitglieder der Arbeitsgruppe, die MNP2000 verwenden, müssen dann die Anwendung aus dem neuen Administrative Source-Image neu installieren, um das Update zu erhalten.

Um die Anwendungen vollständig neu zu installieren und die aktualisierte .msi-Datei auf dem Computer des Benutzers zwischenzuspeichern, können Benutzer einen der folgenden Befehle eingeben.

**msiexec /fvomus /server/MNP2000.msi**

**msiexec /I "/server/MNP2000.msi REINSTALL=ALL REINSTALLMODE=vomus"**

Um nur das aktualisierte Concert-Feature neu zu installieren und die aktualisierte .msi-Datei auf dem Computer des Benutzers zwischenzuspeichern, können Benutzer den folgenden Befehl eingeben.

**msiexec /I "/server/MNP2000.msi REINSTALL=Concert REINSTALLMODE=vomus"**

## <a name="next-example"></a>Nächstes Beispiel

[Ein Lokalisierungsbeispiel](a-localization-example.md)

 

 



