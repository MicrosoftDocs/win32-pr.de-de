---
description: Die Methode "*-wapinputs" gibt an, ob die Übergangs Eingaben ausgetauscht werden.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: Iamtimelinetrans::-Methode für die wapinputs-Methode (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.SetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 4b2deecb393d6532015cf1490aacd1bd50501920
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371757"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>Iamtimelinetrans::-Methode für die wapinputs-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetSwapInputs` Methode gibt an, ob die Übergangs Eingaben ausgetauscht werden.

Standardmäßig wird ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zu der Ebene, auf der sich der Übergang befindet, durchläuft. Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich wieder auf die Zusammensetzung der Ebenen mit niedrigerer Priorität befindet, erfolgt. Weitere Informationen finden Sie unter [Übergangs Richtung](transition-direction.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSwapInputs(
   BOOL Val
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Val* 
</dt> <dd>

Gibt an, ob die Eingaben ausgetauscht werden. Wenn der Wert **false** ist, wird der Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Übergangs Ebene durchgegangen. **True** gibt an, dass der Übergang in die entgegengesetzte Richtung verläuft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Diese Methode ändert nicht die Richtung des visuellen Effekts. Beispielsweise wird von links nach rechts die zurück Löschung von links nach rechts fortgesetzt. Um die Richtung zu ändern, legen Sie **die Eigenschaft Status** mithilfe der [**ipropertysetter**](ipropertysetter.md) -Schnittstelle fest.

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

 

 




