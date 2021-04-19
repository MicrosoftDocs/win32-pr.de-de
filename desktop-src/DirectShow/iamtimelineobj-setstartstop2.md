---
description: 'Mit der SetStartStop2-Methode werden die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts festgelegt. Diese Methode entspricht iamtimelineobj:: setstartstation, erfordert jedoch reftime-Werte.'
ms.assetid: 0fc79c82-d8e1-4b87-9e59-6d9e6ca614f3
title: 'Iamtimelineobj:: SetStartStop2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineObj.SetStartStop2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 190e47d2ccee00d202dc16e20704b545447d844f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356001"
---
# <a name="iamtimelineobjsetstartstop2-method"></a>Iamtimelineobj:: SetStartStop2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `SetStartStop2` -Methode legt die Start-und Endzeit Zeiten des Objekts relativ zum übergeordneten Element des Objekts fest. Diese Methode entspricht [**iamtimelineobj:: setstartstation**](iamtimelineobj-setstartstop.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStartStop2(
   REFTIME Start,
   REFTIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Starten* 
</dt> <dd>

Die neue Startzeit in Sekunden oder – 1, um die vorhandene Startzeit beizubehalten.

</dd> <dt>

*Beenden* 
</dt> <dd>

Neue Endzeit, in Sekunden oder – 1, um die vorhandene Endzeit beizubehalten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                  | Beschreibung                  |
|----------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Erfolg.<br/>          |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>    | Nicht implementiert.<br/>  |



 

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

[**Iamtimelineobj-Schnittstelle**](iamtimelineobj.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




