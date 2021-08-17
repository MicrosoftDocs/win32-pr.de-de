---
title: MemcpySubresource-Funktion (D3dx12.h)
description: Kopiert eine Unterressourcenzeile nach Zeile.
ms.assetid: 33A9F99D-FD85-4FD6-AFD6-7A10F16C3D9B
keywords:
- MemcpySubresource-Funktion
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
ms.openlocfilehash: 8c27e8cf9ffda237c2dad017b3a981ff71498a22c1c7b54ede032d6bf8c012a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117733362"
---
# <a name="memcpysubresource-function"></a>MemcpySubresource-Funktion

Kopiert eine Unterressourcenzeile nach Zeile.

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

*pDest* \[ In\]
</dt> <dd>

Typ: **const [**D3D12 \_ MEMCPY \_ DEST**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) \***

Ein Zeiger auf eine [**D3D12 \_ MEMCPY \_ DEST-Struktur,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_memcpy_dest) die das Ziel des Speicherkopiervorgang beschreibt.

</dd> <dt>

*pSrc* \[ In\]
</dt> <dd>

Typ: **const [**D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) \***

Ein Zeiger auf eine [**D3D12 \_ SUBRESOURCE \_ DATA-Struktur,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) die die Quelle des Speicherkopiervorgang beschreibt.

</dd> <dt>

*RowSizeInBytes* 
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Die Größe jeder Zeile in Bytes.

</dd> <dt>

*NumRows* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl von Zeilen.

</dd> <dt>

*NumSlices* 
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Slices.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Berücksichtigen Sie außerdem die folgenden Methoden:

-   [**ID3D12Resource::WriteToSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-writetosubresource)
-   [**ID3D12Resource::ReadFromSubresource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12resource-readfromsubresource)
-   [**ID3D12GraphicsCommandList::CopyResource**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-copyresource)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

