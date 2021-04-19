---
title: Memcpysubresource-Funktion (D3dx12. h)
description: Kopiert eine untergeordnete Quelle zeilenweise.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- Memcpysubresource-Funktion
topic_type:
- apiref
api_name:
- MemcpySubresource
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b955211a490927033186442480b3449773b4ebcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106370446"
---
# <a name="memcpysubresource-function"></a>Memcpysubresource-Funktion

Kopiert eine untergeordnete Quelle zeilenweise.

## <a name="syntax"></a>Syntax


```C++
void inline MemcpySubresource(
  _In_ const D3D12_MEMCPY_DEST      *pDest,
  _In_ const D3D12_SUBRESOURCE_DATA *pSrc,
             SIZE_T                 RowSizeInBytes,
             UINT                   NumRows,
             UINT                   NumSlices
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdest* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ memcpy \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Ein Zeiger auf eine [**D3D12 \_ memcpy \_ dest**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) -Struktur, die das Ziel des Speicher Kopiervorgangs beschreibt.

</dd> <dt>

*psrc* \[ in\]
</dt> <dd>

Typ: **Konstanten [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Ein Zeiger auf eine [**D3D12 \_ subresource- \_ Daten**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) Struktur, die die Quelle des Speicher Kopiervorgangs beschreibt.

</dd> <dt>

*Rowsizeinbytes* 
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

Die Größe (in Bytes) der einzelnen Zeilen.

</dd> <dt>

*NumRows* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl von Zeilen.

</dd> <dt>

*Numslices* 
</dt> <dd>

Typ: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Slices.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Beachten Sie auch die folgenden Methoden:

-   [**ID3D12Resource:: Write Items**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource:: Read fromsubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList:: copyresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12. h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

