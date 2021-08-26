---
description: Die get InputSize-Methode gibt die aktuelle Eingabegröße \_ des Größenfilters zurück.
ms.assetid: 7066a044-52ea-4851-83f2-f1fb323c2251
title: IResize::get_InputSize-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.get_InputSize
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3b862237f8c51bdf6c22ca9acb667199fadee33b37e425efabfe25bdb8a20dd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078930"
---
# <a name="iresizeget_inputsize-method"></a>IResize::get \_ InputSize-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `get_InputSize` -Methode gibt die aktuelle Eingabegröße des Größenfilters zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_InputSize(
  [out] int *piHeight,
  [out] int *piWidth
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

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Wenn der Eingabepin des Filters nicht verbunden ist, geben Sie einen Fehlercode zurück. Andernfalls geben Sie die Breite und Höhe des Videos zurück, wie durch den Medientyp des Eingabepins angegeben.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



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

 

 




