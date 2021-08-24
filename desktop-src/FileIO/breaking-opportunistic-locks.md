---
description: Das Brechen einer deterministischen Sperre ist der Prozess, bei dem die Sperre eines Clients für eine Datei herabgestuft wird, sodass ein anderer Client die Datei mit oder ohne eine deterministische Sperre öffnen kann.
ms.assetid: 0356c167-2973-4820-85a9-bc14abcbf163
title: Breaking Deterministic Locks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b797feed06c5f02f1b87ff4e05e2d82d44a34f0efe86d7a0881ec1d722023f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582600"
---
# <a name="breaking-opportunistic-locks"></a>Breaking Deterministic Locks

Das Brechen einer deterministischen Sperre ist der Prozess, bei dem die Sperre eines Clients für eine Datei herabgestuft wird, sodass ein anderer Client die Datei mit oder ohne eine deterministische Sperre öffnen kann. Wenn der andere Client den Open-Vorgang an fordert, verzögert der Server den Öffnen-Vorgang und benachrichtigt den Client, der die Sperre hält.

Der Client, der die Sperre hält, führt dann aktionen aus, die für den Typ der Sperre geeignet sind, z. B. das Verabbruch von Lesepuffern, das Schließen der Datei und so weiter. Nur wenn der Client, der die Sperre enthält, den Server benachrichtigt, dass dies erfolgt ist, öffnet der Server die Datei für den Client, der den Öffnen-Vorgang an fordert. Wenn jedoch eine Sperre der Ebene 2 unterbrochen wird, meldet der Server dem Client, dass sie verletzt wurde, wartet aber nicht auf eine Bestätigung, da keine zwischengespeicherten Daten auf den Server geleert werden.

Durch die Bestätigung einer Unterbrechung einer exklusiven Sperre (Filter, Ebene 1 oder Batch) kann der Besitzer einer unterbrochenen Sperre keine weitere exklusive Sperre anfordern. Eine exklusive Sperre kann auf eine Sperre der Ebene 2 oder gar keine Sperre herabgestuft werden. Der Halter gibt in der Regel die Sperre frei und schließt die Datei, wenn die Datei trotzdem geschlossen werden soll.

Anwendungen werden mithilfe des **hEvent-Members** der [**OVERLAPPED-Struktur,**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) die der Datei zugeordnet ist, für die die Sperre unterbrochen wird, benachrichtigt, dass eine Sperre unterbrochen wird. Anwendungen können auch Funktionen wie [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) und [**HasOverlappedIoCompleted verwenden.**](/windows/desktop/api/winbase/nf-winbase-hasoverlappediocompleted)

 

 
