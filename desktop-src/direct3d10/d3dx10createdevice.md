---
description: Erstellen Sie das beste Direct3D 10-Gerät, das den Adapter darstellt. Wenn ein Direct3D 10.1-kompatibles Gerät erstellt werden kann, ist es möglich, einen ID3D10Device1-Schnittstellenzeiger vom zurückgegebenen Geräteschnittstellenzeiger zu erhalten.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: D3DX10CreateDevice-Funktion (D3DX10Core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateDevice
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 9300eb74027d25562dabb9a596face10105110d1750b359bcaae9ab6b2b83084
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634700"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice-Funktion

Erstellen Sie das beste Direct3D 10-Gerät, das den Adapter darstellt. Wenn ein Direct3D 10.1-kompatibles Gerät erstellt werden kann, ist es möglich, einen [**ID3D10Device1-Schnittstellenzeiger**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) vom zurückgegebenen Geräteschnittstellenzeiger zu erhalten.

## <a name="syntax"></a>Syntax


```C++
HRESULT D3DX10CreateDevice(
  _In_  IDXGIAdapter      *pAdapter,
  _In_  D3D10_DRIVER_TYPE DriverType,
  _In_  HMODULE           Software,
  _In_  UINT              Flags,
  _Out_ ID3D10Device      **ppDevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAdapter* \[ In\]
</dt> <dd>

Typ: **[ **IDXGIAdapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Zeiger auf den Adapter (siehe [**IDXGIAdapter-Schnittstelle)**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) beim Erstellen eines Hardwaregeräts; Legen Sie andernfalls diesen Parameter auf **NULL fest.** Wenn **BEIM** Erstellen eines Hardwaregeräts NULL angegeben wird, verwendet Direct3D den ersten Adapter, der von der [**IDXGIFactory-Schnittstelle aufzählt**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) wird.

</dd> <dt>

*DriverType* \[ In\]
</dt> <dd>

Typ: **[ **D3D10 \_ DRIVER \_ TYPE**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Der Gerätetreibertyp (siehe [**D3D10 \_ DRIVER \_ TYPE-Enumeration).**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) Der Treibertyp bestimmt den Typ des Geräts, das Sie erstellen.

</dd> <dt>

*Software* \[ In\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Ein Handle für ein geladenes Modul, das einen Softwaretreiber implementiert (z. B. D3D10Ref.dll). Um ein Handle zu erhalten, rufen Sie die [GetModuleHandle-Funktion](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) auf.

</dd> <dt>

*Flags* \[ In\]
</dt> <dd>

Typ: **[ **UINT**](../winprog/windows-data-types.md)**

Geräteerstellungsflags (siehe [**D3D10 \_ CREATE \_ DEVICE \_ FLAG-Enumeration),**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) die [API-Ebenen aktivieren.](d3d10-graphics-programming-guide-api-features-layers.md) Diese Flags können bitweise OR'd zusammen sein.

</dd> <dt>

*ppDevice* \[ out\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf das erstellte Gerät (siehe [**ID3D10Device-Schnittstelle).**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabecodes zurück.](d3d10-graphics-reference-returnvalues.md)

## <a name="remarks"></a>Hinweise

Diese Funktion versucht, das beste Gerät für die Hardware zu erstellen. Zunächst versucht die Funktion, ein 10.1-Gerät zu erstellen. Wenn ein 10.1-Gerät nicht erstellt werden kann, versucht die Funktion, ein 10.0-Gerät zu erstellen. Wenn keines der beiden Geräte erfolgreich erstellt wurde, gibt die Funktion E \_ FAIL zurück.

Wenn Ihre Anwendung nur ein 10.1-Gerät oder nur ein 10.0-Gerät erstellen muss, verwenden Sie stattdessen die folgenden Funktionen:

-   Verwenden Sie [**die Funktion D3D10CreateDevice,**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) um nur ein Direct3D 10.0-Gerät zu erstellen.
-   Verwenden Sie [**die Funktion D3D10CreateDevice1,**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) um nur ein Direct3D 10.1-Gerät zu erstellen.
-   Verwenden Sie [**die D3DX10GetFeatureLevel1-Funktion,**](d3dx10getfeaturelevel1.md) um einen [**ID3D10Device1-Schnittstellenzeiger**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) von einem [**ID3D10Device-Schnittstellenzeiger**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) zu erhalten.

Ein Direct3D 10.1-Gerät kann nur auf Computern mit Windows Vista Service Pack 1 oder höher und mit installierter Direct3D 10.1-kompatibler Hardware erstellt werden. Es ist jedoch legal, diese Funktion auf Computern auf einem beliebigen Computer auf Windows, auf dem die D3DX10-DLL installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Universell Functions](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
