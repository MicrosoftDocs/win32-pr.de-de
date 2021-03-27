---
title: ID3DX11ThreadPump addworkitem-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Fügt der Thread Pumpe ein Arbeits Element hinzu.
ms.assetid: 2578506c-6175-457a-bf10-94929bb3c0c4
keywords:
- Addworkitem-Methode Direct3D 11
- Addworkitem-Methode Direct3D 11, ID3DX11ThreadPump-Schnittstelle
- ID3DX11ThreadPump Interface Direct3D 11, addworkitem-Methode
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump.AddWorkItem
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebf249405bd71287f93444ae8d23dab694027360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354276"
---
# <a name="id3dx11threadpumpaddworkitem-method"></a>ID3DX11ThreadPump:: addworkitem-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Fügt der Thread Pumpe ein Arbeits Element hinzu.

## <a name="syntax"></a>Syntax


```C++
HRESULT AddWorkItem(
  [in]  ID3DX11DataLoader    *pDataLoader,
  [in]  ID3DX11DataProcessor *pDataProcessor,
  [in]  HRESULT              *pHResult,
  [out] void                 **ppDeviceObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdataloader* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\***

Das Lade Modul, das vom threadpump verwendet wird, wenn ein Arbeits Element zum Laden von Daten benötigt wird.

</dd> <dt>

*pdataprocessor* \[ in\]
</dt> <dd>

Typ: **[ **ID3DX11DataProcessor**](id3dx11dataprocessor.md)\***

Der Prozessor, den das Thread-Pump-Element verwendet, wenn für eine Arbeitsaufgabe die Verarbeitung von Daten erforderlich ist.

</dd> <dt>

*phresult* \[ in\]
</dt> <dd>

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***

Ein Zeiger auf den Rückgabewert. Kann **null** sein.

</dd> <dt>

*ppdeviceobject* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Das Gerät, von dem das-Objekt verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11ThreadPump](id3dx11threadpump.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





