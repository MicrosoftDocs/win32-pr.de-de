---
description: Mit dem lokalen Thread Speicher (Thread Local Storage, TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mit einem globalen Index zugreifen kann. Ein Thread ordnet den Index zu, der von den anderen Threads zum Abrufen der eindeutigen Daten, die dem Index zugeordnet sind, verwendet werden kann.
ms.assetid: 40df7410-64d6-4edd-8009-d9c3d2aca920
title: Threadlokaler Speicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17d2ff7a1ff253ce5a20b3921cc9605bf2989f6
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/03/2021
ms.locfileid: "104565862"
---
# <a name="thread-local-storage"></a>Threadlokaler Speicher

Alle Threads eines Prozesses teilen sich dessen virtuellen Adressraum. Die lokalen Variablen einer Funktion sind für jeden Thread, der die Funktion ausführt, eindeutig. Die statischen und globalen Variablen werden jedoch von allen Threads im Prozess gemeinsam genutzt. Mit dem *lokalen Thread Speicher (Thread Local Storage* , TLS) können Sie eindeutige Daten für jeden Thread bereitstellen, auf den der Prozess mit einem globalen Index zugreifen kann. Ein Thread ordnet den Index zu, der von den anderen Threads zum Abrufen der eindeutigen Daten, die dem Index zugeordnet sind, verwendet werden kann.

Der verfügbare Konstante TLS- \_ Wert \_ definiert die Mindestanzahl von TLS-Indizes, die in jedem Prozess verfügbar sind. Dieser Minimalwert ist garantiert mindestens 64 für alle Systeme. Die maximale Anzahl von Indizes pro Prozess ist 1.088.

Wenn die Threads erstellt werden, ordnet das System ein Array von **LPVOID** -Werten für TLS zu, die mit NULL initialisiert werden. Bevor ein Index verwendet werden kann, muss er von einem der Threads zugeordnet werden. Jeder Thread speichert seine Daten für einen TLS-Index in einem *TLS-Slot* im Array. Wenn die einem Index zugeordneten Daten in einen **LPVOID** -Wert passen, können Sie die Daten direkt im TLS-Slot speichern. Wenn Sie jedoch eine große Anzahl von Indizes auf diese Weise verwenden, ist es besser, separaten Speicher zuzuordnen, die Daten zu konsolidieren und die Anzahl der verwendeten TLS-Slots zu minimieren.

Das folgende Diagramm veranschaulicht die Funktionsweise von TLS. Ein Codebeispiel zur Veranschaulichung der Verwendung von lokalem Thread Speicher finden [Sie unter Verwenden von lokalem Thread Speicher](using-thread-local-storage.md).

![Diagramm, das zeigt, wie der T L S-Prozess funktioniert.](images/tls.png)

Der Prozess verfügt über zwei Threads: Thread 1 und Thread 2. Es ordnet zwei Indizes für die Verwendung mit TLS, gdwTlsIndex1 und gdwTlsIndex2 zu. Jeder Thread ordnet zwei Speicherblöcke (einen für jeden Index) zu, in denen die Daten gespeichert werden, und speichert die Zeiger auf diese Speicherblöcke in den entsprechenden TLS-Slots. Um auf die mit einem Index verknüpften Daten zuzugreifen, ruft der Thread den Zeiger auf den Speicherblock aus dem TLS-Slot ab und speichert ihn in der lokalen lpvdata-Variablen.

Es ist ideal, TLS in einer Dynamic Link Library (dll) zu verwenden. Ein Beispiel finden Sie unter [Verwenden von lokalem Thread Speicher in einer Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Lokaler Thread Speicher (Visual C++)](/cpp/parallel/thread-local-storage-tls?view=vs-2019)
</dt> <dt>

[Verwenden von TLS (threadlokaler Speicher)](using-thread-local-storage.md)
</dt> <dt>

[Verwenden des lokalen Thread Speichers in einer Dynamic Link Library](../dlls/using-thread-local-storage-in-a-dynamic-link-library.md)
</dt> </dl>

 

 
