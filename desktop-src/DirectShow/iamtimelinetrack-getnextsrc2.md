---
description: Die GetNextSrc2-Methode durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht IAMTimelineTrack::GetNextSrc, nimmt jedoch einen REFTIME-Wert an.
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: IAMTimelineTrack::GetNextSrc2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ca9b18ba6ddd56771ac738f0ff831e4ea284d995fb28582a578386321e7ef856
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154821"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>IAMTimelineTrack::GetNextSrc2-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetNextSrc2` -Methode durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht [**IAMTimelineTrack::GetNextSrc,**](iamtimelinetrack-getnextsrc.md)nimmt jedoch einen [**REFTIME-Wert**](reftime.md) an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppSrc* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Quellobjekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Enthält bei der Eingabe die Startzeit für die Suche in Sekunden. Wenn die -Methode eine Quelle abruft, legt sie den Wert auf die Stoppzeit der Quelle fest. Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück, wenn die Methode eine Quelle abruft, andernfalls S \_ FALSE.

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

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




