---
description: Erstellen Sie das beste Direct3D-Gerät und eine Austauschkette.
ms.assetid: c320a6c4-fa68-47fc-b2cb-0dc53c2767e7
title: D3DX10CreateDeviceAndSwapChain-Funktion (D3DX10Core.h)
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
ms.openlocfilehash: aa92b0fd7efb9c6f457fd035fad28992d965a4cf2f6fdad39936292f7a70a996
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119852370"
---
# <a name="d3dx10createdeviceandswapchain-function"></a>D3DX10CreateDeviceAndSwapChain-Funktion

Erstellen Sie das beste Direct3D-Gerät und eine Austauschkette.

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

*pAdapter* \[ In\]
</dt> <dd>

Typ: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Zeiger auf einen [**IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter).

</dd> <dt>

*DriverType* \[ In\]
</dt> <dd>

Typ: **[ **D3D10 \_ DRIVER \_ TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Der Typ des Treibers für das Gerät. Siehe [**D3D10 DRIVER TYPE (D3D10-TREIBERTYP). \_ \_**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)

</dd> <dt>

*Software* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Ein Handle für die DLL, die einen Softwareraster implementiert. Muss **NULL** sein, wenn DriverType nicht Software ist. Das HMODULE einer DLL kann mit [LoadLibrary,](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [LoadLibraryEx](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)oder [GetModuleHandle](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)abgerufen werden.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Optional. Geräteerstellungsflags (siehe [**D3D10 \_ CREATE \_ DEVICE \_ FLAG),**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag)die [API-Ebenen](d3d10-graphics-programming-guide-api-features-layers.md)aktivieren. Diese Flags können bitweise OR'd sein.

</dd> <dt>

*pSwapChainDesc* \[ In\]
</dt> <dd>

Typ: **[ **DXGI \_ SWAP \_ CHAIN \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc)\***

Beschreibung der Swapkette. Weitere Informationen finden Sie unter [**DXGI \_ SWAP CHAIN \_ \_ DESC**](/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc).

</dd> <dt>

*ppSwapChain* \[ out\]
</dt> <dd>

Typ: **[ **IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain)\*\***

Adresse eines Zeigers auf eine [**IDXGISwapChain**](/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain).

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf eine [**ID3D10Device-Schnittstelle,**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) die das neu erstellte Gerät empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Methode gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Um das beste Gerät zu erstellen, implementiert diese Methode mehr als eine Geräteerstellungsoption. Zuerst versucht die -Methode, ein 10.1-Gerät (und eine Austauschkette) zu erstellen. Wenn dies fehlschlägt, versucht die -Methode, ein 10.0-Gerät zu erstellen. Wenn dies fehlschlägt, schlägt die Methode fehl. Wenn Ihre Anwendung nur ein 10.1-Gerät oder nur ein 10.0-Gerät erstellen muss, verwenden Sie stattdessen diese APIs:

-   Verwenden Sie [**D3D10CreateDeviceAndSwapChain,**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdeviceandswapchain) um ein Direct3D 10.0-Gerät (nur) und eine Austauschkette zu erstellen.
-   Verwenden Sie [**D3D10CreateDeviceAndSwapChain1,**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) um ein Direct3D 10.1-Gerät und eine Austauschkette (nur) zu erstellen.

Für diese Methode ist Windows Vista Service Pack 1 erforderlich.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
