---
description: Die \_ methode put ReplicateY gibt an, wie oft das Zurücksetzungsmuster vertikal repliziert wird.
ms.assetid: f27e0d54-1d0f-42fe-9638-39f68b97f9c7
title: IDxtJpeg::p ut_ReplicateY-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDxtJpeg.put_ReplicateY
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 03c7f35ca5b12817045b537d45cc1abe71f3e8d5136b1db4ee7b46884ad5a568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316280"
---
# <a name="idxtjpegput_replicatey-method"></a>IDxtJpeg::p ut \_ ReplicateY-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `put_ReplicateY` -Methode gibt an, wie oft das Zurücksetzungsmuster vertikal repliziert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ReplicateY(
  [in] long newVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*newVal* \[ In\]
</dt> <dd>

Gibt an, wie oft das Zurücksetzungsmuster vertikal repliziert wird.

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

[**IDxtJpeg-Schnittstelle**](idxtjpeg.md)
</dt> </dl>

 

 




