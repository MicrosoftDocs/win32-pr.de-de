---
description: Die RenderOutputPins-Methode erstellt den Vorschaubereich des Filterdiagramms.
ms.assetid: 66bcb698-cd85-4c22-bfef-2e51973958f1
title: IRenderEngine::RenderOutputPins-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.RenderOutputPins
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b81ea650d805c8ed2e42797f4dffdd9851eb3f072cff0abb05f54c4581684bea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818562"
---
# <a name="irenderenginerenderoutputpins-method"></a>IRenderEngine::RenderOutputPins-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `RenderOutputPins` -Methode erstellt den Vorschaubereich des Filterdiagramms.

## <a name="syntax"></a>Syntax


```C++
HRESULT RenderOutputPins();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **HRESULT-Werte** zurück. Folgende Werte sind möglich:



| Rückgabecode                                                                                                  | Beschreibung                                                                |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                        |
| <dl> <dt>**VFW \_ S AUDIO NOT RENDERED (VFW-S-AUDIO \_ NICHT \_ \_ GERENDERT)**</dt> </dl>  | Der Audiostream kann nicht wieder verwendet werden.<br/>                              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Ungültiges Argument.<br/>                                               |
| <dl> <dt>**DIE \_ \_ RENDER-ENGINE \_ IST \_ BESCHÄDIGT.**</dt> </dl> | Fehler beim Vorgang, weil das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                               |



 

## <a name="remarks"></a>Hinweise

Rufen Sie vor dem Aufrufen dieser Methode [**IRenderEngine::ConnectFrontEnd**](irenderengine-connectfrontend.md) auf, um das Front-End des Graphen zu erstellen. Um einen anderen Vorgang als die Vorschau durchzuführen, rufen Sie diese Methode nicht auf. Rufen Sie stattdessen [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) auf, um Zeiger auf die Ausgabepins zu erhalten.

Wenn auf dem Computer des Benutzers keine Soundkarte angezeigt wird, gibt diese Methode VFW \_ S \_ AUDIO NOT \_ \_ RENDERED zurück. In diesem Fall gibt es keine Audiovorschau, die Videovorschau ist jedoch nicht betroffen.

Wenn die Stecknadel aus einer Videogruppe besteht, erstellt diese Methode ein Videofenster. Der aufrufende Thread muss Nachrichten senden, z. B. um das Fenster zu verschieben oder auf Mausklicks im Clientbereich des Fensters zu reagieren.

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

 

 




