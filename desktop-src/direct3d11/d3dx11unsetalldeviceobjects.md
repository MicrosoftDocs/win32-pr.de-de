---
title: D3DX11UnsetAllDeviceObjects-Funktion (D3DX11core.h)
description: Hinweis Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store-Apps nicht unterstützt. Hinweis Anstatt diese Funktion zu verwenden, wird empfohlen, die ID3D11DeviceContext ClearState-Methode zu verwenden.
ms.assetid: 0e52bbca-f171-477f-89b0-ba56a2cfa096
keywords:
- D3DX11UnsetAllDeviceObjects-Funktion Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11UnsetAllDeviceObjects
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e046bbb67cfaf5e13a22e5b704e202c21ebc8fa82dfde3a21fb83f09dfc3a345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535971"
---
# <a name="d3dx11unsetalldeviceobjects-function"></a>D3DX11UnsetAllDeviceObjects-Funktion

> [!Note]  
> Die Hilfsprogrammbibliothek D3DX (D3DX 9, D3DX 10 und D3DX 11) ist für Windows 8 veraltet und wird für Windows Store Apps nicht unterstützt.

 

> [!Note]  
> Anstatt diese Funktion zu verwenden, wird empfohlen, die [**ID3D11DeviceContext::ClearState-Methode**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-clearstate) zu verwenden.

 

Entfernt alle Ressourcen vom Gerät, indem deren Zeiger auf **NULL** festgelegt werden. Dies sollte beim Herunterfahren der Anwendung aufgerufen werden. Dadurch wird sichergestellt, dass beim Freigeben aller Ressourcen keines dieser Ressourcen an das Gerät gebunden ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX11UnsetAllDeviceObjects(
  _In_ ID3D11DeviceContext *pContext
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pContext* \[ In\]
</dt> <dd>

Typ: **[ **ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)\***

Zeiger auf ein [**ID3D11DeviceContext-Objekt.**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Der Rückgabewert ist einer der In [Direct3D 11-Rückgabecodes aufgeführten](d3d11-graphics-reference-returnvalues.md)Werte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX11core.h</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D3DX11.lib</dt> </dl>   |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[D3DX-Funktionen](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

 





