---
description: Ruft eine Liste von nicht komprimierten Pixel Formaten ab, die mithilfe eines angegebenen DirectX-Video Beschleunigung-Profils (DXVA) gerendert werden können.
ms.assetid: 7c69ea5f-6054-4430-95b5-820db6854fc0
title: 'IDirect3DVideoDevice9:: getuncompresseddxvaformats-Methode (DXVA. h)'
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
ms.openlocfilehash: 94784ac5fe164d571a8a02e4170990f8ce06a4a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345078"
---
# <a name="idirect3dvideodevice9getuncompresseddxvaformats-method"></a>IDirect3DVideoDevice9:: getuncompresseddxvaformats-Methode

Ruft eine Liste von nicht komprimierten Pixel Formaten ab, die mithilfe eines angegebenen DirectX-Video Beschleunigung-Profils (DXVA) gerendert werden können.

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

*pguid* 
</dt> <dd>

Zeiger auf eine GUID, die das DXVA-Profil angibt. Um eine Liste der unterstützten Profile abzurufen, nennen Sie [**IDirect3DVideoDevice9:: getdxvage IDs**](idirect3dvideodevice9-getdxvaguids.md).

</dd> <dt>

*pnumformats* 
</dt> <dd>

Gibt bei Eingabe die Anzahl der Elemente im Array " *pformats* " an. Wenn *pformats* **null** ist, muss der Wert von `*pNumFormats` 0 (null) sein.

Bei der Ausgabe empfängt *pnumformats* , wenn *pformats* **null** ist, die Anzahl der unterstützten Pixel Formate. Andernfalls empfängt *pnumformats* die tatsächliche Anzahl der Pixel Formate, die in das Array " *pformats* " kopiert werden.

</dd> <dt>

*pformats* 
</dt> <dd>

Adresse eines Arrays von **D3DFORMAT** -Werten oder **null**. Wenn der Wert nicht **null** ist, empfängt das Array eine Liste von Pixel Formaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Ruft diese Methode zweimal auf. Legen Sie für den ersten-Befehl *pformats* auf **null** fest. Der *pnumformats* -Parameter empfängt die Anzahl von Formaten. Weisen Sie ein **D3DFORMAT** -Array mit der erforderlichen Größe zu, und verwenden Sie die-Methode erneut. Legen Sie dieses Mal *pformats* auf die Adresse des Arrays fest. Die-Methode füllt das Array mit der Liste der Pixel Formate aus.

Der Treiber sollte die Formate in absteigender Reihenfolge der bevorzugte Reihenfolge zurückgeben, wobei das am meisten bevorzugte Format zuerst aufgeführt wird.

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

 

 




