---
description: Die SetStreamNumber-Methode gibt an, welcher Stream aus der Quelldatei gelesen werden soll, die diesem Quellobjekt zugeordnet ist.
ms.assetid: d40d0889-3b28-4114-9dd2-529e380eaeb8
title: IAMTimelineSrc::SetStreamNumber-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.SetStreamNumber
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae313121831dc2855a2f07ba3c7727e87736b77a8c5f98078d2237bb9520cf6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982960"
---
# <a name="iamtimelinesrcsetstreamnumber-method"></a>IAMTimelineSrc::SetStreamNumber-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetStreamNumber` -Methode gibt an, welcher Stream aus der Quelldatei gelesen werden soll, die diesem Quellobjekt zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetStreamNumber(
   long Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Die Streamnummer aus der Gruppe von Streams, die mit dem Medientyp der übergeordneten Gruppe übereinstimmen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der *Val-Parameter* gibt eine Streamnummer aus dem Satz von Streams an, der dem Medientyp der übergeordneten Gruppe entspricht, nicht aus dem gesamten Satz von Streams in der Quelldatei. Angenommen, eine Datei enthält zwei Videostreams und zwei Audiostreams. Wenn sich das Quellobjekt in einer Videogruppe befindet, wird durch Festlegen von *Val* auf 0 der erste Videostream ausgewählt. Der Aufrufer ist für die Angabe einer gültigen Streamnummer verantwortlich.

Die Streamnummer ist standardmäßig auf 0 (null) festgelegt.

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

[**IAMTimelineSrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




