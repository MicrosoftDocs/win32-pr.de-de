---
description: Mit der fixmediatimes-Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Im Allgemeinen müssen Anwendungen diese Methode nicht aufzurufen.
ms.assetid: 11537715-3be1-4a3c-8700-50b13835ffe9
title: 'Iamtimelinesrc:: fixmediatimes-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 1db0a126ebf6ff90d4db7512eb7346d6dbca8b5f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367520"
---
# <a name="iamtimelinesrcfixmediatimes-method"></a>Iamtimelinesrc:: fixmediatimes-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Mit der- `FixMediaTimes` Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Im Allgemeinen müssen Anwendungen diese Methode nicht aufzurufen.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixMediaTimes(
   REFERENCE_TIME *pStart,
   REFERENCE_TIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit in 100-Nanosecond-Einheiten enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in 100-Nanosecond-Einheiten enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ähnelt der [**iamtimelineobj:: fixtimes**](iamtimelineobj-fixtimes.md) -Methode, behält jedoch das ursprüngliche Verhältnis von Medien Zeiten und Zeitachsen Zeiten bei. Wenn Sie nur die Zeiten auf die nächste Frame Grenze umrunden, kann dieses Verhältnis verzerrt werden.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




