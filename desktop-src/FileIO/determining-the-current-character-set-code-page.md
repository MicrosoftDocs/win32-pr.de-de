---
description: Die arefileapisansi-Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden.
ms.assetid: 97ed3b08-ca5d-4ac2-bf1a-7eec40f9ffc2
title: Festlegen der Codepage für den aktuellen Zeichensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e180d908605ec423314ef2197829fd95ff51a18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865544"
---
# <a name="determining-the-current-character-set-code-page"></a>Festlegen der Codepage für den aktuellen Zeichensatz

Die [**arefileapisansi**](/windows/desktop/api/fileapi/nf-fileapi-arefileapisansi) -Funktion bestimmt, ob die Datei-e/a-Funktionen die ANSI-oder OEM-Zeichensatz-Codepage verwenden. Die Funktion [**setfileapistoansi**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) bewirkt, dass die Funktionen die ANSI-Codepage verwenden. Die [**setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) -Funktion bewirkt, dass die Funktionen die OEM-Codepage verwenden.

Standardmäßig verwenden Datei-e/a-Funktionen ANSI-Dateinamen. Die von Kernel32.dll exportierten Funktionen, die Dateinamen akzeptieren oder zurückgeben, sind von der Datei Code Page-Einstellung betroffen.

Sowohl [**setfileapistoansi**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistoansi) als auch [**setfileapistooem**](/windows/desktop/api/fileapi/nf-fileapi-setfileapistooem) legen die Codepage pro Prozess statt pro Thread oder pro Computer fest.

 

 



