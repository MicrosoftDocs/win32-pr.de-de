---
description: Multiheadkarten sind Karten, die über einen gemeinsamen Framepuffer und -accelerator, unabhängige Digital-Analog-Konverter (DACs) und Monitorausgabe verfügen.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a74f51cea282618c9471eb9a63eedf8eef73c38b4d961209064261a93c4d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563515"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Multiheadkarten sind Karten, die über einen gemeinsamen Framepuffer und -accelerator, unabhängige Digital-Analog-Konverter (DACs) und Monitorausgabe verfügen. Solche Geräte können eine viel besser nutzbare Unterstützung mehrerer Monitore bieten als eine ähnliche Anzahl heterogener Grafikkarten.

Multiheadkarten werden in der API als einzelnes Gerät auf API-Ebene verfügbar gemacht, das mehrere Vollbild-Auslagerungsketten unterstützen kann. Folglich werden alle Ressourcen für alle Kopfköpfe freigegeben, und jeder Kopf hat genau die gleichen Funktionen. Jeder Kopf kann auf unabhängige Anzeigemodi festgelegt werden. Sie können separate Aufrufe von [**IDirect3DSwapChain9::P resent**](/windows/desktop/api) verwenden, um jeden Kopf zu aktualisieren. Sie können auch einen Aufruf von [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) verwenden, um jeden Kopf sequenziell zu aktualisieren.

> [!Note]  
> Die Aktualisierung jedes Haupts erfolgt nicht gleichzeitig mit einem einzigen Aufruf von [**IDirect3DDevice9::P resent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Aktuelle Statistiken in Direct3D 9Ex können die [**D3DPRESENTSTATS-Struktur**](d3dpresentstats.md) verwenden, um die Aktualisierungen an jedem Kopf nah beieinander zu halten, um Tränkeffekte über mehrere Adapterköpfe hinweg zu begrenzen. Informationen zum Synchronisieren von Frames von Direct3D 9Ex-Flip-Modellanwendungen finden Sie unter [Direct3D 9Ex Improvements](../direct3darticles/direct3d-9ex-improvements.md).

 

Jede Auslagerungskette für ein Multiheadgerät muss über Vollbildmodus sein. Wenn ein Gerät in den Multiheadmodus übertrat, muss es im Vollbildmodus bleiben. Der Übergang zurück in den Fenstermodus erfordert die Zerstörung des Geräts (mit Ausnahme des normalen ALT+TAB-To-Minimize-Vorgangs).

Die alte Methode, den Videospeicher zwischen den Kopf zu teilen und jeden Kopf als vollständig unabhängigen Beschleuniger zu behandeln, ist weiterhin ein gängiges Verwendungsszenario. Dieser Vorschlag ersetzt diesen Mechanismus nur, wenn die Anwendung speziell für die Funktion im Direct3D 9-Multiheadmodus codiert wurde.

Treiber erhalten ausreichende Kenntnisse, um zwischen den beiden Betriebsmodi zu wechseln.

Ein Kopf wird als Hauptkopf bezeichnet, und alle anderen Kopfköpfe auf derselben Karte werden als untergeordnete Kopfköpfe bezeichnet. Wenn mehr als ein Multiheadadapter in einem System vorhanden ist, werden der Master und seine untergeordneten Elemente von einem Multiheadadapter als Gruppe bezeichnet. Gruppen werden durch die Adapter-Ordnungszahl ihres Hauptkopfs bezeichnet.

Die [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) wurde aktualisiert, um die folgenden neuen Hardware-Caps verfügbar zu machen.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup ist 1 für herkömmliche Adapter und größer als 1 für den Masteradapter einer Multiheadkarte. Der Wert ist 0 (0) für einen untergeordneten Adapter einer Multiheadkarte. Jede Karte kann über mindestens einen Master verfügen, aber möglicherweise über viele untergeordnete Elemente.
-   MasterAdapterOrdinal gibt an, welches Gerät der Master für diesen untergeordneten Computer ist.
-   AdapterOrdinalInGroup gibt die Reihenfolge an, in der die API auf Kopfköpfe verweist. Der Masteradapter verfügt immer über AdapterOrdinalInGroup 0. Diese Werte entsprechen nicht den Adapter-Ordinalzahlen, die an die IDirect3D9-Methoden übergeben werden, sondern gelten nur für Kopfköpfe innerhalb einer Gruppe.

Diese Definition ermöglicht es Multiheadkarten, weiterhin mehrere Adapter wie in DirectX 8 als unabhängige Karten zu präsentieren.

Um ein Multiheadgerät zu erstellen, geben Sie das Verhaltenflag D3DCREATE \_ ADAPTERGROUP \_ DEVICE in [**IDirect3D9::CreateDevice an.**](/windows/desktop/api) Die Präsentationsparameter (ein Array von [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md)) sollten NumberOfAdaptersInGroup-Elemente enthalten. Die Runtime weist jedem Kopf jedes Element in numerischer Reihenfolge AdapterOrdinalInGroup zu. Wenn D3DCREATE \_ ADAPTERGROUP \_ DEVICE festgelegt ist, muss jeder Präsentationsparameter über:

-   Der Windowed-Member ist auf **FALSE** festgelegt (d. h. vollbildbild).
-   Der gleiche Wert für das EnableAutoDepthStencil-Member von [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md).

Wenn EnableAutoDepthStencil auf **TRUE** festgelegt ist, muss jedes der folgenden Felder für jeden [**D3DPRESENT-PARAMETER denselben Wert \_ haben:**](d3dpresent-parameters.md)

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Wenn DAC festgelegt ist, sind zusätzliche Aufrufe von [**IDirect3DDevice9::CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) ungültig.

Wenn das Gerät mit der DAC erstellt wurde, erwartet [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ein Array von [**D3DPRESENT PARAMETERS \_**](d3dpresent-parameters.md).

Jede an [**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) übergebene [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) muss vollbildbar sein. Um zurück in den Fenstermodus zu wechseln, muss die Anwendung das Gerät zerstören und ein Nicht-Multiheadgerät im Fenstermodus neu erstellen.

Hier ist ein einfaches Verwendungsszenario:


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



Weitere Informationen finden Sie unter [**IDirect3D9::CreateDevice**](/windows/desktop/api) und [**IDirect3DDevice9::GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmieren Tipps](programming-tips.md)
</dt> </dl>

 

 
