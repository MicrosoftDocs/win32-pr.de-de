---
title: CD3DX12_ROOT_PARAMETER-Struktur (D3dx12. h)
description: Eine hilfsstruktur, die die einfache Initialisierung einer D3D12-Stamm \_ \_ Parameter Struktur ermöglicht.
ms.assetid: CDDF84D0-4E66-4CF2-999B-3F401E8DD17F
keywords:
- CD3DX12_ROOT_PARAMETER Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9099b0839b6b55676d5a8afdfb913948e70bbb7f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106357220"
---
# <a name="cd3dx12_root_parameter-structure"></a>CD3DX12-Stamm \_ \_ Parameter Struktur

Eine hilfsstruktur, die die einfache Initialisierung einer [**D3D12-Stamm \_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur ermöglicht.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_PARAMETER  : public D3D12_ROOT_PARAMETER{
       CD3DX12_ROOT_PARAMETER();
       explicit CD3DX12_ROOT_PARAMETER(const D3D12_ROOT_PARAMETER &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ root- \_ Parameter ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 root- \_ \_ Parameters.

</dd> <dt>

**expliziter CD3DX12 \_ root- \_ Parameter (Konstanten D3D12 \_ root- \_ Parameter &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root- \_ Parameters, der mit dem Inhalt einer anderen [**D3D12-Stamm \_ \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) Struktur initialisiert wird.

</dd> <dt>

**static Inline initasdescriptortable (D3D12 \_ root \_ Parameter &rootparam, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Range \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam

Uint numdescriptor Ranges

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* pdescriptorranges"

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**statische initas-Inline Konstanten (D3D12 \_ root \_ Parameter &rootparam, uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam

Uint num32BitValues

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasconstantbufferview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasshaderresourceview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasunorderedaccessview (D3D12 \_ root \_ Parameter &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter) &rootparam

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasdescriptortable (uint numdescriptorranges, Konstanten D3D12 \_ \_ Deskriptorbereich \* pdescriptorranges, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numdescriptor Ranges

[**D3D12 \_ \_Deskriptorbereich**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range) " \* pdescriptorranges"

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline-initas-Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint num32BitValues

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasconstantbufferview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasshaderresourceview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasunorderedaccessview (uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Opt Uint registerspace = 0

Opt [**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ root- \_ Parameter**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





