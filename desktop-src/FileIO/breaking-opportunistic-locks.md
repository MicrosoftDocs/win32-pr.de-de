---
description: Die Unterbrechung einer opportunistischen Sperre ist der Prozess der Herabwürdigung der Sperre, die ein Client in einer Datei hat, damit ein anderer Client die Datei mit oder ohne opportunistische Sperre öffnen kann.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Unterbrechen opportunistischer Sperren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a29b6bd36d8c000b5288ea2408897415547c802
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363368"
---
# <a name="breaking-opportunistic-locks"></a>Unterbrechen opportunistischer Sperren

Die Unterbrechung einer opportunistischen Sperre ist der Prozess der Herabwürdigung der Sperre, die ein Client in einer Datei hat, damit ein anderer Client die Datei mit oder ohne opportunistische Sperre öffnen kann. Wenn der andere Client den Öffnungsvorgang anfordert, verzögert der Server den Öffnungsvorgang und benachrichtigt den Client, der die opportunistische Sperre aufrecht erhält.

Der Client, der die Sperre hält, führt dann Aktionen aus, die für den Sperrentyp geeignet sind, z. b. auslassen von Lese Puffern, Schließen der Datei usw. Nur wenn der Server, der die opportunistische Sperre aufrecht erhält, den Server benachrichtigt, dass er abgeschlossen ist, öffnet der Server die Datei für den Client, der den Öffnungsvorgang anfordert. Wenn jedoch eine Sperre der Ebene 2 getrennt ist, meldet der Server dem Client, dass er beschädigt wurde, jedoch nicht auf eine Bestätigung wartet, da keine zwischengespeicherten Daten auf den Server geleert werden müssen.

Wenn Sie eine Unterbrechung einer exklusiven Sperre (Filter, Ebene 1 oder Batch) bestätigen, kann der Inhaber einer gesperrten Sperre keine weitere exklusive Sperre anfordern. Eine exklusive Sperre kann auf eine Sperre der Ebene 2 oder gar keine Sperre herabgestuft werden. Der Halter gibt in der Regel die Sperre frei und schließt die Datei, wenn die Datei trotzdem geschlossen wird.

Anwendungen werden benachrichtigt, dass eine opportunistische Sperre durch die Verwendung des **hevent** -Members der [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp enden Struktur, die der Datei zugeordnet ist, in der die Sperre beschädigt ist, getrennt wird. Anwendungen können auch Funktionen wie [**gedeverlappedresult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) und [**hasoverlappedioabgeschlossene**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)verwenden.

 

 
