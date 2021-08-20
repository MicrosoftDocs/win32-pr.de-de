---
description: Mit dem lokalen Threadspeicher (THREAD Local Storage, TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mithilfe eines globalen Indexes zugreifen kann. Ein Thread ordnet den Index zu, der von den anderen Threads verwendet werden kann, um die eindeutigen Daten abzurufen, die dem Index zugeordnet sind.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Threadlokaler Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a32c1630fb5690fc3ade4d319e7787c5287b27c270a9b43e3825e547e68bd4c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792999"
---
# <a name="thread-local-storage"></a>Threadlokaler Speicher

Alle Threads eines Prozesses teilen sich dessen virtuellen Adressraum. Die lokalen Variablen einer Funktion sind für jeden Thread, der die Funktion ausgeführt, eindeutig. Die statischen und globalen Variablen werden jedoch von allen Threads im Prozess gemeinsam genutzt. Mit *dem lokalen Threadspeicher* (THREAD Local Storage, TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mithilfe eines globalen Indexes zugreifen kann. Ein Thread ordnet den Index zu, der von den anderen Threads verwendet werden kann, um die eindeutigen Daten abzurufen, die dem Index zugeordnet sind.

Die Konstante TLS \_ MINIMUM AVAILABLE definiert die \_ Mindestanzahl von TLS-Indizes, die in jedem Prozess verfügbar sind. Dieser Mindestwert beträgt für alle Systeme garantiert mindestens 64. Die maximale Anzahl von Indizes pro Prozess beträgt 1.088.

Wenn die Threads erstellt werden, ordnet das System ein Array von **LPVOID-Werten** für TLS zu, die mit NULL initialisiert werden. Bevor ein Index verwendet werden kann, muss er von einem der Threads zugeordnet werden. Jeder Thread speichert seine Daten für einen TLS-Index in einem *TLS-Slot* im Array. Wenn die einem Index zugeordneten Daten in einen **LPVOID-Wert** passen, können Sie die Daten direkt im TLS-Slot speichern. Wenn Sie jedoch eine große Anzahl von Indizes auf diese Weise verwenden, ist es besser, separaten Speicher zu reservieren, die Daten zu konsolidieren und die Anzahl der verwendeten TLS-Slots zu minimieren.

Das folgende Diagramm veranschaulicht die Funktionsweise von TLS. Ein Codebeispiel zur Veranschaulichung der Verwendung des lokalen Threadspeichers finden Sie unter [Using Thread Local Storage](using-thread-local-storage.md).

![Diagramm, das die Funktionsweise des T L S-Prozesses zeigt.](images/tls.png)

Der Prozess verfügt über zwei Threads: Thread 1 und Thread 2. Es ordnet zwei Indizes für die Verwendung mit TLS zu: gdwTlsIndex1 und gdwTlsIndex2. Jeder Thread weist zwei Speicherblöcke zu (einen für jeden Index), in dem die Daten gespeichert werden, und speichert die Zeiger auf diese Speicherblöcke in den entsprechenden TLS-Slots. Um auf die einem Index zugeordneten Daten zu zugreifen, ruft der Thread den Zeiger auf den Speicherblock aus dem TLS-Slot ab und speichert ihn in der lokalen lpvData-Variablen.

Es ist ideal, TLS in einer Dynamic Link Library (DLL) zu verwenden. Ein Beispiel finden Sie unter [Verwenden von thread lokalen Storage in einer Dynamic Link Library.](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Thread Local Storage (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Verwenden von TLS (threadlokaler Speicher)](using-thread-local-storage.md)
</dt> <dt>

[Verwenden von thread lokalen Storage in einer Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
