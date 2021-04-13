---
description: Erstellen Sie das beste Direct3D-Gerät und eine SwapChain.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: D3DX10CreateDeviceAndSwapChain-Funktion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDeviceAndSwapChain
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: fe71aeae91f8c43966e0fda2d2f430c7908f2855
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355547"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain-Funktion

Erstellen Sie das beste Direct3D-Gerät und eine SwapChain.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateDeviceAndSwapChain(
  _In_  IDXGIAdapter         *pAdapter,
  _In_  D3D10_DRIVER_TYPE    DriverType,
  _In_  HMODULE              Software,
  _In_  UINT                 Flags,
  _In_  DXGI_SWAP_CHAIN_DESC *pSwapChainDesc,
  _Out_ IDXGISwapChain       **ppSwapChain,
  _Out_ ID3D10Device         **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*padapter* \[ in\]
</dt> <dd>

Typ: **[ **idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Zeiger auf einen [**idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ in\]
</dt> <dd>

Type: **[ **d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Der Typ des Treibers für das Gerät. Siehe [**d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type).

</dd> <dt>

*Software* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Ein Handle für die dll, die einen Software-Rasterizer implementiert. Muss **null** sein, wenn der DriverType nicht-Software ist. Das HMODULE einer DLL kann mit [LoadLibrary](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)oder [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Dies ist optional. Geräteerstellungsflags (siehe [**d3d10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)), die [API-Ebenen](d3d10-graphics-programming-guide-api-features-layers.md)aktivieren. Diese Flags können bitweise oder gleich sein.

</dd> <dt>

*ptauapchaindesc* \[ in\]
</dt> <dd>

Typ: **[ **DXGI- \_ Austausch \_ Kette \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Die Beschreibung der Austausch Kette. Weitere Informationen finden Sie unter [**DXGI \_ Swap \_ Chain \_**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)Debug.

</dd> <dt>

*ppswapchain* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **idxgiswapchain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Adresse eines Zeigers auf eine [**idxgiswapchain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppdevice* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf eine [**ID3D10Device-Schnittstelle**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) , die das neu erstellte Gerät empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Um das beste Gerät zu erstellen, implementiert diese Methode mehr als eine Geräte Erstellungs Option. Zuerst versucht die-Methode, ein 10,1-Gerät (und eine SwapChain) zu erstellen. Wenn dies fehlschlägt, versucht die Methode, ein 10,0-Gerät zu erstellen. Wenn dies fehlschlägt, schlägt die Methode fehl. Wenn Ihre Anwendung nur ein 10,1-Gerät oder nur ein 10,0-Gerät erstellen muss, verwenden Sie stattdessen diese APIs:

-   Verwenden Sie [**D3D10CreateDeviceAndSwapChain**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) , um ein Gerät vom Typ Direct3D 10,0 (nur) und eine Austausch Kette zu erstellen.
-   Verwenden Sie [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) , um ein Gerät vom Typ Direct3D 10,1 (nur) und eine Austausch Kette zu erstellen.

Diese Methode erfordert Windows Vista Service Pack 1.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
