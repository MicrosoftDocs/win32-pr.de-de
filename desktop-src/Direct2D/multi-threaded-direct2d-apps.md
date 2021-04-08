---
title: Direct2D-Multithread-Apps
description: Beschreibt bewährte Methoden zum Erstellen von Multithread Direct2D-apps.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/03/2020
ms.locfileid: "103734792"
---
# <a name="multithreaded-direct2d-apps"></a>Direct2D-Multithread-Apps

Wenn Sie [Direct2D](./direct2d-portal.md) -apps entwickeln, müssen Sie möglicherweise über mehr als einen Thread auf Direct2D-Ressourcen zugreifen. In anderen Fällen empfiehlt es sich, Multithreading zu verwenden, um eine bessere Leistung oder bessere Reaktionsfähigkeit zu erzielen (z. b. die Verwendung eines Threads für die Bildschirm Anzeige und einen separaten Thread für das Offline Rendering).

In diesem Thema werden die bewährten Methoden zum Entwickeln von Multithread [Direct2D](./direct2d-portal.md) -apps mit nur wenig oder ohne [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) Rendering beschrieben. Software Fehler, die durch Parallelitäts Probleme verursacht werden, können schwer zu finden sein, und es ist hilfreich, die Multithreading Richtlinie zu planen und die hier beschriebenen bewährten Methoden zu befolgen.

> [!Note]  
> Wenn Sie auf zwei [Direct2D](./direct2d-portal.md) -Ressourcen zugreifen, die aus zwei unterschiedlichen Single Thread Direct2D Factorys erstellt wurden, verursacht dies keine Zugriffs Konflikte, solange die zugrunde liegenden [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Geräte und-Geräte Kontexte ebenfalls verschieden sind. Wenn Sie über "Zugriff auf Direct2D-Ressourcen" in diesem Artikel sprechen, bedeutet dies, dass der Zugriff auf Direct2D-Ressourcen, die mit demselben Direct2D-Gerät erstellt wurden, nicht anders ist

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Entwickeln von Thread-Safe-apps, die nur Direct2D-APIs anrufen

Sie können eine Multithread [Direct2D](./direct2d-portal.md) Factory-Instanz erstellen. Sie können eine multithreadfactory und alle zugehörigen Ressourcen aus mehreren Threads verwenden und freigeben, aber der Zugriff auf diese Ressourcen (über Direct2D-Aufrufe) wird von Direct2D serialisiert, sodass keine Zugriffs Konflikte auftreten. Wenn in ihrer app nur Direct2D-APIs aufgerufen werden, erfolgt ein solcher Schutz automatisch durch Direct2D auf granularer Ebene mit minimalem Verwaltungsaufwand. Der Code zum Erstellen einer Multithread-Factory.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

Das folgende Bild zeigt, wie [Direct2D](./direct2d-portal.md) zwei Threads serialisiert, die Aufrufe nur mit der Direct2D-API durchführen.

![Diagramm der zwei serialisierten Threads.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Entwickeln von Thread-Safe Direct2D-apps mit minimalen Direct3D-oder DXGI-aufrufen

Es ist häufiger, dass eine [Direct2D](./direct2d-portal.md) -APP auch einige [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-Aufrufe ausführt. Ein Anzeige Thread zeichnet sich z. b. in Direct2D und ist dann mithilfe einer [**DXGI-Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)vorhanden.

In diesem Fall ist die Sicherstellung der Thread Sicherheit komplizierter: einige [Direct2D](./direct2d-portal.md) -Aufrufe greifen indirekt auf die zugrunde liegenden [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Ressourcen zu, die gleichzeitig von einem anderen Thread aufgerufen werden, der Direct3D oder DXGI aufruft. Da es sich bei diesen Direct3D-oder DXGI-Aufrufen nicht um renderingkonventionen Awareness und Control handelt, müssen Sie eine Multithread-Direct2D-Factory erstellen, aber Sie müssen mit Mor Vorgehen, um Zugriffs Konflikte zu vermeiden.

Das Diagramm zeigt einen [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Ressourcen Zugriffs Konflikt, weil Thread T0 indirekt über einen [Direct2D](./direct2d-portal.md) -Befehl auf eine Ressource zugreift und T2 direkt über einen Direct3D-oder DXGI-Befehl auf dieselbe Ressource zugreift.

> [!Note]  
> Der Thread Schutz, den [Direct2D](./direct2d-portal.md) bereitstellt (die blaue Sperre in diesem Bild) ist in diesem Fall nicht hilfreich.

 

![Thread Schutz Diagramm.](images/multi-thread2.png)

Um Ressourcen Zugriffs Konflikte zu vermeiden, wird empfohlen, dass Sie explizit die Sperre abrufen, die von [Direct2D](./direct2d-portal.md) für die interne Zugriffs Synchronisierung verwendet wird, und diese Sperre anwenden, wenn ein Thread [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-Aufrufe ausführen muss, die möglicherweise zu Zugriffs Konflikten führen, wie hier gezeigt. Insbesondere sollten Sie sich mit dem Code, der Ausnahmen verwendet, oder einem frühen System, das auf HRESULT-Rückgabecodes basiert, besonders Gedanken machen. Aus diesem Grund wird empfohlen, ein RAII (Resource Acquisition Is Initialization)-Muster zu verwenden, um die [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) -und [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) -Methoden aufzurufen.

> [!Note]  
> Es ist wichtig, dass Sie Aufrufe der [**Eingabe**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) -und der [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) -Methode kombinieren, da Ihre APP andernfalls einen Deadlock verursachen kann.

 

Der folgende Code zeigt ein Beispiel für das Sperren und anschließende Entsperren von [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-aufrufen.


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
> Einige [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-Aufrufe (insbesondere [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)) können Sperren und/oder Rückrufe in den Code der aufrufenden Funktion oder Methode abrufen. Sie sollten sich dies bewusst sein und sicherstellen, dass dieses Verhalten keine Deadlocks verursacht. Weitere Informationen finden Sie im Thema [Übersicht über DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![Direct2D-und Direct3D-Thread Sperr Diagramm.](images/multi-thread3.png)

Wenn Sie die [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) -und [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) -Methode verwenden, werden die Aufrufe durch die automatische [Direct2D](./direct2d-portal.md) und die explizite Sperre geschützt, sodass die APP keinen Zugriffs Konflikt verursacht.

Es gibt weitere Möglichkeiten, dieses Problem zu umgehen. Es wird jedoch empfohlen, [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-Aufrufe explizit mit der [Direct2D](./direct2d-portal.md) -Sperre zu schützen, da Sie in der Regel eine bessere Leistung bietet, da Sie Parallelität auf einer weitaus präzigerer Ebene und mit geringerem Aufwand unter renderingkonventionen Cover schützt.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Sicherstellen der Atomizität Zustands behafteter Vorgänge

Wenngleich die Thread Sicherheitsfeatures von [DirectX](/previous-versions//ee663301(v=vs.85)) dabei helfen können sicherzustellen, dass keine zwei einzelnen API-Aufrufe gleichzeitig ausgeführt werden, müssen Sie auch sicherstellen, dass Threads, die Zustands behaftete API-Aufrufe ausführen, nicht gegenseitig stören Beispiel:

1.  Es gibt zwei Textzeilen, die Sie sowohl auf dem Bildschirm (Thread 0) als auch auf dem Bildschirm (von Thread 1) renderierender darstellen möchten: Zeile \# 1 ist "A ist größer" und Zeile \# 2 ist "als B", die beide mit einem Pinsel mit Pinsel gezeichnet werden.
2.  Thread 1 zeichnet die erste Textzeile.
3.  Thread 0 reagiert auf eine Benutzereingabe, aktualisiert beide Textzeilen auf "B ist kleiner" bzw. "als ein" und hat die Pinsel Farbe für eine eigene Zeichnung in "rot" geändert.
4.  Thread 1 zeichnet die zweite Textzeile, die jetzt "als A" ist, mit dem roten Farbpinsel.
5.  Schließlich erhalten wir zwei Textzeilen auf dem Bildschirm für das Bildschirm Zeichen: "A ist größer" in schwarz und "als rot".

![ein Diagramm der on-und off-Bildschirm Threads.](images/multi-thread4.png)

In der obersten Zeile zeichnet Thread 0 mit aktuellen Text Zeichenfolgen und dem aktuellen schwarzen Pinsel. Thread 1 schließt die Bildschirm Zeichnung nur in der oberen Hälfte ab.

In der mittleren Zeile antwortet Thread 0 auf Benutzerinteraktion, aktualisiert die Text Zeichenfolgen und den Pinsel und aktualisiert dann den Bildschirm. An diesem Punkt wird Thread 1 blockiert. In der untersten Zeile setzt das abschließende Offscreen-Rendering nach Thread 1 das Zeichnen der unteren Hälfte mit einem geänderten Pinsel und einer geänderten Text Zeichenfolge fort.

Um dieses Problem zu beheben, wird empfohlen, dass Sie für jeden Thread einen separaten Kontext haben.

-   Sie sollten eine Kopie des Geräte Kontexts erstellen, damit änderbare Ressourcen (d. h. Ressourcen, die während des Anzeige-oder Druckvorgangs variieren können, z. b. Textinhalte oder der Pinsel mit voll Tonfarbe im Beispiel) beim Rendering nicht geändert werden. In diesem Beispiel sollten Sie vor dem Zeichnen eine Kopie der beiden Textzeilen und den Farbpinsel aufbewahren. Dadurch wird sichergestellt, dass jeder Thread über umfassende und konsistente Inhalte zum Zeichnen und präsentieren verfügt.
-   Sie sollten Ressourcen mit hohem Gewicht (z. b. Bitmaps und komplexe Effekte) freigeben, die einmal initialisiert und dann nie Thread übergreifend geändert werden, um die Leistung zu verbessern.
-   Sie können entweder einfache Ressourcen (z. b. Pinsel mit voll Tonfarbe und Textformate) freigeben, die einmal initialisiert und dann nie über mehrere Threads hinweg geändert werden.

## <a name="summary"></a>Zusammenfassung

Beim Entwickeln von Multithread [Direct2D](./direct2d-portal.md) -apps müssen Sie eine Multithread Direct2D Factory erstellen und dann alle Direct2D-Ressourcen von dieser Factory ableiten. Wenn ein Thread [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -oder DXGI-Aufrufe durchführt, müssen Sie die Direct2D-Sperre ebenfalls explizit abrufen, um diese Direct3D-oder DXGI-Aufrufe zu schützen. Außerdem müssen Sie die Kontext Integrität sicherstellen, indem Sie für jeden Thread eine Kopie der änderbaren Ressourcen besitzen.
