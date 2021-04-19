---
description: Die setcutsonly-Methode gibt an, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf. Wenn eine Umstellung lange dauert, können Sie Sie als eine Ausschneide-und Geschwindigkeits Vorschau anzeigen.
ms.assetid: 9ccff624-e37b-422e-9cb2-c472e6c8b2bb
title: 'Iamtimelinetrans:: setcutsonly-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetCutsOnly
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 6b2944d652bffac5bf3bfa72a1e2372f734645bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367857"
---
# <a name="iamtimelinetranssetcutsonly-method"></a>Iamtimelinetrans:: setcutsonly-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetCutsOnly` Methode gibt an, ob der Übergang als Ausschneiden gerendert wird. Wenn dies der Fall ist, tritt der Übergang sofort am Ausschneide Punkt auf. Wenn eine Umstellung lange dauert, können Sie Sie als eine Ausschneide-und Geschwindigkeits Vorschau anzeigen.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetCutsOnly(
   BOOL Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Gibt an, ob der Übergang als Ausschneide gereinigen werden soll. **True** gibt an, dass der Übergang als sofortige Ausschneide gerendert wird. **False** gibt an, dass der Übergang über seine normale Dauer gerendert wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Das Rendern eines Übergangs als Ausschneiden ist nicht kompatibel mit dem Austauschen der Eingaben. (Weitere Informationen finden Sie unter [**iamtimelinetrans:: sswapinputs**](iamtimelinetrans-setswapinputs.md).) Wenn Sie `SetCutsOnly` mit dem Wert **true** aufzurufen, wird die Einstellung "Setting- **wapinputs** " vorübergehend überschrieben. Die Einstellung nur für die Kürzung ist für die Vorschau vorgesehen. Daher hat diese Einschränkung keinen Einfluss auf die Dateiausgabe – vergessen Sie nicht, `SetCutsOnly` mit dem Wert **false** aufzurufen, bevor Sie die Datei schreiben.

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

 

 




