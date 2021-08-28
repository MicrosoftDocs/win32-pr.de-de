---
description: Die ScrapIt-Methode verwirft das Filterdiagramm der Render-Engine und alle zugeordneten Objekte.
ms.assetid: b7470947-a661-4c08-8786-9298e5322e58
title: IRenderEngine::ScrapIt-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ScrapIt
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ab89f833167a0a974e860113d342b4486b9649ef3a4cc862a82e345e5d9cd090
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118153956"
---
# <a name="irenderenginescrapit-method"></a>IRenderEngine::ScrapIt-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `ScrapIt` -Methode verwirft das Filterdiagramm der Render-Engine und alle zugeordneten Objekte.

## <a name="syntax"></a>Syntax


```C++
HRESULT ScrapIt();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




