---
description: Gibt an, wie die Glyphendaten aus den Quell- und Zieloberflächen in einem Aufruf von ComposeRects kombiniert werden.
ms.assetid: 4b0e6e48-48e0-4955-bb20-f953fdce785c
title: D3DCOMPOSERECTSOP-Enumeration (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DCOMPOSERECTSOP
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 8d968770eb58d9d3dd59f178b05e8e6536079e8de601ddef602a41da4b52ee51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117911168"
---
# <a name="d3dcomposerectsop-enumeration"></a>D3DCOMPOSERECTSOP-Enumeration

Gibt an, wie die Glyphendaten aus den Quell- und Zieloberflächen in einem Aufruf von [**ComposeRects kombiniert werden.**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9ex-composerects)

## <a name="syntax"></a>Syntax


```C++
typedef enum _D3DCOMPOSERECTSOP { 
  D3DCOMPOSERECTS_COPY         = 1,
  D3DCOMPOSERECTS_OR           = 2,
  D3DCOMPOSERECTS_AND          = 3,
  D3DCOMPOSERECTS_NEG          = 4,
  D3DCOMPOSERECTS_FORCE_DWORD  = 0x7fffffff
} D3DCOMPOSERECTSOP;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DCOMPOSERECTS_COPY"></span><span id="d3dcomposerects_copy"></span>**D3DCOMPOSERECTS \_ COPY**
</dt> <dd>

Kopieren Sie die Quelle in das Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_OR"></span><span id="d3dcomposerects_or"></span>**D3DCOMPOSERECTS \_ ODER**
</dt> <dd>

Bitweises OR die Quelle und das Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_AND"></span><span id="d3dcomposerects_and"></span>**D3DCOMPOSERECTS \_ UND**
</dt> <dd>

Bitweise AND die Quelle und das Ziel.

</dd> <dt>

<span id="D3DCOMPOSERECTS_NEG"></span><span id="d3dcomposerects_neg"></span>**D3DCOMPOSERECTS \_ NEG**
</dt> <dd>

Kopieren Sie die negierte Quelle in das Ziel (Dst & ~Src).

</dd> <dt>

<span id="D3DCOMPOSERECTS_FORCE_DWORD"></span><span id="d3dcomposerects_force_dword"></span>**D3DCOMPOSERECTS \_ FORCE \_ DWORD**
</dt> <dd>

Reserviert. Wird verwendet, um die Enumeration auf eine Größe von 32 Bits zu erzwingen.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Enumerationen](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 




