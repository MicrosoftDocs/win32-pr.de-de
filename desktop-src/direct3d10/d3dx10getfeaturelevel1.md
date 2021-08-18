---
description: Hier erhalten Sie einen Direct3D 10.1-Geräteschnittstellenzeiger von einem Direct3D 10.0-Schnittstellenzeiger.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: D3DX10GetFeatureLevel1-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: c6511e0d3963e21f8950529b32cf8c3b414cc00b0625b97b2a9d569d1523c326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753170"
---
# <a name="d3dx10getfeaturelevel1-function"></a>D3DX10GetFeatureLevel1-Funktion

Hier erhalten Sie einen Direct3D 10.1-Geräteschnittstellenzeiger von einem Direct3D 10.0-Schnittstellenzeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDevice* \[ In\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf das Direct3D 10.0-Gerät (siehe [**ID3D10Device-Schnittstelle).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Zeiger auf das Direct3D 10.1-Gerät (siehe [**ID3D10Device1-Schnittstelle).**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md) Wenn eine Direct3D 10.1-Geräteschnittstelle erworben werden kann, ist diese Funktion erfolgreich und übergibt mithilfe des *ppDevice-Parameters* einen Zeiger auf die 10.1-Schnittstelle. Wenn eine Direct3D 10.1-Geräteschnittstelle nicht erworben werden kann, gibt diese Funktion E FAIL zurück und gibt nichts für den \_ *ppDevice-Parameter* zurück.

## <a name="remarks"></a>Hinweise

Damit diese Funktion erfolgreich ist, müssen Sie den angegebenen [**ID3D10Device-Zeiger**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) mithilfe eines Aufrufs der [**D3DX10CreateDevice-Funktion,**](d3dx10createdevice.md) der [**D3DX10CreateDeviceAndSwapChain-Funktion,**](d3dx10createdeviceandswapchain.md) der [**D3D10CreateDevice1-Funktion**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) oder der [**D3D10CreateDeviceAndSwapChain1-Funktion**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) erhalten haben.

Sie können ein Direct3D 10.1-Gerät nur auf Computern mit Windows Vista Service Pack 1 oder höher und mit installierter Direct3D 10.1-kompatibler Hardware erstellen. Diese Funktion gibt E \_ FAIL auf jedem Computer zurück, der diese Anforderungen nicht erfüllt. Sie können diese Funktion jedoch für jede Version von aufrufen Windows auf der die D3DX10-DLL installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




