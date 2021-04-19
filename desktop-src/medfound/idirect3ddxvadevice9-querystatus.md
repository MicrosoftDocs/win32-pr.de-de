---
description: Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche (DirectX Video Acceleration) ab.
ms.assetid: 8a4c3173-5911-49ec-8cb8-e30f96a4f1c9
title: 'IDirect3DDXVADevice9:: QueryStatus-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DDXVADevice9.QueryStatus
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: ae2b16ef27b1e172b7927652304104563e120709
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356833"
---
# <a name="idirect3ddxvadevice9querystatus-method"></a>IDirect3DDXVADevice9:: QueryStatus-Methode

Fragt den Lese-/Schreibstatus einer DXVA-Decodierungs Oberfläche (DirectX Video Acceleration) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT QueryStatus(
   IDirect3DSurface9 *pSurface,
   DWORD             Flags
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pSurface* 
</dt> <dd>

Ein Zeiger auf die **IDirect3DSurface9** -Schnittstelle der abzufragende Oberfläche.

</dd> <dt>

*Flags* 
</dt> <dd>

Gibt den Typ der auszuführenden Abfrage an.



| Wert                                                                                                                             | Bedeutung                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="0x00"></span><span id="0X00"></span><dl> <dt>**0x00**</dt> </dl> | Testen Sie, ob die Oberfläche sicher zum Schreiben verwendet werden kann.<br/> |
| <span id="0x01"></span><span id="0X01"></span><dl> <dt>**0x01**</dt> </dl> | Testen Sie, ob die Oberfläche sicher zum Lesen verwendet werden kann.<br/> |



 

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

[**IDirect3DDXVADevice9**](idirect3ddxvadevice9.md)
</dt> </dl>

 

 




