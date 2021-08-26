---
title: CD3DX12_SHADER_BYTECODE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ SHADER \_ BYTECODE-Struktur zu ermöglichen.
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
ms.openlocfilehash: 5bd984268a8dcd083b2d42573c6fa0028d2b73e7a3daacecd3fefe41c68150db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988369"
---
# <a name="cd3dx12_shader_bytecode-structure"></a>CD3DX12 \_ SHADER \_ BYTECODE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ SHADER \_ BYTECODE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode) zu ermöglichen.

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

**CD3DX12 \_ SHADER \_ BYTECODE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ SHADER \_ BYTECODE.

</dd> <dt>

**explicit CD3DX12 \_ SHADER \_ BYTECODE(const D3D12 \_ SHADER \_ BYTECODE &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SHADER \_ BYTECODE, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ SHADER \_ BYTECODE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(ID3DBlob \* pShaderBlob)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SHADER \_ BYTECODE und initialisiert die folgenden Parameter:

[**ID3DBlob**](/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)) \* pShaderBlob

</dd> <dt>

**CD3DX12 \_ SHADER \_ BYTECODE(const void \* \_ pShaderBytecode, SIZE \_ T bytecodeLength)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ SHADER \_ BYTECODE und initialisiert die folgenden Parameter:

void \* \_ pShaderBytecode

SIZE \_ T bytecodeLength

</dd> <dt>

**operator const D3D12 \_ SHADER \_ BYTECODE&() const**
</dt> <dd>

Definiert den & Pass-by-Reference-Operator für den übergeordneten Strukturtyp.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ SHADER \_ BYTECODE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_bytecode)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

