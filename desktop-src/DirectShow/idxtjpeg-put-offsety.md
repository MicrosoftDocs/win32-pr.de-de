---
description: Die put \_ OffsetY-Methode gibt den vertikalen Offset des Zurücksetzungsstarts an.
ms.assetid: 1dfd18cf-06ae-46eb-80d7-078efc243bb1
title: IDxtJpeg::p ut_OffsetY-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_OffsetY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: afc71085b3d1f4a03a6680a04ee52eba90c2a0aa230ba4894b2aee39eda6f502
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997590"
---
# <a name="idxtjpegput_offsety-method"></a>IDxtJpeg::p ut \_ OffsetY-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_OffsetY` -Methode gibt den vertikalen Offset des Zurücksetzungsstarts an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_OffsetY(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Der vertikale Offset des Zurücksetzungsstarts in Pixel. Die Mitte der Zurücksetzung wird um diesen Betrag versetzt.

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

[**IDxtJpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 




