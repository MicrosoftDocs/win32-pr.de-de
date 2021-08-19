---
description: Die EnableTransitions-Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse.
ms.assetid: 8610337a-a247-44f0-8674-3cbc43f636d5
title: IAMTimeline::EnableTransitions-Methode (Qedit.h)
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
ms.openlocfilehash: 9356ac53488f68e54a05a85e8e287850138ee131f80dd3bb45b81cf606b5a351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401071"
---
# <a name="iamtimelineenabletransitions-method"></a>IAMTimeline::EnableTransitions-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `EnableTransitions` -Methode aktiviert oder deaktiviert alle Übergänge in der Zeitachse. Wenn Übergänge deaktiviert sind, werden sie von den Render-Engines als Schnitte behandelt. Das heißt, die gerenderte Ausgabe springt sofort von einer Spur zur nächsten. Der Standardmäßige Schnittpunkt befindet sich in der Mitte der Dauer des Übergangs. Sie können den Schnittpunkt ändern, indem Sie beim Übergang die [**IAMTimelineTrans::SetCutPoint-Methode**](iamtimelinetrans-setcutpoint.md) aufrufen. Deaktivierte Übergänge werden nicht aus der Zeitachse entfernt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EnableTransitions(
   BOOL fEnabled
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*fEnabled* 
</dt> <dd>

Boolescher Wert, der angibt, ob Übergänge aktiviert oder deaktiviert werden sollen. True gibt an, dass Übergänge aktiviert sind. False gibt an, dass Übergänge deaktiviert sind.

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

[**IAMTimeline-Schnittstelle**](iamtimeline.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




