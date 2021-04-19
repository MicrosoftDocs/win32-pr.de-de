---
description: 'Die GetTransAtTime2-Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab. Diese Methode entspricht iamtimelinetransable:: gettransattime, erfordert aber einen reftime-Parameter.'
ms.assetid: b51b53ec-4b56-4900-98b5-427d752354b0
title: 'Iamtimelinetransable:: GetTransAtTime2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b3de498791a634ea651da46ba9c95557ca12b87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372487"
---
# <a name="iamtimelinetransablegettransattime2-method"></a>Iamtimelinetransable:: GetTransAtTime2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetTransAtTime2` Methode ruft den Übergang, der dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab. Diese Methode entspricht [**iamtimelinetransable:: gettransattime**](iamtimelinetransable-gettransattime.md), erfordert aber einen [**reftime**](reftime.md) -Parameter.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTransAtTime2(
  [out] IAMTimelineObj **ppObj,
        REFTIME        Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppobj* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs.

</dd> <dt>

*Time* 
</dt> <dd>

Der Zeitpunkt, ab dem mit der Suche begonnen werden soll (in Sekunden).

</dd> <dt>

*Suchrichtung* 
</dt> <dd>

Member des [**dexterf- \_ \_ \_ Suchflags**](dexterf-track-search-flags.md) enumerierten Typs, der die begrenzungsbedingungen für die Suche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>      | Es wurde kein Übergang gefunden.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Übergang wurde gefunden.<br/>      |
| <dl> <dt>**E \_ invalidArg**</dt> </dl> | Ungültiges Argument.<br/>          |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl>    | **Null** -Zeigerargument.<br/> |



 

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

[**Iamtimelinetransable-Schnittstelle**](iamtimelinetransable.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




