---
description: Multihead-Karten sind solche, die über einen gemeinsamen Frame Puffer und eine Zugriffstaste, unabhängige Digital-zu-Analog-Konverter (DACs) und Monitor Ausgaben verfügen.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multihead (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4617666ca623795d33bf1dafcaafeabe73323253
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481299"
---
# <a name="multihead-direct3d-9"></a>Multihead (Direct3D 9)

Multihead-Karten sind solche, die über einen gemeinsamen Frame Puffer und eine Zugriffstaste, unabhängige Digital-zu-Analog-Konverter (DACs) und Monitor Ausgaben verfügen. Diese Geräte können eine viel nützlichere Unterstützung für mehrere Monitore bieten als eine ähnliche Anzahl heterogener Anzeige Adapter.

Multihead-Karten sind in der API als einzelnes Gerät auf API-Ebene verfügbar, das mehrere voll Bildaustausch Ketten steuern kann. Folglich werden alle Ressourcen für alle Köpfe freigegeben, und jeder Head hat genau die gleichen Funktionen. Jeder Head kann auf unabhängige Anzeigemodi festgelegt werden. Sie können separate Aufrufe von [**IDirect3DSwapChain9::P Resent**](/windows/desktop/api) zum Aktualisieren der einzelnen Köpfe verwenden. Sie können auch einen [**:P IDirect3DDevice9**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) -aufrufbefehl verwenden, um die einzelnen Kopfzeile nacheinander zu aktualisieren.

> [!Note]  
> Die Aktualisierung der einzelnen Köpfe erfolgt nicht gleichzeitig mit einem einzelnen IDirect3DDevice9-Rückruf [**::P erneut gesendet**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Die aktuellen Statistiken in Direct3D 9Ex können die [**D3DPRESENTSTATS**](d3dpresentstats.md) -Struktur verwenden, um die Aktualisierungen auf den einzelnen Köpfen zu belassen, um die Auswirkungen auf mehrere Köpfe von Adaptern zu begrenzen. Informationen zum Synchronisieren von Frames von Direct3D 9Ex-Flip-Modell Anwendungen finden Sie unter [Direct3D 9Ex-Verbesserungen](../direct3darticles/direct3d-9ex-improvements.md).

 

Jede austauschkette für ein multiheadgerät muss voll Bildschirm sein. Wenn ein Gerät in den multiheadmodus gewechselt ist, muss es im Vollbildmodus bleiben. Bei der Umstellung auf den Fenstermodus muss das Gerät (außer dem normalen Alt + Tab-bis-minimieren-Vorgang) zerstört werden.

Die alte Methode zum Aufteilen von Videospeicher zwischen den Köpfen und die Behandlung der einzelnen Köpfe als vollständig unabhängige Zugriffstaste ist weiterhin ein häufiges Verwendungs Szenario. Dieser Mechanismus wird nicht durch diesen Vorschlag ersetzt, es sei denn, die Anwendung wurde speziell für die Funktionsweise im Direct3D 9-multiheadmodus programmiert.

Die Treiber verfügen über ausreichende Kenntnisse, um zwischen den beiden Betriebsmodi zu wechseln.

Eine Kopfzeile wird als Haupt Kopfzeile bezeichnet, und alle anderen Köpfe auf derselben Karte werden als untergeordnete Köpfe bezeichnet. Wenn mehr als ein multiheadadapter in einem System vorhanden ist, werden der Master und seine untergeordneten Elemente von einem Multihead-Adapter als Gruppe bezeichnet. Gruppen werden durch die Ordnungszahl des Adapters Ihrer Haupt Kopfzeile bezeichnet.

Die [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur wurde aktualisiert, um die folgenden neuen Hardware-Caps verfügbar zu machen.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   "Numofadaptersingroup" ist 1 für herkömmliche Adapter und größer als 1 für den Master Adapter einer Multihead-Karte. Der Wert ist 0 für einen untergeordneten Adapter einer Multihead-Karte. Jede Karte kann höchstens über einen Master verfügen, kann aber auch über viele untergeordnete Elemente verfügen.
-   Masteradapterordinal gibt an, welches Gerät der Master für diese untergeordnete ist.
-   Adapterordinalingroup gibt die Reihenfolge an, in der die Kopfzeilen von der API referenziert werden. Der Master Adapter hat immer adapterordinalingroup 0. Diese Werte entsprechen nicht den Adapter Ordinalzahlen, die an die IDirect3D9-Methoden übergebenen werden, sondern nur für Köpfe innerhalb einer Gruppe gelten.

Mit dieser Definition können Multihead-Karten weiterhin mehrere Adapter wie in DirectX 8 als unabhängige Karten darstellen.

Um ein multiheadgerät zu erstellen, geben Sie das verhaltenflag D3DCREATE \_ adaptergroup \_ Device in [**IDirect3D9:: kreatedevice**](/windows/desktop/api)an. Die Darstellungs Parameter (ein Array von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md)) sollten "numofadaptersingroup"-Elemente enthalten. Die Laufzeit weist jedes Element jedem Kopf in der numerischen adapterordinalingroup-Reihenfolge zu. Wenn das D3DCREATE \_ adaptergroup- \_ Gerät festgelegt ist, muss für jeden Präsentations Parameter Folgendes vorhanden sein:

-   Der Windowed-Member ist auf **false** festgelegt (mit anderen Worten: Vollbild).
-   Der gleiche Wert für den enableautodepthstencil-Member der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md).

Wenn enableautodepthstencil den Wert **true** hat, muss jedes der folgenden Felder für jeden [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md)denselben Wert aufweisen:

-   Autodepthstencilformat
-   BackBufferWidth
-   BackBufferHeight
-   Backbufferformat

Wenn die DAC festgelegt ist, sind zusätzliche Aufrufe an [**IDirect3DDevice9:: deateadditionalswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) unzulässig.

Wenn das Gerät mit der DAC erstellt wurde, erwartet [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) ein Array von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md).

Jede [**D3DPRESENT \_ Parameter**](d3dpresent-parameters.md) -Struktur, die an [**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) übermittelt wird, muss voll Bildschirm sein. Wenn Sie wieder in den Fenstermodus wechseln möchten, muss die Anwendung das Gerät zerstören und im Fenstermodus ein nicht-Multihead-Gerät neu erstellen.

Im folgenden finden Sie ein grundlegendes Verwendungs Szenario:


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



Weitere Informationen finden Sie unter [**IDirect3D9:: kreatedevice**](/windows/desktop/api) und [**IDirect3DDevice9:: getnumofswapchain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmiertipps](programming-tips.md)
</dt> </dl>

 

 
