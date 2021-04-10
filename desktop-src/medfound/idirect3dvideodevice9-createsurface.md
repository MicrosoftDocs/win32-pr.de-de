---
description: Erstellt eine komprimierte Oberfläche für die DirectX-Video Beschleunigung (DXVA)-Decodierung.
ms.assetid: 2bb8c99d-1151-4f6d-869f-2c1a592e76af
title: 'IDirect3DVideoDevice9:: kreatesurface-Methode (DXVA. h)'
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
ms.openlocfilehash: d9e87c9767619241fd6228bb6b0a531249dd2d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131328"
---
# <a name="idirect3dvideodevice9createsurface-method"></a>IDirect3DVideoDevice9:: kreatesurface-Methode

Erstellt eine komprimierte Oberfläche für die DirectX-Video Beschleunigung (DXVA)-Decodierung.

Um die Oberflächen Anforderungen zu ermitteln, müssen Sie [**IDirect3DVideoDevice9:: getdxvacompressedbufferinfo**](idirect3dvideodevice9-getdxvacompressedbufferinfo.md) aufrufen und die zurückgegebenen [**dxvacompbufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) -Strukturen untersuchen.

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

Die Breite der Oberfläche in Pixel. Legen Sie diesen Parameter auf **dxvacompbufferinfo. widthtocreate** fest.

</dd> <dt>

*Height* 
</dt> <dd>

Die Höhe der Oberfläche in Pixel. Legen Sie diesen Parameter auf **dxvacompbufferinfo. heighttocreate** fest.

</dd> <dt>

*BackBuffer* 
</dt> <dd>

Die Anzahl der Back Puffer. Dieser Parameter kann NULL sein.

</dd> <dt>

*Format* 
</dt> <dd>

Das als **D3DFORMAT** -Wert angegebene Pixel Format. Legen Sie diesen Parameter auf **dxvacompbufferinfo. Format** fest.

</dd> <dt>

*Pool* 
</dt> <dd>

Der Speicherpool, in dem die-Oberfläche erstellt werden soll, angegeben als **D3DPOOL** -Wert. Legen Sie diesen Parameter auf **dxvacompbufferinfo. Pool** fest.

</dd> <dt>

*Verwendung* 
</dt> <dd>

Ein bitweises **or** von mindestens einer **D3DUSAGE** -Konstante. Legen Sie diesen Parameter auf **dxvacompbufferinfo. Usage fest.**

</dd> <dt>

*ppsurface* 
</dt> <dd>

Empfängt einen Zeiger auf die **IDirect3DSurface9** -Schnittstelle. Der Aufrufer muss die-Schnittstelle freigeben.

</dd> <dt>

*psharedhandle* 
</dt> <dd>

Reserviert. Auf **null** festgelegt.

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

 

 




