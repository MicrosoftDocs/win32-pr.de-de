---
title: CD3DX12_DEFAULT -Struktur (D3dx12.h)
description: Übergibt D3D12 \_ DEFAULT an einen Konstruktor für jede Hilfsstruktur. Diese Struktur wird einfach als Mechanismus zum Festlegen von Standardparametern für die anderen Hilfsstrukturen verwendet.
ms.assetid: AD41FD7B-9172-400E-9292-374FFAEDE145
keywords:
- CD3DX12_DEFAULT-Struktur
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
ms.openlocfilehash: 876fbb5e666680e85854196fb9136bfd4d765d6eecf8f16bf6101bb321a7039a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531287"
---
# <a name="cd3dx12_default-structure"></a>CD3DX12 \_ DEFAULT-Struktur

Übergibt D3D12 \_ DEFAULT an einen Konstruktor für jede Hilfsstruktur. Diese Struktur wird einfach als Mechanismus zum Festlegen von Standardparametern für die anderen Hilfsstrukturen verwendet.

## <a name="remarks"></a>Hinweise

Diese Struktur wird wie folgt deklariert:

``` syntax
struct CD3DX12_DEFAULT {};
extern const DECLSPEC_SELECTANY CD3DX12_DEFAULT D3D12_DEFAULT;
```

Übergibt D3D12 \_ DEFAULT an einen Konstruktor für jede Hilfsstruktur. Beispielsweise wird der folgende Konstruktor in d3dx12.h deklariert:

CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(CD3DX12 \_ DEFAULT) { ptr = 0; }

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





