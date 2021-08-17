---
title: GetRequiredIntermediateSize-Funktion (D3dx12.h)
description: Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll.
ms.assetid: 424B52E9-DE52-40D2-B8B0-C27FD3D3C298
keywords:
- GetRequiredIntermediateSize-Funktion
topic_type:
- apiref
api_name:
- GetRequiredIntermediateSize
api_location:
- D3D12.dll
api_type:
- DllExport
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2f6fe927d49bb50d6bdea2889d946c5d9c60b1b703299c2717b881afe1aa7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124178"
---
# <a name="getrequiredintermediatesize-function"></a>GetRequiredIntermediateSize-Funktion

Gibt die erforderliche Größe eines Puffers zurück, der für den Datenupload verwendet werden soll.

## <a name="syntax"></a>Syntax


```C++
UINT64 inline GetRequiredIntermediateSize(
  _In_ ID3D12Resource *pDestinationResource,
  _In_ UINT           FirstSubresource,
  _In_ UINT           NumSubresources
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDestinationResource* \[ In\]
</dt> <dd>

Typ: **[ **ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)\***

Ein Zeiger auf die [**ID3D12Resource-Schnittstelle,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource) die die Zielressource darstellt.

</dd> <dt>

*FirstSubresource* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Der Index der ersten Unterressource in der Ressource. Der Bereich gültiger Werte ist 0 bis D3D12 \_ REQ \_ SUBRESOURCES.

</dd> <dt>

*NumSubresources* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

Die Anzahl der Unterressourcen in der Ressource. Der Bereich gültiger Werte ist 0 bis (D3D12 \_ REQ \_ SUBRESOURCES – *FirstSubresource*).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **UINT64**](/windows/desktop/WinProg/windows-data-types)**

Die Größe des Puffers in Bytes.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx12.h</dt> </dl>  |
| Bibliothek<br/> | <dl> <dt>D3D12.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D3D12.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Funktionen des Hilfsprogramms für D3D12](helper-functions-for-d3d12.md)
</dt> </dl>

 

