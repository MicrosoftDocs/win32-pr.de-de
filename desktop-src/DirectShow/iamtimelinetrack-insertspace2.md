---
description: 'Die InsertSpace2-Methode teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein. Diese Methode entspricht iamtimelinetrack:: Insertspace, erfordert jedoch reftime-Werte.'
ms.assetid: 818a1dad-0c8d-4728-82d6-cd52c6c830a2
title: 'Iamtimelinetrack:: InsertSpace2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.InsertSpace2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 401c20d766fe9751c35cb59c03bca739494b3f8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364840"
---
# <a name="iamtimelinetrackinsertspace2-method"></a>Iamtimelinetrack:: InsertSpace2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `InsertSpace2` -Methode teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein. Diese Methode entspricht [**iamtimelinetrack:: Insertspace**](iamtimelinetrack-insertspace.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT InsertSpace2(
   REFTIME rtStart,
   REFTIME rtEnd
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rtstart* 
</dt> <dd>

Der Zeitpunkt, zu dem die Aufteilung erstellt werden soll, und der Anfangspunkt des eingefügten Speicherplatzes (in Sekunden).

</dd> <dt>

*rtend* 
</dt> <dd>

Endpunkt des eingefügten Raums in Sekunden.

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

 

 




