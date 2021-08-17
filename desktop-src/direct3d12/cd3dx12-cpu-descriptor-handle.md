---
title: CD3DX12_CPU_DESCRIPTOR_HANDLE-Struktur (D3dx12.h)
description: Eine Hilfsstruktur, um eine einfache Initialisierung einer D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur zu ermöglichen.
ms.assetid: 91736069-7D13-47B0-B78C-0F6F104F97EB
keywords:
- CD3DX12_CPU_DESCRIPTOR_HANDLE-Struktur
topic_type:
- apiref
api_name:
- CD3DX12_CPU_DESCRIPTOR_HANDLE
api_location:
- d3dx12.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7e6fd6ba75caccf19f3782e0c39581d1e652de0c4187c3c5a203bb5f3b7ceec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913077"
---
# <a name="cd3dx12_cpu_descriptor_handle-structure"></a>CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur

Eine Hilfsstruktur, um eine einfache Initialisierung einer [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) zu ermöglichen.

## <a name="syntax"></a>Syntax


```C++
struct CD3DX12_CPU_DESCRIPTOR_HANDLE  : public D3D12_CPU_DESCRIPTOR_HANDLE{
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE();
                                  explicit CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &o);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(CD3DX12_DEFAULT);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetScaledByIncrementSize);
                                  CD3DX12_CPU_DESCRIPTOR_HANDLE(const D3D12_CPU_DESCRIPTOR_HANDLE &other, INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetInDescriptors, UINT descriptorIncrementSize);
  CD3DX12_CPU_DESCRIPTOR_HANDLE&  Offset(INT offsetScaledByIncrementSize);
  bool                            operator==( _In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  bool                            operator!=(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE& other) const;
  CD3DX12_CPU_DESCRIPTOR_HANDLE & operator=(const D3D12_CPU_DESCRIPTOR_HANDLE &other);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            inline InitOffsetted(_In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetScaledByIncrementSize);
  void                            static inline InitOffsetted(_Out_ D3D12_CPU_DESCRIPTOR_HANDLE &handle, _In_ const D3D12_CPU_DESCRIPTOR_HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize);
};
```



## <a name="members"></a>Member

<dl> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE()**
</dt> <dd>

Erstellt eine neue, nicht initialisierte Instanz eines CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**Explicit CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &o)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE, initialisiert mit dem Inhalt einer anderen [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur.**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE (CD3DX12 \_ DEFAULT)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE, initialisiert mit Standardparametern (Zeiger auf 0 festgelegt).

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &andere, INT offsetScaledByIncrementSize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE und initialisiert die folgenden Parameter:

D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &andere

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE(const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &andere, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Erstellt eine neue Instanz eines CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE und initialisiert die folgenden Parameter:

D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &andere

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die inkrementiert werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**Offset(INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Deskriptoren und dem für jeden Deskriptor zu erhöhenden Wert fest. Verwendet die folgenden Parameter:

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die inkrementiert werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**Offset(INT offsetScaledByIncrementSize)**
</dt> <dd>

Legt den Offset basierend auf der angegebenen Anzahl von Inkrementen fest. Verwendet die folgenden Parameter:

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**operator==( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Überprüft die Gleichheit zwischen dem aktuellen CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE und dem angegebenen D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator!=( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE& other) const**
</dt> <dd>

Testet auf Ungleichheit zwischen dem aktuellen CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE und dem angegebenen D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE.

</dd> <dt>

**operator=(const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &andere)**
</dt> <dd>

Legt das aktuelle CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE auf die gleichen Werte wie das angegebene D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE oder CD3DX12 \_ CPU \_ DESCRIPTOR \_ HANDLE fest.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) mit der angegebenen Anzahl von Elementen. Verwendet die folgenden Parameter:

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**inline InitOffsetted( \_ In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die versetzt werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetScaledByIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &handle: Gibt das resultierende D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE aus.

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetScaledByIncrementSize: Die Anzahl der Inkremente, um die versetzt werden soll.

</dd> <dt>

**static inline InitOffsetted( \_ Out \_ D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &handle, In \_ \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base, INT offsetInDescriptors, UINT descriptorIncrementSize)**
</dt> <dd>

Initialisiert eine [**D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE-Struktur**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle) mit einem Offset unter Verwendung der angegebenen Anzahl von Deskriptoren der angegebenen Größe. Verwendet die folgenden Parameter:

\_Out \_ D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &handle: Gibt das resultierende D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE aus.

\_In \_ const D3D12 \_ CPU \_ DESCRIPTOR \_ HANDLE &base: Die Basisadresse, von der versetzt werden soll.

INT offsetInDescriptors: Die Anzahl der Deskriptoren, um die versetzt werden soll.

UINT descriptorIncrementSize: Der Betrag, um den für jeden Deskriptor, einschließlich Auffüllung, inkrementiert werden soll.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3dx12.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Strukturen des Hilfsprogramms für D3D12](helper-structures-for-d3d12.md)
</dt> </dl>

 

 





