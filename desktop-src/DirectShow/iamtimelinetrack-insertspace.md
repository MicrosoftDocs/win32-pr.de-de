---
description: Die Insertspace-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt zwischen Ihnen Leerzeichen ein.
ms.assetid: f9e48f58-1867-405c-b208-1ab781912aa1
title: 'Iamtimelinetrack:: Insertspace-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 84d8076f6f89ee5e890db0047d47ade283b1e333
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368323"
---
# <a name="iamtimelinetrackinsertspace-method"></a>Iamtimelinetrack:: Insertspace-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `InsertSpace` -Methode teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein.

## <a name="syntax"></a>Syntax


```C++
HRESULT InsertSpace(
   REFERENCE_TIME rtStart,
   REFERENCE_TIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtstart* 
</dt> <dd>

Der Zeitpunkt, zu dem die Aufteilung erstellt werden soll, und der Anfangspunkt des eingefügten Leerraums in 100-Nanosecond-Einheiten.

</dd> <dt>

*rtend* 
</dt> <dd>

Endpunkt des eingefügten Raums in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Es sind keine Objekte zum angegebenen Zeitpunkt vorhanden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                    |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Ungültiges Argument.<br/>                           |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                        |



 

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

 

 




