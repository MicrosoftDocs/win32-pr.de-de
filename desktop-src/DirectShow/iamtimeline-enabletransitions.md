---
description: Die enabletransitions-Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: 'Iamtimeline:: enabletransitions-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimeline.EnableTransitions
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: c05d3a00a57b8008789b83b16eee155eea974e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372327"
---
# <a name="iamtimelineenabletransitions-method"></a>Iamtimeline:: enabletransitions-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `EnableTransitions` Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse. Wenn Übergänge deaktiviert sind, werden Sie von den Rendering-Engines als Schnitte behandelt. Das heißt, die gerenderte Ausgabe springt sofort von einem Track zum nächsten. Der Standard Ausschneide Punkt liegt in der Mitte der Übergangs Dauer. Sie können den Ausschneide Punkt ändern, indem Sie die [**iamtimelinetrans:: setcutpoint**](iamtimelinetrans-setcutpoint.md) -Methode für den Übergang aufrufen. Deaktivierte Übergänge werden nicht aus der Zeitachse entfernt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fenabled* 
</dt> <dd>

Boolescher Wert, der angibt, ob Übergänge aktiviert oder deaktiviert werden sollen. **True** gibt an, dass Übergänge aktiviert sind. Der Wert **false** gibt an, dass Übergänge deaktiviert werden.

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

[**Iamtimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




