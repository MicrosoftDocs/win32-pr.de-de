---
description: Die SetTimelineObject-Methode legt die Zeitachse für die zu verwendende Render-Engine fest.
ms.assetid: 9b60b148-9768-43ba-a986-a96838c4d2bb
title: IRenderEngine::SetTimelineObject-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: bb7862f247181d9aed6123e90507ed119594306a8d84be59ddd5204a816b33fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952489"
---
# <a name="irenderenginesettimelineobject-method"></a>IRenderEngine::SetTimelineObject-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetTimelineObject` -Methode legt die Zeitachse für die zu verwendende Render-Engine fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetTimelineObject(
   IAMTimeline *pTimeline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pTimeline* 
</dt> <dd>

Zeiger auf die [**IAMTimeline-Schnittstelle**](iamtimeline.md) des Zeitachsenobjekts.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ MUSS \_ RENDERER INIT \_**</dt> </dl> | Fehler beim Initialisieren der Render-Engine.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>          | Nicht genügend Arbeitsspeicher.<br/>                |
| <dl> <dt>**E \_ POINTER**</dt> </dl>              | Ungültiger Zeiger.<br/>                    |



 

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




