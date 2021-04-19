---
description: Erstellen Sie das beste Direct3D 10-Gerät, das den Anzeige Adapter darstellt. Wenn ein Direct3D 10,1-kompatibles Gerät erstellt werden kann, ist es möglich, einen ID3D10Device1-Schnittstellen Zeiger vom zurückgegebenen Geräteschnittstellen Zeiger zu erhalten.
ms.assetid: 1af8f4e5-a59e-403a-95d2-069b91bad93e
title: D3DX10CreateDevice-Funktion (D3DX10Core. h)
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
ms.openlocfilehash: 38236a48cdd5197f7f19ef9be3f6fc0f1faca72c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106355828"
---
# <a name="d3dx10createdevice-function"></a>D3DX10CreateDevice-Funktion

Erstellen Sie das beste Direct3D 10-Gerät, das den Anzeige Adapter darstellt. Wenn ein Direct3D 10,1-kompatibles Gerät erstellt werden kann, ist es möglich, einen [**ID3D10Device1-Schnittstellen**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) Zeiger vom zurückgegebenen Geräteschnittstellen Zeiger zu erhalten.

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

*padapter* \[ in\]
</dt> <dd>

Typ: **[ **idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter)\***

Zeiger auf den Anzeige Adapter (siehe die [**idxgiadapter**](/windows/win32/api/dxgi/nn-dxgi-idxgiadapter) -Schnittstelle), wenn ein Hardware Gerät erstellt wird. andernfalls legen Sie diesen Parameter auf **null** fest. Wenn beim Erstellen eines Hardware Geräts **null** angegeben wird, verwendet Direct3D den ersten Adapter, der von der [**idxgifactory**](/windows/win32/api/dxgi/nn-dxgi-idxgifactory) -Schnittstelle aufgezählt wird.

</dd> <dt>

*DriverType* \[ in\]
</dt> <dd>

Type: **[ **d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type)**

Der Gerätetreiber-Typ (siehe [**d3d10 \_ Driver \_ Type**](/windows/desktop/api/D3D10misc/ne-d3d10misc-d3d10_driver_type) Enumeration). Der Treibertyp bestimmt den Gerätetyp, den Sie erstellen.

</dd> <dt>

*Software* \[ in\]
</dt> <dd>

Typ: **[ **HMODULE**](../winprog/windows-data-types.md)**

Ein Handle für ein geladenes Modul, das einen Software Treiber (z. b. D3D10Ref.dll) implementiert. Zum Abrufen eines Handles aufrufen Sie die [GetModuleHandle](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion.

</dd> <dt>

*Flags* \[in\]
</dt> <dd>

Typ: **[ **uint**](../winprog/windows-data-types.md)**

Geräteerstellungsflags (siehe [**d3d10 \_ Create \_ Device \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_create_device_flag) Enumeration) zum Aktivieren von API- [Ebenen](d3d10-graphics-programming-guide-api-features-layers.md). Diese Flags können bitweise oder gleich sein.

</dd> <dt>

*ppdevice* \[ vorgenommen\]
</dt> <dd>

Typ: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***

Adresse eines Zeigers auf das erstellte Gerät (siehe die [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstelle).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Diese Funktion gibt einen der folgenden [Direct3D 10-Rückgabe Codes](d3d10-graphics-reference-returnvalues.md)zurück.

## <a name="remarks"></a>Bemerkungen

Diese Funktion versucht, das beste Gerät für die Hardware zu erstellen. Zuerst versucht die Funktion, ein 10,1-Gerät zu erstellen. Wenn ein 10,1-Gerät nicht erstellt werden kann, versucht die Funktion, ein 10,0-Gerät zu erstellen. Wenn keines der Geräte erfolgreich erstellt wurde, gibt die Funktion E \_ Fail zurück.

Wenn Ihre Anwendung nur ein 10,1-Gerät oder nur ein 10,0-Gerät erstellen muss, verwenden Sie stattdessen die folgenden Funktionen:

-   Verwenden Sie die [**D3D10CreateDevice**](/windows/desktop/api/D3D10Misc/nf-d3d10misc-d3d10createdevice) -Funktion, um nur ein Direct3D 10,0-Gerät zu erstellen.
-   Verwenden Sie die [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) -Funktion, um nur ein Direct3D 10,1-Gerät zu erstellen.
-   Verwenden Sie die [**D3DX10GetFeatureLevel1**](d3dx10getfeaturelevel1.md) -Funktion, um einen [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) -Schnittstellen Zeiger von einem [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) -Schnittstellen Zeiger zu erhalten.

Ein Direct3D 10,1-Gerät kann nur auf Computern erstellt werden, auf denen Windows Vista Service Pack 1 oder höher ausgeführt wird, und auf denen Direct3D 10,1-kompatible Hardware installiert ist. Es ist jedoch zulässig, diese Funktion auf Computern mit einer beliebigen Windows-Version aufzurufen, auf der die d3dx10-dll installiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3DX10Core. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Universell Funktionen](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
