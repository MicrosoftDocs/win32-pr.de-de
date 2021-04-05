---
description: Eine Fiber ist eine Ausführungs Einheit, die manuell von der Anwendung geplant werden muss.
ms.assetid: 6283f56b-23ae-4840-abd0-2478a50c670c
title: STAP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0383e6d207a77c621f00f358c72bb8873ecb5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756559"
---
# <a name="fibers"></a>STAP

Eine *Fiber* ist eine Ausführungs Einheit, die manuell von der Anwendung geplant werden muss. Fibers werden im Kontext der Threads ausgeführt, die Sie planen. Jeder Thread kann mehrere Fibers planen. Im Allgemeinen bieten Fibers keine Vorteile gegenüber einer gut entworfenen Multithread-Anwendung. Die Verwendung von Fibers kann jedoch das Portieren von Anwendungen erleichtern, die zum Planen Ihrer eigenen Threads entworfen wurden.

Aus Sicht des Systems geht eine Fiber von der Identität des Threads aus, von dem Sie ausgeführt wird. Wenn eine Fiber z. b. auf den [lokalen Thread Speicher](thread-local-storage.md) (TLS) zugreift, greift Sie auf den lokalen Thread Speicher des Threads zu, auf dem Sie ausgeführt wird. Wenn außerdem eine Fiber die [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) -Funktion aufruft, wird der Thread, der ausgeführt wird, beendet. Eine Fiber verfügt jedoch nicht über die gleichen Zustandsinformationen wie die, die mit einem Thread verknüpft sind. Die einzigen Zustandsinformationen, die für eine Fiber aufbewahrt werden, sind der Stapel, eine Teilmenge der Register und die Fiber Daten, die während der Fiber Erstellung bereitgestellt werden. Die gespeicherten Register sind der Satz von Registern, der in der Regel über einen Funktionsbefehl hinweg beibehalten wird.

Fibers sind nicht voremptiv geplant. Sie können eine Fiber planen, indem Sie von einer anderen Fiber darauf wechseln. Das System plant nach wie vor die Durchführung von Threads. Wenn ein Thread, der Fibers ausgeführt wird, vorzeitig entfernt wird, wird seine derzeit ausgelaufende Fiber vorzeitig entfernt, bleibt aber erhalten. Die ausgewählte Fiber wird ausgeführt, wenn der Thread ausgeführt wird.

Bevor Sie die erste Fiber planen, rufen Sie die [**convertthreadesfiber**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) -Funktion auf, um einen Bereich zu erstellen, in dem die Fiber Zustandsinformationen gespeichert werden. Der aufrufende Thread ist nun die derzeit ausgeführte Fiber. Die gespeicherten Zustandsinformationen für diese Fiber enthalten die Fiber-Daten, die als Argument an **convertthreaddefiber** übermittelt werden.

Die Funktion "-Funktion" [**wird zum Erstellen**](/windows/desktop/api/WinBase/nf-winbase-createfiber) einer neuen Fiber aus einer vorhandenen Fiber verwendet. der-Befehl erfordert die Stapelgröße, die Startadresse und die Fiber-Daten. Die Startadresse ist in der Regel eine vom Benutzer bereitgestellte Funktion, die als Fiber Funktion bezeichnet wird, die einen Parameter annimmt (die Fiber Daten) und keinen Wert zurückgibt. Wenn Ihre Fiber Funktion zurückgibt, wird der Thread beendet, der die Fiber durchläuft. Um eine mit " **kreatefiber**" erstellte Fiber auszuführen, müssen Sie die [**switchtoken**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) -Funktion aufrufen. Sie können **switchdefiber** mit der Adresse einer Fiber aufzurufen, die von einem anderen Thread erstellt wurde. Zu diesem Zweck müssen Sie die Adresse an den anderen Thread zurückgegeben haben, wenn Sie " **kreatefiber** " aufgerufen hat, und Sie müssen die ordnungsgemäße Synchronisierung verwenden.

Eine Fiber kann die Fiber Daten abrufen, indem das [**getfiberdata**](/windows/win32/api/winnt/nf-winnt-getfiberdata) -Makro aufgerufen wird. Eine Fiber kann die Fiber Adresse jederzeit abrufen, indem das [**getcurrentfiber**](/windows/win32/api/winnt/nf-winnt-getcurrentfiber) -Makro aufgerufen wird.

## <a name="fiber-local-storage"></a>Fiber-lokaler Speicher

Eine Fiber kann *Fiber Local Storage* (FLS) verwenden, um eine eindeutige Kopie einer Variablen für jede Fiber zu erstellen. Wenn kein Fiber Wechsel erfolgt, verhält sich FLS genauso wie der [lokale Thread Speicher](thread-local-storage.md). Die FLS-Funktionen ([**flsalloc**](/windows/win32/api/fibersapi/nf-fibersapi-flsalloc), [**flsfree**](/windows/win32/api/fibersapi/nf-fibersapi-flsfree), [**flsgetvalue**](/windows/win32/api/fibersapi/nf-fibersapi-flsgetvalue)und [**flssetvalue**](/windows/win32/api/fibersapi/nf-fibersapi-flssetvalue)) bearbeiten die FLS, die dem aktuellen Thread zugeordnet sind. Wenn der Thread eine Fiber ausführt und die Fiber gewechselt wird, wird auch die FLS gewechselt.

Um die einer Fiber zugeordneten Daten zu bereinigen, müssen Sie die [**deletefiber**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) -Funktion aufrufen. Diese Daten umfassen den Stapel, eine Teilmenge der Register und die Fiber-Daten. Wenn die derzeit ausgelaufende Fiber **deletefiber** aufruft, ruft der zugehörige Thread [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) auf und wird beendet. Wenn die ausgewählte Fiber eines Threads jedoch durch eine Fiber gelöscht wird, die in einem anderen Thread ausgeführt wird, wird der Thread mit der gelöschten Fiber wahrscheinlich nicht ordnungsgemäß beendet, da der Fiber Stapel freigegeben wurde.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Fibers](using-fibers.md)
</dt> </dl>

 

 
