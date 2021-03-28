---
title: ID3DX11DataProcessor Process-Methode (D3DX11core. h)
description: Beachten Sie, dass die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) für Windows 8 veraltet ist und für Windows Store-Apps nicht unterstützt wird. Verarbeitet Daten.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Prozess Methode Direct3D 11
- Process Method Direct3D 11, ID3DX11DataProcessor Interface
- ID3DX11DataProcessor-Schnittstelle Direct3D 11, Prozess Methode
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.Process
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6127d62398d212c94669fadaaa2ecb09819d0171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530950"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor::P rocess-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt.

 

Verarbeitet Daten.

## <a name="syntax"></a>Syntax


```C++
HRESULT Process(
  [in] void   *pData,
  [in] SIZE_T cBytes
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Typ: **void \***

Zeiger auf die zu verarbeitenden Daten.

</dd> <dt>

*cbytes* \[ in\]
</dt> <dd>

Typ: **[ **Größe \_ T**](/windows/desktop/WinProg/windows-data-types)**

Die Größe der zu verarbeitenden Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 11-Rückgabe Codes](d3d11-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von einer [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)verwendet.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>Bibliothek d3dx11. lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

