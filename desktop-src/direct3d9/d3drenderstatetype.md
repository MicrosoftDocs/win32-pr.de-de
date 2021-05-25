---
description: Renderzustände definieren Einrichtungszustände für alle Arten der Vertex- und Pixelverarbeitung.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: D3DRENDERSTATETYPE-Enumeration (D3D9Types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343065"
---
# <a name="d3drenderstatetype-enumeration"></a>D3DRENDERSTATETYPE-Enumeration

Renderzustände definieren Einrichtungszustände für alle Arten der Vertex- und Pixelverarbeitung. Einige Renderzustände richten die Scheitelpunktverarbeitung ein, andere richten die Pixelverarbeitung ein (siehe [Renderzustände (Direct3D 9)](render-states.md)). Renderzustände können mit stateblocks gespeichert und wiederhergestellt werden (siehe [Zustandsblöcke Speichern und Wiederherstellen des Zustands (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ ZENABLE**
</dt> <dd>

Tiefenpufferungszustand als member des [**D3DEINANDERUFFERTYPE-Enumerationstyps.**](./d3dzbuffertype.md) Legen Sie diesen Zustand auf D3DFANG \_ TRUE fest, um die Z-Pufferung zu aktivieren, D3DFFE USEW zum Aktivieren der \_ W-Pufferung oder D3DFANG \_ FALSE, um die Tiefenpufferung zu deaktivieren.

Der Standardwert für diesen Renderzustand ist D3DEINANDER \_ TRUE, wenn eine Tiefenschablone zusammen mit der Swapkette erstellt wurde, indem der EnableAutoDepthStencil-Member der [**D3DPRESENT \_ PARAMETERS-Struktur**](d3dpresent-parameters.md) auf **TRUE** festgelegt wurde, andernfalls D3D \_ FALSE.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FILLMODE**
</dt> <dd>

Mindestens ein Member des [**D3DFILLMODE-Enumerationstyps.**](./d3dfillmode.md) Der Standardwert ist D3DFILL \_ SOLID.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Mindestens ein Member des [**D3DSHADEMODE-Enumerationstyps.**](./d3dshademode.md) Der Standardwert ist D3DSHADE \_ GOURAUD.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ ZWRITEENABLE**
</dt> <dd>

**TRUE,** damit die Anwendung in den Tiefenpuffer schreiben kann. Der Standardwert ist **TRUE.** Mit diesem Member kann eine Anwendung verhindern, dass das System den Tiefenpuffer mit neuen Tiefenwerten aktualisiert. False **gibt** an, dass Tiefenvergleiche weiterhin gemäß dem Renderzustand D3DRSUNKUNC vorgenommen werden, vorausgesetzt, dass die Tiefenpufferung stattfindet, aber die Tiefenwerte werden nicht in den Puffer \_ geschrieben.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ ALPHATESTENABLE**
</dt> <dd>

**TRUE,** um Alphatests pro Pixel zu aktivieren. Wenn der Test bestanden wird, wird das Pixel vom Framepuffer verarbeitet. Andernfalls wird die verarbeitung des Framepuffers für das Pixel übersprungen.

Der Test erfolgt durch Vergleichen des eingehenden Alphawerts mit dem Alphawert des Verweises unter Verwendung der Vergleichsfunktion, die vom D3DRS \_ ALPHAFUNC-Renderzustand bereitgestellt wird. Der Alphawert des Verweises wird durch den für D3DRS \_ ALPHAREF festgelegten Wert bestimmt. Weitere Informationen finden Sie unter [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).

Der Standardwert dieses Parameters ist **FALSE.**

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ LASTPIXEL**
</dt> <dd>

Der Standardwert ist **TRUE,** wodurch das Zeichnen des letzten Pixels in einer Linie ermöglicht wird. Um das Zeichnen des letzten Pixels zu verhindern, legen Sie diesen Wert auf **FALSE fest.** Weitere Informationen finden Sie unter [Gliederungs- und Füllzustand (Direct3D 9).](outline-and-fill-state.md)

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ SRCBLEND**
</dt> <dd>

Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md) Der Standardwert ist D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ DESTBLEND**
</dt> <dd>

Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md) Der Standardwert ist D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CULLMODE**
</dt> <dd>

Gibt an, wie rückwärts gerichtete Dreiecke , wenn überhaupt, culled werden. Dieser kann auf einen Member des [**D3DCULL-Enumerationstyps**](./d3dcull.md) festgelegt werden. Der Standardwert ist D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**\_D3DRS–MARKEUNC**
</dt> <dd>

Ein Member des [**D3DCMPFUNC-Enumerationstyps.**](./d3dcmpfunc.md) Der Standardwert ist D3DCMP \_ LESSEQUAL. Mit diesem Member kann eine Anwendung ein Pixel basierend auf seinem Abstand zur Kamera akzeptieren oder ablehnen.

Der Tiefenwert des Pixels wird mit dem Tiefenpufferwert verglichen. Wenn der Tiefenwert des Pixels die Vergleichsfunktion übergibt, wird das Pixel geschrieben.

Der Tiefenwert wird nur in den Tiefenpuffer geschrieben, wenn der Renderzustand **TRUE** ist.

Softwareraster und viele Hardwarebeschleunigungen funktionieren schneller, wenn der Tiefentest fehlschlägt, da die Textur nicht gefiltert und moduliert werden muss, wenn das Pixel nicht gerendert werden soll.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ ALPHAREF**
</dt> <dd>

Wert, der einen Alpha-Verweiswert angibt, für den Pixel getestet werden, wenn Alphatests aktiviert sind. Dies ist ein 8-Bit-Wert, der in den unteren 8 Bits des DWORD-Renderzustandswerts platziert wird. Werte können zwischen 0x00000000 und 0x000000FF liegen. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ ALPHAFUNC**
</dt> <dd>

Ein Member des [**D3DCMPFUNC-Enumerationstyps.**](./d3dcmpfunc.md) Der Standardwert ist D3DCMP \_ ALWAYS. Mit diesem Member kann eine Anwendung ein Pixel basierend auf seinem Alphawert akzeptieren oder ablehnen.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ DITHERENABLE**
</dt> <dd>

**TRUE,** um dithering zu aktivieren. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ ALPHABLENDENABLE**
</dt> <dd>

**TRUE,** um transparenz mit Alphablending zu aktivieren. Der Standardwert ist **FALSE**.

Der Typ des Alphablendings wird durch die Renderzustände D3DRS \_ SRCBLEND und D3DRS \_ DESTBLEND bestimmt.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ – WARTEBAR**
</dt> <dd>

**TRUE,** um blending zu aktivieren. Der Standardwert ist **FALSE**. Weitere Informationen zur Verwendung von Blending finden Sie unter [Überblenden von .](fog.md)

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ SPECULARENABLE**
</dt> <dd>

**TRUE,** um Glanzlichter zu aktivieren. Der Standardwert ist **FALSE**.

Glanzlichter werden so berechnet, als ob sich jeder Scheitelpunkt im objektbelichteten Objekt am Ursprung des Objekts befindet. Dies liefert die erwarteten Ergebnisse, solange das Objekt um den Ursprung herum modelliert wird und der Abstand vom Licht zum Objekt relativ groß ist. In anderen Fällen werden die Ergebnisse als nicht definiert angezeigt.

Wenn dieser Member auf **TRUE festgelegt** ist, wird die Specularfarbe der Basisfarbe nach der Texturkaskade, aber vor dem Alphablending hinzugefügt.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRSCOLOR \_**
</dt> <dd>

Wert, dessen Typ [**D3DCOLOR ist.**](d3dcolor.md) Der Standardwert ist 0. Weitere Informationen zur Farbe des Farbtons finden Sie unter [Farbtonfarbe (Direct3D 9).](fog-color.md)

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ -TABLEMODE**
</dt> <dd>

Die Formel für die Grafik, die für Pixelpixel verwendet werden soll. Legen Sie auf einen der Member des [**aufzählten D3DFOGMODE-Typs**](./d3dfogmode.md) fest. Der Standardwert ist D3DFOG \_ NONE. Weitere Informationen zu Pixelzunge finden Sie unter [Pixel pixel pixels (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS- \_ UND -START**
</dt> <dd>

Tiefe, ab der Pixel- oder Scheitelpunkteffekten für den linearen Linienmodus beginnen. Der Standardwert ist 0,0f. Die Tiefe wird im Weltraum für Scheitelpunkt-Knoten und entweder im Geräteraum \[ 0,0, 1,0 \] oder im Weltraum für Pixelzunge angegeben. Bei Pixelzunge befinden sich diese Werte im Geräteraum, wenn das System z für Berechnungen von Würfen verwendet, und im Raum der Welt, wenn das System augenrelatives Licht (w-eye) verwendet. Weitere Informationen finden Sie unter Parameter für [Metriken (Direct3D 9)](fog-parameters.md) und [Eye-Relative im Vergleich zu Z-basierter Tiefe.](pixel-fog.md)

Werte für diesen Renderzustand sind Gleitkommawerte. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS- \_ UND -END**
</dt> <dd>

Tiefe, bei der Pixel- oder Scheitelpunkteffekten für den linearen Linienmodus enden. Der Standardwert ist 1,0f. Die Tiefe wird im Weltraum für Scheitelpunkt-Knoten und entweder im Geräteraum \[ 0,0, 1,0 \] oder im Weltraum für Pixelzunge angegeben. Bei Pixelzunge befinden sich diese Werte im Geräteraum, wenn das System z für Berechnungen der Fläche verwendet, und im Raum der Welt, wenn das System augen relatives Licht (w-eye) verwendet. Weitere Informationen finden Sie unter Parameter für [Metriken (Direct3D 9)](fog-parameters.md) und [Eye-Relative im Vergleich zu Z-basierter Tiefe.](pixel-fog.md)

Werte für diesen Renderzustand sind Gleitkommawerte. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**\_D3DRS-EMPFINDLICHKEIT**
</dt> <dd>

Die Dichte der Dichte von Pixeln oder Scheitelpunkten, die in den exponentiellen Verzweigungsmodi (D3DFOG \_ EXP und D3DFOG \_ EXP2) verwendet werden. Gültige Dichtewerte liegen zwischen 0,0 und 1,0. Der Standardwert ist 1,0. Weitere Informationen finden Sie unter [Parameters (Direct3D 9)](fog-parameters.md).

Werte für diesen Renderzustand sind Gleitkommawerte. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**TRUE,** um bereichsbasierte Scheitelpunktverschluss zu aktivieren. Der Standardwert ist **FALSE.** In diesem Fall verwendet das System tiefenbasierte Ausfälle. In bereichsbasierten Abständen wird der Abstand eines Objekts vom Viewer verwendet, um Effekten zu berechnen, nicht die Tiefe des Objekts (d. h. die Z-Koordinate) in der Szene. In bereichsbasierten 1:0-Methoden funktionieren alle Methoden wie gewohnt, mit der Ausnahme, dass sie "range" anstelle von "depth" in den Berechnungen verwenden.

Der Bereich ist der richtige Faktor, der für Berechnungsberechnungen verwendet werden kann, aber die Tiefe wird häufig verwendet, da der Bereich zeitaufwändig für die Berechnung ist und die Tiefe allgemein bereits verfügbar ist. Die Verwendung der Tiefe zum Berechnen von Brillen hat den unerwünschten Effekt, dass sich die Freundlichkeit von Peripherieobjekten ändert, wenn sich das Auge des Betrachters bewegt. In diesem Fall ändert sich die Tiefe, und der Bereich bleibt konstant.

Da derzeit keine Hardware bereichsbasierte Spanne pro Pixel unterstützt, wird die Bereichskorrektur nur für Scheitelpunktsyntwinden angeboten.

Weitere Informationen finden Sie unter [Vertex- (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ STENCILENABLE**
</dt> <dd>

**TRUE,** um schablonieren zu aktivieren, oder **FALSE,** um schablonieren zu deaktivieren. Der Standardwert ist **FALSE**. Weitere Informationen finden Sie unter [Schablonenpuffertechniken (Direct3D 9).](stencil-buffer-techniques.md)

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ STENCILFAIL**
</dt> <dd>

Schablonenvorgang, der durchgeführt werden soll, wenn der Schablonentest fehlschlägt. Werte werden vom [**aufzählten D3DSTENCILOP-Typ**](./d3dstencilop.md) verwendet. Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ STENCILZFAIL**
</dt> <dd>

Schablonenvorgang, der ausgeführt werden soll, wenn der Schablonentest erfolgreich war und der Tiefentest (z-test) fehlschlägt. Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md) Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ STENCILPASS**
</dt> <dd>

Schablonenvorgang, der ausgeführt werden soll, wenn sowohl die Schablone als auch die Tiefentests (z) erfolgreich sind. Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md) Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ STENCILFUNC**
</dt> <dd>

Vergleichsfunktion für den Schablonentest. Werte stammen vom [**D3DCMPFUNC-Enumerationstyp.**](./d3dcmpfunc.md) Der Standardwert ist D3DCMP \_ ALWAYS.

Die Vergleichsfunktion wird verwendet, um den Verweiswert mit einem Schablonenpuffereintrag zu vergleichen. Dieser Vergleich gilt nur für die Bits im Verweiswert und den Schablonenpuffereintrag, die in der Schablonenmaske festgelegt sind (festgelegt durch den \_ D3DRS-STENCILMASK-Renderzustand). True gibt an, dass der Schablonentest erfolgreich ist.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ STENCILREF**
</dt> <dd>

Ein int-Verweiswert für den Schablonentest. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ STENCILMASK**
</dt> <dd>

Maske, die auf den Verweiswert und jeden Schablonenpuffereintrag angewendet wird, um die signifikanten Bits für den Schablonentest zu bestimmen. Die Standardmaske ist 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ STENCILWRITEMASK**
</dt> <dd>

Schreibmaske, die auf Werte angewendet wird, die in den Schablonenpuffer geschrieben werden. Die Standardmaske ist 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TEXTUREFACTOR**
</dt> <dd>

Farbe, die für das Mischen mehrerer Texturen mit dem D3DTA \_ TFACTOR-Texturmischungsargument oder dem D3DTOP \_ BLENDFACTORALPHA-Texturmischungsvorgang verwendet wird. Der zugeordnete Wert ist eine [**D3DCOLOR-Variable.**](d3dcolor.md) Der Standardwert ist nicht transparent weiß (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Texturumbruchverhalten für mehrere Sätze von Texturkoordinaten. Gültige Werte für diesen Renderzustand können eine beliebige Kombination der Flags D3DWRAPCOORD \_ 0 (oder D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (oder D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (oder D3DWRAP W) und \_ D3DWRAPCOORD \_ 3 sein. Diese bewirken, dass das System in Richtung der ersten, zweiten, dritten und vierten Dimension, manchmal auch als s-, t-, r- und q-Richtung bezeichnet, für eine bestimmte Textur umschließt. Der Standardwert für diesen Renderzustand ist 0 (umschließen in alle Richtungen deaktiviert).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ CLIPPING**
</dt> <dd>

**TRUE,** um primitives Clipping durch Direct3D zu aktivieren, oder **FALSE,** um es zu deaktivieren. Der Standardwert ist **TRUE.**

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_D3DRS-BELEUCHTUNG**
</dt> <dd>

**TRUE,** um direct3D-Beleuchtung zu aktivieren, oder **FALSE,** um sie zu deaktivieren. Der Standardwert ist **TRUE.** Nur Scheitelpunkte, die einen Scheitelpunkt normal enthalten, werden ordnungsgemäß ausgelichtet. Scheitelpunkte, die kein normales enthalten, verwenden in allen Beleuchtungsberechnungen ein Punktprodukt von 0.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**
</dt> <dd>

Umgebungslichtfarbe. Dieser Wert ist vom Typ [**D3DCOLOR.**](d3dcolor.md) Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**\_D3DRS-VERTEXMODE**
</dt> <dd>

Formel für Die Formel, die für Scheitelpunkt-Scheitelpunkte verwendet werden soll. Legen Sie auf einen Member des [**D3DFOGMODE-Enumerationstyps**](./d3dfogmode.md) fest. Der Standardwert ist D3DFOG \_ NONE.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ COLORVERTEX**
</dt> <dd>

**TRUE,** um die Farbe pro Scheitelpunkt zu aktivieren, oder **FALSE,** um sie zu deaktivieren. Der Standardwert ist **TRUE.** Wenn Sie die Farbe pro Scheitelpunkt aktivieren, kann das System die für einzelne Scheitelpunkte definierte Farbe in seine Beleuchtungsberechnungen einplanen.

Weitere Informationen finden Sie in den folgenden Renderzuständen:

-   D3DRS \_ DIFFUSEMATERIALSOURCE
-   D3DRS \_ SPECULARMATERIALSOURCE
-   D3DRS \_ AMBIENTMATERIALSOURCE
-   D3DRS- \_ UND SIVEMATERIALSOURCE

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ LOCALVIEWER**
</dt> <dd>

**TRUE,** um kamera relative Glanzlichter zu aktivieren, oder **FALSE,** um orthogonale Glanzlichter zu verwenden. Der Standardwert ist **TRUE.** Anwendungen, die die orthogonale Projektion verwenden, sollten **FALSE angeben.**

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ NORMALIZENORMALS**
</dt> <dd>

**TRUE,** um die automatische Normalisierung von Scheitelpunktnormals zu aktivieren, oder **FALSE,** um sie zu deaktivieren. Der Standardwert ist **FALSE**. Die Aktivierung dieses Features bewirkt, dass das System die Scheitelpunktnorm normalisiert, nachdem sie in den Kameraraum transformiert wurden, was rechenintensiv sein kann.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DIFFUSEMATERIALSOURCE**
</dt> <dd>

Diffuse Farbquelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**aufzählten D3DMATERIALCOLORSOURCE-Typs.**](./d3dmaterialcolorsource.md) Der Standardwert ist D3DMCS \_ COLOR1. Der Wert für diesen Renderzustand wird nur verwendet, wenn der D3DRS \_ COLORVERTEX-Renderzustand auf TRUE festgelegt **ist.**

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SPECULARMATERIALSOURCE**
</dt> <dd>

Glanzfarbenquelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md) Der Standardwert ist D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AMBIENTMATERIALSOURCE**
</dt> <dd>

Umgebungsfarbquelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md) Der Standardwert ist D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ EMISSIVEMATERIALSOURCE**
</dt> <dd>

Eine freizügige Farbquelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE-Enumerationstyps.**](./d3dmaterialcolorsource.md) Der Standardwert ist D3DMCS \_ MATERIAL.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ VERTEXBLEND**
</dt> <dd>

Anzahl von Matrizen, die zum Durchführen von Geometrieblending verwendet werden sollen( falls vorhanden). Gültige Werte sind Member des [**D3DVERTEXBLENDFLAGS-Enumerationstyps.**](./d3dvertexblendflags.md) Der Standardwert ist D3DVBF \_ DISABLE.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ CLIPPLANEENABLE**
</dt> <dd>

Aktiviert oder deaktiviert benutzerdefinierte Clippingebenen. Gültige Werte sind alle DWORD-Werte, bei denen der Status jedes Bits (festgelegt oder nicht festgelegt) den Aktivierungszustand einer entsprechenden benutzerdefinierten Clippingebene umschaltet. Das am wenigsten signifikante Bit (Bit 0) steuert die erste Clippingebene bei Index 0, und nachfolgende Bits steuern die Aktivierung von Clippingebenen bei höheren Indizes. Wenn ein Bit festgelegt ist, wendet das System während des Szenenrenderings die entsprechende Clippingebene an. Der Standardwert ist 0.

Die [**D3DCLIPPLANEn-Makros**](d3dclipplanen.md) sind definiert, um eine bequeme Möglichkeit zum Aktivieren von Clippingebenen zu bieten.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**
</dt> <dd>

Ein float-Wert, der die Größe angibt, die für die Berechnung der Punktgröße in Fällen verwendet werden soll, in denen die Punktgröße nicht für jeden Scheitelpunkt angegeben ist. Dieser Wert wird nicht verwendet, wenn der Scheitelpunkt punktgröße enthält. Dieser Wert befindet sich in Bildschirmbereichseinheiten, wenn D3DRS \_ POINTSCALEENABLE **auf FALSE** festgelegt ist; andernfalls ist dieser Wert in Weltraumeinheiten. Der Standardwert ist der Wert, den ein Treiber zurückgibt. Wenn ein Treiber 0 oder 1 zurückgibt, ist der Standardwert 64, was eine Emulation der Softwarepunktgröße zulässt. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ MIN**
</dt> <dd>

Ein float-Wert, der die Mindestgröße von Punktprimitiven angibt. Punktprimitiven werden während des Renderings an diese Größe klammern. Wenn sie auf Werte kleiner als 1,0 festlegen, werden Punkte entfernt, wenn der Punkt keinen Pixelmittelpunkt verdeckt und Antialiasing deaktiviert oder mit geringerer Intensität gerendert wird, wenn Antialiasing aktiviert ist. Der Standardwert ist 1,0f. Der Bereich für diesen Wert ist größer oder gleich 0,0f. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ POINTSPRITEENABLE**
</dt> <dd>

bool-Wert. True **gibt** an, dass Texturkoordinaten von Punktprimitiven so festgelegt werden, dass vollständige Texturen auf jedem Punkt zugeordnet werden. False **gibt** an, dass die Scheitelpunkttexturkoordinaten für den gesamten Punkt verwendet werden. Der Standardwert ist **FALSE**. Sie können DirectX 7-Stilpunkte im Einzelpixelformat erreichen, indem Sie D3DRS \_ POINTSCALEENABLE auf **FALSE** und D3DRS \_ POINTSIZE auf 1.0 festlegen. Dies sind die Standardwerte.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ POINTSCALEENABLE**
</dt> <dd>

bool-Wert, der die Berechnung der Größe für Punktprimitive steuert. True gibt an, dass die Punktgröße als Kameraraumwert interpretiert wird und von der Distance-Funktion und dem Frustum zum Skalieren der Viewport-y-Achse skaliert wird, um die endgültige Bildschirmbereichspunktgröße zu berechnen. False gibt an, dass die Punktgröße als Bildschirmbereich interpretiert und direkt verwendet wird. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ POINTSCALE \_ A**
</dt> <dd>

Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert. Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist. Der Standardwert ist 1,0f. Der Bereich für diesen Wert ist größer oder gleich 0,0f. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ POINTSCALE \_ B**
</dt> <dd>

Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert. Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist. Der Standardwert ist 0,0f. Der Bereich für diesen Wert ist größer oder gleich 0,0f. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ POINTSCALE \_ C**
</dt> <dd>

Ein float-Wert, der die abstandsbasierte Größendämpfung für Punktprimitive steuert. Nur aktiv, wenn D3DRS \_ POINTSCALEENABLE **TRUE** ist. Der Standardwert ist 0,0f. Der Bereich für diesen Wert ist größer oder gleich 0,0f. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ MULTISAMPLEANTIALIAS**
</dt> <dd>

bool-Wert, der bestimmt, wie einzelne Stichproben berechnet werden, wenn ein Multisample-Renderzielpuffer verwendet wird. Wenn dies **auf TRUE** festgelegt ist, werden die mehreren Stichproben berechnet, sodass das Antialiasing in der gesamten Szene durch Stichprobenentnahme an verschiedenen Beispielpositionen für jede stichprobebasierte Stichprobe durchgeführt wird. Wenn diese Option auf **FALSE** festgelegt ist, werden die verschiedenen Stichproben alle mit demselben Beispielwert geschrieben, der in der Pixelmitte entnommen wird, wodurch nicht antialiasiertes Rendering in einen Multisamplepuffer ermöglicht wird. Dieser Renderzustand hat keine Auswirkungen beim Rendern in einen einzelnen Beispielpuffer. Der Standardwert ist **TRUE.**

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ MULTISAMPLEMASK**
</dt> <dd>

Jedes Bit in dieser Maske, beginnend mit dem am wenigsten signifikanten Bit (LSB), steuert die Änderung eines der Beispiele in einem Multisample-Renderziel. Daher enthält das untere Byte für ein Renderziel mit acht Stichproben die acht Schreibberechtigungen für jede der acht Stichproben. Dieser Renderzustand hat keine Auswirkungen beim Rendern in einen einzelnen Beispielpuffer. Der Standardwert ist 0xFFFFFFFF.

Dieser Renderzustand ermöglicht die Verwendung eines Multisamplepuffers als Akkumulationspuffer, wobei multipass-Rendering der Geometrie durchgeführt wird, wobei jeder Durchlauf eine Teilmenge von Stichproben aktualisiert.

Wenn es n Multisamples und k aktivierte Stichproben gibt, sollte die resultierende Intensität des gerenderten Bilds k/n sein. Jede Komponente RGB jedes Pixels wird durch k/n faktor.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ PATCHEDGESTYLE**
</dt> <dd>

Legt fest, ob Patchränder das Mosaik im Float-Stil verwenden. Mögliche Werte werden durch den [**aufzählten D3DPATCHEDGESTYLE-Typ**](./d3dpatchedgestyle.md) definiert. Der Standardwert ist D3DPATCHEDGE \_ DISCRETE.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ DEBUGMONITORTOKEN**
</dt> <dd>

Legen Sie nur für das Debuggen des Monitors fest. Mögliche Werte werden durch den [**D3DDEBUGMONITORTOKENS-Enumerationstyp**](./d3ddebugmonitortokens.md) definiert. Beachten Sie Folgendes: Wenn D3DRS \_ DEBUGMONITORTOKEN festgelegt ist, wird der Aufruf als Übergabe eines Tokens an den Debugmonitor behandelt. Wenn beispielsweise – nach der Übergabe von D3DDMT \_ ENABLE oder D3DDMT \_ DISABLE an D3DRS \_ DEBUGMONITORTOKEN – andere Tokenwerte übergeben werden, bleibt der Zustand (aktiviert oder deaktiviert) des Debugmonitors erhalten.

Dieser Zustand ist nur für Debugbuilds nützlich. Der Debugmonitor ist standardmäßig auf D3DDMT \_ ENABLE eingestellt.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ MAX**
</dt> <dd>

Ein float-Wert, der die maximale Größe angibt, bis zu der Punkt-Sprites klammern werden. Der Wert muss kleiner oder gleich dem MaxPointSize-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) und größer oder gleich D3DRS \_ POINTSIZE \_ MIN sein. Der Standardwert ist 64,0. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable mit dem Wert wandeln, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ INDEXEDVERTEXBLENDENABLE**
</dt> <dd>

bool-Wert, der indizierte Vertexmischung aktiviert oder deaktiviert. Der Standardwert ist **FALSE**. Wenn auf **TRUE** festgelegt ist, ist die vertexvermischung indiziert aktiviert. Wenn **false** festgelegt ist, ist die indizierte Scheitelpunktmischung deaktiviert. Wenn dieser Renderzustand aktiviert ist, muss der Benutzer Matrixindizes als gepacktes DWORD mit jedem Scheitelpunkt übergeben. Wenn der Renderzustand deaktiviert ist und vertex blending über den D3DRS \_ VERTEXBLEND-Zustand aktiviert ist, entspricht dies matrixindizes 0, 1, 2, 3 in jedem Scheitelpunkt.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ COLORWRITEENABLE**
</dt> <dd>

UINT-Wert, der einen kanalbezogenen Schreibvorgang für den Renderzielfarbpuffer ermöglicht. Ein festgelegtes Bit führt zu einer Aktualisierung des Farbkanals während des 3D-Renderings. Ein klares Bit führt zu einer Nichtbeeinflussung des Farbkanals. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ COLORWRITEENABLE-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist. Dieser Renderzustand wirkt sich nicht auf den Clear-Vorgang aus. Der Standardwert ist 0x0000000F.

Gültige Werte für diesen Renderzustand können eine beliebige Kombination der Flags D3DCOLORWRITEENABLE \_ ALPHA, D3DCOLORWRITEENABLE \_ BLUE, D3DCOLORWRITEENABLE GREEN oder \_ D3DCOLORWRITEENABLE \_ RED sein.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ TWEENFACTOR**
</dt> <dd>

Ein float-Wert, der den Tweenfaktor steuert. Der Standardwert ist 0,0f. Da die [**IDirect3DDevice9::SetRenderState-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable, die den Wert enthält, wie im folgenden Codebeispiel gezeigt, casten.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ BLENDOP**
</dt> <dd>

Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die angewendet wird, wenn der Alphablending-Renderzustand D3DRS \_ ALPHABLENDENABLE auf TRUE festgelegt **ist.** Gültige Werte werden durch den [**aufzählten D3DBLENDOP-Typ**](./d3dblendop.md) definiert. Der Standardwert ist D3DBLENDOP \_ ADD.

Wenn die D3DPMISCCAPS BLENDOP-Gerätefunktion nicht \_ unterstützt wird, wird D3DBLENDOP \_ ADD ausgeführt.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ POSITIONDEGREE**
</dt> <dd>

N-Patchpositionsinterpolationsgrad. Die Werte können D3DDEGREE \_ CUBIC (Standard) oder D3DDEGREE \_ LINEAR sein. Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ NORMALDEGREE**
</dt> <dd>

N-Patch Normal Interpolation Degree. Die Werte können D3DDEGREE \_ LINEAR (Standard) oder D3DDEGREE \_ QUADRATIC sein. Weitere Informationen finden Sie unter [**D3DDEGREETYPE.**](./d3ddegreetype.md)

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ SCISSORTESTENABLE**
</dt> <dd>

**TRUE** zum Aktivieren von Scissortests und **FALSE** zum Deaktivieren. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ IM 3DRS-REGLERCALEDEPTHBIAS**
</dt> <dd>

Wird verwendet, um zu bestimmen, wie viel Voreingenommenheit auf co-planare Primitive angewendet werden kann, um Z-Fighting zu reduzieren. Der Standardwert ist 0.

bias = \* (max. D3DRS \_ VERALTUNGSEDEPTHBIAS) + D3DRS \_ DEPTHBIAS.

dabei ist max die maximale Tiefenpiste des gerenderten Dreiecks.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ ANTIALIASEDLINEENABLE**
</dt> <dd>

**TRUE** zum Aktivieren von Zeilen antialiasing, **FALSE** zum Deaktivieren von Zeilen antialiasing. Der Standardwert ist **FALSE**.

Beim Rendern in ein Multisample-Renderziel wird D3DRS \_ ANTIALIASEDLINEENABLE ignoriert, und alle Zeilen werden als Alias gerendert. Verwenden Sie [**ID3DXLine**](id3dxline.md) für antialiasiertes Zeilenrendering in einem Multisample-Renderziel.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ MINTESSELLATIONLEVEL**
</dt> <dd>

Minimale Mosaikebene. Der Standardwert ist 1,0f. Siehe [Mosaik (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ MAXTESSELLATIONLEVEL**
</dt> <dd>

Maximale Mosaikebene. Der Standardwert ist 1,0f. Weitere [Informationen finden Sie unter Mosaik (Direct3D 9).](tessellation.md)

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ ADAPTIVETESS \_ X**
</dt> <dd>

Betrag bis zum adaptiven Mosaik in x-Richtung. Der Standardwert ist 0,0f. Weitere Informationen [finden Sie unter Adaptive Mosaik](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ ADAPTIVETESS \_ Y**
</dt> <dd>

Betrag bis zum adaptiven Mosaik in y-Richtung. Der Standardwert ist 0,0f. Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ ADAPTIVETESS \_ Z**
</dt> <dd>

Betrag bis zum adaptiven Mosaik in z-Richtung. Der Standardwert ist 1,0f. Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ ADAPTIVETESS \_ W**
</dt> <dd>

Betrag bis zum adaptiven Mosaik in w-Richtung. Der Standardwert ist 0,0f. Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ ENABLEADAPTIVETESSELLATION**
</dt> <dd>

**TRUE,** um das adaptive Mosaik zu aktivieren, **FALSE,** um es zu deaktivieren. Der Standardwert ist **FALSE**. Weitere Informationen [finden Sie unter Adaptive \_ Mosaik](tessellation.md).

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ TWOSIDEDSTENCILMODE**
</dt> <dd>

**TRUE** aktiviert die zweiseitige Schablonierung, **FALSE** deaktiviert sie. Der Standardwert ist **FALSE**. Die Anwendung sollte D3DRS \_ CULLMODE auf D3DCULL \_ NONE festlegen, um den zweiseitigen Schablonenmodus zu aktivieren. Wenn die Dreieckswindungsreihenfolge im Uhrzeigersinn erfolgt, werden die \_ D3DRS-STENCIL-Vorgänge \* verwendet. Wenn die Ziehreihenfolge gegen den Uhrzeigersinn lautet, werden die D3DRS \_ \_ CCW-STENCIL-Vorgänge \* verwendet.

Überprüfen Sie den StencilCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für D3DSTENCILCAPS TWOSIDED, um festzustellen, ob die zweiseitige Schablone unterstützt \_ wird. Siehe auch [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ STENCILFAIL**
</dt> <dd>

Schablonenvorgang, der ausgeführt werden soll, wenn der CCW-Schablonentest fehlschlägt. Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md) Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ STENCILZFAIL**
</dt> <dd>

Schablonenvorgang, der ausgeführt werden soll, wenn der CCW-Schablonentest erfolgreich war und z-test fehlschlägt. Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md) Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ STENCILPASS**
</dt> <dd>

Schablonenvorgang, der ausgeführt werden soll, wenn sowohl CCW-Schablone als auch Z-Tests erfolgreich sind. Werte stammen vom [**D3DSTENCILOP-Enumerationstyp.**](./d3dstencilop.md) Der Standardwert ist D3DSTENCILOP \_ KEEP.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ STENCILFUNC**
</dt> <dd>

Die Vergleichsfunktion. Der CCW-Schablonentest besteht, wenn die Schablonenfunktion ((ref & mask) (Schablonen- & maske)) **TRUE ist.** Werte werden vom [**aufzählten D3DCMPFUNC-Typ**](./d3dcmpfunc.md) verwendet. Der Standardwert ist D3DCMP \_ ALWAYS.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Zusätzliche ColorWriteEnable-Werte für die Geräte. Siehe D3DRS \_ COLORWRITEENABLE. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Zusätzliche ColorWriteEnable-Werte für die Geräte. Siehe D3DRS \_ COLORWRITEENABLE. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Zusätzliche ColorWriteEnable-Werte für die Geräte. Siehe D3DRS \_ COLORWRITEENABLE. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ INDEPENDENTWRITEMASKS-Funktionsbit im PrimitiveMiscCaps-Member der [**D3DCAPS9-Struktur**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ BLENDFACTOR**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) wird für einen konstanten Mischungsfaktor während der Alphamischung verwendet. Diese Funktionalität ist verfügbar, wenn das D3DPBLENDCAPS \_ BLENDFACTOR-Funktionsbit im SrcBlendCaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder im DestBlendCaps-Member von **D3DCAPS9** festgelegt ist. Siehe [**D3DRENDERSTATETYPE.**]() Der Standardwert ist 0xffffffff.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ SRGBWRITEENABLE**
</dt> <dd>

Aktivieren Sie render-target-Schreibvorgänge, damit gamma in sRGB korrigiert wird. Das Format muss D3DUSAGE \_ SRGBWRITE verfügbar machen. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ DEPTHBIAS**
</dt> <dd>

Ein Gleitkommawert, der für den Vergleich von Tiefenwerten verwendet wird. Weitere Informationen finden Sie unter [Tiefenabweichung (Direct3D 9).](depth-bias.md) Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

Siehe D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ SEPARATEALPHABLENDENABLE**
</dt> <dd>

**TRUE** aktiviert den separaten Überblendmodus für den Alphakanal. Der Standardwert ist **FALSE**.

Wenn false festgelegt **ist,** müssen die auf alpha angewendeten Renderzielblendingfaktoren und -vorgänge mit denen identisch sein, die für die Farbe definiert sind. Dieser Modus wird bei  Implementierungen, die die Obergrenze D3DPMISCCAPS SEPARATEALPHABLEND nicht festlegen, effektiv auf \_ FALSE festgelegt. Siehe [D3DPMISCCAPS](d3dpmisccaps.md).

Der Typ des separaten Alphablendings wird durch die Renderzustände D3DRS \_ SRCBLENDALPHA und D3DRS \_ DESTBLENDALPHA bestimmt.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ SRCBLENDALPHA**
</dt> <dd>

Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md) Dieser Wert wird ignoriert, es sei denn, D3DRS \_ SEPARATEALPHABLENDENABLE ist **TRUE.** Der Standardwert ist D3DBLEND \_ ONE.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ DESTBLENDALPHA**
</dt> <dd>

Ein Member des [**aufzählten D3DBLEND-Typs.**](./d3dblend.md) Dieser Wert wird ignoriert, es sei denn, D3DRS \_ SEPARATEALPHABLENDENABLE ist **TRUE.** Der Standardwert ist D3DBLEND \_ ZERO.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ BLENDOPALPHA**
</dt> <dd>

Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die auf separate Alphamischung angewendet wird, wenn der Renderzustand D3DRS \_ SEPARATEALPHABLENDENABLE auf **TRUE** festgelegt ist.

Gültige Werte werden vom [**D3DBLENDOP-Enumerationstyp**](./d3dblendop.md) definiert. Der Standardwert ist D3DBLENDOP \_ ADD.

Wenn die D3DPMISCCAPS \_ BLENDOP-Gerätefunktion nicht unterstützt wird, wird D3DBLENDOP \_ ADD ausgeführt. Siehe [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ FORCE \_ DWORD**
</dt> <dd>

Erzwingt, dass diese Enumeration in eine Größe von 32 Bits kompiliert wird. Ohne diesen Wert würden einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise



| Renderzustände        |   Textur-Sampler                 |
|----------------------|--------------------|
| ps \_ 1 \_ 1 bis ps \_ 1 \_ 3 | 4 Textur-Sampler |



 

Direct3D definiert die D3DRENDERSTATE \_ WRAPBIAS-Konstante, um Anwendungen das Aktivieren oder Deaktivieren des Texturumbruchs basierend auf der nullbasierten ganzen Zahl eines Texturkoordinatensatzes zu ermöglichen (anstatt explizit einen der D3DRS \_ WRAP n-Zustandswerte zu verwenden). Fügen Sie den D3DRENDERSTATE \_ WRAPBIAS-Wert dem nullbasierten Index eines Texturkoordinatensatzes hinzu, um den D3DRS \_ WRAP n-Wert zu berechnen, der diesem Index entspricht, wie im folgenden Beispiel gezeigt.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
