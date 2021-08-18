---
description: Die GetSrcAtTime-Methode ruft das Quellobjekt ab, das der angegebenen Zeit gemäß den angegebenen Begrenzungsbedingungen am nächsten ist.
ms.assetid: 0469c0c2-13df-49f7-95b2-15d3069c5b1c
title: IAMTimelineTrack::GetSrcAtTime-Methode (Qedit.h)
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
ms.openlocfilehash: fde7d4d1e1a92c4f403c4d6ae38517bd715cf6d474f22f8a2e262d69fc57139a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052330"
---
# <a name="iamtimelinetrackgetsrcattime-method"></a>IAMTimelineTrack::GetSrcAtTime-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetSrcAtTime` -Methode ruft das Quellobjekt ab, das der angegebenen Zeit gemäß den angegebenen Begrenzungsbedingungen am nächsten ist.

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

*ppSrc* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimelineObj-Schnittstelle**](iamtimelineobj.md) des Quellobjekts.

</dd> <dt>

*Time* 
</dt> <dd>

Startzeit für die Suche in Einheiten von 100 Nanosekunden.

</dd> <dt>

*SearchDirection* 
</dt> <dd>

Member des [**DEXTERF \_ TRACK SEARCH \_ \_ FLAGS-Enumerationstyps,**](dexterf-track-search-flags.md) der die Begrenzungsbedingungen für die Suche angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                  | Beschreibung                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | Ein Quellobjekt wurde nicht gefunden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>         | Ein Quellobjekt wurde gefunden.<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | Ungültiges Argument.<br/>               |
| <dl> <dt>**E \_ POINTER**</dt> </dl>    | **NULL-Zeigerargument.**<br/>      |



 

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

[**IAMTimelineTrack-Schnittstelle**](iamtimelinetrack.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




