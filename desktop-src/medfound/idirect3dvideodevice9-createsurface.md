---
description: Erstellt eine komprimierte Oberfläche für die Decodierung der DirectX-Videobeschleunigung (DXVA).
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: IDirect3DVideoDevice9::CreateSurface-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateSurface
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: b5bc624527c7ef3ea2a8bb9c878f1d97e865a54341ae5902449fb8a015374f3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887870"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9::CreateSurface-Methode

Erstellt eine komprimierte Oberfläche für die Decodierung der DirectX-Videobeschleunigung (DXVA).

Rufen Sie zum Erhalten der Oberflächenanforderungen [**IDirect3DVideoDevice9::GetDXVACompressedBufferInfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) auf, und untersuchen Sie die zurückgegebenen [**DXVACompBufferInfo-Strukturen.**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo)

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateSurface(
   UINT              Width,
   UINT              Height,
   UINT              BackBuffers,
   D3DFORMAT         Format,
   D3DPOOL           Pool,
   DWORD             Usage,
   IDirect3DSurface9 **ppSurface,
   HANDLE            *pSharedHandle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Width* 
</dt> <dd>

Die Breite der Oberfläche in Pixel. Legen Sie diesen Parameter auf **DXVACompBufferInfo.WidthToCreate fest.**

</dd> <dt>

*Height* 
</dt> <dd>

Die Höhe der Oberfläche in Pixel. Legen Sie diesen Parameter auf **DXVACompBufferInfo.HeightToCreate fest.**

</dd> <dt>

*BackBuffers* 
</dt> <dd>

Die Anzahl der Hintergrundpuffer. Dieser Parameter kann 0 (null) sein.

</dd> <dt>

*Format* 
</dt> <dd>

Das Als **D3DFORMAT-Wert** angegebene Pixelformat. Legen Sie diesen Parameter auf **DXVACompBufferInfo.Format fest.**

</dd> <dt>

*Pool* 
</dt> <dd>

Der Speicherpool, in dem die Oberfläche erstellt werden soll, angegeben als **D3DPOOL-Wert.** Legen Sie diesen Parameter auf **DXVACompBufferInfo.Pool fest.**

</dd> <dt>

*Verwendung* 
</dt> <dd>

Ein **bitweises OR** einer oder mehrere **D3DUSAGE-Konstanten.** Legen Sie diesen Parameter auf **DXVACompBufferInfo.Usage fest.**

</dd> <dt>

*ppSurface* 
</dt> <dd>

Empfängt einen Zeiger auf die **IDirect3DSurface9-Schnittstelle.** Der Aufrufer muss die Schnittstelle frei geben.

</dd> <dt>

*pSharedHandle* 
</dt> <dd>

Reserviert. Legen Sie auf **NULL fest.**

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




