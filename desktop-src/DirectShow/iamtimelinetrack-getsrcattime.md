---
description: Die gezr| Time-Methode ruft das Quell Objekt ab, das dem angegebenen Zeitpunkt gemäß den angegebenen begrenzungsbedingungen am nächsten liegt.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: 'Iamtimelinetrack:: gezr| Time-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetSrcAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b726d26efd0550df364200a27d536d60d38274a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365960"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>Iamtimelinetrack:: gezr| Time-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetSrcAtTime` Methode ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSrcAtTime(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsrc* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.

</dd> <dt>

*Time* 
</dt> <dd>

Startzeit für die Suche in 100-Nanosecond-Einheiten.

</dd> <dt>

*Suchrichtung* 
</dt> <dd>

Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                  | Beschreibung                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Es wurde kein Quell Objekt gefunden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Ein Quell Objekt gefunden.<br/>        |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument.<br/>               |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene **iamtimelineobj** -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

 

 




