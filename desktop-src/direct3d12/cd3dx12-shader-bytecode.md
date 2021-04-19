---
title: CD3DX12_SHADER_BYTECODE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12 \_ Shader- \_ Bytecode-Struktur zu ermöglichen.
ms.assetid: 09CEFCCE-C499-493D-ACDE-806E09995315
keywords:
- CD3DX12_SHADER_BYTECODE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_SHADER_BYTECODE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1227c18913492d6533b08f49f5761fab1b93e97b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370403"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>CD3DX12 \_ Shader- \_ Bytecode-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_SHADER_BYTECODE  : public D3D12_SHADER_BYTECODE{
   CD3DX12_SHADER_BYTECODE();
   explicit CD3DX12_SHADER_BYTECODE(const D3D12_SHADER_BYTECODE &o);
   CD3DX12_SHADER_BYTECODE(ID3DBlob* pShaderBlob);
   CD3DX12_SHADER_BYTECODE(const void* _pShaderBytecode, SIZE_T bytecodeLength);
   operator const D3D12_SHADER_BYTECODE&() const;
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ Shader- \_ Bytecode ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ Shader- \_ Bytecode.

</dd> <dt>

**expliziter CD3DX12- \_ Shader- \_ Bytecode (konstant D3D12 \_ Shader- \_ Bytecode &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode, der mit dem Inhalt einer anderen [**D3D12 \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ Shader- \_ Bytecode (ID3DBlob \* pshaderblob)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode und initialisiert die folgenden Parameter:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pshaderblob

</dd> <dt>

**CD3DX12 \_ Shader \_ Bytecode (Konstante void \* \_ pshaderbytecode, size \_ T bytecodelta ength)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ Shader- \_ Bytecode und initialisiert die folgenden Parameter:

void \* \_ pshaderbytecode

Größe \_ T bytecodelta ength

</dd> <dt>

**Operator Konstanten D3D12 \_ Shader- \_ Bytecode& () Konstanten**
</dt> <dd>

Definiert den & Operator "Pass-by-Reference" für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ Shader- \_ Bytecode**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

