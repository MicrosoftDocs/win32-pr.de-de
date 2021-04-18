---
description: Mit der setstartend-Methode werden die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts festgelegt.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: 'Iamtimelineobj:: setstartstation-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e7839417a0406fc2702fb0fbd593edc92fa80437
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365554"
---
# <a name="iamtimelineobjsetstartstop-method"></a>Iamtimelineobj:: setstartstation-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetStartStop` -Methode legt die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

Neue Startzeit in 100-Nanosecond-Einheiten oder – 1, um die vorhandene Startzeit beizubehalten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Neue Endzeit, in 100-Nanosecond-Einheiten oder – 1, um die vorhandene Endzeit beizubehalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                  | Beschreibung                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>    | Nicht implementiert.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wird von nachverfolgen, Kompositionen und Gruppen nicht implementiert. Für diese Objekte ist die Startzeit immer 0 (null), und die Endzeit ist die maximale Endzeit der Objekte, die Sie enthalten.

Legen Sie keine Überlappungs Zeiten für Quell Objekte innerhalb desselben Titels fest. Dies kann zu nicht definiertem Verhalten führen.

Bei Quell Objekten sind Start-und Endzeiten unabhängig von den Start-und Endzeiten des Mediums. Wenn Sie ein Wertepaar ändern, ändert sich das andere nicht. Um die Start-und Endzeit des Mediums festzulegen, müssen Sie die [**iamtimelinesrc:: setmediatimes**](iamtimelinesrc-setmediatimes.md) -Methode aufrufen. Weitere Informationen finden Sie unter [Zeit in DirectShow-Bearbeitungs Diensten](time-in-directshow-editing-services.md).

Um Frame-exakte Ausschnitte und Übergänge zu erhalten, legen Sie die Parameter *Start* und *Ende* auf Frame-Begrenzungen fest. Sie können die [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode verwenden, um einen Zeitwert in die nächste Frame Grenze zu konvertieren, oder Sie können die folgende Funktion verwenden, um von der Frame Nummer in die Verweis Zeit zu konvertieren:


```C++
REFERENCE_TIME inline FrameNumToTime(LONGLONG frame, double fps)
{
    double dt = (frame * 10000000 / fps);
    if (frame >= 0) 
    {
        dt += 0.5;    }
    else
    {
        dt -= 0.5;
    }
    return (REFERENCE_TIME)dt;
}
```



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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




