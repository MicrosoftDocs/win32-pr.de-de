---
description: Die ConnectFrontEnd-Methode erstellt das Front-End des Filterdiagramms aus der aktuellen Zeitachse.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: IRenderEngine::ConnectFrontEnd-Methode (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.ConnectFrontEnd
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: b7e0b00d467eb56dabaf6623f129ed1eb82945a1add63386b2b21fb01f725082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118154037"
---
# <a name="irenderengineconnectfrontend-method"></a>IRenderEngine::ConnectFrontEnd-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `ConnectFrontEnd` -Methode erstellt das Front-End des Filterdiagramms aus der aktuellen Zeitachse.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Rückgabewerte sind:



| Rückgabecode                                                                                                  | Beschreibung                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                            |
| <dl> <dt>**S \_ \_ WARNAUSGABERESET**</dt> </dl>          | Der Renderingteil des Diagramms wurde gelöscht.<br/>                         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                 | Für diese Render-Engine ist keine Zeitachse festgelegt.<br/>                             |
| <dl> <dt>**E \_ MUST \_ \_ INIT-RENDERER**</dt> </dl>       | Fehler beim Initialisieren der Render-Engine.<br/>                                 |
| <dl> <dt>**DIE \_ \_ RENDER-ENGINE \_ IST \_ BESCHÄDIGT.**</dt> </dl> | Fehler beim Vorgang, weil das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt> </dl>      | Ungültiger Medientyp.<br/>                                                 |



 

## <a name="remarks"></a>Hinweise

Diese Methode führt nicht zum Erstellen des Renderingbereichs des Filterdiagramms. Die Anwendung muss die Ausgabepins am Front-End mit den gewünschten Renderingfiltern verbinden:

-   Um eine Vorschau anzuzeigen, rufen Sie die [**IRenderEngine::RenderOutputPins-Methode**](irenderengine-renderoutputpins.md) auf.
-   Rufen Sie zum Ausgabe einer Datei [**IRenderEngine::GetGroupOutputPin**](irenderengine-getgroupoutputpin.md) auf, um den Ausgabepin für jede Gruppe abzurufen, und verbinden Sie dann die Stecknadeln mit einem Multiplexerfilter.

Wenn Sie die einfache Render-Engine verwenden, erzeugen die Ausgabepins am Front-End unkomprimierte Daten. Wenn Sie die intelligente Render-Engine verwenden, erzeugen die Ausgabepins komprimierte Daten.

Wenn Sie die Zeitachse nach dem Erstellen des Filterdiagramms ändern, müssen Sie erneut aufrufen, `ConnectFrontEnd` um das Front-End neu zu erstellen. Die -Methode behält nach Möglichkeit den Renderingteil des Diagramms bei. Wenn Sie jedoch eine Gruppe hinzufügen oder löschen oder die Reihenfolge der Gruppen ändern, wird der Renderingteil gelöscht, und Ihre Anwendung `ConnectFrontEnd` muss ihn neu erstellen. Wenn die Methode den Renderingteil löscht, gibt sie S \_ WARN \_ OUTPUTRESET zurück.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

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

 

 




