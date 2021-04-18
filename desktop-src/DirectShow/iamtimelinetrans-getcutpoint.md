---
description: Die getcutpoint-Methode ruft den Ausschneide Punkt ab.
ms.assetid: f54ef17e-3407-4164-911d-3dc7fad656ed
title: 'Iamtimelinetrans:: getcutpoint-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetCutPoint
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: e89cc2e7bc6d18842212a58bc5c00b6424947b66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361052"
---
# <a name="iamtimelinetransgetcutpoint-method"></a>Iamtimelinetrans:: getcutpoint-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetCutPoint` Methode ruft den Ausschneide Punkt ab. Wenn Sie einen Übergang als Ausschneiden gerenden, ist der Ausschneide Punkt die Zeit, zu der der Übergang von einer Quelle zur nächsten übergeht. Standardmäßig ist dieser Wert die Mitte des Übergangs. Bei einem Übergang, der eine Sekunde umfasst, beträgt der Standard Ausschneide Punkt z. b. 0,5 Sekunden in den Übergang.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCutPoint(
   REFERENCE_TIME *pTLTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ptltime* 
</dt> <dd>

Empfängt den Ausschneide Punkt in Bezug auf die Startzeit des Übergangs in 100-Nanosecond-Einheiten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                               | Beschreibung                                                                    |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>   | Der Ausschneide Punkt wurde nicht festgelegt. Der zurückgegebene Wert ist der Standardwert.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>      | Der Ausschneide Punkt wurde auf einen anderen Wert als den Standardwert festgelegt.<br/>            |
| <dl> <dt>**E- \_ Zeiger**</dt> </dl> | **Null** -Zeigerargument.<br/>                                          |



 

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

[**Iamtimelinetrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[**Iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md)
</dt> <dt>

[**Iamtimelinetrans:: getcutsonly**](iamtimelinetrans-getcutsonly.md)
</dt> <dt>

[**Iamtimeline:: transitionsenabled**](iamtimeline-transitionsenabled.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




