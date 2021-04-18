---
description: Die iamtimelinetrack-Schnittstelle stellt Methoden zum Bearbeiten von Track-Objekten in DirectShow-Bearbeitungs Diensten bereit. Eine Spur enthält eine Liste der Quellen, die in der endgültigen Ausgabe gerendert werden.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: Iamtimelinetrack-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineTrack
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 71003694d33b33980fb262f06f6b2e7aa55a70d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371784"
---
# <a name="iamtimelinetrack-interface"></a>Iamtimelinetrack-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMTimelineTrack` Schnittstelle stellt Methoden zum Bearbeiten von *Track* -Objekten in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.

Eine Spur enthält eine Liste der Quellen, die in der endgültigen Ausgabe gerendert werden. Quellen innerhalb desselben Titels können sich möglicherweise nicht überlappen. Video Spuren können sowohl Effekte als auch Übergänge aufweisen. Die Renderingengine wendet die Auswirkungen an, bevor Übergänge angewendet werden. Audiospuren können Effekte, aber keine Übergänge enthalten. Weitere Informationen finden Sie [im Zeitachsen Modell](the-timeline-model.md).

Um ein Track-Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline \_ Major \_ Type \_ Track auf. Sie können den zurückgegebenen **iamtimelineobj** -Zeiger für die- `IAMTimelineTrack` Schnittstelle Abfragen.

## <a name="members"></a>Member

Die **iamtimelinetrack** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinetrack** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinetrack** -Schnittstelle verfügt über diese Methoden.



| Methode                                                          | BESCHREIBUNG                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Areyoublank**](iamtimelinetrack-areyoublank.md)             | Bestimmt, ob der Titel leer ist (enthält keine Quell Objekte).<br/>                                                                       |
| [**Getnexnerrc**](iamtimelinetrack-getnextsrc.md)               | Durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Durchsucht den Titel nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird, wobei die angegebene als [**ref**](reftime.md) -Wert angegeben wird.<br/> |
| [**Getnexzrcex**](iamtimelinetrack-getnextsrcex.md)           | Ruft die nächste Quelle nach der angegebenen Quelle ab.<br/>                                                                                     |
| [**Getsourcescount**](iamtimelinetrack-getsourcescount.md)     | Ruft die Anzahl der Quellen in der Spur ab.<br/>                                                                                             |
| [**Gezr\time**](iamtimelinetrack-getsrcattime.md)           | Ruft das Quell Objekt, das dem angegebenen Zeitpunkt am nächsten liegt, gemäß den angegebenen begrenzungsbedingungen ab.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Ruft das Quell Objekt ab, das dem angegebenen Zeitpunkt am nächsten liegt, das als [**reftime**](reftime.md) -Wert angegeben wird.<br/>                                   |
| [**Insertspace**](iamtimelinetrack-insertspace.md)             | Teilt alle-Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen diesen ein.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Teilt alle Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt mithilfe von [**ref Time**](reftime.md) -Werten Leerzeichen zwischen diesen ein.<br/>              |
| [**"Muveeverythingby"**](iamtimelinetrack-moveeverythingby.md)   | Wird nicht unterstützt.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Wird nicht unterstützt.<br/>                                                                                                                            |
| [**Srcadd**](iamtimelinetrack-srcadd.md)                       | Fügt der Spur eine Quelle hinzu.<br/>                                                                                                               |
| [**NULL**](iamtimelinetrack-zerobetween.md)             | Entfernt alle Elemente aus der Spur zwischen den angegebenen Uhrzeiten.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Entfernt alle Elemente aus der Spur zwischen den angegebenen Zeiten, die als [**ref-Zeit**](reftime.md) Werte angegeben werden.<br/>                                |



 

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



 

 
