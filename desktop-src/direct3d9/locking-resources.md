---
description: Das Sperren einer Ressource bedeutet, cpu-Zugriff auf ihren Speicher zu gewähren.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Sperren von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6cdb7cde646bd5073bc0c5b574694be69f05f1bf15d8c5c08e00b7182cfe044
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118799493"
---
# <a name="locking-resources-direct3d-9"></a>Sperren von Ressourcen (Direct3D 9)

Das Sperren einer Ressource bedeutet, cpu-Zugriff auf ihren Speicher zu gewähren. Die folgenden Sperroptionen sind für Ressourcen definiert:

-   D3DLOCK \_ DISCARD
-   D3DLOCK \_ READONLY
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ KEIN \_ GEÄNDERTES \_ UPDATE

Ausführliche Informationen zu Sperrflags und deren Beziehung zu bestimmten Ressourcen finden Sie auf den Referenzseiten zu den einzelnen Methoden zum Sperren von Ressourcen. Anwendungsentwickler sollten beachten, dass die Flags D3DLOCK \_ DISCARD, D3DLOCK \_ READONLY und D3DLOCK \_ NOOVERWRITE nur Hinweise sind. Die Laufzeit überprüft nicht, ob Anwendungen die von diesen Flags angegebenen Funktionen befolgen. Eine Anwendung, die D3DLOCK \_ READONLY angibt, dann aber in die Ressource schreibt, sollte nicht definierte Ergebnisse erwarten. Im Allgemeinen funktioniert die Arbeit mit Sperrflags, einschließlich der Sperrverwendungsflags, nicht garantiert in späteren Releases und kann zu erheblichen Leistungseinbußen gehören.

Auf einen Sperrvorgang folgt ein Entsperrvorgang. Beispielsweise gibt die Anwendung nach dem Sperren einer Textur den direkten Zugriff auf gesperrte Texturen auf, indem sie sie entsperrt. Zusätzlich zum Gewähren des Prozessorzugriffs werden alle anderen Vorgänge, die diese Ressource betreffen, für die Dauer einer Sperre serialisiert. Es ist nur eine einzelne Sperre für eine Ressource zulässig, auch für nicht überlappende Bereiche, und es können keine Zugriffstastenvorgänge auf einer Oberfläche durchgeführt werden, während ein Sperrvorgang auf dieser Oberfläche aussteht.

Jede Ressourcenschnittstelle verfügt über Methoden zum Sperren der enthaltenen Puffer. Jede Texturressource kann auch einen Teil dieser Ressource sperren. 2D-Ressourcen (Oberflächen) ermöglichen das Sperren von Unterrechtecke, und Volumeressourcen ermöglichen das Sperren von untergeordneten Volumes oder Feldern. Jede Sperrmethode gibt eine -Struktur zurück, die einen Zeiger auf den Speicher enthält, der die Ressource unterstützt, und Werte, die die Entfernungen zwischen Zeilen oder Datenebenen abhängig vom Ressourcentyp darstellen. Weitere Informationen finden Sie in den Methodenlisten für die Ressourcenschnittstellen. Der zurückgegebene Zeiger zeigt immer auf das obere linke Byte in den gesperrten Unterbereichen.

Wenn Sie mit Index- und Scheitelpunktpuffern arbeiten, können Sie mehrere Sperraufrufe vornehmen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperraufrufe mit der Anzahl der Entsperrungsaufrufe übereinstimmt.

DxTn speichert Pixel in codierten 4x4-Blöcken und kann nur an 4x4-Grenzen gesperrt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 



