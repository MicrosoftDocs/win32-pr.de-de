---
title: Ressourcenlebensdauer und -synchronisierung
description: Um ein nicht definiertes Verhalten zu vermeiden, muss Ihre directml-Anwendung die Objekt Lebensdauer und Synchronisierung zwischen der CPU und der GPU ordnungsgemäß verwalten.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 6e8ab30c5c87c135ef3bdac0c1bc2a3d64040787
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103569"
---
# <a name="resource-lifetime-and-synchronization"></a>Ressourcenlebensdauer und -synchronisierung

Ebenso wie bei Direct3D 12 muss Ihre directml-Anwendung (um ein nicht definiertes Verhalten zu vermeiden) die Objekt Lebensdauer und die Synchronisierung zwischen der CPU und der GPU ordnungsgemäß verwalten. Directml folgt einem identischen Modell für die Ressourcen Lebensdauer wie Direct3D 12.

- Lebensdauer Abhängigkeiten zwischen zwei CPU-Objekten werden von directml mithilfe starker Verweis Zähler verwaltet. Ihre Anwendung muss die Abhängigkeiten der CPU-Lebensdauer nicht manuell verwalten. Beispielsweise enthält jedes untergeordnete Gerät einen starken Verweis auf das übergeordnete Gerät.
- Lebensdauer Abhängigkeiten zwischen GPU &mdash; -Objekten oder Abhängigkeiten, die über CPU und GPU spannen, werden &mdash; nicht automatisch verwaltet. Es ist Aufgabe Ihrer Anwendung, sicherzustellen, dass GPU-Ressourcen zumindest so lange aktiv sind, bis die gesamte Arbeit, die diese Ressource verwendet, die Ausführung auf der GPU abgeschlossen hat

## <a name="directml-devices"></a>Directml-Geräte

Das directml-Gerät ist ein Thread sicheres Zustands Loses Factoryobjekt. Jedes untergeordnete Gerät (siehe [**idmldevicechild**](/windows/desktop/api/directml/nn-directml-idmldevicechild)) enthält einen starken Verweis auf das übergeordnete directml-Gerät (siehe [**idmldevice**](/windows/desktop/api/directml/nn-directml-idmldevice)). Dies bedeutet, dass Sie die übergeordnete Geräteschnittstelle jederzeit von einer beliebigen untergeordneten Geräteschnittstelle abrufen können.

Ein directml-Gerät enthält seinerseits einen starken Verweis auf das Direct3D 12-Gerät, das verwendet wurde, um es zu erstellen (siehe [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device)und abgeleitete Schnittstellen).

Da das directml-Gerät zustandslos ist, ist es implizit Thread sicher. Sie können Methoden auf dem directml-Gerät gleichzeitig aus mehreren Threads abrufen, ohne dass eine externe Synchronisierung erforderlich ist.

Im Gegensatz zum Direct3D 12-Gerät ist das directml-Gerät jedoch kein Singleton-Objekt. Sie können beliebig viele directml-Geräte erstellen. Es ist jedoch möglich, dass Sie die untergeordneten Geräte, die zu verschiedenen Geräten gehören, nicht kombinieren. [**Idmlbindingtable**](/windows/desktop/api/directml/nn-directml-idmlbindingtable) und [**idmlcompiledoperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) sind z. b. zwei Arten von untergeordneten Geräten (beide Schnittstellen werden direkt oder indirekt von **idmldevicechild** abgeleitet). Und Sie dürfen keine Bindungs Tabelle (**idmlbindingtable**) verwenden, um eine Bindung für einen Operator (**idmlcompiledoperator**) herzustellen, wenn der Operator und die Bindungs Tabelle zu unterschiedlichen directml-Geräte Instanzen gehören.

Da es sich bei dem directml-Gerät nicht um ein Singleton handelt, erfolgt die Geräte Entfernung auf Gerätebasis und nicht als Prozess weites Ereignis, da es sich um ein Direct3D 12-Gerät handelt. Weitere Informationen finden Sie unter [Behandeln von Fehlern und Entfernen von Geräten in der directml](dml-errors.md).

## <a name="lifetime-requirements-of-gpu-resources"></a>Lebensdauer Anforderungen von GPU-Ressourcen

Wie bei Direct3D 12 wird die directml nicht automatisch zwischen CPU und GPU synchronisiert. Außerdem werden Ressourcen nicht automatisch aktiv, während Sie von der GPU verwendet werden. Stattdessen sind dies Zuständigkeiten ihrer Anwendung.

Wenn Sie eine Befehlsliste ausführen, die directml-Verteiler enthält, muss Ihre Anwendung sicherstellen, dass GPU-Ressourcen aktiv bleiben, bis die gesamte Arbeit, die diese Ressourcen verwendet, die Ausführung auf der GPU abgeschlossen hat.

Im Fall von [**idmlcommandrecorder:: recorddispatch**](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) für einen directml-Operator, der die folgenden Objekte enthält.

- Der ausgeführte [**idmlcompiledoperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator) (oder [**idmloperatorinitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer) , wenn die Operator Initialisierung durchgeführt wird).
- Der **idmlcompiledoperator** , der die Bindungs Tabelle unterstützt, die zum Binden des Operators verwendet wird.
- Die [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) -Objekte, die als Eingaben/Ausgaben des Operators gebunden sind.
- Die **ID3D12Resource** -Objekte, die ggf. als persistente und temporäre Ressourcen gebunden sind.
- Der [**ID3D12CommandAllocator**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandallocator) , der die Befehlsliste selbst unterstützt.

Nicht alle directml-Schnittstellen stellen GPU-Ressourcen dar. Beispielsweise muss eine Bindungs Tabelle *nicht* aufrechterhalten werden, bis alle mit ihr verwendeten Verteiler die Ausführung auf der GPU abgeschlossen haben. Das liegt daran, dass die Bindungs Tabelle selbst keine GPU-Ressourcen besitzt. Stattdessen wird vom deskriptorheap verwendet. Daher ist der zugrunde liegende *deskriptorheap* das Objekt, das beibehalten werden muss, bis die Ausführung abgeschlossen ist, und nicht die Bindungs Tabelle selbst.

In Direct3D 12 ist ein ähnliches Konzept vorhanden. Ein Befehls *Zuweiser* muss aktiv bleiben, bis alle Ausführungen, die ihn verwenden, auf der GPU abgeschlossen sind. Da es den GPU-Speicher besitzt. Aber eine Befehls *Liste* besitzt keinen GPU-Speicher, daher kann Sie zurückgesetzt oder freigegeben werden, sobald Sie zur Ausführung übermittelt wurde.

In directml müssen kompilierte Operatoren ([**idmlcompiledoperator**](/windows/desktop/api/directml/nn-directml-idmlcompiledoperator)) und Operator Initialisierer ([**idmloperatorinitializer**](/windows/desktop/api/directml/nn-directml-idmloperatorinitializer)) beide GPU-Ressourcen direkt verwenden, sodass Sie aktiv bleiben, bis alle Verteiler, die Sie verwenden, die Ausführung auf der GPU abgeschlossen haben. Außerdem müssen alle verwendeten Direct3D 12-Ressourcen (Befehls Zuweisungen, deskriptorheaps, Puffer, als Beispiele) auf ähnliche Weise von Ihrer Anwendung aufrechterhalten werden.

Wenn Sie ein Objekt vorzeitig freigegeben haben, während es noch von der GPU verwendet wird, ist das Ergebnis nicht definiertes Verhalten, das möglicherweise zum Entfernen von Geräten oder anderen Fehlern führt.

## <a name="cpu-and-gpu-synchronization"></a>CPU-und GPU-Synchronisierung

Directml sendet keinerlei Arbeit für die Ausführung auf der GPU. Stattdessen *zeichnet* die [ **idmlcommandrecorder:: recorddispatch** -Methode](/windows/desktop/api/directml/nf-directml-idmlcommandrecorder-recorddispatch) die Verteilung der in einer Befehlsliste zur späteren Ausführung auf. Die Anwendung muss dann die Befehlsliste für die Ausführung schließen und übermitteln, indem [**ID3D12CommandQueue:: executecommandlists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)aufgerufen wird, wie bei jeder Direct3D 12-Befehlsliste.

Da directml selbst keine Arbeit für die Ausführung auf der GPU absendet, werden auch keine Zäune erstellt, und es wird keine Form der CPU/GPU-Synchronisierung in Ihrem Namen ausgeführt. Es liegt in der Verantwortung der Anwendung, die entsprechenden Direct3D 12-primitiven zu verwenden, um auf den Abschluss der übermittelten Arbeit auf der GPU zu warten, falls erforderlich. Weitere Informationen finden Sie unter [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) und [**ID3D12CommandQueue:: Signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal).

## <a name="see-also"></a>Siehe auch

* [Ausführen und Synchronisieren von Befehlslisten](/windows/desktop/direct3d12/executing-and-synchronizing-command-lists)
* [Behandeln von Fehlern und Entfernen von Geräten in der directml](dml-errors.md)