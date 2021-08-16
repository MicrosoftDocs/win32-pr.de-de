---
title: Direct2D-Multithread-Apps
description: Beschreibt bewährte Methoden zum Erstellen von Multithread-Direct2D-Apps.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5710435f263e7b0f735581e03416f1d01733711429ad95b3ed25e473aca6d936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636420"
---
# <a name="multithreaded-direct2d-apps"></a>Direct2D-Multithread-Apps

Wenn Sie [Direct2D-Apps](./direct2d-portal.md) entwickeln, müssen Sie möglicherweise von mehreren Threads aus auf Direct2D-Ressourcen zugreifen. In anderen Fällen können Sie Multithreading verwenden, um eine bessere Leistung oder Reaktionsfähigkeit zu erzielen (z. B. die Verwendung eines Threads für die Bildschirmanzeige und eines separaten Threads für das Offlinerendering).

In diesem Thema werden die bewährten Methoden für die Entwicklung von [Multithread-Direct2D-Apps](./direct2d-portal.md) mit wenig bis gar keinem [Direct3D-Rendering](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) beschrieben. Softwarefehler, die durch Parallelitätsprobleme verursacht werden, können schwierig nachverfolgt werden, und es ist hilfreich, Ihre Multithreadingrichtlinie zu planen und die hier beschriebenen bewährten Methoden zu befolgen.

> [!Note]  
> Wenn Sie auf zwei [Direct2D-Ressourcen](./direct2d-portal.md) zugreifen, die aus zwei verschiedenen Singlethread-Direct2D-Factorys erstellt wurden, führt dies nicht zu Zugriffskonflikten, solange die zugrunde liegenden [Direct3D-Geräte](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) und Gerätekontexte ebenfalls unterschiedlich sind. Wenn in diesem Artikel von "Zugriff auf Direct2D-Ressourcen" gesprochen wird, bedeutet dies tatsächlich "Zugriff auf Direct2D-Ressourcen, die vom gleichen Direct2D-Gerät erstellt wurden", sofern nicht anders angegeben.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Entwickeln Thread-Safe Apps, die nur Direct2D-APIs aufrufen

Sie können eine [Multithread-Direct2D-Factoryinstanz](./direct2d-portal.md) erstellen. Sie können eine Multithreadfactory und alle zugehörigen Ressourcen aus mehr als einem Thread verwenden und freigeben. Der Zugriff auf diese Ressourcen (über Direct2D-Aufrufe) wird jedoch von Direct2D serialisiert, sodass keine Zugriffskonflikte auftreten. Wenn Ihre App nur Direct2D-APIs aufruft, erfolgt dieser Schutz automatisch durch Direct2D auf einer präzisen Ebene mit minimalem Mehraufwand. Der Code zum Erstellen einer Multithreadfactory hier.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

Die Abbildung hier zeigt, wie [Direct2D](./direct2d-portal.md) zwei Threads serialisiert, die Aufrufe nur mithilfe der Direct2D-API durchführen.

![Diagramm von zwei serialisierten Threads.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Entwickeln Thread-Safe Direct2D-Apps mit minimalen Direct3D- oder DXGI-Aufrufen

Es ist häufiger, dass eine [Direct2D-App](./direct2d-portal.md) auch einige [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe vornimmt. Beispielsweise wird ein Anzeigethread in Direct2D gezeichnet und dann mithilfe einer [**DXGI-Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)dargestellt.

In diesem Fall ist die Threadsicherheit komplizierter: Einige [Direct2D-Aufrufe](./direct2d-portal.md) greifen indirekt auf die zugrunde liegenden [Direct3D-Ressourcen](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) zu, auf die möglicherweise gleichzeitig von einem anderen Thread zugegriffen wird, der Direct3D oder DXGI aufruft. Da diese Direct3D- oder DXGI-Aufrufe nicht von Direct2D bekannt und gesteuert werden, müssen Sie eine Multithread-Direct2D-Factory erstellen, aber Sie müssen versuchen, Zugriffskonflikte zu vermeiden.

Das folgende Diagramm zeigt einen Direct3D-Ressourcenzugriffskonflikt, weil thread T0 indirekt über einen [Direct2D-Aufruf](./direct2d-portal.md) auf eine Ressource zugreift und T2 direkt über einen Direct3D- oder DXGI-Aufruf auf die gleiche Ressource zugreift. [](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11)

> [!Note]  
> Der Threadschutz, den [Direct2D](./direct2d-portal.md) bereitstellt (die blaue Sperre in diesem Bild), ist in diesem Fall nicht hilfreich.

 

![Threadschutzdiagramm.](images/multi-thread2.png)

Zur Vermeidung von Ressourcenzugriffskonflikten empfiehlt es sich, explizit die Sperre zu erhalten, die [Direct2D](./direct2d-portal.md) für die interne Zugriffssynchronisierung verwendet, und diese Sperre anzuwenden, wenn ein Thread [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe ausführen muss, die zu Zugriffskonflikten führen können, wie hier gezeigt. Insbesondere sollten Sie bei Code, der Ausnahmen oder ein Early Out-System verwendet, das auf HRESULT-Rückgabecodes basiert, besondere Vorsicht walten lassen. Aus diesem Grund wird empfohlen, ein RAII-Muster (Resource Acquisition Is Initialization) zu verwenden, um die [**Enter-**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) und [**Leave-Methoden**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) aufzurufen.

> [!Note]  
> Es ist wichtig, dass Sie Aufrufe der [**Enter-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) und der [**Leave-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) koppeln, da andernfalls ihre App zu Deadlocks führen kann.

 

Der Code hier zeigt ein Beispiel dafür, wann [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe gesperrt und anschließend entsperrt werden müssen.


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> Einige [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe (insbesondere [**IDXGISwapChain::P resent)**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)können Sperren abrufen und/oder Rückrufe im Code der aufrufenden Funktion oder Methode auslösen. Dies sollten Sie beachten und sicherstellen, dass ein solches Verhalten keine Deadlocks verursacht. Weitere Informationen finden Sie im Thema [DXGI Overview](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![Diagramm zur Threadsperrung direct2d und direct3d.](images/multi-thread3.png)

Wenn Sie die [**Enter-**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) und [**Leave-Methoden**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) verwenden, werden die Aufrufe durch die automatische [Direct2D-Sperre](./direct2d-portal.md) und die explizite Sperre geschützt, sodass für die App kein Zugriffskonflikt vorkommt.

Es gibt andere Ansätze, um dieses Problem zu umgehen. Es wird jedoch empfohlen, [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe explizit mit der [Direct2D-Sperre](./direct2d-portal.md) zu schützen, da sie in der Regel eine bessere Leistung bietet, da die Parallelität auf einer viel feineren Ebene und mit geringerem Mehraufwand unter der Abdeckung von Direct2D geschützt wird.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Sicherstellen der Atomarität zustandsvoller Vorgänge

Threadsicherheitsfeatures von [DirectX](/previous-versions//ee663301(v=vs.85)) können zwar dazu beitragen, sicherzustellen, dass keine zwei einzelnen API-Aufrufe gleichzeitig erfolgen, Sie müssen aber auch sicherstellen, dass Threads, die zustandsbehaftete API-Aufrufe durchführen, nicht miteinander beeinträchtigen. Beispiel:

1.  Es gibt zwei Textzeilen, die Sie sowohl auf dem Bildschirm (von Thread 0) als auch außerhalb des Bildschirms (von Thread 1) rendern möchten: Zeile \# 1 ist "A ist größer" und Zeile \# 2 ist "als B", die beide mit einem soliden schwarzen Pinsel gezeichnet werden.
2.  Thread 1 zeichnet die erste Textzeile.
3.  Thread 0 reagiert auf eine Benutzereingabe, aktualisiert beide Textzeilen auf "B ist kleiner" bzw. "als A" und ändert die Pinselfarbe für seine eigene Zeichnung in Volltonrot.
4.  Thread 1 setzt das Zeichnen der zweiten Textzeile ( jetzt "als A" ) mit dem roten Farbpinsel fort.
5.  Schließlich erhalten wir zwei Textzeilen auf dem Zeichenziel außerhalb des Bildschirms: "A ist größer" in Schwarz und "als A" rot.

![Ein Diagramm von Ein- und Ausbildschirmthreads.](images/multi-thread4.png)

In der oberen Zeile zeichnet Thread 0 mit aktuellen Textzeichenfolgen und dem aktuellen schwarzen Pinsel. Thread 1 beendet nur das Zeichnen außerhalb des Bildschirms in der oberen Hälfte.

In der mittleren Zeile reagiert Thread 0 auf benutzerinteraktion, aktualisiert die Textzeichenfolgen und den Pinsel und aktualisiert dann den Bildschirm. An diesem Punkt wird Thread 1 blockiert. In der unteren Zeile setzt das endgültige Rendering außerhalb des Bildschirms nach Thread 1 das Zeichnen der unteren Hälfte mit einem geänderten Pinsel und einer geänderten Textzeichenfolge fort.

Um dieses Problem zu beheben, empfiehlt es sich, für jeden Thread einen separaten Kontext zu haben, sodass Folgendes gilt:

-   Sie sollten eine Kopie des Gerätekontexts erstellen, damit veränderliche Ressourcen (d. h. Ressourcen, die während der Anzeige oder beim Drucken variieren können, z. B. Textinhalte oder der Volltonfarbpinsel im Beispiel) beim Rendern nicht geändert werden. In diesem Beispiel sollten Sie eine Kopie dieser beiden Textzeilen und den Farbpinsel beibehalten, bevor Sie zeichnen. Auf diese Weise garantieren Sie, dass jeder Thread über vollständigen und konsistenten Inhalt verfügt, der gezeichnet und dargestellt werden kann.
-   Sie sollten umfangreiche Ressourcen (z. B. Bitmaps und komplexe Effektdiagramme) gemeinsam nutzen, die einmal initialisiert und dann nicht threadübergreifend geändert werden, um die Leistung zu steigern.
-   Sie können entweder einfachen Ressourcen (z. B. Volltonfarbenpinsel und Textformate) freigeben, die einmal initialisiert und dann nicht threadübergreifend geändert werden.

## <a name="summary"></a>Zusammenfassung

Wenn Sie [Multithread-Direct2D-Apps](./direct2d-portal.md) entwickeln, müssen Sie eine Multithread-Direct2D-Factory erstellen und dann alle Direct2D-Ressourcen von dieser Factory ableiten. Wenn ein Thread [Direct3D-](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) oder DXGI-Aufrufe aufruft, müssen Sie auch explizit die Direct2D-Sperre anwenden, um diese Direct3D- oder DXGI-Aufrufe zu schützen. Darüber hinaus müssen Sie die Kontextintegrität sicherstellen, indem Sie eine Kopie von veränderlichen Ressourcen für jeden Thread erstellen.
