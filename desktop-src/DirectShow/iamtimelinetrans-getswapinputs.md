---
description: Die GetSwapInputs-Methode ruft einen Wert ab, der angibt, ob die Übergangseingaben ausgetauscht werden.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: IAMTimelineTrans::GetSwapInputs-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrans.GetSwapInputs
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 566dbc54b30619c67ffb9d804e4854d51cae86d3688bda0b48eebfeb64cdb749
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119316300"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>IAMTimelineTrans::GetSwapInputs-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `GetSwapInputs` -Methode ruft einen Wert ab, der angibt, ob die Übergangseingaben ausgetauscht werden.

Standardmäßig erfolgt ein Übergang von der zusammengesetzten aller Schichten mit niedrigerer Priorität zu der Ebene, in der sich der Übergang befindet. Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich befindet, zurück zur zusammengesetzten Ebene mit niedrigerer Priorität wechselt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetSwapInputs(
   BOOL *pVal
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pVal* 
</dt> <dd>

Empfängt einen booleschen Wert. Wenn der Wert **FALSE** ist, wechselt der Übergang von der Zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Übergangsschicht. Wenn der Wert **TRUE** ist, verläuft der Übergang in die entgegengesetzte Richtung. Der Standardwert ist **FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

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

 

 




