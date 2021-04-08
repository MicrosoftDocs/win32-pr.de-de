---
description: Jeder neue Thread oder diese Fiber erhält einen eigenen Stapelbereich, der aus reserviertem und anfänglich zugespeichertem Arbeitsspeicher besteht.
ms.assetid: abb2d5c1-040b-4c36-aae5-3517b6a8c540
title: Thread Stapelgröße
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4204e0bffa13fb43b6ea9520b60c0505372bad6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959923"
---
# <a name="thread-stack-size"></a>Thread Stapelgröße

Jeder neue Thread oder diese Fiber erhält einen eigenen Stapelbereich, der aus reserviertem und anfänglich zugespeichertem Arbeitsspeicher besteht. Die reservierte Arbeitsspeicher Größe stellt die gesamte Stapel Zuordnung im virtuellen Arbeitsspeicher dar. Daher ist die reservierte Größe auf den virtuellen Adressbereich beschränkt. Die anfänglich zugesicherte Seiten verbrauchen keinen physischen Speicher, bis auf Sie verwiesen wird. Allerdings entfernen Sie Seiten aus dem gesamten commitlimit des Systems, d. h. die Größe der Auslagerungs Datei zuzüglich der Größe des physischen Speichers. Das System führt einen Commit für zusätzliche Seiten aus dem reservierten Stapel Speicher aus, wenn Sie benötigt werden, bis der Stapel die reservierte Größe minus eine Seite erreicht (die als Wächter Seite verwendet wird, um Stapelüberlauf zu verhindern) oder das System so wenig Arbeitsspeicher hat, dass der Vorgang nicht ausgeführt werden kann.

Es empfiehlt sich, möglichst wenig Stapelgröße auszuwählen und den Stapel zu commitden, der für die zuverlässige Ausführung des Threads oder der Fiber benötigt wird. Jede Seite, die für den Stapel reserviert ist, kann nicht für andere Zwecke verwendet werden.

Ein Stapel wird freigegeben, wenn der Thread beendet wird. Er wird nicht freigegeben, wenn der Thread von einem anderen Thread beendet wird.

Die Standardgröße für den reservierten und anfänglich zugesicherte Stapel Speicher wird im Header der ausführbaren Datei angegeben. Die Thread-oder Fiber Erstellung schlägt fehl, wenn nicht genügend Arbeitsspeicher zur Reservierung oder zum Commit der Anzahl der angeforderten Bytes vorhanden ist. Die vom Linker verwendete standardmäßige Stapel Reservierungs Größe beträgt 1 MB. Um eine andere standardmäßige Stapel Reservierungs Größe für alle Threads und Fibers anzugeben, verwenden Sie die STACKSIZE-Anweisung in der Modul Definitionsdatei (. def). Das Betriebssystem rundet die angegebene Größe auf das nächste Vielfache der Zuordnungs Granularität des Systems (in der Regel 64 KB) ab. Um die Zuordnungs Granularität des aktuellen Systems abzurufen, verwenden Sie die [**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo) -Funktion.

Verwenden Sie den *dwstacksize* -Parameter der Funktion " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread)", " [**forateremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)" oder " [**foratefiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) ", um den anfänglich zugegebenen Stapel Speicher zu ändern. Dieser Wert wird auf die nächste Seite aufgerundet. Im Allgemeinen ist die Reserve Größe die Standard Reserve Größe, die im Header der ausführbaren Datei angegeben ist. Wenn jedoch die von *dwstacksize* angegebene anfängliche Zugesicherte Größe größer oder gleich der Standard Reserve Größe ist, wird diese neue Commitgröße auf das nächste Vielfache von 1 MB aufgerundet.

Legen Sie zum Ändern der reservierten Stapelgröße den *dwupationflags* -Parameter von " [**foratethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) " oder " [**forateremotethread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread) " auf "Stack \_ size \_ Param" \_ ist \_ eine Reservierung fest, \_ und verwenden Sie den Parameter " *dwstacksize* ". In diesem Fall ist die anfängliche Zugesicherte Größe die im ausführbaren Header angegebene Standardgröße. Verwenden Sie für Fibers den *dwstackreservesize* -Parameter von " [**kreatefiberex**](/windows/desktop/api/WinBase/nf-winbase-createfiberex)". Die Zugesicherte Größe wird im *dwstackcommitsize* -Parameter angegeben.

Die [**setthreadstackguarantee**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadstackguarantee) -Funktion legt die minimale Größe des Stapels fest, der dem aufrufenden Thread oder der Fiber zugeordnet ist, der während der Stapelüberlauf Ausnahmen verfügbar sein wird.

 

 
