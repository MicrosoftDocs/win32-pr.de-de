---
description: Die SetMediaTimes2-Methode legt die Stopp- und Startzeiten der Medien fest. Diese Methode entspricht IAMTimelineSrc::SetMediaTimes, nimmt jedoch REFTIME-Werte an.
ms.assetid: 9eea7965-46c5-416c-97df-134d29130c8a
title: IAMTimelineSrc::SetMediaTimes2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 5d94515f2e810f74e788f5d8909ddee377bebee29525cc3d0c12b0463635043e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154902"
---
# <a name="iamtimelinesrcsetmediatimes2-method"></a>IAMTimelineSrc::SetMediaTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetMediaTimes2` -Methode legt die Stopp- und Startzeiten der Medien fest. Diese Methode entspricht [**IAMTimelineSrc::SetMediaTimes,**](iamtimelinesrc-setmediatimes.md)nimmt jedoch [**REFTIME-Werte**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetMediaTimes2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Startzeit des Mediums in Sekunden.

</dd> <dt>

*Beenden* 
</dt> <dd>

Medienstoppzeit in Sekunden.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




