---
title: CD3DX12_STATIC_SAMPLER_DESC-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ STATIC \_ SAMPLER \_ DESC-Struktur zu ermöglichen.
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_STATIC_SAMPLER_DESC
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd2e64a98a8dd11b62154bb3239934fd8da29eb6f8bf2919ef88452d280de6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069760"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>CD3DX12 \_ STATIC \_ SAMPLER \_ DESC-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ STATIC \_ SAMPLER \_ DESC-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_STATIC_SAMPLER_DESC  : public D3D12_STATIC_SAMPLER_DESC{
       CD3DX12_STATIC_SAMPLER_DESC();
       explicit CD3DX12_STATIC_SAMPLER_DESC(const D3D12_STATIC_SAMPLER_DESC &o);
       CD3DX12_STATIC_SAMPLER_DESC(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void static inline Init(D3D12_STATIC_SAMPLER_DESC &samplerDesc, UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
  void inline Init(UINT shaderRegister, D3D12_FILTER filter = D3D12_FILTER_ANISOTROPIC, D3D12_TEXTURE_ADDRESS_MODE addressU = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressV = D3D12_TEXTURE_ADDRESS_MODE_WRAP, D3D12_TEXTURE_ADDRESS_MODE addressW = D3D12_TEXTURE_ADDRESS_MODE_WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12_COMPARISON_FUNC comparisonFunc = D3D12_COMPARISON_FUNC_LESS_EQUAL, D3D12_STATIC_BORDER_COLOR borderColor = D3D12_STATIC_BORDER_COLOR_OPAQUE_WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12_FLOAT32_MAX, D3D12_SHADER_VISIBILITY shaderVisibility = D3D12_SHADER_VISIBILITY_ALL, UINT registerSpace = 0);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ STATIC \_ SAMPLER \_ DESC()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ STATIC \_ SAMPLER \_ DESC.

</dd> <dt>

**Explicit CD3DX12 \_ STATIC \_ SAMPLER \_ DESC(const D3D12 \_ STATIC \_ SAMPLER \_ DESC &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ STATIC \_ SAMPLER \_ DESC, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ STATIC \_ SAMPLER \_ DESC-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)

</dd> <dt>

**CD3DX12 \_ STATIC \_ SAMPLER \_ DESC(UINT shaderRegister, D3D12 \_ FILTER filter = D3D12 FILTER \_ \_ ANISOTROP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressW = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12 \_ COMPARISON \_ FUNC comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE \_ \_ \_ \_ WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY \_ shaderVisibility = D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ STATIC \_ SAMPLER \_ DESC und initialisiert die folgenden Parameter:

UINT-ShaderRegister

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ VERGLEICH \_ FUNC-VergleichFunc**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) = D3D12 \_ VERGLEICH \_ FUNC \_ LESS \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0,f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12 \_ SHADER \_ VISIBILITY \_ ALL

(opt) UINT registerSpace = 0

</dd> <dt>

**static inline Init(D3D12 \_ STATIC \_ SAMPLER \_ DESC &samplerDesc, UINT shaderRegister, D3D12 \_ FILTER filter = D3D12 FILTER \_ \_ ANISOTROP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressW = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12 \_ COMPARISON \_ FUNC comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE \_ \_ \_ \_ WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY \_ shaderVisibility = D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) &samplerDesc

UINT-ShaderRegister

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ VERGLEICH \_ FUNC-VergleichFunc**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) = D3D12 \_ VERGLEICH \_ FUNC \_ LESS \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0,f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12 \_ SHADER \_ VISIBILITY \_ ALL

(opt) UINT registerSpace = 0

</dd> <dt>

**inline Init(UINT shaderRegister, D3D12 \_ FILTER filter = D3D12 \_ FILTER \_ ANISOTROP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressU = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressV = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, D3D12 \_ TEXTURE ADDRESS MODE \_ \_ addressW = D3D12 \_ TEXTURE ADDRESS MODE \_ \_ \_ WRAP, FLOAT mipLODBias = 0, UINT maxAnisotropy = 16, D3D12 \_ COMPARISON \_ FUNC comparisonFunc = D3D12 \_ COMPARISON \_ FUNC LESS \_ \_ EQUAL, D3D12 \_ STATIC BORDER COLOR \_ \_ borderColor = D3D12 \_ STATIC BORDER COLOR OPAQUE \_ \_ \_ \_ WHITE, FLOAT minLOD = 0.f, FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX, D3D12 \_ SHADER VISIBILITY \_ shaderVisibility = D3D12 \_ SHADER VISIBILITY \_ \_ ALL, UINT registerSpace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

UINT-ShaderRegister

(opt) [**D3D12 \_ FILTER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) filter = D3D12 \_ FILTER \_ ANISOTROP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressU = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressV = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) [**D3D12 \_ TEXTURE \_ ADDRESS \_ MODE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) addressW = D3D12 \_ TEXTURE \_ ADDRESS \_ MODE \_ WRAP

(opt) FLOAT mipLODBias = 0

(opt) UINT maxAnisotropy = 16

(opt) [**D3D12 \_ VERGLEICH \_ FUNC-VergleichFunc**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) = D3D12 \_ VERGLEICH \_ FUNC \_ LESS \_ EQUAL

(opt) [**D3D12 \_ STATIC \_ BORDER \_ COLOR**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) borderColor = D3D12 \_ STATIC \_ BORDER \_ COLOR \_ OPAQUE \_ WHITE

(opt) FLOAT minLOD = 0,f

(opt) FLOAT maxLOD = D3D12 \_ FLOAT32 \_ MAX

(opt) [**D3D12 \_ SHADER \_ VISIBILITY**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shaderVisibility = D3D12 \_ SHADER \_ VISIBILITY \_ ALL

(opt) UINT registerSpace = 0

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ STATIC \_ SAMPLER \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





