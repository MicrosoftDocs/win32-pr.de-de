---
title: UpdateSubresources-Funktion (Stapelzuweisung) (D3dx12.h)
description: Aktualisiert Unterressourcen mit einer Stapelzuweisungsimplementierung.
ms.assetid: 2F30FDF1-4450-473E-AEA8-C5FF54260BCE
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
ms.openlocfilehash: 43ffe9dd9e519b402126976db8ceaf1aba32f6d36a73745c951bb6a8db52a7fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300445"
---
# <a name="updatesubresources-stack-allocating-function"></a>UpdateSubresources-Funktion (Stapelzuweisung)

Aktualisiert Unterressourcen mit einer Stapelzuweisungsimplementierung.

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

Die Befehlsliste als Zeiger auf eine [**ID3D12GraphicsCommandList.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12graphicscommandlist)

</dd> <dt>

*pDestinationResource* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die Zielressource als Zeiger auf eine [**ID3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*pIntermediate* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Die Zwischenressource als Zeiger auf eine [**ID3D12Resource.**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)

</dd> <dt>

*IntermediateOffset* 
</dt> <dd>

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Der Offset in Bytes zur Zwischenressource.

</dd> <dt>

*FirstSubresource* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten Unterressource in der Ressource. Gültige Werte reichen von 0 bis *MaxSubresources.*

</dd> <dt>

*NumSubresources* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Unterressourcen in der Ressource. Gültige Werte reichen von 1 bis (*MaxSubresources*  -  *FirstSubresource*).

</dd> <dt>

*pSrcData* \[ In\]
</dt> <dd>

Typ: **[ **D3D12 \_ SUBRESOURCE \_ DATA**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data)\***

Zeiger auf ein Array (mit der Länge *NumSubresources)* von Zeigern auf [**D3D12 \_ SUBRESOURCE \_ DATA-Strukturen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_subresource_data) mit Beschreibungen der für das Update verwendeten Unterressourcendaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Cookies in Bytes.

## <a name="remarks"></a>Hinweise

Die Deklaration dieser Funktion beginnt mit: `template <UINT MaxSubresources>`

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> <dt>

[Unterressourcen](subresources.md)
</dt> </dl>

 

