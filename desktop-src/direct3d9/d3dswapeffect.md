---
description: Definiert Auslagerungs Effekte.
ms.assetid: 522a5f71-3ad9-4cfc-a899-e25b9b721b1b
title: D3DSWAPEFFECT-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DSWAPEFFECT
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 41327dc66f676c6f498ad0cefb23202bedc13112
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370421"
---
# <a name="d3dswapeffect-enumeration"></a>D3DSWAPEFFECT-Enumeration

Definiert Auslagerungs Effekte.

## <a name="syntax"></a>Syntax

```cpp
typedef enum D3DSWAPEFFECT { 
  D3DSWAPEFFECT_DISCARD      = 1,
  D3DSWAPEFFECT_FLIP         = 2,
  D3DSWAPEFFECT_COPY         = 3,
  D3DSWAPEFFECT_OVERLAY      = 4,
  D3DSWAPEFFECT_FLIPEX       = 5,
  D3DSWAPEFFECT_FORCE_DWORD  = 0xFFFFFFFF
} D3DSWAPEFFECT, *LPD3DSWAPEFFECT;
```

## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ verwerfen**
</dt> <dd>

Wenn eine SwapChain mit einem Auslagerungs Effekt von D3DSWAPEFFECT \_ Flip oder D3DSWAPEFFECT Copy erstellt wird \_ , gewährleistet die Laufzeit, dass ein [**IDirect3DDevice9::P Resent**](/windows/desktop/api) -Vorgang den Inhalt eines beliebigen backpuffers nicht beeinträchtigt. Leider kann diese Garantie durch einen beträchtlichen Video-oder Verarbeitungsaufwand erreicht werden, insbesondere bei der Implementierung von Flip-Semantik für eine Fensteraustausch Kette oder Kopier Semantik für eine voll Bildaustausch Kette. Eine Anwendung kann den D3DSWAPEFFECT \_ DISCARD-Swap-Effekt verwenden, um diese Ober Köpfe zu vermeiden und den Anzeigetreiber zu aktivieren, um die effizienteste Präsentationstechnik für die SwapChain auszuwählen. Dies ist auch der einzige Auslagerungs Effekt, der beim Angeben eines anderen Werts als D3DMULTISAMPLE \_ None für den MultiSampleType-Member von [**D3DPRESENT- \_ Parametern**](d3dpresent-parameters.md)verwendet werden kann.

Wie eine Swapkette, die D3DSWAPEFFECT \_ Flip verwendet, kann eine Swapkette, die D3DSWAPEFFECT verwerfen verwendet, \_ mehr als einen BackBuffer enthalten, auf den möglicherweise mit [**IDirect3DDevice9:: GetBackBuffer**](/windows/desktop/api) oder [**IDirect3DSwapChain9:: GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)zugegriffen wird. Die Swapkette ist am besten als Warteschlange gedacht, bei der 0 immer den zurück Puffer indiziert, der vom nächsten aktuellen Vorgang angezeigt wird, und von dem Puffer verworfen werden, wenn Sie angezeigt werden.

Eine Anwendung, die diesen swapffekt verwendet, kann keine Annahmen über den Inhalt eines verworfenen backpuffers treffen und sollte daher einen gesamten Hintergrund Puffer aktualisieren, bevor Sie einen vorhandenen Vorgang aufrufen, der ihn anzeigen würde. Obwohl dies nicht erzwungen wird, überschreibt die Debugversion der Laufzeit den Inhalt der verworfenen Puffer mit zufälligen Daten, damit Entwickler sicherstellen können, dass Ihre Anwendungen den gesamten Hintergrund Puffer ordnungsgemäß aktualisieren.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ kippen**
</dt> <dd>

Die Swapkette enthält möglicherweise mehrere Back-Puffer und ist am besten als eine zirkuläre Warteschlange mit dem Front-Puffer vorgesehen. In dieser Warteschlange werden die Back Puffer immer sequenziell von 0 bis (n-1) nummeriert, wobei n die Anzahl der Back Puffer ist, d. h., 0 steht für den am wenigsten aktuell dargestellten Puffer. Wenn Present aufgerufen wird, wird die Warteschlange "gedreht", sodass der Vorder-Puffer in den Puffer (n-1) wechselt, während der Hintergrund Puffer 0 zum neuen Front-Puffer wird.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT \_ Kopieren**
</dt> <dd>

Dieser swapffekt kann nur für eine Austausch Kette angegeben werden, die einen einzelnen Hintergrund Puffer umfasst. Unabhängig davon, ob es sich um die Swapkette oder den voll Bildschirm handelt, gewährleistet die Laufzeit die Semantik, die von einem Kopier basierten, aktuellen Vorgang impliziert wird, d. h., dass der Vorgang den Inhalt des Hintergrund Puffers unverändert lässt, anstatt ihn durch den Inhalt des Front-Puffers zu ersetzen, der durch einen Flip-basierten aktuellen Vorgang

Bei einer Vollbild-Swapkette verwendet die Laufzeit eine Kombination aus Flip-und Kopier Vorgängen, die ggf. von ausgeblendeten Puffer unterstützt werden, um den aktuellen Vorgang auszuführen. Dementsprechend wird die Präsentation mit der vertikalen neuverfolgung des Anzeige Adapters synchronisiert, und die Rate wird durch das ausgewählte Präsentations Intervall eingeschränkt. Eine Auslagerungs Kette, die mit dem D3DPRESENT \_ Interval \_ immediate-Flag angegeben wird, ist die einzige Ausnahme. (Weitere Informationen finden Sie in der Beschreibung des **presentationintervalle** -Members der [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur.) In diesem Fall kopiert ein vorhandener Vorgang den Hintergrund Pufferinhalt direkt in den Vorder-Puffer, ohne auf die vertikale neuverfolgung zu warten.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT- \_ Overlay**
</dt> <dd>

Verwenden Sie einen dedizierten Bereich von Video Arbeitsspeicher, der auf der primären Oberfläche überlastet werden kann. Wenn das Overlay angezeigt wird, wird kein Kopiervorgang durchgeführt. Der Überlagerungs Vorgang wird in Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.

|                                                                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DSWAPEFFECT \_ Overlay ist nur in Direct3D9Ex verfügbar, die unter Windows 7 (oder einem höheren aktuellen Betriebssystem) ausgeführt werden.<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ flipex**
</dt> <dd>

Wird festgelegt, wenn eine Anwendung den Flip-Modus annimmt. während dieser Zeit wird der Frame einer Anwendung statt in den Desktopfenster-Manager (DWM) zur Komposition kopiert, wenn die Anwendung im Fenstermodus präsentiert wird. Der Modus "Kippen" ermöglicht es einer Anwendung, die Arbeitsspeicher Bandbreite effizienter zu nutzen und einer Anwendung zu ermöglichen, die Vollbildansicht der Statistiken zu nutzen. Der Modus "Kippen" wirkt sich nicht auf das voll Bild Verhalten aus.

> [!Note]  
> Wenn Sie eine Austausch Kette mit D3DSWAPEFFECT \_ flipex erstellen, können Sie das **hdevicewindow** -Element der [**D3DPRESENT- \_ Parameter**](d3dpresent-parameters.md) Struktur nicht überschreiben, wenn Sie einen neuen Frame für die Anzeige darstellen. Das heißt, Sie müssen **null** an den *hdestwindowoverride* -Parameter von [**IDirect3DDevice9Ex::P resentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) übergeben, um die Laufzeit anzuweisen, den **hdevicewindow** -Member von **D3DPRESENT- \_ Parametern** für die Präsentation zu verwenden.

|                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:<br/> D3DSWAPEFFECT \_ flipex ist nur in Direct3D9Ex verfügbar, die unter Windows 7 (oder einem höheren Betriebssystem) ausgeführt werden.<br/> |

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zustand des Hintergrund Puffers, nachdem ein-Befehl vorhanden ist, ist durch die einzelnen Auslagerungs Effekte wohl definiert, und ob das Direct3D-Gerät mit einer Vollbild-Swapkette erstellt wurde, oder eine Fensteraustausch Kette hat keine Auswirkung auf diesen Zustand. Der D3DSWAPEFFECT \_ Flip-swapffekt funktioniert insbesondere unabhängig davon, ob es sich um ein Fenster oder einen voll Bildschirm handelt, und die Direct3D-Laufzeit gewährleistet dies durch das Erstellen zusätzlicher Puffer Daher wird empfohlen, dass Anwendungen D3DSWAPEFFECT \_ verwerfen, wann immer möglich, verwenden, um derartige Strafen zu vermeiden. Dies liegt daran, dass dieser Auslagerungs Effekt in Bezug auf den Arbeitsspeicher Verbrauch und die Leistung immer die effizienteste ist.

Anwendungen, die D3DSWAPEFFECT \_ Flip oder D3DSWAPEFFECT \_ DISCARD verwenden, sollten nicht erwarten, dass das Vollbild-zielalpha funktioniert. Dies bedeutet, dass der D3DRS \_ destblend-renderzustand nicht erwartungsgemäß funktioniert, weil Vollbild-Austausch Ketten mit diesen Swap-Effekten kein explizites Pixel Format aus der Sicht des Treibers aufweisen. Der Treiber leitet das Anzeige Format ab, das nicht über einen Alphakanal verfügt. Um dieses Problem zu umgehen, führen Sie die folgenden Schritte aus:

-   Verwenden Sie D3DSWAPEFFECT \_ Copy.
-   Aktivieren Sie das \_ Flag D3DCAPS3 Alpha \_ Fullscreen \_ Flip \_ oder \_ DISCARD im Caps3-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur. Dieses Flag gibt an, ob der Treiber Alpha Blending durchführen kann, wenn D3DSWAPEFFECT \_ Flip oder D3DSWAPEFFECT \_ DISCARD verwendet wird.
-   Anwendungen, die den Flip-modusauslagerungs Effekt (D3DSWAPEFFECT \_ flipex) verwenden, sollten " [**presentex**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) " aufrufen, nachdem die Größe des Fensters geändert oder die Änderung des Fensters geändert wurde.

Ein unsichtbares Fenster kann keine benutzermodusereignisse empfangen. Außerdem wird ein unsichtbares Vollbild-Fenster mit der Darstellung des Fensters Fenster einer anderen Anwendung beeinträchtigt. Daher muss jede Anwendung sicherstellen, dass ein Geräte Fenster sichtbar ist, wenn eine vorhandenes SwapChain im Vollbildmodus angezeigt wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |

## <a name="see-also"></a>Siehe auch

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9:: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
