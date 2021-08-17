---
description: Die put \_ Hue-Methode gibt den Farbtonwert an, für den die Taste festgelegt werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ HUE ist.
ms.assetid: 90c8c610-7ceb-479b-bb0e-d8753d0d7dac
title: IDxtKey::p ut_Hue-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtKey.put_Hue
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 063b8be8986a7a8a3fe3c7d14db31c0cb737d537b74366bee0ce3ed3550e3b24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819447"
---
# <a name="idxtkeyput_hue-method"></a>IDxtKey::p ut \_ Hue-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_Hue` -Methode gibt den Farbtonwert an, für den die Taste festgelegt werden soll. Diese Eigenschaft gilt nur, wenn der Schlüsseltyp DXTKEY \_ HUE ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_Hue(
  [in] int newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Der Farbtonwert, für den die Taste geschaltet werden soll. Der gültige Bereich liegt zwischen 0 und 360.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




