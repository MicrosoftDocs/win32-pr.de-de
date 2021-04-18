---
description: Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.
ms.assetid: 5a9fb077-fd79-4faa-a0f8-b3ac987adf36
title: 'IDirect3DVideoDevice9:: getdxvacompressedbufferinfo-Methode (DXVA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVACompressedBufferInfo
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 2bd2dcdd931ac8778e4f1c11f1479fe54e23d1b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357415"
---
# <a name="idirect3dvideodevice9getdxvacompressedbufferinfo-method"></a>IDirect3DVideoDevice9:: getdxvacompressedbufferinfo-Methode

Ruft Informationen zu den für die Hardware beschleunigten Decodierung benötigten komprimierten Puffern ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVACompressedBufferInfo(
   GUID               *pGuid,
   DXVAUncompDataInfo *pUncompData,
   DWORD              *pNumBuffers,
   DXVACompBufferInfo *pBufferInfo
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

*pnumbuffers* 
</dt> <dd>

Gibt bei Eingabe die Anzahl der Elemente im *pbufferinfo* -Array an. Wenn *pbufferinfo* **null** ist, muss der Wert von `*pNumBuffers` 0 (null) lauten.

Wenn *pbufferinfo* bei der Ausgabe **null** ist, wird die Größe des zuzuordnenden Arrays von *pnumbuffers* empfangen. Andernfalls empfängt *pnumbuffers* die tatsächliche Anzahl der Elemente, die in das *pbufferinfo* -Array kopiert werden.

</dd> <dt>

*pbufferinfo* 
</dt> <dd>

Adresse eines Arrays mit [**dxvacompbufferinfo**](/windows/desktop/api/dxva9typ/ns-dxva9typ-dxvacompbufferinfo) -Strukturen oder **null**. Wenn der Wert ungleich **null** ist, kopiert die Methode eine Liste mit **dxvacompbufferinfo** -Strukturen in dieses Array. Jede Struktur entspricht einem komprimierten Datenpuffer, der von der Video Zugriffstaste verwendet wird.

Legen Sie vor dem Aufrufen dieser Methode alle Array Elemente auf 0 (null) fest.

Jeder Array Index entspricht einem der DXVA-Oberflächentypen, die in "DXVA. h" definiert sind. Die Video Zugriffstaste gibt eine Liste von bis zu **DXVA \_ NUM-Typen von Comp- \_ \_ \_ Puffer** Array Einträgen zurück. Weitere Informationen finden Sie in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration), Abschnitt 3,4, "Buffer Description List". Wenn ein bestimmter Puffertyp nicht vom DXVA-Profil verwendet wird, enthält der Eintrag an diesem Index Nullen für alle Werte.

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

 

 
