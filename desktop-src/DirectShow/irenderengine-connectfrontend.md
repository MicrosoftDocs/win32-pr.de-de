---
description: Die connectfrontend-Methode erstellt das Front-End des Filter Diagramms aus der aktuellen Zeitachse.
ms.assetid: ac484fd6-b88d-4c3a-bc4d-f118083d706d
title: 'Unenderengine:: connectfrontend-Methode (qedit. h)'
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
ms.openlocfilehash: 58ebd8e162f376b6ef942397e601139c46d8e4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371225"
---
# <a name="irenderengineconnectfrontend-method"></a>Unenderengine:: connectfrontend-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Mit der- `ConnectFrontEnd` Methode wird das Front-End des Filter Diagramms aus der aktuellen Zeitachse erstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ConnectFrontEnd();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                                  | Beschreibung                                                                    |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                         | Erfolg.<br/>                                                            |
| <dl> <dt>**S \_ Warnung \_ outputreset**</dt> </dl>          | Der Renderingbereich des Diagramms wurde gelöscht.<br/>                         |
| <dl> <dt>**E \_ invalidArg**</dt> </dl>                 | Es wurde keine Zeitachse für diese Renderingengine<br/>                             |
| <dl> <dt>**E \_ muss \_ Init \_ Renderer**</dt> </dl>       | Fehler beim Initialisieren der Rendering-Engine.<br/>                                 |
| <dl> <dt>**E- \_ Rendering- \_ Engine \_ ist \_ beschädigt.**</dt> </dl> | Fehler beim Vorgang, da das Projekt nicht erfolgreich gerendert wurde.<br/> |
| <dl> <dt>**E \_ unerwartet**</dt> </dl>                 | Unerwarteter Fehler.<br/>                                                   |
| <dl> <dt>**VFW \_ E \_ invalidmediatype**</dt> </dl>      | Ungültiger Medientyp.<br/>                                                 |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode erstellt nicht den renderingteil des Filter Diagramms. Die Anwendung muss die Ausgabe Pins auf dem Front-End mit den gewünschten renderingfiltern verbinden:

-   Um die Vorschau anzuzeigen, wenden Sie die Methode " [**irienderengine:: renderoutputpins**](irenderengine-renderoutputpins.md) " an.
-   Um eine Datei auszugeben, rufen Sie die Datei " [**faienderengine:: getgroupoutputpin**](irenderengine-getgroupoutputpin.md) " auf, um die Ausgabe-PIN für jede Gruppe abzurufen, und verbinden Sie dann die Pins mit einem Multiplexer-Filter.

Wenn Sie die einfache Renderingengine verwenden, erzeugen die Ausgabe Pins auf dem Front-End unkomprimierte Daten. Wenn Sie die Smart-Rendering-Engine verwenden, erzeugen die Ausgabe Pins komprimierte Daten.

Wenn Sie die Zeitachse nach dem Erstellen des Filter Diagramms ändern, müssen Sie erneut einen Aufruf `ConnectFrontEnd` zum erneuten Erstellen des Front-Ends durchsetzen. Die-Methode behält den Renderingbereich des Diagramms bei, wenn möglich. Wenn Sie jedoch eine Gruppe hinzufügen oder löschen oder die Reihenfolge der Gruppen ändern, `ConnectFrontEnd` Löscht den renderingteil, und die Anwendung muss Sie neu erstellen. Wenn die-Methode den renderingteil löscht, gibt Sie "S \_ Warn \_ outputreset" zurück.

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

[**Schnittstelle ""**](irenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




