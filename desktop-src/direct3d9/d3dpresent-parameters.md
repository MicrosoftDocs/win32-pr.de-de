---
description: Beschreibt die Präsentations Parameter.
ms.assetid: d677aeb7-a188-4ddc-b8c9-48e13676e9c8
title: D3DPRESENT_PARAMETERS-Struktur (D3D9Types. h)
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
ms.openlocfilehash: f83ab03773356a01c8c6ac490bb099c6e7508be2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355057"
---
# <a name="d3dpresent_parameters-structure"></a>D3DPRESENT \_ Parameters-Struktur

Beschreibt die Präsentations Parameter.

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

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Breite der Hintergrund Puffer der neuen Austausch Kette in Pixel. Wenn " **Windowed** " den Wert " **false** " hat (die Präsentation ist voll Bildschirm), muss dieser Wert mit der Breite eines der aufgelisteten Anzeigemodi identisch sein, die über [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden. Wenn **Windowed** den Wert **true** aufweist und entweder **BackBufferWidth** oder **BackBufferHeight** gleich NULL ist, wird die entsprechende Dimension des Client Bereichs von **hdevicewindow** (oder im Fokus Fenster, wenn **hdevicewindow** **null** ist) übernommen.

</dd> <dt>

**BackBufferHeight**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Höhe der Hintergrund Puffer der neuen Austausch Kette in Pixel. Wenn " **Windowed** " den Wert " **false** " hat (die Präsentation ist voll Bildschirm), muss dieser Wert mit der Höhe eines der aufgelisteten Anzeigemodi identisch sein, die über [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)gefunden werden. Wenn **Windowed** den Wert **true** aufweist und entweder **BackBufferWidth** oder **BackBufferHeight** gleich NULL ist, wird die entsprechende Dimension des Client Bereichs von **hdevicewindow** (oder im Fokus Fenster, wenn **hdevicewindow** **null** ist) übernommen.

</dd> <dt>

**Backbufferformat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Das Format des Hintergrund Puffers. Weitere Informationen zu Formaten finden Sie unter [D3DFORMAT](d3dformat.md). Bei diesem Wert muss es sich um eines der renderzielformate handeln, die von [**CheckDeviceType**](/windows/desktop/api)überprüft werden. Sie können [**getdisplaymode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode) zum Abrufen des aktuellen Formats verwenden.

Tatsächlich \_ kann D3DFMT Unknown für das **backbufferformat** im Fenstermodus angegeben werden. Dadurch wird der Laufzeit mitgeteilt, dass das aktuelle Anzeigemodus-Format verwendet wird, und es entfällt, dass [**getdisplaymode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdisplaymode)aufgerufen werden muss.

Für Fenster Anwendungen muss das Hintergrund Puffer Format nicht mehr dem Anzeigemodus entsprechen, da die Farbkonvertierung nun von der Hardware durchgeführt werden kann (wenn die Hardware Farbkonvertierung unterstützt). Der Satz möglicher backpufferformate ist eingeschränkt, aber die Laufzeit lässt zu, dass jedes beliebige gültige Hintergrund Puffer Format allen Desktop Formaten angezeigt wird. (Es ist erforderlich, dass das Gerät auf dem Desktop betriebsbereit ist. Geräte funktionieren in der Regel nicht im Modus von 8 Bits pro Pixel.)

Vollbildanwendungen können keine Farbkonvertierung durchführen.

</dd> <dt>

**BackBufferCount**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Dieser Wert kann zwischen 0 und [D3DPRESENT \_ Back \_ Puffern \_ Max](d3dpresent-back-buffers.md) (oder [D3DPRESENT \_ Back \_ Puffern \_ Max \_ Ex](d3dpresent-back-buffers.md) bei Verwendung von Direct3D 9Ex) liegen. Werte von 0 werden als 1 behandelt. Wenn die Anzahl der Back Puffer nicht erstellt werden kann, misslingt die Laufzeit den Methoden Aufrufvorgang und füllen diesen Wert mit der Anzahl der zu erstellenden Sicherungs Puffer aus. Daher kann eine Anwendung die Methode zweimal mit der gleichen D3DPRESENT \_ Parameters-Struktur abrufen und erwarten, dass Sie beim zweiten Mal funktioniert.

Die Methode schlägt fehl, wenn ein BackBuffer nicht erstellt werden kann. Der Wert von **BackBufferCount** wirkt sich darauf aus, welche Gruppe von Swap-Effekten zulässig sind. Insbesondere ist es erforderlich, dass für jeden D3DSWAPEFFECT-Auslagerungs \_ Effekt genau ein Hintergrund Puffer vorhanden ist.

</dd> <dt>

**MultiSampleType**
</dt> <dd>

Type: **[ **D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md)**

</dd> <dd>

Member des [**D3DMULTISAMPLE \_ Type**](./d3dmultisample-type.md) -enumerierten Typs. Der Wert muss D3DMULTISAMPLE \_ None lauten, es sei denn, für " **Swap** " wurde "D3DSWAPEFFECT DISCARD" festgelegt \_ . Multisampling wird nur unterstützt, wenn der Auslagerungs Effekt D3DSWAPEFFECT \_ verwerfen ist.

</dd> <dt>

**Multisamplequality**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Qualitätsstufe. Der gültige Bereich liegt zwischen 0 (null) und einem niedrigeren Wert als der von " [**checkdevicemultisampletype**](/windows/desktop/api)" verwendeten pqualitylevels. Wenn Sie einen größeren Wert übergeben, wird der Fehler D3DERR \_ invalidcallzurück gegeben. Gekoppelte Werte von renderzielen oder tiefen Schablonen und der [**D3DMULTISAMPLE- \_ Typ**](./d3dmultisample-type.md) müssen mit identisch sein.

</dd> <dt>

**SwapEffect verwenden**
</dt> <dd>

Typ: **[ **D3DSWAPEFFECT**](./d3dswapeffect.md)**

</dd> <dd>

Member des [**D3DSWAPEFFECT**](./d3dswapeffect.md) -Enumerationstyps. Die Laufzeit gewährleistet die implizite Semantik bezüglich des Puffer Austausch Verhaltens. Wenn " **Windowed** " auf " **true** " festgelegt ist und " **Swap** " auf "D3DSWAPEFFECT Flip" festgelegt ist \_ , erstellt die Laufzeit einen zusätzlichen Hintergrund Puffer und kopiert, je nachdem, welcher der vordere Puffer zur Präsentationszeit wird.

D3DSWAPEFFECT \_ Copy erfordert, dass **BackBufferCount** auf 1 festgelegt ist.

D3DSWAPEFFECT \_ verwerfen wird in der Debug-Laufzeit erzwungen, indem jeder Puffer mit Rauschen aufgefüllt wird, nachdem er angezeigt wird.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterschiede zwischen von Direct3D9 und Direct3D9Ex<br/> In Direct3D9Ex wird D3DSWAPEFFECT \_ flipex hinzugefügt, um zu bestimmen, wann eine Anwendung den Flip-Modus annimmt. Das heißt, der Rahmen einer Anwendung wird im Fenstermodus (anstelle von kopiert) zur Komposition an den Desktopfenster-Manager (DWM) übermittelt. Der Flip-Modus sorgt für eine effizientere Arbeitsspeicher Bandbreite und ermöglicht einer Anwendung, die Vollbildansicht von Statistiken zu nutzen. Das Verhalten der voll Bild Anzeige wird nicht geändert. Das Verhalten des Flip-Modus ist ab Windows 7 verfügbar.<br/> |



 

</dd> <dt>

**hdevicewindow**
</dt> <dd>

Typ: **[ **HWND**](../winprog/windows-data-types.md)**

</dd> <dd>

Das Geräte Fenster bestimmt den Speicherort und die Größe des Hintergrund Puffers auf dem Bildschirm. Diese wird von Direct3D verwendet, wenn der Hintergrund Pufferinhalt während der [**Anwesenheit**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)in den Vorder-Puffer kopiert wird.

-   Bei einer Vollbildanwendung handelt es sich hierbei um ein Handle für das obere Fenster (das Fokus Fenster).

    Bei Anwendungen mit mehreren voll Bild Geräten (z. b. einem Multimonitor-System) kann genau ein Gerät das Fokus Fenster als Geräte Fenster verwenden. Alle anderen Geräte müssen über eindeutige Geräte Fenster verfügen.

-   Bei einer Anwendung im Windowed-Modus ist dieses handle das Standardziel Fenster für das [**vorhanden**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)sein. Wenn dieses Handle **null** ist, wird das Fokus Fenster übernommen.

Beachten Sie, dass die Laufzeit keinen Versuch hat, Benutzer Änderungen in der Fenstergröße widerzuspiegeln. Der Hintergrund Puffer wird beim Zurücksetzen dieses Fensters nicht implizit zurückgesetzt. Allerdings werden die Änderungen an der Fensterposition von der [**aktuellen**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) Methode automatisch nachverfolgt.

</dd> <dt>

**Fenster**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

**True** , wenn die Anwendung ausgeführt wird. **False** , wenn die Anwendung voll Bildschirm ausführt.

</dd> <dt>

**Enableautodepthstencil**
</dt> <dd>

Typ: **[ **bool**](../winprog/windows-data-types.md)**

</dd> <dd>

Wenn dieser Wert **true** ist, verwaltet Direct3D Tiefe Puffer für die Anwendung. Das Gerät erstellt einen tiefen Schablone-Puffer, wenn er erstellt wird. Der tiefen Schablone-Puffer wird automatisch als Renderziel des Geräts festgelegt. Wenn das Gerät zurückgesetzt wird, wird der tiefen Schablone-Puffer automatisch zerstört und in der neuen Größe neu erstellt.

Wenn enableautodepthstencil den Wert **true** hat, muss autodepthstencilformat ein gültiges tiefen Schablone-Format aufweisen.

</dd> <dt>

**Autodepthstencilformat**
</dt> <dd>

Typ: **[D3DFORMAT](d3dformat.md)**

</dd> <dd>

Member des [D3DFORMAT](d3dformat.md) -Enumerationstyps. Das Format der automatischen tiefen Schablone, die vom Gerät erstellt wird. Dieser Member wird ignoriert, es sei denn, **enableautodepthstencil** ist " **true**".

</dd> <dt>

**Flags**
</dt> <dd>

Typ: **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

Eine der [D3DPRESENTFLAG](d3dpresentflag.md) -Konstanten.

</dd> <dt>

**Vollbild- \_ aktuscreenshrateingehz**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die Rate, mit der der Anzeige Adapter den Bildschirm aktualisiert. Der Wert hängt vom Modus ab, in dem die Anwendung ausgeführt wird:

-   Für den Fenstermodus muss die Aktualisierungsrate 0 betragen.
-   Für den Vollbildmodus ist die Aktualisierungsrate einer der von [**enumadaptermodes**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-enumadaptermodes)zurückgegebenen Aktualisierungs Raten.

</dd> <dt>

**Presentationinterval**
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

</dd> <dd>

Die maximale Rate, mit der die Hintergrund Puffer der Swapkette dem Vorder Puffer angezeigt werden können. Eine ausführliche Erläuterung der Modi und der unterstützten Intervalle finden Sie unter [D3DPRESENT](d3dpresent.md).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Strukturen](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[**"Kreatedevice"**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-createdevice)
</dt> <dt>

[**"Kreateadditionalswapchain"**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain)
</dt> <dt>

[**Anzahl**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)
</dt> <dt>

[**Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset)
</dt> </dl>

 

 
