---
description: Sie erhalten einen Direct3D 10,1-Geräteschnittstellen Zeiger von einem Direct3D 10,0-Schnittstellen Zeiger.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: D3DX10GetFeatureLevel1-Funktion (D3DX10Core. h)
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
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106351921"
---
# <a name="d3dx10getfeaturelevel1-function"></a>D3DX10GetFeatureLevel1-Funktion

Sie erhalten einen Direct3D 10,1-Geräteschnittstellen Zeiger von einem Direct3D 10,0-Schnittstellen Zeiger.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pdevice* \[ in\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***

Zeiger auf das Direct3D 10,0-Gerät (siehe die [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstelle).

</dd> <dt>

*ppdevice* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***

Zeiger auf das Direct3D 10,1-Gerät (siehe die [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) -Schnittstelle).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück. Wenn eine Direct3D 10,1-Geräteschnittstelle abgerufen werden kann, ist diese Funktion erfolgreich und übergibt mithilfe des *ppdevice* -Parameters einen Zeiger an die 10,1-Schnittstelle. Wenn eine Direct3D 10,1-Geräteschnittstelle nicht abgerufen werden kann, gibt diese Funktion "E Fail" zurück \_ und gibt für den *ppdevice* -Parameter nichts zurück.

## <a name="remarks"></a>Bemerkungen

Damit diese Funktion erfolgreich ausgeführt wird, müssen Sie den bereitgestellten [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Zeiger mithilfe eines Aufrufes der [**D3DX10CreateDevice**](d3dx10createdevice.md) -Funktion, der [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) -Funktion, der [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) -Funktion oder der [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) -Funktion abgerufen haben.

Sie können auf Computern, auf denen Windows Vista Service Pack 1 oder höher ausgeführt wird, und bei installierter Direct3D 10,1-kompatibler Hardware nur ein Direct3D 10,1-Gerät erstellen. Diese Funktion gibt "E \_ Fail" auf allen Computern zurück, die diese Anforderungen nicht erfüllen. Sie können diese Funktion jedoch für jede Windows-Version mit installierter d3dx10-dll-Version aufzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




