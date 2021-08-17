---
title: D3DX11_PASS_DESC -Struktur (D3dx11effect.h)
description: Beschreibt einen Effektpass, der den Pipelinezustand enthält.
ms.assetid: 3695b99f-d379-403b-aa10-e3e370a6c864
keywords:
- D3DX11_PASS_DESC-Struktur Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_PASS_DESC
api_location:
- d3dx11effect.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f00cc28e6ab901073e30abd2554046d61144c42af2217869c0b87dc6c19d29d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124945"
---
# <a name="d3dx11_pass_desc-structure"></a>D3DX11 \_ PASS \_ DESC-Struktur

Beschreibt einen Effektpass, der den Pipelinezustand enthält.

## <a name="syntax"></a>Syntax


```C++
typedef struct _D3DX11_PASS_DESC {
  LPCSTR Name;
  UINT   Annotations;
  BYTE   *pIAInputSignature;
  SIZE_T IAInputSignatureSize;
  UINT   StencilRef;
  UINT   SampleMask;
  FLOAT  BlendFactor[4];
} D3DX11_PASS_DESC;
```



## <a name="members"></a>Member

<dl> <dt>

**Name**
</dt> <dd>

Typ: **[ **LPCSTR**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Name dieses Durchgangs (**NULL,** wenn nicht anonym).

</dd> <dt>

**Anmerkungen**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Anzahl der Anmerkungen in diesem Durchgang.

</dd> <dt>

**pIAInputSignature**
</dt> <dd>

Typ: **[ **BYTE**](/windows/desktop/WinProg/windows-data-types)\***

</dd> <dd>

Signatur vom Vertex-Shader oder Geometrie-Shader (wenn kein Vertex-Shader vorhanden ist) oder **NULL,** wenn keines vorhanden ist.

</dd> <dt>

**IAInputSignatureSize**
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Singature-Größe in Bytes.

</dd> <dt>

**StencilRef**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Der Schablonenverweiswert, der im Tiefen-Schablonenzustand verwendet wird.

</dd> <dt>

**SampleMask**
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die Beispielmaske für den Überblendzustand.

</dd> <dt>

**BlendFactor**
</dt> <dd>

Typ: **[ **FLOAT**](/windows/desktop/WinProg/windows-data-types)**

</dd> <dd>

Die einzelnen Komponentenblendfaktoren (RGBA) für den Überblendungszustand.

</dd> </dl>

## <a name="remarks"></a>Hinweise

D3DX11 \_ PASS \_ DESC wird mit [**ID3DX11EffectPass::GetDesc verwendet.**](id3dx11effectpass-getdesc.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx11effect.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Effects 11 Structures](d3d11-graphics-reference-effects11-structures.md)
</dt> </dl>

 

