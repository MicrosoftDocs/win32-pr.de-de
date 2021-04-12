---
description: Erstellt ein DXVA-Decodergerät (DirectX Video Acceleration).
ms.assetid: aeebf65f-1bde-4a33-87cd-25c62dcc0248
title: 'IDirect3DVideoDevice9:: kreatedxvadevice-Methode (DXVA. h)'
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
ms.openlocfilehash: 50ce7cee350479f4286921b6cdf69b319033c721
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130341"
---
# <a name="idirect3dvideodevice9createdxvadevice-method"></a>IDirect3DVideoDevice9:: kreatedxvadevice-Methode

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

*pguid* 
</dt> <dd>

Zeiger auf eine GUID, die das zu Erstell Bare Gerät angibt.

</dd> <dt>

*puncompdata* 
</dt> <dd>

Ein Zeiger auf eine [**dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) -Struktur, die das Format des nicht komprimierten Bilds angibt.

</dd> <dt>

*pData* 
</dt> <dd>

Zeiger auf eine **DXVA- \_ ConnectMode** -Struktur, die den DXVA-Modus und das eingeschränkte Profil angibt.

</dd> <dt>

*DataSize* 
</dt> <dd>

Größe der **DXVA- \_ ConnectMode** -Struktur in Bytes.

</dd> <dt>

*ppdxvadevice* 
</dt> <dd>

Empfängt einen Zeiger auf die [**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md) -Schnittstelle. Der Aufrufer muss die-Schnittstelle freigeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 




