---
description: 'D3DX10CheckVersion-Funktion: Stellen Sie sicher, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.'
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: D3DX10CheckVersion-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4fc8befa88fb706965a30224843745b033ea205b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105348"
---
# <a name="d3dx10checkversion-function"></a>D3DX10CheckVersion-Funktion

Stellen Sie sicher, dass die Version von D3DX, mit der Sie kompiliert haben, die Version ist, die Sie ausführen.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*D3DSdkVersion* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Verwenden Sie die D3D10 \_ \_ SDK-VERSION. Siehe Bemerkungen.

</dd> <dt>

*D3DX10SdkVersion* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Verwenden Sie die D3DX10 \_ \_ SDK-VERSION. Siehe Bemerkungen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Wenn die Version nicht entspricht, gibt die Funktion FALSE zurück (eine Zahl kleiner oder gleich 0, die Zahl selbst hat keine Bedeutung).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion während der Initialisierung Ihrer Anwendung.


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10Core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX10.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
