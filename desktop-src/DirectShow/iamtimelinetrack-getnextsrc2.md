---
description: 'Mit der GetNextSrc2-Methode wird der Titel nach der nächsten Quelle durchsucht, die zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht iamtimelinetrack:: getnexzrc, aber nimmt einen reftime-Wert an.'
ms.assetid: f3f7b000-ec73-4ae9-802b-a9bc6f1840b3
title: 'Iamtimelinetrack:: GetNextSrc2-Methode (qedit. h)'
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
ms.openlocfilehash: c934cfd6c4f58c5fca59e78e120fee89af3f73a3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352878"
---
# <a name="iamtimelinetrackgetnextsrc2-method"></a>Iamtimelinetrack:: GetNextSrc2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextSrc2` Methode durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht [**iamtimelinetrack:: getnexzrc**](iamtimelinetrack-getnextsrc.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrc2(
  [out] IAMTimelineObj **ppSrc,
        REFTIME        *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsrc* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Enthält bei Eingabe die Startzeit für die Suche in Sekunden. Wenn die Methode eine Quelle abruft, wird der Wert auf die Endzeit der Quelle festgelegt. Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iamtimelinetrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




