---
description: Die gezwapinputs-Methode ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.
ms.assetid: 84cb5c3d-7c3a-4c35-aac7-97d812d99a38
title: 'Iamtimelinetrans:: gezwapinputs-Methode (qedit. h)'
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
ms.openlocfilehash: a2acdff1007bd26773ce495d024676632eee1767
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364538"
---
# <a name="iamtimelinetransgetswapinputs-method"></a>Iamtimelinetrans:: gezwapinputs-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `GetSwapInputs` Methode ruft einen Wert ab, der angibt, ob die Übergangs Eingaben ausgetauscht werden.

Standardmäßig wird ein Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zu der Ebene, auf der sich der Übergang befindet, durchläuft. Sie können diesen Fortschritt umkehren, sodass der Übergang von der Ebene, in der er sich wieder auf die Zusammensetzung der Ebenen mit niedrigerer Priorität befindet, erfolgt.

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

Empfängt einen booleschen Wert. Wenn der Wert **false** ist, wird der Übergang von der zusammengesetzten aller Ebenen mit niedrigerer Priorität zur Übergangs Schicht geleitet. Wenn der Wert **true** ist, wird der Übergang in die entgegengesetzte Richtung geleitet. Der Standardwert ist **FALSE**.

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

[**Iamtimelinetrans-Schnittstelle**](iamtimelinetrans.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




