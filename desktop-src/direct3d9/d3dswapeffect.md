---
description: Definiert Swapeffekte.
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
ms.openlocfilehash: 58354e35ca8456f6fde57d2f2567a6b6a202f6d7
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343035"
---
# <a name="d3dswapeffect-enumeration"></a>D3DSWAPEFFECT-Enumeration

Definiert Swapeffekte.

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

<span id="D3DSWAPEFFECT_DISCARD"></span><span id="d3dswapeffect_discard"></span>**D3DSWAPEFFECT \_ DISCARD**
</dt> <dd>

Wenn eine Swapkette mit dem Swapeffekt D3DSWAPEFFECT \_ FLIP oder D3DSWAPEFFECT COPY erstellt \_ wird, garantiert die Laufzeit, dass ein [**IDirect3DDevice9::P Resent-Vorgang**](/windows/desktop/api) keine Auswirkungen auf den Inhalt der Backpuffer hat. Leider kann die Erfüllung dieser Garantie beträchtlichen Mehraufwand für Videospeicher oder Verarbeitung bedeuten, insbesondere bei der Implementierung der Flip-Semantik für eine Auslagerungskette mit Fenstern oder der Kopiersemantik für eine Vollbild-Austauschkette. Eine Anwendung kann den D3DSWAPEFFECT \_ DISCARD-Swapeffekt verwenden, um diesen Mehraufwand zu vermeiden und dem Anzeigetreiber zu ermöglichen, die effizienteste Präsentationstechnik für die Austauschkette auszuwählen. Dies ist auch der einzige Swapeffekt, der verwendet werden kann, wenn ein anderer Wert als D3DMULTISAMPLE \_ NONE für den MultiSampleType-Member von [**D3DPRESENT \_ PARAMETERS**](d3dpresent-parameters.md)angegeben wird.

Wie eine Swapkette, die D3DSWAPEFFECT \_ FLIP verwendet, kann eine Swapkette, die D3DSWAPEFFECT \_ DISCARD verwendet, mehrere Backpuffer enthalten, auf die mit [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) oder [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)zugegriffen werden kann. Die Swapkette wird am besten als Warteschlange bezeichnet, in der 0 immer den Backpuffer indiziert, der beim nächsten Present-Vorgang angezeigt wird und aus der Puffer verworfen werden, wenn sie angezeigt werden.

Eine Anwendung, die diesen Swapeffekt verwendet, kann keine Annahmen über den Inhalt eines verworfenen Hintergrundpuffers treffen und sollte daher einen gesamten Hintergrundpuffer aktualisieren, bevor ein Present-Vorgang ausgelöst wird, der ihn anzeigen würde. Obwohl dies nicht erzwungen wird, überschreibt die Debugversion der Runtime den Inhalt verworfener Backpuffer mit zufälligen Daten, damit Entwickler überprüfen können, ob ihre Anwendungen die gesamte Backpufferoberfläche ordnungsgemäß aktualisieren.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**
</dt> <dd>

Die Swapkette kann mehrere Hintergrundpuffer enthalten und wird am besten als kreisförmige Warteschlange mit dem Frontpuffer verwendet. Innerhalb dieser Warteschlange werden die Backpuffer immer sequenziell von 0 bis (n - 1) nummeriert, wobei n die Anzahl der Hintergrundpuffer ist, sodass 0 den am wenigsten kürzlich präsentierten Puffer anschließt. Wenn Present aufgerufen wird, wird die Warteschlange "gedreht", sodass der Frontpuffer zum Backpuffer (n - 1) wird, während der Backpuffer 0 zum neuen Frontpuffer wird.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT \_ COPY**
</dt> <dd>

Dieser Swapeffekt kann nur für eine Swapkette angegeben werden, die aus einem einzelnen Backpuffer besteht. Unabhängig davon, ob die Swapkette im Fenster oder im Vollbildmodus angezeigt wird, garantiert die Laufzeit die Semantik, die durch einen kopierbasierten Present-Vorgang impliziert wird, nämlich dass der Vorgang den Inhalt des Hintergrundpuffers unverändert lässt, anstatt ihn durch den Inhalt des Frontpuffers als flipbasierten Present-Vorgang zu ersetzen.

Für eine Vollbild-Swapkette verwendet die Laufzeit eine Kombination aus Flip-Vorgängen und Kopiervorgängen, die bei Bedarf von ausgeblendeten Hintergrundpuffern unterstützt werden, um den Present-Vorgang zu erreichen. Entsprechend wird die Präsentation mit dem vertikalen Retrace des Anzeigeadapters synchronisiert, und die Geschwindigkeit wird durch das ausgewählte Präsentationsintervall eingeschränkt. Eine Mit dem D3DPRESENT INTERVAL IMMEDIATE-Flag angegebene Swapkette \_ \_ ist die einzige Ausnahme. (Weitere Informationen finden Sie in der Beschreibung des **PresentationIntervals-Elements** der [**D3DPRESENT PARAMETERS-Struktur.) \_**](d3dpresent-parameters.md) In diesem Fall kopiert ein Present-Vorgang den Inhalt des Hintergrundpuffers direkt in den Frontpuffer, ohne auf den vertikalen Retrace zu warten.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT-ÜBERLAGERUNG \_**
</dt> <dd>

Verwenden Sie einen dedizierten Bereich des Videospeichers, der auf der primären Oberfläche überlagert werden kann. Es wird keine Kopie ausgeführt, wenn die Überlagerung angezeigt wird. Der Überlagerungsvorgang wird auf Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- D3DSWAPEFFECT \_ OVERLAY ist nur in Direct3D9Ex unter Windows 7 (oder einem aktuelleren Betriebssystem) verfügbar.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Legt fest, wann eine Anwendung den Flip-Modus einnimmt. In diesem Zeitraum wird der Frame einer Anwendung übergeben, anstatt zur Komposition in den Desktopfenster-Manager (DWM) kopiert zu werden, wenn die Anwendung im Fenstermodus angezeigt wird. Der Flip-Modus ermöglicht es einer Anwendung, die Speicherbandbreite effizienter zu nutzen und einer Anwendung die Nutzung von statistiken im Vollbildmodus zu ermöglichen. Der Flip-Modus wirkt sich nicht auf das Vollbildverhalten aus.

> [!Note]  
> Wenn Sie eine Swapkette mit D3DSWAPEFFECT \_ FLIPEX erstellen, können Sie den **hDeviceWindow-Member** der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) nicht überschreiben, wenn Sie einen neuen Frame für die Anzeige präsentieren. Das heißt, Sie müssen **NULL** an den *hDestWindowOverride-Parameter* von [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) übergeben, um die Laufzeit anzuweisen, den **hDeviceWindow-Member** von **D3DPRESENT \_ PARAMETERS** für die Präsentation zu verwenden.

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- D3DSWAPEFFECT \_ FLIPEX ist nur in Direct3D9Ex unter Windows 7 (oder einem aktuelleren Betriebssystem) verfügbar.

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zustand des Backpuffers nach einem Aufruf von Present ist durch jeden dieser Austauscheffekte klar definiert, und ob das Direct3D-Gerät mit einer Vollbild-Auslagerungskette oder einer Auslagerungskette im Fenster erstellt wurde, hat keine Auswirkungen auf diesen Zustand. Insbesondere funktioniert der Flip-Swapeffekt D3DSWAPEFFECT \_ unabhängig davon, ob es sich um ein Fenster oder einen Vollbildmodus handelt, und die Direct3D-Laufzeit garantiert dies, indem zusätzliche Puffer erstellt werden. Daher wird empfohlen, dass Anwendungen nach Möglichkeit D3DSWAPEFFECT \_ DISCARD verwenden, um derartige Nachteile zu vermeiden. Dies liegt daran, dass dieser Auslagerungseffekt in Bezug auf Arbeitsspeicherverbrauch und Leistung immer am effizientesten ist.

Anwendungen, die D3DSWAPEFFECT FLIP oder \_ D3DSWAPEFFECT DISCARD verwenden, sollten nicht erwarten, dass vollbildbasierte \_ Ziel alpha funktioniert. Dies bedeutet, dass der D3DRS DESTBLEND-Renderzustand nicht wie erwartet funktioniert, da Vollbild-Swapketten mit diesen Swapeffekten aus Sicht des Treibers kein explizites Pixelformat \_ haben. Der Treiber abgeleitet, dass er das Anzeigeformat verwenden sollte, das keinen Alphakanal hat. Führen Sie die folgenden Schritte aus, um dies zu umarbeiten:

-   Verwenden Sie D3DSWAPEFFECT \_ COPY.
-   Überprüfen Sie das Flag D3DCAPS3 \_ ALPHA \_ FULLSCREEN \_ FLIP OR DISCARD im \_ Caps3-Member der \_ [**D3DCAPS9-Struktur.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Dieses Flag gibt an, ob der Treiber alphablenden kann, wenn D3DSWAPEFFECT \_ FLIP oder D3DSWAPEFFECT \_ DISCARD verwendet wird.
-   Anwendungen, die den Tauscheffekt des Flip-Modus (D3DSWAPEFFECT FLIPEX) verwenden, sollten PresentEx nach einer Größenänderung des Fensters oder einer Änderung der Region aufrufen, um sicherzustellen, dass der Anzeigeinhalt \_ aktualisiert wird. [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)

Ein unsichtbares Fenster kann keine Ereignisse im Benutzermodus empfangen. darüber hinaus beeinträchtigt ein unsichtbares Vollbildfenster die Darstellung des Fensters im Fenstermodus einer anderen Anwendung. Daher muss jede Anwendung sicherstellen, dass ein Gerätefenster sichtbar ist, wenn eine Swapchain im Vollbildmodus angezeigt wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
