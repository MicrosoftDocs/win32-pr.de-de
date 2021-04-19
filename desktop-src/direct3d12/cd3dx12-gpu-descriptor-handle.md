---
title: CD3DX12_GPU_DESCRIPTOR_HANDLE-Struktur (D3dx12. h)
description: Eine hilfsstruktur, um die einfache Initialisierung einer D3D12- \_ GPU- \_ Deskriptorhandle-Struktur zu ermöglichen \_ .
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- CD3DX12_GPU_DESCRIPTOR_HANDLE Struktur
topic_type:
- apiref
api_name:
- CD3DX12_GPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429d41d401b7d3e928bc4ab76850b36ae41b1e8a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106350663"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>CD3DX12 \_ GPU- \_ \_ Deskriptorhandle-Struktur

Eine hilfsstruktur, um die einfache Initialisierung einer [**D3D12- \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_GPU_DESCRIPTOR_HANDLE  : public D3D12_GPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_GPU_DESCRIPTOR_HANDLE(const D3D12_GPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_GPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            inline operator==( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  bool                            inline operator!=( _In_ const D3D12_GPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_GPU_DESCRIPTOR_HANDLE & operator=(const D3D12_GPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_GPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_GPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ GPU- \_ \_ Deskriptorhandle ()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12- \_ GPU- \_ \_ Deskriptorhandles.

</dd> <dt>

**explizites CD3DX12 \_ GPU- \_ \_ Deskriptorhandle (konstant D3D12 \_ GPU- \_ \_ Deskriptorhandle &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ GPU- \_ \_ Deskriptorhandles, das mit dem Inhalt einer anderen [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur initialisiert wird.

</dd> <dt>

**CD3DX12 \_ GPU- \_ \_ Deskriptorhandle (CD3DX12 \_ Standard)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ GPU- \_ \_ Deskriptorhandles, das mit Standardparametern initialisiert wird (legt den Zeiger auf NULL fest).

</dd> <dt>

**CD3DX12 \_ GPU- \_ \_ Deskriptorhandle (konstant D3D12 \_ GPU- \_ \_ Deskriptorhandle &Sonstiges, int offsetscaledbyincrementsize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ GPU- \_ \_ Deskriptorhandles und initialisiert die folgenden Parameter:

D3D12 \_ GPU- \_ \_ Deskriptorhandle &anderen

INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.

</dd> <dt>

**CD3DX12 \_ GPU- \_ \_ Deskriptorhandle (const D3D12 \_ GPU- \_ Deskriptorhandle \_ &Sonstiges, int offsetindescriptors, uint descriptorincrementsize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12- \_ GPU- \_ \_ Deskriptorhandles und initialisiert die folgenden Parameter:

D3D12 \_ GPU- \_ \_ Deskriptorhandle &anderen

INT offsetindescriptors: die Anzahl der Deskriptoren, um die Inkrement erhöht werden soll.

Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.

</dd> <dt>

**Offset (int offsetindescriptors, uint descriptorincrementsize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Deskriptoren und dem für jeden Deskriptor zu Inkrement enden Wert fest. Verwendet die folgenden Parameter:

INT offsetindescriptors: die Anzahl der Deskriptoren, um die Inkrement erhöht werden soll.

Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.

</dd> <dt>

**Offset (int offsetscaledbyincrementsize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Inkrementen fest. Verwendet die folgenden Parameter:

INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.

</dd> <dt>

**Inline Operator = = ( \_ in \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle& anderen) Konstanten**
</dt> <dd>

Testet auf Gleichheit zwischen dem aktuellen CD3DX12 \_ \_ -GPU-Deskriptorhandle \_ und dem angegebenen D3D12 GPU-Deskriptorhandle \_ \_ \_ oder CD3DX12-GPU- \_ \_ Deskriptorhandle \_ .

</dd> <dt>

**Inline Operator! = ( \_ in \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle& anderen) Konstanten**
</dt> <dd>

Testet die Ungleichheit zwischen dem aktuellen CD3DX12 \_ \_ -GPU-Deskriptorhandle \_ und dem angegebenen D3D12 GPU-Deskriptorhandle \_ \_ \_ oder CD3DX12-GPU- \_ \_ Deskriptorhandle \_ .

</dd> <dt>

**Operator = (Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &andere)**
</dt> <dd>

Legt das aktuelle CD3DX12- \_ GPU- \_ \_ Deskriptorhandle auf die gleichen Werte wie das angegebene D3D12 \_ GPU- \_ \_ Deskriptorhandle oder CD3DX12- \_ GPU- \_ Deskriptorhandle fest \_ .

</dd> <dt>

**Inline-initoffsetted ( \_ in \_ Konstanten D3D12 \_ GPU- \_ Deskriptorhandle \_ &Basis, int offsetscaledbyincrementsize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur mit der angegebenen Anzahl von Elementen. Verwendet die folgenden Parameter:

\_Im \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.

INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.

</dd> <dt>

**Inline-initoffsetted ( \_ in \_ const D3D12 \_ GPU- \_ Deskriptorhandle \_ &Base, int offsetindescriptors, uint descriptorincrementsize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe. Verwendet die folgenden Parameter:

\_Im \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.

INT offsetindescriptors: die Anzahl der Deskriptoren, nach denen versetzt werden soll.

Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.

</dd> <dt>

**statischer Inline-initoffsetted ( \_ out \_ D3D12 \_ GPU- \_ \_ Deskriptorhandle &handle, \_ in \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &Base, int offsetscaledbyincrementsize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ GPU- \_ \_ Deskriptorhandle &handle: gibt das resultierende D3D12 \_ GPU- \_ \_ Deskriptorhandle aus.

\_Im \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.

INT offsetscaledbyincrementsize: die Anzahl der Inkremente, um die der Offset erfolgt.

</dd> <dt>

**statischer Inline-initoffsetted ( \_ out \_ D3D12 \_ GPU- \_ \_ Deskriptorhandle &handle, \_ in \_ const D3D12 \_ GPU- \_ \_ Deskriptorhandle &Base, int offsetindescriptors, uint descriptorincrementsize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) -Struktur mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren für die angegebene Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ GPU- \_ \_ Deskriptorhandle &handle: gibt das resultierende D3D12 \_ GPU- \_ \_ Deskriptorhandle aus.

\_Im \_ Konstanten D3D12 \_ GPU- \_ \_ Deskriptorhandle &Basis: die Basisadresse, von der abgeglichen werden soll.

INT offsetindescriptors: die Anzahl der Deskriptoren, nach denen versetzt werden soll.

Uint descriptorincrementsize: der Betrag, um den für jeden Deskriptor erhöht werden soll, einschließlich Padding.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D3D12- \_ GPU- \_ \_ Deskriptorhandle**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





