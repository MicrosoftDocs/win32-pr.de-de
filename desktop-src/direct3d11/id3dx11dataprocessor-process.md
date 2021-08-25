---
title: ID3DX11DataProcessor-Methode (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt. Verarbeitet Daten.
ms.assetid: be20b231-9c2e-4b4a-bdb1-cdc75552bf9d
keywords:
- Prozessmethode Direct3D 11
- Prozessmethode Direct3D 11 , ID3DX11DataProcessor-Schnittstelle
- ID3DX11DataProcessor-Schnittstelle Direct3D 11 , Process-Methode
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
ms.openlocfilehash: 458e7dc68c4a64099dc5cab327901fda38f8fd4e6cde4ca7d62e3def5472d86d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894920"
---
# <a name="id3dx11dataprocessorprocess-method"></a>ID3DX11DataProcessor::P rocess-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

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

*pData* \[ In\]
</dt> <dd>

Typ: **\* void**

Zeiger auf die zu verarbeitenden Daten.

</dd> <dt>

*cBytes* \[ In\]
</dt> <dd>

Typ: **[ **SIZE \_ T**](/windows/desktop/WinProg/windows-data-types)**

Größe der zu verarbeitenden Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="remarks"></a>Hinweise

Diese Methode wird von einer [**ID3DX11ThreadPump-Schnittstelle**](id3dx11threadpump.md)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX11DataProcessor](id3dx11dataprocessor.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

