---
description: Die IAMTimelineTrack-Schnittstelle stellt Methoden zum Bearbeiten von Trackobjekten in DirectShow Editing Services (DES) bereit. Eine Spur enthält eine Liste von Quellen, die in der endgültigen Ausgabe gerendert werden.
ms.assetid: 42ac88f2-1361-413a-a9b0-95f5c32a7c3c
title: IAMTimelineTrack-Schnittstelle (Qedit.h)
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
ms.openlocfilehash: 9cc33facc22023d6e93c8dcfa3804d111d9c99f49be16d8271b09a7bf938b49e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119965080"
---
# <a name="iamtimelinetrack-interface"></a>IAMTimelineTrack-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IAMTimelineTrack` -Schnittstelle stellt Methoden zum Bearbeiten von *Trackobjekten* in [DirectShow Editing Services](directshow-editing-services.md) (DES) bereit.

Eine Spur enthält eine Liste von Quellen, die in der endgültigen Ausgabe gerendert werden. Quellen innerhalb derselben Spur dürfen sich nicht überschneiden. Videospuren können sowohl Auswirkungen als auch Übergänge haben. Die Render-Engine wendet Effekte an, bevor sie Übergänge anwendet. Audiospuren können Auswirkungen haben, aber keine Übergänge. Weitere Informationen finden Sie unter [Das Zeitachsenmodell.](the-timeline-model.md)

Um ein Trackobjekt zu erstellen, rufen [**Sie IAMTimeline::CreateEmptyNode**](iamtimeline-createemptynode.md) mit dem Wert TIMELINE \_ MAJOR TYPE TRACK \_ \_ auf. Sie können den zurückgegebenen **IAMTimelineObj-Zeiger** für die `IAMTimelineTrack` Schnittstelle abfragen.

## <a name="members"></a>Member

Die **IAMTimelineTrack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMTimelineTrack** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMTimelineTrack-Schnittstelle** verfügt über diese Methoden.



| Methode                                                          | Beschreibung                                                                                                                                          |
|:----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AreYouBlank**](iamtimelinetrack-areyoublank.md)             | Bestimmt, ob die Spur leer ist (enthält keine Quellobjekte).<br/>                                                                       |
| [**GetNextSrc**](iamtimelinetrack-getnextsrc.md)               | Durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später angezeigt wird.<br/>                                                       |
| [**GetNextSrc2**](iamtimelinetrack-getnextsrc2.md)             | Durchsucht die Spur nach der nächsten Quelle, die zum angegebenen Zeitpunkt oder später mit dem angegebenen als [**REFTIME-Wert**](reftime.md) angezeigt wird.<br/> |
| [**GetNextSrcEx**](iamtimelinetrack-getnextsrcex.md)           | Ruft die nächste Quelle nach der angegebenen Quelle ab.<br/>                                                                                     |
| [**GetSourcesCount**](iamtimelinetrack-getsourcescount.md)     | Ruft die Anzahl der Quellen in der Spur ab.<br/>                                                                                             |
| [**GetSrcAtTime**](iamtimelinetrack-getsrcattime.md)           | Ruft das Quellobjekt ab, das der angegebenen Zeit gemäß den angegebenen Begrenzungsbedingungen am nächsten ist.<br/>                                |
| [**GetSrcAtTime2**](iamtimelinetrack-getsrcattime2.md)         | Ruft das Quellobjekt ab, das der angegebenen Zeit am nächsten ist, angegeben als [**REFTIME-Wert.**](reftime.md)<br/>                                   |
| [**InsertSpace**](iamtimelinetrack-insertspace.md)             | Teilt alle Objekte auf, die zum angegebenen Zeitpunkt vorhanden sind, und fügt Leerzeichen zwischen ihnen ein.<br/>                                                       |
| [**InsertSpace2**](iamtimelinetrack-insertspace2.md)           | Teilt alle Objekte, die zum angegebenen Zeitpunkt vorhanden sind, und fügt mithilfe von [**REFTIME-Werten**](reftime.md) Leerzeichen zwischen ihnen ein.<br/>              |
| [**MoveEverythingBy**](iamtimelinetrack-moveeverythingby.md)   | Wird nicht unterstützt.<br/>                                                                                                                            |
| [**MoveEverythingBy2**](iamtimelinetrack-moveeverythingby2.md) | Wird nicht unterstützt.<br/>                                                                                                                            |
| [**SrcAdd**](iamtimelinetrack-srcadd.md)                       | Fügt der Spur eine Quelle hinzu.<br/>                                                                                                               |
| [**ZeroBetween**](iamtimelinetrack-zerobetween.md)             | Entfernt alles aus der Spur zwischen den angegebenen Zeiten.<br/>                                                                            |
| [**ZeroBetween2**](iamtimelinetrack-zerobetween2.md)           | Entfernt alles aus der Spur zwischen den angegebenen Zeiten, angegeben als [**REFTIME-Werte.**](reftime.md)<br/>                                |



 

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



 

 
