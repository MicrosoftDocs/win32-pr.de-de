---
title: CD3DX12_STATIC_SAMPLER_DESC-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ static- \_ Sampler- \_ DESC-Struktur zu ermöglichen.
ms.assetid: C402415D-7BD5-4E23-82C9-B29B0B5669B8
keywords:
- CD3DX12_STATIC_SAMPLER_DESC Struktur
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
ms.openlocfilehash: 6d6b10749f7a56d928e0a4218d534cc2a8ec4fab
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106361841"
---
# <a name="cd3dx12_static_sampler_desc-structure"></a>CD3DX12 \_ statische \_ Sampler- \_ decoderstruktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ static- \_ Sampler- \_ DESC**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -Struktur zu ermöglichen.

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

**CD3DX12 \_ statischer \_ Sampler- \_ Decoder ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ static Sampler- \_ Objekts \_ .

</dd> <dt>

**expliziter CD3DX12 \_ statischer Sampler-Debug \_ \_ (konstant D3D12 \_ statischer \_ Sampler- \_ &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ static Sampler-Objekts \_ \_ , das mit dem Inhalt einer anderen [**D3D12 \_ static \_ Sampler \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -Debug-Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ statischer \_ Sampler- \_ DESC (uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture \_ Address Mode \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode \_ addressssv = D3D12 Texture Address Mode \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ static \_ Sampler \_ DESC und initialisiert die folgenden Parameter:

Uint-shaderregister

Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt FLOAT miplodbias = 0

Opt Uint MaxAnisotropy = 16

Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich

Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß

Opt FLOAT minlod = 0. f

Opt FLOAT maxlod = D3D12 \_ float32 \_ Max

Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all

Opt Uint registerspace = 0

</dd> <dt>

**static Inline init (D3D12 \_ static \_ Sampler \_ &samplerdebug, uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture \_ Address Mode \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode addressssv = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ Statischer \_ Sampler \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc) -&samplerdebug

Uint-shaderregister

Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt FLOAT miplodbias = 0

Opt Uint MaxAnisotropy = 16

Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich

Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß

Opt FLOAT minlod = 0. f

Opt FLOAT maxlod = D3D12 \_ float32 \_ Max

Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all

Opt Uint registerspace = 0

</dd> <dt>

**Inline-init (uint shaderregister, D3D12 \_ Filter Filter = D3D12 \_ Filter \_ Anisotropic, D3D12 \_ Texture \_ Address \_ Mode adressssu = D3D12 \_ Texture Address Mode \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode addressssv = D3D12 Texture Address Modus \_ \_ \_ \_ Wrap, D3D12 \_ Texture \_ Address \_ Mode AddressW = D3D12 Texture Address Mode \_ \_ \_ \_ Wrap, float miplodbias = 0, uint MaxAnisotropy = 16, D3D12 \_ Comparison \_ Func comparisonfunc = D3D12 \_ Comparison \_ Func \_ less \_ EQUAL, D3D12 \_ static \_ Border \_ Color BorderColor = D3D12 \_ static Border Color \_ \_ \_ undurchsichtig \_ White, float minlod = 0. f, float maxlod = D3D12 \_ float32 \_ Max, D3D12 \_ Shader \_ Visibility shadervisibility = D3D12 \_ Shader \_ Visibility \_ all, uint registerspace = 0)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Opt [**D3D12 \_ Filter**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_filter) Filter = D3D12 \_ Filter \_ anisotrope

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) adressssu = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus-Adressenmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) = D3D12 \_ Textur \_ Adress \_ Modus \_ Wrap

Opt [**D3D12 \_ Textur \_ Adress \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_texture_address_mode) AddressW = D3D12 \_ Texture \_ Address \_ Mode \_ Wrap

Opt FLOAT miplodbias = 0

Opt Uint MaxAnisotropy = 16

Opt [**D3D12 \_ Vergleichs- \_ Func**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_comparison_func) comparisonfunc = D3D12 \_ Vergleichs- \_ Func ist \_ weniger \_ gleich

Opt [**D3D12 \_ Statische \_ Rahmen \_ Farbe**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_static_border_color) BorderColor = D3D12 \_ statische \_ Rahmen \_ Farbe \_ undurchsichtiges \_ weiß

Opt FLOAT minlod = 0. f

Opt FLOAT maxlod = D3D12 \_ float32 \_ Max

Opt [**D3D12 \_ Shader \_ Visibility**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) shadervisibility = D3D12 \_ Shader \_ Visibility \_ all

Opt Uint registerspace = 0

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ statischer \_ Sampler- \_ Decoder**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_static_sampler_desc)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





