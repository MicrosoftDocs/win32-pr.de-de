---
description: Die getnexttrans-Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.
ms.assetid: 40598d8d-ce74-4a6f-83d0-ea409b0a858c
title: 'Iamtimelinetransable:: getnexttrans-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: cc8f7c88dab2b8c0dfece6f2799b6648c0b9da2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353419"
---
# <a name="iamtimelinetransablegetnexttrans-method"></a>Iamtimelinetransable:: getnexttrans-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextTrans` Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextTrans(
  [out] IAMTimelineObj **ppTrans,
        REFERENCE_TIME *pInOut
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pptrans* \[ vorgenommen\]
</dt> <dd>

Empfängt einen Zeiger auf die [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle des Übergangs Objekts.

</dd> <dt>

*Pinout* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Zeit in 100-Nanosecond-Einheiten angibt. Bei der Eingabe gibt dieser Wert die Zeit an, nach der der Übergang gesucht werden soll. Bei der Ausgabe wird dieser Wert auf die Endzeit des Übergangs festgelegt, wenn ein Übergang abgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn die Methode einen Übergang abruft, oder s \_ false, wenn kein Übergang gefunden wird. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.

## <a name="remarks"></a>Bemerkungen

Die Startzeit des Übergangs kann kleiner sein als die Zeit, die Sie in *Pinout* angegeben haben, wenn der Übergang die angegebene Zeitspanne überschreitet.

Wenn die Methode S OK zurückgibt \_ , weist die zurückgegebene [**iamtimelineobj**](iamtimelineobj.md) -Schnittstelle einen ausstehenden Verweis Zähler auf. Stellen Sie sicher, dass Sie die-Schnittstelle freigeben, wenn Sie Sie nicht mehr benötigen.

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

 

 




