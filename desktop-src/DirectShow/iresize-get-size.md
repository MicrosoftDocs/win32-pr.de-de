---
description: Die Get \_ Size-Methode gibt die aktuelle Ausgabegröße und den stretch-Modus zurück.
ms.assetid: 61c0e439-26ce-45fc-986a-0ffc17056a55
title: IResize::get_Size-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 747ca8d7fd839321a9dbf4403c503652b932403e49bb964ae6148da2f49c5ac5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818211"
---
# <a name="iresizeget_size-method"></a>IResize::get \_ Size-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_Size` -Methode gibt die aktuelle Ausgabegröße und den stretch-Modus zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_Size(
  [out] int  *piHeight,
  [out] int  *piWidth,
  [out] long *pFlag
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piHeight* \[ out\]
</dt> <dd>

Empfängt die Videohöhe in Pixel.

</dd> <dt>

*piWidth* \[ out\]
</dt> <dd>

Empfängt die Videobreite in Pixel.

</dd> <dt>

*pFlag* \[ out\]
</dt> <dd>

Empfängt ein Flag, das den Streckungsmodus an gibt. Mögliche [**Werte finden Sie unter Größenflags**](resize-flags.md) ändern.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der Ausgabetyp nicht festgelegt wurde, sollte der Filter Standardwerte zurückgeben. Diese Werte können zur Entwurfszeit willkürlich ausgewählt werden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | DirectX 9.0 oder höher<br/>                                                         |
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> <dt>

[**IResize-Schnittstelle**](iresize.md)
</dt> </dl>

 

 




