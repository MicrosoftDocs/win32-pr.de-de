---
description: Verarbeiten einiger Daten.
ms.assetid: c64f6a2d-4512-4028-8ed9-bfc5e9e86758
title: ID3DX10DataProcessor::P rocess-Methode (d3dx10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.Process
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 2ddad2f6350f48f65bc82e094eccb92b1b8bf390
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219725"
---
# <a name="id3dx10dataprocessorprocess-method"></a>ID3DX10DataProcessor::P rocess-Methode

Verarbeiten einiger Daten.

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

Typ: **[ **Größe \_ T**](../winprog/windows-data-types.md)**

Die Größe der zu verarbeitenden Daten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der Werte, die in [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)aufgelistet sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx10. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D3dx10. lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ID3DX10DataProcessor](id3dx10dataprocessor.md)
</dt> <dt>

[D3DX-Schnittstellen](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
