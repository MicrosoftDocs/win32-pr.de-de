---
description: Die put \_ Invert-Methode gibt an, ob der Schlüsselvorgang invertiert ist. Diese Eigenschaft gilt für alle Schlüsseltypen außer DXTKEY \_ ALPHA.
ms.assetid: 06acdd9f-eb3a-49bd-961d-00966df2ccb4
title: IDxtKey::p ut_Invert-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Invert
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ed1ed445e7a6f5f1f07eff74ac739934f2c9ca1358affe3e0cd699b7a101f0a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819437"
---
# <a name="idxtkeyput_invert-method"></a>IDxtKey::p ut \_ Invert-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_Invert` -Methode gibt an, ob der Schlüsselvorgang invertiert ist. Diese Eigenschaft gilt für alle Schlüsseltypen außer DXTKEY \_ ALPHA.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Invert(
  [in] BOOL newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Gibt einen booleschen Wert an. True **gibt** an, dass Pixel im überzählenden Bild in Bezug auf den Standardvorgang invertiert werden. False **gibt** an, dass Pixel im überzähligen Bild standardmäßig transparent gemacht werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




