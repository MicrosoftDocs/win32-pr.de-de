---
title: CD3DX12_GPU_DESCRIPTOR_HANDLE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur zu ermöglichen.
ms.assetid: 6E405AD6-D370-4B87-849A-C52D64C79BF7
keywords:
- CD3DX12_GPU_DESCRIPTOR_HANDLE-Struktur
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
ms.openlocfilehash: d8039b20be8898c7bc81e57926ab82cd662d9e8a702d2d7a720915a1e35bcc93
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461000"
---
# <a name="cd3dx12_gpu_descriptor_handle-structure"></a>CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) zu ermöglichen.

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

**CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**Explicit CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

</dd> <dt>

**CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ \_ GPU-DESCRIPTOR-HANDLES, \_ initialisiert mit Standardparametern (legt den Zeiger auf 0 fest).

</dd> <dt>

**CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &andere, INT offsetScaledByIncrementSize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ \_ GPU-DESCRIPTOR-HANDLES \_ und initialisiert die folgenden Parameter:

D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &andere

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ \_ GPU-DESCRIPTOR-HANDLES \_ und initialisiert die folgenden Parameter:

D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &andere

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die inkrementiert werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Deskriptoren und dem inkrementierenden Wert für jeden Deskriptor fest. Verwendet die folgenden Parameter:

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die inkrementiert werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**Offset(INT offsetScaledByIncrementSize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Inkrementen fest. Verwendet die folgenden Parameter:

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**inline operator==( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Überprüft die Gleichheit zwischen dem aktuellen CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE und dem angegebenen D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**inline operator!=( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Testet auf Ungleichheit zwischen dem aktuellen CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE und dem angegebenen D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator=(const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &andere)**
</dt> <dd>

Legt das aktuelle CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE auf die gleichen Werte wie das angegebene D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ GPU \_ DESCRIPTOR \_ HANDLE fest.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) mit der angegebenen Anzahl von Elementen. Verwendet die folgenden Parameter:

\_In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die versetzt werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle: Gibt das resultierende D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE aus.

\_In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &handle: Gibt das resultierende D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE aus.

\_In \_ const D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die versetzt werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**D3D12 \_ GPU \_ DESCRIPTOR \_ HANDLE**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)
</dt> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





