---
description: Die FixMediaTimes2-Methode rundet die angegebenen Zeitwerte auf die nächste Framegrenze, wie durch die Ausgabebildrate definiert. Diese Methode entspricht IAMTimelineSrc::FixMediaTimes, nimmt jedoch REFTIME-Werte an.
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: IAMTimelineSrc::FixMediaTimes2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ceff01e17d82ed59e8d63811841e58e97323a9be4ec4c40b719bb655aac464e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399620"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>IAMTimelineSrc::FixMediaTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Methode rundet die angegebenen Zeitwerte auf die nächste Framegrenze, wie durch `FixMediaTimes2` die Ausgabebildrate definiert. Diese Methode entspricht [**IAMTimelineSrc::FixMediaTimes,**](iamtimelinesrc-fixmediatimes.md)nimmt jedoch [**REFTIME-Werte**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

</dd> <dt>

*Pstop* 
</dt> <dd>

Zeiger auf eine Variable, die die Stoppzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die gerundete Zeit festgelegt.

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




