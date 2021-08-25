---
description: Beschreibt die Präsentationsparameter.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS -Struktur (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DPRESENT_PARAMETERS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 543b6b40d3fe24f902eb999a9377b8dbf60e1baa31efb70febbd2c0261d47305
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857440"
---
# <a name="d3dpresent_parameters-structure"></a>D3DPRESENT \_ PARAMETERS-Struktur

Beschreibt die Präsentationsparameter.

## <a name="syntax"></a>Syntax


```C++
typedef struct D3DPRESENT_PARAMETERS {
  UINT                BackBufferWidth;
  UINT                BackBufferHeight;
  D3DFORMAT           BackBufferFormat;
  UINT                BackBufferCount;
  D3DMULTISAMPLE_TYPE MultiSampleType;
  DWORD               MultiSampleQuality;
  D3DSWAPEFFECT       SwapEffect;
  HWND                hDeviceWindow;
  BOOL                Windowed;
  BOOL                EnableAutoDepthStencil;
  D3DFORMAT           AutoDepthStencilFormat;
  DWORD               Flags;
  UINT                FullScreen_RefreshRateInHz;
  UINT                PresentationInterval;
} D3DPRESENT_PARAMETERS, *LPD3DPRESENT_PARAMETERS;
```



## <a name="members"></a>Member

<dl> <dt>

**BackBufferWidth**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Hintergrundpuffer der neuen Austauschkette in Pixel. Wenn **Windowed** **auf FALSE** festgelegt ist (die Präsentation ist vollbildfähig), muss dieser Wert der Breite eines der aufzählten Anzeigemodi von [**EnumAdapterModes entspricht.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) Wenn **Windowed** **true ist** und **BackBufferWidth** oder **BackBufferHeight** 0 (null) ist, wird die entsprechende Dimension des Clientbereichs von **hDeviceWindow** (oder das Fokusfenster, wenn **hDeviceWindow** **NULL** ist) verwendet.

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Höhe der Hintergrundpuffer der neuen Austauschkette in Pixel. Wenn **Windowed** **auf FALSE** festgelegt ist (die Präsentation ist vollbildfähig), muss dieser Wert der Höhe eines der aufzählten Anzeigemodi von [**EnumAdapterModes entspricht.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes) Wenn **Windowed** **true ist** und **BackBufferWidth** oder **BackBufferHeight** 0 (null) ist, wird die entsprechende Dimension des Clientbereichs von **hDeviceWindow** (oder das Fokusfenster, wenn **hDeviceWindow** **NULL** ist) verwendet.

</dd> <dt>

**BackBufferFormat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Das Format des Hintergrundpuffers. Weitere Informationen zu Formaten finden Sie unter [D3DFORMAT](d3dformat.md). Dieser Wert muss eines der Renderzielformate sein, wie von [**CheckDeviceType überprüft.**](/windows/desktop/api) Sie können [**GetDisplayMode verwenden,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) um das aktuelle Format zu erhalten.

Tatsächlich kann D3DFMT \_ UNKNOWN für **das BackBufferFormat** im Fenstermodus angegeben werden. Dies weist die Runtime an, das aktuelle Anzeigemodusformat zu verwenden, und macht es nicht mehr notwendig, [**GetDisplayMode auf aufruft.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)

Bei Anwendungen mit Fenstern muss das Format des Hintergrundpuffers nicht mehr mit dem Anzeigemodusformat übereinstimmen, da die Farbkonvertierung jetzt von der Hardware durchgeführt werden kann (wenn die Hardware die Farbkonvertierung unterstützt). Der Satz möglicher Backpufferformate ist eingeschränkt, aber die Runtime lässt zu, dass jedes gültige Backpufferformat in jedem Desktopformat dargestellt wird. (Es gibt die zusätzliche Anforderung, dass das Gerät auf dem Desktop ausgeführt werden kann. Geräte funktionieren in der Regel nicht in 8 Bits pro Pixelmodus.)

Vollbildanwendungen können keine Farbkonvertierung verwenden.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Dieser Wert kann zwischen 0 und [D3DPRESENT \_ BACK \_ BUFFERS \_ MAX](d3dpresent-back-buffers.md) (oder [D3DPRESENT \_ BACK \_ BUFFERS MAX \_ \_ EX](d3dpresent-back-buffers.md) bei Verwendung von Direct3D 9Ex) liegen. Werte von 0 werden als 1 behandelt. Wenn die Anzahl der Backpuffer nicht erstellt werden kann, erzeugt die Laufzeit einen Fehler beim Methodenaufruf und füllt diesen Wert mit der Anzahl der Backpuffer auf, die erstellt werden könnten. Daher kann eine Anwendung die -Methode zweimal mit derselben D3DPRESENT PARAMETERS-Struktur aufrufen und erwarten, dass sie beim \_ zweiten Mal funktioniert.

Die Methode schlägt fehl, wenn kein Backpuffer erstellt werden kann. Der Wert von **BackBufferCount beeinflusst,** welche Swapeffekte zulässig sind. Insbesondere erfordert jeder D3DSWAPEFFECT \_ COPY-Auslagerungseffekt genau einen Hintergrundpuffer.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Typ: **[ **D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md)**

</dd> <dd>

Member des [**aufzählten D3DMULTISAMPLE \_ TYPE-Typs.**](./d3dmultisample-type.md) Der Wert muss D3DMULTISAMPLE NONE sein, es sei \_ **denn, SwapEffect** wurde auf D3DSWAPEFFECT \_ DISCARD festgelegt. Multisampling wird nur unterstützt, wenn der Swapeffekt D3DSWAPEFFECT \_ DISCARD ist.

</dd> <dt>

**MultiSampleQuality**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualitätsstufe. Der gültige Bereich liegt zwischen 0 und 1 kleiner als die von pQualityLevels zurückgegebene Ebene, die von [**CheckDeviceMultiSampleType verwendet wird.**](/windows/desktop/api) Die Übergabe eines größeren Werts gibt den Fehler D3DERR \_ INVALIDCALL zurück. Gekoppelte Werte von Renderzielen oder tiefen Schablonenoberflächen und [**D3DMULTISAMPLE \_ TYPE**](./d3dmultisample-type.md) müssen übereinstimmen.

</dd> <dt>

**SwapEffect**
</dt> <dd>

Typ: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Member des [**aufzählten D3DSWAPEFFECT-Typs.**](./d3dswapeffect.md) Die Laufzeit garantiert die implizite Semantik in Bezug auf das Puffertauschverhalten. Wenn **Windowed** auf **TRUE** festgelegt ist und **SwapEffect** auf D3DSWAPEFFECT FLIP festgelegt ist, erstellt die Laufzeit einen zusätzlichen Hintergrundpuffer und kopiert den Puffer, der zur Präsentationszeit zum Frontpuffer \_ wird.

D3DSWAPEFFECT \_ COPY erfordert, dass **BackBufferCount** auf 1 festgelegt ist.

D3DSWAPEFFECT DISCARD wird in der Debuglaufzeit erzwungen, indem jeder Puffer mit Rauschen gefüllt wird, \_ nachdem er dargestellt wurde.

Unterschiede zwischen Direct3D9 und Direct3D9Ex:

- In Direct3D9Ex wird D3DSWAPEFFECT FLIPEX hinzugefügt, um zu bestimmen, wann eine Anwendung den \_ Flip-Modus einschlägt. Das heißt, dass der Frame einer Anwendung im Fenstermodus (anstatt kopiert) zur Komposition an den Desktopfenster-Manager(DWM) übergeben wird. Der Flip-Modus bietet eine effizientere Speicherbandbreite und ermöglicht es einer Anwendung, die Vorteile von Statistiken im Vollbildmodus zu nutzen. Das Verhalten des Vollbildmodus wird nicht geändert. Das Verhalten des Flip-Modus ist ab Windows 7 verfügbar.



 

</dd> <dt>

**hDeviceWindow**
</dt> <dd>

Typ: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Das Gerätefenster bestimmt den Speicherort und die Größe des Hintergrundpuffers auf dem Bildschirm. Dies wird von Direct3D verwendet, wenn der Inhalt des Hintergrundpuffers während present in den Frontpuffer [**kopiert wird.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)

-   Bei einer Vollbildanwendung ist dies ein Handle für das obere Fenster (das Fokusfenster).

    Für Anwendungen, die mehrere Vollbildgeräte verwenden (z. B. ein System mit mehreren Monitoren), kann genau ein Gerät das Fokusfenster als Gerätefenster verwenden. Alle anderen Geräte müssen über eindeutige Gerätefenster verfügen.

-   Für eine Anwendung im Fenstermodus ist dieses Handle das Standardzielfenster für [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Wenn dieses Handle NULL **ist,** wird das Fokusfenster verwendet.

Beachten Sie, dass die Runtime nicht versucht, Benutzeränderungen in der Fenstergröße widerzu spiegeln. Der Hintergrundpuffer wird nicht implizit zurückgesetzt, wenn dieses Fenster zurückgesetzt wird. Die [**Present-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) verfolgt änderungen an der Fensterposition jedoch automatisch nach.

</dd> <dt>

**Fenstermodus**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

**TRUE,** wenn die Anwendung im Fenster ausgeführt wird; **FALSE,** wenn die Anwendung im Vollbildmodus ausgeführt wird.

</dd> <dt>

**EnableAutoDepthStencil**
</dt> <dd>

Typ: **[ **BOOL**](../winprog/windows-data-types.md)**

</dd> <dd>

Wenn dieser Wert **TRUE ist,** verwaltet Direct3D Tiefenpuffer für die Anwendung. Das Gerät erstellt einen Tiefen-Schablonenpuffer, wenn es erstellt wird. Der Tiefen-Schablonenpuffer wird automatisch als Renderziel des Geräts festgelegt. Wenn das Gerät zurückgesetzt wird, wird der Tiefen-Schablonenpuffer automatisch zerstört und in der neuen Größe neu erstellt.

Wenn EnableAutoDepthStencil **true** ist, muss AutoDepthStencilFormat ein gültiges Tiefen-Schablonenformat sein.

</dd> <dt>

**AutoDepthStencilFormat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [aufzählten D3DFORMAT-Typs.](d3dformat.md) Das Format der automatischen Tiefen-Schablonenoberfläche, die das Gerät erstellt. Dieser Member wird ignoriert, es sei **denn, EnableAutoDepthStencil ist** **TRUE.**

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine der [D3DPRESENTFLAG-Konstanten.](d3dpresentflag.md)

</dd> <dt>

**FullScreen \_ RefreshRateInHz**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Rate, mit der der Adapter den Bildschirm aktualisiert. Der Wert hängt vom Modus ab, in dem die Anwendung ausgeführt wird:

-   Für den Fenstermodus muss die Aktualisierungsrate 0 sein.
-   Im Vollbildmodus ist die Aktualisierungsrate eine der Aktualisierungsraten, die von [**EnumAdapterModes zurückgegeben werden.**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)

</dd> <dt>

**PresentationInterval**
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

</dd> <dd>

Die maximale Rate, mit der die Hintergrundpuffer der Auslagerungskette dem Frontpuffer präsentiert werden können. Eine ausführliche Erläuterung der unterstützten Modi und Intervalle finden Sie unter [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**CreateDevice**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
