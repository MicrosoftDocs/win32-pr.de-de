---
description: Die GetTransAtTime-Methode ruft den Übergang ab, der der angegebenen Zeit entsprechend den angegebenen Begrenzungsbedingungen am nächsten ist.
ms.assetid: 33b3686b-5a9d-4eb2-bd40-4d6f569e7d89
title: IAMTimelineTransable::GetTransAtTime-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetTransAtTime
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: db81cf9a91f34699765e89f917ec31a902ebd188dc61dd77a1b909d10b09788c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118399207"
---
# <a name="iamtimelinetransablegettransattime-method"></a>IAMTimelineTransable::GetTransAtTime-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetTransAtTime` -Methode ruft den Übergang ab, der der angegebenen Zeit am nächsten ist, entsprechend den angegebenen Begrenzungsbedingungen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTransAtTime(
  [out] IAMTimelineObj **ppObj,
        REFERENCE_TIME Time,
        long           SearchDirection
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppObj* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Übergangs.

</dd> <dt>

*Time* 
</dt> <dd>

Die Zeit, ab der mit der Suche begonnen werden soll, in Einheiten von 100 Nanosekunden.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Member des [**DEXTERF \_ TRACK SEARCH \_ \_ FLAGS-Enumerationstyps,**](dexterf-track-search-flags.md) der die Begrenzungsbedingungen für die Suche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                  | Beschreibung                           |
|----------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | Es wurde kein Übergang gefunden.<br/>   |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Der Übergang wurde gefunden.<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument.<br/>          |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument.**<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn die Methode S \_ OK zurückgibt, verfügt die **zurückgegebene IAMTimelineObj-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die Schnittstelle freigeben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAMTimelineTransable-Schnittstelle**](iamtimelinetransable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




