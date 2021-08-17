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
ms.openlocfilehash: db869d277c98c3e99bd2bbc54f7e40ac86770f647e8258ee5718a96eaedec18c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118096615"
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

Wenn eine Swapkette mit einer Swap-Auswirkung von D3DSWAPEFFECT FLIP oder D3DSWAPEFFECT COPY erstellt wird, garantiert die Laufzeit, dass ein \_ \_ [**IDirect3DDevice9::P resent-Vorgang**](/windows/desktop/api) den Inhalt eines der Hintergrundpuffer nicht beeinflusst. Leider kann die Erfüllung dieser Garantie erheblichen Videospeicher- oder Verarbeitungsaufwand mit sich bringen, insbesondere bei der Implementierung von Flip-Semantik für eine Swapkette mit Fenstern oder einer Kopiersemantik für eine Auslagerungskette im Vollbildmodus. Eine Anwendung kann den D3DSWAPEFFECT DISCARD-Swapeffekt verwenden, um diesen Mehraufwand zu vermeiden und es dem Anzeigetreiber zu ermöglichen, die effizienteste Präsentationstechnik für die \_ Austauschkette auszuwählen. Dies ist auch der einzige Swapeffekt, der beim Angeben eines anderen Werts als D3DMULTISAMPLE NONE für den \_ MultiSampleType-Member von [**D3DPRESENT PARAMETERS verwendet \_ werden kann.**](d3dpresent-parameters.md)

Wie bei einer Swapkette, die D3DSWAPEFFECT FLIP verwendet, kann eine Swapkette, die D3DSWAPEFFECT DISCARD verwendet, mehrere Backpuffer enthalten, auf die über \_ \_ [**IDirect3DDevice9::GetBackBuffer**](/windows/desktop/api) oder [**IDirect3DSwapChain9::GetBackBuffer**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dswapchain9-getbackbuffer)zugegriffen werden kann. Die Swapkette wird am besten als Warteschlange bezeichnet, in der 0 immer den Hintergrundpuffer indiziert, der vom nächsten Present-Vorgang angezeigt wird und aus dem Puffer verworfen werden, wenn sie angezeigt wurden.

Eine Anwendung, die diesen Swapeffekt verwendet, kann keine Annahmen über den Inhalt eines verworfenen Zurückpuffers treffen und sollte daher vor dem Aufrufen eines Present-Vorgangs, der ihn anzeigen würde, einen gesamten Hintergrundpuffer aktualisieren. Obwohl dies nicht erzwungen wird, überschreibt die Debugversion der Laufzeit den Inhalt verworfener Puffer mit zufälligen Daten, damit Entwickler überprüfen können, ob ihre Anwendungen die gesamten Hintergrundpufferoberflächen ordnungsgemäß aktualisieren.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIP"></span><span id="d3dswapeffect_flip"></span>**D3DSWAPEFFECT \_ FLIP**
</dt> <dd>

Die Swapkette kann mehrere Hintergrundpuffer enthalten und wird am besten als kreisförmige Warteschlange mit dem Frontpuffer bezeichnet. Innerhalb dieser Warteschlange werden die Backpuffer immer sequenziell von 0 bis (n - 1) nummeriert, wobei n die Anzahl der Hintergrundpuffer ist, sodass 0 den am wenigsten kürzlich dargestellten Puffer anklangt. Wenn Present aufgerufen wird, wird die Warteschlange "gedreht", sodass der Frontpuffer zu einem Backpuffer (n - 1) wird, während der Hintergrundpuffer 0 zum neuen Frontpuffer wird.

</dd> <dt>

<span id="D3DSWAPEFFECT_COPY"></span><span id="d3dswapeffect_copy"></span>**D3DSWAPEFFECT \_ COPY**
</dt> <dd>

Dieser Swapeffekt kann nur für eine Auslagerungskette angegeben werden, die einen einzelnen Hintergrundpuffer umfasst. Unabhängig davon, ob es sich bei der Auslagerungskette um ein Fenster oder einen Vollbildmodus handelt, garantiert die Laufzeit die Semantik, die durch einen kopierbasierten Present-Vorgang impliziert wird, d. h., dass der Inhalt des Hintergrundpuffers unverändert bleibt, anstatt ihn durch den Inhalt des Frontpuffers zu ersetzen, wie es bei einem flip-basierten Present-Vorgang der Fall wäre.

Für eine Vollbild-Swapkette verwendet die Laufzeit eine Kombination aus Flip-Vorgängen und Kopiervorgängen, die bei Bedarf von ausgeblendeten Hintergrundpuffern unterstützt werden, um den Present-Vorgang durchzuführen. Entsprechend wird die Präsentation mit der vertikalen Rückverziehung des Adapters synchronisiert, und ihre Rate wird durch das ausgewählte Präsentationsintervall eingeschränkt. Eine Swapkette, die mit dem D3DPRESENT \_ INTERVAL \_ IMMEDIATE-Flag angegeben wird, ist die einzige Ausnahme. (Weitere Informationen finden Sie in der Beschreibung des **PresentationIntervals-Members** der [**D3DPRESENT \_ PARAMETERS-Struktur.)**](d3dpresent-parameters.md) In diesem Fall kopiert ein Present-Vorgang den Inhalt des Zurückpuffers direkt in den Frontpuffer, ohne auf die vertikale Rückverläufe zu warten.

</dd> <dt>

<span id="D3DSWAPEFFECT_OVERLAY"></span><span id="d3dswapeffect_overlay"></span>**D3DSWAPEFFECT \_ OVERLAY**
</dt> <dd>

Verwenden Sie einen dedizierten Bereich des Videospeichers, der auf der primären Oberfläche überlagert werden kann. Wenn die Überlagerung angezeigt wird, wird keine Kopie ausgeführt. Der Überlagerungsvorgang wird auf Hardware ausgeführt, ohne die Daten auf der primären Oberfläche zu ändern.

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- D3DSWAPEFFECT OVERLAY ist nur in Direct3D9Ex verfügbar, das auf \_ Windows 7 (oder mehr aktuellem Betriebssystem) ausgeführt wird.

</dd> <dt>

<span id="D3DSWAPEFFECT_FLIPEX"></span><span id="d3dswapeffect_flipex"></span>**D3DSWAPEFFECT \_ FLIPEX**
</dt> <dd>

Gibt an, wann eine Anwendung den Flip-Modus einschlägt. In diesem Zeitraum wird der Rahmen einer Anwendung übergeben und nicht zur Komposition in den Desktopfenster-Manager(DWM) kopiert, wenn die Anwendung im Fenstermodus dargestellt wird. Der Flip-Modus ermöglicht es einer Anwendung, die Speicherbandbreite effizienter zu nutzen und einer Anwendung die Nutzung von Statistiken im Vollbildmodus zu ermöglichen. Der Flip-Modus wirkt sich nicht auf das Vollbildverhalten aus.

> [!Note]  
> Wenn Sie eine Swapkette mit D3DSWAPEFFECT FLIPEX erstellen, können Sie das \_ **hDeviceWindow-Member** der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) nicht überschreiben, wenn Sie einen neuen Frame für die Anzeige präsentieren. Das heißt, Sie müssen **NULL** an den *hDestWindowOverride-Parameter* von [**IDirect3DDevice9Ex::P resentEx**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex) übergeben, um die Runtime anweisen zu lassen, den **hDeviceWindow-Member** von **D3DPRESENT \_ PARAMETERS** für die Präsentation zu verwenden.

Unterschiede zwischen Direct3D 9 und Direct3D 9Ex:

- D3DSWAPEFFECT FLIPEX ist nur in Direct3D9Ex verfügbar, das auf \_ Windows 7 (oder mehr aktuellem Betriebssystem) ausgeführt wird.

</dd> <dt>

<span id="D3DSWAPEFFECT_FORCE_DWORD"></span><span id="d3dswapeffect_force_dword"></span>**D3DSWAPEFFECT \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration auf eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Zustand des Hintergrundpuffers nach einem Aufruf von Present ist durch jeden dieser Swapeffekte klar definiert, und ob das Direct3D-Gerät mit einer Vollbild-Swapkette oder einer Fenster-Swapkette erstellt wurde, hat keine Auswirkungen auf diesen Zustand. Insbesondere der D3DSWAPEFFECT FLIP-Swap-Effekt funktioniert unabhängig davon, ob im Fenstermodus oder im Vollbildmodus, und die Direct3D-Laufzeit garantiert dies, indem zusätzliche Puffer erstellt \_ werden. Daher wird empfohlen, dass Anwendungen nach Möglichkeit D3DSWAPEFFECT DISCARD verwenden, \_ um solche Lästungen zu vermeiden. Dies liegt daran, dass dieser Auslagerungseffekt in Bezug auf Arbeitsspeicherverbrauch und Leistung immer am effizientesten ist.

Anwendungen, die D3DSWAPEFFECT FLIP oder \_ D3DSWAPEFFECT DISCARD verwenden, sollten nicht erwarten, dass vollbildbasierte \_ Ziel alpha funktioniert. Dies bedeutet, dass der D3DRS DESTBLEND-Renderzustand nicht wie erwartet funktioniert, da Vollbild-Austauschketten mit diesen Swapeffekten aus Sicht des Treibers kein explizites Pixelformat \_ haben. Der Treiber abgeleitet, dass er das Anzeigeformat verwenden sollte, das keinen Alphakanal hat. Führen Sie die folgenden Schritte aus, um dies zu umarbeiten:

-   Verwenden Sie D3DSWAPEFFECT \_ COPY.
-   Überprüfen Sie das Flag D3DCAPS3 ALPHA FULLSCREEN FLIP OR DISCARD im \_ \_ \_ Caps3-Member der \_ \_ [**D3DCAPS9-Struktur.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) Dieses Flag gibt an, ob der Treiber alphablenden kann, wenn D3DSWAPEFFECT \_ FLIP oder D3DSWAPEFFECT \_ DISCARD verwendet wird.
-   Anwendungen, die den Tauscheffekt im Flipmodus (D3DSWAPEFFECT FLIPEX) verwenden, sollten PresentEx nach einer Größenänderung des Fensters oder einer Änderung der Region aufrufen, um sicherzustellen, dass der Anzeigeinhalt \_ aktualisiert wird. [](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-presentex)

Ein unsichtbares Fenster kann keine Ereignisse im Benutzermodus empfangen. darüber hinaus beeinträchtigt ein unsichtbares Vollbildfenster die Darstellung des Fensters im Fenstermodus einer anderen Anwendung. Daher muss jede Anwendung sicherstellen, dass ein Gerätefenster sichtbar ist, wenn eine Swapchain im Vollbildmodus angezeigt wird.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |

## <a name="see-also"></a>Weitere Informationen

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)

[**IDirect3DDevice9::Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
