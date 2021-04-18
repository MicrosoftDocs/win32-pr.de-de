---
description: Mit der setcutpoint-Methode wird die Uhrzeit festgelegt, zu der der Übergang von einer Quelle zum nächsten erfolgt, wenn der Übergang als Ausschneiden gerendert wird.
ms.assetid: 2660f4a8-e249-45d7-8866-02a9f2ef52b8
title: 'Iamtimelinetrans:: setcutpoint-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c1dad934d373a52b7e6c076c8c20dc8e1c6809ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357649"
---
# <a name="iamtimelinetranssetcutpoint-method"></a>Iamtimelinetrans:: setcutpoint-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetCutPoint` Methode legt die Zeit fest, zu der der Übergang von einer Quelle zum nächsten abbricht, wenn der Übergang als Ausschneiden gerendert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutPoint(
   REFERENCE_TIME TLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Tltime* 
</dt> <dd>

Der Ausschneide Punkt relativ zum Anfang des Übergangs in 100-Nanosecond-Einheiten. Wenn der Wert außerhalb der Grenzen des Übergangs liegt, wird er auf die nächste gültige Zeit abgeschnitten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Standardmäßig ist der Ausschneide Punkt die Mitte des Übergangs. Bei einem Übergang, der eine Sekunde umfasst, beträgt der Standard Ausschneide Punkt z. b. 0,5 Sekunden in den Übergang.

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

[**Iamtimelinetrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




