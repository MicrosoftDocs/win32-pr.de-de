---
description: 'Mit der FixMediaTimes2-Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Diese Methode entspricht iamtimelinesrc:: fixmediatimes, erfordert jedoch reftime-Werte.'
ms.assetid: c51172ea-b5d7-4a2e-ace2-85e6e671c1e9
title: 'Iamtimelinesrc:: FixMediaTimes2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineSrc.FixMediaTimes2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 98e38b6c1ea4c49372a52a805920fa95ccf795f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373577"
---
# <a name="iamtimelinesrcfixmediatimes2-method"></a>Iamtimelinesrc:: FixMediaTimes2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Mit der- `FixMediaTimes2` Methode werden die angegebenen Uhrzeitwerte auf die nächste Frame Grenze gerundet, wie durch die Ausgabe Frame Rate definiert. Diese Methode entspricht [**iamtimelinesrc:: fixmediatimes**](iamtimelinesrc-fixmediatimes.md), erfordert jedoch [**reftime**](reftime.md) -Werte.

## <a name="syntax"></a>Syntax


```C++
HRESULT FixMediaTimes2(
   REFTIME *pStart,
   REFTIME *pStop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PStart* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> <dt>

*pstopps* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit in Sekunden enthält. Wenn der Aufruf erfolgreich ist, wird diese Variable auf die abgerundete Zeit festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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

[**Iamtimelinesrc-Schnittstelle**](iamtimelinesrc.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




