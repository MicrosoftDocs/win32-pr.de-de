---
title: CD3DX12_ROOT_PARAMETER1-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ root \_ PARAMETER1-Struktur zu ermöglichen.
ms.assetid: CDE0C02E-0112-4FD9-A4A2-36E8C326715C
keywords:
- CD3DX12_ROOT_PARAMETER1 Struktur
topic_type:
- apiref
api_name:
- CD3DX12_ROOT_PARAMETER1
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d582016b26df0d57f7792afd30fc4fcbf3ba97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355232"
---
# <a name="cd3dx12_root_parameter1-structure"></a>CD3DX12 \_ root \_ PARAMETER1-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_ROOT_PARAMETER1  : public D3D12_ROOT_PARAMETER1{
       CD3DX12_ROOT_PARAMETER1();
       explicit CD3DX12_ROOT_PARAMETER1(const D3D12_ROOT_PARAMETER1 &o);
  void static inline InitAsDescriptorTable(D3D12_ROOT_PARAMETER1 &rootParam, UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstants(D3D12_ROOT_PARAMETER1 &rootParam, UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsConstantBufferView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsShaderResourceView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void static inline InitAsUnorderedAccessView(D3D12_ROOT_PARAMETER1 &rootParam, UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsDescriptorTable(UINT numDescriptorRanges, const D3D12_DESCRIPTOR_RANGE1* pDescriptorRanges, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstants(UINT num32BitValues, UINT shaderRegister, UINT registerSpace = 0, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsConstantBufferView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsShaderResourceView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
  void inline InitAsUnorderedAccessView(UINT shaderRegister, UINT registerSpace = 0, D3D12_ROOT_DESCRIPTOR_FLAGS flags = D3D12_ROOT_DESCRIPTOR_FLAG_NONE, D3D12_SHADER_VISIBILITY visibility = D3D12_SHADER_VISIBILITY_ALL);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ root \_ PARAMETER1 ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ root \_ PARAMETER1.

</dd> <dt>

**explizites CD3DX12 \_ root \_ PARAMETER1 (Konstanten D3D12 \_ root \_ PARAMETER1 &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ root \_ PARAMETER1, das mit dem Inhalt einer anderen [**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) -Struktur initialisiert wird.

</dd> <dt>

**static Inline initasdescriptortable (D3D12 \_ root \_ PARAMETER1 &rootparam, uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam

Uint numdescriptor Ranges

Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pdescriptorranges

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**statische initas-Inline Konstanten (D3D12 \_ root \_ PARAMETER1 &rootparam, uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam

Uint num32BitValues

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasconstantbufferview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasshaderresourceview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**static Inline initasunorderedaccessview (D3D12 \_ root \_ PARAMETER1 &rootparam, uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

[**D3D12 \_ ROOT \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1) &rootparam

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasdescriptortable (uint numdescriptorranges, Konstanten D3D12 \_ Descriptor \_ Bereich1 \* pdescriptorranges, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint numdescriptor Ranges

Konstanten [**D3D12 \_ Deskriptor \_ Bereich1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_descriptor_range1) \* pdescriptorranges

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline-initas-Konstanten (uint num32BitValues, uint shaderregister, uint registerspace = 0, D3D12 \_ Shader Visibility \_ Visibility = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint num32BitValues

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasconstantbufferview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasshaderresourceview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> <dt>

**Inline initasunorderedaccessview (uint shaderregister, uint registerspace = 0, D3D12 \_ root \_ Descriptor \_ Flags Flags = D3D12 \_ root \_ Descriptor \_ Flag \_ None, D3D12 \_ Shader Visibility Visibility \_ = D3D12 \_ Shader \_ Visibility \_ all)**
</dt> <dd>

Gibt eine Funktion an, die die folgenden Parameter initialisiert:

Uint-shaderregister

Uint registerspace = 0

[**D3D12 \_ Flags für \_ \_ stammdeskriptorflags**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_descriptor_flags) = D3D12 \_ root \_ Descriptor \_ Flag \_ None

[**D3D12 \_ \_Sichtbarkeit der Shader**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shader_visibility) -Sichtbarkeit = D3D12 \_ Shader \_ Visibility \_ all

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12 \_ root \_ PARAMETER1**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_parameter1)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





