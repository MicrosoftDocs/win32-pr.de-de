---
description: Die splitat-Methode teilt das Objekt zum angegebenen Zeitpunkt.
ms.assetid: 37870c6f-a35e-4c08-8188-1c4c7b25ff88
title: 'Iamtimelinesplicustom:: splitat-Methode (qedit. h)'
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
ms.openlocfilehash: a44aabf3386a4e906bd4f3e149c416642ba6c4fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371610"
---
# <a name="iamtimelinesplittablesplitat-method"></a>Iamtimelinesplicustom:: splitat-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SplitAt` Methode teilt das Objekt zum angegebenen Zeitpunkt.

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

Der Zeitpunkt, an dem das Objekt in Relation zum Anfang der Zeitachse aufgeteilt werden soll, in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>       | Nichts zu teilen.<br/>                       |
| <dl> <dt>**S \_ OK**</dt> </dl>          | Erfolg.<br/>                                |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>  | Das Objekt ist zu diesem Zeitpunkt nicht vorhanden.<br/> |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Quelle, einen Effekt oder einen Übergang aufteilen, erstellt diese Methode ein zweites Objekt desselben Typs. Das ursprüngliche-Objekt wird zur angegebenen Teilzeit abgeschnitten, und das neue-Objekt ersetzt den abgeschnittene Teil. Das neue-Objekt erbt alle gleichen Eigenschaften. In einem-Quell Objekt teilt die-Methode auch alle Effekte, die auf die geteilte Zeit fallen.

Wenn Sie diese Methode für einen Track aufrufen, werden alle Quellen, Effekte und Übergänge, die in der Spur enthalten sind, zur angegebenen Teilzeit aufgeteilt. Es wird keine zweite Spur erstellt. (Ein Track beginnt bei der Zeit NULL und erstreckt sich auf unendlich.)

Bei einer Nachverfolgung gibt die Methode den Wert "false" zurück, wenn die Teilzeit nach dem Zeitpunkt der Nachverfolgung liegt \_ . Wenn die Split-Zeit für ein beliebiges anderes Objekt nicht innerhalb des Objekts liegt, gibt die Methode E \_ invalidArg zurück.

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

[**Iamtimelinesplicustom-Schnittstelle**](iamtimelinesplittable.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




