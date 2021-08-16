---
description: Die SetRenderRange2-Methode legt den Zeitraum auf der zu renderenden Zeitachse fest. Diese Methode entspricht IRenderEngine::SetRenderRange, nimmt jedoch Werte vom Typ double an.
ms.assetid: 07df97a8-aa83-405d-91a0-45cd99185588
title: IRenderEngine::SetRenderRange2-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange2
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a81d186ac648d2dcf617def0069c486b888e791c301cb45d4661e95b44dcbc25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397571"
---
# <a name="irenderenginesetrenderrange2-method"></a>IRenderEngine::SetRenderRange2-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetRenderRange2` -Methode legt den Zeitraum auf der Zeitachse fest, der gerendert werden soll. Diese Methode entspricht [**IRenderEngine::SetRenderRange,**](irenderengine-setrenderrange.md)nimmt jedoch Werte vom Typ **double** an.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderRange2(
   double Start,
   double Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Startzeit in Sekunden.

</dd> <dt>

*Beenden* 
</dt> <dd>

Beendigungszeit in Sekunden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**E \_ MUSS \_ RENDERER INIT \_**</dt> </dl> | Fehler beim Initialisieren der Render-Engine.<br/> |



 

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

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




