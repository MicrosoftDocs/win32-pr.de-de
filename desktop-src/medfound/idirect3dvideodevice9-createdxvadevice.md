---
description: Erstellt ein DXVA-Decodergerät (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: IDirect3DVideoDevice9::CreateDXVADevice-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.CreateDXVADevice
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 4f70f976487db270145c8587107499f3c4e84ad85dacf99bec21050a2684b723
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555730"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>IDirect3DVideoDevice9::CreateDXVADevice-Methode

Erstellt ein DXVA-Decodergerät (DirectX Video Acceleration).

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateDXVADevice(
   GUID                 *pGuid,
   DXVAUncompDataInfo   *pUncompData,
   LPVOID               pData,
   DWORD                DataSize,
   IDirect3DDXVADevice9 **ppDXVADevice
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* 
</dt> <dd>

Zeiger auf eine GUID, die das zu erstellende Gerät angibt.

</dd> <dt>

*pUncompData* 
</dt> <dd>

Zeiger auf eine [**DXVAUncompDataInfo-Struktur,**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) die das Format des nicht komprimierten Bilds angibt.

</dd> <dt>

*Pdata* 
</dt> <dd>

Zeiger auf eine **DXVA \_ ConnectMode-Struktur,** die den DXVA-Modus und das eingeschränkte Profil angibt.

</dd> <dt>

*Datasize* 
</dt> <dd>

Größe der **DXVA \_ ConnectMode-Struktur** in Bytes.

</dd> <dt>

*ppDXVADevice* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IDirect3DDXVADevice9-Schnittstelle.**](idirect3ddxvadevice9.md) Der Aufrufer muss die Schnittstelle freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




