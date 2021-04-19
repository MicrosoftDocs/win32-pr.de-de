---
description: Das Sperren einer Ressource bedeutet, den CPU-Zugriff auf den Speicher zu gewähren.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Sperren von Ressourcen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106342553"
---
# <a name="locking-resources-direct3d-9"></a>Sperren von Ressourcen (Direct3D 9)

Das Sperren einer Ressource bedeutet, den CPU-Zugriff auf den Speicher zu gewähren. Die folgenden Sperr Optionen sind für Ressourcen definiert:

-   D3DLOCK \_ verwerfen
-   D3DLOCK \_ schreibgeschützt
-   D3DLOCK \_ noüberschreibung
-   D3DLOCK \_ nosyslock
-   D3DLOCK \_ kein \_ Dirty \_ Update

Ausführliche Informationen zu Sperr Flags und deren Beziehung zu bestimmten Ressourcen finden Sie auf den Referenzseiten zu den einzelnen Methoden zum Sperren von Ressourcen. Anwendungsentwickler sollten beachten, dass die \_ Flags D3DLOCK DISCARD, D3DLOCK Read \_ only und D3DLOCK \_ noüberschreibung nur Hinweise sind. Die Laufzeit überprüft nicht, ob Anwendungen den von diesen Flags angegebenen Funktionen folgen. Eine Anwendung, die D3DLOCK-schreibgeschützt angibt, \_ aber dann in die Ressource schreibt, sollte nicht definierte Ergebnisse erwarten. Im Allgemeinen ist es nicht gewährleistet, dass die Verwendung von Sperrflags, einschließlich der sperrnutzungsflags, in späteren Releases funktioniert und eine erhebliche Leistungs Einbuße verursachen kann.

Auf einen Sperr Vorgang folgt ein Entsperrvorgang. Wenn z. b. eine Textur gesperrt ist, gibt die Anwendung den direkten Zugriff auf gesperrte Texturen aus, indem Sie sie entsperrt. Zusätzlich zum Gewähren von Prozessor Zugriff werden alle anderen Vorgänge, die diese Ressource betreffen, für die Dauer einer Sperre serialisiert. Nur eine einzige Sperre für eine Ressource ist zulässig, auch bei nicht überlappenden Regionen, und es können keine Zugriffstasten auf einer Oberfläche fortgeführt werden, während ein Sperr Vorgang auf dieser Oberfläche aussteht.

Jede Ressourcen Schnittstelle verfügt über Methoden zum Sperren der enthaltenen Puffer. Jede Textur Ressource kann auch einen Teil Teil dieser Ressource sperren. 2D-Ressourcen (Oberflächen) ermöglichen das Sperren von unter Rechtecke, und volumeressourcen ermöglichen das Sperren von Subvolumes oder Feldern. Jede Lock-Methode gibt eine-Struktur zurück, die einen Zeiger auf den Speicher, der die Ressource unterstützt, und die Werte, die die Abstände zwischen Zeilen oder Daten Ebenen darstellen, abhängig vom Ressourcentyp enthält. Weitere Informationen finden Sie in den Methoden Listen für die Ressourcen Schnittstellen. Der zurückgegebene Zeiger zeigt immer auf das linke obere Byte in den gesperrten Unterregionen.

Wenn Sie mit Index-und Vertexpuffern arbeiten, können Sie mehrere Sperr Aufrufe durchführen. Sie müssen jedoch sicherstellen, dass die Anzahl der Sperr Aufrufe mit der Anzahl der entsperrungs Aufrufe übereinstimmt.

DXTn speichert Pixel in codierten 4 x 4-Blöcken und kann nur für 4 x 4-Grenzen gesperrt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Ressourcen](direct3d-resources.md)
</dt> </dl>

 

 



