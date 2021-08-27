---
description: Die SetSwapInputs-Methode gibt an, ob die Übergangseingaben ausgetauscht werden.
ms.assetid: c7303302-dbc4-41b6-8049-5c4496ee9264
title: IAMTimelineTrans::SetSwapInputs-Methode (Qedit.h)
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
ms.openlocfilehash: 3da350c6fe34f671d7af53ca67c404b4e327690918434b5e2fb1426e4a0953ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052080"
---
# <a name="iamtimelinetranssetswapinputs-method"></a>IAMTimelineTrans::SetSwapInputs-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetSwapInputs` -Methode gibt an, ob die Übergangseingaben ausgetauscht werden.

Standardmäßig erfolgt ein Übergang von der zusammengesetzten aller Schichten mit niedrigerer Priorität zu der Ebene, in der sich der Übergang befindet. Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich befindet, zurück zur zusammengesetzten Ebene mit niedrigerer Priorität wechselt. Weitere Informationen finden Sie unter [Übergangsrichtung.](transition-direction.md)

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

Gibt an, ob die Eingaben ausgetauscht werden. **False** gibt an, dass der Übergang von der zusammengesetzten Ebene aller Schichten mit niedrigerer Priorität zur Übergangsschicht wechselt. True gibt an, dass der Übergang in die entgegengesetzte Richtung verläuft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Diese Methode ändert nicht die Richtung des visuellen Effekts. Beispielsweise wird das Zurücksetzen von links nach rechts weiterhin von links nach rechts erfolgen. Um die Richtung zu ändern, legen Sie die **Progress-Eigenschaft** mithilfe der [**IPropertySetter-Schnittstelle**](ipropertysetter.md) fest.

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

[**IAMTimelineTrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




