---
description: Die SetRenderRange-Methode legt den Zeitraum auf der zu renderenden Zeitachse fest. Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ihnen werden keine Ressourcen zugeordnet.
ms.assetid: 2dcdca6b-2bae-4a27-bfbc-19a9b2ea633a
title: IRenderEngine::SetRenderRange-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetRenderRange
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0255b7806e2e2303bb2ca953fc5e59886480cbf3525d4de1bf1ef2fbd1388caf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952519"
---
# <a name="irenderenginesetrenderrange-method"></a>IRenderEngine::SetRenderRange-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `SetRenderRange` -Methode legt den Zeitraum auf der Zeitachse fest, der gerendert werden soll. Objekte, die sich außerhalb des angegebenen Bereichs befinden, werden nicht gerendert, und Ihnen werden keine Ressourcen zugeordnet.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetRenderRange(
   REFERENCE_TIME Start,
   REFERENCE_TIME Stop
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Start* 
</dt> <dd>

Startzeit in Einheiten von 100 Nanosekunden.

</dd> <dt>

*Beenden* 
</dt> <dd>

Beendigungszeit in Einheiten von 100 Nanosekunden.

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

 

 




