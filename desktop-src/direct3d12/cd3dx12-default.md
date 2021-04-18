---
title: CD3DX12_DEFAULT-Struktur (D3dx12. h)
description: Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur. Diese Struktur wird einfach als Mechanismus verwendet, um Standardparameter für die anderen Hilfsstrukturen festzulegen.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT Struktur
topic_type:
- apiref
api_name:
- CD3DX12_DEFAULT
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b010e8f0fdce67f16750d0f66d1cf272c8ddb849
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354352"
---
# <a name="cd3dx12_default-structure"></a>CD3DX12- \_ Standardstruktur

Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur. Diese Struktur wird einfach als Mechanismus verwendet, um Standardparameter für die anderen Hilfsstrukturen festzulegen.

## <a name="remarks"></a>Bemerkungen

Diese Struktur wird wie folgt deklariert:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Übergibt D3D12 \_ default an einen Konstruktor für jede hilfsstruktur. Der folgende Konstruktor wird z. b. in d3dx12. h deklariert:

CD3DX12- \_ CPU- \_ \_ Deskriptorhandle (CD3DX12 \_ Standard) {PTR = 0;}

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





