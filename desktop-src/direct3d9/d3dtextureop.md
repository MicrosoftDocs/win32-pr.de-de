---
description: Definiert einstufige Textur Mischungs Vorgänge.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: D3DTEXTUREOP-Enumeration (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354516"
---
# <a name="d3dtextureop-enumeration"></a>D3DTEXTUREOP-Enumeration

Definiert einstufige Textur Mischungs Vorgänge.

## <a name="syntax"></a>Syntax


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**D3DTOP \_ Deaktivieren**
</dt> <dd>

Deaktiviert die Ausgabe dieser Textur Phase und aller Stufen mit einem höheren Index. Um die Textur Zuordnung zu deaktivieren, legen Sie diese als Farb Vorgang für die erste Textur Phase fest (Phase 0). Alpha Vorgänge können nicht deaktiviert werden, wenn Farb Vorgänge aktiviert sind. Das Festlegen des Alpha-Vorgangs auf D3DTOP \_ deaktivieren, wenn die Farbmischung aktiviert ist, verursacht ein nicht definiertes Verhalten

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Verwenden Sie die erste Farbe oder das Alpha Argument der Textur Phase, unverändert als Ausgabe. Dieser Vorgang wirkt sich auf das Color-Argument aus, wenn es mit dem D3DTSS \_ colorop-Textur Stufen Zustand verwendet wird, und das Alpha-Argument bei Verwendung mit D3DTSS \_ alphaop.

![Gleichung dieses Arguments (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Verwenden Sie die zweite Farbe oder das Alpha Argument der Textur Phase unverändert als Ausgabe. Dieser Vorgang wirkt sich auf das Color-Argument aus, wenn es mit dem D3DTSS \_ colorop-Textur Stufen Zustand verwendet wird, und das Alpha-Argument bei der Verwendung mit D3DTSS \_ alphaop.

![Gleichung dieses Arguments (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOP \_ modulate**
</dt> <dd>

Multiplizieren Sie die Komponenten der Argumente.

![Gleichung der modulieren-Operation (s (RGBA) = arg1 x Arg 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

Multiplizieren Sie die Komponenten der Argumente, und verschieben Sie die Produkte auf das linke 1 Bit (wodurch Sie effektiv um 2 multipliziert werden), um die Beleuchtung zu verbessern.

![Gleichung der Modulate2X Operation (s (RGBA) = (arg1 x Arg 2), dann Shift Left 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

Multiplizieren Sie die Komponenten der Argumente, und verschieben Sie die Produkte auf die linken 2 Bits (wodurch Sie durch 4 multipliziert werden), um die Beleuchtung zu verbessern.

![Gleichung der Modulate4X Operation (s (RGBA) = (arg1 x Arg 2), UMSCHALT Left 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Hinzufügen**
</dt> <dd>

Fügen Sie die Komponenten der Argumente hinzu.

![Gleichung des Add-Vorgangs (s (RGBA) = arg1 + Arg 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ AddSigned**
</dt> <dd>

Fügen Sie die Komponenten der Argumente mit einem-0,5-Bias hinzu, und legen Sie den effektiven Wertebereich von-0,5 bis 0,5.

![Gleichung der hinzu zufügenden signierten Operation (s (RGBA) = arg1 + Arg 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Fügen Sie die Komponenten der Argumente mit einem-0,5-Bias hinzu, und verschieben Sie die Produkte auf das linke 1-Bit.

![Gleichung des hinzu fügenden 2X-Vorgangs ((s (RGBA) = arg1 + Arg 2-0,5) und nach links 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**D3DTOP \_ subtrahieren**
</dt> <dd>

Subtrahieren Sie die Komponenten des zweiten Arguments von denen des ersten Arguments.

![Gleichung des subtrahieren-Vorgangs (s (RGBA) = arg1-Arg 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ AddSmooth**
</dt> <dd>

Fügen Sie das erste und zweite Argument hinzu. subtrahieren Sie dann das Produkt von der Summe.

![Gleichung des hinzu fügenden Smooth-Vorgangs (s (RGBA) = arg1 + Arg 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ blenddiffusealpha**
</dt> <dd>

Linear Blend diese Textur Phase, wobei das interpoliert-Alpha aus jedem Scheitelpunkt verwendet wird.

![Gleichung der Blend-diffuses Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ blendtexturealpha**
</dt> <dd>

Linear Blend diese Textur Phase, wobei das Alpha aus der Textur dieser Stufe verwendet wird.

![Gleichung der Blend-Textur Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ blendfactor Alpha**
</dt> <dd>

Linear Blend diese Textur Phase, wobei eine skalare Alpha Gruppe mit dem D3DRS \_ TextureFactor-Rendering-Zustand verwendet wird.

![Gleichung der Blend Faktor Alpha Operation (s (RGBA) = arg1 x Alpha + Arg 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ blendtexturealphapm**
</dt> <dd>

Linear Blend eine Textur Phase, in der ein prämultipliziertes Alpha verwendet wird.

![Gleichung des Blend-Textur-Alpha-pm-Vorgangs (s (RGBA) = arg1 + Arg 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ blendcurrentalpha**
</dt> <dd>

Linear Blend diese Textur Phase mit dem Alpha aus der vorherigen Textur Phase.

![Gleichung der Blend-aktuellen Alpha Operation (s (RGBA) = arg1 x Alpha + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOP \_ PreModulate**
</dt> <dd>

D3DTOP \_ PreModulate wird in Phase n festgelegt. Die Ausgabe von Phase n ist arg1. Wenn eine Textur in der Phase n + 1 vorhanden ist, werden alle D3DTA, die \_ in Phase n + 1 aktuell sind, in der Phase n + 1 mit der Textur aufgefüllt.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ modulatealpha \_ addcolor**
</dt> <dd>

Gibt die Farbe des zweiten Arguments mit dem Alpha des ersten Arguments an. Fügen Sie dann das Ergebnis zu Argument 1 hinzu. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

![Gleichung des Vorgangs zum Hinzufügen von Color modulieren Alpha (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ modulatecolor \_ addalpha**
</dt> <dd>

Modulate der Argumente. Fügen Sie dann das Alpha des ersten Arguments hinzu. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

![Gleichung des hinzu fügenden Alpha modulieren Color-Vorgangs (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ modulateinvalpha \_ addcolor**
</dt> <dd>

Vergleichbar mit D3DTOP \_ modulatealpha \_ addcolor, aber mit der Umkehrung der Alpha des ersten Arguments. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

![Gleichung des Vorgangs zum Hinzufügen von farbmodulen mit umgekehrtem Alpha (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ modulateinvcolor \_ addalpha**
</dt> <dd>

Vergleichbar mit D3DTOP \_ modulatecolor \_ addalpha, aber verwenden Sie die Umkehrung der Farbe des ersten Arguments. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

![Gleichung des hinzu fügenden Alpha modulieren-Farb Vorgangs (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ bumpenvmap**
</dt> <dd>

Durchführen einer pro-Pixel-Bump-Zuordnung mithilfe der Umgebungs Zuordnung in der nächsten Textur Phase ohne Leuchtkraft. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ bumpumvmapluminance**
</dt> <dd>

Durchführen einer pro-Pixel-Bump-Zuordnung mithilfe der Umgebungs Zuordnung in der nächsten Textur Phase mit Leuchtkraft. Dieser Vorgang wird nur für Farb Vorgänge (D3DTSS \_ colorop) unterstützt.

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Modulieren Sie die Komponenten der einzelnen Argumente als signierte Komponenten, und fügen Sie Ihre Produkte hinzu. Replizieren Sie die Summe dann in alle Farbkanäle, einschließlich alpha. Dieser Vorgang wird für Farb-und Alpha Vorgänge unterstützt.

![Gleichung der Punktprodukt 3 Operation (s (RGBA) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

In DirectX 6 und DirectX 7 werden die oben genannten Eingaben vor der Verwendung zum simulieren signierter Daten um die Hälfte (y = x-0,5) nach unten verschoben, und das skalare Ergebnis wird automatisch an positive Werte gebunden und auf alle drei Ausgabekanäle repliziert. Beachten Sie außerdem, dass bei einem Farb Vorgang die Alpha-Komponenten nicht aktualisiert werden.

In DirectX 8,1-Shadern können Sie jedoch angeben, dass die Ausgabe an die RGB-oder die. a-Komponente oder beides (Standard) weitergeleitet werden soll. Sie können auch einen separaten skalarvorgang für den Alphakanal angeben.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ MultiplyAdd**
</dt> <dd>

Führt einen Multiplikations Vorgang aus. Es werden die beiden letzten Argumente abgerufen, multipliziert und dem verbleibenden Eingabe-/Quellargument hinzugefügt und in das Ergebnis eingefügt.

S<sub>RGBA</sub> = arg1 + arg2 \* arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ Lerp**
</dt> <dd>

Linearly interpoliert zwischen dem zweiten und dritten Quell Argument durch einen proportional, der im ersten Quell Argument angegeben ist.

S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Erzwingen von \_ DWORD**
</dt> <dd>

Erzwingt die Kompilierung dieser Enumeration in 32 Bits. Ohne diesen Wert können einige Compiler zulassen, dass diese Enumeration in eine andere Größe als 32 Bits kompiliert wird. Dieser Wert wird nicht verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die Member dieses Typs werden verwendet, wenn Farb-oder Alpha Operationen mithilfe der D3DTSS \_ colorop-oder D3DTSS \_ alphaop-Werte mit der [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) -Methode festgelegt werden.

In den obigen Formeln ist S<sub>RGBA</sub> die von einer Textur Operation erzeugte RGBA-Farbe, und arg1, arg2 und arg3 stellen die gesamte RGBA-Farbe der Textur Argumente dar. Einzelne Komponenten eines Arguments werden mit Indexzeichen angezeigt. Die Alpha Komponente für Argument 1 würde z. b. als arg1<sub>A</sub>angezeigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
