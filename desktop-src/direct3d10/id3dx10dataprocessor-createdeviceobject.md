---
description: Erstellen Sie ein Geräte Objekt.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'ID3DX10DataProcessor:: kreatedeviceobject-Methode (d3dx10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219537"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a>ID3DX10DataProcessor:: kreatedeviceobject-Methode

Erstellen Sie ein Geräte Objekt.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppdataobject* \[ vorgenommen\]
</dt> <dd>

Typ: **void \* \***

Adresse eines Zeigers auf das erstellte Geräte Objekt.

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

 

 




