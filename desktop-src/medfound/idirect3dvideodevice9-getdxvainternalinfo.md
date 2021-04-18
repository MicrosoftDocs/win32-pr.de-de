---
description: Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab.
ms.assetid: 20e3dbef-daf5-487a-8d50-e2ebdb712cc0
title: 'IDirect3DVideoDevice9:: getdxvainternalinfo-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAInternalInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: aa512130b622d192acc37d8c309f462f8ecc87e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354555"
---
# <a name="idirect3dvideodevice9getdxvainternalinfo-method"></a>IDirect3DVideoDevice9:: getdxvainternalinfo-Methode

Fragt den von der Hardware Abstraktionsschicht (HAL) für die private Verwendung zugewiesenen Speicherplatz ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVAInternalInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pMemoryUsed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguid* 
</dt> <dd>

Zeiger auf eine GUID, die das DXVA-Profil angibt. Um eine Liste der unterstützten Profile abzurufen, nennen Sie [**IDirect3DVideoDevice9:: getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*puncompdata* 
</dt> <dd>

Ein Zeiger auf eine [**dxvauncompdatainfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvauncompdatainfo) -Struktur, die die Größe und das Pixel Format der nicht komprimierten Daten angibt.

</dd> <dt>

*pmemoryused* 
</dt> <dd>

Empfängt die Größe des von der HAL zugewiesenen temporären Speichers in Byte.

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

 

 




