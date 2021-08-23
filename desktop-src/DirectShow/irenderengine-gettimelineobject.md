---
description: Die GetTimelineObject-Methode ruft die Zeitachse ab, die die Render-Engine derzeit verwendet.
ms.assetid: 74398f85-07b2-42fa-bb4f-a1e7e1669e3f
title: IRenderEngine::GetTimelineObject-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.GetTimelineObject
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 0c21868dc705a5c9f3b40649540fcaadb1f9219a7443d58c59964606cb7ed7d0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119823360"
---
# <a name="irenderenginegettimelineobject-method"></a>IRenderEngine::GetTimelineObject-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `GetTimelineObject` -Methode ruft die Zeitachse ab, die die Render-Engine derzeit verwendet.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTimelineObject(
  [out] IAMTimeline **ppTimeline
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppTimeline* \[ out\]
</dt> <dd>

Empfängt einen Zeiger auf die [**IAMTimeline-Schnittstelle der Zeitachse.**](iamtimeline.md) Sie empfängt den Wert **NULL,** wenn keine Zeitachse vorkommt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                                            | Beschreibung                                    |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                   | Erfolg.<br/>                            |
| <dl> <dt>**\_E-ZEIGER**</dt> </dl>              | Ungültiger Zeiger.<br/>                    |
| <dl> <dt>**E \_ MUST \_ \_ INIT-RENDERER**</dt> </dl> | Fehler beim Initialisieren der Render-Engine.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn bei der Rückgabe der Wert *\* von ppTimeline* nicht **NULL** ist, verfügt die **IAMTimeline-Schnittstelle** über einen ausstehenden Verweiszähler. Stellen Sie sicher, dass Sie die -Schnittstelle wieder frei geben, wenn Sie sie nicht mehr verwenden.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




