---
description: Die SplitAt-Methode teilt das Objekt zum angegebenen Zeitpunkt auf.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: IAMTimelineSplittable::SplitAt-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSplittable.SplitAt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cdcedc25cf7f0998c6eac11de63f6e0d329e2ca8500576e0ad9e69cfc0bb3067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052410"
---
# <a name="iamtimelinesplittablesplitat-method"></a>IAMTimelineSplittable::SplitAt-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SplitAt` -Methode teilt das -Objekt zum angegebenen Zeitpunkt auf.

## <a name="syntax"></a>Syntax


```C++
HRESULT SplitAt(
   REFERENCE_TIME Time
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Time* 
</dt> <dd>

Zeit, zu der das Objekt relativ zum Anfang der Zeitachse in Einheiten von 100 Nanosekunden aufgeteilt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>       | Nichts aufzuteilen.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Das -Objekt ist zu diesem Zeitpunkt nicht vorhanden.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Hinweise

Wenn Sie eine Quelle, einen Effekt oder einen Übergang teilen, erstellt diese Methode ein zweites Objekt desselben Typs. Das ursprüngliche Objekt wird zur angegebenen Aufteilungszeit abgeschnitten, und das neue -Objekt ersetzt den abgeschnittenen Teil. Das neue -Objekt erbt alle eigenschaften. In einem Quellobjekt teilt die Methode auch alle Auswirkungen auf, die auf die Teilungszeit fallen.

Durch Aufrufen dieser Methode auf einer Spur werden alle Quellen, Effekte und Übergänge aufgeteilt, die zur angegebenen Teilungszeit in der Spur enthalten sind. Es wird keine zweite Spur erstellt. (Eine Spur beginnt zur Zeit 0 (null) und erstreckt sich bis unendlich.)

Bei einer Spur gibt die Methode S FALSE zurück, wenn die Teilungszeit später als alles in der Spur \_ ist. Für jedes andere Objekt gibt die Methode E INVALIDARG zurück, wenn die Teilungszeit nicht innerhalb des -Objekts \_ liegt.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IAMTimelineSplittable-Schnittstelle**](iamtimelinesplittable.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




