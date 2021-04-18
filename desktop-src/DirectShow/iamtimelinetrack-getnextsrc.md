---
description: Mit der getnexzrc-Methode wird der Titel nach der nächsten Quelle durchsucht, die zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: e87d8978-7b45-41a3-a74d-b5dd231d1d85
title: 'Iamtimelinetrack:: getnextrc-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack.GetNextSrc
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: dd8ca25b2d5a551d803e79e69cf8d1095ee47511
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364820"
---
# <a name="iamtimelinetrackgetnextsrc-method"></a>Iamtimelinetrack:: getnexzrc-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextSrc` Methode durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextSrc(
  [out] IAMTimelineObj **ppSrc,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppsrc* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Quell Objekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit für die Suche enthält, in 100-Nanosecond-Einheiten. Wenn die Methode eine Quelle abruft, wird der Wert auf die Endzeit der Quelle festgelegt. Wenn die Methode keine Quelle abruft, wird der Wert ungültig, und die Anwendung sollte ihn nicht verwenden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt "s OK" zurück \_ , wenn die Methode eine Quelle abruft, \_ andernfalls "false".

## <a name="remarks"></a>Bemerkungen

Wenn die durch *Pinout* angegebene Zeit zwischen den Start-und Endzeiten einer Quelle liegt, ruft die Methode diese Quelle ab.

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

 

 




