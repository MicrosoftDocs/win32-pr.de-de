---
description: Der Cabinet-Datentyp muss in der Spalte "Cabinet" der Media-Tabelle verwendet werden.
ms.assetid: 149c74ea-4342-45dd-8da4-4dfa7f4317a0
title: Kabinett
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16acfd031a6580f898d4cb464a15c895644995a2499a62ac79c9adeced8ccec1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105360"
---
# <a name="cabinet"></a>Kabinett

Der Cabinet-Datentyp muss in der Spalte "Cabinet" der [Media-Tabelle verwendet werden.](media-table.md)

Wenn dem Namen des Schränken das Nummernzeichen voran steht, wird die Schränkung als Datenstrom innerhalb des Pakets gespeichert. Die Zeichenfolge, die auf \# folgt, ist ein [Bezeichner](identifier.md) für diesen Datenstrom. Beachten Sie, dass beim Namen eines Schränkes die Schreibung beachtet wird, wenn die Schränkung als Datenstrom gespeichert wird.

Wenn dem Namen des Schränkchens nicht das Nummernzeichen vorangegangen ist, wird die Schränkung in einer separaten Datei gespeichert, die sich im Stamm der Quellstruktur befindet, die von der \# [Verzeichnistabelle angegeben wird.](directory-table.md) Die Schränkdatei muss die Syntax für kurze Dateinamen verwenden, die aus einem Achtzeichennamen, einem Zeitraum und einer Drei-Zeichen-Erweiterung besteht. Der Cabinet-Datentyp kann nicht die Syntax short \| longname für Dateinamen verwenden. Wenn die Schränkdatei als separate Datei gespeichert wird, wird beim Namen der Datei "cabinet" die Schreibung nicht beachtet.

Um Speicherplatz zu sparen, entfernt das Installationsprogramm alle in die .msi-Datei eingebetteten Schränken, bevor das Installationspaket auf dem Computer des Benutzers zwischenspeichert.

Weitere [Informationen finden Sie unter Including a Cabinet File in an Installation](including-a-cabinet-file-in-an-installation.md).

 

 



