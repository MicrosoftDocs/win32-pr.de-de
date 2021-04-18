---
description: 'Die GetNextTrans2-Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht iamtimelinetransable:: getnexttrans, aber nimmt einen reftime-Wert an.'
ms.assetid: e6910e94-f289-4a5d-9976-1e8f7373c882
title: 'Iamtimelinetransable:: GetNextTrans2-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTransable.GetNextTrans2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 2c5f79ff20507247fbcac3badceaf2c3e28f0303
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364526"
---
# <a name="iamtimelinetransablegetnexttrans2-method"></a>Iamtimelinetransable:: GetNextTrans2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetNextTrans2` Methode ruft den ersten Übergang ab, der zum angegebenen Zeitpunkt oder später angezeigt wird. Diese Methode entspricht [**iamtimelinetransable:: getnexttrans**](iamtimelinetransable-getnexttrans.md), aber nimmt einen [**reftime**](reftime.md) -Wert an.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetNextTrans2(
  [out] IAMTimelineObj **ppTrans,
        REFTIME        *pInOut
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

Ein Zeiger auf eine Variable, die die Zeit in Sekunden angibt. Bei der Eingabe gibt dieser Wert die Zeit an, nach der der Übergang gesucht werden soll. Bei der Ausgabe wird dieser Wert auf die Endzeit des Übergangs festgelegt, wenn ein Übergang abgerufen wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt s \_ OK zurück, wenn die Methode einen Übergang abruft, oder s \_ false, wenn kein Übergang gefunden wird. Andernfalls wird ein **HRESULT** -Wert zurückgegeben, der die Ursache des Fehlers angibt.

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

 

 




