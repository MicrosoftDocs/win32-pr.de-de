---
description: Die SetStartStop-Methode legt die Start- und Stoppzeiten des Objekts relativ zum übergeordneten Element des Objekts fest.
ms.assetid: 6275a36b-f963-4916-bf60-ea68008ad153
title: IAMTimelineObj::SetStartStop-Methode (Qedit.h)
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
ms.openlocfilehash: e2806d926c9842f5900f46f923f4cbdf8caa47f112e1832077ab7d2b80a9341c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052450"
---
# <a name="iamtimelineobjsetstartstop-method"></a>IAMTimelineObj::SetStartStop-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetStartStop` -Methode legt die Start- und Stoppzeiten des Objekts relativ zum übergeordneten Element des Objekts fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStartStop(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Neue Startzeit in Einheiten von 100 Nanosekunden oder –1, um die vorhandene Startzeit zu behalten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Neue Stoppzeit in Einheiten von 100 Nanosekunden oder –1, um die vorhandene Stoppzeit zu behalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                  | Beschreibung                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>          |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument.<br/> |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl>    | Nicht implementiert.<br/>  |



 

## <a name="remarks"></a>Hinweise

Spuren, Kompositionen und Gruppen implementieren diese Methode nicht. Für diese Objekte ist die Startzeit immer 0 (null), und die Stoppzeit ist die maximale Stoppzeit der objekte, die sie enthalten.

Legen Sie keine überlappenden Zeiten für Quellobjekte innerhalb derselben Spur fest. Dies kann zu nicht definierten Verhaltensweisen führen.

Bei Quellobjekten sind die Start- und Stoppzeiten unabhängig von den Start- und Stoppzeiten der Medien. Das Ändern eines Wertepaars ändert das andere nicht. Rufen Sie zum Festlegen der Start- und Stoppzeiten der Medien die [**IAMTimelineSrc::SetMediaTimes-Methode**](iamtimelinesrc-setmediatimes.md) auf. Weitere Informationen finden Sie unter [Time in DirectShow Editing Services](time-in-directshow-editing-services.md).

Um framegenaue Schnitte und Übergänge zu erhalten, legen Sie die *Parameter Start* und *Stop* auf Rahmengrenzen fest. Sie können die [**IAMTimelineObj::FixTimes-Methode**](iamtimelineobj-fixtimes.md) verwenden, um einen Zeitwert in die nächste Framegrenze zu konvertieren, oder sie können die folgende Funktion verwenden, um die Framenummer in die Verweiszeit zu konvertieren:


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

[**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




