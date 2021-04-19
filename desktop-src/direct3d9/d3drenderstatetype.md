---
description: Renderzustände definieren Setup Zustände für alle Arten von Vertex-und Pixel Verarbeitung.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: D3DRENDERSTATETYPE-Enumeration (D3D9Types. h)
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
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353704"
---
# <a name="d3drenderstatetype-enumeration"></a>D3DRENDERSTATETYPE-Enumeration

Renderzustände definieren Setup Zustände für alle Arten von Vertex-und Pixel Verarbeitung. Einige renderzustände richten die Vertexverarbeitung ein, und einige einrichten die Pixel Verarbeitung (siehe [renderzustände (Direct3D 9)](render-states.md)). Renderzustände können mithilfe von stateblocks gespeichert und wieder hergestellt werden (siehe [Status Blöcke speichern und Wiederherstellen (Direct3D 9)](state-blocks-save-and-restore-state.md)).

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

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ zenable**
</dt> <dd>

Der tiefen Puffer Zustand als ein Member des [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) -enumerierten Typs. Legen Sie diesen Status auf D3DZB true fest, \_ um z-Pufferung zu aktivieren, D3DZB \_ usew, um w-buffereing zu aktivieren, oder D3DZB \_ false, um die tiefen Pufferung zu deaktivieren.

Der Standardwert für diesen renderzustand ist D3DZB \_ true, wenn eine tiefen Schablone zusammen mit der SwapChain erstellt wurde, indem der enableautodepthstencil-Member der [**D3DPRESENT \_ Parameters**](d3dpresent-parameters.md) -Struktur auf **true** festgelegt wurde, \_ andernfalls D3DZB false.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ FillMode**
</dt> <dd>

Mindestens ein Member des [**D3DFILLMODE**](./d3dfillmode.md) -Enumerationstyps. Der Standardwert ist D3DFILL \_ Solid.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ SHADEMODE**
</dt> <dd>

Mindestens ein Member des [**D3DSHADEMODE**](./d3dshademode.md) -Enumerationstyps. Der Standardwert ist D3DSHADE \_ Gouraud.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ zbeschreib teenable**
</dt> <dd>

**True** , wenn die Anwendung in den tiefen Puffer schreiben soll. Der Standardwert ist " **true**". Mit diesem Member kann eine Anwendung verhindern, dass das System den tiefen Puffer mit neuen tiefen Werten aktualisiert. **False** gibt an, dass tiefe Vergleiche weiterhin gemäß dem \_ renderzustand D3DRS zfunc erfolgen, vorausgesetzt, dass die tiefen Pufferung stattfindet, aber keine tiefen Werte in den Puffer geschrieben werden.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ Alpha atestenable**
</dt> <dd>

**True** , um pro Pixel-Alpha Tests zu aktivieren. Wenn der Test durchlaufen wird, wird das Pixel vom Frame Puffer verarbeitet. Andernfalls wird die gesamte Verarbeitung des Frame Puffers für das Pixel übersprungen.

Der Test wird durchgeführt, indem der eingehende Alpha-Wert mit dem Reference-Alpha-Wert verglichen wird, wobei die Vergleichsfunktion des D3DRS \_ alphafunc-gerengerstatus verwendet wird. Der Reference Alpha-Wert wird durch den Wert bestimmt, der für D3DRS \_ Alpha Aref festgelegt ist. Weitere Informationen finden Sie unter [Status des Alpha Tests (Direct3D 9)](alpha-testing-state.md).

Der Standardwert dieses Parameters ist **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ lastpixel**
</dt> <dd>

Der Standardwert ist **true**, wodurch das Zeichnen des letzten Pixels in einer Zeile ermöglicht wird. Legen Sie diesen Wert auf **false** fest, um das Zeichnen des letzten Pixels zu verhindern. Weitere Informationen finden Sie Untergliederung [und Füll Zustand (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ srcblend**
</dt> <dd>

Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps. Der Standardwert ist D3DBLEND \_ 1.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ destblend**
</dt> <dd>

Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps. Der Standardwert ist D3DBLEND \_ 0 (null).

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ CullMode**
</dt> <dd>

Gibt an, wie rückwärts gerichtete Dreiecke durchgeführt werden, wenn überhaupt. Dies kann auf einen Member des [**D3DCULL**](./d3dcull.md) -enumerierten Typs festgelegt werden. Der Standardwert ist D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ zfunc**
</dt> <dd>

Ein Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyps. Der Standardwert ist D3DCMP \_ lessequal. Dieser Member ermöglicht es einer Anwendung, ein Pixel basierend auf der Entfernung von der Kamera zu akzeptieren oder abzulehnen.

Der tiefen Wert des Pixels wird mit dem tiefen Puffer Wert verglichen. Wenn der tiefen Wert des Pixels die Vergleichsfunktion übergibt, wird das Pixel geschrieben.

Der tiefen Wert wird nur in den tiefen Puffer geschrieben, wenn der renderzustand " **true**" ist.

Software Rasterizer und viele Hardware Accelerators arbeiten schneller, wenn der tiefen Test fehlschlägt, da die Textur nicht gefiltert und modulieren werden muss, wenn das Pixel nicht gerendert wird.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ Alpha Aref**
</dt> <dd>

Ein Wert, der einen Alpha-Verweiswert angibt, mit dem Pixel getestet werden, wenn Alpha Tests aktiviert werden. Dabei handelt es sich um einen 8-Bit-Wert, der in die unteren 8 Bits des DWORD-Rendering-State-Werts eingefügt wird. Die Werte liegen im Bereich von 0x00000000 bis 0x000000ff. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ alphafunc**
</dt> <dd>

Ein Member des [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyps. Der Standardwert ist D3DCMP \_ Always. Dieser Member ermöglicht es einer Anwendung, ein Pixel auf der Grundlage des Alphawerts zu akzeptieren oder abzulehnen.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ ditherenable**
</dt> <dd>

**True** , um Dithering zu aktivieren. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ AlphaBlendEnable**
</dt> <dd>

" **True** ", um eine Alpha Gemischte Transparenz zu aktivieren. Der Standardwert ist **FALSE**.

Der Typ der Alpha Mischung wird durch die D3DRS \_ srcblend-und D3DRS \_ destblend-Rendering-Zustände bestimmt.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ fogenable**
</dt> <dd>

**True** , um eine Nebel Mischung zu aktivieren. Der Standardwert ist **FALSE**. Weitere Informationen zur Verwendung der Nebel Mischung finden Sie unter [Nebel](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ specularenable**
</dt> <dd>

**True** , um Glanzlichter zu aktivieren. Der Standardwert ist **FALSE**.

Glanzlichter werden berechnet, als wäre jeder Scheitelpunkt in dem Objekt, das beleuchtet wird, am Ursprung des Objekts. Dadurch werden die erwarteten Ergebnisse generiert, solange das Objekt um den Ursprung modelliert wird und der Abstand vom Licht zum Objekt relativ groß ist. In anderen Fällen sind die Ergebnisse als nicht definiert.

Wenn dieser Member auf **true** festgelegt ist, wird die Glanz Farbe der Basis Farbe nach der Textur kaskadierenden, aber vor dem Alpha Blending hinzugefügt.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ fogcolor**
</dt> <dd>

Der Wert, dessen Typ " [**D3DCOLOR**](d3dcolor.md)" ist. Der Standardwert ist 0. Weitere Informationen zur Nebelfarbe finden Sie unter [Nebelfarbe (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ fogtablemode**
</dt> <dd>

Die für den Pixel Nebel zu verwendende Nebelformel. Legen Sie auf einen der Member des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps fest. Der Standardwert ist D3DFOG \_ None. Weitere Informationen zu Pixel Nebel finden Sie unter [Pixel Nebel (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ fogstart**
</dt> <dd>

Die Tiefe, bei der Pixel-oder Scheitelpunkt Effekte für den linearen Nebel Modus beginnen. Der Standardwert ist 0,0 f. Die Tiefe wird im Welt Raum für den Scheitelpunkt Nebel und entweder den Geräteraum \[ 0,0, 1,0 \] oder den Raum für den Pixel Nebel angegeben. Bei Pixel Nebel befinden sich diese Werte im Geräteraum, wenn das System z für Nebel Berechnungen und weltweiten Raum verwendet, wenn das System den Augen relativen Nebel (w-Fog) verwendet. Weitere Informationen finden Sie unter [Nebel Parameter (Direct3D 9)](fog-parameters.md) und [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md).

Werte für diesen Rendering-Zustand sind Gleit Komma Werte. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ fogend**
</dt> <dd>

Die Tiefe, bei der Pixel-oder Scheitelpunkt Effekte für den linearen Nebel Modus enden. Der Standardwert ist 1.0 f. Die Tiefe wird im Welt Raum für den Scheitelpunkt Nebel und entweder den Geräteraum \[ 0,0, 1,0 \] oder den Raum für den Pixel Nebel angegeben. Bei Pixel Nebel befinden sich diese Werte im Geräteraum, wenn das System z für Nebel Berechnungen und in Welt Raum verwendet, wenn das System den Augen relativen Nebel (w-Fog) verwendet. Weitere Informationen finden Sie unter [Nebel Parameter (Direct3D 9)](fog-parameters.md) und [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md).

Werte für diesen Rendering-Zustand sind Gleit Komma Werte. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS- \_ fogdensity**
</dt> <dd>

In den exponentialnebelmodi (D3DFOG \_ exp und D3DFOG exp2) verwendete Nebeldichte für Pixel-oder Vertexnebel \_ . Gültige Dichte Werte liegen zwischen 0,0 und 1,0. Der Standardwert ist 1,0. Weitere Informationen finden Sie unter " [Fog Parameters" (Direct3D 9)](fog-parameters.md).

Werte für diesen Rendering-Zustand sind Gleit Komma Werte. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ RANGEFOGENABLE**
</dt> <dd>

**True** , um Bereichs basierten Scheitelpunkt Nebel zu aktivieren. Der Standardwert ist **false**. in diesem Fall verwendet das System tiefen basierten Nebel. Im Bereichs basierten Nebel wird der Abstand eines Objekts vom Viewer zum Berechnen von Nebeleffekten verwendet, nicht die Tiefe des Objekts (d. h. die z-Koordinate) in der Szene. Im Bereichs basierten Nebel funktionieren alle Nebel Methoden wie üblich, mit dem Unterschied, dass Sie in den Berechnungen den Bereich anstelle von Tiefe verwenden.

Range ist der richtige Faktor für die Berechnung von Nebel Berechnungen, aber die Tiefe wird häufig verwendet, da Range zeitaufwändig ist, und Tiefe ist im allgemeinen bereits verfügbar. Die Verwendung der Tiefe zur Berechnung von Nebel hat den unerwünschten Effekt, dass sich das fogginess von peripheren Objekten ändert, wenn der Viewer das Auge bewegt. in diesem Fall werden die tiefen Änderungen und der Bereich konstant bleiben.

Da derzeit keine Hardware den Bereichs basierten Nebel pro Pixel unterstützt, wird die Bereichs Korrektur nur für Scheitel Punkte angezeigt.

Weitere Informationen finden Sie unter [Scheitelpunkt Nebel (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ Schablone**
</dt> <dd>

**True** zum Aktivieren der Schablone oder **false** zum Deaktivieren der Schablone. Der Standardwert ist **FALSE**. Weitere Informationen finden Sie unter [Schablonen Puffer Techniken (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ stencilfail**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn der Schablonen Test fehlschlägt. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ stencilzfail**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn der Schablone-Test erfolgreich verläuft und der tiefen Test (z-Test) fehlschlägt. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ stencilpass**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn sowohl die Schablone als auch die Tiefe (z)-Tests bestanden werden. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ stencilfunc**
</dt> <dd>

Vergleichsfunktion für den Schablonen Test. Werte stammen aus dem [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyp. Der Standardwert ist D3DCMP \_ Always.

Die Vergleichsfunktion wird verwendet, um den Verweis Wert mit einem Schablone-Puffer Eintrag zu vergleichen. Dieser Vergleich gilt nur für die Bits im Verweis-und Schablonen Puffer Eintrag, die in der Schablonen Maske festgelegt sind (durch den D3DRS \_ stencilmask-Rendering festgelegt). **True** gibt an, dass der Schablone-Test durchlaufen wird.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ stencilref**
</dt> <dd>

Ein int-Verweis Wert für den Schablonen Test. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ stencilmask**
</dt> <dd>

Die auf den Verweis Wert angewendete Maske und die einzelnen Schablonen Puffer Einträge, um die signifikanten Bits für den Schablonen Test zu bestimmen. Die Standard Maske ist 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ stencilschreitefrage**
</dt> <dd>

Schreib Maske, die auf Werte angewendet wird, die in den Schablonen Puffer geschrieben wurden. Die Standard Maske ist 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ TextureFactor**
</dt> <dd>

Die Farbe, die für die mehrfach Textur Mischung mit dem D3DTA \_ Tfactor-Textur Mischungs Argument oder dem D3DTOP \_ blendfactoralpha-Textur Mischungs Vorgang verwendet wird. Der zugeordnete Wert ist eine [**D3DCOLOR**](d3dcolor.md) -Variable. Der Standardwert ist undurchsichtig weiß (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Textur Wrapping Verhalten für mehrere Sätze von Texturkoordinaten. Gültige Werte für diesen Rendering-Zustand können eine beliebige Kombination aus den \_ Flags D3DWRAPCOORD 0 (oder D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (oder D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (oder D3DWRAP \_ W) und D3DWRAPCOORD \_ 3 sein. Diese bewirken, dass das System in der Richtung der ersten, zweiten, dritten und vierten Dimensionen (manchmal auch als s-, t-, r-und q-Richtung) für eine bestimmte Textur eingebunden wird. Der Standardwert für diesen Rendering-Zustand ist 0 (Wrapping in alle Richtungen deaktiviert).

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

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ Clipping**
</dt> <dd>

**True** , um das primitive Clipping durch Direct3D zu aktivieren, oder **false** , um es zu deaktivieren. Der Standardwert ist " **true**".

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS- \_ Beleuchtung**
</dt> <dd>

**True** , um die Direct3D-Beleuchtung zu aktivieren, oder **false** , um Sie zu deaktivieren. Der Standardwert ist " **true**". Nur Scheitel Punkte, die eine Scheitelpunkt normale enthalten, werden ordnungsgemäß beleuchtet. Scheitel Punkte, die keine normale enthalten, verwenden in allen Beleuchtungsberechnungen ein Punktprodukt von 0.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ AMBIENT**
</dt> <dd>

Helle Farbe der Umgebung. Dieser Wert ist vom Typ [**D3DCOLOR**](d3dcolor.md). Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ fogvertexmode**
</dt> <dd>

Für Scheitelpunkt Nebel zu verwendende Nebelformel. Legen Sie auf einen Member des [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyps fest. Der Standardwert ist D3DFOG \_ None.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ ColorVertex**
</dt> <dd>

**True** , um die pro-Vertex-Farbe zu aktivieren oder **false** , um Sie zu deaktivieren. Der Standardwert ist " **true**". Durch das Aktivieren der pro-Vertex-Farbe kann das System die Farbe, die für einzelne Scheitel Punkte in seinen Beleuchtungsberechnungen definiert ist, einschließen.

Weitere Informationen finden Sie in den folgenden Rendering-Zuständen:

-   D3DRS \_ DiffuseMaterialSource
-   D3DRS \_ SpecularMaterialSource
-   D3DRS \_ AmbientMaterialSource
-   D3DRS \_ emissivematerialsource

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ localviewer**
</dt> <dd>

" **True** ", um für die Kamera relative Glanzlichter zu aktivieren, oder " **false** ", um orthogonale Glanzlichter zu verwenden. Der Standardwert ist " **true**". Anwendungen, die eine orthogonale Projektion verwenden, sollten **false** angeben.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ normalizenormals**
</dt> <dd>

**True** , um die automatische Normalisierung von Scheitelpunkt normalen zu aktivieren, oder **false** , um Sie zu deaktivieren. Der Standardwert ist **FALSE**. Wenn Sie diese Funktion aktivieren, normalisiert das System die Scheitelpunkt normale für Scheitel Punkte, nachdem Sie in einen Kamerabereich transformiert wurden, der Rechenzeit aufwändig sein kann.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ DiffuseMaterialSource**
</dt> <dd>

Diffuse Farb Quelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps. Der Standardwert ist D3DMCS \_ COLOR1. Der Wert für diesen Rendering-Zustand wird nur verwendet, wenn der D3DRS \_ ColorVertex-Rendering-Zustand auf **true** festgelegt ist.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ SpecularMaterialSource**
</dt> <dd>

Glanz Farben Quelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps. Der Standardwert ist D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ AmbientMaterialSource**
</dt> <dd>

Umgebungs Farb Quelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps. Der Standardwert ist D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ emissivematerialsource**
</dt> <dd>

Emissive-Farb Quelle für Beleuchtungsberechnungen. Gültige Werte sind Member des [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) -Enumerationstyps. Der Standardwert ist D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ vertexblend**
</dt> <dd>

Anzahl von Matrizen, die zum Durchführen von Geometrie Mischungen verwendet werden sollen, sofern vorhanden. Gültige Werte sind Member des [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) -Enumerationstyps. Der Standardwert ist D3DVBF \_ deaktivieren.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ clipplaneenable**
</dt> <dd>

Aktiviert oder deaktiviert benutzerdefinierte Clippingebenen. Gültige Werte sind ein beliebiges DWORD-Objekt, in dem der Status jedes Bits (festgelegt oder nicht festgelegt) den Aktivierungszustand einer entsprechenden benutzerdefinierten Clippingebene schaltet. Das unwichtigste Bit (Bit 0) steuert die erste Clippingebene am Index 0, und nachfolgende Bits steuern die Aktivierung von Clippingebenen bei höheren Indizes. Wenn ein Bit festgelegt ist, wendet das System während des Szenen Rendering die entsprechende Clippingebene an. Der Standardwert ist 0.

Die [**D3DCLIPPLANEn**](d3dclipplanen.md) -Makros werden definiert, um eine bequeme Möglichkeit zum Aktivieren von Clippingebenen bereitzustellen.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ pointsize**
</dt> <dd>

Ein Gleit Komma Wert, der die Größe angibt, die für die Berechnung der Punktgröße in Fällen verwendet wird, in denen für jeden Scheitelpunkt keine Punktgröße angegeben wird. Dieser Wert wird nicht verwendet, wenn der Scheitelpunkt die Punktgröße enthält. Dieser Wert befindet sich in Bildschirmraum Einheiten, wenn D3DRS \_ pointscaleenable den Wert **false** hat. andernfalls befindet sich dieser Wert in Welt Raumeinheiten. Der Standardwert ist der Wert, den ein Treiber zurückgibt. Wenn ein Treiber 0 oder 1 zurückgibt, ist der Standardwert 64, womit die Software Punktgröße emulieren kann. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ pointsize \_ Min**
</dt> <dd>

Ein float-Wert, der die minimale Größe von Punkt primitiven angibt. Punkt primitiven werden während des Renderings an diese Größe gebunden. Wenn Sie diese Einstellung auf Werte festlegen, die kleiner als 1,0 sind, werden Punkte verworfen, wenn der Punkt keine Pixel Zentrierung abdeckt und das Antialiasing deaktiviert ist oder mit reduzierter Intensität gerendert wird, wenn das Antialiasing aktiviert ist. Der Standardwert ist 1.0 f. Der Bereich für diesen Wert ist größer als oder gleich 0,0 f. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ pointspriteenable**
</dt> <dd>

boolescher Wert. Wenn **true**, werden Texturkoordinaten von Punkt primitiven festgelegt, sodass an jedem Punkt vollständige Texturen zugeordnet werden. Bei " **false**" werden die Scheitelpunkt Texturkoordinaten für den gesamten Punkt verwendet. Der Standardwert ist **FALSE**. Sie können Einzel Pixel Punkte im DirectX 7-Stil erzielen, indem Sie D3DRS \_ pointscaleenable auf **false** und D3DRS \_ pointsize auf 1,0 festlegen. Dies sind die Standardwerte.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ pointscaleenable**
</dt> <dd>

boolescher Wert, der die Berechnung der Größe für Punkt primitive steuert. **True** gibt an, dass die Punktgröße als Wert für die Kamera Fläche interpretiert wird und durch die Entfernungs Funktion skaliert wird, und durch den Wert von "Frustum" wird die y-Achsen-Skalierung berechnet, um die endgültige Größe des Bildschirm Raums zu berechnen. Bei " **false**" wird die Punktgröße als Bildschirmfläche interpretiert und direkt verwendet. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ pointscale \_ A**
</dt> <dd>

Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert. Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat. Der Standardwert ist 1.0 f. Der Bereich für diesen Wert ist größer als oder gleich 0,0 f. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ pointscale \_ B**
</dt> <dd>

Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert. Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat. Der Standardwert ist 0,0 f. Der Bereich für diesen Wert ist größer als oder gleich 0,0 f. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ pointscale \_ C**
</dt> <dd>

Ein float-Wert, der die Entfernungs basierte Größen Dämpfung für Punkt primitive steuert. Nur aktiv, wenn D3DRS \_ pointscaleenable den Wert **true** hat. Der Standardwert ist 0,0 f. Der Bereich für diesen Wert ist größer als oder gleich 0,0 f. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ multisampleantialias**
</dt> <dd>

boolescher Wert, der bestimmt, wie einzelne Stichproben berechnet werden, wenn ein Multisampling-Renderziel-Puffer verwendet wird. Wenn diese Einstellung auf " **true**" festgelegt ist, werden mehrere Stichproben berechnet, sodass das Vollbild-Antialiasing durch Sampling an verschiedenen Beispiel Positionen für die einzelnen Stichproben durchgeführt wird. Wenn diese Einstellung auf " **false**" festgelegt ist, werden alle Samplings mit dem gleichen Stichproben Wert geschrieben, der im Pixel Center Stichprobe ist, wodurch das Rendering von nicht-Antialiasing an einen Multisampling-Puffer ermöglicht wird. Dieser renderzustand hat keine Auswirkung, wenn ein einzelner Beispiel Puffer gerendert wird. Der Standardwert ist " **true**".

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ multisamplemask**
</dt> <dd>

Jedes Bit in dieser Maske, beginnend mit dem am wenigsten signifikanten Bit (LSB), steuert die Änderung eines der Beispiele in einem Multisampling-Renderziel. Daher enthält das niedrige Byte bei einem 8-Stichproben-Renderziel die acht Schreibvorgänge für jedes der acht Stichproben. Dieser renderzustand hat keine Auswirkung, wenn ein einzelner Beispiel Puffer gerendert wird. Der Standardwert ist 0xFFFFFFFF.

Dieser renderzustand ermöglicht die Verwendung eines Multisampling-Puffers als Akkumulations Puffer und ermöglicht das Multipass-Rendering der Geometrie, bei der jeder Pass eine Teilmenge von Beispielen aktualisiert.

Wenn n multisamples-und k-aktivierte Beispiele vorhanden sind, sollte die resultierende Intensität des gerenderten Bilds k/n sein. Jede Komponente RGB jedes Pixels wird von k/n berücksichtigt.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ patchedgestyle**
</dt> <dd>

Legt fest, ob patchkanten den Mosaik Stil verwenden. Mögliche Werte werden durch den [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) -enumerierten Typ definiert. Der Standardwert ist D3DPATCHEDGE \_ diskret.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS-Debug- \_ monitortoken**
</dt> <dd>

Wird nur zum Debuggen des Monitors festgelegt. Mögliche Werte werden durch den [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) -enumerierten Typ definiert. Beachten Sie Folgendes: Wenn D3DRS \_ debugmonitortoken festgelegt ist, wird der-Befehl als übergeben eines Tokens an den Debug-Monitor behandelt. Wenn z \_ . b. nach dem übergeben von D3DDMT enable oder D3DDMT \_ Deaktivieren an D3DRS \_ debugmonitortoken-andere Tokenwerte übergeben werden, wird der Status (aktiviert oder deaktiviert) des debugmonitors weiterhin beibehalten.

Dieser Status ist nur für Debugbuilds nützlich. Der Debugmonitor wird standardmäßig auf D3DDMT \_ enable eingestellt.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ pointsize \_ Max**
</dt> <dd>

Ein float-Wert, der die maximale Größe angibt, an die Punkt Sprites gebunden werden. Der Wert muss kleiner oder gleich dem maxpointsize-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) und größer oder gleich D3DRS \_ pointsize \_ min sein. Der Standardwert ist 64,0. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ indexedvertexblendenable**
</dt> <dd>

boolescher Wert, der die indizierte Vertex-Mischung aktiviert oder deaktiviert. Der Standardwert ist **FALSE**. Wenn diese Option auf **true** festgelegt ist, wird die indizierte vertexmischung aktiviert. Wenn **false** festgelegt ist, wird die indizierte vertexmischung deaktiviert. Wenn dieser renderzustand aktiviert ist, muss der Benutzer Matrix Indizes als gepacktes dwordan jeden Scheitelpunkt übergeben. Wenn der renderzustand deaktiviert ist und Vertex-Blending über den D3DRS \_ vertexblend-Zustand aktiviert wird, entspricht er den Matrix Indizes 0, 1, 2 und 3 in jedem Scheitelpunkt.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ colorschreiteenable**
</dt> <dd>

Uint-Wert, der einen pro-Channel-Schreibvorgang für den Renderziel-Farb Puffer ermöglicht. Ein Set-Bit führt dazu, dass der Farbkanal während des 3D-Renderings aktualisiert wird. Ein Clear-Bit führt dazu, dass der Farbkanal nicht beeinträchtigt wird. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ colorwrite teenable-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist. Dieser Rendering-Zustand wirkt sich nicht auf den Löschvorgang aus. Der Standardwert ist 0x0000000f.

Gültige Werte für diesen gerengerzustand können eine beliebige Kombination aus den \_ Flags D3DCOLORWRITEENABLE Alpha, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ grün oder D3DCOLORWRITEENABLE \_ Red sein.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ tweumfactor**
</dt> <dd>

Ein float-Wert, der den Tween-Faktor steuert. Der Standardwert ist 0,0 f. Da die [**IDirect3DDevice9:: setrenderstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) -Methode DWORD-Werte akzeptiert, muss Ihre Anwendung eine Variable umwandeln, die den Wert enthält, wie im folgenden Codebeispiel gezeigt.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ blendop**
</dt> <dd>

Der Wert, der verwendet wird, um die arithmetische Operation auszuwählen, die angewendet wird, wenn der D3DRS \_ AlphaBlendEnable-Mischungs Zustand auf **true** festgelegt ist. Gültige Werte werden durch den [**D3DBLENDOP**](./d3dblendop.md) -enumerierten Typ definiert. Der Standardwert ist D3DBLENDOP \_ Add.

Wenn die D3DPMISCCAPS \_ blendop-Geräte Funktion nicht unterstützt wird, \_ wird D3DBLENDOP Add ausgeführt.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ positiondegree**
</dt> <dd>

N-patchpositions-Interpolations Grad. Die Werte können D3DDEGREE \_ Cubic (Standard) oder D3DDEGREE \_ linear lauten. Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ normaldegree**
</dt> <dd>

N-Patch-normaler Interpolations Grad. Die Werte können D3DDEGREE \_ linear (Standard) oder D3DDEGREE \_ Quadratic lauten. Weitere Informationen finden Sie unter [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ scissortestenable**
</dt> <dd>

**True** , um das Testen von Scheren zu aktivieren und **false** zu deaktivieren. Der Standardwert ist **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ slopescaledepthbias**
</dt> <dd>

Wird verwendet, um zu bestimmen, wie viel Bias auf die Co-planaren primitiven angewendet werden kann, um die z-Bekämpfung zu verringern. Der Standardwert ist 0.

Bias = (Max \* D3DRS \_ slopescaledepthbias) + D3DRS \_ depthbias.

Dabei ist Max die maximale Tiefe Steigung des gerenderten Dreiecks.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ antialiasedlineenable**
</dt> <dd>

**True** , um das Zeilen-Antialiasing zu aktivieren, **false** , um das Zeilen-Antialiasing zu deaktivieren Der Standardwert ist **FALSE**.

Beim Rendern in ein Multisampling-Renderziel \_ wird D3DRS antialiasedlineenable ignoriert, und alle Zeilen werden als Alias gerendert. Verwenden Sie [**ID3DXLine**](id3dxline.md) für das Zeilen Rendering mit Antialiasing in einem Multisampling-Renderziel.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ mintmeellationlevel**
</dt> <dd>

Minimale Mosaik Ebene. Der Standardwert ist 1.0 f. Weitere Informationen finden Sie unter Mosaik [(Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ maxtmeellationlevel**
</dt> <dd>

Maximale Mosaik Ebene. Der Standardwert ist 1.0 f. Weitere Informationen finden Sie unter Mosaik [(Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ adaptivetess \_ X**
</dt> <dd>

In der x-Richtung auf adaptiver Mosaik Wert. Der Standardwert ist 0,0 f. Weitere [Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ adaptivetess \_ Y**
</dt> <dd>

In der y-Richtung auf adaptiver Mosaik Wert. Der Standardwert ist 0,0 f. Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ adaptivetess \_ Z**
</dt> <dd>

Zu adaptiver Mosaik Wert in der z-Richtung. Der Standardwert ist 1.0 f. Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ adaptivetess \_ W**
</dt> <dd>

In der w-Richtung auf adaptiver Mosaik Wert. Der Standardwert ist 0,0 f. Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ enableadaptivetess**
</dt> <dd>

" **True** ", um das adaptive Mosaik zu aktivieren, " **false** ", um es zu deaktivieren. Der Standardwert ist **FALSE**. Weitere [ \_ Informationen](tessellation.md)finden Sie unter Adaptive Mosaik.

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ twosidedstencilmode**
</dt> <dd>

**True** aktiviert die zweiseitige Schablone, **false** deaktiviert sie. Der Standardwert ist **FALSE**. Die Anwendung sollte D3DRS \_ CullMode auf D3DCULL \_ None festlegen, um den zweiseitigen Schablonen Modus zu aktivieren. Wenn die dreieckige Reihenfolge im Uhrzeigersinn liegt, werden die D3DRS \_ Stencil- \* Vorgänge verwendet. Wenn die Sortierreihenfolge gegen den Uhrzeigersinn steht, werden die D3DRS \_ CCW- \_ Schablone- \* Vorgänge verwendet.

Um festzustellen, ob zweiseitige Schablonen unterstützt werden, überprüfen Sie das Schablone-Element von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) für D3DSTENCILCAPS \_ twotional. Siehe auch [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ stencilfail**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn der CCW-Schablonen Test fehlschlägt. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ stencilzfail**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn der CCW-Schablonen Test erfolgreich verläuft und z-Test fehlschlägt. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ stencilpass**
</dt> <dd>

Der Schablonen Vorgang, der ausgeführt werden soll, wenn die CCW-Schablone und die z-Tests bestanden werden. Werte stammen aus dem [**D3DSTENCILOP**](./d3dstencilop.md) -Enumerationstyp. Der Standardwert ist D3DSTENCILOP \_ Keep.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ stencilfunc**
</dt> <dd>

Die Vergleichsfunktion. Der CCW-Schablone-Test wird durchgeführt, wenn ((Ref & Mask) die Schablone-Funktion (Schablone & Mask)) " **true**" ist. Werte stammen aus dem [**D3DCMPFUNC**](./d3dcmpfunc.md) -Enumerationstyp. Der Standardwert ist D3DCMP \_ Always.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Zusätzliche colorschreiteenable-Werte für die Geräte. Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Zusätzliche colorschreiteenable-Werte für die Geräte. Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Zusätzliche colorschreiteenable-Werte für die Geräte. Weitere Informationen finden Sie unter D3DRS \_ colorschreiteenable. Diese Funktionalität ist verfügbar, wenn das D3DPMISCCAPS \_ independentwrite temasks-Funktionen-Bit im primitivefehlcaps-Member der [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) -Struktur für das Gerät festgelegt ist. Der Standardwert ist 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ blendfactor**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) wird für einen konstanten Blend-Faktor während der Alpha Mischung verwendet. Diese Funktionalität ist verfügbar, wenn das D3DPBLENDCAPS \_ blendfactor-Funktionen-Bit im srcblendcaps-Member von [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) oder dem destblendcaps-Member von **D3DCAPS9** festgelegt ist. Siehe [**D3DRENDERSTATETYPE**](). Der Standardwert ist 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ srgbschreiteenable**
</dt> <dd>

Renderziel-Schreibvorgänge für die Gammakorrektur in sRGB aktivieren. Das Format muss D3DUSAGE \_ srgbwrite verfügbar machen. Der Standardwert ist 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ depthbias**
</dt> <dd>

Ein Gleit Komma Wert, der für den Vergleich von tiefen Werten verwendet wird. Siehe [tiefen Bias (Direct3D 9)](depth-bias.md). Der Standardwert ist 0.

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

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ separatealphablendenable**
</dt> <dd>

**True** aktiviert den separaten Blend-Modus für den Alphakanal. Der Standardwert ist **FALSE**.

Wenn diese Einstellung auf " **false**" festgelegt ist, werden die auf Alpha angewendeten Mischungs Ziel Faktoren und-Vorgänge mit den für die Farbe definierten Vorgängen erzwungen. Dieser Modus ist für Implementierungen, die nicht die Cap-D3DPMISCCAPS-Trennzeichen festgelegt haben, auf **false** festgelegt \_ . Siehe [D3DPMISCCAPS](d3dpmisccaps.md).

Der Typ der separaten Alpha Mischung wird durch die \_ Rendering-Zustände D3DRS srcblendalpha und D3DRS \_ destblendalpha bestimmt.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ srcblendalpha**
</dt> <dd>

Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps. Dieser Wert wird ignoriert, es sei denn, D3DRS \_ separatealphablendenable ist " **true**". Der Standardwert ist D3DBLEND \_ 1.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ destblendalpha**
</dt> <dd>

Ein Member des [**D3DBLEND**](./d3dblend.md) -Enumerationstyps. Dieser Wert wird ignoriert, es sei denn, D3DRS \_ separatealphablendenable ist " **true**". Der Standardwert ist D3DBLEND \_ 0 (null).

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ blendopalpha**
</dt> <dd>

Der Wert, der zum Auswählen der arithmetischen Operation verwendet wird, die auf separate Alpha Blending angewendet wird, wenn der Rendering-Zustand, D3DRS \_ separatealphablendenable, auf **true** festgelegt ist

Gültige Werte werden durch den [**D3DBLENDOP**](./d3dblendop.md) -enumerierten Typ definiert. Der Standardwert ist D3DBLENDOP \_ Add.

Wenn die D3DPMISCCAPS \_ blendop-Geräte Funktion nicht unterstützt wird, \_ wird D3DBLENDOP Add ausgeführt. Siehe [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen



| Rendering-Zustände        |                    |
|----------------------|--------------------|
| PS \_ 1 1 \_ bis PS \_ 1 \_ 3 | vier Textur-Samplern |



 

Direct3D definiert die D3DRENDERSTATE \_ wrapbias-Konstante als praktische Möglichkeit für Anwendungen, um die Textur Umbrüche basierend auf der NULL basierten Ganzzahl eines Texturkoordinaten Satzes (anstatt explizit einen der D3DRS Wrap n-Zustands Werte zu verwenden) zu aktivieren oder zu deaktivieren \_ . Fügen Sie dem \_ NULL basierten Index eines Texturkoordinaten Satzes den D3DRENDERSTATE wrapbias-Wert hinzu, um den D3DRS \_ Wrap n-Wert zu berechnen, der diesem Index entspricht, wie im folgenden Beispiel gezeigt.


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
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9::GetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9:: * Trend List State**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
