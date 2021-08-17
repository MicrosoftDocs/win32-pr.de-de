---
description: Die methode put \_ RGB gibt die RGB-Farbe an, für die eine Taste festgelegt werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB ist.
ms.assetid: 7a0b794e-bea6-4061-98a0-3f70521e89a3
title: IDxtKey::p ut_RGB-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_RGB
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f53cb5d856377b611c5ea90d3b9c1f7fa522d892e6c79aa50d350883497398a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819393"
---
# <a name="idxtkeyput_rgb-method"></a>IDxtKey::p ut-RGB-Methode \_

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_RGB` -Methode gibt die RGB-Farbe an, für die ein Schlüssel verwendet werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ RGB ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_RGB(
  [in] DWORD newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Gibt die Farbe als Hexadezimalzahl im Format 0xRRGGBB an, wobei RR der rote Wert, GG der grüne Wert und BB der blaue Wert ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




