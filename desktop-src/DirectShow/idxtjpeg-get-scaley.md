---
description: Die \_ Get ScaleY-Methode ruft den Betrag ab, um den das Zurücksetzen vertikal gestreckt wird.
ms.assetid: d8b80f19-2ec5-4d66-bd13-d6f7b5144345
title: IDxtJpeg::get_ScaleY-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.get_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 3da97c829c8234a5bd0e8c9b82bf9a7f3334bca78de395be2e5724d8a52f4838
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639400"
---
# <a name="idxtjpegget_scaley-method"></a>IDxtJpeg::get \_ ScaleY-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `get_ScaleY` -Methode ruft den Betrag ab, um den das Zurücksetzen vertikal gestreckt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT get_ScaleY(
  [out, retval] long *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* \[ out, retval\]
</dt> <dd>

Empfängt den Betrag, um den das Zurücksetzen vertikal gestreckt wird, als Prozentsatz der ursprünglichen Zurücksetzungsdefinition. Der Wert 1.0 bedeutet z.B. kein Stretching, und 2,0 bedeutet 200 % Stretching.

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

 

 




