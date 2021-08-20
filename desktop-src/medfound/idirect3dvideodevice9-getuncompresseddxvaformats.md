---
description: Ruft eine Liste der nicht komprimierten Pixelformate ab, die mit einem angegebenen DXVA-Profil (DirectX Video Acceleration) gerendert werden können.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: IDirect3DVideoDevice9::GetUncompressedDXVAFormats-Methode (Dxva.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirect3DVideoDevice9.GetUncompressedDXVAFormats
api_type:
- COM
api_location:
- dxva.h
ms.openlocfilehash: 3d7f27060d0c9e43f1852c86697826986c0c095c14a19fbfafa53978e96cbe79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878797"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9::GetUncompressedDXVAFormats-Methode

Ruft eine Liste der nicht komprimierten Pixelformate ab, die mit einem angegebenen DXVA-Profil (DirectX Video Acceleration) gerendert werden können.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUncompressedDXVAFormats(
   GUID      *pGuid,
   DWORD     *pNumFormats,
   D3DFORMAT *pFormats
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pGuid* 
</dt> <dd>

Zeiger auf eine GUID, die das DXVA-Profil angibt. Rufen Sie [**IDirect3DVideoDevice9::GetDXVAGuids**](idirect3dvideodevice9-getdxvaguids.md)auf, um eine Liste der unterstützten Profile abzurufen.

</dd> <dt>

*pNumFormats* 
</dt> <dd>

Gibt bei eingabe die Anzahl der Elemente im *pFormats-Array an.* Wenn *pFormats* **NULL** ist, muss der Wert von `*pNumFormats` 0 (null) sein.

Wenn *pFormats* bei der Ausgabe **NULL** ist, empfängt *pNumFormats* die Anzahl der unterstützten Pixelformate. Andernfalls empfängt *pNumFormats* die tatsächliche Anzahl von Pixelformaten, die in das *pFormats-Array* kopiert wurden.

</dd> <dt>

*pFormats* 
</dt> <dd>

Adresse eines Arrays von **D3DFORMAT-Werten** oder **NULL.** Wenn der Wert ungleich **NULL** ist, empfängt das Array eine Liste von Pixelformaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode zweimal auf. Legen Sie beim ersten Aufruf *pFormats* auf **NULL** fest. Der *Parameter pNumFormats* empfängt die Anzahl der Formate. Ordnen Sie ein **D3DFORMAT-Array** mit der erforderlichen Größe zu, und rufen Sie die -Methode erneut auf. Legen Sie dieses Mal *pFormats* auf die Adresse des Arrays fest. Die -Methode füllt das Array mit der Liste der Pixelformate auf.

Der Treiber sollte die Formate in absteigender Reihenfolge zurückgeben, wobei zuerst das bevorzugte Format aufgeführt wird.

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

 

 




