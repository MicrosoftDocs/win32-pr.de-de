---
title: UpdateSubresources-Funktion (Heapzuweisung) (D3dx12.h)
description: Aktualisiert Unterressourcen mit einer Heapzuweisungsimplementierung.
ms.assetid: 328D8755-D328-471D-AAF4-9771CBFF7539
keywords:
- UpdateSubresources-Funktion
topic_type:
- apiref
api_name:
- UpdateSubresources
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc4e476501c91c3e7508c0aefdc1d9d6c99a057840b5a126879c8b4ff3608f68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460751"
---
# <a name="updatesubresources-heap-allocating-function"></a>UpdateSubresources-Funktion (Heapzuweisung)

Aktualisiert Unterressourcen mit einer Heapzuweisungsimplementierung.

## <a name="syntax"></a>Syntax


```C++
UINT64 inline UpdateSubresources(
  _In_ ID3D12GraphicsCommandList *pCmdList,
  _In_ ID3D12Resource            *pDestinationResource,
  _In_ ID3D12Resource            *pIntermediate,
       UINT64                    IntermediateOffset,
  _In_ UINT                      FirstSubresource,
  _In_ UINT                      NumSubresources,
  _In_ D3D12_SUBRESOURCE_DATA    *pSrcData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pCmdList* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12GraphicsCommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)\***

Ein Zeiger auf die [**ID3D12GraphicsCommandList-Schnittstelle**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist) für die Befehlsliste.

</dd> <dt>

*pDestinationResource* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Ein Zeiger auf die [**ID3D12Resource-Schnittstelle,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) die die Zielressource darstellt.

</dd> <dt>

*pIntermediate* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Ein Zeiger auf die [**ID3D12Resource-Schnittstelle,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) die die Zwischenressource darstellt.

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Der Offset in Bytes zur Zwischenressource.

</dd> <dt>

*FirstSubresource* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten Unterressource in der Ressource. Der Bereich der gültigen Werte beträgt 0 bis D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Unterressourcen in der Ressource. Der Bereich der gültigen Werte beträgt 0 bis (D3D12 \_ REQ \_ SUBRESOURCES – *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Zeiger auf ein Array (der Länge *NumSubresources*) von Zeigern auf [**D3D12 \_ SUBRESOURCE \_ DATA-Strukturen,**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) die Beschreibungen der für das Update verwendeten Unterressourcendaten enthalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Cookies in Bytes.

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

 

