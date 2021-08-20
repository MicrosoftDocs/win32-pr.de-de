---
description: Die put \_ Luminance-Methode gibt den Ludominanzwert an, für den eine Schlüsseltaste festgelegt werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ LUMINANCE ist.
ms.assetid: 3e255423-1724-49fe-b1a1-49bc1d5fa6ae
title: IDxtKey::p ut_Luminance-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Luminance
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae51fe72220355cb6e206ea437f547a0a8ca2d77633195debeb364f17e7f136f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819383"
---
# <a name="idxtkeyput_luminance-method"></a>IDxtKey::p ut \_ Luminance-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_Luminance` -Methode gibt den Luminanzwert an, für den eine Schlüsseltaste festgelegt werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ LUMINANCE ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Luminance(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Der Ludominanzwert, für den die Schlüsseltastenwerte schlüsselt werden. Der gültige Bereich liegt zwischen 0 und 100.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDxtKey-Schnittstelle**](idxtkey.md)
</dt> <dt>

[**IDxtKey::put \_ KeyType**](idxtkey-put-keytype.md)
</dt> </dl>

 

 




