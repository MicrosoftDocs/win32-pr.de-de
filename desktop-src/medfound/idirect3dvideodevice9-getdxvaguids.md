---
description: Ruft eine Liste der DXVA-Profile (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: IDirect3DVideoDevice9::GetDXVAGuids-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetDXVAGuids
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 6a355c27177a546a2e91e769f72d9f4b9e216b005f711d42b5b7af39b4b78361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119269240"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9::GetDXVAGuids-Methode

Ruft eine Liste der DXVA-Profile (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pNumGuids* 
</dt> <dd>

Gibt bei der Eingabe die Anzahl der Elemente im *pGuids-Array* an. Wenn *pGuids* NULL **ist,** muss der Wert `*pNumGuids` von 0 (null) sein.

Wenn *pGuids* bei der Ausgabe **NULL ist,** empfängt *pNumGuids* die Anzahl der DXVA-Profile im eingeschränkten Modus. *Andernfalls empfängt pNumGuids* die tatsächliche Anzahl von GUIDs, die in das *pGuids-Array kopiert* werden.

</dd> <dt>

*pGuids* 
</dt> <dd>

Adresse eines Arrays von GUIDs oder **NULL.** Wenn der Wert nicht NULL ist,**empfängt** das Array eine Liste von GUIDs, die DXVA-Profile im eingeschränkten Modus angeben. Diese GUIDs sind in dxva.h definiert und in der [DXVA 1.0-Spezifikation dokumentiert.](/windows-hardware/drivers/display/directx-video-acceleration)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode zweimal auf. Legen Sie beim ersten Aufruf *pGuids auf* **NULL fest.** Der *pNumGuids-Parameter* empfängt die Anzahl der DXVA-Profil-GUIDs. Ordnen Sie ein Array von GUIDs mit der erforderlichen Größe zu, und rufen Sie die -Methode erneut auf. Legen Sie dieses Mal *pGuids auf* die Adresse des Arrays fest. Die -Methode füllt das Array mit der Liste der DXVA-Profil-GUIDs auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                              |
| Header<br/>                   | <dl> <dt>Dxva.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDirect3DVideoDevice9**](idirect3dvideodevice9.md)
</dt> </dl>

 

 
