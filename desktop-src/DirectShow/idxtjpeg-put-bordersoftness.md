---
description: Die \_ Put BorderSoftness-Methode gibt die Breite des unscharfen Bereichs um die Ränder des Zurücksetzungsmusters an.
ms.assetid: 9fdbda7f-c89b-4ed8-8035-054bc28f3231
title: IDxtJpeg::p ut_BorderSoftness-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_BorderSoftness
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3a505f370880241606829f94d1efd0dda6e49e3c1613cf8e790c797ae8d33594
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965033"
---
# <a name="idxtjpegput_bordersoftness-method"></a>IDxtJpeg::p ut \_ BorderSoftness-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_BorderSoftness` -Methode gibt die Breite des unscharfen Bereichs um die Ränder des Löschmusters an.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_BorderSoftness(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Die Breite des unscharfen Bereichs in Pixel.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IDxtJpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 




