---
title: ID3DX11DataProcessor CreateDeviceObject-Methode (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Erstellt ein Geräteobjekt.
ms.assetid: 797d216b-2f54-4d24-aa97-04be0c71f909
keywords:
- CreateDeviceObject-Methode Direct3D 11
- CreateDeviceObject-Methode Direct3D 11 , ID3DX11DataProcessor-Schnittstelle
- ID3DX11DataProcessor-Schnittstelle Direct3D 11 , CreateDeviceObject-Methode
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor.CreateDeviceObject
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15627fc823de8a46a1299607f74694a0f93236082423910adf395b2b00ad57f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894930"
---
# <a name="id3dx11dataprocessorcreatedeviceobject-method"></a>ID3DX11DataProcessor::CreateDeviceObject-Methode

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

Erstellt ein Geräteobjekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppDataObject* \[ out\]
</dt> <dd>

Typ: **\* \* void**

Adresse eines Zeigers auf das erstellte Geräteobjekt.

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

 

 





