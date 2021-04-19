---
description: Ruft eine Liste von DXVA-Profilen (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.
ms.assetid: 4adbbac2-a25d-4e17-b62e-a02a67dcdbed
title: 'IDirect3DVideoDevice9:: getdxvage IDs-Methode (DXVA. h)'
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
ms.openlocfilehash: 3ea05af8f27399af38419e177d7bd40b029cd63b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360211"
---
# <a name="idirect3dvideodevice9getdxvaguids-method"></a>IDirect3DVideoDevice9:: getdxvage IDs-Methode

Ruft eine Liste von DXVA-Profilen (DirectX Video Acceleration) ab, die vom Anzeigetreiber unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetDXVAGuids(
   DWORD *pNumGuids,
   GUID  *pGuids
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnumguids* 
</dt> <dd>

Gibt bei Eingabe die Anzahl der Elemente im *pguids* -Array an. Wenn *pguids* **null** ist, muss der Wert von `*pNumGuids` 0 (null) lauten.

Bei Ausgabe, wenn *pguids* **null** ist, empfängt *pnumguids* die Anzahl der DXVA-Profile im eingeschränkten Modus. Andernfalls empfängt *pnumguids* die tatsächliche Anzahl der GUIDs, die in das *pguids* -Array kopiert werden.

</dd> <dt>

*pguids* 
</dt> <dd>

Adresse eines Arrays von GUIDs oder **null**. Wenn der Wert nicht **null** ist, empfängt das Array eine Liste von GUIDs, die DXVA-Profile im eingeschränkten Modus angeben. Diese GUIDs werden in "DXVA. h" definiert und in der [DXVA 1,0-Spezifikation](/windows-hardware/drivers/display/directx-video-acceleration)dokumentiert.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode zweimal auf. Legen Sie für den ersten-Befehl *pguids* auf **null** fest. Der *pnumguids* -Parameter empfängt die Anzahl der DXVA-Profil-GUIDs. Weisen Sie ein Array von GUIDs der erforderlichen Größe zu, und nennen Sie die Methode erneut. Legen Sie dieses Mal *pguids* auf die Adresse des Arrays fest. Die-Methode füllt das Array mit der Liste der DXVA-Profil-GUIDs auf.

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

 

 
