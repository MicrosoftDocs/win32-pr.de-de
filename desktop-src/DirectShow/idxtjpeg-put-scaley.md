---
description: Die Put \_ ScaleY-Methode gibt den Betrag an, um den die Zurücksetzung vertikal gestreckt wird.
ms.assetid: 1dd84540-b249-482c-9cb7-aab8c7dc4d25
title: IDxtJpeg::p ut_ScaleY-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ScaleY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e16b3e2e94a2878bd425b705544701362242f305471b063cdbaff70cbaba63cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119213310"
---
# <a name="idxtjpegput_scaley-method"></a>IDxtJpeg::p ut \_ ScaleY-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `put_ScaleY` -Methode gibt den Betrag an, um den die Zurücksetzung vertikal gestreckt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScaleY(
  [in] double newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Der Betrag, um den die Zurücksetzung vertikal gestreckt wird, als Prozentsatz der ursprünglichen Zurücksetzungsdefinition. Beispielsweise bedeutet der Wert 1,0 kein Strecken, und 2,0 bedeutet 200 % Stretching.

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

[**IDxtJpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 




